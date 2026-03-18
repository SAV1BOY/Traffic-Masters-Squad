# Acquisition Plan

> **Type**: Task
> **Category**: strategy
> **Agents**: Traffic Chief, Pittman, Burns
> **Frameworks**: Traffic Engine, CaAMP (Campaign Architecture and Media Planning)
> **Checklists**: acquisition-plan-checklist
> **Output template**: templates/acquisition-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.acquisition-plan`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [molly-pittman](../../agents/molly-pittman.md), [ralph-burns](../../agents/ralph-burns.md)
> **Frameworks**: `pittman-traffic-engine-9-steps`, `burns-caamp`, `ltv-cac-unit-economics`, `full-funnel-ads-strategy`
> **Checklists**: `acquisition-strategy-quality`, `offer-quality`, `budget-pacing-quality`
> **Templates**: `briefs/acquisition-strategy-brief`, `plans/media-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Develop a full acquisition strategy defining channels, campaign architecture, budget allocation, KPI targets, and timeline that aligns paid media investment with business growth objectives.

## Inputs
- ICP and avatar research document
- Platform feasibility assessment
- Offer hypothesis document
- Business goals: revenue targets, CPA/ROAS targets, growth rate
- Available monthly budget for paid media
- Funnel and conversion data (if existing)

## Steps
1. Define primary and secondary acquisition channels based on platform feasibility
2. Set KPI targets per channel: CPA, ROAS, CPL, conversion rate, volume targets
3. Design campaign architecture per channel using CaAMP framework
4. Map campaign types to funnel stages: prospecting, engagement, conversion, retention
5. Allocate budget across channels using the 70/20/10 rule (proven/testing/experimental)
6. Define audience strategy per channel: broad, interest, lookalike, custom, remarketing
7. Plan creative requirements per campaign type and channel
8. Set measurement framework: primary and secondary KPIs, attribution model
9. Build a 90-day launch timeline with milestones and checkpoints
10. Define decision criteria for scaling, pausing, or pivoting each channel
11. Document risk factors and contingency plans

## Output
Acquisition plan containing: channel strategy with rationale, campaign architecture diagrams, budget allocation table, KPI targets per channel, 90-day timeline, audience strategy, creative requirements summary, and decision framework for ongoing management.

## Quality Gate
- Acquisition plan checklist confirms all strategic elements addressed
- Burns validates unit economics and nCAC projections are realistic
- Traffic Chief approves overall strategy alignment with business objectives

## Duration
4-6 hours for strategy development; 2 hours for documentation and review
