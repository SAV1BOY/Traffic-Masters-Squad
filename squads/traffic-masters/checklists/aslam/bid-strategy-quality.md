# 2-4 Bid Strategy Framework Quality Gate

> Quality gate for Kasim Aslam's 2-4 Bid Strategy framework for progressing through Google Ads bid strategies. Must pass before any bid strategy transition is executed.

## Section 1: Phase 1 - Manual CPC (Foundation)
- [ ] Campaign launches on Manual CPC with Enhanced CPC disabled
- [ ] Initial bids are informed by Keyword Planner and competitive landscape analysis
- [ ] Bids are managed at the keyword level for granular control
- [ ] Data collection goals are defined (target impressions, clicks, and conversions for baseline)
- [ ] Manual CPC phase runs for minimum 2-4 weeks to establish reliable patterns

## Section 2: Phase 2 - Enhanced CPC (Assisted Control)
- [ ] Transition to Enhanced CPC occurs only after Manual CPC baseline is established
- [ ] At least 15-20 conversions are recorded before enabling Enhanced CPC
- [ ] Enhanced CPC is monitored closely for the first 7 days after activation
- [ ] CPA under Enhanced CPC is compared to Manual CPC baseline
- [ ] If Enhanced CPC increases CPA by more than 25%, revert to Manual CPC

## Section 3: Phase 3 - Target CPA or Target ROAS (Automated)
- [ ] Transition to Target CPA/ROAS occurs only after 30+ conversions in the last 30 days
- [ ] Target CPA is set at or slightly above the actual CPA from Enhanced CPC phase
- [ ] Target ROAS is set at or slightly below the actual ROAS from Enhanced CPC phase
- [ ] Learning period (2 weeks) is expected and performance is not judged during this time
- [ ] Bid strategy targets are loosened initially, then tightened as the algorithm stabilizes
- [ ] Portfolio bid strategies are considered for campaigns with insufficient individual volume

## Section 4: Phase 4 - Maximize Conversions / Value (Full Automation)
- [ ] Maximize Conversions/Value is only used for campaigns with 50+ conversions per month
- [ ] Budget acts as the primary control lever (since there is no CPA/ROAS target cap)
- [ ] Performance is closely monitored as the algorithm has maximum freedom
- [ ] Maximum CPC limits are considered to prevent bid spikes on individual auctions
- [ ] Rollback to Target CPA/ROAS is ready if cost efficiency drops unacceptably

## Section 5: Bid Strategy Governance
- [ ] Only one bid strategy change is made per campaign at a time
- [ ] Bid strategy changes are logged with date, reason, and expected outcome
- [ ] A 2-week stabilization period follows every bid strategy change
- [ ] Campaigns are never moved backward and forward between strategies in rapid succession
- [ ] Seasonal adjustments use bid strategy modifiers, not strategy changes
- [ ] Account-level bid strategy distribution is documented (how many campaigns on each strategy)

## Section 6: Monitoring & Rollback
- [ ] Daily monitoring for the first 7 days after any bid strategy change
- [ ] Weekly monitoring thereafter with automated alerts for anomalies
- [ ] Rollback triggers are defined (e.g., CPA exceeds 1.5x target for 10+ days)
- [ ] Rollback procedure is documented step-by-step
- [ ] Post-rollback analysis identifies why the transition failed before reattempting

## Approval
- **Minimum pass rate**: 21/25 items (84%)
- **Reviewer**: aslam-google-ads-strategist
- **Escalation**: If any phase transition is made without meeting the prerequisite data thresholds, revert to the previous phase immediately
