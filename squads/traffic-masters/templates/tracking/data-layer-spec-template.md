# Data Layer Spec Template

> **Type**: Template
> **Category**: tracking
> **Used by tasks**: data-layer-implementation, tracking-setup, developer-handoff
> **Filled by agents**: tracking-agent, analytics-agent

## Purpose
Specifies all dataLayer variable names, types, when they are pushed, and example payloads, along with mappings to platform events, providing developers with a clear implementation guide.

## Template

### Spec Metadata
**Project / client**: [name]
**Platform**: [Shopify / WordPress / WooCommerce / custom / headless]
**GTM Container**: [GTM-XXXXXXX]
**Version**: [spec version number]
**Last updated**: [date]
**Author**: [person or agent]

### Data Layer Initialization
**When**: On every page load, before GTM container snippet.
**Code**:
```javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  'pageType': '[page type]',
  'userId': '[hashed user ID or empty]',
  'userLoggedIn': [true/false],
  'siteCurrency': 'USD'
});
```

### Page View Data
**When pushed**: On every page load, after dataLayer initialization.
**Variable names and types**:
| Variable | Type | Description | Example |
|---|---|---|---|
| pageType | string | Type of page | "home", "product", "category", "cart", "checkout", "confirmation" |
| pageName | string | Human-readable page name | "Blue Running Shoes - Product Page" |
| userId | string | Hashed user identifier | "abc123def456" |
| userLoggedIn | boolean | Login status | true |

### Product View (ViewContent)
**When pushed**: On product page load or quick-view modal open.
**Payload**:
```javascript
dataLayer.push({
  'event': 'view_item',
  'eventId': '[unique-event-id]',
  'ecommerce': {
    'currency': 'USD',
    'value': 49.99,
    'items': [{
      'item_id': 'SKU-12345',
      'item_name': 'Blue Running Shoes',
      'item_brand': 'BrandName',
      'item_category': 'Footwear',
      'item_variant': 'Size 10',
      'price': 49.99,
      'quantity': 1
    }]
  }
});
```

### Add to Cart
**When pushed**: On add-to-cart button click, after item is added.
**Payload**:
```javascript
dataLayer.push({
  'event': 'add_to_cart',
  'eventId': '[unique-event-id]',
  'ecommerce': {
    'currency': 'USD',
    'value': 49.99,
    'items': [{
      'item_id': 'SKU-12345',
      'item_name': 'Blue Running Shoes',
      'item_brand': 'BrandName',
      'item_category': 'Footwear',
      'item_variant': 'Size 10',
      'price': 49.99,
      'quantity': 1
    }]
  }
});
```

### Begin Checkout
**When pushed**: On checkout page load or checkout button click.
**Payload**:
```javascript
dataLayer.push({
  'event': 'begin_checkout',
  'eventId': '[unique-event-id]',
  'ecommerce': {
    'currency': 'USD',
    'value': 99.98,
    'items': [
      { 'item_id': 'SKU-12345', 'item_name': 'Blue Running Shoes', 'price': 49.99, 'quantity': 1 },
      { 'item_id': 'SKU-67890', 'item_name': 'Running Socks', 'price': 49.99, 'quantity': 1 }
    ]
  }
});
```

### Purchase
**When pushed**: On order confirmation page load, once per transaction.
**Payload**:
```javascript
dataLayer.push({
  'event': 'purchase',
  'eventId': '[unique-event-id]',
  'ecommerce': {
    'transaction_id': 'ORD-98765',
    'currency': 'USD',
    'value': 99.98,
    'tax': 8.00,
    'shipping': 5.99,
    'items': [
      { 'item_id': 'SKU-12345', 'item_name': 'Blue Running Shoes', 'price': 49.99, 'quantity': 1 },
      { 'item_id': 'SKU-67890', 'item_name': 'Running Socks', 'price': 49.99, 'quantity': 1 }
    ]
  }
});
```
**Dedup note**: Use transaction_id to prevent duplicate purchase events on page refresh.

### Lead / Form Submit
**When pushed**: On successful form submission (after validation).
**Payload**:
```javascript
dataLayer.push({
  'event': 'generate_lead',
  'eventId': '[unique-event-id]',
  'formName': 'contact-form',
  'leadType': 'consultation-request',
  'value': 50.00,
  'currency': 'USD'
});
```

### Custom Events
| Event | When Pushed | Payload Variables |
|---|---|---|
| quiz_complete | Quiz final answer submitted | event, eventId, quizResult, quizScore |
| video_milestone | Video reaches 25/50/75/100% | event, videoTitle, videoPercent |
| upsell_accept | Upsell offer accepted | event, eventId, upsellProduct, value |
| exit_intent | Exit intent popup shown | event, pageType, timeOnPage |

### Mapping to Platform Events
| dataLayer Event | GA4 Event | Meta Pixel Event | Google Ads | TikTok |
|---|---|---|---|---|
| view_item | view_item | ViewContent | -- | ViewContent |
| add_to_cart | add_to_cart | AddToCart | -- | AddToCart |
| begin_checkout | begin_checkout | InitiateCheckout | -- | InitiateCheckout |
| purchase | purchase | Purchase | Conversion (Purchase) | CompletePayment |
| generate_lead | generate_lead | Lead | Conversion (Lead) | SubmitForm |

### Implementation Notes
- Always push `dataLayer.push({'ecommerce': null})` before each ecommerce push to clear previous data.
- The eventId must be unique per event instance; use a UUID generator function.
- All monetary values should be numbers (not strings) with no currency symbols.
- Currency must be a valid ISO 4217 code.
- Item arrays must follow GA4 ecommerce item schema.

## Usage Notes
- Hand this spec to developers alongside the event-map-template.md.
- Validate implementation using GTM Preview mode and browser console.
- Test with real transactions in staging before going live.

## Example
Shopify store with standard ecommerce events plus custom quiz_complete event. All events push to dataLayer with eventId for CAPI deduplication. GTM reads dataLayer and distributes to GA4, Meta, and TikTok.

## Related
- event-map-template.md
- gtm-container-template.md
- qa-checklist-template.md
