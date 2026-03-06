# Manual CPC First Strategy Quality Gate

> Quality gate for Kasim Aslam's Manual CPC First approach to Google Ads bidding. Must pass before transitioning from Manual CPC to any automated bid strategy.

## Section 1: Manual CPC Setup
- [ ] All campaigns start on Manual CPC bidding (not Enhanced CPC or automated strategies)
- [ ] Initial CPC bids are set based on keyword planner estimates and competitive analysis
- [ ] Bids are set at the keyword level, not just the ad group level, for maximum control
- [ ] Enhanced CPC is explicitly disabled (not left as default)
- [ ] Bid adjustments for device, location, schedule, and audience are applied manually

## Section 2: Data Collection Phase
- [ ] Minimum 2 weeks of Manual CPC data is collected before considering automation
- [ ] Search term reports are reviewed and refined during the manual phase
- [ ] At least 15-30 conversions are recorded to establish a conversion baseline
- [ ] Click-through rate, conversion rate, and cost per conversion baselines are documented
- [ ] Quality Score trends are tracked for all primary keywords

## Section 3: Manual CPC Optimization
- [ ] Bids are increased for keywords with high conversion rate and low impression share
- [ ] Bids are decreased for keywords with high spend and low/no conversions
- [ ] Keyword-level bid adjustments are made weekly based on performance data
- [ ] Device bid adjustments reflect actual conversion rate differences (mobile vs. desktop)
- [ ] Geographic bid adjustments are applied based on location performance data
- [ ] Ad schedule bid adjustments are set based on hourly/daily conversion patterns

## Section 4: Transition Readiness Assessment
- [ ] Account has accumulated 30+ conversions in the last 30 days (platform recommendation minimum)
- [ ] Conversion tracking is verified accurate (no duplicates, no missed conversions)
- [ ] Conversion action values are set correctly for value-based bidding strategies
- [ ] Manual CPC performance is stable (CPA variance under 20% week-over-week)
- [ ] Target CPA or Target ROAS for automated bidding is calculated from Manual CPC data

## Section 5: Automated Bidding Transition Protocol
- [ ] Transition to automated bidding is done campaign by campaign, not all at once
- [ ] A 2-week learning period is expected and budgeted for after switching
- [ ] Performance during learning phase is monitored but not prematurely adjusted
- [ ] Rollback criteria are defined (if CPA exceeds 1.5x target for 14+ days, revert to Manual CPC)
- [ ] Manual CPC remains the strategy for low-volume campaigns that lack sufficient conversion data
- [ ] Portfolio bid strategies are considered for campaigns that individually lack volume but collectively have enough data

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: aslam-google-ads-strategist
- **Escalation**: If the transition to automated bidding causes CPA to exceed 2x the Manual CPC baseline for more than 2 weeks, revert immediately and investigate
