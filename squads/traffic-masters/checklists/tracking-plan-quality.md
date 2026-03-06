# Tracking Plan Quality
> **Type**: Quality Gate
> **Domain**: Analytics & Measurement
> **Reviewed by**: Tracking Specialist

## Purpose
Ensures the tracking plan is comprehensive, accurate, and fully implemented before any paid traffic is activated. Bad tracking leads to bad decisions and wasted budget.

## Checklist

### Event Definitions
- [ ] All conversion events are defined with clear names and descriptions
- [ ] Micro-conversion events (add to cart, initiate checkout, lead form start) are included
- [ ] Engagement events (scroll depth, video views, time on page) are documented
- [ ] Each event has a clear business purpose and use case
- [ ] Events follow a consistent naming taxonomy across platforms

### Event Parameters
- [ ] Each event has required parameters specified (value, currency, content_id)
- [ ] Custom parameters are documented with expected data types
- [ ] Parameter values are validated against actual data sources
- [ ] Content group or category parameters are included for segmentation
- [ ] User properties are defined for audience building

### Deduplication
- [ ] Event deduplication is configured between pixel and CAPI
- [ ] Unique event_id is generated and passed with each event
- [ ] Deduplication has been tested and verified in events manager
- [ ] No duplicate conversions appear in platform reporting

### UTM Standards
- [ ] UTM naming convention is documented and standardized
- [ ] utm_source, utm_medium, utm_campaign are mandatory for all links
- [ ] utm_content and utm_term are used consistently for creative and keyword tracking
- [ ] UTM values are lowercase with consistent delimiter usage
- [ ] UTM parameters are validated in a test click-through

### Pixel and CAPI Implementation
- [ ] Pixel is installed on all pages of the website or funnel
- [ ] Conversions API (CAPI) is configured and sending events server-side
- [ ] Pixel and CAPI events are matched by event name and event_id
- [ ] Event match quality score is monitored and above 6.0
- [ ] Both pixel and CAPI fire for all key conversion events

### GA4 Mapping
- [ ] All ad platform events have corresponding GA4 events
- [ ] GA4 event names follow the recommended naming convention
- [ ] GA4 conversions are marked for the most important events
- [ ] GA4 audiences are built for remarketing where applicable
- [ ] GA4 and ad platform data are regularly cross-referenced

### Attribution Window
- [ ] Attribution window is set and documented for each platform
- [ ] Click-through and view-through windows are configured intentionally
- [ ] Attribution model is selected with documented rationale
- [ ] Cross-device attribution settings are reviewed

### QA and Validation
- [ ] All events have been tested in a staging or preview environment
- [ ] Real-time event verification is confirmed in each platform
- [ ] Tag assistant or debugging tools have been used to validate firing
- [ ] End-to-end test conversions have been completed and verified
- [ ] QA sign-off is documented with date and tester name

## Pass/Fail Criteria
All checklist items must pass. No campaign launches without verified tracking across all defined events.

## If Failed
Halt campaign activation. Identify and fix tracking gaps. Re-run full QA and obtain sign-off before proceeding.

## Related
- `pixel-and-capi-quality.md`
- `attribution-quality.md`
- `campaign-build-quality.md`
