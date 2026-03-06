# MPI (Media Performance Index) Quality Gate

> Quality gate for Charley T. Burns' MPI (Media Performance Index) composite scoring system. Must pass before MPI is used as a decision-making tool for campaign optimization.

## Section 1: MPI Component Metrics
- [ ] All component metrics are defined (e.g., CTR, CPC, CPA, ROAS, frequency, conversion rate)
- [ ] Each component metric has a weight assigned based on business priority
- [ ] Weights sum to 100% across all components
- [ ] Component metric data sources are reliable and consistent (no sampling issues)
- [ ] Vanity metrics (impressions, reach) are excluded or minimally weighted

## Section 2: MPI Scoring Formula
- [ ] MPI formula is documented and shared with all team members
- [ ] Each metric is normalized to a 0-100 scale for fair comparison
- [ ] Normalization method accounts for metric directionality (higher CTR = good, higher CPA = bad)
- [ ] The formula produces a single composite score that is intuitive to interpret
- [ ] MPI scores are benchmarked against historical performance (what score is "good"?)

## Section 3: MPI Application Rules
- [ ] MPI is calculated at the ad set or campaign level (not aggregated across unrelated campaigns)
- [ ] MPI is recalculated on a consistent cadence (daily, weekly)
- [ ] MPI is used alongside raw metrics, not as a replacement for detailed analysis
- [ ] MPI thresholds for action are defined (e.g., MPI below 40 = pause, above 70 = scale)
- [ ] MPI comparisons are made within the same campaign type (prospecting vs. prospecting, not prospecting vs. retargeting)

## Section 4: MPI Data Integrity
- [ ] Data is pulled from a single source of truth (ad platform or BI tool, not mixed)
- [ ] MPI calculations exclude campaigns still in the learning phase
- [ ] Minimum data thresholds are met before MPI is calculated (e.g., 1,000 impressions, 10 conversions)
- [ ] Outliers are flagged but not automatically removed without investigation
- [ ] MPI spreadsheet or dashboard is automated to reduce manual calculation errors

## Section 5: MPI Review & Calibration
- [ ] MPI weights are reviewed quarterly and adjusted if business priorities shift
- [ ] MPI scores are validated against actual business outcomes (does high MPI = high profit?)
- [ ] Team alignment on MPI interpretation is confirmed (no conflicting definitions)
- [ ] MPI is presented in leadership reports with context and recommended actions

## Approval
- **Minimum pass rate**: 18/23 items (78%)
- **Reviewer**: burns-performance-strategist
- **Escalation**: If MPI scores consistently misalign with business outcomes, pause usage and recalibrate the formula and weights
