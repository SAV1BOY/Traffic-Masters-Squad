# Daily Optimization Loop

> **Type**: Task
> **Category**: optimization
> **Agents**: Media Buyer, Performance Analyst, Sobral
> **Frameworks**: GECO-ANA Daily Routine (Gather, Evaluate, Compare, Optimize - Analyze, Note, Act)
> **Checklists**: daily-optimization-checklist
> **Output template**: templates/daily-actions.md

## ROUTING (from config.yaml)

> **Config key**: `routing.daily-optimization-loop`
> **Agents**: [media-buyer](../../agents/media-buyer.md), [performance-analyst](../../agents/performance-analyst.md), [pedro-sobral](../../agents/pedro-sobral.md)
> **Frameworks**: `optimization-layer`, `sobral-geco-ana`, `pacing-and-guardrails`
> **Checklists**: `budget-pacing-quality`, `sobral/sobral-geco-ana-cycle`
> **Templates**: `reports/daily-pacing-report`
> **Registry**: N/A
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Execute the daily GECO-ANA optimization routine to monitor campaign performance, identify issues and opportunities, and take timely actions that keep campaigns on track toward KPI targets.

## Inputs
- Access to all ad platform dashboards
- Daily pacing targets: spend, conversions, CPA, ROAS
- Active campaign list with current status
- Previous day's optimization notes
- Alert thresholds for anomaly detection

## Steps
1. GATHER: Pull performance data from all active platforms for the last 24 hours and trailing 7 days
2. EVALUATE: Compare yesterday's performance against daily targets and trailing averages
3. COMPARE: Benchmark each campaign against its peers and historical performance
4. OPTIMIZE: Identify campaigns requiring action based on evaluation
5. Check for budget delivery issues: underspend or overspend versus daily targets
6. Review top and bottom performing ad sets and creatives
7. Check for learning phase status changes and their impact
8. ANALYZE: Investigate root causes for any significant performance changes
9. NOTE: Document all findings, decisions, and actions taken with rationale
10. ACT: Execute optimization actions: bid adjustments, budget shifts, creative pauses, audience changes
11. Flag any issues requiring escalation to Traffic Chief or specialist review
12. Update the daily pacing tracker with actuals and forecast

## Output
Daily actions log containing: performance summary, anomalies detected, actions taken with rationale, escalations raised, pacing update, and notes for next day's review.

## Quality Gate
- Daily optimization checklist confirms all platforms reviewed
- All actions documented with clear rationale
- Pacing tracker updated before end of business day

## Duration
30-60 minutes for standard daily review; up to 2 hours if significant issues arise
