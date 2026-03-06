# Event Map Template

> **Type**: Template
> **Category**: tracking
> **Used by tasks**: tracking-setup, event-planning, analytics-configuration
> **Filled by agents**: tracking-agent, analytics-agent

## Purpose
Documents every trackable event across the funnel, mapping event names, triggers, parameters, priorities, platforms, deduplication methods, and ownership to ensure consistent and complete tracking implementation.

## Template

### Event Map Metadata
**Project / client**: [name]
**Funnel type**: [ecommerce / lead-gen / SaaS / application / webinar]
**Last updated**: [date]
**Owner**: [person or agent responsible]

### Standard Events

| Event Name | Trigger | Parameters | Priority | Platform(s) | Dedup Method | Owner |
|---|---|---|---|---|---|---|
| PageView | Every page load | page_title, page_url, page_referrer | Required | Meta, GA4, TikTok | N/A (expected multiple) | [owner] |
| ViewContent | Product or key page view | content_id, content_name, content_type, value, currency | Required | Meta, GA4 | event_id | [owner] |
| Search | Site search executed | search_term | Recommended | GA4 | N/A | [owner] |
| AddToCart | Add-to-cart button click | content_id, content_name, value, currency, quantity | Required | Meta, GA4, TikTok | event_id | [owner] |
| InitiateCheckout | Checkout page load or start | value, currency, num_items, content_ids | Required | Meta, GA4 | event_id | [owner] |
| AddPaymentInfo | Payment info entered | value, currency, payment_method | Recommended | Meta, GA4 | event_id | [owner] |
| Purchase | Order confirmation | value, currency, order_id, content_ids, num_items | Required | Meta, Google, GA4, TikTok | order_id | [owner] |
| Lead | Form submission | form_name, lead_type, value | Required | Meta, Google, GA4 | event_id | [owner] |
| CompleteRegistration | Registration form submit | registration_method, value | Required | Meta, TikTok, GA4 | event_id | [owner] |
| Contact | Contact form or chat initiated | contact_method | Recommended | Google, GA4 | N/A | [owner] |
| Subscribe | Email or SMS subscription | subscription_type | Recommended | GA4 | N/A | [owner] |

### Custom Events

| Event Name | Trigger | Parameters | Priority | Platform(s) | Dedup Method | Owner |
|---|---|---|---|---|---|---|
| [custom_event_1] | [describe trigger] | [param1, param2] | [Required/Recommended/Optional] | [platforms] | [method] | [owner] |
| [custom_event_2] | [describe trigger] | [param1, param2] | [priority] | [platforms] | [method] | [owner] |
| [custom_event_3] | [describe trigger] | [param1, param2] | [priority] | [platforms] | [method] | [owner] |

### Event Parameters Reference

| Parameter | Type | Description | Example |
|---|---|---|---|
| content_id | string | Product or content identifier | "SKU-12345" |
| content_name | string | Product or content name | "Blue Running Shoes" |
| content_type | string | Category of content | "product", "article" |
| value | float | Monetary value | 49.99 |
| currency | string | ISO currency code | "USD" |
| order_id | string | Unique order identifier | "ORD-98765" |
| num_items | integer | Number of items | 3 |
| search_term | string | User search query | "running shoes" |
| event_id | string | Unique event identifier for dedup | "evt_abc123" |

### Deduplication Methods
| Method | When to Use | How It Works |
|---|---|---|
| event_id | Browser pixel + CAPI fire same event | Both send matching event_id; platform deduplicates |
| order_id | Purchase events across channels | Use order_id to prevent double-counting across platforms |
| fbp + timestamp | Meta fallback when event_id unavailable | Combines Facebook browser ID with event timestamp |
| session-based | Prevent duplicate fires on page refresh | Check session storage before firing event |

### Event Flow Diagram
```
Landing Page (PageView)
  -> Product View (ViewContent)
    -> Add to Cart (AddToCart)
      -> Checkout (InitiateCheckout)
        -> Payment (AddPaymentInfo)
          -> Confirmation (Purchase)
```

### Platform-Specific Notes
**Meta**: Use both browser pixel and CAPI. Always include event_id for dedup.
**Google Ads**: Map to Google conversion actions. Use enhanced conversions where possible.
**GA4**: All events flow through Measurement Protocol or gtag.js. Use enhanced measurement for scroll, outbound clicks, file downloads.
**TikTok**: Use TikTok pixel + Events API. Parameter names differ from Meta.

## Usage Notes
- Review this map before any tracking implementation begins.
- Update when new pages, funnels, or features are launched.
- Cross-reference with qa-checklist-template.md during QA phase.

## Example
Ecommerce store with 6 standard events (PageView through Purchase) plus 2 custom events (quiz_complete, upsell_accept) tracked across Meta, Google, and GA4 with CAPI deduplication.

## Related
- tracking-brief.md
- data-layer-spec-template.md
- qa-checklist-template.md
- gtm-container-template.md
