# Retargeting Sequence Build
> **Type**: Workflow
> **Duration**: 3-4 business days
> **Agents involved**: traffic-chief, media-buyer, ad-midas

## Trigger
Cold traffic campaigns generating sufficient audience pools (1,000+ in each retargeting window).

## Steps
1. Audience Definition → Agent: traffic-chief → Framework: Sobral Funnel Windows → Output: Retargeting windows defined (1-3d, 4-7d, 8-14d, 15-30d, 31-60d, 61-180d)
2. Audience Creation → Agent: media-buyer → Framework: Custom Audience Builder → Output: Audiences created in platform with proper exclusions
3. Exclusion Logic → Agent: media-buyer → Framework: Funnel Exclusion Matrix → Output: Each stage excludes downstream audiences (retarget excludes converters)
4. Message Mapping → Agent: traffic-chief → Framework: Temperature-Based Messaging → Output: Message matrix mapping content type to each window
5. Creative Production → Agent: ad-midas → Framework: Retarget Creative Specs → Output: Creatives tailored per window (testimonials, urgency, objection handling)
6. Sequence Build → Agent: media-buyer → Framework: Sequential Exposure → Output: Campaigns built with frequency caps and sequential logic
7. Budget Allocation → Agent: media-buyer → Framework: Pool-Based Budgeting → Output: Budget split proportional to audience pool size
8. Launch and Monitor → Agent: media-buyer → Framework: GECO-ANA → Output: Retargeting live with daily monitoring

## Quality Gates
- [ ] All retargeting audiences have 1,000+ people minimum
- [ ] Exclusions properly set (no audience overlap)
- [ ] Frequency cap set (max 2-3 impressions per day)
- [ ] Message matches funnel stage (no hard sell to 1-day visitors)
- [ ] Converters excluded from all retargeting
- [ ] Dynamic product ads configured for e-commerce
- [ ] Privacy/LGPD compliant audience creation

## Output
Full retargeting sequence with documented audience windows, messaging, and creative per stage.
Budget allocation model based on pool sizes.
Performance benchmarks by retargeting stage.

## Retargeting Message Framework
- 1-3 days: Remind, reinforce value proposition
- 4-7 days: Social proof, testimonials, case studies
- 8-14 days: Objection handling, FAQ content
- 15-30 days: Special offer, limited incentive
- 31-60 days: Re-engagement, new angle
- 61-180 days: Brand awareness, nurture content

## Notes
- Retargeting should be 15-25% of total ad budget
- Video viewers retargeting is highest-intent warm audience
- Always create a "super warm" audience (add to cart, initiate checkout)
- Refresh retargeting creatives every 2 weeks to prevent fatigue

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
