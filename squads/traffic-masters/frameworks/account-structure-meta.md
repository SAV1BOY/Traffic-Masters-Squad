# Account Structure — Meta (Facebook/Instagram)

> **Type**: Internal
> **Domain**: Media Buying — Meta Platforms
> **Used by agents**: Media Buyer, Traffic Chief, Performance Analyst

## Overview

Defines the standard hierarchy and organizational structure for Meta advertising accounts. A disciplined account structure prevents budget waste, simplifies reporting, and enables systematic scaling. Every Meta engagement follows this blueprint unless a documented exception is approved by Traffic Chief.

## When to Use

- New client onboarding (Meta channel)
- Account audits and restructures
- Scaling into new product lines or geos
- Transitioning from agency to in-house or vice versa

## The Framework

### Hierarchy

1. **Business Manager (BM)** — One per client entity. Houses all assets.
2. **Ad Accounts** — Separate by brand/product line or geo if spend justifies it. One primary, one backup minimum.
3. **Pixels** — One pixel per ad account. CAPI configured on all. Events verified via Events Manager and GTM.
4. **Campaigns** — Organized by objective and funnel stage.

### Campaign Structure

| Layer | Campaign Type | Objective | Budget Model |
|-------|--------------|-----------|--------------|
| Prospecting | Cold traffic | Conversions / Sales | CBO preferred |
| Retargeting | Warm audiences | Conversions / Sales | ABO for control |
| Testing | Creative/audience tests | Conversions | ABO with equal budgets |
| Scaling | Proven winners | Conversions / Sales | CBO with high budget |

### CBO vs ABO Decision

- **CBO (Campaign Budget Optimization)**: Use when you have 3+ ad sets with proven audiences and want Meta to allocate. Best for scaling.
- **ABO (Ad Set Budget Optimization)**: Use for testing (equal budget distribution), retargeting (controlled frequency), and when specific audience spend control is needed.

### Advantage+ Considerations

- Advantage+ Shopping Campaigns (ASC): Deploy for ecommerce with 100+ conversions/month. Provide existing customer list for exclusion.
- Advantage+ Audience: Allow as expansion layer, not primary targeting.
- Advantage+ Placements: Default ON unless creative is platform-specific.
- Monitor ASC closely — it can cannibalize retargeting pools.

## Key Concepts

- **Naming Convention**: `[Client]_[Funnel Stage]_[Objective]_[Audience]_[Date]` at campaign level. Ad set: `[Audience Type]_[Detail]`. Ad: `[Angle]_[Format]_[Version]`.
- **Budget Allocation**: 70% Prospecting, 20% Retargeting, 10% Testing as default split. Adjust based on funnel maturity.
- **Account Spend Limits**: Set at 2x daily target to prevent runaway spend. Raise incrementally.

## Decision Rules

1. New accounts start with ABO testing structure. Move to CBO after 3+ winning ad sets identified.
2. Never run more than 5-7 active ad sets per CBO campaign — dilution reduces learning.
3. Separate iOS 14.5+ campaigns if attribution windows differ (1-day click vs 7-day click).
4. Create dedicated Advantage+ campaign only after standard campaigns generate 50+ conversions/week.
5. Backup ad account must be warmed with low-spend evergreen campaign at all times.

## Common Mistakes

- Running too many campaigns simultaneously, fragmenting pixel learning.
- Mixing conversion objectives within a single campaign.
- Not excluding retargeting audiences from prospecting campaigns.
- Ignoring account spending limits — one bad day can drain monthly budget.
- Using Advantage+ too early before establishing baseline performance data.
- Failing to maintain naming conventions, making reporting impossible at scale.

## Integration

- Feeds into `scaling-playbook.md` for budget increase protocols.
- Pairs with `audience-building-system.md` for ad set audience configuration.
- Reporting structure aligns with `pacing-and-guardrails.md` thresholds.
- Creative testing methodology connects to `dynamic-creative-optimization.md`.

## Output

- Documented account map (BM > Accounts > Pixels > Campaigns) in client folder.
- Naming convention sheet shared with all agents touching the account.
- Budget allocation plan with CBO/ABO rationale per campaign.
- Quarterly audit checklist to verify structure integrity.
