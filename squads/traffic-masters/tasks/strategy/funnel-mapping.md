# Funnel Mapping

> **Type**: Task
> **Category**: strategy
> **Agents**: Traffic Chief, Pittman
> **Frameworks**: Customer Journey Framework, Funnel Types Classification
> **Checklists**: funnel-mapping-checklist
> **Output template**: templates/funnel-map.md

## ROUTING (from config.yaml)

> **Config key**: `routing.funnel-mapping`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [molly-pittman](../../agents/molly-pittman.md)
> **Frameworks**: `customer-journey-mapping`, `funnel-types-library`, `pittman-traffic-temperature`
> **Checklists**: `funnel-integrity-quality`
> **Templates**: `briefs/acquisition-strategy-brief`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Map the complete customer funnel from first ad impression to purchase and post-purchase, defining messaging at each stage, conversion events, expected drop-off rates, and optimization levers.

## Inputs
- ICP and avatar document with awareness levels
- Acquisition plan with channel strategy
- Offer hypothesis document
- Existing funnel data and conversion rates (if available)
- Landing page URLs and current flow

## Steps
1. Define the funnel type: direct response, lead gen, webinar, VSL, quiz, free trial, e-commerce
2. Map each stage of the funnel: awareness, interest, consideration, intent, purchase, retention
3. Define the primary message and emotional driver for each funnel stage
4. Identify the conversion event at each stage transition
5. Set expected conversion rates per stage based on benchmarks and historical data
6. Map traffic sources to funnel entry points
7. Define retargeting triggers at each drop-off point
8. Document the email/SMS touchpoints that support the funnel
9. Identify friction points and potential leaks in the current flow
10. Create a visual funnel diagram with metrics at each stage
11. Define A/B test opportunities at key conversion points

## Output
Funnel map containing: visual funnel diagram, stage-by-stage messaging guide, conversion event definitions, expected conversion rates, retargeting trigger map, friction point analysis, and test opportunity roadmap.

## Quality Gate
- Funnel mapping checklist confirms all stages documented with messaging
- Conversion events defined and measurable for each transition
- Pittman validates messaging alignment with offer strategy

## Duration
2-4 hours for mapping; 1-2 hours for documentation and visual creation
