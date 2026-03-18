# Budget Reallocation

> **Type**: Task
> **Category**: optimization
> **Agents**: Scale Optimizer, Traffic Chief, Mandalia
> **Frameworks**: Budget Reallocation Model, Diminishing Returns Analysis
> **Checklists**: budget-reallocation-checklist
> **Output template**: templates/reallocation-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.budget-reallocation`
> **Agents**: [scale-optimizer](../../agents/scale-optimizer.md), [traffic-chief](../../agents/traffic-chief.md), [depesh-mandalia](../../agents/depesh-mandalia.md)
> **Frameworks**: `budget-allocation-model`, `mandalia-punisher-method`, `pacing-and-guardrails`
> **Checklists**: `budget-pacing-quality`, `mandalia/mandalia-punisher-optimization`
> **Templates**: N/A
> **Registry**: `data/registries/budgets-and-guardrails`, `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Reallocate budget across channels, campaigns, and ad sets based on performance data to shift spend from underperformers to proven winners while maintaining testing allocation and respecting platform learning requirements.

## Inputs
- Current budget allocation across all channels and campaigns
- Performance data: CPA, ROAS, conversion volume by campaign
- Budget allocation strategy with reallocation rules
- Minimum spend thresholds per campaign for statistical validity
- Learning phase status for each campaign
- Seasonal and promotional calendar context

## Steps
1. Export performance data for all campaigns over the analysis window (7-14 days)
2. Rank campaigns by efficiency: CPA or ROAS relative to targets
3. Identify campaigns significantly above target (candidates for budget increase)
4. Identify campaigns significantly below target (candidates for budget decrease or pause)
5. Check for campaigns in learning phase that need time before reallocation decisions
6. Analyze diminishing returns: campaigns where additional spend degrades efficiency
7. Calculate optimal budget shift amounts respecting platform daily change limits
8. Model projected impact of reallocation on total portfolio performance
9. Preserve testing budget allocation: do not cannibalize test budget for proven campaigns
10. Document reallocation decisions with rationale and expected impact
11. Execute budget changes with proper pacing to avoid learning phase resets
12. Set follow-up review date to evaluate reallocation impact

## Output
Reallocation plan containing: current vs proposed budget table, performance justification per change, projected impact model, execution timeline, preserved test budget, and follow-up review schedule.

## Quality Gate
- Budget reallocation checklist confirms all campaigns evaluated
- No campaign reduced below minimum viable spend threshold
- Traffic Chief approves reallocation aligns with strategic priorities

## Duration
1-2 hours for analysis and planning; 30 minutes for execution
