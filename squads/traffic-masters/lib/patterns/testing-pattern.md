# Testing Pattern

## Purpose
Structured pattern for designing, executing, and analyzing A/B tests and experiments in paid traffic campaigns. Ensures statistically valid results and actionable learnings.

---

## Testing Hierarchy

Test the elements that have the biggest impact first:

```
1. OFFER (What you sell and how you package it)         -- Highest Impact
2. AUDIENCE (Who you target)                            -- High Impact
3. CREATIVE CONCEPT (Core message and angle)            -- High Impact
4. HOOK (Opening line, first 3 seconds)                 -- Medium-High Impact
5. FORMAT (Video vs. static vs. carousel)               -- Medium Impact
6. COPY (Body text, headline)                           -- Medium Impact
7. CTA (Call to action)                                 -- Medium-Low Impact
8. PLACEMENT (Feed vs. stories vs. reels)               -- Low-Medium Impact
9. BID STRATEGY (CBO vs. ABO, tCPA vs. max conversions) -- Low Impact
10. SCHEDULE (Day-parting, day of week)                  -- Low Impact
```

**Rule:** Always test highest-impact variables first. Do not test CTA color when you have not validated your offer.

---

## Test Design Protocol

### Step 1: Define the Hypothesis

```
HYPOTHESIS: If we {{CHANGE}}, then {{METRIC}} will {{IMPROVE/DECREASE}} by {{AMOUNT}},
because {{RATIONALE}}.

Example: If we change the hook from a question to a bold statistic,
then CTR will improve by 20%, because our audience responds to data-driven claims.
```

### Step 2: Choose Test Parameters

| Parameter | Value | Rationale |
|---|---|---|
| **Variable** | `{{SINGLE_VARIABLE}}` | Only one variable per test |
| **Control (A)** | `{{CURRENT_BEST}}` | Existing winner or baseline |
| **Variant (B)** | `{{NEW_APPROACH}}` | The change being tested |
| **Primary Metric** | `{{CPA / CTR / CVR / ROAS}}` | The metric that determines the winner |
| **Secondary Metrics** | `{{OTHER_METRICS}}` | Additional context metrics |
| **Traffic Split** | `{{50/50}}` | Equal split recommended |
| **Min. Sample Size** | `{{CALCULATED}}` | Based on MDE and confidence level |
| **Confidence Level** | `{{90% or 95%}}` | 90% for speed, 95% for certainty |
| **Min. Detectable Effect** | `{{10-20%}}` | Smallest meaningful difference |
| **Duration** | `{{7-14 days}}` | Minimum to capture full weekly cycle |
| **Budget per Variant** | $`{{}}` | Enough to reach sample size |

### Step 3: Calculate Required Sample Size

**For Conversion Rate Tests:**
```
Sample Size per Variant = (Z^2 x p x (1-p)) / MDE^2

Where:
  Z = 1.645 (90% confidence) or 1.96 (95% confidence)
  p = baseline conversion rate
  MDE = minimum detectable effect (as a proportion)
```

**Quick Reference Table (95% confidence):**

| Baseline CVR | MDE 10% | MDE 15% | MDE 20% | MDE 25% |
|---|---|---|---|---|
| 1% | 380,000 | 170,000 | 95,000 | 61,000 |
| 2% | 188,000 | 84,000 | 47,000 | 30,000 |
| 5% | 73,000 | 33,000 | 18,000 | 12,000 |
| 10% | 35,000 | 15,000 | 8,600 | 5,500 |
| 20% | 15,000 | 6,800 | 3,800 | 2,500 |

*Values represent total clicks/visitors needed per variant.*

---

## Test Execution

### Platform-Level A/B Testing

| Platform | Built-In Tool | How It Works |
|---|---|---|
| **Meta** | A/B Test (Experiments) | Creates holdout groups, measures lift |
| **Meta** | Dynamic Creative | Tests multiple elements simultaneously |
| **Google** | Campaign Experiments | Splits traffic between control and variant |
| **Google** | Ad Variations | Tests copy changes across campaigns |
| **TikTok** | Split Test | Splits audience into non-overlapping groups |

### Manual A/B Testing (Fallback)
If platform tools are not available:
1. Create identical ad sets targeting the same audience
2. Change only the variable being tested
3. Ensure no audience overlap (use different ad sets in same campaign)
4. Run simultaneously with equal budgets
5. Monitor for even delivery across variants

### Test Integrity Rules
- **One variable at a time:** Never test hook AND format simultaneously
- **Equal budgets:** Both variants must receive equal spend
- **Same audience:** Both variants must target identical audiences
- **Same timeframe:** Both variants must run simultaneously
- **No interference:** Do not make other changes to the campaign during the test
- **Full cycle:** Run for at least 7 days to capture day-of-week effects
- **No peeking:** Do not stop the test early based on initial results

---

## Test Evaluation

### Winner Declaration Criteria

| Criterion | Threshold |
|---|---|
| Statistical significance | 90%+ confidence (95% preferred) |
| Minimum conversions per variant | 20+ (50+ preferred) |
| Consistent performance | Winner leads for 5+ of 7 days |
| No external confounders | No major events during test period |

### Evaluation Checklist

- [ ] Sample size met for both variants
- [ ] Test ran for minimum 7 days
- [ ] Statistical significance calculated
- [ ] Results are consistent (not driven by a spike)
- [ ] Secondary metrics reviewed (no hidden trade-offs)
- [ ] External factors accounted for

### Possible Outcomes

| Outcome | Criteria | Action |
|---|---|---|
| **Clear Winner** | Significant result, 90%+ confidence | Implement winner, document learning |
| **Inconclusive** | No significant difference | Test had too small sample, or the variable does not matter. Retest with larger sample or move to next variable |
| **Unexpected Result** | Winner is surprising or counter-intuitive | Validate with a confirmation test before scaling |
| **Negative Result** | Variant performed worse | Document the learning, revert to control |

---

## Test Types

### Creative Tests

| Test | Control | Variant | Primary Metric |
|---|---|---|---|
| Hook test | Question hook | Bold statement hook | CTR |
| Angle test | Pain-point angle | Benefit-led angle | CPA |
| Format test | Static image | 30s video | CPA, ROAS |
| CTA test | "Shop Now" | "Get 20% Off" | CVR |
| Length test | 15s video | 60s video | CPA |
| UGC vs. Polished | Professional video | UGC testimonial | CPA |

### Audience Tests

| Test | Control | Variant | Primary Metric |
|---|---|---|---|
| LAL seed test | LAL 1% purchasers | LAL 1% leads | CPA |
| LAL size test | LAL 1% | LAL 3% | CPA at scale |
| Interest test | Interest A | Interest B | CPA |
| Broad vs. targeted | Interest stack | Broad (no targeting) | CPA |
| Retargeting window | 7-day visitors | 30-day visitors | CPA, ROAS |

### Structural Tests

| Test | Control | Variant | Primary Metric |
|---|---|---|---|
| Bid strategy | Cost cap | Lowest cost | CPA, volume |
| CBO vs. ABO | ABO (ad set budgets) | CBO (campaign budget) | CPA, distribution |
| Placement | Automatic | Manual (feed only) | CPA |
| Landing page | Long-form LP | Short-form LP | CVR |

---

## Testing Cadence

| Maturity Level | Tests per Month | Focus |
|---|---|---|
| **New Account** | 2-3 | Audience + Offer validation |
| **Growing Account** | 4-6 | Creative + Audience expansion |
| **Mature Account** | 6-10 | Iterative creative + Structural optimization |
| **Enterprise Account** | 10+ | Continuous multi-variable optimization |

---

## Test Documentation Template

```
TEST NAME: {{NAME}}
TEST ID: {{ID}}
DATE STARTED: {{START}}
DATE ENDED: {{END}}
PLATFORM: {{PLATFORM}}
CAMPAIGN: {{CAMPAIGN}}

HYPOTHESIS:
{{IF_THEN_BECAUSE}}

VARIABLE: {{VARIABLE}}
CONTROL: {{CONTROL_DESCRIPTION}}
VARIANT: {{VARIANT_DESCRIPTION}}

PRIMARY METRIC: {{METRIC}}
SECONDARY METRICS: {{METRICS}}

RESULTS:
  Control: {{METRIC}} = {{VALUE}} (n={{SAMPLE}})
  Variant: {{METRIC}} = {{VALUE}} (n={{SAMPLE}})
  Lift: {{PERCENT}}%
  Confidence: {{PERCENT}}%
  Significant: {{YES/NO}}

WINNER: {{CONTROL/VARIANT/INCONCLUSIVE}}

KEY LEARNING:
{{LEARNING}}

NEXT ACTION:
{{ACTION}}

FOLLOW-UP TEST:
{{NEXT_TEST_IDEA}}
```
