# Scaling Playbook

> **Type**: Internal
> **Domain**: Media Buying — Budget Scaling
> **Used by agents**: Media Buyer, Traffic Chief, Scale Optimizer, Performance Analyst, Mandali

## Overview

A rule-based system for scaling ad spend while maintaining target CPA/ROAS. Scaling is the highest-risk phase in paid media — move too fast and you trigger algorithmic resets and CPA spikes; move too slow and you miss market windows. This playbook defines vertical scaling (more budget to winners), horizontal scaling (new dimensions), and stop-loss protocols. Connects to Mandali methodology for scaling recipes.

## When to Use

- Campaigns achieving target CPA/ROAS for 5+ consecutive days
- Client requests budget increase or growth acceleration
- Seasonal opportunity windows (BFCM, Q4, product launches)
- After creative testing identifies multiple winning assets
- When current spend covers less than 30% of addressable audience

## The Framework

### Vertical Scaling (Budget Increases)

**Rule**: Increase budget by 15-20% every 3 days if CPA remains within target range.

| Day | Action | Condition |
|-----|--------|-----------|
| Day 1-5 | Hold — establish baseline | CPA within target, 50+ conversions |
| Day 6 | +15% budget increase | CPA within 100% of target |
| Day 9 | +15% budget increase | CPA within 110% of target |
| Day 12 | +20% budget increase | CPA within 110% of target |
| Day 15 | +20% budget increase | CPA within 120% of target |
| Day 18+ | Continue +20% every 3 days | Monitor daily |

**Hard Ceiling**: Never increase budget more than 50% in a single change. Algorithmic learning resets above this threshold on Meta.

**CBO Scaling**: Increase campaign budget. Let Meta redistribute across ad sets. Add minimum spend floors to protect proven ad sets.

**ABO Scaling**: Duplicate winning ad set with higher budget rather than editing existing. Run parallel for 3 days, then pause underperformer.

### Horizontal Scaling (New Dimensions)

Expand across new axes when vertical scaling plateaus or CPA begins rising:

1. **New Audiences**: Next LAL percentage, new interest stacks, untested custom intent groups. Follow `audience-building-system.md` layer progression.
2. **New Placements**: Instagram Reels, Facebook Marketplace, Audience Network, YouTube Shorts, Discovery. Test one new placement at a time.
3. **New Geos**: Expand to adjacent markets. Start with same-language countries. Separate campaigns per geo for clean data.
4. **New Creatives**: Launch 3-5 new creative variations per week during scaling phase. Creative is the scaling lever.
5. **New Platforms**: Expand to Google if scaling Meta, or vice versa. Follow respective account structure frameworks.
6. **New Offers**: Test offer variations (pricing, bundles, free shipping thresholds) to unlock new CPA ceilings.

### Stop-Loss Protocol

| Condition | Action | Timeline |
|-----------|--------|----------|
| CPA > 120% of target | Reduce budget by 20% | Immediate |
| CPA > 150% of target for 1 day | Pause, investigate | Same day |
| CPA > 150% of target for 3 days | Kill campaign, revert to last stable state | Day 3 |
| ROAS < 80% of target for 3 days | Reduce budget 30%, refresh creative | Day 3 |
| Frequency > 4x/week (prospecting) | Expand audience or pause | Immediate |
| CTR drops > 30% from baseline | Creative fatigue — rotate assets | Same day |

### Diversification Triggers

When any single campaign represents more than 60% of total spend, trigger diversification:
- Launch new campaign on same platform with different structure
- Allocate 20% of budget to secondary platform
- Test new funnel (different landing page, offer, or product)

## Key Concepts

- **Mandali Connection**: Scaling recipes from Mandali methodology — each recipe is a proven scaling pattern (e.g., "The Audience Ladder", "The Creative Blitz", "The Geo Expansion"). Reference Mandali agent for specific recipe selection.
- **Learning Phase**: Meta requires 50 conversions per week per ad set to exit learning. During scaling, maintain this threshold or consolidate.
- **Scaling Ceiling**: Every audience-creative combination has a natural ceiling. Recognize it and shift to horizontal scaling rather than forcing vertical.
- **Algorithmic Patience**: After budget changes, wait 72 hours before evaluating. Day 1 after a change is unreliable data.

## Decision Rules

1. Never scale a campaign with fewer than 5 days of stable performance data.
2. Always have 3+ winning creatives before scaling — single-creative scaling is fragile.
3. Vertical scaling first (simpler, faster), horizontal scaling when vertical plateaus.
4. Stop-loss rules are non-negotiable. No exceptions without Traffic Chief approval.
5. During BFCM or peak seasons, increase budgets 3-5 days before the event, not during.
6. Track blended CPA/ROAS across all campaigns, not just the scaled one.

## Common Mistakes

- Increasing budget by 50-100% in one jump, triggering learning phase reset.
- Scaling without creative depth — one winning ad cannot sustain increased spend.
- Ignoring frequency as a scaling constraint.
- Not having stop-loss rules pre-defined, leading to emotional decisions.
- Scaling on weekends or holidays when team cannot monitor.
- Celebrating single-day results without waiting for the 3-day stabilization window.

## Integration

- Budget increases follow structure in `account-structure-meta.md` and `account-structure-google.md`.
- Audience expansion sequence in `audience-building-system.md`.
- Creative refresh rate increases per `creative-production-pipeline.md`.
- Pacing monitored via `pacing-and-guardrails.md` with scaling-specific thresholds.
- Connects to `scaling-layer.md` for strategic scaling decisions.

## Output

- Scaling log with daily budget, CPA, ROAS, and actions taken.
- Stop-loss alert history with outcomes.
- Horizontal expansion roadmap with prioritized dimensions.
- Weekly scaling report to Traffic Chief and client stakeholders.
- Diversification tracker showing spend distribution across campaigns/platforms.
