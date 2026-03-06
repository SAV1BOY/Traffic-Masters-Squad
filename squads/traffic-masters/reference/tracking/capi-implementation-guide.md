# Conversions API (CAPI) Implementation Guide

> Technical reference for implementing server-side conversion tracking across Meta, TikTok, and Google platforms.

---

## 1. Why Server-Side Tracking?

### The Problem with Browser-Only Tracking
- **Ad blockers**: 25-40% of users block tracking scripts
- **iOS 14+ ATT**: ~75% of iOS users opt out of tracking
- **Browser restrictions**: Safari ITP limits cookie life to 7 days (24 hours for classified domains); Firefox ETP blocks third-party cookies
- **Chrome Privacy Sandbox**: Third-party cookie deprecation (phased rollout)
- **Page load failures**: Slow pages, navigation away before pixel fires

### Server-Side Benefits
- Not blocked by ad blockers or browser privacy features
- More reliable data delivery
- Better data quality (server-controlled parameters)
- Improved match rates (more user data available server-side)
- Longer cookie persistence (first-party server-set cookies)
- Greater control over what data is shared

---

## 2. Meta Conversions API (CAPI)

### Architecture Options

**Option A: Direct API Integration**
```
User Action -> Your Server -> Meta CAPI Endpoint
                           -> Browser Pixel (for redundancy)
```

**Option B: Partner Integration**
```
User Action -> Your Platform (Shopify, WooCommerce, etc.) -> Meta CAPI
```

**Option C: GTM Server-Side**
```
User Action -> Browser GTM -> Server GTM Container -> Meta CAPI
                           -> Browser Pixel (for redundancy)
```

### API Endpoint

```
POST https://graph.facebook.com/v18.0/{PIXEL_ID}/events
```

### Request Structure

```json
{
  "data": [
    {
      "event_name": "Purchase",
      "event_time": 1709726400,
      "event_id": "purchase_ORD123_1709726400",
      "event_source_url": "https://example.com/thank-you",
      "action_source": "website",
      "user_data": {
        "em": ["309a0a5c3e211326ae75ca18196d301a9bdbd1a882a4d2569511033da23f0abd"],
        "ph": ["254aa248acb47dd654ca3ea53f48c2c26d641571e29e1f3b183be7d0f9e53c14"],
        "fn": ["a8cfcd74832004951b4408cdb0a5dbcd8c7e52d43f7fe244bf720582e05241da"],
        "ln": ["2e99758548972a8e8822ad47fa1017ff72f06f3ff6a016851f45c398732bc50c"],
        "ct": ["1b16b1df538ba12dc3f97edbb85caa7050d46c148134290feba80f8236c83db9"],
        "st": ["36c3132d3bfee41cf1e3d70fed548ceb00e8a31c7a32dbc0d1beca6bf3971e02"],
        "zp": ["e77e434c3e3bbc85fd19a5e5b3b80e00e6c216d6d4f3ece3c22c1c67e5e5b866"],
        "country": ["9b202ecbc6d45c6d8901d989a918878397a3eb9d00e8f48022fc051b19d21a1d"],
        "external_id": ["abcd1234"],
        "client_ip_address": "123.456.78.90",
        "client_user_agent": "Mozilla/5.0...",
        "fbc": "fb.1.1709726400.IwAR...",
        "fbp": "_fbp cookie value"
      },
      "custom_data": {
        "value": 49.99,
        "currency": "USD",
        "content_ids": ["SKU123"],
        "content_type": "product",
        "order_id": "ORD-12345",
        "num_items": 1
      }
    }
  ],
  "access_token": "YOUR_ACCESS_TOKEN"
}
```

### Key Parameters Explained

| Parameter | Description | Impact on Match Rate |
|-----------|-------------|---------------------|
| `em` | SHA256 hashed email | HIGH - Primary matching signal |
| `ph` | SHA256 hashed phone | HIGH |
| `fn`, `ln` | SHA256 hashed first/last name | MEDIUM |
| `external_id` | Your internal user ID | MEDIUM - Enables cross-device matching |
| `fbc` | Facebook click ID cookie (`_fbc`) | HIGH - Links to ad click |
| `fbp` | Facebook browser ID cookie (`_fbp`) | HIGH - Links to browser session |
| `client_ip_address` | User's IP address | MEDIUM |
| `client_user_agent` | User's browser user agent | LOW-MEDIUM |
| `ct`, `st`, `zp`, `country` | Hashed location data | LOW |

### Event Deduplication

Send the same `event_id` from both browser pixel and CAPI:

**Browser Pixel**:
```javascript
fbq('track', 'Purchase', {value: 49.99, currency: 'USD'}, {eventID: 'purchase_ORD123'});
```

**Server CAPI**:
```json
{
  "event_name": "Purchase",
  "event_id": "purchase_ORD123",
  ...
}
```

Meta deduplicates events with matching `event_name` + `event_id` within 48 hours.

### Hashing Requirements (Meta)
- Use SHA256
- Lowercase and trim all values before hashing
- Phone numbers: Remove all non-numeric characters, include country code
- Email: Lowercase, trim whitespace
- Names: Lowercase, remove special characters

```python
import hashlib

def hash_for_meta(value):
    """Hash a value for Meta CAPI"""
    cleaned = str(value).lower().strip()
    return hashlib.sha256(cleaned.encode('utf-8')).hexdigest()

# Example
hashed_email = hash_for_meta("User@Example.com")
# Result: same as hash of "user@example.com"
```

---

## 3. TikTok Events API

### API Endpoint

```
POST https://business-api.tiktok.com/open_api/v1.3/event/track/
```

### Request Structure

```json
{
  "event_source": "web",
  "event_source_id": "PIXEL_ID",
  "data": [
    {
      "event": "CompletePayment",
      "event_time": 1709726400,
      "event_id": "purchase_ORD123",
      "page": {
        "url": "https://example.com/thank-you",
        "referrer": "https://example.com/checkout"
      },
      "user": {
        "email": "309a0a5c3e211326ae75ca18196d301a9bdbd1a882a4d2569511033da23f0abd",
        "phone": "254aa248acb47dd654ca3ea53f48c2c26d641571e29e1f3b183be7d0f9e53c14",
        "external_id": "USER-12345",
        "ttp": "TikTok cookie value",
        "ip": "123.456.78.90",
        "user_agent": "Mozilla/5.0..."
      },
      "properties": {
        "value": 49.99,
        "currency": "USD",
        "content_id": "SKU123",
        "content_type": "product",
        "content_name": "Wireless Headphones",
        "quantity": 1,
        "order_id": "ORD-12345"
      }
    }
  ]
}
```

### TikTok Standard Events

| Event Name | Description |
|------------|-------------|
| `ViewContent` | Product/content page view |
| `ClickButton` | Button click |
| `Search` | Search performed |
| `AddToWishlist` | Item added to wishlist |
| `AddToCart` | Item added to cart |
| `InitiateCheckout` | Checkout started |
| `AddPaymentInfo` | Payment info entered |
| `CompletePayment` | Purchase completed |
| `PlaceAnOrder` | Order placed (without payment confirmation) |
| `Subscribe` | Subscription started |
| `SubmitForm` | Form submitted |
| `Contact` | Contact action taken |
| `Download` | File downloaded |
| `CompleteRegistration` | Registration completed |

### TikTok Cookie (`ttp`)
- The `_ttp` cookie is TikTok's equivalent of Meta's `_fbp`
- Must be passed via the Events API for proper attribution
- Set by the TikTok pixel on the browser side
- Read from the cookie and include in server-side events

---

## 4. Google Ads Server-Side Tracking

### Google Ads Offline Conversion Import (via API)

```json
{
  "conversions": [
    {
      "gclid": "EAIaIQobChMI...",
      "conversion_action": "customers/1234567890/conversionActions/987654321",
      "conversion_date_time": "2026-03-06 14:30:00-05:00",
      "conversion_value": 49.99,
      "currency_code": "USD",
      "order_id": "ORD-12345"
    }
  ]
}
```

### Enhanced Conversions via API

For server-side enhanced conversions without GCLID:

```json
{
  "conversions": [
    {
      "conversion_action": "customers/1234567890/conversionActions/987654321",
      "conversion_date_time": "2026-03-06 14:30:00-05:00",
      "conversion_value": 49.99,
      "currency_code": "USD",
      "order_id": "ORD-12345",
      "user_identifiers": [
        {
          "hashed_email": "309a0a5c3e211326ae75ca18196d301a9bdbd1a882a4d2569511033da23f0abd"
        },
        {
          "hashed_phone_number": "254aa248acb47dd654ca3ea53f48c2c26d641571e29e1f3b183be7d0f9e53c14"
        }
      ]
    }
  ]
}
```

### GTM Server-Side Container (Google)

This is Google's recommended approach for server-side tracking:

1. **Set up a server-side GTM container** (hosted on Cloud Run, App Engine, or your own server)
2. **Configure the GA4 client** in the server container to receive hits
3. **Add conversion tags** in the server container (Google Ads, Meta CAPI, TikTok Events API)
4. **Route browser hits** to the server container first, then to vendor endpoints

**Benefits**:
- Single server endpoint manages all vendor tags
- First-party domain for tracking (reduces ad blocker impact)
- Full control over data before it reaches vendors
- Can strip PII or add parameters server-side

---

## 5. Implementation Approaches Compared

### Approach 1: Direct API Integration

**Best for**: Custom-built platforms, high-volume advertisers

| Pros | Cons |
|------|------|
| Full control over data | Requires developer resources |
| Lowest latency | Must maintain for each platform |
| Most flexible | Error handling is your responsibility |

### Approach 2: Platform Plugins

**Best for**: E-commerce platforms (Shopify, WooCommerce, Magento)

| Platform | Meta CAPI | TikTok Events API | Google |
|----------|-----------|-------------------|--------|
| Shopify | Native integration | Native integration | Native + Enhanced Conversions |
| WooCommerce | Plugin available | Plugin available | Plugin available |
| Magento | Extension available | Extension available | Extension available |
| BigCommerce | Native integration | Partner integration | Native integration |

**Shopify CAPI setup**: Settings > Customer Events > Meta (automatic CAPI with browser pixel deduplication built in)

### Approach 3: GTM Server-Side

**Best for**: Multi-platform advertisers, agencies managing multiple clients

**Architecture**:
```
Browser -> GTM Web Container -> GTM Server Container -> Meta CAPI
                                                     -> TikTok Events API
                                                     -> Google Ads
                                                     -> GA4
```

**Hosting options**:
- Google Cloud Run (recommended by Google)
- AWS (Lambda + API Gateway)
- Custom server (Node.js, Docker)
- Stape.io or Addingwell (managed hosting)

**Cost**: $50-$200/month for small-medium sites; scales with traffic

### Approach 4: CDP/iPaaS Integration

**Best for**: Enterprise advertisers with existing data infrastructure

Tools like Segment, Rudderstack, or Tealium can route events to multiple APIs:

```
User Action -> Segment -> Meta CAPI
                       -> TikTok Events API
                       -> Google Ads API
                       -> CRM
                       -> Data Warehouse
```

---

## 6. Data Quality & Match Rates

### Target Match Rates by Platform

| Platform | Good | Excellent |
|----------|------|-----------|
| Meta CAPI | 6.0+ Event Match Quality | 8.0+ Event Match Quality |
| TikTok Events API | 50%+ match rate | 70%+ match rate |
| Google Enhanced Conversions | 60%+ coverage | 80%+ coverage |

### Improving Match Quality

**Priority order for user data parameters**:
1. **Email** (highest impact across all platforms)
2. **Phone number** (high impact)
3. **Click ID cookies** (fbc/fbp for Meta, ttp for TikTok, gclid for Google)
4. **External ID** (your internal user ID)
5. **IP address + user agent** (medium impact, available for all visitors)
6. **Name, location** (supplementary)

### Common Match Rate Issues

| Issue | Impact | Fix |
|-------|--------|-----|
| Missing click ID cookies | -20-30% match rate | Pass fbc/fbp/ttp cookies from browser to server |
| Unhashed or incorrectly hashed data | Events rejected | Verify SHA256 hashing with test values |
| Missing email/phone | Low match rate | Capture user data earlier in funnel; use enhanced matching |
| Event time too far from actual time | Events may be dropped | Send events within minutes, not hours |
| Wrong event names | Events not recognized | Use exact standard event names (case-sensitive) |

---

## 7. Testing & Debugging

### Meta CAPI
- **Test Events tool**: Events Manager > Test Events > Server tab
- **Payload Helper**: `developers.facebook.com/tools/pixel/payload-helper`
- **Graph API Explorer**: Test API calls directly
- **Event Match Quality**: Monitor in Events Manager (aim for 6+)

### TikTok Events API
- **Events Manager**: Shows received events and match status
- **Debug mode**: Send test events with `test_event_code` parameter
- **API response codes**: Check for errors in API responses

### Google Enhanced Conversions
- **Conversion Diagnostics**: Google Ads > Conversions > Diagnostics
- **Tag Assistant**: Verify enhanced conversion data
- **Conversion Reports**: Check for increased conversion volume after implementation

### End-to-End Testing Checklist
- [ ] Fire a test conversion on your website
- [ ] Verify browser pixel fires correctly (Pixel Helper / Tag Assistant)
- [ ] Verify server event is received (platform test tools)
- [ ] Check deduplication (only 1 event recorded, not 2)
- [ ] Verify user data parameters are present and correctly hashed
- [ ] Confirm event appears in platform reporting within 24 hours
- [ ] Test with and without ad blockers enabled
- [ ] Test on iOS Safari with ITP
- [ ] Test consent flow (EU users)

---

## 8. Privacy & Compliance

### Data Minimization
- Only send user data parameters that you have consent to share
- Implement consent checks before firing server-side events
- Log which events were sent with and without user data

### GDPR/LGPD Compliance
- CAPI still requires user consent for personal data
- Server-side tracking does NOT bypass consent requirements
- Implement consent gating on the server side, not just the browser
- Consent Mode (Google) should be mirrored in server-side logic

### Data Retention
- Do not store raw user data longer than necessary
- Hash PII at the point of collection
- Maintain data processing agreements with all platforms
- Document your data flow for privacy audits

---

## 9. Performance Impact Benchmarks

### Before vs. After CAPI Implementation (Typical Results)

| Metric | Before CAPI | After CAPI | Improvement |
|--------|-------------|------------|-------------|
| Reported conversions | Baseline | +15-30% | More events captured |
| Match rate (Meta) | 4-5 EMQ | 7-9 EMQ | Better user matching |
| CPA (reported) | Baseline | -10-20% | Better optimization signal |
| ROAS (reported) | Baseline | +15-25% | More revenue attributed |
| Attribution accuracy | Moderate | High | Fewer missed conversions |
| iOS conversion tracking | 40-60% loss | 10-20% loss | Significant recovery |

---

*Last updated: March 2026. Server-side tracking implementations evolve rapidly. Always verify API versions and endpoints against official platform documentation.*
