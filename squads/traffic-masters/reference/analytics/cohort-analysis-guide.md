# Cohort Analysis Guide for LTV and Retention

> Practical guide for paid traffic professionals using cohort analysis to measure customer lifetime value, retention, and payback periods.

---

## 1. What Is Cohort Analysis?

A cohort is a group of users who share a common characteristic within a defined time period. Cohort analysis tracks how these groups behave over time.

### Common Cohort Types for Advertising

| Cohort Type | Definition | Use Case |
|-------------|-----------|----------|
| **Acquisition date** | Users acquired in the same week/month | Track LTV by acquisition period |
| **Acquisition source** | Users from the same ad platform/campaign | Compare channel quality |
| **First purchase value** | Users with similar first order value | Predict LTV from first purchase |
| **Product category** | Users who first bought a specific category | Identify high-LTV entry products |
| **Geographic** | Users from the same region | Regional performance analysis |
| **Campaign/creative** | Users acquired by the same campaign | Measure creative quality beyond initial ROAS |

---

## 2. Retention Cohort Tables

### Building a Retention Cohort Table

**Example: Monthly acquisition cohorts, tracking repeat purchases**

| Cohort (Acquisition Month) | Month 0 | Month 1 | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 |
|---------------------------|---------|---------|---------|---------|---------|---------|---------|
| Jan 2026 (n=1,000) | 100% | 22% | 15% | 12% | 10% | 9% | 8% |
| Feb 2026 (n=1,200) | 100% | 25% | 17% | 13% | 11% | 10% | - |
| Mar 2026 (n=950) | 100% | 20% | 14% | 11% | 10% | - | - |
| Apr 2026 (n=1,100) | 100% | 28% | 19% | 14% | - | - | - |

**Reading this table**: Of the 1,000 customers acquired in January, 22% made a purchase again in Month 1, 15% in Month 2, etc.

### Interpreting Trends

- **Improving cohorts** (Apr > Mar > Feb > Jan retention): Your product/experience is improving, or ad targeting is getting better
- **Declining cohorts**: Product issues, or you're acquiring lower-quality customers as you scale
- **Flat cohorts**: Stable business; growth comes from new customer acquisition

---

## 3. Revenue Cohort Tables (LTV)

### Cumulative Revenue per Customer

| Cohort | Month 0 | Month 1 | Month 2 | Month 3 | Month 6 | Month 12 |
|--------|---------|---------|---------|---------|---------|----------|
| Jan 2026 | $52.00 | $63.40 | $71.10 | $76.80 | $89.50 | $108.20 |
| Feb 2026 | $48.00 | $60.00 | $68.40 | $74.50 | $88.20 | - |
| Mar 2026 | $55.00 | $66.50 | $74.00 | $80.20 | - | - |

**Reading this table**: Customers acquired in January generated $52 in their first month, $63.40 cumulatively by end of Month 1, and $108.20 cumulatively by Month 12.

### LTV/CAC Ratio by Cohort

| Cohort | CAC | LTV (6-month) | LTV:CAC | Payback Period |
|--------|-----|---------------|---------|---------------|
| Meta - Broad | $35 | $89.50 | 2.56x | 1.8 months |
| Meta - Lookalike | $28 | $95.20 | 3.40x | 1.2 months |
| Google - Brand | $12 | $102.00 | 8.50x | 0.4 months |
| Google - Non-Brand | $45 | $78.00 | 1.73x | 3.2 months |
| TikTok - In-Feed | $22 | $62.00 | 2.82x | 2.1 months |

**Actionable insight**: Google Brand has the best LTV:CAC but limited scale. Meta Lookalike offers the best balance of quality and scale. Google Non-Brand has the longest payback period.

---

## 4. LTV Calculation Methods

### Method 1: Historical (Actual Data)

```
LTV = Sum of all revenue from cohort / Number of customers in cohort
```

**Pros**: Accurate for mature cohorts.
**Cons**: Must wait months/years for complete data; not available for recent cohorts.

### Method 2: Predictive (Curve Fitting)

Model the revenue curve using historical data, then project forward.

**Common models**:

**Power law / Log curve**:
```
Revenue(t) = a * t^b

Where:
- t = month number
- a, b = parameters fitted to historical data
```

**BG/NBD Model** (Buy Till You Die):
Predicts individual customer purchase frequency and probability of still being "alive."

**Shifted Beta-Geometric**:
Models retention rates and predicts LTV based on retention decay curve.

### Method 3: Simplified LTV Formula

```
LTV = AOV * Purchase Frequency * Customer Lifespan

Where:
- AOV = Average Order Value
- Purchase Frequency = Average purchases per year
- Customer Lifespan = Average years active (or 1/churn rate)
```

**Example**:
- AOV: $65
- Purchase Frequency: 3.2x per year
- Customer Lifespan: 2.5 years
- LTV = $65 * 3.2 * 2.5 = $520

### Method 4: Contribution Margin LTV

```
CM-LTV = LTV * Gross Margin %

Example: $520 LTV * 60% margin = $312 contribution margin LTV
```

**This is what matters for advertising**: Your CAC must be lower than contribution margin LTV, not gross revenue LTV.

---

## 5. Payback Period Analysis

### What Is Payback Period?

The time it takes for cumulative revenue from a customer to exceed the cost of acquiring them.

### Calculating Payback Period

```
Payback Period = Month where Cumulative Revenue per Customer >= CAC
```

**Example**:

| Month | Cumulative Revenue | CAC | Profitable? |
|-------|-------------------|-----|-------------|
| 0 | $52.00 | $35.00 | Yes (Month 0 payback) |
| 1 | $63.40 | $35.00 | Yes |

vs.

| Month | Cumulative Revenue | CAC | Profitable? |
|-------|-------------------|-----|-------------|
| 0 | $25.00 | $45.00 | No |
| 1 | $38.00 | $45.00 | No |
| 2 | $47.00 | $45.00 | Yes (Month 2 payback) |

### Payback Period Benchmarks

| Business Model | Acceptable Payback | Good Payback | Excellent Payback |
|---------------|-------------------|--------------|-------------------|
| E-commerce (consumables) | < 3 months | < 2 months | < 1 month |
| E-commerce (one-time) | Immediate (Month 0) | N/A | N/A |
| SaaS (monthly) | < 12 months | < 6 months | < 3 months |
| SaaS (annual) | < 18 months | < 12 months | < 6 months |
| Subscription boxes | < 4 months | < 3 months | < 2 months |
| Info products | Immediate | N/A | N/A |
| B2B services | < 6 months | < 3 months | < 1 month |

### Why Payback Period Matters for Ad Spend

- **Short payback** = Can reinvest revenue into ads faster (compounding growth)
- **Long payback** = Need more working capital; cash flow risk
- **Rule of thumb**: If payback > 3 months, you need a cash reserve equal to 3 months of ad spend to sustain growth

---

## 6. Cohort Analysis by Ad Source

### Setting Up Source-Based Cohorts

**Data requirements**:
1. Customer acquisition date
2. Acquisition source (UTM parameters or platform attribution)
3. All subsequent purchases with dates and revenue
4. Customer ID to link purchases across sessions

**UTM structure for cohort tracking**:
```
utm_source=meta&utm_medium=paid&utm_campaign=prospecting_broad_jan2026
utm_source=google&utm_medium=cpc&utm_campaign=nonbrand_electronics
```

### Example: Source Quality Comparison

| Source | Customers | First Purchase AOV | 6-Month LTV | 12-Month LTV | Repeat Rate | CAC | LTV:CAC |
|--------|-----------|-------------------|-------------|--------------|-------------|-----|---------|
| Meta Prospecting | 2,500 | $48 | $82 | $115 | 35% | $32 | 3.6x |
| Meta Retargeting | 1,200 | $62 | $95 | $128 | 42% | $18 | 7.1x |
| Google Non-Brand | 1,800 | $55 | $78 | $105 | 30% | $42 | 2.5x |
| Google Brand | 800 | $65 | $110 | $155 | 48% | $8 | 19.4x |
| TikTok | 900 | $38 | $58 | $72 | 22% | $20 | 3.6x |
| Organic | 3,000 | $60 | $105 | $150 | 45% | $0 | Infinite |

**Key insights from this data**:
- Google Brand and Organic have the highest LTV, but these customers likely discovered you through other channels first
- Meta Prospecting and TikTok are the true growth drivers; their LTV:CAC is healthy
- TikTok customers have the lowest repeat rate; worth investigating why (younger audience? impulse purchases?)
- Meta Retargeting has excellent metrics but is dependent on prospecting to fill the retargeting pool

---

## 7. Building Cohort Reports

### Data Sources

| Source | Data Available | Pros | Cons |
|--------|---------------|------|------|
| GA4 | Cohort exploration report | Built-in; free | Limited to web data |
| Shopify | Customer cohort reports | E-commerce native; easy | Shopify only |
| BigQuery + GA4 | Raw event data | Maximum flexibility | Requires SQL |
| CRM (HubSpot, Salesforce) | Customer lifecycle data | Complete view | Setup required |
| Spreadsheet | Manual analysis | Simple; customizable | Doesn't scale |

### GA4 Cohort Exploration

1. GA4 > Explore > Cohort Exploration
2. Configure:
   - Cohort inclusion: First touch date
   - Return criteria: Any event, purchase, etc.
   - Granularity: Daily, weekly, or monthly
   - Segments: By source/medium
3. Export data for further analysis

### SQL Example (BigQuery + GA4)

```sql
-- Monthly revenue cohort by acquisition source
WITH first_touch AS (
  SELECT
    user_pseudo_id,
    MIN(event_date) AS acquisition_date,
    -- Get first traffic source
    FIRST_VALUE(traffic_source.source)
      OVER (PARTITION BY user_pseudo_id ORDER BY event_timestamp) AS source
  FROM `project.analytics_XXXXXX.events_*`
  WHERE event_name = 'session_start'
  GROUP BY user_pseudo_id
),
purchases AS (
  SELECT
    user_pseudo_id,
    event_date AS purchase_date,
    (SELECT value.double_value FROM UNNEST(event_params)
     WHERE key = 'value') AS revenue
  FROM `project.analytics_XXXXXX.events_*`
  WHERE event_name = 'purchase'
)
SELECT
  FORMAT_DATE('%Y-%m', PARSE_DATE('%Y%m%d', ft.acquisition_date)) AS cohort_month,
  ft.source,
  DATE_DIFF(
    PARSE_DATE('%Y%m%d', p.purchase_date),
    PARSE_DATE('%Y%m%d', ft.acquisition_date),
    MONTH
  ) AS months_since_acquisition,
  COUNT(DISTINCT ft.user_pseudo_id) AS customers,
  SUM(p.revenue) AS total_revenue,
  SUM(p.revenue) / COUNT(DISTINCT ft.user_pseudo_id) AS revenue_per_customer
FROM first_touch ft
LEFT JOIN purchases p ON ft.user_pseudo_id = p.user_pseudo_id
GROUP BY 1, 2, 3
ORDER BY 1, 2, 3;
```

---

## 8. Acting on Cohort Insights

### Decisions Cohort Analysis Enables

| Insight | Action |
|---------|--------|
| TikTok cohorts have 40% lower LTV than Meta | Reduce TikTok CPA target to match lower LTV |
| January cohort has best retention (post-holiday motivation) | Increase January ad spend; seasonal strategy |
| Customers from "pain point" ads have higher LTV than "discount" ads | Shift creative mix toward pain point messaging |
| First purchase of Product A leads to 2x higher repeat rate than Product B | Promote Product A as the entry point in ads |
| Mobile-acquired customers churn 30% faster than desktop | Optimize mobile landing pages; add post-purchase nurture for mobile |
| Cohorts are declining month-over-month | Diagnose: ad quality issue, product issue, or market saturation |

### Feeding LTV Back Into Ad Platforms

**Meta Value-Based Lookalike Audiences**:
1. Upload customer list with LTV values
2. Create Lookalike based on highest-LTV customers
3. Meta optimizes for users similar to your best customers

**Google Ads Value-Based Bidding**:
1. Import offline conversion values (LTV-adjusted)
2. Use Target ROAS or Maximize Conversion Value bidding
3. Google bids more for users likely to have higher LTV

**TikTok Value-Based Optimization**:
1. Send purchase events with value parameter
2. Optimize campaigns for "Value" rather than just "Conversions"

---

## 9. LTV Benchmarks by Industry

| Industry | Typical 12-Month LTV | Typical Repeat Rate | Typical Payback |
|----------|---------------------|--------------------|-----------------|
| E-commerce (consumables/beauty) | $120-$300 | 30-50% | 1-3 months |
| E-commerce (fashion) | $150-$400 | 25-40% | 1-2 months |
| E-commerce (electronics) | $80-$200 | 10-20% | Immediate |
| SaaS (SMB) | $300-$1,200 | 70-90% annual retention | 3-12 months |
| SaaS (Enterprise) | $5,000-$50,000 | 85-95% annual retention | 6-18 months |
| Subscription boxes | $150-$500 | 40-60% 12-month retention | 2-4 months |
| Info products/courses | $100-$500 | 10-30% (upsells) | Immediate |
| Local services | $200-$2,000 | 20-50% | 1-3 months |

---

## 10. Common Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Using revenue LTV instead of margin LTV | Overspending on acquisition | Calculate contribution margin LTV |
| Not accounting for returns/refunds | LTV inflated | Deduct returns from revenue before calculating |
| Blending all customers into one LTV | Hides channel quality differences | Segment by acquisition source |
| Using averages only (not distributions) | Outliers skew results | Look at median LTV and percentile distributions |
| Projecting LTV too far into future | Over-optimistic; justifies high CAC | Use conservative projections (6-12 months) |
| Ignoring cohort trends | Missing deterioration signals | Track cohort performance month-over-month |

---

*Last updated: March 2026. Cohort analysis is the foundation of sustainable paid traffic scaling. The best traffic managers don't just optimize for ROAS on Day 0; they optimize for LTV:CAC ratios over time.*
