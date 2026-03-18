# Horizontal Scaling

> **Type**: Task
> **Category**: scaling
> **Agents**: Scale Optimizer, Traffic Chief
> **Frameworks**: Horizontal Expansion Framework, Audience Diversification
> **Checklists**: horizontal-scaling-checklist
> **Output template**: templates/expansion-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.horizontal-scaling`
> **Agents**: [scale-optimizer](../../agents/scale-optimizer.md), [traffic-chief](../../agents/traffic-chief.md)
> **Frameworks**: `scaling-playbook`, `audience-building-system`
> **Checklists**: `scaling-quality`
> **Templates**: `plans/scaling-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Scale horizontally by expanding into new audiences, geographic markets, ad formats, and placements to increase total addressable reach while maintaining performance efficiency across the expanded portfolio.

## Inputs
- Current campaign performance data with audience saturation indicators
- Scaling strategy with horizontal expansion roadmap
- ICP research for potential new audience segments
- Platform audience size estimates for expansion targets
- Creative assets adaptable to new formats and placements
- Budget available for horizontal expansion testing

## Steps
1. Identify horizontal scaling opportunities: new audiences, geos, formats, placements, dayparts
2. Prioritize opportunities by estimated reach, expected performance, and implementation effort
3. Design test campaigns for each expansion opportunity with proper isolation
4. Audience expansion: test broader targeting, new interest stacks, new lookalike sources
5. Geographic expansion: test new regions, cities, or countries with localized considerations
6. Format expansion: test new ad formats (Reels, Stories, Shorts) with adapted creatives
7. Placement expansion: test new placements (Audience Network, Discovery, Explore)
8. Set test budgets sufficient for statistical significance within reasonable timeframes
9. Define success criteria: CPA or ROAS thresholds that justify continued investment
10. Launch expansion tests with proper tracking and naming conventions
11. Evaluate results after sufficient data collection (minimum 50 conversions or 7 days)
12. Graduate successful tests to ongoing campaigns and sunset failures

## Output
Expansion plan containing: prioritized opportunity list, test campaign designs, budget allocations, success criteria, launch timeline, evaluation schedule, and graduation/sunset decision framework.

## Quality Gate
- Horizontal scaling checklist confirms all expansion opportunities evaluated
- Test designs isolate variables for clear learnings
- Traffic Chief approves expansion priorities align with growth strategy

## Duration
2-3 hours for planning; ongoing 1-2 hours per week for test management and evaluation
