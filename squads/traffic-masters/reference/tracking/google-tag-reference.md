# Google Tag / gtag.js Implementation Reference

> Technical reference for paid traffic professionals implementing Google Ads conversion tracking, remarketing, and Google Analytics 4 via gtag.js.

---

## 1. Global Site Tag (gtag.js) Base Installation

### Standard Installation

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXX');  // GA4 Measurement ID
</script>
```

### Multiple Products on One Page

```javascript
gtag('config', 'G-XXXXXXX');         // GA4
gtag('config', 'AW-YYYYYYYYY');      // Google Ads
gtag('config', 'DC-ZZZZZZZZ');       // Campaign Manager 360 (Floodlight)
```

### With Consent Mode v2

```javascript
// Set default consent state BEFORE loading gtag.js
gtag('consent', 'default', {
  'ad_storage': 'denied',
  'ad_user_data': 'denied',
  'ad_personalization': 'denied',
  'analytics_storage': 'denied',
  'functionality_storage': 'granted',
  'security_storage': 'granted',
  'wait_for_update': 500
});

gtag('js', new Date());
gtag('config', 'G-XXXXXXX');
gtag('config', 'AW-YYYYYYYYY');

// After user consents (triggered by CMP callback)
function grantConsent() {
  gtag('consent', 'update', {
    'ad_storage': 'granted',
    'ad_user_data': 'granted',
    'ad_personalization': 'granted',
    'analytics_storage': 'granted'
  });
}
```

---

## 2. Google Ads Conversion Tracking

### Standard Conversion Event

```javascript
gtag('event', 'conversion', {
  'send_to': 'AW-YYYYYYYYY/CONVERSION_LABEL',
  'value': 49.99,
  'currency': 'USD',
  'transaction_id': 'ORD-12345'  // For deduplication
});
```

### Common Conversion Types

**Purchase/Sale**:
```javascript
gtag('event', 'conversion', {
  'send_to': 'AW-YYYYYYYYY/abcDEF123',
  'value': 149.97,
  'currency': 'USD',
  'transaction_id': 'ORD-20260306-001'
});
```

**Lead Form Submission**:
```javascript
gtag('event', 'conversion', {
  'send_to': 'AW-YYYYYYYYY/xyzGHI456',
  'value': 25.00,
  'currency': 'USD'
});
```

**Phone Call (Click-to-Call)**:
```javascript
gtag('event', 'conversion', {
  'send_to': 'AW-YYYYYYYYY/callLABEL',
  'value': 50.00,
  'currency': 'USD'
});
```

### Enhanced Conversions

Enhanced conversions send hashed first-party customer data to improve conversion matching:

**Method 1: Global Site Tag (Automatic)**
```javascript
gtag('config', 'AW-YYYYYYYYY', {
  // User-provided data is automatically detected from form fields
  'allow_enhanced_conversions': true
});
```

**Method 2: Manual Data Layer**
```javascript
gtag('set', 'user_data', {
  'email': 'user@example.com',    // Will be hashed automatically
  'phone_number': '+11234567890',
  'address': {
    'first_name': 'John',
    'last_name': 'Doe',
    'street': '123 Main St',
    'city': 'New York',
    'region': 'NY',
    'postal_code': '10001',
    'country': 'US'
  }
});

// Then fire the conversion
gtag('event', 'conversion', {
  'send_to': 'AW-YYYYYYYYY/CONVERSION_LABEL',
  'value': 49.99,
  'currency': 'USD',
  'transaction_id': 'ORD-12345'
});
```

**Method 3: Via Google Tag Manager (recommended for complex setups)**
- Use the "User-Provided Data" variable in GTM
- Map form fields or data layer variables to user data fields
- Configure in the Google Ads conversion tag settings

### Enhanced Conversions for Leads

For lead gen businesses where the conversion happens offline:

1. **Capture lead on website** (with hashed email/phone):
```javascript
gtag('event', 'conversion', {
  'send_to': 'AW-YYYYYYYYY/LEAD_LABEL',
  'value': 0,
  'currency': 'USD'
});
gtag('set', 'user_data', {
  'email': 'lead@example.com'
});
```

2. **Upload offline conversion data** matching the hashed email to attribute the sale back to the ad click

---

## 3. Google Ads Remarketing

### Standard Remarketing Tag

```javascript
gtag('config', 'AW-YYYYYYYYY');  // Enables remarketing automatically
```

### Dynamic Remarketing Parameters

**Retail/E-commerce**:
```javascript
gtag('event', 'view_item', {
  'send_to': 'AW-YYYYYYYYY',
  'value': 29.99,
  'items': [{
    'id': 'SKU123',                // Must match Merchant Center feed
    'google_business_vertical': 'retail'
  }]
});
```

**Travel**:
```javascript
gtag('event', 'view_item', {
  'send_to': 'AW-YYYYYYYYY',
  'value': 299.00,
  'items': [{
    'id': 'HOTEL-NYC-001',
    'origin': 'SFO',
    'destination': 'JFK',
    'start_date': '2026-04-01',
    'end_date': '2026-04-05',
    'google_business_vertical': 'hotel_rental'  // or 'flights'
  }]
});
```

**Education**:
```javascript
gtag('event', 'view_item', {
  'send_to': 'AW-YYYYYYYYY',
  'items': [{
    'id': 'COURSE-101',
    'location_id': 'NYC',
    'google_business_vertical': 'education'
  }]
});
```

**Real Estate**:
```javascript
gtag('event', 'view_item', {
  'send_to': 'AW-YYYYYYYYY',
  'items': [{
    'id': 'LISTING-12345',
    'listing_type': 'for_sale',
    'google_business_vertical': 'real_estate'
  }]
});
```

### Business Verticals for Dynamic Remarketing

| Vertical | `google_business_vertical` Value |
|----------|--------------------------------|
| Retail | `retail` |
| Education | `education` |
| Flights | `flights` |
| Hotels | `hotel_rental` |
| Jobs | `jobs` |
| Local deals | `local` |
| Real estate | `real_estate` |
| Travel | `travel` |
| Custom | `custom` |

---

## 4. GA4 Integration via gtag.js

### Recommended E-commerce Events

```javascript
// View item list (category page)
gtag('event', 'view_item_list', {
  'item_list_id': 'category_electronics',
  'item_list_name': 'Electronics',
  'items': [{
    'item_id': 'SKU123',
    'item_name': 'Wireless Headphones',
    'price': 29.99,
    'item_category': 'Electronics',
    'index': 0
  }]
});

// View item (product page)
gtag('event', 'view_item', {
  'currency': 'USD',
  'value': 29.99,
  'items': [{
    'item_id': 'SKU123',
    'item_name': 'Wireless Headphones',
    'price': 29.99,
    'item_category': 'Electronics',
    'quantity': 1
  }]
});

// Add to cart
gtag('event', 'add_to_cart', {
  'currency': 'USD',
  'value': 29.99,
  'items': [{
    'item_id': 'SKU123',
    'item_name': 'Wireless Headphones',
    'price': 29.99,
    'quantity': 1
  }]
});

// Begin checkout
gtag('event', 'begin_checkout', {
  'currency': 'USD',
  'value': 59.98,
  'items': [
    {'item_id': 'SKU123', 'item_name': 'Wireless Headphones', 'price': 29.99, 'quantity': 1},
    {'item_id': 'SKU456', 'item_name': 'Phone Case', 'price': 29.99, 'quantity': 1}
  ]
});

// Purchase
gtag('event', 'purchase', {
  'transaction_id': 'ORD-12345',
  'value': 59.98,
  'currency': 'USD',
  'tax': 4.80,
  'shipping': 5.99,
  'items': [
    {'item_id': 'SKU123', 'item_name': 'Wireless Headphones', 'price': 29.99, 'quantity': 1},
    {'item_id': 'SKU456', 'item_name': 'Phone Case', 'price': 29.99, 'quantity': 1}
  ]
});
```

### Lead Generation Events

```javascript
// Generate lead
gtag('event', 'generate_lead', {
  'currency': 'USD',
  'value': 50.00
});

// Sign up
gtag('event', 'sign_up', {
  'method': 'email'
});
```

---

## 5. Conversion Linker

The conversion linker tag reads ad click information (GCLID, DCLID) from URL parameters and stores it in first-party cookies.

**Automatic with gtag.js**: The conversion linker is included automatically when you use `gtag('config', 'AW-XXXXXXX')`.

**GTM**: Must add a separate Conversion Linker tag (fires on All Pages).

### Cross-Domain Tracking

If your funnel spans multiple domains:

```javascript
gtag('config', 'AW-YYYYYYYYY', {
  'linker': {
    'domains': ['example.com', 'checkout.example.com', 'shop.example.com']
  }
});

gtag('config', 'G-XXXXXXX', {
  'linker': {
    'domains': ['example.com', 'checkout.example.com', 'shop.example.com']
  }
});
```

---

## 6. Offline Conversion Import

For businesses where the sale happens offline (phone, in-store, sales team):

### Process
1. Capture GCLID from the landing page URL parameter
2. Store GCLID alongside the lead record in your CRM
3. When the lead converts offline, upload the conversion with the GCLID

### GCLID Capture (JavaScript)

```javascript
function getGclid() {
  const urlParams = new URLSearchParams(window.location.search);
  return urlParams.get('gclid');
}

// Store in hidden form field
document.getElementById('gclid_field').value = getGclid() || '';

// Or store in cookie for later form submissions
function storeGclid() {
  const gclid = getGclid();
  if (gclid) {
    document.cookie = `gclid=${gclid};max-age=7776000;path=/`; // 90 days
  }
}
```

### Upload Format (CSV)

```
Google Click ID, Conversion Name, Conversion Time, Conversion Value, Conversion Currency
EAIaIQobChMI..., Qualified Lead, 2026-03-06 14:30:00-0500, 500.00, USD
```

---

## 7. Debugging & Validation

### Google Tag Assistant
- Chrome extension for validating Google tags
- Shows all tags firing on a page
- Validates conversion parameters
- Checks for common errors

### GA4 DebugView
1. Enable debug mode: `gtag('config', 'G-XXXXXXX', {'debug_mode': true})`
2. View events in real-time at: GA4 > Admin > DebugView
3. Shows event parameters, user properties, and errors

### Google Ads Conversion Diagnostics
- Available in Google Ads under Tools > Measurement > Conversions
- Shows tag status, recent conversions, and potential issues
- Check for "No recent conversions" or "Unverified" status

### Common Issues & Fixes

| Issue | Symptom | Fix |
|-------|---------|-----|
| Tag not firing | No conversions recorded | Verify gtag.js loads; check consent state |
| GCLID not captured | Conversions not attributed | Ensure auto-tagging is enabled in Google Ads |
| Duplicate conversions | Inflated conversion count | Add `transaction_id` parameter for deduplication |
| Cross-domain break | Conversions lost between domains | Configure linker domains; verify cookie consent across domains |
| Value = 0 | Conversion value not recorded | Pass dynamic value, not hardcoded 0 |
| Enhanced conversions not matching | Low match rate | Verify user data format; ensure hashing is correct |
| Consent Mode blocking all data | No conversions in EU | Verify consent update triggers properly after user accepts |

---

## 8. gtag.js vs. GTM Decision Guide

| Factor | gtag.js (Direct) | GTM |
|--------|-----------------|-----|
| **Simplicity** | Simpler for basic setups | More complex but more flexible |
| **Speed** | Slightly faster (fewer redirects) | Marginal latency from container load |
| **Maintenance** | Requires code changes for updates | UI-based changes, no code deploys |
| **Multi-platform** | Google-focused | Manages all vendor tags |
| **Debugging** | Tag Assistant | GTM Preview Mode + Tag Assistant |
| **Team access** | Developer-dependent | Marketers can manage tags |
| **Version control** | Via source code | Built-in GTM versioning |

**Recommendation**: Use GTM for most production setups. Use gtag.js directly for simple sites or when GTM is not available.

---

## 9. Key Reference URLs

| Resource | URL |
|----------|-----|
| gtag.js Developer Guide | `developers.google.com/tag-platform/gtagjs` |
| Google Ads Conversion Tracking | `support.google.com/google-ads/answer/6095821` |
| Enhanced Conversions | `support.google.com/google-ads/answer/11062876` |
| Consent Mode | `developers.google.com/tag-platform/security/guides/consent` |
| GA4 Event Reference | `support.google.com/analytics/answer/9267735` |
| Tag Assistant | `tagassistant.google.com` |

---

*Last updated: March 2026. Google's tag ecosystem evolves frequently. Verify implementation details against the official Google Tag Platform documentation.*
