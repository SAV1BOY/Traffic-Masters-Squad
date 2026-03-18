# Seasonal Opportunity Research

> **Type**: Task
> **Category**: research
> **Agents**: Traffic Chief, Performance Analyst
> **Frameworks**: Seasonal Planning Framework, Traffic Calendar
> **Checklists**: seasonal-research-checklist
> **Output template**: templates/seasonal-calendar.md

## ROUTING (from config.yaml)

> **Config key**: `routing.seasonal-opportunity-research`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [performance-analyst](../../agents/performance-analyst.md)
> **Frameworks**: `full-funnel-ads-strategy`
> **Checklists**: `seasonal-campaign-quality`
> **Templates**: `plans/seasonal-campaign-plan`
> **Registry**: `data/research/platform-benchmarks`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Identify seasonal opportunities, demand fluctuations, and key dates that impact advertising performance to build a timing-optimized traffic calendar that maximizes spend efficiency and captures peak demand periods.

## Inputs
- Industry vertical and product category
- Historical sales data with monthly/weekly breakdowns (if available)
- Google Trends data for core keywords
- Platform auction data showing CPM seasonality
- Key industry events, holidays, and cultural moments
- Competitor promotional calendars (observed or inferred)

## Steps
1. Pull Google Trends data for top 10 keywords to identify seasonal demand patterns
2. Analyze historical sales or conversion data for monthly and weekly trends
3. Map industry-specific peak seasons and off-seasons with date ranges
4. Identify major shopping events: Black Friday, Prime Day, back-to-school, etc.
5. Research platform-specific auction dynamics: Q4 CPM spikes, election year impacts
6. Document cultural moments and holidays relevant to the target audience
7. Identify competitor promotional patterns and likely budget surges
8. Calculate expected CPM multipliers by month based on historical auction data
9. Define budget pacing strategy: when to increase, maintain, or decrease spend
10. Create a 12-month seasonal calendar with recommended actions per period
11. Flag early preparation windows for creative and landing page updates

## Output
Seasonal calendar containing: 12-month demand forecast, CPM seasonality projections, key dates and events timeline, budget pacing recommendations, creative preparation deadlines, and competitive timing considerations.

## Quality Gate
- Seasonal research checklist confirms all data sources consulted
- Calendar covers full 12-month period with actionable recommendations
- Traffic Chief validates budget pacing alignment with business goals

## Duration
2-3 hours for research; 1-2 hours for calendar assembly and documentation
