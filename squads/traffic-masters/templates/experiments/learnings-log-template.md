# Learnings Log Template

> **Type**: Template
> **Category**: experiments
> **Used by tasks**: experiment-analysis, knowledge-management, optimization-planning
> **Filled by agents**: analyst-agent, strategist-agent

## Purpose
Records the outcome of every test and experiment in a structured format, building an institutional knowledge base of what works, what does not, and why, enabling compounding improvement over time.

## Template

### Log Entry Header
**Entry ID**: [L-001]
**Date**: [date test concluded]
**Logged by**: [person or agent]
**Test ID**: [reference to test-plan-template.md entry]
**Hypothesis ID**: [reference to hypothesis-template.md entry]

### Test Name
**Name**: [descriptive test name]
**Platform**: [Meta / Google / YouTube / TikTok / LinkedIn / cross-platform]
**Campaign**: [campaign name]
**Test duration**: [start date to end date]
**Total spend**: [amount spent during test]

### Hypothesis
**Original hypothesis**: "If we [change X] for [audience Y], then [metric Z] will [improve by N%] because [rationale]."

### Result
**Outcome**: [Won / Lost / Inconclusive]
**Statistical confidence**: [percentage]
**Sample size achieved**: [number per variant]

### Performance Data
| Metric | Control (A) | Variant (B) | Delta | Significant? |
|---|---|---|---|---|
| [Primary metric] | [value] | [value] | [+/- %] | [yes/no] |
| [Secondary metric 1] | [value] | [value] | [+/- %] | [yes/no] |
| [Secondary metric 2] | [value] | [value] | [+/- %] | [yes/no] |
| [Guardrail metric] | [value] | [value] | [+/- %] | [within bounds?] |

### Key Insight
**What we learned**: "[One clear sentence summarizing the takeaway. This should be actionable and generalizable.]"

**Why this happened**: "[Explain the underlying reason for the result. Was the hypothesis correct, partially correct, or wrong? What drove the outcome?]"

**Surprising findings**: "[Anything unexpected in the data, even if not the primary metric.]"

### Next Action
**Immediate action**: [Scale winner / Kill loser / Iterate / Retest]
**Follow-up test**: [Describe the next experiment this learning suggests]
**Apply to other campaigns**: [yes/no - if yes, which ones]
**Timeline for next action**: [date or sprint]

### Confidence Level
**How confident are we in this learning?**
- [ ] **High** - Large sample, strong statistical significance, clear causal mechanism
- [ ] **Medium** - Adequate sample, moderate significance, plausible explanation
- [ ] **Low** - Small sample, borderline significance, or confounding factors present

**Caveats**: [Any factors that limit the generalizability of this learning]

### Data Source
**Primary data source**: [platform reporting / GA4 / blended / offline data]
**Screenshots or links**: [link to dashboard, report, or data export]
**Raw data location**: [file path or database reference]

### Tags
**Variable tested**: [hook / angle / audience / bid-strategy / format / landing-page / offer / copy]
**Platform**: [meta / google / youtube / tiktok / linkedin]
**Funnel stage**: [tofu / mofu / bofu]
**Category**: [creative / targeting / bidding / funnel / tracking]

### Cumulative Learnings Index
Use this section to maintain a running summary of patterns across multiple log entries.

| Pattern | Supporting Tests | Confidence |
|---|---|---|
| [Stat hooks outperform question hooks] | [L-001, L-005, L-012] | High |
| [UGC outperforms polished on TikTok TOFU] | [L-003, L-008] | Medium |
| [Pain angles beat desire for cold audiences] | [L-002, L-007, L-011] | High |
| [pattern] | [test IDs] | [confidence] |

## Usage Notes
- Log every test result, including losses and inconclusive outcomes.
- Review the cumulative learnings index monthly to identify macro patterns.
- Share learnings across teams; insights from one campaign often apply to others.
- Never delete log entries; the history of failed experiments is as valuable as successes.

## Example
Test L-015: Tested bold-stat hook vs. question hook on Meta for cold LAL audience. Stat hook reduced CPA by 22% at 96% confidence over 14 days. Key insight: data-driven hooks create stronger pattern interrupts for this audience. Next action: roll out stat hooks across all TOFU campaigns and test stat variations.

## Related
- hypothesis-template.md
- test-plan-template.md
- creative-iteration-template.md
- creative-analysis-report.md
