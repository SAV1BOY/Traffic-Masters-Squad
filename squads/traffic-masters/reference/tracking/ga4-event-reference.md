# GA4 Event Naming & Parameter Reference

> Complete reference for paid traffic professionals implementing and analyzing GA4 events for advertising performance measurement.

---

## 1. GA4 Event Model Overview

GA4 uses an event-based data model. Every interaction is an event with parameters.

### Event Categories

| Category | Description | Examples |
|----------|-------------|---------|
| **Automatically collected** | Collected without any code | `page_view`, `first_visit`, `session_start` |
| **Enhanced measurement** | Collected when enabled in GA4 settings | `scroll`, `click` (outbound), `file_download`, `video_start` |
| **Recommended events** | Predefined by Google; you implement them | `purchase`, `add_to_cart`, `generate_lead` |
| **Custom events** | Events you define yourself | `quiz_completed`, `pricing_page_view` |

**Best practice**: Always use recommended events when they fit. They enable built-in GA4 reports, audience building, and Google Ads integration.

---

## 2. Automatically Collected Events

These fire without any implementation:

| Event | Trigger | Key Parameters |
|-------|---------|----------------|
| `first_visit` | First time a user visits | `- ` |
| `session_start` | New session begins | `- ` |
| `page_view` | Page loads (or history change in SPA) | `page_location`, `page_referrer`, `page_title` |
| `user_engagement` | App in foreground / page focused for 10+ seconds | `engagement_time_msec` |

---

## 3. Enhanced Measurement Events

Enable/disable in GA4 Admin > Data Streams > Enhanced Measurement:

| Event | Trigger | Key Parameters |
|-------|---------|----------------|
| `scroll` | User scrolls 90% of page | `percent_scrolled` (always 90) |
| `click` | User clicks outbound link | `link_url`, `link_domain`, `outbound` |
| `file_download` | User downloads a file | `file_name`, `file_extension`, `link_url` |
| `video_start` | Embedded YouTube video starts | `video_title`, `video_url`, `video_provider` |
| `video_progress` | Video reaches 10%, 25%, 50%, 75% | `video_percent`, `video_title` |
| `video_complete` | Video reaches end | `video_title`, `video_url` |
| `view_search_results` | User performs site search | `search_term` |
| `form_start` | User begins interacting with form | `form_id`, `form_name`, `form_destination` |
| `form_submit` | User submits a form | `form_id`, `form_name`, `form_destination` |

---

## 4. Recommended E-commerce Events

### Full E-commerce Funnel

| Funnel Stage | Event | When to Fire |
|-------------|-------|--------------|
| Browse | `view_item_list` | Category/listing page loads |
| Browse | `select_item` | User clicks a product in a list |
| Product | `view_item` | Product detail page loads |
| Cart | `add_to_cart` | Item added to cart |
| Cart | `remove_from_cart` | Item removed from cart |
| Cart | `view_cart` | Cart page loads |
| Checkout | `begin_checkout` | Checkout process starts |
| Checkout | `add_shipping_info` | Shipping info submitted |
| Checkout | `add_payment_info` | Payment info submitted |
| Purchase | `purchase` | Order confirmed |
| Post-purchase | `refund` | Full or partial refund processed |

### Event Implementation Details

**view_item_list**:
```javascript
gtag('event', 'view_item_list', {
  item_list_id: 'category_electronics',
  item_list_name: 'Electronics',
  items: [
    {
      item_id: 'SKU001',
      item_name: 'Wireless Headphones',
      item_brand: 'BrandX',
      item_category: 'Electronics',
      item_category2: 'Audio',
      item_list_id: 'category_electronics',
      item_list_name: 'Electronics',
      index: 0,
      price: 29.99,
      quantity: 1
    },
    {
      item_id: 'SKU002',
      item_name: 'Bluetooth Speaker',
      item_brand: 'BrandY',
      item_category: 'Electronics',
      item_category2: 'Audio',
      index: 1,
      price: 49.99,
      quantity: 1
    }
  ]
});
```

**purchase** (complete):
```javascript
gtag('event', 'purchase', {
  transaction_id: 'ORD-12345',
  value: 65.97,
  tax: 5.28,
  shipping: 5.99,
  currency: 'USD',
  coupon: 'SAVE10',
  items: [
    {
      item_id: 'SKU001',
      item_name: 'Wireless Headphones',
      item_brand: 'BrandX',
      item_category: 'Electronics',
      item_variant: 'Black',
      price: 29.99,
      quantity: 1,
      coupon: 'SAVE10',
      discount: 3.00
    },
    {
      item_id: 'SKU002',
      item_name: 'Bluetooth Speaker',
      price: 49.99,
      quantity: 1
    }
  ]
});
```

### Item Parameters Reference

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `item_id` | string | Yes* | Product SKU or ID |
| `item_name` | string | Yes* | Product name |
| `affiliation` | string | No | Store or affiliation |
| `coupon` | string | No | Coupon code applied |
| `discount` | number | No | Discount amount |
| `index` | number | No | Position in list |
| `item_brand` | string | No | Product brand |
| `item_category` | string | No | Primary category |
| `item_category2` through `item_category5` | string | No | Sub-categories |
| `item_list_id` | string | No | List identifier |
| `item_list_name` | string | No | List name |
| `item_variant` | string | No | Variant (color, size) |
| `location_id` | string | No | Physical store location |
| `price` | number | No | Unit price |
| `quantity` | number | No | Quantity |

*Either `item_id` or `item_name` is required.

---

## 5. Recommended Lead Generation Events

| Event | When to Fire | Key Parameters |
|-------|--------------|----------------|
| `generate_lead` | Lead form submitted | `value`, `currency` |
| `sign_up` | Account created | `method` (email, google, etc.) |
| `login` | User logs in | `method` |
| `select_content` | Content selected | `content_type`, `content_id` |
| `share` | Content shared | `method`, `content_type`, `item_id` |

### Lead Gen Implementation

```javascript
// Lead form submitted
gtag('event', 'generate_lead', {
  currency: 'USD',
  value: 50.00  // Estimated lead value
});

// Sign up completed
gtag('event', 'sign_up', {
  method: 'email'
});

// Content downloaded (use custom event if needed)
gtag('event', 'file_download_lead', {
  file_name: 'Pricing Guide 2026',
  content_type: 'whitepaper',
  value: 25.00,
  currency: 'USD'
});
```

---

## 6. Custom Event Naming Rules

### Naming Conventions

**Rules**:
- Maximum 40 characters
- Must start with a letter
- Only letters, numbers, and underscores
- Case-sensitive (`Page_View` and `page_view` are different events)
- Cannot use reserved prefixes: `firebase_`, `ga_`, `google_`, `gtag.`

**Recommended naming pattern**: `object_action`
- `video_play`
- `form_start`
- `quiz_complete`
- `pricing_view`
- `chat_open`
- `demo_request`
- `trial_start`
- `subscription_upgrade`

### Custom Event Examples for Advertising

```javascript
// Micro-conversions
gtag('event', 'pricing_page_view', {
  plan_type: 'enterprise',
  time_on_page: 45
});

gtag('event', 'video_milestone', {
  video_name: 'Product Demo',
  milestone: '50_percent',
  video_duration: 120
});

gtag('event', 'quiz_complete', {
  quiz_name: 'Product Finder',
  result: 'Plan A',
  score: 85
});

gtag('event', 'chatbot_engaged', {
  conversation_length: 5,
  topic: 'pricing'
});

// Qualification events
gtag('event', 'lead_qualified', {
  lead_score: 85,
  qualification_method: 'form_scoring',
  value: 200.00,
  currency: 'USD'
});
```

---

## 7. Event Parameters Reference

### Standard Parameters (Available for All Events)

| Parameter | Type | Max Length | Description |
|-----------|------|-----------|-------------|
| `currency` | string | 3 chars | ISO 4217 currency code |
| `value` | number | - | Monetary value |
| `method` | string | 100 chars | Method (login, signup, share) |
| `search_term` | string | 100 chars | Search query |
| `content_type` | string | 100 chars | Type of content |
| `content_id` | string | 100 chars | Content identifier |

### Custom Parameter Limits

| Limit | Amount |
|-------|--------|
| Event-scoped custom parameters (per event) | 25 |
| Event-scoped custom parameters (total per property) | 50 text + 50 numeric |
| User-scoped custom parameters (per property) | 25 text + 25 numeric |
| Parameter name max length | 40 characters |
| Parameter value max length | 100 characters (text) |

**Important**: Custom parameters must be registered in GA4 Admin > Custom Definitions before they appear in reports.

### Registering Custom Parameters

1. GA4 > Admin > Custom Definitions > Custom Dimensions/Metrics
2. Select scope: Event-scoped or User-scoped
3. Enter parameter name (must match exactly what you send in code)
4. Data starts appearing in reports within 24-48 hours (not retroactive)

---

## 8. User Properties

User properties persist across sessions and are associated with the user:

```javascript
gtag('set', 'user_properties', {
  customer_type: 'premium',
  lifetime_value_tier: 'high',
  acquisition_source: 'google_ads',
  plan_name: 'enterprise'
});
```

### Useful User Properties for Advertising

| Property | Values | Use Case |
|----------|--------|----------|
| `customer_type` | new, returning, premium | Segment audiences for remarketing |
| `ltv_tier` | low, medium, high | Build value-based audiences |
| `plan_name` | free, starter, pro, enterprise | Target upsell campaigns |
| `industry` | tech, finance, healthcare | B2B audience segmentation |
| `company_size` | smb, mid_market, enterprise | B2B targeting |

---

## 9. GA4 Audiences for Google Ads

### Building Audiences from Events

In GA4 > Admin > Audiences, create audiences based on event data:

**High-Intent Visitors**:
- Condition: `begin_checkout` event in last 7 days AND NOT `purchase` event in last 7 days
- Use: Cart abandonment remarketing

**Engaged Visitors**:
- Condition: `session_duration` > 120 seconds AND `page_view` count >= 3 in last 30 days
- Use: Prospecting lookalike base

**High-Value Customers**:
- Condition: `purchase` event with `value` > 100 in last 90 days
- Use: Upsell/cross-sell campaigns; lookalike base

**Product Category Viewers**:
- Condition: `view_item` event with `item_category` = 'Electronics' in last 14 days
- Use: Category-specific remarketing

### Predictive Audiences (GA4)

GA4 offers machine-learning predictive audiences:

| Audience | Definition |
|----------|------------|
| **Likely 7-day purchasers** | Users predicted to purchase in next 7 days |
| **Likely 7-day churning users** | Active users predicted to become inactive |
| **Predicted top spenders** | Users predicted to generate most revenue in 28 days |

**Requirements**: At least 1,000 returning users with positive (purchase) and negative (no purchase) examples over 28 days.

---

## 10. GA4 to Google Ads Integration

### Linking GA4 to Google Ads

1. GA4 > Admin > Google Ads Links > Link
2. Select your Google Ads account
3. Enable "Auto-tagging" in Google Ads
4. Enable "Personalized Advertising" (for remarketing)

### Importing GA4 Conversions into Google Ads

1. Google Ads > Goals > Conversions > New Conversion Action > Import > GA4
2. Select the GA4 events you want as Google Ads conversions
3. Set conversion counting (One or Every), value, and attribution window

### Recommended Conversion Setup

| GA4 Event | Google Ads Conversion | Counting | Attribution Window |
|-----------|----------------------|----------|-------------------|
| `purchase` | Primary (Optimize for) | Every | 30-day click, 1-day view |
| `begin_checkout` | Secondary (Observe) | One per user | 30-day click |
| `generate_lead` | Primary (Optimize for) | One per user | 30-day click, 1-day view |
| `add_to_cart` | Secondary (Observe) | One per user | 7-day click |
| `sign_up` | Secondary (Observe) | One per user | 30-day click |

---

## 11. Debugging GA4 Events

### DebugView

1. Enable: `gtag('config', 'G-XXXXXXX', {'debug_mode': true})`
2. Or install GA4 Debugger Chrome extension
3. View in GA4 > Admin > DebugView
4. Shows events in real-time with all parameters

### Realtime Report
- GA4 > Reports > Realtime
- Shows events, conversions, and users in the last 30 minutes
- Less detailed than DebugView but no debug mode required

### Common Issues

| Issue | Symptom | Fix |
|-------|---------|-----|
| Missing events | Events don't appear in reports | Check DebugView; verify `event` name spelling |
| Missing parameters | Parameters not in reports | Register as custom dimensions in Admin |
| Duplicate transactions | Revenue inflated | Add `transaction_id` to `purchase` events |
| Currency mismatch | Revenue converted incorrectly | Use consistent ISO 4217 codes |
| Events delayed | Events appear hours later | Normal; GA4 processing takes up to 24-48 hours |
| Thresholding | Data hidden in reports | Increase date range or remove identity-based dimensions |

---

## 12. Event Naming Quick Reference Card

### E-commerce
```
view_item_list -> select_item -> view_item -> add_to_cart ->
view_cart -> begin_checkout -> add_shipping_info ->
add_payment_info -> purchase
```

### Lead Generation
```
page_view -> form_start -> generate_lead -> [offline: lead_qualified -> lead_closed]
```

### SaaS
```
sign_up -> login -> trial_start -> [custom: feature_used] ->
[custom: upgrade_started] -> purchase (subscription)
```

### Content/Media
```
page_view -> scroll -> select_content -> share ->
[custom: subscribe_newsletter] -> generate_lead
```

---

*Last updated: March 2026. GA4 is actively developed with new features released regularly. Verify event specifications against the official GA4 developer documentation.*
