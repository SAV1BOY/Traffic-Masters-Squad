# Weekly Business Review (WBR)

> **Type**: Task
> **Category**: reporting
> **Agents**: Performance Analyst, Traffic Chief
> **Frameworks**: WBR Framework, Performance Reporting Structure
> **Checklists**: wbr-checklist
> **Output template**: templates/weekly-report.md

## ROUTING (from config.yaml)

> **Config key**: `routing.weekly-business-review`
> **Agents**: [performance-analyst](../../agents/performance-analyst.md), [traffic-chief](../../agents/traffic-chief.md)
> **Frameworks**: `burns-mpi`, `kpi-tree-acquisition`
> **Checklists**: `reporting-quality`
> **Templates**: `reports/weekly-performance-report`
> **Registry**: `data/metrics/weekly-scorecards`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Produce a Weekly Business Review that summarizes performance across all channels, highlights key wins and issues, provides actionable insights, and documents decisions made for the upcoming week.

## Inputs
- Daily pacing reports from the past week
- Platform performance data: spend, impressions, clicks, conversions, revenue
- Backend conversion data for attribution reconciliation
- Creative performance data for the week
- Previous WBR for trend comparison
- Action items from last week's review

## Steps
1. Compile week-over-week performance data across all channels
2. Calculate blended metrics: total spend, total conversions, blended CPA, blended ROAS
3. Break down performance by channel: Meta, Google, TikTok, YouTube, LinkedIn, etc.
4. Highlight top 3 wins: what worked well and should be expanded
5. Highlight top 3 issues: what underperformed and needs attention
6. Review creative performance: top performers, fatigue alerts, new test results
7. Check audience performance: which segments are improving or declining
8. Reconcile platform-reported data against backend truth for key metrics
9. Review progress on action items from last week's WBR
10. Define action items for the coming week with owners and deadlines
11. Provide budget pacing update: MTD spend vs plan, projected month-end
12. Summarize key decisions made and strategic adjustments for the week ahead

## Output
Weekly report containing: performance dashboard, channel breakdowns, win/issue highlights, creative performance summary, audience insights, backend reconciliation, action item tracker, budget pacing, and strategic decisions.

## Quality Gate
- WBR checklist confirms all channels and metrics covered
- Backend reconciliation completed and discrepancies noted
- Traffic Chief reviews and approves action items and strategic decisions

## Duration
2-3 hours for data compilation and analysis; 1 hour for report writing and review
