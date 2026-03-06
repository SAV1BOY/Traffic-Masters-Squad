# Attribution and Incrementality
> **Type**: Measurement Framework
> **Used by agents**: Performance Analyst, Traffic Chief, Pixel Specialist

## Overview
Framework for understanding how to credit conversions across touchpoints and how to measure the true incremental impact of advertising. Combines attribution models (who gets credit) with incrementality testing (did the ad actually cause the conversion). Platform data is for optimization; blended MER is for strategy.

## When to Use
- Setting up measurement strategy for multi-channel campaigns
- When platform-reported ROAS does not match actual business results
- Evaluating true channel contribution beyond last-click
- Making budget allocation decisions across channels

## The Framework

### Attribution Models
1. **Last-Click**: Credits the final touchpoint before conversion. Simple, biased toward BOFU.
2. **First-Click**: Credits the first touchpoint. Biased toward TOFU discovery channels.
3. **Linear**: Equal credit across all touchpoints. Fair but uninformative.
4. **Time-Decay**: More credit to touchpoints closer to conversion.
5. **Data-Driven**: Algorithmic, uses machine learning. Best available but opaque.
6. **Platform-Reported**: Each platform claims credit. Sum always exceeds actual conversions.

### Limitations of Attribution
- Every model has bias — no model is "correct"
- Cross-device and cross-browser journeys break tracking
- iOS 14.5+ reduced attribution accuracy significantly
- Walled gardens (Meta, Google) cannot see each other's touchpoints
- Attribution answers "who touched it" not "did it matter"

### Incrementality Testing
- **Holdout Tests**: Withhold ads from a random group; compare conversion rates
- **Geo Tests**: Run ads in some regions, not others; compare outcomes
- **Conversion Lift Studies**: Platform-native (Meta, Google) incrementality measurement
- Incrementality answers: "Would this conversion have happened WITHOUT the ad?"

### The Two-Layer Measurement Stack
- **Platform data**: Use for in-platform optimization (bidding, targeting, creative)
- **MER (Marketing Efficiency Ratio)**: Use for strategic budget allocation across channels
- Never make cross-channel budget decisions using platform-reported ROAS alone

## Key Concepts
- Attribution is a model, not reality. All models are wrong; some are useful.
- Incrementality is the gold standard but expensive and slow to measure
- Platform-reported conversions are inflated; MER is the honest metric
- The gap between attributed and actual revenue is your measurement blind spot

## Decision Rules
1. Use platform attribution for in-platform optimization only
2. Use MER (total revenue / total spend) for cross-channel budget decisions
3. Run incrementality tests quarterly on top-spending channels
4. If platform ROAS is strong but MER is weak, investigate over-attribution
5. If cutting a channel does not decrease total revenue, it was not incremental

## Integration
- Feeds into: Budget Allocation Model, MER Framework, Optimization Layer
- Receives from: Tracking Stack Standard, Pixel and CAPI data
- Pairs with: iOS Privacy Adaptation Framework

## Output
- Attribution model selection rationale for the account
- Incrementality test plan (holdout or geo test design)
- Platform vs actual ROAS comparison report
- MER dashboard for strategic decision-making
- Quarterly incrementality assessment with channel-level findings
