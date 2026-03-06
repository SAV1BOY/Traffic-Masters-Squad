# Experiment Results Report

## Report Metadata

| Field | Value |
|---|---|
| **Experiment Name** | `{{EXPERIMENT_NAME}}` |
| **Experiment ID** | `{{EXPERIMENT_ID}}` |
| **Prepared By** | `{{ANALYST_NAME}}` |
| **Client / Account** | `{{CLIENT_NAME}}` |
| **Platform** | `{{PLATFORM}}` |
| **Test Start Date** | `{{START_DATE}}` |
| **Test End Date** | `{{END_DATE}}` |
| **Test Duration** | `{{DURATION}}` days |
| **Status** | `{{COMPLETED / STILL RUNNING / STOPPED EARLY}}` |

---

## Executive Summary

> One-paragraph summary: what was tested, which variant won, by how much, and what the recommended next action is.

`{{EXECUTIVE_SUMMARY}}`

---

## Test Design

### Hypothesis

> **If** we `{{CHANGE_DESCRIPTION}}`, **then** `{{EXPECTED_OUTCOME}}`, **because** `{{RATIONALE}}`.

### Test Variable

| Element | Description |
|---|---|
| **Variable Type** | `{{CREATIVE / AUDIENCE / BID STRATEGY / COPY / LANDING PAGE / OFFER / PLACEMENT}}` |
| **Control (A)** | `{{CONTROL_DESCRIPTION}}` |
| **Variant (B)** | `{{VARIANT_B_DESCRIPTION}}` |
| **Variant (C)** | `{{VARIANT_C_DESCRIPTION}}` (if applicable) |

### Test Parameters

| Parameter | Value |
|---|---|
| **Primary Success Metric** | `{{CPA / ROAS / CTR / CVR / OTHER}}` |
| **Secondary Metrics** | `{{SECONDARY_METRICS}}` |
| **Minimum Detectable Effect** | `{{}}`% |
| **Required Confidence Level** | `{{}}`% |
| **Required Sample Size** | `{{}}` per variant |
| **Traffic Split** | `{{50/50, 33/33/33, etc.}}` |
| **Budget Allocation** | $`{{}}` per variant |

### Holdout and Controls
- **Audience Isolation:** `{{YES/NO}}` -- Method: `{{METHOD}}`
- **Time of Day Controls:** `{{YES/NO}}`
- **Geo Controls:** `{{YES/NO}}`
- **External Variables Noted:** `{{VARIABLES}}`

---

## Results Summary

### Primary Metric

| Variant | `{{PRIMARY_METRIC}}` | vs. Control | Confidence | Statistical Significance |
|---|---|---|---|---|
| **Control (A)** | `{{VALUE}}` | -- | -- | -- |
| **Variant B** | `{{VALUE}}` | `{{}}`% | `{{}}`% | `{{YES/NO}}` |
| **Variant C** | `{{VALUE}}` | `{{}}`% | `{{}}`% | `{{YES/NO}}` |

### Winner: `{{VARIANT_NAME}}`

### Secondary Metrics

| Metric | Control (A) | Variant B | B vs. A | Variant C | C vs. A |
|---|---|---|---|---|---|
| Spend | $`{{}}` | $`{{}}` | `{{}}`% | $`{{}}` | `{{}}`% |
| Impressions | `{{}}` | `{{}}` | `{{}}`% | `{{}}` | `{{}}`% |
| Clicks | `{{}}` | `{{}}` | `{{}}`% | `{{}}` | `{{}}`% |
| CTR | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% |
| CPC | $`{{}}` | $`{{}}` | `{{}}`% | $`{{}}` | `{{}}`% |
| Conversions | `{{}}` | `{{}}` | `{{}}`% | `{{}}` | `{{}}`% |
| CPA | $`{{}}` | $`{{}}` | `{{}}`% | $`{{}}` | `{{}}`% |
| ROAS | `{{}}`x | `{{}}`x | `{{}}`% | `{{}}`x | `{{}}`% |
| CVR | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% |
| Revenue | $`{{}}` | $`{{}}` | `{{}}`% | $`{{}}` | `{{}}`% |

---

## Statistical Analysis

### Sample Size Achieved

| Variant | Impressions | Clicks | Conversions | Sufficient Sample? |
|---|---|---|---|---|
| Control (A) | `{{}}` | `{{}}` | `{{}}` | `{{YES/NO}}` |
| Variant B | `{{}}` | `{{}}` | `{{}}` | `{{YES/NO}}` |
| Variant C | `{{}}` | `{{}}` | `{{}}` | `{{YES/NO}}` |

### Confidence Intervals

| Variant | Primary Metric | 95% CI Lower | 95% CI Upper |
|---|---|---|---|
| Control (A) | `{{}}` | `{{}}` | `{{}}` |
| Variant B | `{{}}` | `{{}}` | `{{}}` |
| Variant C | `{{}}` | `{{}}` | `{{}}` |

### Statistical Test Used
- **Test Type:** `{{Z-TEST / T-TEST / CHI-SQUARED / BAYESIAN}}` |
- **p-value:** `{{}}`
- **Confidence Level:** `{{}}`%
- **Power:** `{{}}`%

### Validity Check

| Check | Status | Notes |
|---|---|---|
| Sample size met | `{{PASS/FAIL}}` | `{{}}` |
| Even traffic split | `{{PASS/FAIL}}` | `{{}}` |
| No external confounders | `{{PASS/FAIL}}` | `{{}}` |
| Consistent throughout test | `{{PASS/FAIL}}` | `{{}}` |
| Novelty effect controlled | `{{PASS/FAIL}}` | `{{}}` |

---

## Daily Performance Trend

| Date | Control Conv. | Control CPA | Variant B Conv. | Variant B CPA | Variant C Conv. | Variant C CPA |
|---|---|---|---|---|---|---|
| `{{DAY_1}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` |
| `{{DAY_2}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` |
| `{{DAY_N}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` |

---

## Segment Analysis

### Results by Audience Segment

| Segment | Control CPA | Variant B CPA | Lift | Significant? |
|---|---|---|---|---|
| `{{SEGMENT_1}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{YES/NO}}` |
| `{{SEGMENT_2}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{YES/NO}}` |

### Results by Placement (if applicable)

| Placement | Control CTR | Variant B CTR | Lift | Significant? |
|---|---|---|---|---|
| Feed | `{{}}`% | `{{}}`% | `{{}}`% | `{{YES/NO}}` |
| Stories | `{{}}`% | `{{}}`% | `{{}}`% | `{{YES/NO}}` |
| Reels | `{{}}`% | `{{}}`% | `{{}}`% | `{{YES/NO}}` |

---

## Financial Impact Projection

| Scenario | Monthly Conversions | Monthly CPA | Monthly Spend | Monthly Revenue | Monthly ROAS |
|---|---|---|---|---|---|
| **Current (Control)** | `{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`x |
| **If Winner Deployed** | `{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`x |
| **Projected Lift** | +`{{}}` | -$`{{}}` | -- | +$`{{}}` | +`{{}}`x |
| **Annual Impact** | +`{{}}` | -- | -- | +$`{{}}` | -- |

---

## Key Learnings

1. `{{LEARNING_1}}`
2. `{{LEARNING_2}}`
3. `{{LEARNING_3}}`

### What This Tells Us
- `{{INSIGHT_1}}`
- `{{INSIGHT_2}}`

### What This Does NOT Tell Us
- `{{LIMITATION_1}}`
- `{{LIMITATION_2}}`

---

## Decision and Recommendation

### Verdict: `{{IMPLEMENT WINNER / ITERATE FURTHER / INCONCLUSIVE / RETEST}}`

### Rationale
`{{RATIONALE}}`

### Implementation Plan

| Step | Action | Owner | Timeline |
|---|---|---|---|
| 1 | `{{}}` | `{{}}` | `{{}}` |
| 2 | `{{}}` | `{{}}` | `{{}}` |
| 3 | `{{}}` | `{{}}` | `{{}}` |

---

## Follow-Up Tests

| Test | Hypothesis | Building On | Priority |
|---|---|---|---|
| `{{}}` | `{{}}` | This experiment | `{{P1/P2/P3}}` |

---

## Next Steps

- [ ] `{{ACTION_1}}` -- Owner: `{{OWNER}}` -- Due: `{{DATE}}`
- [ ] `{{ACTION_2}}` -- Owner: `{{OWNER}}` -- Due: `{{DATE}}`
- [ ] `{{ACTION_3}}` -- Owner: `{{OWNER}}` -- Due: `{{DATE}}`

---

*Report generated at `{{TIMESTAMP}}`. Statistical calculations performed using `{{METHOD}}`. Confidence threshold: `{{}}`%.*
