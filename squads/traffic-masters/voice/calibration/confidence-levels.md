# Confidence Levels Calibration Guide

## Purpose
Framework for calibrating how confidently to express recommendations, conclusions, and predictions in paid traffic operations. Ensures communication accuracy matches evidence quality.

---

## Confidence Scale

| Level | Label | Evidence Required | Language Pattern |
|---|---|---|---|
| **5** | Very High | Statistical significance + consistent over 2+ weeks + large sample | "We are confident that..." / "The data clearly shows..." |
| **4** | High | Strong directional data + consistent over 1+ weeks + adequate sample | "We recommend..." / "Based on strong evidence..." |
| **3** | Moderate | Directional data + short observation period or moderate sample | "We suggest..." / "Initial data indicates..." |
| **2** | Low | Limited data + early results + small sample | "We propose testing..." / "Early signals suggest..." |
| **1** | Very Low | No data + hypothesis only + industry intuition | "One option to explore..." / "It may be worth considering..." |

---

## Confidence Level Detail

### Level 5: Very High Confidence

**When to use:**
- A/B test with 95%+ statistical significance and 50+ conversions per variant
- KPI trend consistent for 14+ days across multiple campaigns
- Historical pattern confirmed across 3+ previous instances

**Language:**
- "We are confident that [CONCLUSION]."
- "The data clearly demonstrates that [FINDING]."
- "This is a proven approach based on [EVIDENCE]."
- "[VARIANT_B] outperforms the control with 97% confidence."

**Example:**
> "We are confident that UGC video creative outperforms polished studio content for cold audiences in this account. This finding is consistent across 8 creative tests over 3 months, with an average CPA reduction of 28% (95% confidence interval: 18-38%)."

---

### Level 4: High Confidence

**When to use:**
- Performance metric has been consistent for 7-14 days
- 20-50 conversions supporting the conclusion
- Pattern aligns with known best practices or previous account data

**Language:**
- "We recommend [ACTION] based on [EVIDENCE]."
- "The data supports [CONCLUSION]."
- "Based on [PERIOD] of consistent performance, [FINDING]."
- "We have strong reason to believe [CONCLUSION]."

**Example:**
> "We recommend scaling the Google Shopping campaign budget by 20%. Over the past 10 days, it has delivered a consistent $32 CPA on 38 conversions, 36% below our $50 target. This performance aligns with the historical pattern we've observed for this campaign type."

---

### Level 3: Moderate Confidence

**When to use:**
- 10-20 conversions supporting the observation
- 3-7 days of data
- Pattern is logical but not yet statistically validated

**Language:**
- "We suggest [ACTION] based on initial data."
- "Initial results indicate [FINDING], though we need more data to confirm."
- "The trend is directional: [OBSERVATION]. We recommend [ACTION] while continuing to monitor."
- "Our analysis points toward [CONCLUSION], with moderate confidence."

**Example:**
> "Initial results from the TikTok test indicate promising performance -- 12 conversions at $38 CPA over 5 days. We suggest maintaining the current budget for 10 more days to build a statistically meaningful sample before scaling."

---

### Level 4 -> Level 2: Low Confidence

**When to use:**
- Fewer than 10 conversions
- Less than 3 days of data
- New territory with no historical reference point

**Language:**
- "Early signals suggest [OBSERVATION], but the data is insufficient for a definitive conclusion."
- "We propose testing [APPROACH] to validate whether [HYPOTHESIS]."
- "Preliminary data is [PROMISING/CONCERNING], but we need [X] more [DAYS/CONVERSIONS] before recommending action."
- "This is our working hypothesis, pending further data."

**Example:**
> "After 2 days and 4 conversions on the new audience segment, early signals suggest a CPA in the $40-$60 range. This is preliminary -- we propose continuing the test for at least 10 more days before drawing conclusions."

---

### Level 1: Very Low Confidence (Hypothesis)

**When to use:**
- No direct data available
- Pure hypothesis based on industry knowledge, competitor analysis, or intuition
- New platform, market, or approach

**Language:**
- "One option to explore is [APPROACH]."
- "It may be worth considering [ACTION], based on [INDIRECT_EVIDENCE]."
- "We hypothesize that [THEORY]. We recommend a small-budget test to validate."
- "Based on industry trends (not account-specific data), [OBSERVATION]."

**Example:**
> "It may be worth considering Pinterest as an additional channel for this product category. We don't have direct data, but competitor analysis shows 2 of our 5 key competitors have been running Pinterest ads for 6+ months, suggesting they are finding value. We recommend a $1,000, 3-week pilot to gather initial data."

---

## Calibration Rules

### Upgrade Confidence When:
- Sample size increases past significance thresholds
- Observation period extends and pattern holds
- Multiple independent data points confirm the same conclusion
- Result aligns with established best practices or historical patterns

### Downgrade Confidence When:
- Sample size is smaller than initially assumed
- External factors may be influencing results (seasonality, platform changes)
- Result contradicts established patterns (may be novelty effect)
- Data is from a single campaign or ad set (not generalizable)

---

## Common Calibration Mistakes

| Mistake | Problem | Correction |
|---|---|---|
| **Overconfidence with small data** | Declaring a winner after 8 conversions | State the evidence level: "directional but not conclusive" |
| **Underconfidence with strong data** | Hedging despite clear statistical significance | Use confident language when the data warrants it |
| **False precision** | "CPA will be exactly $42.37" | Use ranges: "We project CPA in the $40-$50 range" |
| **Anchoring to a single metric** | High confidence based on CTR alone, ignoring CPA | Cross-reference multiple metrics before declaring confidence |
| **Ignoring base rates** | "This is definitely going to work" for a new strategy | Most new strategies fail; calibrate accordingly |

---

## Expressing Uncertainty Ranges

### For Projections
- **High confidence:** "We project [X] conversions, plus or minus 10%."
- **Moderate confidence:** "We estimate [X]-[Y] conversions, depending on [VARIABLE]."
- **Low confidence:** "If performance holds, we could see anywhere from [X] to [Y] conversions."

### For Timelines
- **High confidence:** "We expect to see results within [X] days."
- **Moderate confidence:** "Results should begin to appear within [X]-[Y] days."
- **Low confidence:** "We will have directional data within [X] days, but conclusive results may take [Y] days."
