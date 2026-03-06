# Scaling Layer

> **Type**: Stack Layer
> **Domain**: Growth — Strategic Scaling Operations
> **Used by agents**: Scale Optimizer, Mandali, Traffic Chief, Media Buyer

## Overview

The Scaling Layer governs the strategic expansion of proven campaigns beyond their initial parameters. While the `scaling-playbook.md` provides tactical rules for budget increases, this layer addresses the strategic dimensions of growth: when to scale, which direction to scale, how to maintain efficiency during rapid growth, and when to diversify. This is an ongoing layer that activates once campaigns demonstrate repeatable, profitable performance.

## When to Use

- Campaigns achieving target CPA/ROAS consistently for 2+ weeks
- Client growth mandate requiring increased volume
- Market opportunity window (seasonal, competitive exit, trending demand)
- Single-channel dependency creating business risk
- After optimization layer has maximized current campaign performance

## The Framework

### Scaling Readiness Assessment

Before entering the Scaling Layer, verify these prerequisites:

| Prerequisite | Threshold | Status Check |
|-------------|-----------|-------------|
| Performance stability | CPA within target for 14+ consecutive days | Review daily logs |
| Creative depth | 5+ winning ads active across 3+ formats | Creative inventory audit |
| Audience headroom | Current reach < 50% of total addressable | Platform audience size tools |
| Tracking reliability | Platform vs CRM variance < 20% | Monthly tracking audit |
| Creative pipeline capacity | Can produce 15+ new concepts/month | Pipeline assessment |
| Budget ceiling | Client approved increased spend | Written confirmation |
| Operations capacity | Team can monitor increased volume | Resource planning |

### Scaling Dimensions

#### Dimension 1: Vertical Scaling (Budget Depth)

Scale existing winning campaigns with increased budgets following `scaling-playbook.md` tactical rules.

**Strategic Considerations**:
- Vertical scaling has diminishing returns — each additional dollar produces less marginal return.
- Track marginal CPA: the cost of each additional conversion, not just average CPA.
- When marginal CPA exceeds 130% of average CPA, vertical scaling is approaching ceiling.
- Shift focus to horizontal dimensions before forcing vertical beyond ceiling.

#### Dimension 2: Horizontal Scaling (New Audiences)

**Expansion Sequence**:
1. Next LAL percentage (1% > 2-3% > 5% > 10%)
2. Interest-based audiences not yet tested
3. Broad targeting (if pixel data is sufficient)
4. New demographic segments within existing geo
5. Custom intent audiences (Google) with new keyword themes

**Rules**:
- Test one new audience per campaign per week maximum.
- Give each new audience 7 days and $500 minimum before evaluation.
- Do not retire existing winning audiences to fund new tests — add budget incrementally.

#### Dimension 3: Channel Diversification

**When to Add a Channel**:
- Primary channel produces consistent results for 30+ days.
- Single channel represents > 70% of total ad spend (concentration risk).
- Target audience is active on additional platforms (verified in discovery).
- Creative assets can be adapted to new platform format requirements.

**Expansion Priority Order**:
1. Meta > Google Search (or reverse, depending on where you started)
2. Google Shopping / PMax (ecommerce)
3. YouTube (video-ready brands)
4. TikTok (younger demos, trending products)
5. LinkedIn (B2B high-ticket)
6. Programmatic Display (scale reach)

**Budget for New Channel**: Start at 15-20% of total budget. Scale independently based on that channel's performance. Do not subsidize underperforming channels with primary channel budget.

#### Dimension 4: Creative System Scaling

As spend increases, creative volume must increase proportionally.

| Monthly Spend | Required Creative Velocity | Formats Active | Creators/Producers |
|--------------|--------------------------|---------------|-------------------|
| $10-25K | 10-12 concepts/month | 2-3 | 1-2 |
| $25-50K | 15-20 concepts/month | 3-4 | 2-3 |
| $50-100K | 20-30 concepts/month | 4-5 | 3-5 |
| $100K+ | 30+ concepts/month | 5+ | 5+ |

Creative is the fuel of scaling. Budget increases without creative increases lead to fatigue-driven CPA increases.

#### Dimension 5: Geographic Expansion

**Readiness Criteria**:
- Domestic market performing at or below target CPA.
- Product/service deliverable in target geography.
- Landing page and checkout localized (language, currency, shipping).
- Policy compliance verified for target country.

**Expansion Approach**:
- Start with same-language countries (US > UK > AU > CA for English).
- Separate campaigns per country — never mix geos in one campaign.
- Allow 2-4 weeks for new geo to establish performance baseline.
- Localize creative — do not assume domestic ads work in new markets.

#### Dimension 6: International Scaling

Beyond same-language expansion:
- Requires localized creative, landing pages, and customer support.
- Partner with local translators — do not rely on automated translation for ad copy.
- Research platform dominance by country (Meta dominant globally, but LINE in Japan, VK in Russia, etc.).
- Tax, legal, and payment processing must be resolved before advertising.
- Create separate ad accounts per major market for clean reporting.

### Mandali Scaling Recipes

Reference Mandali agent for specific scaling recipes:
- **The Audience Ladder**: Systematic expansion through audience layers with budget gates.
- **The Creative Blitz**: Concentrated creative production to support rapid budget increase.
- **The Geo Expansion**: Structured international rollout with localization gates.
- **The Channel Bridge**: Methodology for launching secondary channels using primary channel learnings.
- **The Offer Matrix**: Testing offer variations to unlock new CPA ceilings during scale.

### Stop-Loss at Scale

Scaling amplifies risk. Larger budgets mean larger potential losses.

- **Daily Dollar Limit**: Maximum acceptable daily loss = 2x daily target spend.
- **Weekly Review**: If blended CPA exceeds 120% of target for a full week, halt scaling and revert to last stable state.
- **Channel Kill Switch**: If a new channel fails to reach 80% of target CPA within 30 days, pause and reassess.
- **Diversification Minimum**: No single campaign should represent more than 40% of total spend at scale.

## Key Concepts

- **Scale Is Not Linear**: Doubling budget does not double results. Expect 60-80% of proportional return during aggressive scaling.
- **Creative Velocity = Scaling Velocity**: You can only scale as fast as you can produce winning creative.
- **Diversification Reduces Risk**: Multi-channel, multi-creative, multi-audience diversification protects against platform changes, algorithm shifts, and audience fatigue.
- **Mandali Recipes**: Structured scaling patterns that have been proven across multiple accounts. Use them rather than improvising.

## Decision Rules

1. Scaling readiness assessment must pass before entering this layer.
2. Vertical scaling first (simpler), horizontal when vertical plateaus.
3. Never scale without proportional creative pipeline increase.
4. Channel diversification is mandatory once primary channel exceeds 70% of spend.
5. Geographic expansion requires localized assets — no exceptions.
6. Stop-loss protocols from `scaling-playbook.md` remain active during all scaling phases.

## Common Mistakes

- Scaling budget without scaling creative — guaranteed fatigue and CPA increase.
- Expanding to 4+ channels simultaneously without establishing any of them.
- Forcing vertical scaling past the ceiling instead of shifting to horizontal.
- Not tracking marginal CPA — average CPA masks diminishing returns.
- Assuming domestic creative works in international markets without localization.
- Ignoring diversification and concentrating risk in one campaign or platform.

## Integration

- Tactical execution follows `scaling-playbook.md` rules.
- Creative velocity managed through `creative-production-pipeline.md` and `creative-layer.md`.
- Audience expansion per `audience-building-system.md`.
- New channel setup follows respective account structure frameworks.
- Performance monitoring per `pacing-and-guardrails.md` with scaling-adjusted thresholds.
- Strategic direction from `strategy-layer.md` updated to reflect scaling decisions.
- Financial oversight via `governance-layer.md`.

## Output

- Scaling readiness assessment document.
- Scaling roadmap with prioritized dimensions and timeline.
- Channel diversification plan with budget allocation per channel.
- Creative velocity plan aligned to spend trajectory.
- Geographic expansion plan with localization requirements.
- Weekly scaling performance report with marginal CPA tracking.
- Stop-loss incident log with actions and outcomes.
