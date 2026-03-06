# Recommendation Language Guide

## Purpose
Standard language for making recommendations in paid traffic operations. Ensures recommendations are clear, actionable, evidence-based, and appropriately confident.

---

## Recommendation Structure

Every recommendation should follow this pattern:
```
WHAT: [Specific action to take]
WHY: [Evidence or rationale]
IMPACT: [Expected outcome, quantified if possible]
PRIORITY: [P1/P2/P3]
TIMELINE: [When to execute]
```

---

## Confidence Tiers

### High Confidence -- Strong Evidence
**Use when:** Data clearly supports the recommendation with statistical significance or consistent historical pattern.

| Language | Example |
|---|---|
| "We recommend..." | "We recommend increasing budget on Campaign X by 20%, based on 14 days of CPA consistently below target." |
| "The data strongly supports..." | "The data strongly supports pausing Ad Set Y -- CPA is 180% of target across 45 conversions." |
| "Based on clear evidence..." | "Based on clear evidence of creative fatigue (CTR down 40% from peak), we recommend launching new creative variants." |

### Medium Confidence -- Directional Evidence
**Use when:** Evidence is suggestive but not conclusive, or sample size is moderate.

| Language | Example |
|---|---|
| "We suggest..." | "We suggest testing a broader lookalike audience, as initial data from our 2% LAL shows promising CPA." |
| "Initial data indicates..." | "Initial data indicates UGC outperforms polished creative for this audience -- we suggest expanding this approach." |
| "Our analysis points toward..." | "Our analysis points toward Google Shopping as the most efficient channel; we suggest a 15% budget shift." |

### Low Confidence -- Hypothesis or Limited Data
**Use when:** Limited data, new territory, or speculative reasoning.

| Language | Example |
|---|---|
| "We propose testing..." | "We propose testing TikTok as a new channel; while we have no direct data, competitor analysis suggests opportunity." |
| "It may be worth exploring..." | "It may be worth exploring dayparting, as we observe a pattern of higher CPA during overnight hours." |
| "One option to consider..." | "One option to consider is reducing retargeting window from 30 to 14 days, which may improve audience quality." |

---

## Action Language

### Prescriptive Actions (Use for P1 recommendations)

| Action | Phrasing |
|---|---|
| Increase | "Increase budget by [X]% on [CAMPAIGN]." |
| Decrease | "Reduce spend on [CAMPAIGN] by [X]%." |
| Pause | "Pause [AD_SET/CAMPAIGN] immediately." |
| Launch | "Launch [NEW_CAMPAIGN/CREATIVE/AUDIENCE]." |
| Test | "Run an A/B test comparing [A] vs. [B]." |
| Shift | "Reallocate $[AMOUNT] from [SOURCE] to [DESTINATION]." |
| Monitor | "Monitor [METRIC] daily for [DURATION] before acting." |
| Refresh | "Refresh creative in [CAMPAIGN] with [X] new variations." |

### Conditional Actions (Use for contingency recommendations)

```
"If [CONDITION] persists for [DURATION], then [ACTION]."
"Should [METRIC] exceed [THRESHOLD], we recommend [ACTION]."
"In the event that [SCENARIO], the contingency plan is [PLAN]."
```

**Examples:**
- "If CPA remains above $60 for 3 more days, we recommend reducing daily budget by 20%."
- "Should the new creative variants not outperform the control within 7 days, we will revert to the original strategy."

---

## Impact Language

### Quantified Impact (Preferred)
- "This is projected to reduce CPA by 15-20%, saving approximately $3,000/month."
- "We estimate this change will increase conversion volume by 25% while maintaining current CPA."
- "At current ROAS, reallocating $5,000 to Google Shopping would generate an additional $25,000 in monthly revenue."

### Directional Impact (When quantification is not possible)
- "This should improve efficiency by reducing wasted spend on low-performing segments."
- "We expect this to positively impact CTR as the new creative addresses a proven pain point."
- "This positions us to scale more efficiently once the learning phase completes."

---

## Priority Language

| Priority | Language | Implication |
|---|---|---|
| **P0** | "Immediate action required" | Do this today, drop everything else |
| **P1** | "High priority -- execute this week" | Part of this week's optimization plan |
| **P2** | "Recommended for this month" | Important but not time-sensitive |
| **P3** | "Worth considering when capacity allows" | Nice to have, not urgent |

---

## Framing Recommendations Positively

| Instead of | Use |
|---|---|
| "We need to stop wasting money on..." | "We recommend reallocating budget from underperforming areas to higher-efficiency channels." |
| "This campaign is failing." | "This campaign is not meeting performance thresholds. We recommend [action]." |
| "You should have been doing this already." | "An opportunity exists to improve results by implementing [action]." |
| "The landing page is terrible." | "Landing page optimization represents the highest-impact opportunity in the current funnel." |

---

## Example Recommendation Blocks

**Strong Recommendation:**
> We recommend increasing the daily budget on the Google Shopping campaign from $150 to $200 per day. Over the past 21 days, this campaign has delivered a consistent 5.8x ROAS with a CPA of $28 -- well below our $40 target. At the proposed budget level, we project an additional 35 monthly conversions and $9,800 in revenue. This is our highest-priority optimization for this week.

**Conditional Recommendation:**
> If Meta prospecting CPA remains above $55 through Friday, we suggest reducing the daily budget by 15% and redirecting the savings to retargeting campaigns, which are currently delivering $35 CPA. We will reassess on Monday after the creative refresh launches.

**Exploratory Recommendation:**
> We propose allocating $1,500 from the testing budget to a 2-week TikTok pilot campaign. While we do not have direct performance data, competitor analysis shows 3 of our top 5 competitors actively advertising on TikTok, and the platform's CPM is approximately 40% lower than Meta for similar audiences. Expected outcome: directional CPA data within 14 days.
