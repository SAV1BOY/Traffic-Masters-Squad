# Conversion Modeling Guide
> **Category**: Advanced Measurement
> **Last Updated**: 2026-03

## Overview
Conversion modeling uses statistical methods and machine learning to estimate conversions that cannot be directly observed due to privacy restrictions, cookie limitations, ad blockers, and cross-device behavior.

## Why Conversion Modeling Exists
- iOS 14+ App Tracking Transparency reduced observable conversions by 30-50%
- Cookie deprecation and ad blockers create data gaps
- Cross-device journeys break last-click attribution
- Platforms use modeling to fill measurement gaps

## Platform-Provided Modeling
- **Meta**: Aggregated Event Measurement (AEM), modeled conversions in reporting
- **Google**: Consent Mode modeling, Enhanced Conversions, data-driven attribution
- **TikTok**: Modeled attribution for iOS users

## Custom Modeling Approaches
### Media Mix Modeling (MMM)
- Statistical model using aggregate data (spend, impressions, conversions over time)
- Does not require user-level data (privacy-safe)
- Captures online and offline channels
- Requires 2+ years of historical data for best results

### Multi-Touch Attribution (MTA)
- User-level path analysis across touchpoints
- Assigns fractional credit to each interaction
- Requires robust tracking across all channels
- Increasingly difficult due to privacy restrictions

### Triangulation Approach
- Combine platform reporting, GA4 attribution, and incrementality tests
- No single source is correct — use multiple lenses
- The truth is usually between platform over-reporting and GA4 under-reporting

## Implementation for Traffic Squad
1. Trust platform-modeled data for directional optimization (daily decisions)
2. Use GA4 data-driven attribution for cross-channel comparison
3. Run incrementality tests quarterly for ground truth
4. Reconcile all three data sources in monthly reviews

## Key Takeaways
- Accept that perfect measurement is no longer possible — model and triangulate
- Platform-modeled conversions are directionally useful for optimization
- Incrementality testing provides the closest thing to ground truth
- Media Mix Modeling is the best long-term investment for mature advertisers
- Document your measurement methodology so decisions are reproducible
