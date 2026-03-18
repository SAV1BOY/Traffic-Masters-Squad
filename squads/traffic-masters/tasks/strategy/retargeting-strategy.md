# Retargeting Strategy

> **Type**: Task
> **Category**: strategy
> **Agents**: Mandalia, Media Buyer
> **Frameworks**: Infinity Retargeting Framework
> **Checklists**: retargeting-strategy-checklist
> **Output template**: templates/retargeting-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.retargeting-strategy`
> **Agents**: [depesh-mandalia](../../agents/depesh-mandalia.md), [media-buyer](../../agents/media-buyer.md)
> **Frameworks**: `mandalia-infinity-retargeting`, `retargeting-architecture`, `retargeting-sequence-system`
> **Checklists**: `retargeting-quality`
> **Templates**: `ads/retargeting-ad-template`
> **Registry**: `data/registries/audiences-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Plan a comprehensive retargeting strategy defining audience windows, segmentation logic, creative sequences, and frequency controls that systematically moves warm audiences toward conversion without causing fatigue.

## Inputs
- Funnel map with conversion events and drop-off points
- Pixel and tracking setup details
- Available audience sizes by engagement level
- Creative assets inventory
- Average sales cycle length
- Historical retargeting performance data (if available)

## Steps
1. Define retargeting audience windows: 1-3 days, 3-7 days, 7-14 days, 14-30 days, 30-60 days, 60-180 days
2. Segment audiences by engagement depth: page view, content view, add to cart, initiate checkout, past purchaser
3. Apply the Infinity Retargeting framework: sequence messages by awareness and intent level
4. Map creative sequences per segment: what message each audience sees and in what order
5. Design exclusion logic to prevent audience overlap and message confusion
6. Set frequency caps per window to prevent fatigue: impressions per day and per week
7. Define bid strategy adjustments by window: higher bids for shorter windows
8. Plan dynamic retargeting for product-specific remarketing (e-commerce)
9. Design cross-platform retargeting coordination: Meta, Google Display, YouTube
10. Set performance triggers: when to refresh creative, adjust windows, or pause segments
11. Calculate expected audience decay rates and plan for audience replenishment

## Output
Retargeting plan containing: audience window definitions, segmentation matrix, creative sequence maps per segment, exclusion logic rules, frequency cap settings, bid strategy guidelines, cross-platform coordination plan, and performance trigger definitions.

## Quality Gate
- Retargeting strategy checklist confirms all windows and segments defined
- Exclusion logic prevents audience overlap across campaigns
- Mandalia validates messaging sequence aligns with psychological progression

## Duration
3-4 hours for strategy development; 1-2 hours for documentation
