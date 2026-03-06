# Meta Pixel and CAPI Events Quality Gate

> Quality gate for Meta Pixel and Conversions API (CAPI) event setup. Must pass before campaigns relying on pixel data are launched.

## Section 1: Pixel Installation
- [ ] Meta Pixel base code is installed on all pages of the website (verified via Meta Pixel Helper extension)
- [ ] Pixel ID matches the correct Business Manager / Ad Account
- [ ] Pixel fires a PageView event on every page load without errors
- [ ] Pixel is installed via Google Tag Manager or server-side container (not hardcoded inline, unless justified)
- [ ] No duplicate pixel installations exist on the same page

## Section 2: Standard Event Configuration
- [ ] All required standard events are implemented: ViewContent, AddToCart, InitiateCheckout, Purchase (for e-commerce) or Lead, CompleteRegistration (for lead gen)
- [ ] Each standard event fires on the correct page/action (e.g., Purchase fires only on order confirmation)
- [ ] Event parameters are populated correctly: content_ids, content_type, value, currency, content_name
- [ ] Currency parameter uses ISO 4217 format (e.g., BRL, USD) and value is numeric (no currency symbols)
- [ ] Purchase event value matches the actual transaction amount (verified against backend data)

## Section 3: Custom Event and Conversion Setup
- [ ] Custom events follow a documented naming convention (lowercase, underscores, no spaces)
- [ ] Custom conversions are created in Events Manager for any non-standard conversion points
- [ ] Event deduplication is configured between Pixel (browser) and CAPI (server) using event_id parameter
- [ ] Aggregated Event Measurement (AEM) priority ranking is configured for iOS 14.5+ optimization
- [ ] Top 8 prioritized events are ordered correctly by business value (highest priority = Purchase)

## Section 4: Conversions API (CAPI) Setup
- [ ] Server-side events are sent via CAPI for all key conversion events (Purchase, Lead, AddToCart)
- [ ] CAPI events include required user parameters: client_ip_address, client_user_agent, em (hashed email), ph (hashed phone)
- [ ] Event Match Quality (EMQ) score is 6.0 or above for each CAPI event
- [ ] CAPI integration is tested via Events Manager Test Events tool with real traffic
- [ ] Server-side and browser-side events are deduplicated (matching event_id and event_name)

## Section 5: Data Quality Validation
- [ ] Events Manager shows green status (active) for all configured events
- [ ] No "Event received with errors" warnings in Events Manager for the past 7 days
- [ ] Test purchase / test lead has been fired and verified end-to-end (browser + CAPI)
- [ ] Event volume trends are stable (no sudden drops indicating broken implementation)
- [ ] Domain verification is completed for the pixel's primary domain in Business Manager

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: tracking-specialist-agent
- **Escalation**: Any deduplication or CAPI failure is a hard block; tracking must be fixed before campaign launch
