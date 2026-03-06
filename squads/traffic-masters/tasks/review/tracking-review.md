# Tracking Review

> **Type**: Task
> **Category**: review
> **Agents**: Pixel Specialist
> **Frameworks**: Tracking Health Assessment, Data Quality Framework
> **Checklists**: tracking-review-checklist
> **Output template**: templates/tracking-audit.md

## Objective
Review the complete tracking infrastructure to verify ongoing accuracy, identify degradation, check for new tracking gaps, and ensure data quality supports reliable performance reporting and optimization decisions.

## Inputs
- Current tracking documentation: event map, GTM config, pixel setup details
- Platform event manager dashboards for all active platforms
- GA4 real-time and historical event data
- Server-side tracking logs (if applicable)
- Recent website or funnel changes that may affect tracking
- Known tracking issues or discrepancies from recent reports

## Steps
1. Check pixel health across all platforms: active status, event volume trends, error rates
2. Verify event match quality scores for Meta CAPI: targeting above 6.0 (good)
3. Compare event volumes across platforms to detect discrepancies or missing events
4. Review GTM container for unauthorized changes, broken tags, or outdated triggers
5. Test key conversion events by walking through the funnel in GTM preview mode
6. Verify deduplication is still working: browser events not double-counted with server events
7. Check consent mode implementation: are events properly gated by user consent
8. Review GA4 data quality: check for data gaps, unusual patterns, or referral spam
9. Verify UTM parameters are still flowing correctly from ads to analytics
10. Check for any new pages or funnel steps that lack proper tracking
11. Review cross-domain tracking if applicable: verify user sessions are not breaking
12. Document all findings: healthy elements, degraded elements, and new gaps

## Output
Tracking audit containing: pixel health status per platform, event match quality scores, event volume comparison, GTM container audit, deduplication verification, consent mode check, data quality findings, and remediation action items.

## Quality Gate
- Tracking review checklist confirms all tracking components assessed
- No critical tracking gaps (missing purchase or lead events) go undetected
- Pixel Specialist confirms data quality sufficient for optimization decisions

## Duration
1-3 hours for standard periodic review; more if significant issues found
