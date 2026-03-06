# Server-Side Tracking Architecture Guide

> Architecture and implementation guide for paid traffic professionals building server-side tracking infrastructure.

---

## 1. Architecture Overview

### Why Server-Side Tracking?

| Challenge | Client-Side Impact | Server-Side Solution |
|-----------|-------------------|---------------------|
| Ad blockers | 25-40% of events blocked | Events sent server-to-server; not blockable |
| iOS ITP | Cookies limited to 7 days (24h for classified) | Server-set first-party cookies persist longer |
| Browser privacy | Third-party cookies dying | First-party domain tracking |
| Page speed | Multiple scripts slow pages | One tag sends to server; server fans out |
| Data control | PII sent directly to vendors | Server filters/transforms data before sending |
| Reliability | JS errors, tab closures lose events | Server queues ensure delivery |

### The Hybrid Model (Recommended)

Run both client-side and server-side tracking for maximum coverage:

```
┌─────────────┐     ┌─────────────────────┐     ┌──────────────┐
│   Browser    │────>│   Your Server /     │────>│ Meta CAPI    │
│  (Pixel/JS)  │     │   Tracking Endpoint │────>│ Google Ads   │
│              │     │                     │────>│ TikTok API   │
│  Pixel fires │     │  Receives, enriches,│────>│ GA4          │
│  for backup  │     │  deduplicates, sends│────>│ Data Warehouse│
└─────────────┘     └─────────────────────┘     └──────────────┘
```

---

## 2. Architecture Patterns

### Pattern 1: GTM Server-Side Container

**Best for**: Most advertisers; balances flexibility and simplicity.

```
Browser                              Server
┌──────────────────┐                ┌──────────────────────────┐
│ GTM Web Container│                │ GTM Server Container     │
│                  │   HTTPS POST   │ (track.yourdomain.com)   │
│ GA4 Config Tag   │───────────────>│                          │
│ (server URL set) │                │ ┌─ GA4 Client ─────────┐│
│                  │                │ │  Parses GA4 hits      ││
│ Also fires:      │                │ │  ├─ GA4 Tag           ││
│ - Meta Pixel     │                │ │  ├─ Meta CAPI Tag     ││
│ - Browser events │                │ │  ├─ Google Ads Tag    ││
│   (for dedup)    │                │ │  └─ TikTok API Tag    ││
└──────────────────┘                │ └───────────────────────┘│
                                    └──────────────────────────┘
```

**Hosting options**:
| Provider | Cost | Complexity | Performance |
|----------|------|------------|-------------|
| Google Cloud Run | $30-150/mo | Medium | Excellent |
| Stape.io | $20-100/mo | Low | Good |
| Addingwell | $50-200/mo | Low | Good |
| AWS (Lambda/ECS) | $20-100/mo | High | Excellent |
| Custom VPS | $20-80/mo | High | Good |

### Pattern 2: Direct API Integration

**Best for**: Custom platforms, high-volume advertisers with engineering resources.

```
┌──────────────┐    ┌─────────────────┐    ┌──────────────┐
│ Your Website │───>│ Your Backend    │───>│ Platform APIs│
│              │    │                 │    │              │
│ Form submit  │    │ Process event   │    │ Meta CAPI    │
│ Purchase     │    │ Hash PII        │    │ Google API   │
│ Page view    │    │ Enrich data     │    │ TikTok API   │
│              │    │ Send to APIs    │    │              │
└──────────────┘    └─────────────────┘    └──────────────┘
```

**Implementation example (Node.js)**:
```javascript
// Simplified server-side event handler
app.post('/api/track', async (req, res) => {
  const { event, userData, eventData } = req.body;

  // Hash PII
  const hashedEmail = sha256(userData.email.toLowerCase().trim());
  const hashedPhone = sha256(userData.phone.replace(/\D/g, ''));

  // Send to multiple platforms in parallel
  await Promise.all([
    sendToMetaCAPI(event, hashedEmail, hashedPhone, eventData),
    sendToGoogleAds(event, userData.gclid, eventData),
    sendToTikTokEvents(event, hashedEmail, hashedPhone, eventData),
    sendToGA4(event, eventData)
  ]);

  res.json({ status: 'ok' });
});
```

### Pattern 3: CDP/Event Pipeline

**Best for**: Enterprise advertisers with data infrastructure.

```
┌──────────┐    ┌─────────────┐    ┌──────────────┐    ┌────────────┐
│ Website  │───>│ Segment /   │───>│ Destinations │───>│ Platforms  │
│ App      │    │ Rudderstack │    │              │    │            │
│ CRM      │    │ mParticle   │    │ Meta CAPI    │    │ Meta       │
│ POS      │    │             │    │ Google Ads   │    │ Google     │
│          │    │ Unified     │    │ TikTok API   │    │ TikTok     │
│          │    │ Event Bus   │    │ Warehouse    │    │ BigQuery   │
└──────────┘    └─────────────┘    └──────────────┘    └────────────┘
```

**CDPs with server-side ad platform integrations**:
- Segment: Meta CAPI, Google Ads, TikTok
- Rudderstack: Meta CAPI, Google Ads, TikTok (open-source option available)
- mParticle: Meta CAPI, Google Ads
- Tealium: Meta CAPI, Google Ads, TikTok

### Pattern 4: Webhook-Based (E-commerce Platforms)

**Best for**: Shopify, WooCommerce, and other platforms with webhook support.

```
┌──────────────┐    ┌─────────────────┐    ┌──────────────┐
│ Shopify      │───>│ Webhook Handler │───>│ Platform APIs│
│              │    │ (Cloudflare     │    │              │
│ Order Created│    │  Worker / AWS   │    │ Meta CAPI    │
│ Checkout     │    │  Lambda / etc.) │    │ Google Ads   │
│ Cart Updated │    │                 │    │ TikTok API   │
└──────────────┘    └─────────────────┘    └──────────────┘
```

---

## 3. First-Party Domain Setup

### Why First-Party Domain Matters

Using a subdomain of your main site (e.g., `track.yourdomain.com`) instead of a third-party domain:

- Cookies set by your subdomain are treated as first-party (not blocked by ITP)
- Ad blockers less likely to block requests to your own domain
- Users trust requests to your domain more
- CORS issues eliminated

### Setup Steps

1. **Create DNS record**: Point `track.yourdomain.com` to your server container
2. **SSL certificate**: Ensure HTTPS (required)
3. **Configure server container**: Accept requests on the custom domain
4. **Update browser tags**: Point data collection to `track.yourdomain.com`

### DNS Configuration Examples

**Google Cloud Run**:
```
track.yourdomain.com  CNAME  your-service-xxxxxxxx-uc.a.run.app
```

**Stape.io**:
```
track.yourdomain.com  CNAME  your-container.stape.io
```

**Custom server**:
```
track.yourdomain.com  A  203.0.113.10  (your server IP)
```

---

## 4. Cookie Management

### Server-Set First-Party Cookies

Server-set cookies persist longer than JavaScript-set cookies under ITP:

```
HTTP Response Header:
Set-Cookie: _tracking_id=abc123; Domain=.yourdomain.com; Path=/; Max-Age=31536000; Secure; HttpOnly; SameSite=Lax
```

| Cookie Attribute | Recommended Value | Purpose |
|-----------------|-------------------|---------|
| `Domain` | `.yourdomain.com` | First-party scope |
| `Path` | `/` | Available site-wide |
| `Max-Age` | `31536000` (1 year) | Persistence |
| `Secure` | Required | HTTPS only |
| `HttpOnly` | Recommended | Prevents JS access (security) |
| `SameSite` | `Lax` | Cross-site protection |

### Key Cookies to Manage

| Cookie | Source | Purpose | Server-Side Handling |
|--------|--------|---------|---------------------|
| `_fbp` | Meta Pixel | Browser ID for matching | Read and pass to CAPI |
| `_fbc` | Meta Pixel | Click ID from `fbclid` param | Read and pass to CAPI |
| `_ttp` | TikTok Pixel | TikTok browser ID | Read and pass to Events API |
| `_ga` | GA4 | Client ID | Read and pass to GA4 server |
| `_gclid` | Google Ads | Click ID | Capture from URL, store as cookie |
| `_tracking_id` | Your server | Cross-session user ID | Generate and set server-side |

### Cookie Sync Strategy

```javascript
// On your server endpoint, read cookies from the incoming request
function extractTrackingCookies(req) {
  return {
    fbp: req.cookies['_fbp'],
    fbc: req.cookies['_fbc'],
    ttp: req.cookies['_ttp'],
    ga: req.cookies['_ga'],
    gclid: req.cookies['_gclid'] || req.query.gclid,
    internalId: req.cookies['_tracking_id']
  };
}
```

---

## 5. Data Enrichment Layer

Server-side tracking enables data enrichment before sending to platforms:

### Enrichment Opportunities

| Data Point | Source | Benefit |
|-----------|--------|---------|
| Customer LTV | CRM/Database | Value-based optimization |
| Customer segment | CRM | Audience quality signals |
| Order margin | ERP/Backend | Profit-based ROAS |
| Lead score | CRM/Scoring system | Quality-based lead optimization |
| Offline conversion status | CRM | Close the attribution loop |
| Geo data | IP lookup | Refined location targeting |
| Device data | User-Agent parsing | Device-level insights |

### Example: Enriched Purchase Event

```javascript
async function enrichPurchaseEvent(rawEvent) {
  // Raw event from browser
  const { orderId, email, value } = rawEvent;

  // Enrich from database
  const customer = await db.getCustomerByEmail(email);
  const order = await db.getOrderById(orderId);

  return {
    event_name: 'Purchase',
    value: order.grossProfit,          // Send profit, not revenue
    currency: 'USD',
    transaction_id: orderId,
    user_data: {
      em: sha256(email),
      customer_ltv: customer.lifetimeValue,
      customer_segment: customer.segment, // 'high_value', 'at_risk', etc.
      first_purchase_date: customer.firstPurchaseDate,
      purchase_count: customer.totalOrders
    },
    custom_data: {
      product_margin: order.marginPercentage,
      new_vs_returning: customer.totalOrders === 1 ? 'new' : 'returning',
      payment_method: order.paymentMethod,
      coupon_used: order.couponCode || 'none'
    }
  };
}
```

---

## 6. Event Queue & Reliability

### Why Queuing Matters

API calls can fail due to rate limits, network issues, or platform outages. A queue ensures no events are lost.

### Queue Architecture

```
┌──────────┐    ┌───────────┐    ┌─────────┐    ┌──────────────┐
│ Incoming │───>│ Event     │───>│ Worker  │───>│ Platform API │
│ Events   │    │ Queue     │    │ Process │    │              │
│          │    │ (Redis /  │    │         │    │ Success: ACK │
│          │    │  SQS /    │    │ Retry   │    │ Failure: DLQ │
│          │    │  Pub/Sub) │    │ Logic   │    │              │
└──────────┘    └───────────┘    └─────────┘    └──────────────┘
```

### Retry Strategy

```javascript
const RETRY_CONFIG = {
  maxRetries: 5,
  baseDelay: 1000,      // 1 second
  maxDelay: 60000,       // 60 seconds
  backoffMultiplier: 2   // Exponential backoff
};

async function sendWithRetry(event, platform) {
  for (let attempt = 0; attempt < RETRY_CONFIG.maxRetries; attempt++) {
    try {
      const response = await sendToAPI(event, platform);
      if (response.ok) return response;
    } catch (error) {
      const delay = Math.min(
        RETRY_CONFIG.baseDelay * Math.pow(RETRY_CONFIG.backoffMultiplier, attempt),
        RETRY_CONFIG.maxDelay
      );
      await sleep(delay);
    }
  }
  // After max retries, send to dead letter queue
  await deadLetterQueue.push({ event, platform, timestamp: Date.now() });
}
```

### Rate Limits by Platform

| Platform | Rate Limit | Batch Size | Recommendation |
|----------|-----------|------------|----------------|
| Meta CAPI | 2,000 events/sec per pixel | Up to 1,000 events per request | Batch events; send every 5-10 seconds |
| TikTok Events API | 500 events/sec | Up to 50 events per request | Batch events; send every 10 seconds |
| Google Ads API | Varies by method | 2,000 operations per request | Batch offline conversions daily |
| GA4 Measurement Protocol | 25 events per request | 25 events | Batch in groups of 25 |

---

## 7. Data Privacy & Filtering

### PII Filtering Pipeline

```
Raw Event Data
    │
    ├── Hash PII fields (email, phone, name)
    │
    ├── Strip unnecessary PII (credit card, SSN - never needed)
    │
    ├── Apply consent rules (check user consent status)
    │
    ├── Apply geo rules (GDPR regions get additional filtering)
    │
    └── Forward cleaned data to platforms
```

### Server-Side Consent Enforcement

```javascript
function applyConsent(event, userConsent) {
  if (!userConsent.advertising) {
    // No advertising consent: don't send to ad platforms
    return {
      sendToMeta: false,
      sendToGoogle: false,
      sendToTikTok: false,
      sendToGA4: userConsent.analytics  // Only if analytics consent
    };
  }

  if (!userConsent.adUserData) {
    // Has advertising but not user data consent
    // Send event but strip user identifiers
    event.user_data = {
      client_ip_address: event.user_data.client_ip_address,
      client_user_agent: event.user_data.client_user_agent
      // Remove email, phone, name, etc.
    };
  }

  return {
    sendToMeta: true,
    sendToGoogle: true,
    sendToTikTok: true,
    sendToGA4: true
  };
}
```

---

## 8. Monitoring & Alerting

### Key Metrics to Monitor

| Metric | Normal Range | Alert Threshold |
|--------|-------------|-----------------|
| Events received/minute | Baseline +/- 20% | >50% drop |
| API success rate | >99% | <95% |
| API latency (P95) | <500ms | >2000ms |
| Queue depth | <1000 events | >10,000 events |
| Event match quality (Meta) | 6-10 | <5 |
| Deduplication rate | 10-30% | >50% (likely double-firing) |
| Consent rate (EU) | 40-70% | <30% (CMP issue) |

### Alerting Rules

Set up alerts for:
1. **Event volume drop > 50%**: Possible tracking code removal or site issue
2. **API errors > 5%**: Platform API issues or auth token expiration
3. **Queue depth growing**: Processing falling behind; scale workers
4. **Zero events from a source**: Tag removed, site down, or code error
5. **Match quality drop**: User data parameters missing from events

### Monitoring Stack Recommendations

| Component | Options |
|-----------|---------|
| Metrics collection | Prometheus, CloudWatch, Datadog |
| Dashboard | Grafana, CloudWatch Dashboards, Datadog |
| Alerting | PagerDuty, Opsgenie, Slack webhooks |
| Logging | CloudWatch Logs, Elasticsearch, Loki |

---

## 9. Cost Optimization

### Server Costs by Scale

| Monthly Events | GTM Server (Cloud Run) | Custom Server | CDP (Segment) |
|---------------|----------------------|---------------|---------------|
| 100K | $20-40/mo | $20-30/mo | $120/mo |
| 1M | $40-80/mo | $40-60/mo | $120/mo |
| 10M | $100-200/mo | $80-150/mo | $120-500/mo |
| 100M | $500-1,000/mo | $300-600/mo | Custom pricing |

### Cost Reduction Strategies

1. **Batch API calls**: Reduce number of HTTP requests
2. **Auto-scaling**: Scale down during off-peak hours
3. **Event sampling**: For analytics (not conversions), sample high-volume events
4. **Regional deployment**: Deploy in the region closest to your users
5. **Caching**: Cache frequently looked-up data (customer segments, product data)

---

## 10. Migration Checklist

### Moving from Client-Only to Hybrid Tracking

**Phase 1: Setup (Week 1-2)**
- [ ] Choose architecture pattern (GTM Server-Side, Direct API, CDP)
- [ ] Provision server infrastructure
- [ ] Set up first-party domain (DNS, SSL)
- [ ] Configure server container or API endpoints
- [ ] Implement event deduplication IDs in browser pixel/tags

**Phase 2: Implementation (Week 2-4)**
- [ ] Configure server-side tags for each platform (Meta, Google, TikTok)
- [ ] Implement data enrichment layer
- [ ] Set up consent enforcement on server side
- [ ] Configure PII hashing and filtering
- [ ] Implement event queue and retry logic

**Phase 3: Testing (Week 4-5)**
- [ ] Test each event type end-to-end
- [ ] Verify deduplication (no double-counting)
- [ ] Test with ad blockers enabled (server events should still fire)
- [ ] Test consent flow (EU and non-EU scenarios)
- [ ] Verify data appears correctly in all platforms
- [ ] Load test at expected peak traffic

**Phase 4: Launch & Monitor (Week 5-6)**
- [ ] Enable server-side tracking in production
- [ ] Monitor event volumes for 7 days (compare to baseline)
- [ ] Verify match rates are improving
- [ ] Check platform reporting for data consistency
- [ ] Set up ongoing monitoring and alerting

**Phase 5: Optimization (Ongoing)**
- [ ] Tune event batching and timing
- [ ] Add additional user data parameters to improve match rates
- [ ] Build data enrichment from CRM/backend systems
- [ ] Regularly audit data quality and consent compliance
- [ ] Optimize server costs based on actual usage

---

*Last updated: March 2026. Server-side tracking is a rapidly evolving field. Architecture decisions should factor in your team's technical capabilities, budget, and the number of advertising platforms in your stack.*
