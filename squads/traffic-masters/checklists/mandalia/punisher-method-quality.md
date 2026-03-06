# Punisher Method Optimization Quality Gate

> Quality gate for Depesh Mandalia's Punisher Method for aggressive ad account optimization. Must pass before the Punisher optimization protocol is executed on any campaign.

## Section 1: Pre-Punisher Prerequisites
- [ ] Campaign has been running for at least 7 days with consistent data
- [ ] Minimum 50 conversions have been recorded in the evaluation period
- [ ] All tracking is verified accurate (no data gaps or duplicate events)
- [ ] Baseline metrics are documented (CPA, ROAS, CTR, CVR, frequency)
- [ ] Budget is sufficient to sustain the optimization period without running out mid-cycle

## Section 2: Performance Triage
- [ ] Every ad set is categorized: winners (below CPA target), borderline (within 20% of target), losers (above 20% of target)
- [ ] Losers are identified for immediate budget cut or pause
- [ ] Winners are identified for immediate budget increase
- [ ] Borderline ad sets are given a defined probation period (48-72 hours)
- [ ] Triage decisions are based on statistically significant data, not small sample sizes

## Section 3: Budget Reallocation
- [ ] Budget from paused losers is redistributed to proven winners
- [ ] Budget increases to winners do not exceed 20-30% per day to avoid resetting learning
- [ ] Total account spend remains within the approved daily/weekly budget
- [ ] New budget allocation is documented with rationale for each change
- [ ] Emergency budget reserves are maintained (10-15% of total) for unexpected opportunities

## Section 4: Creative Punishing
- [ ] Underperforming ads within winning ad sets are paused (not just underperforming ad sets)
- [ ] Creative fatigue is identified by declining CTR with stable or rising frequency
- [ ] Fatigued creatives are replaced with fresh iterations, not just paused
- [ ] Top 3 performing ad creatives are documented as templates for future production
- [ ] No ad set is left with fewer than 2 active ads after the punishing cycle

## Section 5: Audience Punishing
- [ ] Overlapping audiences are identified and consolidated or excluded
- [ ] Audience expansion is applied to winning ad sets that are audience-constrained
- [ ] Poorly performing interest or lookalike segments are removed
- [ ] Retargeting audience windows are tightened for better recency relevance
- [ ] New prospecting audiences are queued to replace depleted ones

## Section 6: Post-Punisher Monitoring
- [ ] Performance is monitored hourly for the first 24 hours post-optimization
- [ ] CPA and ROAS are tracked against pre-Punisher baseline at 24h, 48h, and 72h
- [ ] Any campaigns that worsen post-optimization are flagged for rollback
- [ ] Punisher results are logged with before/after metrics for future reference
- [ ] Next Punisher cycle is scheduled (typically weekly or bi-weekly)

## Approval
- **Minimum pass rate**: 20/25 items (80%)
- **Reviewer**: mandalia-scaling-strategist
- **Escalation**: If post-Punisher performance declines by more than 20%, execute rollback protocol and investigate root cause before next cycle
