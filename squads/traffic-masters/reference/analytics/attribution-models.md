# Attribution Models Reference
> **Category**: Analytics Methodology
> **Last Updated**: 2026-03

## Overview
Attribution models determine how credit for conversions is assigned across multiple touchpoints in the customer journey. No single model is "correct" — each offers a different lens.

## Model Types

### Last Click
- 100% credit to the last touchpoint before conversion
- Pros: Simple, conservative, easy to act on
- Cons: Ignores upper-funnel contribution, biases toward bottom-funnel

### First Click
- 100% credit to the first touchpoint that introduced the user
- Pros: Values prospecting and awareness efforts
- Cons: Ignores nurturing and closing touchpoints

### Linear
- Equal credit to every touchpoint in the journey
- Pros: Fair representation of all channels
- Cons: Over-simplifies; not all touchpoints contribute equally

### Position-Based (U-Shaped)
- 40% to first touch, 40% to last touch, 20% split among middle
- Pros: Values both discovery and conversion
- Cons: Arbitrary weighting, undervalues mid-funnel

### Data-Driven (Algorithmic)
- Machine learning assigns credit based on actual conversion patterns
- Pros: Most accurate, adapts to your specific data
- Cons: Requires sufficient conversion volume, black box

## Platform Default Models
- Meta: 7-day click, 1-day view (self-attributed)
- Google Ads: Data-driven (default since 2023)
- GA4: Data-driven (default), with paid and organic cross-channel view
- TikTok: 7-day click, 1-day view

## Practical Application
1. Use platform attribution for in-platform optimization decisions
2. Use GA4 cross-channel attribution for budget allocation across platforms
3. Use incrementality testing for ground truth on channel value
4. Compare multiple models to understand the full picture

## Key Takeaways
- No model is perfect — use multiple models as different lenses
- Platform self-attribution always over-counts; GA4 under-counts paid social
- Data-driven is the best automated model but needs sufficient data
- Incrementality testing is the gold standard for proving true channel impact
- Document which model you use for which decisions to maintain consistency
