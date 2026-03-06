# Metrics Language Guide

## Purpose
Standard language patterns for discussing, presenting, and interpreting advertising metrics. Ensures consistency in how the team describes performance data.

---

## Describing Metric Changes

### Direction Language

| Situation | Preferred Phrasing | Avoid |
|---|---|---|
| Metric increased | "increased," "rose," "climbed," "grew" | "spiked" (unless > 50%), "exploded" |
| Metric decreased | "decreased," "declined," "fell," "dropped" | "crashed" (unless > 50%), "tanked" |
| Metric stable | "remained stable," "held steady," "flat" | "didn't change" |
| Metric improved | "improved" (use only when direction is inherently good) | "got better" |
| Metric worsened | "deteriorated," "worsened," "degraded" | "got worse," "went bad" |

### Magnitude Language

| Change Magnitude | Descriptor | Usage |
|---|---|---|
| < 5% | "marginal," "slight," "negligible" | "CPA saw a marginal increase of 3%." |
| 5-15% | "moderate," "notable," "meaningful" | "CTR showed a moderate decline of 12%." |
| 15-30% | "significant," "substantial" | "Conversions grew significantly, up 22%." |
| 30-50% | "sharp," "pronounced," "major" | "CPM experienced a sharp increase of 35%." |
| > 50% | "dramatic," "steep" | "ROAS declined dramatically, falling 55%." |

### Timeframe Language

| Period | Standard Phrasing |
|---|---|
| Day-over-day | "compared to yesterday," "day-over-day (DoD)" |
| Week-over-week | "compared to last week," "week-over-week (WoW)" |
| Month-over-month | "compared to last month," "month-over-month (MoM)" |
| Year-over-year | "compared to the same period last year," "year-over-year (YoY)" |
| vs. target | "relative to target," "against the [CPA/ROAS] target of [X]" |
| vs. benchmark | "relative to benchmark," "compared to the account/industry benchmark" |

---

## Describing Metric Status

### Relative to Target

| Status | Language |
|---|---|
| Meeting target | "CPA is at target ($50)." "ROAS is meeting the 4.0x target." |
| Above target (good) | "ROAS is exceeding target at 4.8x (vs. 4.0x target)." |
| Above target (bad) | "CPA is 20% above target at $60 (vs. $50 target)." |
| Below target (good) | "CPA is 15% below target at $42.50 (vs. $50 target)." |
| Below target (bad) | "ROAS is below target at 3.2x (vs. 4.0x target)." |

### Traffic Light Language

| Color | When | Language |
|---|---|---|
| **Green** | Metric within target range | "On track," "within target," "healthy" |
| **Yellow** | Metric approaching threshold | "Approaching threshold," "trending toward concern," "monitoring" |
| **Red** | Metric outside acceptable range | "Outside target," "requires action," "below acceptable threshold" |

---

## Describing Trends

### Trend Language

| Trend | Phrasing |
|---|---|
| Consistently improving | "CPA has declined steadily over the past 4 weeks." |
| Consistently worsening | "CTR has been declining week-over-week for 3 consecutive weeks." |
| Volatile | "CPA has been volatile, ranging from $35 to $65 over the past 2 weeks." |
| Stabilizing | "After the initial volatility, CPA has stabilized around $48." |
| Accelerating | "The rate of improvement is accelerating -- CPA fell 5% in week 1 and 12% in week 2." |
| Plateauing | "Performance has plateaued, with CPA flat at $50 for the past 10 days." |

---

## Presenting Comparisons

### Preferred Comparison Format
```
"[METRIC] is [VALUE], [DIRECTION] [AMOUNT/PERCENT] [COMPARISON]."
```

**Examples:**
- "CPA is $52, up 8% week-over-week."
- "ROAS is 4.3x, exceeding our 3.5x target by 23%."
- "CTR is 1.1%, in line with the 30-day average of 1.2%."

### Percentage Points vs. Percentage Change

| Metric Type | Use |
|---|---|
| Rates (CTR, CVR) | Percentage points (pp): "CTR increased by 0.3 percentage points, from 1.0% to 1.3%." |
| Absolute values (CPA, spend) | Percentage change: "CPA decreased 15%, from $50 to $42.50." |

**Why this matters:** "CTR increased 30%" could mean 1.0% to 1.3% (30% relative increase) or 1.0% to 31.0% (30 percentage points). Use pp for rates to avoid ambiguity.

---

## Metric Abbreviation Standards

Always define abbreviations on first use in any document. After definition, abbreviations are acceptable.

| Metric | Abbreviation | First Use Example |
|---|---|---|
| Cost Per Acquisition | CPA | "Cost per acquisition (CPA) was $50." |
| Return on Ad Spend | ROAS | "Return on ad spend (ROAS) reached 4.2x." |
| Click-Through Rate | CTR | "Click-through rate (CTR) averaged 1.2%." |
| Cost Per Click | CPC | "Cost per click (CPC) was $1.80." |
| Cost Per Mille | CPM | "Cost per 1,000 impressions (CPM) was $12." |
| Conversion Rate | CVR | "Conversion rate (CVR) was 3.5%." |
| Average Order Value | AOV | "Average order value (AOV) was $120." |
| Lifetime Value | LTV | "Customer lifetime value (LTV) is estimated at $850." |

---

## Numbers Formatting

| Element | Format | Example |
|---|---|---|
| Currency | Dollar sign, two decimals for < $100; no decimals for larger | $42.50, $1,200 |
| Percentages | One decimal place | 1.2%, 45.3% |
| Large numbers | Comma separator or K/M notation | 125,000 or 125K |
| Multipliers (ROAS) | One decimal with "x" | 4.2x |
| Changes | Include + or - sign | +15%, -$8.00 |
