# MER: Marketing Efficiency Ratio Framework
> **Author**: Universal / Performance Measurement
> **Domain**: Analytics, Blended Metrics, Strategic Measurement
> **Used by agents**: analytics-agent, strategist-agent, media-buyer-agent

## Overview
MER (Marketing Efficiency Ratio) = Total Revenue / Total Marketing Spend. A blended,
top-level metric that cuts through attribution complexity by measuring the overall
efficiency of all marketing investment. While platform-level ROAS is useful for
tactical optimization, MER tells the strategic truth about whether marketing is
working as a system.

## When to Use
- Weekly and monthly strategic performance reviews
- When platform-reported ROAS does not match actual business results
- Making budget allocation decisions across channels
- Setting overall marketing efficiency targets by business model

## The Framework
### MER Calculation
- **Formula**: Total Business Revenue / Total Marketing Spend
- Include ALL revenue (organic + paid + direct + referral)
- Include ALL marketing spend (ads + tools + agency + creative production)
- Calculate weekly and track the trend over time
- Compare to target MER for your business model

### MER Targets by Business Model
- **E-commerce (physical products)**: MER 3:1 to 5:1 (varies by margin)
- **SaaS / Subscription**: MER 5:1 to 10:1 (high margin, recurring revenue)
- **Infoproducts / Courses**: MER 4:1 to 8:1 (high margin, one-time + upsells)
- **Lead Gen / Services**: MER 5:1 to 15:1 (revenue per client varies widely)
- **DTC with high LTV**: MER 2:1 to 4:1 (acceptable if payback < 90 days)

### MER Tracking Protocol
- Calculate every Monday for the previous week
- Track on a rolling 4-week average to smooth variance
- Compare to the same period last year for seasonal context
- Break down by week-over-week change and month-over-month trend
- Alert threshold: MER drops >15% week-over-week → investigate

### MER vs. Platform ROAS
| Metric | Use Case | Pros | Cons |
|--------|----------|------|------|
| MER | Strategic decisions | Honest, simple, no attribution bias | Cannot isolate channel contribution |
| Platform ROAS | Tactical optimization | Granular, actionable | Inflated, double-counted, biased |
| Both together | Complete picture | Strategic + tactical alignment | Requires discipline to use correctly |

## Key Concepts
- MER is the great equalizer — it does not care about attribution models
- Platform ROAS will always be higher than MER because platforms over-count
- Rising MER = marketing is becoming more efficient overall
- Falling MER = something is breaking, even if platform ROAS looks fine
- MER includes organic revenue intentionally — paid and organic influence each other
- A business can have positive channel ROAS but negative MER (overhead, tools, team)

## Decision Rules
- IF MER is above target → consider scaling spend cautiously
- IF MER is below target → audit channel efficiency and reduce weakest
- IF MER is declining despite stable platform ROAS → attribution is misleading
- IF MER varies wildly week to week → smooth with rolling 4-week average
- IF launching a new channel → expect MER to dip temporarily, set 90-day timeline
- IF MER is strong but one channel ROAS is weak → channel may drive unmeasured value

## Common Mistakes
- Ignoring MER and relying solely on platform-reported ROAS
- Not including all spend in the denominator (forgetting tools, team, creative costs)
- Reacting to weekly MER fluctuations instead of watching the trend
- Comparing MER across different business models (targets differ by model)
- Using MER to make channel-level decisions (it is a strategic metric, not tactical)

## Integration
- Feeds into: Budget Allocation Model (MER gates scaling decisions)
- Pairs with: Attribution and Incrementality (MER + incrementality = complete picture)
- Complements: LTV-CAC Unit Economics (MER is the top-level efficiency view)
- Source data: All revenue and spend data from finance, CRM, and ad platforms

## Output
- Weekly MER calculation with rolling 4-week average
- MER trend chart for the trailing 12 weeks
- MER vs. platform ROAS comparison analysis
- Target MER by business model with actual vs. target tracking
