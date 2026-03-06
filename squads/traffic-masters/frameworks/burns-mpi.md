# MPI - Marketing Performance Indicators

> **Author**: Ralph Burns
> **Domain**: Marketing Analytics & Performance Measurement
> **Used by agents**: data-analyst, media-buyer, traffic-strategist, account-manager
> **Checklists**: mpi-dashboard-setup-checklist, weekly-mpi-review-template

## Overview

MPI (Marketing Performance Indicators) is Ralph Burns' replacement for vanity dashboards. Most marketers track metrics that look good in reports but do not drive decisions. MPI organizes metrics into three tiers -- Leading, Lagging, and Action indicators -- each with a definition, benchmark, alert threshold, and prescribed action when triggered. The goal is a dashboard where every number tells you what to do, not just what happened.

## When to Use

- Setting up reporting for a new account or campaign
- Replacing vanity metric dashboards with actionable ones
- Conducting weekly or bi-weekly performance reviews
- Training teams on which metrics matter and why
- Diagnosing performance issues by following the indicator chain

## The Framework

### Tier 1: Leading Indicators

Leading indicators predict future performance. They move first, giving you early warning before lagging indicators shift. Monitor these daily.

**1. Hook Rate (Thumb-Stop Ratio)**
- Definition: Percentage of impressions where the user paused on the ad (3+ seconds on video, or click/engagement on static)
- Benchmark: 25-35% for video on Meta
- Alert threshold: Below 20% for 3+ consecutive days
- Action when triggered: Test new hooks immediately. The opening is failing to earn attention.

**2. Click-Through Rate (CTR)**
- Definition: Link clicks / Impressions
- Benchmark: 1.0-2.5% for Meta feed ads, varies by platform
- Alert threshold: 30% below account average for 3+ days
- Action when triggered: Audit ad creative. Check if the hook promises a relevant next step. Review audience targeting for relevance.

**3. Conversion Rate (CVR)**
- Definition: Conversions / Link clicks (landing page conversion rate)
- Benchmark: 20-40% for lead gen, 2-5% for e-commerce
- Alert threshold: 20% below baseline for 5+ days
- Action when triggered: Run the 24-point Conversion Architecture checklist. Check page speed, ad-to-page congruence, and form friction.

**4. CPA Trend (Cost Per Acquisition Direction)**
- Definition: 7-day rolling average CPA compared to 30-day average
- Benchmark: Within 15% of target CPA
- Alert threshold: 7-day CPA exceeds 30-day average by 20%+
- Action when triggered: Identify which variable changed. Check creative fatigue (frequency), audience saturation (CPM trend), or funnel changes.

**5. CPM Trend**
- Definition: Cost per 1,000 impressions, 7-day rolling average
- Benchmark: Platform and industry specific (Meta average $8-15)
- Alert threshold: 25% increase over 14-day period
- Action when triggered: Check audience overlap, competitive pressure (seasonal?), and creative quality score. Consider audience expansion or platform diversification.

### Tier 2: Lagging Indicators

Lagging indicators confirm whether the business is actually growing. They move slower and reflect cumulative impact. Review these weekly and monthly.

**6. nCAC (New Customer Acquisition Cost)**
- Definition: Total ad spend / New customers acquired (see burns-ncac-method.md)
- Benchmark: Must be below acceptable nCAC based on LTV
- Alert threshold: Exceeds target nCAC for 2+ consecutive weeks
- Action when triggered: Deep-dive by channel. Identify which channel's nCAC is rising. Check for audience quality decline, creative fatigue, or funnel degradation.

**7. LTV (Lifetime Value) by Cohort**
- Definition: Cumulative revenue per customer by acquisition month and source
- Benchmark: LTV must exceed nCAC by target margin (typically 3x+ at 12 months)
- Alert threshold: New cohort 30-day LTV drops 15%+ below previous cohort
- Action when triggered: Investigate customer quality. Check if targeting changes attracted lower-quality buyers. Review onboarding and product experience.

**8. MER (Marketing Efficiency Ratio)**
- Definition: Total revenue / Total marketing spend (all channels, not just paid)
- Benchmark: Industry specific (3-5x is common for e-commerce)
- Alert threshold: 20% decline over 30-day period
- Action when triggered: Holistic review. MER declining while individual channel ROAS is stable suggests attribution problems or organic revenue decline.

**9. Payback Period**
- Definition: Number of days until ad spend is recovered from customer revenue
- Benchmark: Under 90 days for most businesses, under 30 for cash-constrained
- Alert threshold: Exceeds target payback period by 20%+
- Action when triggered: Review pricing, upsell performance, and email revenue. Longer payback periods may require reducing spend until the funnel is fixed.

### Tier 3: Action Indicators

Action indicators measure the health of your optimization process itself. They ensure you are doing the work that drives improvement.

**10. Test Velocity**
- Definition: Number of new ad concepts tested per week
- Benchmark: 5-15 new concepts per week (depending on budget)
- Alert threshold: Below 5 per week for 2+ consecutive weeks
- Action when triggered: The creative pipeline is stalling. Return to Creative Lab research. Ensure the Kaizen Kreative cycle is running.

**11. Creative Refresh Rate**
- Definition: Percentage of active ad spend going to creative less than 14 days old
- Benchmark: 30-50% of spend on fresh creative
- Alert threshold: Below 20% (over-reliance on aging creative)
- Action when triggered: Accelerate creative production. Iterate on current winners. Prioritize hook variations of top performers.

**12. Spend Efficiency**
- Definition: Percentage of total budget actually spent (vs. allocated but unspent)
- Benchmark: 85-95% spend efficiency
- Alert threshold: Below 80% (budget sitting idle) or above 98% (potential missed opportunities)
- Action when triggered: Below 80% -- check campaign delivery issues, bid caps, audience size. Above 98% -- consider if budget is limiting scale opportunities.

**13. Winner Ratio**
- Definition: Percentage of new creative that outperforms the control
- Benchmark: 10-20% (most creative fails -- this is normal)
- Alert threshold: Below 5% for 3+ consecutive test cycles
- Action when triggered: Research quality is declining. Return to Creative Lab. Audit the quality of hooks and angles being tested.

## Key Concepts

- **Three tiers, three cadences**: Leading = daily, Lagging = weekly/monthly, Action = weekly
- **Every metric has a response**: A number without a prescribed action is a vanity metric
- **Alert thresholds prevent overreaction**: Small fluctuations are normal. Only act when thresholds are breached.
- **Leading predicts lagging**: If leading indicators drop, lagging will follow in 7-14 days. Act on leading indicators to prevent lagging problems.
- **Action indicators prevent stagnation**: Even when results are good, if action indicators decline, results will follow

## Decision Rules

- IF Hook Rate drops below threshold THEN it is a creative problem -- test new hooks
- IF CTR is strong but CVR drops THEN it is a landing page or offer problem
- IF CPA trend is rising and CPM is stable THEN creative fatigue -- refresh creative
- IF CPA trend is rising and CPM is rising THEN audience saturation -- expand audiences
- IF nCAC exceeds target but MER is stable THEN attribution may be shifting between channels
- IF test velocity drops THEN the creative pipeline needs attention before results decline
- IF winner ratio drops below 5% THEN the research phase is producing weak angles

## Common Mistakes

- Tracking 30+ metrics with no alert thresholds or prescribed actions
- Reviewing lagging indicators daily and overreacting to normal fluctuations
- Ignoring action indicators -- when results are good, teams stop testing and then wonder why results decline
- Not connecting leading to lagging -- treating each metric as independent instead of seeing the chain
- Using platform-reported metrics without cross-referencing against actual business data
- Building dashboards that look impressive but do not drive weekly decisions

## Integration

- nCAC indicator connects to **burns-ncac-method.md** for detailed calculation
- CVR indicator connects to **burns-conversion-architecture.md** for diagnosis
- Creative indicators connect to **burns-kaizen-kreative.md** and **burns-creative-lab.md**
- MER connects to **burns-caamp.md** for holistic acquisition health
- All indicators are reviewed in **burns-sgp-30-60-90.md** during the 111-point audit
- Hook rate indicator connects to **pittman-hook-framework.md** for creative improvement

## Output

- Configured MPI dashboard with all 13 indicators, benchmarks, and alert thresholds
- Weekly MPI review report highlighting triggered alerts and prescribed actions
- Monthly trend report showing leading-to-lagging indicator relationships
- Quarterly benchmark recalibration based on accumulated performance data
