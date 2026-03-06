# KPI Calculator Component

## Purpose
Reusable KPI calculation formulas for paid traffic campaigns. Use this component whenever you need to compute, validate, or explain advertising performance metrics.

---

## Core Traffic Metrics

### CPM (Cost Per Mille / Cost Per 1,000 Impressions)
```
CPM = (Total Spend / Impressions) x 1,000
```
- **Example:** $500 spend / 100,000 impressions x 1,000 = $5.00 CPM
- **Benchmark Range:** $5-$15 (Meta), $2-$8 (TikTok), $10-$30 (LinkedIn)
- **What it tells you:** How expensive it is to reach your audience; measures auction competitiveness

### CPC (Cost Per Click)
```
CPC = Total Spend / Total Clicks
```
- **Example:** $500 spend / 250 clicks = $2.00 CPC
- **Benchmark Range:** $0.50-$2.00 (Meta), $1.00-$5.00 (Google Search), $0.30-$1.50 (TikTok)
- **What it tells you:** Cost efficiency of driving traffic

### CTR (Click-Through Rate)
```
CTR = (Total Clicks / Total Impressions) x 100
```
- **Example:** 250 clicks / 100,000 impressions x 100 = 0.25% CTR
- **Benchmark Range:** 0.8%-2.0% (Meta Feed), 2%-5% (Google Search), 0.5%-1.5% (Display)
- **What it tells you:** How compelling your ad is to the audience seeing it

### CPC from CPM and CTR
```
CPC = CPM / (CTR x 10)
```
- **Example:** $10 CPM / (1.0% x 10) = $1.00 CPC

---

## Conversion Metrics

### CPA (Cost Per Acquisition / Cost Per Action)
```
CPA = Total Spend / Total Conversions
```
- **Example:** $1,000 spend / 20 conversions = $50.00 CPA
- **What it tells you:** How much each desired action (purchase, lead, signup) costs

### CPL (Cost Per Lead)
```
CPL = Total Spend / Total Leads
```
- **Example:** $1,000 spend / 50 leads = $20.00 CPL
- **Note:** Specific form of CPA where the conversion event is a lead

### CVR (Conversion Rate)
```
CVR = (Total Conversions / Total Clicks) x 100
```
- **Example:** 20 conversions / 250 clicks x 100 = 8.0% CVR
- **Benchmark Range:** 2%-5% (ecommerce), 5%-15% (lead gen), 10%-25% (high-intent search)

### Landing Page View Rate
```
LP View Rate = (Landing Page Views / Link Clicks) x 100
```
- **Example:** 200 LP views / 250 clicks x 100 = 80%
- **Healthy Range:** 70%-90%. Below 70% suggests slow page load or bounce issues.

### Add to Cart Rate
```
ATC Rate = (Add to Cart Events / Landing Page Views) x 100
```
- **Example:** 40 ATC / 200 LP views x 100 = 20%

### Checkout Initiation Rate
```
IC Rate = (Initiate Checkout Events / Add to Cart Events) x 100
```
- **Example:** 25 IC / 40 ATC x 100 = 62.5%

### Purchase Conversion Rate (from ATC)
```
Purchase Rate = (Purchases / Add to Cart Events) x 100
```
- **Example:** 20 purchases / 40 ATC x 100 = 50%

---

## Revenue and Profitability Metrics

### ROAS (Return on Ad Spend)
```
ROAS = Total Revenue / Total Ad Spend
```
- **Example:** $5,000 revenue / $1,000 spend = 5.0x ROAS
- **Note:** Express as a multiple (e.g., 5.0x), not percentage

### ROI (Return on Investment)
```
ROI = ((Revenue - Total Cost) / Total Cost) x 100
```
- **Example:** (($5,000 - $2,500) / $2,500) x 100 = 100% ROI
- **Total Cost includes:** Ad spend + COGS + agency fees + tool costs

### Break-Even ROAS
```
Break-Even ROAS = 1 / Gross Margin %
```
- **Example:** 1 / 0.60 (60% margin) = 1.67x ROAS needed to break even
- **Critical for:** Determining minimum acceptable ROAS

### Target ROAS (for desired net margin)
```
Target ROAS = 1 / (Gross Margin % - Target Net Margin %)
```
- **Example:** 1 / (0.60 - 0.20) = 2.5x ROAS for 20% net margin after ads

### AOV (Average Order Value)
```
AOV = Total Revenue / Total Orders
```
- **Example:** $5,000 / 20 orders = $250.00 AOV

### Revenue Per Click (RPC)
```
RPC = Total Revenue / Total Clicks
```
- **Example:** $5,000 / 250 clicks = $20.00 RPC

### Profit Per Conversion
```
Profit Per Conversion = AOV x Gross Margin % - CPA
```
- **Example:** $250 x 0.60 - $50 = $100 profit per conversion

---

## Customer Value Metrics

### CAC (Customer Acquisition Cost)
```
CAC = Total Marketing & Sales Cost / New Customers Acquired
```
- **Example:** $10,000 total cost / 100 new customers = $100 CAC
- **Note:** CAC includes all costs (not just ad spend), unlike CPA

### LTV (Lifetime Value)
```
LTV = AOV x Purchase Frequency x Customer Lifespan
```
- **Example:** $250 x 2.5 purchases/year x 3 years = $1,875 LTV
- **Alternative:** LTV = Average Revenue Per User (ARPU) / Churn Rate

### LTV:CAC Ratio
```
LTV:CAC = Customer Lifetime Value / Customer Acquisition Cost
```
- **Example:** $1,875 / $100 = 18.75x
- **Healthy Range:** 3x+ is generally healthy; below 1x is unsustainable

### Payback Period
```
Payback Period = CAC / (Monthly Revenue Per Customer x Gross Margin %)
```
- **Example:** $100 / ($50 x 0.60) = 3.3 months

---

## Engagement and Quality Metrics

### Frequency
```
Frequency = Total Impressions / Unique Reach
```
- **Example:** 100,000 impressions / 25,000 reach = 4.0 frequency
- **Healthy Range:** 1.5-3.0 for prospecting; up to 8-10 for retargeting

### Thumb-Stop Rate (Video)
```
Thumb-Stop Rate = (3-Second Video Views / Impressions) x 100
```
- **Example:** 30,000 views / 100,000 impressions x 100 = 30%
- **Good Range:** 25%+ is considered strong

### Hook Rate (Video)
```
Hook Rate = (Video Views at 25% / Total Video Plays) x 100
```

### Hold Rate (Video)
```
Hold Rate = (Video Views at 75% / Video Views at 25%) x 100
```

### Video View Rate
```
View Rate = (Video Views / Impressions) x 100
```

### Quality Score (Google Ads)
```
Quality Score = f(Expected CTR, Ad Relevance, Landing Page Experience)
```
- Scale: 1-10; target 7+
- **Impact:** Higher quality score = lower CPC, better positions

---

## Efficiency and Scaling Metrics

### Efficiency Index
```
Efficiency Index = Share of Conversions % / Share of Spend %
```
- **Example:** 30% of conversions / 20% of spend = 1.5 (over-indexing)
- **Above 1.0:** Channel converts efficiently relative to investment
- **Below 1.0:** Channel under-indexes on conversions

### Marginal CPA
```
Marginal CPA = Change in Spend / Change in Conversions
```
- **Example:** ($2,000 - $1,000) / (35 - 20) = $66.67 marginal CPA
- **Use for:** Evaluating whether incremental spend is still efficient

### Impression Share (Google)
```
Impression Share = Impressions / Total Eligible Impressions
```

### Budget Utilization
```
Budget Utilization = Actual Spend / Allocated Budget x 100
```

---

## How to Use This Component

1. **Daily Monitoring:** Focus on Spend, CPA, ROAS, CTR, CPC
2. **Weekly Analysis:** Add CVR, Frequency, Creative Metrics, Efficiency Index
3. **Monthly Review:** Full suite including LTV, CAC, Marginal CPA, Break-Even ROAS
4. **Quarterly Strategy:** LTV:CAC, Payback Period, Profitability Analysis

### Quick Health Check

| Signal | Green | Yellow | Red |
|---|---|---|---|
| CPA vs. Target | < 90% of target | 90-110% of target | > 110% of target |
| ROAS vs. Break-Even | > 1.5x break-even | 1.0-1.5x break-even | Below break-even |
| CTR vs. Benchmark | > benchmark | Within 20% of benchmark | > 20% below benchmark |
| Frequency | < 3.0 | 3.0-5.0 | > 5.0 (prospecting) |
| CVR vs. Historical | Improving | Stable | Declining > 15% |
