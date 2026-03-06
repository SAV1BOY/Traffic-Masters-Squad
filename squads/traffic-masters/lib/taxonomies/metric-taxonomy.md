# Metric Taxonomy

## Purpose
Standard taxonomy for classifying, organizing, and prioritizing metrics and KPIs in paid traffic operations. Provides a shared vocabulary for metric discussions across teams.

---

## Metric Classification Hierarchy

```
Level 1: Metric Category
  Level 2: Metric Name
    Level 3: Calculation Method
      Level 4: Context (Platform, Funnel Stage, Use Case)
```

---

## Level 1: Metric Categories

| Category | Purpose | When to Use | Audience |
|---|---|---|---|
| **Volume Metrics** | Measure quantity and scale | Always -- foundational | All stakeholders |
| **Efficiency Metrics** | Measure cost-effectiveness | Always -- core performance | Media buyers, analysts |
| **Quality Metrics** | Measure engagement and relevance | Creative reviews, diagnostics | Creative teams, analysts |
| **Revenue Metrics** | Measure financial returns | Business reviews, ROI analysis | Leadership, finance |
| **Customer Metrics** | Measure customer value and behavior | Strategic planning, LTV analysis | Leadership, strategy |
| **Funnel Metrics** | Measure progression through stages | Funnel diagnostics, optimization | Analysts, CRO teams |
| **Health Metrics** | Measure campaign and account health | Ongoing monitoring, diagnostics | Media buyers |

---

## Volume Metrics

| Metric | Formula | Unit | Direction | Priority |
|---|---|---|---|---|
| **Impressions** | Raw count | Count | Higher = more reach | Standard |
| **Reach** | Unique users who saw ad | Count | Higher = more unique exposure | Standard |
| **Clicks** | Raw count of ad clicks | Count | Higher = more traffic | Standard |
| **Link Clicks** | Clicks to destination URL | Count | Higher = more landing page traffic | High |
| **Landing Page Views** | Confirmed page loads after click | Count | Higher = more quality traffic | High |
| **Conversions** | Completed desired actions | Count | Higher = more results | Critical |
| **Revenue** | Total attributed revenue | Currency | Higher = more return | Critical |
| **Video Views** | Views meeting platform threshold | Count | Higher = more engagement | Standard |
| **Leads** | Lead form submissions | Count | Higher = more pipeline | Critical (lead gen) |
| **Orders** | Completed purchases | Count | Higher = more sales | Critical (e-commerce) |

---

## Efficiency Metrics

| Metric | Formula | Unit | Direction | Priority |
|---|---|---|---|---|
| **CPA** | Spend / Conversions | Currency | Lower = better | Critical |
| **CPL** | Spend / Leads | Currency | Lower = better | Critical (lead gen) |
| **CPC** | Spend / Clicks | Currency | Lower = better | High |
| **CPM** | (Spend / Impressions) x 1,000 | Currency | Lower = better | Standard |
| **ROAS** | Revenue / Ad Spend | Multiple (x) | Higher = better | Critical |
| **ROI** | ((Revenue - Costs) / Costs) x 100 | Percentage | Higher = better | Critical |
| **Cost per LP View** | Spend / Landing Page Views | Currency | Lower = better | High |
| **Cost per ATC** | Spend / Add to Cart Events | Currency | Lower = better | High (e-commerce) |
| **Cost per IC** | Spend / Initiate Checkout | Currency | Lower = better | Standard |
| **Cost per Video View** | Spend / Video Views | Currency | Lower = better | Standard |
| **Efficiency Index** | Share of Conv % / Share of Spend % | Index | Higher = better | High |
| **Marginal CPA** | Delta Spend / Delta Conversions | Currency | Lower = better | High (scaling) |

---

## Quality Metrics

| Metric | Formula | Unit | Direction | Priority |
|---|---|---|---|---|
| **CTR** | (Clicks / Impressions) x 100 | Percentage | Higher = better | High |
| **Thumb-Stop Rate** | (3s Views / Impressions) x 100 | Percentage | Higher = better | High (video) |
| **Hook Rate** | (25% Views / Plays) x 100 | Percentage | Higher = better | High (video) |
| **Hold Rate** | (75% Views / 25% Views) x 100 | Percentage | Higher = better | Medium (video) |
| **VCR** | (Complete Views / Plays) x 100 | Percentage | Higher = better | Medium (video) |
| **Engagement Rate** | (Engagements / Impressions) x 100 | Percentage | Higher = better | Standard |
| **Bounce Rate** | (Single-page Sessions / Sessions) x 100 | Percentage | Lower = better | High |
| **Avg. Session Duration** | Total Time / Sessions | Time | Higher = better | Medium |
| **Pages per Session** | Total Pageviews / Sessions | Count | Higher = better | Medium |
| **Quality Score** | Platform-calculated (1-10) | Score | Higher = better | High (Google) |
| **Ad Relevance** | Platform-calculated | Rating | Higher = better | Standard |
| **LP View Rate** | (LP Views / Link Clicks) x 100 | Percentage | Higher = better | High |

---

## Revenue Metrics

| Metric | Formula | Unit | Direction | Priority |
|---|---|---|---|---|
| **Total Revenue** | Sum of attributed revenue | Currency | Higher = better | Critical |
| **AOV** | Revenue / Orders | Currency | Higher = better | High |
| **Revenue per Click** | Revenue / Clicks | Currency | Higher = better | Medium |
| **Revenue per Impression** | (Revenue / Impressions) x 1,000 | Currency | Higher = better | Low |
| **Gross Profit** | Revenue - COGS | Currency | Higher = better | Critical |
| **Net Profit** | Revenue - COGS - Ad Spend - Costs | Currency | Higher = better | Critical |
| **Gross Margin** | (Revenue - COGS) / Revenue x 100 | Percentage | Higher = better | High |
| **Break-Even ROAS** | 1 / Gross Margin % | Multiple | -- | Reference |
| **Break-Even CPA** | AOV x Gross Margin % | Currency | -- | Reference |
| **Profit per Conversion** | (AOV x Margin %) - CPA | Currency | Higher = better | Critical |

---

## Customer Metrics

| Metric | Formula | Unit | Direction | Priority |
|---|---|---|---|---|
| **CAC** | Total Marketing + Sales Cost / New Customers | Currency | Lower = better | Critical |
| **LTV** | AOV x Purchase Frequency x Customer Lifespan | Currency | Higher = better | Critical |
| **LTV:CAC Ratio** | LTV / CAC | Ratio | Higher = better | Critical |
| **Payback Period** | CAC / (Monthly Rev x Margin %) | Months | Shorter = better | High |
| **New Customer Rate** | New Customers / Total Conversions x 100 | Percentage | Context-dependent | High |
| **Repeat Purchase Rate** | Repeat Buyers / Total Buyers x 100 | Percentage | Higher = better | High |
| **Churn Rate** | Lost Customers / Start Customers x 100 | Percentage | Lower = better | High |
| **Retention Rate** | 100% - Churn Rate | Percentage | Higher = better | High |

---

## Funnel Metrics

| Stage | Input Metric | Output Metric | Rate Metric | Cost Metric |
|---|---|---|---|---|
| **Impression to Click** | Impressions | Clicks | CTR | CPC |
| **Click to LP View** | Clicks | LP Views | LP View Rate | Cost per LP View |
| **LP View to Lead/ATC** | LP Views | Leads/ATCs | Conversion Rate | CPL / Cost per ATC |
| **ATC to Checkout** | ATCs | Checkouts | Checkout Init Rate | Cost per IC |
| **Checkout to Purchase** | Checkouts | Purchases | Purchase Completion Rate | CPA |

---

## Health Metrics

| Metric | Formula | Unit | Healthy Range | Alert Threshold |
|---|---|---|---|---|
| **Frequency** | Impressions / Reach | Count | 1.5-3.0 (prosp) | > 4.0 (prosp), > 8.0 (retarg) |
| **Impression Share** | Your Impr / Eligible Impr | Percentage | > 70% | < 50% |
| **Budget Utilization** | Actual Spend / Budget x 100 | Percentage | 90-100% | < 80% or > 105% |
| **Pacing Index** | % Budget Spent / % Period Elapsed | Index | 0.95-1.05 | < 0.80 or > 1.15 |
| **Learning Status** | Platform-reported | Status | Active | Learning Limited |
| **Ad Approval Rate** | Approved Ads / Total Ads x 100 | Percentage | 95%+ | < 90% |
| **Event Match Quality** | Platform-reported (1-10) | Score | 7+ | < 5 |
| **Creative Freshness** | Days since last new creative launch | Days | < 14 | > 21 |

---

## Metric Priority by Report Type

| Metric | Daily | Weekly | Monthly | Executive |
|---|---|---|---|---|
| Spend | Yes | Yes | Yes | Yes |
| Conversions | Yes | Yes | Yes | Yes |
| CPA | Yes | Yes | Yes | Yes |
| ROAS | Yes | Yes | Yes | Yes |
| Revenue | Optional | Yes | Yes | Yes |
| CTR | Yes | Yes | Yes | No |
| CPC | Yes | Yes | Yes | No |
| CPM | No | Yes | Yes | No |
| CVR | No | Yes | Yes | No |
| Frequency | Optional | Yes | Yes | No |
| AOV | No | Yes | Yes | Yes |
| LTV | No | No | Yes | Yes |
| CAC | No | No | Yes | Yes |
| ROI | No | No | Yes | Yes |

---

## Metric Interpretation Guide

### Always Compare Metrics To:
1. **Target** -- Are we meeting goals?
2. **Previous Period** -- Are we improving?
3. **Benchmark** -- Are we competitive?

### Metric Relationships
- **CPA = CPM / (CTR x CVR x 10)** -- CPA is driven by auction cost, creative quality, and funnel efficiency
- **ROAS = AOV x CVR / CPC** -- ROAS is driven by what people spend, how often they convert, and traffic cost
- **ROI = ROAS x Gross Margin - 1** -- ROI accounts for product costs, not just revenue

### Red Flags

| Combination | Indicates |
|---|---|
| CTR down + CPA up | Creative fatigue |
| CTR stable + CPA up | Funnel/LP issue |
| CPM up + CTR stable | Auction competition |
| Conversions down + spend stable | Tracking issue or funnel break |
| ROAS up + volume down | Over-optimization for efficiency at expense of scale |
