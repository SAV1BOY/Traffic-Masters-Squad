# Meta Scaling Quality Gate

> Quality gate for Meta campaign scaling decisions (budget increases, audience expansion, new placements). Must pass before any scaling action is executed.

## Section 1: Performance Baseline Validation
- [ ] Campaign has completed the learning phase (at least 50 conversion events per ad set in 7 days)
- [ ] CPA/ROAS has been stable for at least 3-5 consecutive days before scaling
- [ ] Statistical significance of current results has been verified (minimum 100 conversions at campaign level)
- [ ] Current spend is at least 80% of daily budget (campaign is not under-delivering)
- [ ] Frequency is below 3.0 for prospecting and below 5.0 for retargeting audiences

## Section 2: Budget Scaling Rules
- [ ] Budget increase does not exceed 20% per change to avoid resetting the learning phase
- [ ] If budget increase exceeds 20%, a new ad set or campaign is created instead of modifying the existing one
- [ ] Budget changes are documented with date, previous amount, new amount, and rationale
- [ ] CBO campaigns have ad set minimum spend limits reviewed after budget increase
- [ ] Lifetime budget campaigns have pacing recalculated after any budget adjustment

## Section 3: Audience Expansion
- [ ] Lookalike audience percentages are expanded incrementally (1% to 3% to 5%, not 1% to 10%)
- [ ] New interest or behavioral targeting layers are tested in separate ad sets (not added to winning ad sets)
- [ ] Broad targeting (no interests, age/geo only) is tested only after narrow audiences are saturated
- [ ] Audience overlap analysis is re-run after adding new audiences to prevent cannibalization
- [ ] Retargeting pool size is sufficient to support increased spend (at least 1,000 users in the audience)

## Section 4: Creative Scaling
- [ ] Top-performing creatives have been identified using statistically valid data (CTR, CPA, ROAS)
- [ ] New creative variants (iterations on winners) are prepared before scaling to prevent fatigue
- [ ] Ad fatigue indicators are monitored: rising frequency, declining CTR, increasing CPA over 7-day trend
- [ ] At least 3-5 active ad variants exist per ad set to give the algorithm sufficient options
- [ ] Underperforming ads (bottom 20% by CPA) are paused before scaling spend

## Section 5: Monitoring and Rollback
- [ ] Automated rules are set to pause ad sets if CPA exceeds 150% of target for 2 consecutive days
- [ ] Daily monitoring schedule is confirmed for the first 72 hours post-scaling
- [ ] Rollback plan is documented: revert budget, pause new audiences, restore previous structure
- [ ] Pacing alerts are configured to flag under-delivery or overspend within 24 hours
- [ ] Scaling log is updated with actions taken, dates, and observed impact

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: If learning phase resets or CPA increases more than 30% within 48 hours of scaling, revert to previous state and escalate to strategy review
