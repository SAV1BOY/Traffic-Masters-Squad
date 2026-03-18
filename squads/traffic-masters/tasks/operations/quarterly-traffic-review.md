# Quarterly Traffic Review

> **Type**: Task
> **Category**: operations
> **Agents**: Traffic Chief, Performance Analyst
> **Frameworks**: Quarterly Business Review Framework, Strategic Assessment
> **Checklists**: quarterly-review-checklist
> **Output template**: templates/quarterly-review.md

## ROUTING (from config.yaml)

> **Config key**: `routing.quarterly-traffic-review`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [performance-analyst](../../agents/performance-analyst.md)
> **Frameworks**: `governance-layer`, `burns-mpi`
> **Checklists**: `reporting-quality`
> **Templates**: `reports/quarterly-media-report`
> **Registry**: `data/metrics/kpi-dashboard-spec`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Conduct a comprehensive quarterly review of the Traffic Masters Squad's performance, processes, and strategic direction to evaluate progress against goals, refine the approach, and set priorities for the next quarter.

## Inputs
- Monthly growth reviews from the quarter
- Quarterly performance data across all channels
- Budget actual vs planned for the quarter
- Squad process feedback from all agents
- Industry trends and platform updates from the quarter
- Business-level results: revenue, customer acquisition, market share

## Steps
1. Compile quarterly performance metrics: total spend, revenue attributed, blended CPA, blended ROAS
2. Compare quarterly results against targets set at the beginning of the quarter
3. Analyze channel evolution: which channels grew, shrank, or shifted in efficiency
4. Review unit economics trends: CAC, LTV, LTV:CAC ratio, payback period over the quarter
5. Assess creative system health: production volume, winner rate, fatigue patterns
6. Evaluate tracking and data quality: were decisions made on accurate data
7. Review squad processes: what workflows worked well, what caused friction or delays
8. Analyze competitive landscape changes: new competitors, market shifts, pricing changes
9. Assess platform changes impact: algorithm updates, new features, policy changes
10. Calculate the squad's efficiency: cost of operations vs value delivered
11. Set priorities for the next quarter: top 3 strategic initiatives with OKRs
12. Document lessons learned and process improvement commitments

## Output
Quarterly review containing: performance scoreboard, channel analysis, unit economics trends, creative system assessment, process evaluation, competitive update, next quarter priorities with OKRs, and lessons learned.

## Quality Gate
- Quarterly review checklist confirms all performance areas and processes evaluated
- Next quarter priorities are specific, measurable, and resource-feasible
- Traffic Chief presents review to business leadership for alignment

## Duration
6-8 hours for analysis and report; 2 hours for presentation and discussion
