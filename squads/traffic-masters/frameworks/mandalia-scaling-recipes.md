# Scaling Recipes

> **Author**: Depesh Mandalia
> **Domain**: Budget Scaling and Campaign Expansion
> **Used by agents**: media-buyer, performance-analyst, strategy-orchestrator
> **Checklists**: scaling-checklist, budget-management-checklist

## Overview

Scaling Recipes is Depesh Mandalia's collection of proven strategies for increasing ad spend while maintaining performance. Each recipe addresses a different scaling scenario — from cautious vertical increases to aggressive horizontal expansion. The key insight: scaling is not just "spend more money." Each approach has specific conditions, setup requirements, and stop-loss criteria.

## When to Use

- A campaign has graduated from testing and is ready for more budget
- Client wants to increase spend but maintain CPA/ROAS targets
- Performance is strong and there is headroom to grow
- You need to expand reach beyond current audience pools
- Seasonal or promotional pushes require rapid scale-up

## The Framework

### Recipe 1: V-Scale (Vertical Scaling)
1. **When**: Winning ad set with consistent results, moderate headroom
2. **Setup**: Increase budget on the existing winning ad set
3. **Budget rule**: Maximum 20% increase per move, no more than once per 48-72 hours
4. **Stop-loss**: If CPA increases 30%+ after a budget bump, revert to previous budget
5. **Expected outcome**: Gradual, stable growth in volume at similar CPA
6. **Best for**: Steady, predictable scaling without disrupting the algorithm
7. **Risk level**: Low

### Recipe 2: Nitro (Aggressive Vertical)
1. **When**: Proven winner with clear headroom, time-sensitive opportunity, strong data
2. **Setup**: Larger budget increases on winning ad sets (50-100% jumps)
3. **Budget rule**: Only apply to ad sets with 50+ conversions and stable CPA for 14+ days
4. **Stop-loss**: If CPA exceeds 1.5x target for 3 consecutive days, cut back to pre-Nitro level
5. **Expected outcome**: Rapid volume increase; expect CPA volatility for 3-5 days
6. **Best for**: Flash sales, product launches, seasonal peaks with proven creative
7. **Risk level**: High — requires close monitoring

### Recipe 3: H-Scale (Horizontal Scaling)
1. **When**: Winning creative but current audience is saturating
2. **Setup**: Duplicate winning ads into new ad sets with different audiences
3. **Audience expansion**: New lookalike percentages, new interest stacks, new geos
4. **Budget rule**: Each new ad set starts at the original winning budget level
5. **Stop-loss**: If a new ad set does not meet CPA benchmark within 5 days, cut it
6. **Expected outcome**: Broader reach at similar CPA; some ad sets will fail
7. **Best for**: Breaking through audience saturation ceilings
8. **Risk level**: Medium

### Recipe 4: M-Scale (Mixed Scaling)
1. **When**: Want to test variations of a winning formula without risking the original
2. **Setup**: Create new campaigns mirroring winners but with creative or audience variations
3. **Variations**: New hooks, new formats (video vs. image), new copy angles, new offers
4. **Budget rule**: New campaigns start at Phase 1 budget; only scale if they prove themselves
5. **Stop-loss**: Standard graduation testing criteria apply
6. **Expected outcome**: Discovery of new winning combinations that can be V-Scaled or H-Scaled
7. **Best for**: Building a portfolio of winners rather than depending on one
8. **Risk level**: Medium-low

### CBO vs. ABO Considerations
- **ABO (Ad Set Budget Optimization)**: More control, better for testing and initial scaling
- **CBO (Campaign Budget Optimization)**: Better for mature campaigns with proven ad sets
- Use ABO for V-Scale and Nitro (precise budget control per ad set)
- Use CBO for H-Scale when multiple ad sets need flexible allocation
- M-Scale can use either depending on the variation type

## Key Concepts

- **Never scale unproven concepts**: Only apply recipes to graduated winners
- **Budget increases reset learning**: Give the algorithm 48-72 hours to restabilize after changes
- **Audience saturation is the enemy of V-Scale**: Monitor frequency closely
- **H-Scale compensates for V-Scale limits**: When vertical hits a wall, go horizontal
- **Portfolio approach**: Use M-Scale to ensure you are never dependent on a single winner

## Decision Rules

- IF CPA is stable and frequency is below 2.0 THEN apply V-Scale
- IF CPA is stable and frequency is above 2.5 THEN apply H-Scale to new audiences
- IF there is a time-sensitive opportunity and the ad set has 50+ conversions THEN consider Nitro
- IF you have one dominant winner and no backup THEN prioritize M-Scale to build a portfolio
- IF V-Scale causes CPA spike after 72 hours THEN revert budget and try H-Scale instead
- IF H-Scale ad sets consistently fail THEN the creative may be audience-specific — create new creative

## Common Mistakes

- Applying Nitro to ad sets without sufficient conversion history
- Increasing budget more than 20% at a time on V-Scale and blaming the platform when CPA spikes
- Duplicating ad sets into the same audiences (audience overlap causes self-competition)
- Not setting stop-loss criteria before scaling (emotional decisions during volatility)
- Scaling and optimizing simultaneously (change one thing at a time)
- Ignoring frequency as an early warning signal of saturation

## Integration

- Depends on: mandalia-graduation-testing (only graduated concepts enter scaling)
- Feeds into: mandalia-punisher-method (scaled ad sets that underperform get punished)
- Feeds into: mandalia-4-funnel-system (scaling recipes apply differently per funnel)
- Connects to: kusmich-ponds-lakes-oceans (H-Scale is essentially moving from ponds to lakes to oceans)

## Output

- A scaling plan specifying which recipe to apply to each winning campaign
- Budget schedule with specific increase amounts and timing
- Stop-loss thresholds documented per campaign before scaling begins
- Weekly scaling report: budget changes, CPA impact, frequency trends, headroom assessment
