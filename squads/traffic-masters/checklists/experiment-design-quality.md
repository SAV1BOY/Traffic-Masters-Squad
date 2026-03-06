# Experiment Design Quality
> **Type**: Quality Gate
> **Domain**: Testing & Optimization
> **Reviewed by**: Testing Lead

## Purpose
Ensures every experiment is properly designed with a clear hypothesis, controlled variables, and valid statistical parameters. Poorly designed tests produce misleading results and bad decisions.

## Checklist

### Hypothesis
- [ ] Hypothesis is written in a clear if/then/because format
- [ ] The expected outcome is specific and measurable
- [ ] The hypothesis is based on data, observation, or a documented rationale
- [ ] The hypothesis addresses a meaningful business question
- [ ] Prior test results or insights that informed the hypothesis are referenced

### Single Variable
- [ ] Only one variable is being changed between control and variant
- [ ] The variable being tested is clearly identified and documented
- [ ] All other elements remain identical across test groups
- [ ] If multiple variables must be tested, a multivariate framework is used
- [ ] The variable is significant enough to produce a detectable difference

### Sample Size Calculation
- [ ] Required sample size is calculated before the test begins
- [ ] Calculation uses the expected baseline conversion rate
- [ ] Minimum detectable effect size is defined and realistic
- [ ] Statistical significance threshold is set (typically 95%)
- [ ] Statistical power is set (typically 80%)
- [ ] Calculator or tool used for sample size is documented

### Duration
- [ ] Minimum test duration is 7 days to account for day-of-week variation
- [ ] Test duration accounts for reaching the required sample size
- [ ] Tests are not stopped early due to preliminary positive results
- [ ] Maximum test duration is defined to prevent indefinite running
- [ ] Seasonality or promotional periods are considered in timing

### Success Metric
- [ ] Primary success metric is defined before the test starts
- [ ] Secondary metrics are identified for additional learning
- [ ] Metrics are measurable with current tracking infrastructure
- [ ] Metric definitions are consistent with how they are tracked in analytics
- [ ] Guardrail metrics are set to detect unintended negative effects

### Decision Criteria
- [ ] Win, lose, and inconclusive outcomes are predefined
- [ ] Statistical significance threshold for declaring a winner is agreed upon
- [ ] Minimum practical significance is defined (not just statistical)
- [ ] Decision-making authority is assigned before the test begins
- [ ] Timeline for implementing the winning variant is established

### Fallback Plan
- [ ] Rollback procedure is documented in case the test variant performs badly
- [ ] Monitoring cadence during the test is defined
- [ ] Threshold for emergency test termination is set
- [ ] Impact on live campaigns is assessed and mitigated
- [ ] Communication plan exists for stakeholders if the test is stopped early

## Pass/Fail Criteria
All seven sections must pass before the experiment is launched. No test should run without a documented hypothesis and predefined decision criteria.

## If Failed
Return the experiment design for revision. Do not launch until all items are addressed. Document what was missing for process improvement.

## Related
- `scaling-quality.md`
- `creative-fatigue-quality.md`
- `reporting-quality.md`
