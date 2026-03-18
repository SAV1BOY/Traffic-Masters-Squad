# Monthly Growth Review (MBR)

> **Type**: Task
> **Category**: reporting
> **Agents**: Traffic Chief, Performance Analyst
> **Frameworks**: Monthly Business Review Framework, Unit Economics Analysis
> **Checklists**: monthly-review-checklist
> **Output template**: templates/monthly-report.md

## ROUTING (from config.yaml)

> **Config key**: `routing.monthly-growth-review`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [performance-analyst](../../agents/performance-analyst.md)
> **Frameworks**: `burns-mpi`, `ltv-cac-unit-economics`, `mer-marketing-efficiency-ratio`
> **Checklists**: `reporting-quality`
> **Templates**: `reports/monthly-growth-report`
> **Registry**: `data/metrics/weekly-scorecards`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Produce a Monthly Growth Review that analyzes performance trends, unit economics, channel efficiency, creative learnings, and strategic progress to inform budget decisions and strategy adjustments for the coming month.

## Inputs
- Weekly business reviews from the past month
- Full month platform performance data across all channels
- Backend revenue and conversion data for the month
- Creative analysis reports from the month
- Budget plan vs actual spend comparison
- Business-level metrics: revenue, customer acquisition, LTV data

## Steps
1. Compile full-month performance data with month-over-month and year-over-year comparisons
2. Calculate unit economics: CAC, nCAC, LTV, LTV:CAC ratio, payback period
3. Analyze channel efficiency trends: which channels improved or degraded over the month
4. Review budget efficiency: actual spend vs planned, cost per incremental dollar of revenue
5. Summarize creative learnings: validated angles, winning formats, fatigue patterns
6. Analyze audience insights: which segments grew, shrank, or shifted in performance
7. Review scaling progress: budget growth achieved vs planned, efficiency at new spend levels
8. Assess funnel health: conversion rates by stage, drop-off improvements or regressions
9. Compare performance against quarterly and annual targets: on track or off track
10. Identify strategic adjustments needed: channel mix, budget allocation, creative direction
11. Build the next month's plan: budget allocation, testing priorities, campaign changes
12. Document key learnings and strategic recommendations for leadership

## Output
Monthly report containing: performance dashboard with trends, unit economics analysis, channel efficiency breakdown, creative learnings summary, audience insights, scaling progress, funnel health, target tracking, and next month's plan with budget.

## Quality Gate
- Monthly review checklist confirms all metrics and analyses completed
- Unit economics validated against backend financial data
- Traffic Chief approves next month's plan and strategic recommendations

## Duration
4-6 hours for analysis and report; 1-2 hours for review and plan finalization
