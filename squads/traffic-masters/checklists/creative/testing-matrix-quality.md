# Creative Testing Matrix Design Quality Gate

> Quality gate for creative testing matrix design and A/B test structure. Must pass before creative tests are launched on any platform.

## Section 1: Test Hypothesis Definition
- [ ] Each test has a clearly written hypothesis: "If we change [variable], then [expected outcome] because [rationale]"
- [ ] The hypothesis is based on data or insights (past performance, audience research, competitor analysis), not guesswork
- [ ] Only one variable is tested per experiment (isolate: visual, headline, CTA, format, or audience)
- [ ] The expected impact is quantified with a target lift percentage (e.g., "We expect CTR to improve by 15%")
- [ ] The test has a documented learning goal beyond just "which one wins" (what insight will inform future creative)

## Section 2: Test Matrix Structure
- [ ] The testing matrix is documented in a spreadsheet or project management tool with all variants mapped
- [ ] Control variant (current best performer or baseline) is included in every test
- [ ] Number of variants is manageable: 2-4 per test (more than 4 dilutes traffic and delays significance)
- [ ] Naming convention for test variants is consistent: [Test Name]_[Variable]_[Variant Letter] (e.g., "Q1-Promo_Headline_A")
- [ ] Test variants are mapped to specific ad sets or campaigns with clear tagging

## Section 3: Statistical Rigor
- [ ] Minimum sample size per variant is calculated before launch (use a statistical significance calculator)
- [ ] Expected test duration is documented based on daily traffic and required sample size
- [ ] Confidence level is set at 95% (p < 0.05) for declaring a winner
- [ ] Test will not be called early (minimum 7 days runtime or minimum sample size, whichever is longer)
- [ ] External factors (seasonality, promotions, algorithm changes) are accounted for in the test design

## Section 4: Creative Variant Design
- [ ] Visual variants test meaningful differences (different imagery, not just color tweaks)
- [ ] Copy variants test different messaging angles (benefit vs. feature, emotional vs. rational)
- [ ] CTA variants test different actions or urgency levels (Shop Now vs. Learn More, with/without urgency)
- [ ] Format variants test different ad types (static vs. video, carousel vs. single image)
- [ ] Each variant is production-quality (no "quick and dirty" variants that would bias results)

## Section 5: Measurement and Learning Documentation
- [ ] Primary metric for declaring a winner is defined before launch (CTR, CPA, ROAS, or conversion rate)
- [ ] Secondary metrics are tracked for additional context (engagement rate, view-through rate, bounce rate)
- [ ] Test results template is prepared with fields for: hypothesis, variants, metrics, winner, confidence level, insights
- [ ] Process exists for applying learnings: winning elements are incorporated into the next round of creative
- [ ] Testing cadence is established: continuous testing with a new test launching as the previous one concludes
- [ ] Historical test results are archived in a shared repository for team-wide learning

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: creative-strategist-agent + analytics-agent
- **Escalation**: Tests without a clear hypothesis or with more than one variable changed simultaneously must be redesigned before launch
