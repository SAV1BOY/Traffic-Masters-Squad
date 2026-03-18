# Offer Research

> **Type**: Task
> **Category**: research
> **Agents**: Pittman, Mandalia
> **Frameworks**: Pittman Offer Stack, Mandalia Offer Mapping
> **Checklists**: offer-research-checklist
> **Output template**: templates/offer-hypothesis-document.md

## ROUTING (from config.yaml)

> **Config key**: `routing.offer-research`
> **Agents**: [molly-pittman](../../agents/molly-pittman.md), [depesh-mandalia](../../agents/depesh-mandalia.md), [traffic-chief](../../agents/traffic-chief.md)
> **Frameworks**: `pittman-offer-formula`, `mandalia-ac4`, `offer-and-proof-stack`
> **Checklists**: `offer-quality`, `pittman/pittman-offer-formula-audit`
> **Templates**: `briefs/acquisition-strategy-brief`
> **Registry**: `data/research/offer-research`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Research and document competitor offers, available proof elements, guarantee options, and pricing structures to develop a differentiated offer hypothesis that maximizes conversion potential.

## Inputs
- Product or service details and current pricing
- Competitor list with known offers
- Customer reviews mentioning value perception
- Sales data on objections and conversion barriers
- Industry benchmarks for pricing and guarantees

## Steps
1. Audit all direct competitor offers: pricing, bonuses, guarantees, urgency mechanisms
2. Document competitor offer stacks including main offer, bonuses, and risk reversal
3. Catalog available proof elements: testimonials, case studies, data points, certifications
4. Research guarantee options viable for the business: money-back, results-based, conditional
5. Analyze pricing psychology: anchoring, decoy, bundle vs unbundle strategies
6. Identify the primary objection the offer must overcome based on avatar research
7. Draft three offer hypotheses ranked by predicted conversion impact
8. Map each hypothesis to a Pittman offer stack structure
9. Define the proof hierarchy: which proof elements support which claims
10. Document risk factors and policy considerations for each offer variant

## Output
Offer hypothesis document containing: competitor offer audit, proof inventory, guarantee options matrix, three ranked offer hypotheses with full stack details, pricing rationale, and recommended test plan for offer variants.

## Quality Gate
- Offer research checklist confirms at least five competitor offers documented
- Each hypothesis includes complete offer stack with proof and guarantee
- Pittman reviews offer logic; Mandalia validates emotional alignment with avatar

## Duration
3-4 hours for research; 1-2 hours for hypothesis development and documentation
