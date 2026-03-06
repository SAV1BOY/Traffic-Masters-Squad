# Hypothesis Template

> **Type**: Template
> **Category**: experiments
> **Used by tasks**: experiment-design, creative-testing, optimization
> **Filled by agents**: strategist-agent, analyst-agent, creative-strategist-agent

## Purpose
Structures a clear, testable hypothesis for any paid media experiment, defining the change, target audience, expected outcome, rationale, variables, metrics, duration, and decision criteria before the test begins.

## Template

### Hypothesis Metadata
**Hypothesis ID**: [H-001]
**Date created**: [date]
**Created by**: [person or agent]
**Related campaign**: [campaign name or ID]
**Priority**: [high / medium / low]
**Status**: [draft / approved / in-test / complete]

### Hypothesis Statement
**Format**: "If we [change X] for [audience Y], then [metric Z] will [improve by N%] because [rationale]."

**Completed statement**:
"If we [describe the specific change being made] for [describe the target audience segment], then [name the primary metric] will [increase/decrease] by [expected magnitude or range] because [explain the reasoning based on data, insight, or theory]."

### Variables

#### Independent Variable (What We Change)
**Variable name**: [the thing being tested]
**Control (A)**: [current state or baseline version]
**Variant (B)**: [new version being tested]
**Variant (C)**: [additional variant if applicable]
**Isolation**: [confirm only one variable changes between control and variant]

#### Dependent Variable (What We Measure)
**Primary metric**: [the one metric that determines success]
**Secondary metrics**: [supporting metrics to monitor]
**Guardrail metrics**: [metrics that must not degrade]

### Metrics and Targets
| Metric | Current Baseline | Target (Variant) | Minimum Detectable Effect | Guardrail |
|---|---|---|---|---|
| [Primary metric] | [current value] | [target value] | [smallest meaningful difference] | N/A |
| [Secondary metric 1] | [current value] | [target value] | [MDE] | [must not drop below X] |
| [Secondary metric 2] | [current value] | [target value] | [MDE] | [must not drop below X] |

### Duration and Sample Size
**Estimated duration**: [days or weeks]
**Required sample size**: [number of impressions, clicks, or conversions per variant]
**Calculation method**: [statistical power calculator, platform recommendation, or rule of thumb]
**Statistical significance target**: [95% confidence / 90% confidence]
**Minimum data threshold**: [minimum conversions before evaluating - typically 50 per variant]

### Decision Criteria
**Winner declared if**: [Primary metric improves by X% with Y% confidence]
**Loser declared if**: [Primary metric does not improve or degrades with Y% confidence]
**Inconclusive if**: [Neither threshold met after maximum duration]
**If winner**: [Scale variant, iterate further, apply learning to other campaigns]
**If loser**: [Revert to control, document learning, test next hypothesis]
**If inconclusive**: [Extend test, increase budget, or deprioritize this variable]

### Rationale and Evidence
**Why we believe this will work**:
- [Data point or past result supporting the hypothesis]
- [Industry benchmark or competitor observation]
- [Theoretical framework or psychological principle]

**Risks and assumptions**:
- [Assumption 1 that must be true for hypothesis to hold]
- [Risk 1 that could invalidate results]
- [External factor that could confound the test]

### Pre-Test Checklist
- [ ] Hypothesis statement is specific and falsifiable
- [ ] Only one variable changes between control and variant
- [ ] Sample size calculation is complete
- [ ] Tracking is in place to measure all metrics
- [ ] Test duration is agreed upon before launch
- [ ] Decision criteria are documented before launch
- [ ] Stakeholders are aligned on the test plan

## Usage Notes
- Write the hypothesis before building the test. Never run a test without a documented hypothesis.
- Decision criteria must be agreed upon before the test starts to prevent post-hoc rationalization.
- Log all results in the learnings-log-template.md regardless of outcome.

## Example
"If we change the hook from a question to a bold stat for our cold LAL audience on Meta, then CTR will increase by 15% because data-driven hooks have outperformed questions in our last 3 tests at 95% confidence."

## Related
- test-plan-template.md
- learnings-log-template.md
- creative-iteration-template.md
