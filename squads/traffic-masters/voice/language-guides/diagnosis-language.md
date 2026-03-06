# Diagnosis Language Guide

## Purpose
Standard language for diagnosing, explaining, and communicating performance issues in paid traffic campaigns. Ensures root cause analysis is communicated clearly and constructively.

---

## Diagnosis Communication Structure

```
1. SYMPTOM: What we are observing (data-backed)
2. LOCATION: Where in the funnel/system the issue occurs
3. TIMING: When it started and how long it has persisted
4. CAUSE: What is driving the issue (confirmed or hypothesized)
5. SEVERITY: How significant is the impact
6. ACTION: What we are doing about it
```

---

## Symptom Language

### How to Describe What You See

| Symptom | Clear Language | Avoid |
|---|---|---|
| CPA rising | "CPA has increased [X]% over [PERIOD], from $[A] to $[B]." | "CPA is getting worse." |
| Conversions dropping | "Conversion volume declined [X]% WoW, from [A] to [B] conversions." | "We're not getting enough sales." |
| Spend not delivering | "The campaign is spending only [X]% of its daily budget." | "The campaign isn't working." |
| CTR declining | "CTR has fallen from [A]% to [B]% over the past [PERIOD]." | "Nobody's clicking." |
| ROAS below target | "ROAS is [X]x, which is [Y]% below our [Z]x target." | "We're losing money." |
| Tracking gap | "Platform-reported conversions are [X]% lower than backend data." | "The numbers don't add up." |

---

## Location Language

### Funnel Stage Diagnosis

| Stage | Diagnostic Language |
|---|---|
| **Delivery** | "The issue is occurring at the delivery level -- the campaign is not serving impressions as expected." |
| **Creative/Attention** | "The issue appears to be at the creative level -- CTR has declined while other funnel metrics remain stable." |
| **Traffic Quality** | "The issue is in traffic quality -- clicks are coming through but landing page view rate has dropped significantly." |
| **Landing Page** | "The drop-off is occurring on the landing page -- LP view-to-conversion rate has decreased." |
| **Checkout/Form** | "The issue is at the checkout stage -- add-to-cart rates are stable but checkout completion has declined." |
| **Tracking** | "This appears to be a tracking issue rather than a performance issue -- backend data shows conversions the platform is not capturing." |
| **Attribution** | "This may be an attribution issue -- the change in reported performance coincides with a change in attribution settings." |

---

## Cause Language

### Confirmed Causes
**Use when the root cause has been verified:**

- "The root cause has been identified: [SPECIFIC_CAUSE]."
- "We have confirmed that [CAUSE] is responsible for [SYMPTOM]."
- "After investigation, we determined that [CHANGE/EVENT] triggered [OUTCOME]."

### Hypothesized Causes
**Use when the cause is likely but not confirmed:**

- "The most likely cause is [HYPOTHESIS], based on [EVIDENCE]."
- "We believe this is driven by [CAUSE], as indicated by [SUPPORTING_DATA]."
- "Our working hypothesis is [CAUSE]. We are validating this by [METHOD]."

### Multiple Potential Causes
**Use when several factors may be contributing:**

- "We have identified [NUMBER] potential contributing factors: [CAUSE_1], [CAUSE_2], and [CAUSE_3]. We are evaluating each."
- "This appears to be a combination of [CAUSE_1] and [CAUSE_2], with [CAUSE_1] being the primary driver."

---

## Common Diagnosis Templates

### Creative Fatigue
> "CTR on [CREATIVE_NAME] has declined [X]% from its peak of [Y]% over the past [PERIOD]. Frequency has reached [Z], suggesting the audience has been over-exposed to this creative. The CPA impact is approximately +$[AMOUNT]. We recommend launching [N] new creative variations to address this fatigue."

### Audience Saturation
> "Frequency on [AD_SET] has exceeded [X], and we are seeing diminishing returns with marginal CPA now [Y]% above average CPA. The audience pool appears saturated at the current spend level. Options include expanding to a broader lookalike, adding new interest targets, or reducing spend on this segment."

### Funnel Breakdown
> "Conversion rate on the landing page has dropped from [X]% to [Y]% over the past [PERIOD], while traffic quality metrics (CTR, CPC) remain stable. This isolates the issue to the landing page or post-click experience. We are investigating whether a recent page change, load speed issue, or offer change is responsible."

### Tracking Issue
> "We are observing a [X]% discrepancy between platform-reported conversions and backend/analytics data. The gap began approximately [DATE]. Possible causes include: (1) pixel code modification during a recent site deployment, (2) CAPI connection interruption, or (3) changes to cookie consent settings. We are testing each hypothesis."

### Market/Competition
> "CPM on [PLATFORM] has increased [X]% over the past [PERIOD] across all campaigns, while our ad quality metrics remain stable. This suggests the increase is market-driven (competitive pressure or seasonal demand) rather than account-specific. This is consistent with the [Y]% CPM increase we observed during the same period last year."

---

## Severity Language

| Severity | Language | Numerical Threshold |
|---|---|---|
| **Critical** | "This requires immediate attention." | CPA > 2x target, tracking broken, budget overrun |
| **High** | "This is a significant concern that needs to be addressed this week." | CPA 50-100% above target for 3+ days |
| **Moderate** | "This is worth monitoring and acting on if the trend continues." | CPA 20-50% above target, CTR declining |
| **Low** | "This is noted but does not require immediate action." | Minor fluctuation, single-day anomaly |

---

## Separating Signal from Noise

### Signal (Requires diagnosis)
- "This is a sustained trend across [X] days/weeks, affecting [SCOPE]."
- "This change coincides with [SPECIFIC_EVENT] and is consistent across [SEGMENTS]."
- "The magnitude of this change ([X]%) exceeds normal day-to-day variation."

### Noise (Note but do not overreact)
- "This is a single-day fluctuation within normal variance."
- "This change is within the expected range given [SAMPLE_SIZE/DAY_OF_WEEK/SEASONALITY]."
- "We do not see this pattern across other campaigns, suggesting it is isolated and likely temporary."

---

## Anti-Patterns

| Avoid | Use Instead |
|---|---|
| "I don't know why this is happening." | "We are investigating [X] potential causes and will have clarity by [DATE]." |
| "It's the platform's fault." | "The change appears to be driven by platform-level auction dynamics." |
| "Everything is broken." | "We have identified a specific issue at [STAGE] that is impacting [METRIC]." |
| "This always happens." | "This pattern is consistent with [SEASONAL/HISTORICAL_TREND]." |
| Diagnosing without data | "Based on [DATA/EVIDENCE], the most likely cause is [CAUSE]." |
| Presenting diagnosis without a plan | Always end with: "Here is what we are doing about it: [ACTION]." |
