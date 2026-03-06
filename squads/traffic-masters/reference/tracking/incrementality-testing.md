# Incrementality Testing Guide
> **Category**: Advanced Measurement
> **Last Updated**: 2026-03

## Overview
Incrementality testing measures the TRUE causal impact of advertising by comparing outcomes between exposed and unexposed groups. It answers: "Would this conversion have happened anyway without the ad?"

## Why It Matters
- Platform attribution over-reports (every platform claims credit)
- Last-click attribution misses upper-funnel influence
- Correlation is not causation — incrementality proves causation
- Essential for accurate budget allocation decisions

## Testing Methods

### Geo-Split Test
- Divide regions into test (ads on) and control (ads off)
- Compare conversion rates between groups
- Best for: large geo footprint, significant spend levels
- Duration: 2-4 weeks minimum per phase

### Conversion Lift (Platform-Provided)
- Meta Conversion Lift: splits users into test/holdout groups
- Google Brand Lift / Conversion Lift: similar methodology
- Advantages: easy setup, platform handles randomization
- Limitations: only measures within that platform

### Ghost Ads / Intent-to-Treat
- Show ad to test group, placeholder to control group
- Measures impact of actual ad exposure
- More sophisticated but requires custom implementation

### Holdout Testing
- Randomly exclude 10-20% of audience from seeing ads
- Compare conversion behavior of holdout vs exposed
- Duration: 4+ weeks for statistical significance

## Key Metrics
- Incremental conversions: conversions caused by ads (not just correlated)
- Incremental ROAS (iROAS): revenue from incremental conversions / ad spend
- Incrementality rate: % of total conversions that are truly incremental

## Implementation Steps
1. Define hypothesis (e.g., "Meta retargeting drives 30% incremental conversions")
2. Design test (method, duration, sample size, control group)
3. Execute test (minimum 2 weeks, ideally 4)
4. Analyze results (statistical significance required)
5. Apply learnings to budget allocation

## Key Takeaways
- Run incrementality tests on your largest spend channels first
- Retargeting often has lower incrementality than assumed
- Prospecting (cold traffic) often has higher incrementality than attributed
- Use results to reallocate budget toward truly incremental channels
- Retest every 6-12 months as market conditions change
