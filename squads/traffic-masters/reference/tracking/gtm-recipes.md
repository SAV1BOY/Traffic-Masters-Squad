# GTM Recipes Reference
> **Tool**: Google Tag Manager
> **Last Updated**: 2026-03

## Recipe 1: Meta Pixel Base Code
- Tag Type: Custom HTML
- Trigger: All Pages
- Content: Meta Pixel base code with fbq('init') and fbq('track', 'PageView')
- Note: Use GTM's built-in Meta tag template if available

## Recipe 2: Meta Standard Events
- Tag Type: Custom HTML with fbq('track', 'EventName')
- Events: ViewContent, AddToCart, InitiateCheckout, Purchase, Lead, CompleteRegistration
- Trigger: Custom event from dataLayer or URL/click-based trigger
- Parameters: value, currency, content_ids, content_type

## Recipe 3: GA4 Event Tags
- Tag Type: GA4 Event (built-in)
- Configuration tag: GA4 Configuration with Measurement ID
- Event tags: one per custom event with parameters mapped from dataLayer

## Recipe 4: Google Ads Conversion Tracking
- Tag Type: Google Ads Conversion Tracking
- Required: Conversion ID + Conversion Label
- Enhanced Conversions: enable and map user-provided data (email, phone)
- Trigger: Thank you page or custom event

## Recipe 5: DataLayer Push for Dynamic Values
```
dataLayer.push({
  event: 'purchase',
  ecommerce: {
    transaction_id: '12345',
    value: 99.90,
    currency: 'BRL',
    items: [{item_id: 'SKU001', item_name: 'Product', price: 99.90, quantity: 1}]
  }
});
```

## Recipe 6: Scroll Depth Tracking
- Trigger Type: Scroll Depth
- Thresholds: 25%, 50%, 75%, 90%
- Tag: GA4 Event with scroll_percentage parameter

## Recipe 7: Click Tracking (Outbound Links)
- Trigger: Click - Just Links, with Click URL does not contain your domain
- Tag: GA4 Event 'outbound_click' with click_url parameter

## Key Takeaways
- Always use Preview mode before publishing
- Version and name every container update
- Keep a backup export of the container before major changes
- Use folders to organize tags by platform (Meta, Google, TikTok)
- Test every tag with real conversions, not just preview mode
