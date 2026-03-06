# Meta Conversions API (CAPI) Guide
> **Tool**: Meta Conversions API
> **Last Updated**: 2026-03

## Overview
The Conversions API sends conversion events directly from your server to Meta, bypassing browser limitations (ad blockers, iOS restrictions, cookie deprecation).

## Implementation Methods
1. **Partner Integration**: Shopify, WooCommerce, WordPress plugins (easiest)
2. **Google Tag Manager Server-Side**: GTM server container sends events to Meta
3. **Direct API Integration**: Custom server-side code sending events via HTTP
4. **Meta Gateway**: Meta's managed server-side solution

## Required Event Parameters
- event_name: Standard event name (Purchase, Lead, AddToCart, etc.)
- event_time: Unix timestamp of the event
- action_source: "website" for web conversions
- user_data: hashed email, phone, IP, user agent (for matching)
- event_id: Unique ID for deduplication with browser pixel

## Deduplication
- Both browser pixel and CAPI send the same event
- event_id must match between pixel and CAPI for the same conversion
- Meta deduplicates based on event_id + event_name within 48h window
- Without proper deduplication, conversions will be double-counted

## Event Match Quality (EMQ)
- Score from 1-10 measuring how well CAPI events can match to Meta users
- Target: 6.0+ (good), 8.0+ (excellent)
- Improve by sending more user data parameters (email, phone, fbp, fbc)
- Check EMQ in Events Manager > Data Sources > CAPI tab

## Testing and Validation
- Use Meta Events Manager Test Events tab
- Send test events with test_event_code parameter
- Verify events appear with correct parameters and deduplication
- Check EMQ score after implementation

## Key Takeaways
- CAPI is no longer optional — it is essential for accurate tracking on Meta
- Deduplication is the most common implementation mistake
- Send as many user data parameters as possible (hashed) to improve matching
- Monitor EMQ score monthly and optimize if below 6.0
- Server-side tracking does not bypass LGPD consent requirements
