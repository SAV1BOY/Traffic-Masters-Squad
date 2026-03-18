# Scaling Strategy

> **Type**: Task
> **Category**: strategy
> **Agents**: Scale Optimizer, Mandalia, Traffic Chief
> **Frameworks**: Scaling Recipes, Mandalia Scaling Principles
> **Checklists**: scaling-strategy-checklist
> **Output template**: templates/scaling-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.scaling-strategy`
> **Agents**: [scale-optimizer](../../agents/scale-optimizer.md), [depesh-mandalia](../../agents/depesh-mandalia.md), [traffic-chief](../../agents/traffic-chief.md)
> **Frameworks**: `mandalia-scaling-recipes`, `scaling-playbook`, `kusmich-ponds-lakes-oceans`
> **Checklists**: `scaling-quality`, `mandalia/mandalia-cbo-recipes-selection`
> **Templates**: `plans/scaling-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Plan the scaling approach for proven campaigns, defining vertical and horizontal scaling methods, budget increase cadence, performance guardrails, and contingency plans to grow spend while maintaining efficiency targets.

## Inputs
- Current campaign performance data with proven winners identified
- Current daily and monthly spend levels
- Target scale: desired daily/monthly spend and volume
- Historical scaling attempts and outcomes (if available)
- Creative production capacity
- Platform-specific scaling constraints and best practices

## Steps
1. Identify campaigns eligible for scaling: minimum performance history and statistical significance
2. Define vertical scaling plan: budget increase percentages and cadence (10-20% every 3-5 days)
3. Define horizontal scaling plan: new audiences, geos, placements, and formats to test
4. Set performance guardrails: maximum acceptable CPA/ROAS degradation during scaling
5. Establish the lookback window for evaluating scaling impact (3-day, 7-day, 14-day)
6. Plan creative pipeline requirements to support increased spend without fatigue
7. Define the kill criteria: when to stop scaling and stabilize or pull back
8. Map scaling stages: $100/day to $500/day to $1K/day to $5K/day with different rules per stage
9. Plan for learning phase resets and how to minimize their impact
10. Design the scaling dashboard with early warning indicators
11. Document contingency plans for performance drops during scaling

## Output
Scaling plan containing: eligible campaign list, vertical scaling schedule, horizontal expansion roadmap, performance guardrails, kill criteria, creative pipeline requirements, stage-gate thresholds, and contingency playbook.

## Quality Gate
- Scaling strategy checklist confirms all scaling methods and guardrails defined
- Creative pipeline capacity validated against projected spend increases
- Traffic Chief approves scaling targets and risk tolerance levels

## Duration
3-4 hours for strategy development; 1-2 hours for documentation
