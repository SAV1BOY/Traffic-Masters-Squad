# Retargeting Sequence Setup

> **Type**: Task
> **Category**: optimization
> **Agents**: Media Buyer, Mandalia
> **Frameworks**: Infinity Retargeting Framework, Sequential Messaging
> **Checklists**: retargeting-setup-checklist
> **Output template**: templates/retargeting-campaigns.md

## Objective
Set up retargeting campaigns with sequenced messaging by audience window, implementing exclusion logic, frequency controls, and creative rotation to systematically convert warm audiences through progressive persuasion.

## Inputs
- Retargeting strategy with window definitions and sequences
- Custom audience segments built from pixel data
- Creative assets mapped to each retargeting stage
- Exclusion audience lists: converters, irrelevant visitors
- Frequency cap guidelines from strategy
- Budget allocation for retargeting campaigns

## Steps
1. Build custom audiences for each retargeting window: 1-3d, 3-7d, 7-14d, 14-30d, 30-60d
2. Create exclusion audiences: purchasers, existing customers, bounced visitors under 5 seconds
3. Build campaign structure with separate ad sets per window and engagement level
4. Apply strict exclusion logic: each window excludes shorter windows and converters
5. Assign creative sequences per window following the progressive messaging plan
6. Configure frequency caps per ad set: daily and weekly impression limits
7. Set bid adjustments: higher bids for shorter windows with stronger intent signals
8. Set up dynamic product retargeting for e-commerce (DPA campaigns)
9. Configure cross-platform retargeting: Meta retargeting Google visitors and vice versa
10. Test exclusion logic by verifying audience overlap reports show clean separation
11. Set up monitoring for audience size decay and replenishment rates
12. Document the complete retargeting setup with audience definitions and creative mapping

## Output
Retargeting campaigns live with: audience window configurations, exclusion logic verified, creative sequence assignments, frequency cap settings, bid adjustments, cross-platform coordination, and monitoring dashboard.

## Quality Gate
- Retargeting setup checklist confirms all windows configured with proper exclusions
- Audience overlap reports show clean separation between windows
- Mandalia validates messaging progression matches psychological journey

## Duration
3-5 hours for setup; 1-2 hours for testing and verification
