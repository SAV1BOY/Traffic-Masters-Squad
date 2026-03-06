# Conversions API (CAPI) Setup Quality Gate

> Quality gate for server-side Conversions API setup across platforms (Meta CAPI, TikTok Events API, Google Enhanced Conversions). Must pass before server-side tracking is considered production-ready.

## Section 1: Server-Side Infrastructure
- [ ] CAPI endpoint is hosted on reliable infrastructure (cloud server, serverless function, or partner integration)
- [ ] Server response time for CAPI calls is under 500ms to avoid delays in conversion reporting
- [ ] Error handling and retry logic are implemented for failed API calls (exponential backoff)
- [ ] CAPI integration uses HTTPS for all data transmission
- [ ] Server logs are enabled for debugging and auditing CAPI event delivery

## Section 2: Meta Conversions API
- [ ] Meta CAPI access token is generated and stored securely (not hardcoded in client-side code)
- [ ] Server events include required parameters: event_name, event_time, event_source_url, action_source
- [ ] User data parameters are populated and SHA256 hashed: em (email), ph (phone), fn (first name), ln (last name), ct (city), st (state), zp (zip), country
- [ ] Event Match Quality (EMQ) score is 6.0 or above for each event type
- [ ] Browser and server events are deduplicated using matching event_id values

## Section 3: TikTok Events API
- [ ] TikTok Events API access token is generated via TikTok Marketing API
- [ ] Server events include required parameters: event, event_id, timestamp, user (with hashed identifiers)
- [ ] Event deduplication between browser pixel and Events API uses matching event_id
- [ ] Events API test events are verified in TikTok Events Manager

## Section 4: Google Enhanced Conversions
- [ ] Enhanced conversions for web are configured with first-party data (hashed email, phone, address)
- [ ] Enhanced conversions for leads are set up with GCLID passback from CRM
- [ ] User-provided data is hashed using SHA256 before transmission (or auto-hashed by Google tag)
- [ ] Enhanced conversion diagnostic reports show healthy match rates

## Section 5: Data Quality and Compliance
- [ ] All personally identifiable information (PII) is hashed before transmission to any platform
- [ ] Consent management platform (CMP) signals are respected: no CAPI events sent for users who opted out
- [ ] CAPI event timestamps are accurate and within the platform's accepted time window (usually within 72 hours)
- [ ] Data volume from CAPI matches expected event counts from browser-side tracking (within 10% variance)
- [ ] Regular data quality audits are scheduled (weekly for the first month, monthly thereafter)
- [ ] CAPI configuration is documented including endpoints, authentication, event mapping, and data flow diagrams

## Approval
- **Minimum pass rate**: 18/22 items (82%)
- **Reviewer**: tracking-specialist-agent
- **Escalation**: Missing deduplication or unhashed PII transmission are critical failures; CAPI must not go live until resolved
