# Creative Analysis and Learnings

> **Type**: Task
> **Category**: creative
> **Agents**: Creative Analyst, Burns
> **Frameworks**: Creative Performance Analysis, Statistical Significance Testing
> **Checklists**: creative-analysis-checklist
> **Output template**: templates/creative-analysis-report.md

## ROUTING (from config.yaml)

> **Config key**: `routing.creative-analysis-and-learnings`
> **Agents**: [creative-analyst](../../agents/creative-analyst.md), [ralph-burns](../../agents/ralph-burns.md)
> **Frameworks**: `burns-kaizen-kreative`, `creative-iteration-loop`, `hook-library-system`
> **Checklists**: `creative-fatigue-quality`, `burns/burns-kaizen-kreative-iteration`
> **Templates**: `reports/creative-analysis-report`, `experiments/learnings-log-template`
> **Registry**: `data/registries/creatives-registry`, `data/metrics/learnings-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Analyze creative performance data to extract actionable learnings about which hooks, angles, formats, and elements drive results, feeding insights back into the creative strategy and production pipeline.

## Inputs
- Campaign performance data with creative-level breakdowns
- Creative assets with metadata: angle, format, hook type, variant
- Platform-specific creative metrics: CTR, hook rate, hold rate, ThruPlay rate
- Conversion data: CPA, ROAS, conversion rate per creative
- Minimum data thresholds for statistical significance
- Previous creative analysis reports for trend comparison

## Steps
1. Export creative-level performance data from all active platforms
2. Normalize metrics across platforms for comparable analysis
3. Rank creatives by primary KPI: CPA or ROAS with sufficient spend threshold
4. Analyze performance by angle: which angles consistently outperform
5. Analyze performance by format: static vs video vs carousel vs UGC
6. Analyze performance by hook type: which hook categories drive best engagement
7. Evaluate creative fatigue: identify declining performers by week-over-week trend
8. Extract specific element learnings: colors, faces, text placement, CTA styles
9. Compare performance against creative strategy hypotheses: what was validated, what was not
10. Document top 5 winners and bottom 5 losers with hypothesized reasons
11. Generate iteration briefs: how to build on winners and test new variants
12. Update the creative strategy document with validated learnings

## Output
Creative analysis report containing: performance rankings by creative, angle analysis, format analysis, hook analysis, fatigue indicators, element-level learnings, winner/loser breakdown with rationale, and iteration briefs for next sprint.

## Quality Gate
- Creative analysis checklist confirms sufficient data volume for valid conclusions
- Burns validates that performance calculations use correct attribution data
- Learnings translated into specific actionable briefs for next creative sprint

## Duration
2-4 hours for analysis; 1-2 hours for documentation and brief creation
