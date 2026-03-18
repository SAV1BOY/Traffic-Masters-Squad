# Account Audit 30-60-90
> **Type**: Workflow
> **Duration**: 90 days (phased)
> **Agents involved**: traffic-chief, media-buyer, pixel-specialist, performance-analyst, creative-analyst

## Trigger
New client onboarding, quarterly review, or performance decline exceeding 30 days.

## Steps
1. Data Export (Day 1-2) → Agent: performance-analyst → Framework: Full Data Pull → Output: Last 90 days of account data exported and normalized
2. Structure Audit (Day 2-3) → Agent: media-buyer → Framework: Sobral/Mandalia Structure Review → Output: Campaign structure assessment with issues flagged
3. Tracking Audit (Day 3-4) → Agent: pixel-specialist → Framework: Pixel + CAPI Validation → Output: Tracking health report with discrepancies noted
4. Creative Audit (Day 4-5) → Agent: creative-analyst → Framework: Creative Fatigue Analysis → Output: Creative performance timeline and fatigue indicators
5. Audience Audit (Day 5-6) → Agent: traffic-chief → Framework: Audience Overlap + Saturation → Output: Audience health report with overlap percentages
6. Findings Report (Day 7) → Agent: traffic-chief → Framework: GECO Summary → Output: Prioritized findings with severity ratings (critical/high/medium/low)
7. 30-Day Plan → Agent: traffic-chief → Framework: Quick Wins First → Output: Immediate actions for first 30 days (fix tracking, pause waste, restructure)
8. 60-Day Plan → Agent: traffic-chief → Framework: Optimization Phase → Output: Testing plan, new audiences, creative refresh
9. 90-Day Plan → Agent: traffic-chief → Framework: Scale Phase → Output: Scaling strategy, budget increase plan, new channels

## Quality Gates
- [ ] All data sources reconciled (platform vs GA4 vs CRM)
- [ ] Every active campaign reviewed
- [ ] Tracking verified with test conversions
- [ ] Audience overlap below 25% between ad sets
- [ ] Wasted spend identified and quantified
- [ ] Each finding has a specific action item
- [ ] Timeline realistic with resource allocation

## Output
Comprehensive audit document with 30/60/90-day action plan.
Executive summary for stakeholder presentation.
Prioritized task list in project management tool.

## Audit Scoring
- Account Health Score: 0-100 based on weighted criteria
- Categories: Structure (20%), Tracking (20%), Creative (20%), Audience (20%), Performance (20%)
- Red: 0-40 | Yellow: 41-70 | Green: 71-100

## Notes
- Compare metrics to industry benchmarks from reference/industries/
- Check for policy violations that could trigger account restrictions
- Brazilian accounts: verify NF and LGPD compliance
- Document everything — audit becomes the baseline for future comparison

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
