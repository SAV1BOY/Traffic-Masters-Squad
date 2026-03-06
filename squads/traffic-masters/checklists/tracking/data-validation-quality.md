# Tracking Data Validation and QA Quality Gate

> Quality gate for tracking data validation, quality assurance, and discrepancy resolution. Must pass before tracking data is trusted for reporting or optimization decisions.

## Section 1: End-to-End Event Validation
- [ ] Test conversions (purchase, lead, sign-up) have been triggered on staging and production environments
- [ ] Each test conversion is verified in every platform's event manager: Meta Events Manager, Google Ads, TikTok Events Manager, LinkedIn
- [ ] Event parameters (value, currency, content_id) are verified for correctness in each platform
- [ ] Server-side events (CAPI) match browser-side events in count and parameter values
- [ ] Events fire correctly across all key user paths: direct URL, paid ad click-through, organic search

## Section 2: Cross-Platform Data Reconciliation
- [ ] Total conversions reported by each ad platform are compared to the source of truth (CRM, e-commerce backend, GA4)
- [ ] Discrepancies between platform-reported conversions and backend data are within acceptable tolerance (10-15%)
- [ ] Revenue values reported by platforms are reconciled against actual revenue (accounting for returns, cancellations)
- [ ] Click counts from ad platforms are compared to GA4 session counts (expected variance: 10-20%)
- [ ] Impression and reach data from platforms are sanity-checked against audience size estimates

## Section 3: Deduplication Verification
- [ ] No single conversion is counted more than once within the same platform (event_id deduplication working)
- [ ] Cross-platform deduplication is documented: if a user converts, which platform gets credit in internal reporting
- [ ] GA4 is used as the neutral source for cross-platform attribution comparison
- [ ] Test scenarios confirm that refreshing the thank-you/confirmation page does not re-fire conversion events
- [ ] Form resubmission protection is verified (double-click or back-button does not create duplicate leads)

## Section 4: Data Layer and Tag Audit
- [ ] Data layer values are inspected on key pages using browser developer tools or GTM Preview
- [ ] No undefined, null, NaN, or empty string values appear in required data layer fields
- [ ] Tag firing sequence is correct (verified in GTM Preview mode or equivalent)
- [ ] No JavaScript errors in the console are caused by tracking code
- [ ] Page load performance impact of all tracking tags is measured and acceptable (under 500ms total)

## Section 5: Ongoing Monitoring and Alerting
- [ ] Automated alerts are configured for: zero conversions in 24h, 50%+ drop in event volume, pixel error spikes
- [ ] Weekly data quality report compares platform data vs. backend data for key metrics
- [ ] Monthly tracking audit is scheduled to verify all events still fire correctly after site changes
- [ ] A runbook exists for diagnosing and resolving common tracking discrepancies
- [ ] Tracking QA is re-run after any website deployment, tag configuration change, or platform update
- [ ] Data validation results are documented in a shared tracking health dashboard

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: tracking-specialist-agent + analytics-agent
- **Escalation**: Deduplication failures or data discrepancies above 20% are hard blocks; tracking must be investigated and fixed before data is used for optimization
