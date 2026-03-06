# Optimization Layer
> **Type**: Stack Layer
> **Used by agents**: Performance Analyst, Media Buyer

## Overview
The continuous improvement engine of the traffic stack. Once campaigns are live and baseline data is established, this layer governs daily monitoring, diagnostic analysis, budget reallocation, creative refresh decisions, and conversion rate optimization. This is not a one-time phase — it runs perpetually for the lifetime of every active campaign. Ongoing.

## When to Use
- Every active campaign, every day (mandatory daily monitoring)
- Post-learning phase (after Day 7 of campaign launch)
- When performance deviates from benchmarks (Yellow or Red alerts)
- Weekly optimization cycles for budget and creative decisions
- Monthly strategic optimization reviews

## The Framework

### Daily Monitoring Protocol (Before 10 AM)
1. **Spend Pacing**: Is daily spend on track for monthly budget?
2. **CPA/ROAS Check**: Are primary metrics within target range?
3. **Delivery Issues**: Campaigns underspending, stuck in learning, or errors?
4. **Ad Rejections**: New rejections since last check? Resolve within 4 hours.
5. **Frequency Check**: Any audiences exceeding frequency caps?
6. **Creative Performance**: Any ads showing CTR decline >20% from peak?
7. **Anomaly Detection**: CPM spikes, CTR drops, conversion gaps?

### Diagnostic Framework
- Low impressions: Check budget, bid, audience size
- High CPM + normal CTR: Audience saturation or high auction demand
- Low CTR: Creative fatigue or audience-creative mismatch
- High CTR + low CVR: Landing page issue, audience quality, or tracking gap
- High CVR + high CPA: CPM driving up cost per conversion
- Rising frequency: Audience exhaustion, expand or refresh

### Budget Reallocation (Weekly)
- Shift from underperforming to outperforming campaigns/ad sets
- Follow 70/20/10: 70% proven, 20% promising, 10% testing
- Never cut budget by more than 30% in a single change
- Document every reallocation with rationale

### Creative Refresh (Bi-Weekly)
- Fatigue indicators: CTR declined 25%+ from peak, frequency above 3x, CPM up + CTR down
- Swap underperforming ads with new variations
- Test new hooks on winning body content
- Introduce new formats, rotate UGC alongside brand creative

### Audience Optimization (Weekly)
- Pause ad sets consistently above CPA target for 5+ days
- Refresh lookalike sources with updated conversion data
- Test exclusion refinements to reduce overlap
- Evaluate broad targeting readiness (50+ conversions/week threshold)

### CRO — Conversion Rate Optimization (Monthly)
- Analyze landing page: bounce rate, time on page, scroll depth
- Identify funnel drop-off points
- Prioritize landing page tests: headline, CTA, social proof, form length
- Page speed: every 1-second improvement increases CVR 5-7%
- Review mobile vs desktop conversion rates

## Key Concepts
- The optimization paradox: the better campaigns perform, the harder incremental gains become
- Weekly rhythm: daily monitoring catches emergencies, weekly reviews drive strategy
- Compounding effect: 2% weekly CPA improvement = 62% improvement over 6 months
- Creative is the lever: when targeting and bidding are optimized, creative remains the variable

## Decision Rules
1. Daily monitoring is mandatory — no day without a performance check
2. No optimization changes during learning phase (first 7 days) except emergencies
3. Use 3-day rolling averages for decisions — never act on single-day data
4. Budget reallocation must be documented with rationale
5. Creative refresh is proactive, not reactive — queue before fatigue hits
6. CRO recommendations require data evidence, not opinion

## Integration
- Receives campaigns from Media Buying Layer after launch phase
- Performance thresholds from pacing and guardrails trigger actions
- Creative refresh requests go to Creative Layer
- Scaling triggers transition to Scaling Layer
- Diagnostic findings feed back to Strategy Layer for pivots

## Output
- Daily monitoring log with observations and actions
- Weekly optimization report: changes made, rationale, expected impact
- Monthly optimization review: trend analysis, strategic recommendations
- Creative fatigue alerts with refresh timeline
- CRO recommendation document with prioritized tests
- Budget reallocation history with performance impact tracking
