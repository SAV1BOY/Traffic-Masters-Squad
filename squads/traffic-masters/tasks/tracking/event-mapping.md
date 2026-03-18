# Event Mapping

> **Type**: Task
> **Category**: tracking
> **Agents**: Pixel Specialist
> **Frameworks**: Event Taxonomy Framework, Data Layer Architecture
> **Checklists**: event-mapping-checklist
> **Output template**: templates/event-map.md

## ROUTING (from config.yaml)

> **Config key**: `routing.event-mapping`
> **Agents**: [pixel-specialist](../../agents/pixel-specialist.md)
> **Frameworks**: `tracking-stack-standard`
> **Checklists**: `tracking-plan-quality`
> **Templates**: `tracking/event-map-template`, `tracking/data-layer-spec-template`
> **Registry**: `data/registries/pixels-and-events-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Map all trackable events and their parameters across the entire funnel, defining naming conventions, trigger conditions, parameter schemas, and platform-specific implementations to create a single source of truth for measurement.

## Inputs
- Funnel map with all conversion points
- Measurement plan with KPI definitions
- Website or app technical architecture
- Platform list requiring event tracking
- E-commerce product catalog structure (if applicable)
- CRM and backend systems with conversion data

## Steps
1. List every user action worth tracking across the funnel from landing to post-purchase
2. Define a consistent naming convention: snake_case, platform prefixes, category groupings
3. Map standard events per platform: Meta (ViewContent, AddToCart, Purchase), Google (page_view, purchase), TikTok (CompletePayment)
4. Define custom events for business-specific actions not covered by standard events
5. Specify parameters for each event: value, currency, content_id, content_type, content_name
6. Document trigger conditions: what user action fires each event and on which page
7. Define the data layer schema for GTM implementation
8. Map event deduplication rules: how to prevent double-firing across browser and server
9. Specify which events serve as optimization targets per platform
10. Document event priority hierarchy for attribution and reporting
11. Create a cross-platform event mapping table showing equivalent events across platforms

## Output
Event map containing: complete event inventory, naming convention guide, parameter schemas per event, trigger conditions, data layer specification, platform-specific implementation notes, deduplication rules, and cross-platform equivalence table.

## Quality Gate
- Event mapping checklist confirms all funnel stages have corresponding events
- Naming conventions are consistent and documented
- Pixel Specialist verifies technical feasibility of all event implementations

## Duration
2-4 hours for mapping; 1-2 hours for documentation and cross-platform alignment
