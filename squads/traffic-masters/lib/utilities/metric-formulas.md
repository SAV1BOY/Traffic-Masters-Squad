# Metric Formulas Reference

## Purpose
Complete reference of all advertising metric calculation formulas with examples. Use as a quick lookup when calculating or explaining metrics.

---

## Traffic Metrics

### Impressions
Total number of times an ad was displayed on screen.
- No formula (raw count from platform)
- One user can generate multiple impressions

### Reach
Total number of unique users who saw the ad.
- No formula (raw count from platform)
- Reach <= Impressions (always)

### Frequency
```
Frequency = Impressions / Reach
```
**Example:** 50,000 impressions / 20,000 reach = 2.5 frequency
**Benchmarks:** Prospecting: 1.5-3.0 | Retargeting: 3.0-8.0

### CPM (Cost Per Mille)
```
CPM = (Spend / Impressions) x 1,000
```
**Example:** $500 / 100,000 x 1,000 = $5.00

### CPC (Cost Per Click)
```
CPC = Spend / Clicks
```
**Example:** $500 / 250 = $2.00

### CTR (Click-Through Rate)
```
CTR = (Clicks / Impressions) x 100
```
**Example:** 250 / 100,000 x 100 = 0.25%

### CPC from CPM and CTR
```
CPC = CPM / (CTR% x 10)
```
**Example:** $10.00 / (1.0 x 10) = $1.00

### Impression Share (Google)
```
Impression Share = Your Impressions / Total Eligible Impressions
```
**Example:** 8,000 / 10,000 = 80%

---

## Engagement Metrics

### Thumb-Stop Rate
```
Thumb-Stop Rate = (3-Second Video Views / Impressions) x 100
```
**Example:** 25,000 / 100,000 x 100 = 25%

### Hook Rate
```
Hook Rate = (Video Views at 25% / Video Plays) x 100
```
**Example:** 15,000 / 30,000 x 100 = 50%

### Hold Rate
```
Hold Rate = (Video Views at 75% / Video Views at 25%) x 100
```
**Example:** 6,000 / 15,000 x 100 = 40%

### Video Completion Rate (VCR)
```
VCR = (Video Views at 100% / Video Plays) x 100
```
**Example:** 3,000 / 30,000 x 100 = 10%

### Average Watch Time
```
Avg Watch Time = Total Watch Time / Video Plays
```
**Example:** 150,000 seconds / 30,000 plays = 5.0 seconds

### Engagement Rate
```
Engagement Rate = (Engagements / Impressions) x 100
```
Where engagements = likes + comments + shares + saves + clicks

### Cost Per Engagement (CPE)
```
CPE = Spend / Engagements
```

### Cost Per Video View (CPVV)
```
CPVV = Spend / Video Views
```

---

## Landing Page Metrics

### Landing Page View Rate
```
LP View Rate = (Landing Page Views / Link Clicks) x 100
```
**Example:** 200 / 250 x 100 = 80%
**Healthy:** 70-90%. Below 70% = slow page or redirect issue.

### Bounce Rate
```
Bounce Rate = (Single-Page Sessions / Total Sessions) x 100
```
**Example:** 60 / 200 x 100 = 30%

### Pages Per Session
```
Pages/Session = Total Pageviews / Total Sessions
```

### Average Session Duration
```
Avg Duration = Total Session Time / Total Sessions
```

---

## Conversion Metrics

### Conversion Rate (CVR)
```
CVR = (Conversions / Clicks) x 100
```
**Example:** 20 / 250 x 100 = 8.0%

### Landing Page Conversion Rate
```
LP CVR = (Conversions / Landing Page Views) x 100
```
**Example:** 20 / 200 x 100 = 10.0%

### CPA (Cost Per Acquisition)
```
CPA = Spend / Conversions
```
**Example:** $1,000 / 20 = $50.00

### CPL (Cost Per Lead)
```
CPL = Spend / Leads
```
Same formula as CPA but conversion event is a lead.

### Cost Per Add-to-Cart
```
Cost Per ATC = Spend / Add to Cart Events
```

### Cost Per Initiate Checkout
```
Cost Per IC = Spend / Initiate Checkout Events
```

### Add-to-Cart Rate
```
ATC Rate = (ATC Events / Landing Page Views) x 100
```
**Example:** 40 / 200 x 100 = 20%

### Cart-to-Purchase Rate
```
Cart-to-Purchase = (Purchases / ATC Events) x 100
```
**Example:** 20 / 40 x 100 = 50%

### Checkout Completion Rate
```
Checkout Completion = (Purchases / Initiate Checkout Events) x 100
```
**Example:** 20 / 25 x 100 = 80%

---

## Revenue Metrics

### ROAS (Return on Ad Spend)
```
ROAS = Revenue / Ad Spend
```
**Example:** $5,000 / $1,000 = 5.0x

### AOV (Average Order Value)
```
AOV = Total Revenue / Total Orders
```
**Example:** $5,000 / 20 = $250

### Revenue Per Click (RPC)
```
RPC = Revenue / Clicks
```
**Example:** $5,000 / 250 = $20.00

### Revenue Per Impression (RPI)
```
RPI = Revenue / Impressions x 1,000
```
**Example:** $5,000 / 100,000 x 1,000 = $50 per 1,000 impressions

---

## Profitability Metrics

### Gross Profit
```
Gross Profit = Revenue - COGS
```

### Gross Margin
```
Gross Margin = (Revenue - COGS) / Revenue x 100
```
**Example:** ($5,000 - $2,000) / $5,000 x 100 = 60%

### Net Profit After Ads
```
Net Profit = Revenue - COGS - Ad Spend - Other Costs
```

### ROI (Return on Investment)
```
ROI = ((Revenue - Total Costs) / Total Costs) x 100
```
**Example:** (($5,000 - $3,000) / $3,000) x 100 = 66.7%

### Break-Even ROAS
```
Break-Even ROAS = 1 / Gross Margin %
```
**Example:** 1 / 0.60 = 1.67x

### Break-Even CPA
```
Break-Even CPA = AOV x Gross Margin %
```
**Example:** $250 x 0.60 = $150

### Profit Per Conversion
```
Profit Per Conv = (AOV x Gross Margin %) - CPA
```
**Example:** ($250 x 0.60) - $50 = $100

### Contribution Margin
```
Contribution Margin = (Revenue - Variable Costs) / Revenue x 100
```

---

## Customer Metrics

### CAC (Customer Acquisition Cost)
```
CAC = Total Sales & Marketing Cost / New Customers
```
Note: CAC is broader than CPA -- includes salaries, tools, overhead.

### LTV (Lifetime Value)
```
LTV = AOV x Purchase Frequency x Customer Lifespan (years)
```
**Example:** $250 x 2.5 x 3 = $1,875

### LTV (Margin-Adjusted)
```
LTV (Margin) = LTV x Gross Margin %
```
**Example:** $1,875 x 0.60 = $1,125

### LTV:CAC Ratio
```
LTV:CAC = LTV / CAC
```
**Example:** $1,875 / $100 = 18.75x

### Payback Period
```
Payback (months) = CAC / (Monthly Revenue per Customer x Gross Margin %)
```
**Example:** $100 / ($50 x 0.60) = 3.3 months

### Churn Rate
```
Churn Rate = Customers Lost in Period / Customers at Start of Period x 100
```

### Retention Rate
```
Retention Rate = 100% - Churn Rate
```

---

## Efficiency Metrics

### Efficiency Index
```
Efficiency Index = (Share of Conversions %) / (Share of Spend %)
```
**Example:** 30% of conversions / 20% of spend = 1.5 (over-indexing)

### Marginal CPA
```
Marginal CPA = (Spend_new - Spend_old) / (Conv_new - Conv_old)
```
**Example:** ($2,000 - $1,000) / (35 - 20) = $66.67

### Budget Utilization
```
Utilization = Actual Spend / Allocated Budget x 100
```

### Pacing Index
```
Pacing Index = (% Budget Spent) / (% Period Elapsed)
```
**Example:** 55% spent / 50% elapsed = 1.10 (slightly over-pacing)

---

## Statistical Metrics

### Statistical Significance (Z-Test)
```
Z = (p1 - p2) / sqrt(p_pool x (1 - p_pool) x (1/n1 + 1/n2))

Where:
  p1 = conversion rate of variant A
  p2 = conversion rate of variant B
  p_pool = total conversions / total sample size
  n1, n2 = sample sizes
```
Z > 1.645 = 90% confidence | Z > 1.96 = 95% confidence

### Confidence Interval
```
CI = p +/- Z x sqrt(p x (1-p) / n)
```

### Minimum Sample Size
```
n = (Z^2 x p x (1-p)) / MDE^2
```
Where MDE = minimum detectable effect (as proportion)
