# Pixel and CAPI Quality
> **Type**: Quality Gate
> **Domain**: Technical Tracking
> **Reviewed by**: Tracking Specialist

## Purpose
Ensures pixel and Conversions API implementations are accurate, complete, and properly deduplicated. Faulty signal infrastructure undermines all optimization and attribution.

## Checklist

### Pixel Coverage
- [ ] Pixel base code is installed on every page of the website
- [ ] Pixel fires on page load and is confirmed via browser developer tools
- [ ] Pixel is present on landing pages, checkout pages, and thank-you pages
- [ ] Pixel ID is correct and matches the intended ad account
- [ ] No duplicate pixel installations exist on any page

### CAPI Configuration
- [ ] CAPI is configured and actively sending server-side events
- [ ] CAPI endpoint is authenticated with a valid access token
- [ ] CAPI events include user data parameters for matching (email, phone, IP, user agent)
- [ ] CAPI events are sent within an acceptable time window (under 1 hour)
- [ ] Server environment is reliable with monitoring for failures

### Event ID Deduplication
- [ ] Every event sent via both pixel and CAPI includes a unique event_id
- [ ] The same event_id is used for the same action across pixel and CAPI
- [ ] Deduplication is verified in the platform events manager (no duplicate counts)
- [ ] Event_id generation logic is documented and consistent
- [ ] Edge cases (page refreshes, back button) are handled without duplicate events

### Event Match Quality
- [ ] Event match quality score is above 6.0 in the ad platform
- [ ] Customer information parameters are maximized (email, phone, name, location)
- [ ] Data is hashed correctly before being sent (SHA-256 for Meta)
- [ ] Match quality is monitored weekly and improvements are tracked
- [ ] Low match quality triggers are investigated and resolved promptly

### Enhanced Matching
- [ ] Advanced matching or enhanced conversions are enabled
- [ ] User data fields are correctly mapped to platform parameters
- [ ] Enhanced matching data is validated in platform diagnostics
- [ ] Consent requirements are met for data sharing in all regions

### Standard Events
- [ ] All relevant standard events are implemented (ViewContent, AddToCart, Purchase, Lead)
- [ ] Standard event parameters include required fields (value, currency, content_ids)
- [ ] Standard events fire at the correct trigger points in the user journey
- [ ] Event values are accurate and match actual transaction data
- [ ] Standard events are tested across multiple user paths

### Custom Events
- [ ] Custom events are documented with name, trigger, and purpose
- [ ] Custom event naming follows a consistent convention
- [ ] Custom events do not duplicate standard event functionality
- [ ] Custom events have been tested and verified in events manager
- [ ] Documentation includes when and why each custom event was created

### Duplicate Prevention
- [ ] No events fire more than once per user action
- [ ] Page refresh does not re-trigger conversion events
- [ ] Back button navigation does not create duplicate events
- [ ] Form resubmission protection is in place
- [ ] Duplicate event monitoring is part of the ongoing QA process

## Pass/Fail Criteria
All checklist items must pass. Pixel and CAPI issues directly degrade campaign optimization and must be resolved before spend is activated.

## If Failed
Pause affected campaigns. Diagnose the root cause using platform diagnostics and tag debugging tools. Fix and re-verify with a full end-to-end test before reactivating.

## Related
- `tracking-plan-quality.md`
- `attribution-quality.md`
- `funnel-integrity-quality.md`
