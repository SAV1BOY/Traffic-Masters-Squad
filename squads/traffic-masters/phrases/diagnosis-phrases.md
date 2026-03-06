# Standard Phrases for Campaign Diagnostics

> Professional language for diagnosing campaign issues, identifying root causes, and communicating findings.

---

## Issue Identification Phrases

### Performance Degradation
- "Performance on [Campaign/Ad Set] has degraded [X]% over [timeframe], triggering a diagnostic review."
- "A [metric] anomaly was detected on [date], with values deviating [X]% from the trailing [Y]-day average."
- "[Metric] has breached the [upper/lower] threshold of [value], indicating a potential issue."
- "Sequential decline in [metric] over [X] consecutive days suggests a systemic issue rather than normal variance."
- "The performance pattern is inconsistent with expected behavior based on historical data and seasonality."

### Sudden Changes
- "An abrupt [increase/decrease] in [metric] occurred on [date], coinciding with [potential cause]."
- "[Metric] dropped [X]% between [date] and [date] without a corresponding change in inputs."
- "The account experienced a sharp performance shift beginning [date], which does not correlate with any scheduled changes."
- "Overnight [metric] movement of [X]% warrants immediate investigation."

### Gradual Erosion
- "[Metric] has gradually eroded from [value] to [value] over [timeframe], suggesting [creative fatigue / audience saturation / competitive pressure]."
- "Slow degradation in [metric] is consistent with [hypothesized cause]."
- "The trend line shows a steady [X]% [weekly/monthly] decline in [metric], compounding over time."

---

## Root Cause Analysis Phrases

### Creative-Related
- "Creative fatigue appears to be the primary driver, with frequency reaching [X] and CTR declining [Y]%."
- "Ad relevance diagnostics indicate below-average engagement, suggesting the creative is no longer resonating."
- "The winning creative has been running for [X] days without refresh — performance typically degrades after [Y] days in this account."
- "Creative A/B analysis shows all variants below historical CTR benchmarks, indicating the concept, not the execution, needs revision."
- "Image/video completion rates have declined [X]%, suggesting the creative is losing audience attention."

### Audience-Related
- "Audience saturation is indicated by rising frequency ([X]) and declining unique reach ([Y]%)."
- "The target audience has been exposed to ads an average of [X] times, exceeding the optimal frequency threshold of [Y]."
- "Audience overlap analysis reveals [X]% overlap between [Ad Set A] and [Ad Set B], causing internal competition."
- "Lookalike audience performance has degraded, potentially due to a change in the seed audience quality."
- "Exclusion lists have not been updated since [date], resulting in budget waste on already-converted users."

### Bidding & Budget-Related
- "The campaign exited the learning phase with insufficient conversions ([X] vs. the recommended [Y])."
- "Bid cap of $[X] appears too restrictive, limiting delivery and forcing suboptimal auction participation."
- "Budget distribution is heavily skewed — [X]% of spend is concentrated in [Y]% of ad sets."
- "Daily budget changes on [dates] reset the learning phase, preventing stable optimization."
- "Cost-per-result increase correlates with a budget increase that exceeded the recommended [X]% threshold."

### Landing Page / Conversion-Related
- "Click-through rate remains healthy at [X]%, but landing page conversion rate dropped to [Y]%, indicating a post-click issue."
- "Page load time increased from [X]s to [Y]s on [date], coinciding with the conversion rate decline."
- "Form submission errors spiked [X]% on [date], suggesting a technical issue on the destination page."
- "The disconnect between ad messaging and landing page content is likely causing the high bounce rate of [X]%."
- "Tracking pixel is not firing correctly on [page/event], resulting in underreported conversions."

### Platform / External-Related
- "A platform algorithm update on [date] appears to have impacted delivery patterns across the account."
- "Increased competitive activity in the auction (estimated [X]% CPM increase industry-wide) is pressuring costs."
- "Seasonal demand patterns for [industry] typically show a [X]% [increase/decrease] in CPMs during [period]."
- "Policy changes effective [date] resulted in [X] ad disapprovals, reducing active delivery."
- "Attribution window changes from [old] to [new] are affecting reported conversion counts."

### Tracking & Measurement-Related
- "Conversion tracking discrepancy of [X]% between [Platform] and [Analytics Tool] suggests a data integrity issue."
- "The [pixel/tag/SDK] was not firing on [specific page/event] between [date] and [date]."
- "UTM parameters are inconsistent across [X] campaigns, degrading attribution accuracy."
- "Server-side tracking shows [X]% more conversions than client-side, indicating ad blocker or browser privacy impact."
- "Cross-domain tracking is misconfigured, resulting in broken user sessions and lost attribution."

---

## Severity Classification Phrases

### Critical (Immediate Action Required)
- "This issue is actively losing revenue / wasting spend and requires immediate intervention."
- "Severity: Critical — estimated impact of $[X] per day if unresolved."
- "This is a P0 issue: tracking is broken and all reported data since [date] is unreliable."
- "Campaigns should be paused until [specific issue] is resolved."

### High (Action Within 24-48 Hours)
- "This issue is materially impacting performance and should be addressed within [X] hours."
- "Severity: High — performance is degrading at a rate that will significantly impact [period] results."
- "Continued operation without correction will compound the negative impact."

### Medium (Action Within the Week)
- "This issue is reducing efficiency but is not immediately critical."
- "Severity: Medium — optimization opportunity that, if addressed, could improve [metric] by [X]%."
- "This should be included in the next optimization cycle."

### Low (Monitor and Address When Possible)
- "This is a minor issue that does not currently impact performance materially."
- "Severity: Low — recommend monitoring over [timeframe] before taking action."
- "This represents a best-practice gap rather than an active performance issue."

---

## Hypothesis & Testing Phrases

- "Primary hypothesis: [Specific hypothesis]. Confidence: [High/Medium/Low] based on [evidence]."
- "We are testing the hypothesis that [cause] is driving the [metric] change by [test methodology]."
- "Two competing hypotheses: (1) [Hypothesis A] and (2) [Hypothesis B]. The diagnostic test plan is designed to isolate which is correct."
- "Preliminary data supports [hypothesis], though additional [timeframe/data] is needed for confirmation."
- "The diagnosis is inconclusive at this time. We recommend [specific diagnostic action] to narrow the root cause."

---

## Resolution & Next Steps Phrases

- "Recommended corrective action: [Specific action] with expected impact of [X]% improvement in [metric]."
- "Resolution implemented on [date]: [Description of fix]. Monitoring period: [X] days."
- "The issue has been resolved. Post-fix data shows [metric] returning to [expected range/value]."
- "Multiple contributing factors identified. Remediation plan addresses them in order of impact: [1, 2, 3]."
- "Root cause confirmed. Preventive measures have been added to the monitoring checklist to catch this earlier in the future."

---

## Usage Guidelines

1. **Be specific** — Vague diagnoses erode confidence; always name the metric, the magnitude, and the timeframe
2. **Separate symptoms from causes** — Rising CPA is a symptom; audience saturation is a cause
3. **Present hypotheses, not guesses** — Frame potential causes as hypotheses with supporting evidence
4. **Include severity and urgency** — Not all issues require immediate action; classify appropriately
5. **Provide actionable next steps** — Every diagnosis must end with a recommended action
6. **Document for future reference** — Diagnostic findings should be logged to prevent repeat issues
