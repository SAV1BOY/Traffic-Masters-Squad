# Statistical Significance Calculator Guide

## Purpose
Reference guide for calculating and interpreting statistical significance in A/B tests and experiments for paid traffic campaigns.

---

## When to Use Statistical Significance

- Comparing two or more ad creative variants
- Evaluating audience segment performance differences
- Testing landing page variations
- Comparing bid strategy performance
- Any A/B or multivariate test decision

---

## Key Concepts

### Confidence Level
The probability that the observed difference is real (not due to chance).
- **90%** -- Acceptable for fast-moving tests with low-risk decisions
- **95%** -- Standard for most business decisions
- **99%** -- Required for high-stakes or irreversible changes

### p-value
The probability that the observed result occurred by chance.
- p < 0.10 -- 90% confidence
- p < 0.05 -- 95% confidence
- p < 0.01 -- 99% confidence

### Minimum Detectable Effect (MDE)
The smallest difference between variants that you want to be able to detect.
- Smaller MDE = larger sample size needed
- Typical MDE for ad tests: 10-20%

### Statistical Power
The probability of detecting a real difference when one exists.
- Standard: 80% power
- Higher power = larger sample size needed

---

## Sample Size Calculator

### For Conversion Rate Tests

```
n = (Z_alpha/2 + Z_beta)^2 x (p1(1-p1) + p2(1-p2)) / (p1 - p2)^2
```

**Simplified version (equal groups, 95% confidence, 80% power):**
```
n per group = 16 x p x (1-p) / MDE^2
```

Where:
- `p` = baseline conversion rate (as decimal)
- `MDE` = minimum detectable effect (as decimal, e.g., 0.02 for 2 percentage points)

### Quick Reference Table

**95% confidence, 80% power, two-sided test:**

| Baseline CVR | MDE (Relative) | MDE (Absolute) | Sample Size Per Variant |
|---|---|---|---|
| 1.0% | 20% | 0.2pp | 195,000 |
| 1.0% | 30% | 0.3pp | 87,000 |
| 1.0% | 50% | 0.5pp | 31,500 |
| 2.0% | 20% | 0.4pp | 96,000 |
| 2.0% | 30% | 0.6pp | 43,000 |
| 2.0% | 50% | 1.0pp | 15,500 |
| 5.0% | 10% | 0.5pp | 146,000 |
| 5.0% | 20% | 1.0pp | 37,000 |
| 5.0% | 30% | 1.5pp | 16,500 |
| 10.0% | 10% | 1.0pp | 69,000 |
| 10.0% | 20% | 2.0pp | 17,500 |
| 10.0% | 30% | 3.0pp | 7,800 |
| 20.0% | 10% | 2.0pp | 31,000 |
| 20.0% | 20% | 4.0pp | 7,800 |
| 20.0% | 30% | 6.0pp | 3,500 |

*pp = percentage points. Sample size = clicks or visitors per variant.*

---

## Performing a Z-Test (Two Proportions)

### Step-by-Step

**Given:**
- Control: n_A clicks, c_A conversions
- Variant: n_B clicks, c_B conversions

**Step 1: Calculate conversion rates**
```
p_A = c_A / n_A
p_B = c_B / n_B
```

**Step 2: Calculate pooled proportion**
```
p_pool = (c_A + c_B) / (n_A + n_B)
```

**Step 3: Calculate standard error**
```
SE = sqrt(p_pool x (1 - p_pool) x (1/n_A + 1/n_B))
```

**Step 4: Calculate Z-score**
```
Z = (p_B - p_A) / SE
```

**Step 5: Interpret**

| Z-Score | Confidence Level | Significant? |
|---|---|---|
| < 1.28 | < 80% | No |
| 1.28 - 1.645 | 80-90% | Marginal |
| 1.645 - 1.96 | 90-95% | Yes (at 90%) |
| 1.96 - 2.576 | 95-99% | Yes (at 95%) |
| > 2.576 | > 99% | Yes (at 99%) |

### Worked Example

```
Control:  5,000 clicks, 100 conversions (2.00% CVR)
Variant:  5,000 clicks, 130 conversions (2.60% CVR)

p_A = 100 / 5,000 = 0.0200
p_B = 130 / 5,000 = 0.0260
p_pool = (100 + 130) / (5,000 + 5,000) = 0.0230

SE = sqrt(0.0230 x (1 - 0.0230) x (1/5,000 + 1/5,000))
SE = sqrt(0.0230 x 0.977 x 0.0004)
SE = sqrt(0.000008988)
SE = 0.002998

Z = (0.0260 - 0.0200) / 0.002998
Z = 0.006 / 0.002998
Z = 2.00

Result: Z = 2.00 > 1.96 -- Statistically significant at 95% confidence.
The variant (2.60% CVR) beats the control (2.00% CVR).
Lift = (2.60 - 2.00) / 2.00 x 100 = 30% relative lift.
```

---

## For CPA / ROAS Comparisons

CPA and ROAS are continuous metrics (not proportions), so use a different approach.

### Method: Bootstrap or T-Test

For CPA comparison, calculate per-day CPA for each variant and use a paired t-test:

```
Given daily CPA values for Control: [c1, c2, ..., cn]
Given daily CPA values for Variant: [v1, v2, ..., vn]

Calculate difference: d_i = c_i - v_i for each day
Mean difference: d_bar = mean(d)
Std of difference: s_d = std(d)
t = d_bar / (s_d / sqrt(n))
```

Compare t to t-distribution with n-1 degrees of freedom.

### Practical Shortcut

For most ad platform tests, use the conversion count method:
1. Count conversions for each variant
2. Treat as a proportion test (conversions / clicks)
3. If the conversion rates are significantly different, the CPAs are significantly different (assuming equal spend)

---

## Common Pitfalls

### 1. Peeking at Results Early
**Problem:** Checking results daily and stopping when you see a winner inflates false positive rate.
**Solution:** Pre-determine test duration based on sample size calculation. Do not stop early.

### 2. Insufficient Sample Size
**Problem:** Declaring a winner with 10 conversions per variant.
**Solution:** Use the sample size table above. For CPA-based decisions, aim for 50+ conversions per variant.

### 3. Simpson's Paradox
**Problem:** Overall variant B wins, but control A wins in every individual segment.
**Solution:** Check segment-level results when overall results seem surprising.

### 4. Multiple Comparisons
**Problem:** Testing 5 variants and declaring the best one the winner increases false positive rate.
**Solution:** Apply Bonferroni correction: divide significance threshold by number of comparisons (0.05 / 5 = 0.01 per comparison).

### 5. Novelty Effect
**Problem:** New variant performs well initially because it is novel, then regresses.
**Solution:** Run tests for 2+ weeks. Discount the first 2-3 days of data.

### 6. Day-of-Week Effects
**Problem:** Test starts on Monday for Control and Wednesday for Variant -- different day mix.
**Solution:** Always run both variants simultaneously for complete weekly cycles.

---

## Decision Framework

```
IF confidence >= 95% AND sample size met AND consistent for 7+ days:
  -> DECLARE WINNER, implement

IF confidence 90-95% AND sample size met:
  -> LIKELY WINNER, implement with monitoring

IF confidence 80-90%:
  -> LEANING toward a winner, consider extending test duration

IF confidence < 80%:
  -> INCONCLUSIVE, either extend test or accept no meaningful difference

IF test ran full duration with sufficient sample and no significant difference:
  -> NO DIFFERENCE between variants
  -> Both are equivalent -- keep the simpler/cheaper option
  -> Move on to testing a different variable
```

---

## Online Calculators (for quick reference)

- **AB Test Calculator:** https://abtestguide.com/calc/
- **Evan Miller Calculator:** https://www.evanmiller.org/ab-testing/
- **Optimizely Sample Size Calculator:** https://www.optimizely.com/sample-size-calculator/

These tools automate the calculations above and are useful for quick checks.
