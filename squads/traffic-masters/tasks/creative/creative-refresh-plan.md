# Creative Refresh Plan

> **Type**: Task
> **Category**: creative
> **Agents**: Creative Analyst, Ad Midas
> **Frameworks**: Creative Fatigue Detection, Refresh Cadence Model
> **Checklists**: creative-refresh-checklist
> **Output template**: templates/refresh-calendar.md

## ROUTING (from config.yaml)

> **Config key**: `routing.creative-refresh-plan`
> **Agents**: [creative-analyst](../../agents/creative-analyst.md), [ad-midas](../../agents/ad-midas.md)
> **Frameworks**: `creative-iteration-loop`, `creative-production-pipeline`
> **Checklists**: `creative-fatigue-quality`, `creative/creative-refresh-cadence`
> **Templates**: `plans/creative-production-plan`
> **Registry**: `data/registries/creatives-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Plan the creative refresh cadence to proactively combat ad fatigue, maintain performance consistency, and ensure a continuous pipeline of fresh creatives replaces declining performers before they damage campaign efficiency.

## Inputs
- Creative analysis report with fatigue indicators
- Current creative inventory with launch dates and performance trends
- Historical fatigue timelines: average days until creative performance declines
- Creative production capacity and turnaround times
- Campaign spend levels: higher spend accelerates fatigue
- Platform-specific fatigue patterns and frequency data

## Steps
1. Analyze historical data to determine average creative lifespan by format and platform
2. Define fatigue detection triggers: CTR decline percentage, CPA increase threshold, frequency ceiling
3. Set up automated monitoring rules for fatigue indicators in dashboards
4. Calculate required creative production volume based on spend level and fatigue rate
5. Build a refresh calendar with planned creative replacement dates
6. Define the creative pipeline lead time: days from brief to live asset
7. Plan evergreen creatives that resist fatigue for sustained background performance
8. Design the iteration strategy: how to create variants of winners before they fatigue
9. Set rules for creative retirement: when to pause vs when to rest and re-launch
10. Coordinate refresh timing with seasonal events and promotional calendar
11. Establish the creative backlog buffer: always have N ready creatives in reserve
12. Define roles and responsibilities for refresh execution and monitoring

## Output
Refresh calendar containing: creative lifespan benchmarks, fatigue detection rules, production volume requirements, monthly refresh schedule, evergreen creative strategy, iteration pipeline, retirement rules, and backlog buffer targets.

## Quality Gate
- Creative refresh checklist confirms fatigue detection rules are actionable and measurable
- Production capacity validated as sufficient for projected refresh volume
- Ad Midas approves the balance between iteration and net-new creative approaches

## Duration
2-3 hours for planning; 1 hour for calendar creation and documentation
