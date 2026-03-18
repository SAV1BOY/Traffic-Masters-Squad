# Meta Campaign Build

> **Type**: Task
> **Category**: setup
> **Agents**: Media Buyer, Pixel Specialist, Pittman
> **Frameworks**: Meta Campaign Architecture, CBO/ABO Strategy
> **Checklists**: meta-campaign-build-checklist
> **Output template**: templates/campaign-build-sheet.md

## ROUTING (from config.yaml)

> **Config key**: `routing.meta-campaign-build`
> **Agents**: [media-buyer](../../agents/media-buyer.md), [pixel-specialist](../../agents/pixel-specialist.md), [molly-pittman](../../agents/molly-pittman.md)
> **Frameworks**: `account-structure-meta`, `pittman-ad-grid-7-steps`, `pittman-traffic-temperature`
> **Checklists**: `campaign-build-quality`, `meta/meta-account-structure-quality`, `meta/meta-capi-quality`, `pittman/pittman-traffic-temperature-mapping`
> **Templates**: `ads/meta-ad-template`, `naming/campaign-naming-standard`
> **Registry**: `data/registries/campaigns-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Build Meta (Facebook/Instagram) campaigns with proper structure, audience targeting, creative assignments, tracking configuration, and bid strategy to launch prospecting and retargeting campaigns according to the acquisition plan.

## Inputs
- Acquisition plan with Meta-specific strategy
- Creative assets: images, videos, copy variants
- Audience definitions: interests, lookalikes, custom audiences, broad
- Pixel and CAPI setup confirmation
- Budget allocation for Meta campaigns
- Landing page URLs with UTM parameters

## Steps
1. Create campaign structure following the approved architecture: CBO vs ABO decisions per campaign
2. Set campaign objectives aligned with funnel stage: awareness, traffic, leads, conversions, sales
3. Build prospecting ad sets with defined audiences: broad, interest stacks, lookalike tiers
4. Build retargeting ad sets with window-based custom audiences and proper exclusions
5. Upload creative assets and build ad variations with proper naming conventions
6. Configure conversion events and optimization targets per ad set
7. Set bid strategy: lowest cost, cost cap, bid cap, or ROAS target per campaign
8. Apply budget allocations: campaign-level budgets for CBO, ad-set-level for ABO
9. Configure placement selections: automatic vs manual based on creative format
10. Set up UTM parameters consistently across all ads for GA4 tracking
11. Verify pixel fires correctly on all landing pages before going live
12. Set campaign and ad set naming conventions for reporting clarity

## Output
Live Meta campaigns with: documented campaign structure, audience targeting details, creative assignments, tracking verification, bid and budget settings, UTM conventions, and naming convention reference.

## Quality Gate
- Meta campaign build checklist confirms all elements configured
- Pixel Specialist verifies tracking fires correctly on all destinations
- Pittman reviews ad copy alignment with offer strategy

## Duration
4-6 hours for build; 1-2 hours for QA and verification
