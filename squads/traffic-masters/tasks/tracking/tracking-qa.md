# Tracking QA

> **Type**: Task
> **Category**: tracking
> **Agents**: Pixel Specialist
> **Frameworks**: Tracking QA Protocol, Event Validation Framework
> **Checklists**: tracking-qa-checklist
> **Output template**: templates/qa-report.md

## Objective
Perform comprehensive quality assurance on the entire tracking stack to verify all events fire correctly, parameters are accurate, deduplication works, and data flows properly from user action to platform reporting.

## Inputs
- Event map as the source of truth for expected events
- Access to all platform event managers and debug tools
- GTM preview mode access
- GA4 DebugView access
- Test environment or staging URLs
- Browser developer tools and network inspection

## Steps
1. Create a QA test plan listing every event, expected trigger, and validation method
2. Walk through the complete funnel in GTM preview mode verifying each tag fires
3. Check GA4 DebugView to confirm events arrive with correct parameters and values
4. Verify Meta Events Manager shows events with correct parameters and match quality
5. Check TikTok Events Manager for proper event receipt and parameter accuracy
6. Verify Google Ads conversion tracking shows test conversions with correct values
7. Test deduplication: confirm browser and server events resolve to single conversions
8. Test cross-device scenarios: start on mobile, convert on desktop
9. Test consent scenarios: verify tracking respects consent denial properly
10. Validate UTM parameters flow correctly from ad click to analytics
11. Check for common errors: duplicate pixels, missing parameters, wrong event names, currency issues
12. Document all findings: passes, failures, and recommended fixes

## Output
QA report containing: test plan with pass/fail results per event, parameter accuracy audit, deduplication verification, cross-device test results, consent compliance check, error log with severity ratings, and recommended fixes with priority.

## Quality Gate
- Tracking QA checklist confirms all events tested across all platforms
- Zero critical failures (missing purchase events, wrong values, broken deduplication)
- All medium-severity issues have documented fix plans with timelines

## Duration
3-5 hours for full QA cycle; 1-2 hours for documentation and fix planning
