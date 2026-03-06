# Optimization Layer

> **Type**: Stack Layer
> **Domain**: Performance Improvement — Ongoing Optimization
> **Used by agents**: Performance Analyst, Media Buyer, Sobral, Traffic Chief

## Overview

The Optimization Layer is the continuous improvement engine of the traffic stack. Once campaigns are live and baseline data is established, this layer governs daily monitoring, diagnostic analysis, budget reallocation, creative refresh decisions, and conversion rate optimization. This is not a one-time phase — it runs perpetually for the lifetime of every active campaign. The difference between a good media buyer and a great one lives in this layer.

## When to Use

- Every active campaign, every day (mandatory daily monitoring)
- Post-learning phase (after Day 7 of campaign launch)
- When performance deviates from benchmarks (Yellow or Red alerts)
- Weekly optimization cycles for budget and creative decisions
- Monthly strategic optimization reviews

## The Framework

### Daily Monitoring Protocol

**Time**: Before 10 AM local time, every business day.
**Owner**: Performance Analyst (primary), Media Buyer (secondary)

**Daily Check Sequence**:
1. **Spend Pacing**: Is daily spend on track for monthly budget? (Per `pacing-and-guardrails.md`)
2. **CPA/ROAS Check**: Are primary metrics within target range? Flag Yellow/Red.
3. **Delivery Issues**: Any campaigns underspending, stuck in learning, or showing errors?
4. **Ad Rejections**: New rejections since last check? Resolve within 4 hours.
5. **Frequency Check**: Any audiences exceeding frequency caps?
6. **Creative Performance**: Any ads showing CTR decline > 20% from peak?
7. **Anomaly Detection**: Anything unusual — CPM spikes, CTR drops, conversion gaps?

**Daily Log**: Document findings, actions taken, and items to watch. This log is the institutional memory of the account.

### Diagnostic Framework

When performance deviates from target, diagnose using the funnel diagnostic approach:

| Symptom | Likely Cause | Diagnostic Action |
|---------|-------------|-------------------|
| Low impressions | Budget, bid, audience too narrow | Check auction competition, expand audience, increase bid |
| High CPM, normal CTR | Audience saturation or high auction demand | Rotate audience, adjust placements, test new geos |
| Low CTR | Creative fatigue, wrong audience-creative match | Review creative age, test new hooks, check audience alignment |
| High CTR, low CVR | Landing page issue, audience quality, tracking gap | Audit landing page, check load speed, verify tracking, review audience quality |
| High CVR, high CPA | High CPM driving up cost per conversion | Address CPM through audience/placement optimization |
| Rising frequency | Audience exhaustion | Expand audience layer, add new seed audiences, increase budget to reach |
| Tracking discrepancy | Pixel/CAPI misconfiguration | Re-run tracking QA per `tracking-layer.md` |

### Optimization Actions

#### Budget Reallocation (Weekly)
**Owner**: Media Buyer, approved by Performance Analyst

- Shift budget from underperforming campaigns/ad sets to outperformers.
- Follow the 70/20/10 rule: 70% to proven winners, 20% to promising performers, 10% to testing.
- Never cut budget by more than 30% in a single change (triggers re-learning).
- Document every reallocation with rationale in campaign log.

#### Creative Refresh (Bi-Weekly)
**Owner**: Ad Midas, Creative Analyst

**Fatigue Indicators**:
- CTR declined 25%+ from peak over 7-day rolling average
- Frequency above 3x/week on prospecting
- CPM increasing while CTR decreasing (double signal)
- Creative running for 3+ weeks without variation

**Refresh Actions**:
1. Swap underperforming ads with new variations from creative pipeline.
2. Test new hooks on existing winning body content.
3. Introduce new format (if all current are video, try static or carousel).
4. Rotate in UGC content alongside brand creative.
5. Update copy with seasonal or timely references.

#### Audience Optimization (Weekly)
**Owner**: Media Buyer

- Pause ad sets with audiences consistently above CPA target for 5+ days.
- Promote next-layer audiences per `audience-building-system.md`.
- Refresh lookalike sources with updated conversion data.
- Test exclusion refinements to reduce overlap.
- Evaluate broad targeting readiness (50+ conversions/week threshold met?).

#### Bid Strategy Optimization (Bi-Weekly)
**Owner**: Media Buyer

- Evaluate current bid strategy performance (lowest cost, cost cap, target ROAS).
- If CPA is volatile with lowest cost, test cost cap with target set at 120% of desired CPA.
- If ROAS is inconsistent, test target ROAS bidding with 80% of desired ROAS as target.
- Google: evaluate Smart Bidding signals — is algorithm using them effectively?
- Never change bid strategy during learning phase.

#### CRO (Conversion Rate Optimization) (Monthly)
**Owner**: Performance Analyst, Traffic Chief

- Analyze landing page performance: bounce rate, time on page, scroll depth.
- Identify drop-off points in conversion funnel.
- Recommend and prioritize landing page tests (headline, CTA, social proof, form length).
- Test page speed improvements — every 1-second improvement increases CVR 5-7%.
- Review mobile vs desktop conversion rates — optimize for dominant device.

### Sobral Methodology Integration

Apply Sobral diagnostic methodology for systematic performance analysis:
- **Layer-by-layer diagnosis**: Do not assume the problem. Walk through each funnel stage methodically.
- **Data-driven decisions only**: Never optimize based on feelings or single data points.
- **Minimum data thresholds**: Require statistically significant data before making changes (100+ clicks, 20+ conversions minimum).
- **Isolation testing**: Change one variable at a time. Multiple simultaneous changes make attribution impossible.

## Key Concepts

- **The Optimization Paradox**: The better campaigns perform, the harder incremental improvement becomes. Set expectations that optimization gains diminish over time.
- **Weekly Rhythm**: Major optimization decisions happen weekly, not daily. Daily monitoring catches emergencies. Weekly reviews drive strategic changes.
- **Compounding Effect**: Small daily improvements compound. A 2% weekly improvement in CPA means 62% improvement over 6 months.
- **Creative Is the Lever**: When all targeting and bidding is optimized, creative remains the primary variable. The optimization layer should generate as many creative insights as it does media buying adjustments.

## Decision Rules

1. Daily monitoring is mandatory — no day without a performance check on active accounts.
2. No optimization changes during learning phase (first 7 days) except emergencies.
3. Use 3-day rolling averages for decisions. Never act on single-day data (except emergencies).
4. Budget reallocation must be documented with rationale. No undocumented changes.
5. Creative refresh is proactive, not reactive — queue new creative before fatigue hits.
6. CRO recommendations require data evidence. No "I think the page should..." without metrics.

## Common Mistakes

- Optimizing too frequently — making daily changes that reset learning and create noise.
- Not optimizing enough — "set it and forget it" is not a strategy.
- Focusing only on in-platform metrics and ignoring downstream business outcomes.
- Making multiple changes simultaneously and being unable to attribute improvement.
- Ignoring CRO — optimizing traffic to a broken landing page wastes every improvement.
- Reacting emotionally to single bad days instead of analyzing trends.

## Integration

- Receives campaigns from `media-buying-layer.md` after launch phase.
- Performance thresholds from `pacing-and-guardrails.md` trigger optimization actions.
- Creative refresh requests go to `creative-layer.md` and `creative-production-pipeline.md`.
- Audience adjustments follow `audience-building-system.md` layer progression.
- Scaling triggers transition to `scaling-layer.md`.
- Business outcomes reconciled via `client-ops-handoff.md`.
- Diagnostic findings feed back to `strategy-layer.md` for strategic pivots.

## Output

- Daily monitoring log with observations and actions.
- Weekly optimization report: changes made, rationale, expected impact.
- Monthly optimization review: trend analysis, strategic recommendations.
- Creative fatigue alerts with refresh timeline.
- CRO recommendation document with prioritized tests.
- Budget reallocation history with performance impact tracking.
