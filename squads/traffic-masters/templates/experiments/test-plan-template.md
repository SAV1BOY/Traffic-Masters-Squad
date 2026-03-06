# Test Plan Template

> **Type**: Template
> **Category**: experiments
> **Used by tasks**: experiment-execution, a-b-testing, campaign-optimization
> **Filled by agents**: strategist-agent, media-buyer-agent, analyst-agent

## Purpose
Provides the operational plan for executing a test, covering hypothesis, test type, sample size, duration, budget, control vs variant setup, success metrics, and stop criteria to ensure rigorous and actionable experiments.

## Template

### Test Metadata
**Test ID**: [T-001]
**Test name**: [descriptive name]
**Hypothesis ID**: [link to hypothesis-template.md entry]
**Created by**: [person or agent]
**Start date**: [date]
**Planned end date**: [date]
**Status**: [planned / active / paused / complete / cancelled]

### Hypothesis
**Statement**: "If we [change X] for [audience Y], then [metric Z] will [improve by N%] because [rationale]."
**Reference**: [link to full hypothesis document]

### Test Type
**Method**: [A/B test / A/B/C test / multivariate / sequential / holdout]
**Platform tool**: [Meta A/B test / Google Experiments / manual split / third-party tool]
**Split method**: [random / audience split / geo split / time split]
**Split ratio**: [50/50 / 70/30 / 33/33/33]
**Randomization**: [platform-managed / manual]

### Sample Size
**Required per variant**: [number of conversions or impressions]
**Total required**: [across all variants]
**Calculation inputs**:
- Baseline conversion rate: [current rate]
- Minimum detectable effect: [percentage improvement to detect]
- Statistical power: [80% / 90%]
- Significance level: [95% / 90%]
**Calculator used**: [tool name or formula]

### Duration
**Minimum duration**: [days - based on sample size and daily volume]
**Maximum duration**: [days - beyond which external factors confound results]
**Full business cycles**: [ensure test covers at least 1-2 complete weekly cycles]
**Blackout dates**: [dates to exclude: holidays, sales events, outages]

### Budget
**Total test budget**: [amount]
**Budget per variant**: [amount]
**Daily spend per variant**: [amount]
**Budget source**: [testing reserve / campaign budget / incremental]
**Overspend protection**: [daily or lifetime cap per variant]

### Control vs Variant

#### Control (A)
**Description**: [current version - what exists today]
**Creative / copy**: [exact creative or ad being used]
**Audience**: [targeting details]
**Landing page**: [URL]
**Settings**: [bid strategy, placements, schedule]

#### Variant (B)
**Description**: [what changed and only what changed]
**Creative / copy**: [exact creative or ad being tested]
**Audience**: [must match control unless audience is the variable]
**Landing page**: [URL - must match control unless LP is the variable]
**Settings**: [must match control unless settings are the variable]

#### Variant (C) [if applicable]
**Description**: [second variant details]
**Change from control**: [single variable difference]

### Success Metric
**Primary metric**: [the one metric that decides the winner]
**How measured**: [platform reporting / GA4 / blended / offline]
**Current baseline**: [value]
**Target improvement**: [percentage or absolute value]
**Confidence threshold**: [95% / 90%]

### Secondary Metrics
| Metric | Baseline | Monitor For | Alert Threshold |
|---|---|---|---|
| [CTR] | [value] | Improvement | Drop below [X] |
| [CPA] | [value] | Improvement | Increase above [X] |
| [CVR] | [value] | Improvement | Drop below [X] |
| [ROAS] | [value] | Improvement | Drop below [X] |

### Stop Criteria
**Stop early if**:
- Variant CPA exceeds control by more than [X]% for [Y] consecutive days
- Variant spend reaches [amount] with zero conversions
- External event invalidates test conditions (platform outage, site issue)
- One variant reaches statistical significance early with [confidence level]

**Do NOT stop if**:
- Results fluctuate day-to-day within normal variance
- One variant is "winning" but below confidence threshold
- Sample size has not been reached

### Execution Checklist
- [ ] Hypothesis documented and approved
- [ ] Test setup verified (only one variable differs)
- [ ] Tracking confirmed for all metrics
- [ ] Budget allocated and caps set
- [ ] Start date and end date agreed
- [ ] Monitoring schedule defined (daily check-ins)
- [ ] Stop criteria documented and shared
- [ ] Results template prepared (learnings-log-template.md)

### Post-Test Actions
**If variant wins**: [scale variant, kill control, document learning, plan iteration]
**If control wins**: [keep control, document why variant failed, plan next test]
**If inconclusive**: [extend test / increase budget / redesign test / deprioritize]
**Documentation**: Record all results in learnings-log-template.md

## Usage Notes
- Never evaluate a test before reaching minimum sample size.
- Run tests for complete weekly cycles to avoid day-of-week bias.
- One test at a time per audience to prevent interaction effects.

## Example
A/B test on Meta: Control uses question hook, Variant uses stat hook. Same audience, same body copy, same landing page. 50/50 split, $50/day per variant, 14-day duration, primary metric is CPA with 95% confidence target.

## Related
- hypothesis-template.md
- learnings-log-template.md
- creative-iteration-template.md
