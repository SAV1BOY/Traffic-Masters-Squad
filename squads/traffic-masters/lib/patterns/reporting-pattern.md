# Reporting Pattern

## Purpose
Structured pattern for generating consistent, insightful paid traffic reports at all cadences (daily, weekly, monthly). Ensures reports drive decisions rather than just display data.

---

## Reporting Principles

1. **Lead with the answer, not the data.** Start with what happened and what it means.
2. **Compare to context.** Raw numbers are meaningless without benchmarks, targets, or trends.
3. **Separate signal from noise.** Not every fluctuation requires commentary.
4. **Include so-what and now-what.** Every insight should lead to a recommendation.
5. **Match depth to audience.** Executives need headlines. Analysts need details.

---

## Report Generation Workflow

```
1. GATHER DATA
    |
    v
2. VALIDATE & CLEAN
    |
    v
3. CALCULATE KPIs
    |
    v
4. COMPARE TO BENCHMARKS
    |
    v
5. IDENTIFY SIGNALS
    |
    v
6. ANALYZE ROOT CAUSES
    |
    v
7. FORMULATE RECOMMENDATIONS
    |
    v
8. ASSEMBLE REPORT
    |
    v
9. REVIEW & SEND
```

---

## Step 1: Gather Data

### Data Sources

| Source | Data Points | Cadence |
|---|---|---|
| Meta Ads Manager | Spend, impressions, clicks, conversions, creative metrics | Real-time |
| Google Ads | Spend, clicks, conversions, search terms, quality scores | Real-time |
| TikTok Ads Manager | Spend, impressions, video metrics, conversions | Real-time |
| Google Analytics 4 | Sessions, conversions, attribution, user behavior | Real-time |
| CRM / Backend | Revenue, orders, leads, LTV data | Varies |
| Spreadsheet / BI Tool | Calculated metrics, historical trends | Updated per cadence |

### Data Pull Timing
- **Daily reports:** Pull data after 11:00 AM in the account timezone (allows overnight attribution)
- **Weekly reports:** Pull Monday morning for the previous Mon-Sun period
- **Monthly reports:** Pull on the 2nd of the month (allows 1 day for delayed attribution)

---

## Step 2: Validate and Clean

### Validation Checklist

- [ ] Spend matches across platform and billing
- [ ] Conversion counts are plausible (no zero days that should have data)
- [ ] No duplicate data from multiple sources
- [ ] Date ranges are correct and consistent
- [ ] Currency is consistent across all sources
- [ ] Attribution window settings have not changed

### Common Data Issues

| Issue | Detection | Fix |
|---|---|---|
| Missing data | Zero values on days with active campaigns | Re-pull data, check API |
| Duplicate rows | Sum exceeds expected range | De-duplicate by campaign ID + date |
| Currency mismatch | ROAS looks abnormally high/low | Normalize to single currency |
| Attribution delay | Conversions lower than expected for recent days | Wait 24-48 hours for attribution |
| Reporting discrepancy | Platform and analytics numbers differ | Note discrepancy, use consistent source |

---

## Step 3: Calculate KPIs

Use the KPI Calculator component for all formulas. Key calculations:

### Primary KPIs (Always Include)

| KPI | Formula | Include in |
|---|---|---|
| Total Spend | Sum of all platform spend | All reports |
| Conversions | Sum of conversion events | All reports |
| CPA | Spend / Conversions | All reports |
| Revenue | Sum of attributed revenue | All reports |
| ROAS | Revenue / Spend | All reports |

### Secondary KPIs (Include by Cadence)

| KPI | Daily | Weekly | Monthly |
|---|---|---|---|
| CTR | Yes | Yes | Yes |
| CPC | Yes | Yes | Yes |
| CPM | Optional | Yes | Yes |
| CVR | Optional | Yes | Yes |
| AOV | No | Yes | Yes |
| LTV / CAC | No | No | Yes |
| Frequency | Optional | Yes | Yes |

---

## Step 4: Compare to Benchmarks

Every metric should be compared to at least two reference points:

| Comparison | Purpose |
|---|---|
| **vs. Target** | Are we hitting goals? |
| **vs. Previous Period** | Is performance improving or declining? |
| **vs. Same Period Last Year** | Are we ahead of historical performance? |
| **vs. Moving Average (7d, 30d)** | Is this an anomaly or a trend? |
| **vs. Industry Benchmark** | How do we compare to peers? |

### Significance Thresholds

| Change | Interpretation | Report Action |
|---|---|---|
| < 5% | Normal fluctuation | Note but do not highlight |
| 5-15% | Noteworthy change | Mention in analysis section |
| 15-30% | Significant change | Highlight with analysis and recommendation |
| > 30% | Major change | Lead with this, include root cause and action plan |

---

## Step 5: Identify Signals

### What Counts as a Signal

| Type | Example | Action |
|---|---|---|
| **Trend** | CPA has risen 5 consecutive days | Investigate and act |
| **Breakout** | One creative has 3x the CTR of others | Scale this creative |
| **Breakdown** | Conversion rate dropped 40% overnight | Emergency diagnostic |
| **Milestone** | Hit 100% of monthly target with 10 days remaining | Communicate win, plan next month |
| **Anomaly** | Unusually high spend on a single day | Investigate cause |

### What is NOT a Signal
- Single-day fluctuations of < 15%
- Normal day-of-week patterns (lower weekends for B2B, etc.)
- Metrics with insufficient data (< 100 impressions, < 10 clicks)

---

## Step 6: Analyze Root Causes

For each significant signal, answer:
1. **What** happened? (Describe the change in specific terms)
2. **When** did it start? (Identify the timing)
3. **Where** in the funnel? (Which stage is affected)
4. **Why** did it happen? (Root cause analysis)
5. **So what?** (Business impact)

---

## Step 7: Formulate Recommendations

### Recommendation Framework

```
RECOMMENDATION: {{SPECIFIC_ACTION}}
RATIONALE: {{WHY_THIS_ACTION}} based on {{DATA_POINT}}
EXPECTED IMPACT: {{QUANTIFIED_OUTCOME}}
EFFORT: {{LOW / MEDIUM / HIGH}}
PRIORITY: {{P1 / P2 / P3}}
TIMELINE: {{WHEN_TO_EXECUTE}}
```

### Recommendation Rules
- Every report should have 2-5 recommendations
- Each recommendation should be specific and actionable (not "improve creative")
- Quantify expected impact where possible
- Prioritize recommendations (P1 = do this week, P2 = do this month, P3 = consider)
- Include effort level so stakeholders can plan resources

---

## Step 8: Assemble the Report

### Report Structure (All Cadences)

```
1. METADATA (date, preparer, client, period)
2. EXECUTIVE SUMMARY (2-3 sentences: what happened, why, what next)
3. KPI SCORECARD (table with key metrics vs. targets and trends)
4. HIGHLIGHTS AND LOWLIGHTS (wins and challenges)
5. DETAILED BREAKDOWN (by channel, campaign, audience, creative)
6. ANALYSIS (root causes, insights, external factors)
7. RECOMMENDATIONS (prioritized action items)
8. NEXT STEPS (specific tasks with owners and deadlines)
```

### Depth by Cadence

| Section | Daily | Weekly | Monthly |
|---|---|---|---|
| Executive Summary | 1-2 sentences | 2-3 sentences | 3-5 sentences |
| KPI Scorecard | 5-7 metrics | 8-12 metrics | Full suite |
| Breakdown | Campaign-level | Campaign + ad set | Full drill-down |
| Creative Analysis | Top/bottom only | Performance table | Full creative report |
| Recommendations | 1-2 quick actions | 3-5 recommendations | 5-8 strategic recommendations |
| Next Steps | Today's priorities | This week's tasks | This month's roadmap |

---

## Step 9: Review and Send

### Pre-Send Checklist

- [ ] Numbers are accurate (spot-check 2-3 key metrics against source)
- [ ] All comparisons use the correct periods
- [ ] Commentary matches the data (no contradictions)
- [ ] Recommendations are specific and actionable
- [ ] Report uses proper naming conventions
- [ ] Formatting is clean and consistent
- [ ] Sent on schedule

### Distribution Schedule

| Report | Due | Recipients | Format |
|---|---|---|---|
| Daily | By 11:00 AM | Internal team | Slack/chat message or brief doc |
| Weekly | Monday by noon | Team + client (if applicable) | Document or slide deck |
| Monthly | 3rd business day | Client + leadership | Formal presentation or document |
| Quarterly | 5th business day | Executive stakeholders | Presentation with strategic review |
