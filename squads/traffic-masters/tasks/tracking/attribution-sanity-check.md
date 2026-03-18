# Attribution Sanity Check

> **Type**: Task
> **Category**: tracking
> **Agents**: Pixel Specialist, Performance Analyst
> **Frameworks**: Attribution Reconciliation Framework, Blended Metrics Model
> **Checklists**: attribution-sanity-checklist
> **Output template**: templates/attribution-audit.md

## ROUTING (from config.yaml)

> **Config key**: `routing.attribution-sanity-check`
> **Agents**: [pixel-specialist](../../agents/pixel-specialist.md), [performance-analyst](../../agents/performance-analyst.md)
> **Frameworks**: `attribution-and-incrementality`
> **Checklists**: `attribution-quality`, `tracking/attribution-window-policy`
> **Templates**: `reports/attribution-report`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Perform a sanity check on attribution data by comparing platform-reported conversions against backend truth, identifying discrepancies, and calibrating reporting to ensure budget decisions are based on accurate performance data.

## Inputs
- Platform-reported conversion data: Meta, Google, TikTok, LinkedIn
- Backend conversion data: CRM, Shopify, database exports
- GA4 conversion data as a neutral reference
- Attribution strategy document with reconciliation methodology
- Date range for comparison: minimum 7 days of data

## Steps
1. Export conversion data from each ad platform for the comparison period
2. Export backend truth data: actual orders, leads, or revenue from the source of record
3. Export GA4 conversion data as a third reference point
4. Compare total conversions: sum of platform-reported vs backend actual
5. Calculate the over-reporting ratio for each platform (platform reported / backend actual)
6. Identify the primary cause of discrepancies: attribution windows, view-through, cross-device
7. Check for double-counting across platforms where the same conversion is claimed by multiple channels
8. Validate revenue values: platform-reported revenue vs actual backend revenue
9. Calculate blended CPA and blended ROAS using backend truth data
10. Set up calibration factors per platform to adjust reported data to reality
11. Document the attribution gap and recommended adjustments for ongoing reporting
12. Establish a recurring reconciliation schedule (weekly or bi-weekly)

## Output
Attribution audit containing: platform vs backend comparison tables, over-reporting ratios per platform, root cause analysis of discrepancies, calibration factors, blended metrics calculations, and recurring reconciliation schedule.

## Quality Gate
- Attribution sanity checklist confirms all platforms compared against backend truth
- Calibration factors calculated and documented for ongoing use
- Performance Analyst validates blended metrics methodology is sound and actionable

## Duration
2-4 hours for data gathering and analysis; 1-2 hours for documentation
