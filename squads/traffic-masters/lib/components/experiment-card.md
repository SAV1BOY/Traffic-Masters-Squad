# Experiment Card Component

## Purpose
Standardized format for documenting and tracking individual experiments.

## Card Fields

### Setup
- **Experiment ID:** [EXP-XXX]
- **Name:** [Descriptive test name]
- **Hypothesis:** "If we [change], then [metric] will [improve/decrease] by [amount] because [reason]"
- **Variable:** What is being changed (one variable only)
- **Control:** Description of control variant
- **Variant:** Description of test variant

### Configuration
- **Platform:** Meta / Google / TikTok / YouTube / LinkedIn
- **Campaign:** [Campaign ID]
- **Primary Metric:** The one metric that determines the winner
- **Secondary Metrics:** Supporting metrics to monitor
- **Target Sample Size:** Minimum conversions for significance
- **Duration:** Estimated days to reach sample size
- **Budget Allocation:** Split percentage (usually 50/50)

### Results
- **Start Date:** [Date]
- **End Date:** [Date]
- **Control Result:** [Primary metric value]
- **Variant Result:** [Primary metric value]
- **Lift:** [% change]
- **Statistical Confidence:** [%]
- **Winner:** Control / Variant / Inconclusive

### Learnings
- **Key Insight:** What we learned
- **Next Test:** What this result suggests we test next
- **Applied To:** Campaigns where the learning was implemented

## Rules
1. One variable per test
2. Minimum 100 conversions per variant (ideally 300+)
3. Run for at least 7 days (full week cycle)
4. Document regardless of outcome
