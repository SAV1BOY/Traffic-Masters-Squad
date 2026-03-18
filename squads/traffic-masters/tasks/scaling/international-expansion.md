# International Expansion

> **Type**: Task
> **Category**: scaling
> **Agents**: Traffic Chief, Media Buyer
> **Frameworks**: International Expansion Framework, Localization Strategy
> **Checklists**: international-expansion-checklist
> **Output template**: templates/international-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.international-expansion`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [media-buyer](../../agents/media-buyer.md)
> **Frameworks**: `omnichannel-media-strategy`, `scaling-playbook`
> **Checklists**: `cross-platform-consistency-quality`, `compliance-ad-policies-quality`
> **Templates**: `plans/scaling-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Expand advertising campaigns into new international markets by evaluating market viability, adapting creative and messaging for local audiences, configuring proper tracking and currency handling, and managing multi-market campaign operations.

## Inputs
- Current market performance as a baseline
- Target market list with business viability assessment
- Market-specific data: population, internet penetration, platform usage, purchasing power
- Language and cultural considerations per target market
- Legal and regulatory requirements per market
- Shipping, pricing, and operational readiness per market

## Steps
1. Evaluate target markets on: audience size, platform availability, CPM levels, competitive landscape
2. Assess operational readiness: can the business fulfill orders and support customers in each market
3. Research platform-specific dynamics per market: which platforms dominate, local alternatives
4. Plan creative localization: translation, cultural adaptation, local proof elements, imagery
5. Configure currency and pricing for each market in landing pages and tracking
6. Set up market-specific tracking: separate campaigns, UTM parameters, currency conversion in analytics
7. Research local regulations: GDPR (EU), LGPD (Brazil), PIPL (China), local ad policies
8. Build market-specific audiences: local interests, behaviors, lookalikes from local converters
9. Adapt bidding strategy for local auction dynamics and CPM levels
10. Launch pilot campaigns in top priority markets with conservative budgets
11. Set up reporting to compare cross-market performance normalized by purchasing power
12. Define market graduation criteria and timeline for full rollout

## Output
International plan containing: market evaluation matrix, localization requirements, tracking configuration, regulatory compliance notes, pilot campaign designs, cross-market reporting framework, and graduation criteria.

## Quality Gate
- International expansion checklist confirms all markets evaluated on all criteria
- Localization reviewed by native speakers or cultural consultants
- Traffic Chief validates expansion aligns with business operational capacity

## Duration
4-8 hours for planning per market; pilots run 2-4 weeks per market
