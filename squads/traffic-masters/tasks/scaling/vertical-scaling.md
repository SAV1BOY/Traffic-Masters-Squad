# Vertical Scaling

> **Type**: Task
> **Category**: scaling
> **Agents**: Scale Optimizer, Mandalia
> **Frameworks**: Vertical Scaling Protocol, Budget Increase Cadence
> **Checklists**: vertical-scaling-checklist
> **Output template**: templates/scaling-actions.md

## ROUTING (from config.yaml)

> **Config key**: `routing.vertical-scaling`
> **Agents**: [scale-optimizer](../../agents/scale-optimizer.md), [depesh-mandalia](../../agents/depesh-mandalia.md)
> **Frameworks**: `mandalia-scaling-recipes`, `scaling-playbook`, `scaling-layer`
> **Checklists**: `scaling-quality`, `mandalia/mandalia-cbo-recipes-selection`
> **Templates**: `plans/scaling-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Scale budget vertically on proven winning campaigns by systematically increasing daily spend while monitoring for efficiency degradation, learning phase disruption, and audience saturation.

## Inputs
- Campaign performance data with proven winners identified (minimum 7 days above target)
- Current daily budgets and spend levels
- Target daily budget for each campaign
- Scaling strategy with guardrails and kill criteria
- Platform-specific scaling best practices
- Creative inventory supporting increased delivery

## Steps
1. Confirm campaign eligibility: consistent performance above target for minimum lookback window
2. Check creative health: sufficient creative volume to support increased delivery without fatigue
3. Review audience size: confirm target audience is large enough to absorb budget increase
4. Calculate the budget increase increment: 10-20% per step based on current spend level
5. Apply the first budget increase and document the starting performance baseline
6. Monitor for 48-72 hours post-increase: check CPA, ROAS, delivery, and learning phase status
7. If performance holds within guardrails, apply the next increment
8. If performance degrades beyond threshold, pause scaling and stabilize at previous level
9. Track the scaling curve: plot CPA against daily spend to identify diminishing returns
10. Adjust bid strategy if needed: move from lowest cost to cost cap at higher spend levels
11. Document each scaling step with performance data and decision rationale
12. Set the maximum viable daily budget based on efficiency floor analysis

## Output
Scaling actions log containing: campaign-by-campaign scaling steps, performance at each level, scaling curve visualization, maximum viable budget findings, and decision rationale for each action.

## Quality Gate
- Vertical scaling checklist confirms all guardrails monitored at each step
- No campaign scaled past the efficiency floor without explicit approval
- Mandalia validates audience targeting remains aligned at higher spend levels

## Duration
Ongoing process: 30-60 minutes per scaling step review, executed every 2-3 days per campaign
