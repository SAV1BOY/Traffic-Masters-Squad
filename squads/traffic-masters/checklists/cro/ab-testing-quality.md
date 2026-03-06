# A/B Testing Setup and Statistical Rigor Quality Gate

> Quality gate for A/B testing methodology, setup, and statistical validity. Must pass before any A/B test is launched or results are declared.

## Section 1: Test Hypothesis and Design
- [ ] Test hypothesis is documented: "Changing [element] from [control] to [variant] will improve [metric] by [expected lift] because [rationale]"
- [ ] Hypothesis is based on qualitative or quantitative data (heatmaps, user research, analytics patterns, not gut feeling)
- [ ] Only one variable is changed between control and variant (or a multivariate test is explicitly designed)
- [ ] Primary success metric is defined before test launch (conversion rate, revenue per visitor, lead quality score)
- [ ] Secondary metrics are identified to watch for unintended consequences (bounce rate, time on page, form abandonment)

## Section 2: Sample Size and Duration
- [ ] Minimum sample size per variant is calculated using a statistical power calculator (80% power, 95% confidence)
- [ ] Expected minimum detectable effect (MDE) is realistic for the traffic volume (typically 5-20% relative lift)
- [ ] Test duration is estimated based on daily traffic and required sample size (minimum 7 days to capture day-of-week effects)
- [ ] Maximum test duration is set to avoid indefinite running (typically 4-6 weeks cap)
- [ ] Traffic split is documented: 50/50 for two variants, equal distribution for multivariate

## Section 3: Technical Setup
- [ ] A/B testing tool is configured correctly (Google Optimize successor, VWO, Optimizely, or platform-native split testing)
- [ ] Traffic allocation is random and consistent (same user always sees the same variant via cookie/user ID)
- [ ] Test does not cause page flicker or visible layout shift during variant loading
- [ ] Analytics integration tracks variant exposure alongside conversion events
- [ ] QA testing confirms both control and variant render correctly across devices and browsers

## Section 4: Test Integrity
- [ ] No other significant changes are made to the page during the test period (feature launches, redesigns, promotions)
- [ ] External factors that could skew results are documented (holidays, PR events, competitor actions)
- [ ] Test is not peeked at prematurely for decision-making (no stopping early when results look promising)
- [ ] Statistical significance is calculated using a valid method: frequentist (p < 0.05) or Bayesian (95% probability to beat control)
- [ ] Multiple comparison correction is applied if testing more than 2 variants (Bonferroni or similar)
- [ ] Segmentation analysis is pre-planned (device, traffic source, new vs. returning) and not data-mined post-hoc

## Section 5: Results and Documentation
- [ ] Test results include: sample size per variant, conversion rate, statistical significance, confidence interval
- [ ] Winner is declared only after reaching the pre-calculated sample size AND minimum duration
- [ ] Results document includes insights and learnings, not just "Variant B won"
- [ ] Implementation plan for the winning variant is documented (who deploys, by when)
- [ ] Test results are archived in a shared repository with searchable tags for future reference
- [ ] Next test in the optimization roadmap is queued based on learnings from this test

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: cro-specialist-agent + analytics-agent
- **Escalation**: Tests declared without reaching statistical significance or with multiple uncontrolled variables are invalidated; results must not be used for decision-making
