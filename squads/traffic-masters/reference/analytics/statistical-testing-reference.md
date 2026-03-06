# Statistical Testing Reference for A/B Tests

> Practical statistical reference for paid traffic professionals designing and analyzing A/B tests on ads, landing pages, and funnels.

---

## 1. Core Concepts

### Hypothesis Testing Framework

Every A/B test has:
- **Null hypothesis (H0)**: There is no difference between control and variant
- **Alternative hypothesis (H1)**: There IS a difference
- **Goal**: Determine if observed differences are real or due to random chance

### Key Terms

| Term | Definition | Typical Value |
|------|-----------|---------------|
| **Significance level (alpha)** | Probability of declaring a winner when there isn't one (false positive) | 0.05 (5%) |
| **p-value** | Probability of seeing results this extreme if H0 is true | Declare winner if p < alpha |
| **Confidence level** | 1 - alpha; probability the result is not a false positive | 95% (standard) |
| **Statistical power** | Probability of detecting a real difference when one exists | 80% (standard minimum) |
| **Beta** | Probability of missing a real difference (false negative) | 0.20 (20%) |
| **MDE** | Minimum Detectable Effect; smallest difference you want to reliably detect | Depends on business impact |
| **Confidence interval** | Range of values likely to contain the true effect | Narrower = more precise |

---

## 2. Sample Size Calculation

### Formula (for conversion rate tests)

```
n = (Z_alpha/2 + Z_beta)^2 * (p1(1-p1) + p2(1-p2)) / (p2 - p1)^2
```

Where:
- `n` = sample size per variant
- `Z_alpha/2` = 1.96 for 95% confidence
- `Z_beta` = 0.84 for 80% power
- `p1` = control conversion rate
- `p2` = expected variant conversion rate (p1 + MDE)

### Sample Size Quick Reference Table

**95% confidence, 80% power, two-tailed test**

| Baseline CR | MDE (Relative) | MDE (Absolute) | Sample per Variant |
|-------------|----------------|-----------------|-------------------|
| 1% | 10% | 0.1% | 1,568,000 |
| 1% | 20% | 0.2% | 392,000 |
| 1% | 50% | 0.5% | 62,700 |
| 2% | 10% | 0.2% | 768,000 |
| 2% | 20% | 0.4% | 192,000 |
| 2% | 50% | 1.0% | 30,700 |
| 5% | 10% | 0.5% | 292,000 |
| 5% | 20% | 1.0% | 73,000 |
| 5% | 50% | 2.5% | 11,700 |
| 10% | 10% | 1.0% | 140,000 |
| 10% | 20% | 2.0% | 35,000 |
| 10% | 50% | 5.0% | 5,600 |
| 20% | 10% | 2.0% | 62,000 |
| 20% | 20% | 4.0% | 15,500 |
| 20% | 50% | 10.0% | 2,500 |

**Takeaway**: Low conversion rates and small MDE = massive sample sizes required. This is why landing page tests (higher CR) are easier to run than purchase tests (lower CR).

### Practical MDE Guidelines

| Test Type | Realistic MDE | Notes |
|-----------|--------------|-------|
| Ad creative (CTR) | 10-20% relative | High volume makes this feasible |
| Landing page (CR) | 10-30% relative | Moderate volume; test big changes |
| Pricing page | 15-40% relative | Usually lower traffic; test bold changes |
| Checkout flow | 5-15% relative | High impact; worth the patience |
| Email subject line | 10-25% relative | High volume; quick tests |

---

## 3. Test Duration Guidelines

### Minimum Duration Rules

1. **At least 1 full business cycle** (usually 7 days) to capture day-of-week effects
2. **At least 2 business cycles** (14 days) recommended for purchase tests
3. **Never call a test early** based on interim results (peeking problem)
4. **Cap at 4-6 weeks** maximum; beyond this, external factors contaminate results

### Duration Estimate Formula

```
Duration (days) = Required Sample Size / Daily Traffic per Variant
```

**Example**:
- Baseline CR: 3%, MDE: 20% relative (0.6% absolute)
- Required sample: ~73,000 per variant
- Daily traffic: 5,000 visitors
- Traffic per variant (50/50 split): 2,500/day
- Duration: 73,000 / 2,500 = 29 days

### When You Don't Have Enough Traffic

| Option | Trade-off |
|--------|-----------|
| Accept larger MDE (20-50%) | Only detect big wins; miss small improvements |
| Reduce confidence to 90% | Slightly higher false positive risk |
| Test fewer variants | More traffic per variant |
| Test higher-funnel metrics (CTR vs. purchase) | More events = faster results |
| Use sequential testing methods | Monitor results without inflating error rate |

---

## 4. Types of Statistical Tests

### Z-Test for Proportions (Conversion Rates)

**When to use**: Comparing conversion rates between two groups.

```
z = (p_variant - p_control) / sqrt(p_pooled * (1-p_pooled) * (1/n_control + 1/n_variant))

p_pooled = (conversions_control + conversions_variant) / (n_control + n_variant)
```

**Example**:
- Control: 500 conversions / 10,000 visitors = 5.0%
- Variant: 560 conversions / 10,000 visitors = 5.6%
- p_pooled = 1060/20000 = 5.3%
- z = (0.056 - 0.050) / sqrt(0.053 * 0.947 * (1/10000 + 1/10000))
- z = 0.006 / 0.00317 = 1.89
- p-value = 0.059 (two-tailed)
- Result: NOT statistically significant at 95% confidence (p > 0.05)

### T-Test for Means (Revenue per User, AOV)

**When to use**: Comparing average values (revenue, order value, LTV) between groups.

**Important**: Revenue data is often highly skewed (many $0, few large orders). Consider:
- Log-transforming data
- Using Mann-Whitney U test (non-parametric)
- Bootstrapping confidence intervals

### Chi-Squared Test

**When to use**: Comparing more than 2 variants simultaneously (A/B/C/D tests).

**Caution**: If the overall chi-squared test is significant, run pairwise comparisons with Bonferroni correction to identify which variants differ.

---

## 5. Common Pitfalls

### The Peeking Problem

Checking results repeatedly and stopping when you see significance inflates your false positive rate dramatically:

| Times You Check | Actual False Positive Rate (at nominal 5%) |
|----------------|---------------------------------------------|
| 1 (end of test only) | 5% |
| 2 | 8% |
| 5 | 14% |
| 10 | 19% |
| 20 | 25% |
| Daily for 30 days | ~30% |

**Solution**: Use sequential testing methods (see Section 6) or commit to checking only once at the pre-determined end date.

### Simpson's Paradox

A trend that appears in different groups of data can reverse when groups are combined.

**Example**: Variant B wins on desktop (60% of traffic) and loses on mobile (40% of traffic), but when combined, it appears B loses overall due to different traffic volumes and conversion rates.

**Solution**: Segment results by device, traffic source, and geo to verify consistency.

### Novelty Effect

New designs or features may show initial improvement simply because they're different. This effect fades over time.

**Solution**: Run tests for at least 2 weeks. For major design changes, monitor the winning variant for 4+ weeks after implementation.

### Selection Bias

If randomization is not truly random (e.g., splitting by time period, geography, or device), your test is invalid.

**Solution**: Use proper randomization at the user level. Use platform-native split testing features or tools like Google Optimize (sunset), VWO, or Optimizely.

---

## 6. Sequential Testing (Monitoring Without Peeking Risk)

### What It Is

Sequential testing adjusts the significance threshold based on how many times you check, maintaining the overall false positive rate.

### Methods

**Alpha Spending Functions** (O'Brien-Fleming, Pocock):
- Pre-define a checking schedule (e.g., check every 1,000 visitors)
- Each check uses a stricter significance threshold
- O'Brien-Fleming: Very strict early, more lenient later (recommended)
- Pocock: Equal threshold at each check

**O'Brien-Fleming Example (4 scheduled checks)**:

| Check | Cumulative Sample % | Alpha Spent | Required p-value |
|-------|---------------------|-------------|-----------------|
| 1 | 25% | 0.0001 | < 0.0001 |
| 2 | 50% | 0.004 | < 0.004 |
| 3 | 75% | 0.019 | < 0.019 |
| 4 | 100% | 0.043 | < 0.043 |

**Bayesian A/B Testing**:
- Does not use p-values; uses probability of being best
- Can be checked at any time without inflation
- Reports "Probability that B beats A" (e.g., 94.2%)
- More intuitive for non-statisticians
- Tools: VWO, Dynamic Yield, custom implementations

---

## 7. Multi-Armed Bandit vs. A/B Tests

| Feature | A/B Test | Multi-Armed Bandit |
|---------|----------|-------------------|
| Traffic split | Fixed (e.g., 50/50) | Dynamic (shifts to winner) |
| Goal | Statistical certainty | Maximize conversions during test |
| When to use | Need to know the true winner | Ongoing optimization, always-on |
| Duration | Fixed endpoint | Continuous |
| Regret | Higher (equal traffic to loser) | Lower (less traffic to loser) |
| Statistical rigor | Higher | Lower (harder to get clean results) |

**Use A/B tests when**: You need to definitively know if a change works (major decisions, website redesigns).

**Use bandits when**: You're continuously testing ad creatives and want to maximize conversions (Meta and Google already do this within campaigns via ad rotation).

---

## 8. Effect Size & Practical Significance

### Statistical vs. Practical Significance

A result can be statistically significant but practically meaningless.

**Example**: A/B test with 1M visitors per variant shows a 0.01% improvement (from 5.00% to 5.01%). This is statistically significant (huge sample) but practically irrelevant.

### Minimum Meaningful Effect

Before running a test, define: "What's the smallest improvement worth implementing?"

Consider:
- Implementation cost of the change
- Revenue impact of the improvement
- Opportunity cost of the test duration

**Rule of thumb**: If the expected revenue impact doesn't exceed the cost of implementation + testing within 3-6 months, it's not worth testing.

---

## 9. Reporting A/B Test Results

### What to Include in Reports

| Metric | Example |
|--------|---------|
| Sample size per variant | Control: 25,000, Variant: 25,000 |
| Conversion rate per variant | Control: 4.2%, Variant: 5.1% |
| Relative lift | +21.4% |
| Absolute lift | +0.9 percentage points |
| Confidence level | 97.3% |
| p-value | 0.027 |
| Confidence interval (relative) | [+3.1%, +41.2%] |
| Test duration | 21 days |
| Estimated revenue impact | +$12,500/month |

### Interpreting Confidence Intervals

"We are 95% confident that the true effect lies between +3.1% and +41.2% relative improvement."

**Wide intervals** = high uncertainty. Even if significant, the actual effect could be much smaller than the point estimate.

**Narrow intervals** = high precision. You can trust the point estimate more closely.

---

## 10. Quick Reference: Test Calculators & Tools

| Tool | Purpose | URL/Access |
|------|---------|-----------|
| Evan Miller's Calculator | Sample size + significance | `evanmiller.org/ab-testing` |
| Optimizely Stats Engine | Sequential testing calculator | `optimizely.com` |
| VWO | Bayesian A/B testing platform | `vwo.com` |
| ABTestGuide Calculator | Simple significance calculator | `abtestguide.com/calc` |
| Google Sheets (Z-test) | `=2*(1-NORM.S.DIST(ABS(z),TRUE))` | Manual calculation |
| Python (scipy.stats) | `proportions_ztest()` from statsmodels | Code-based analysis |
| R | `prop.test(c(x1,x2), c(n1,n2))` | Code-based analysis |

---

## 11. Ad Platform A/B Testing Features

| Platform | Feature | Notes |
|----------|---------|-------|
| Meta | A/B Test (Experiments) | Split at ad set or campaign level; controls for audience overlap |
| Google Ads | Campaign Experiments | Split traffic %; full statistical reporting |
| TikTok | Split Test | Budget split between test cells |
| LinkedIn | A/B testing | Limited; creative rotation within ad groups |
| GA4 | n/a (no built-in testing) | Use third-party tools; GA4 provides measurement |

---

*Last updated: March 2026. Statistical rigor is the foundation of data-driven advertising decisions. When in doubt, run the test longer rather than calling it early.*
