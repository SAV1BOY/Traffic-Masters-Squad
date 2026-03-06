# ROI Calculator Component

## Purpose
Reusable ROI and ROAS calculation toolkit for evaluating paid traffic profitability. Includes formulas, break-even analysis, scenario modeling, and LTV-based projections.

---

## Core ROI Formulas

### ROAS (Return on Ad Spend)
```
ROAS = Total Revenue / Total Ad Spend
```
- **Example:** $25,000 revenue / $5,000 ad spend = 5.0x ROAS
- **Interpretation:** For every $1 spent on ads, $5 in revenue was generated

### ROI (Return on Investment)
```
ROI = ((Revenue - Total Costs) / Total Costs) x 100
```
- **Total Costs** = Ad Spend + COGS + Agency Fees + Tools + Creative Production
- **Example:** (($25,000 - $15,000) / $15,000) x 100 = 66.7% ROI

### Net Profit from Ads
```
Net Profit = Revenue - COGS - Ad Spend - Other Costs
```
- **Example:** $25,000 - $10,000 (COGS) - $5,000 (ads) - $1,000 (fees) = $9,000 net profit

### Profit Margin After Ads
```
Margin = (Revenue - COGS - Ad Spend) / Revenue x 100
```
- **Example:** ($25,000 - $10,000 - $5,000) / $25,000 x 100 = 40%

---

## Break-Even Analysis

### Break-Even ROAS
The minimum ROAS needed to cover cost of goods sold (zero profit on first purchase).

```
Break-Even ROAS = 1 / Gross Margin %
```

| Gross Margin | Break-Even ROAS |
|---|---|
| 80% | 1.25x |
| 70% | 1.43x |
| 60% | 1.67x |
| 50% | 2.00x |
| 40% | 2.50x |
| 30% | 3.33x |
| 20% | 5.00x |

### Break-Even CPA
The maximum you can spend to acquire a customer and still break even.

```
Break-Even CPA = AOV x Gross Margin %
```
- **Example:** $100 AOV x 60% margin = $60 max CPA

### Target ROAS (for desired profit)
```
Target ROAS = 1 / (Gross Margin % - Desired Net Margin %)
```
- **Example:** 1 / (0.60 - 0.15) = 2.22x ROAS for 15% net margin

### Target CPA (for desired profit)
```
Target CPA = AOV x (Gross Margin % - Desired Net Margin %)
```
- **Example:** $100 x (0.60 - 0.15) = $45 target CPA

---

## Profitability Calculator

### Per-Conversion Profitability

```
Input:
  Average Order Value (AOV):     ${{AOV}}
  Cost of Goods Sold (COGS):     ${{COGS}} or {{COGS_PCT}}%
  Ad Spend per Conversion (CPA): ${{CPA}}
  Other Variable Costs:          ${{OTHER}} (shipping, payment processing, etc.)

Calculations:
  Gross Profit = AOV - COGS = ${{}}
  Gross Margin = Gross Profit / AOV = {{}}%
  Net Profit = Gross Profit - CPA - Other Costs = ${{}}
  Net Margin = Net Profit / AOV = {{}}%
  Profitable? = {{YES / NO}}
```

### Quick Profit Table

| AOV | COGS (40%) | Gross Profit | CPA | Other Costs | Net Profit | Verdict |
|---|---|---|---|---|---|---|
| $50 | $20 | $30 | $15 | $3 | $12 | Profitable |
| $50 | $20 | $30 | $25 | $3 | $2 | Marginal |
| $50 | $20 | $30 | $35 | $3 | -$8 | Unprofitable |
| $100 | $40 | $60 | $30 | $5 | $25 | Profitable |
| $100 | $40 | $60 | $50 | $5 | $5 | Marginal |
| $100 | $40 | $60 | $70 | $5 | -$15 | Unprofitable |

---

## LTV-Based ROI

### When first-purchase ROI is negative but LTV justifies acquisition:

```
LTV = AOV x Purchase Frequency x Customer Lifespan
LTV Gross Profit = LTV x Gross Margin %
LTV-Based ROI = ((LTV Gross Profit - CAC) / CAC) x 100
```

**Example:**
- AOV: $80 | Purchase Frequency: 3x/year | Lifespan: 2.5 years
- LTV = $80 x 3 x 2.5 = $600
- LTV Gross Profit = $600 x 60% = $360
- CAC = $100
- LTV ROI = (($360 - $100) / $100) x 100 = 260%

### LTV:CAC Ratio

| Ratio | Interpretation | Action |
|---|---|---|
| < 1.0x | Losing money even long-term | Reduce CAC or improve retention |
| 1.0 - 2.0x | Marginal, high risk | Optimize both acquisition and retention |
| 2.0 - 3.0x | Acceptable | Stable business, room to scale cautiously |
| 3.0 - 5.0x | Healthy | Scale confidently |
| > 5.0x | Very strong (or under-investing in growth) | Increase ad spend to capture more market |

### Payback Period
```
Payback Period (months) = CAC / (Monthly Revenue per Customer x Gross Margin %)
```
- **Example:** $100 / ($20/month x 0.60) = 8.3 months to recoup acquisition cost

---

## Scenario Modeling

### Input Variables

```
Current Monthly Ad Spend:    ${{SPEND}}
Current Monthly Revenue:     ${{REVENUE}}
Current ROAS:                {{ROAS}}x
Current CPA:                 ${{CPA}}
Current Monthly Conversions: {{CONVERSIONS}}
Gross Margin:                {{MARGIN}}%
```

### Scenarios

| Scenario | Monthly Spend | Est. ROAS | Est. Revenue | Est. Conv. | Est. CPA | Net Profit | ROI |
|---|---|---|---|---|---|---|---|
| **Cut 30%** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Cut 15%** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Current** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Increase 15%** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Increase 30%** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Increase 50%** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Double** | $`{{}}` | `{{}}`x | $`{{}}` | `{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |

**Note:** Apply diminishing returns factor of 10-20% CPA increase for each 25% spend increase.

---

## Channel-Level ROI Comparison

| Channel | Spend | Revenue | ROAS | COGS | Gross Profit | Net After Ads | ROI | Rank |
|---|---|---|---|---|---|---|---|---|
| `{{}}` | $`{{}}` | $`{{}}` | `{{}}`x | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |

### Where to Invest Next Dollar

Rank channels by **marginal ROI** (not average ROI):
```
Marginal ROI = (Incremental Revenue x Gross Margin - Incremental Spend) / Incremental Spend
```

The channel with the highest marginal ROI should receive the next incremental dollar.

---

## Annual ROI Projection

```
Annual Ad Spend:        ${{ANNUAL_SPEND}}
Projected Annual Rev:   ${{ANNUAL_REVENUE}}
Annual COGS:            ${{ANNUAL_COGS}}
Annual Gross Profit:    ${{ANNUAL_GP}}
Annual Net After Ads:   ${{ANNUAL_NET}}
Annual ROAS:            {{}}x
Annual ROI:             {{}}%
New Customers (Annual): {{}}
LTV of Cohort:          ${{}} (projected over {{}} years)
```

---

## Decision Framework

### Is the campaign profitable?

```
IF ROAS > Break-Even ROAS:
  -> Campaign is covering COGS (but may not yield profit after other costs)

IF ROAS > Target ROAS:
  -> Campaign is hitting desired profitability
  -> Consider scaling

IF ROAS < Break-Even ROAS:
  -> Campaign is losing money on first purchase
  -> Check: Does LTV justify the CAC?
    -> IF LTV:CAC > 3.0x AND payback < 6 months: acceptable loss-leader strategy
    -> IF LTV:CAC < 2.0x: campaign needs optimization or should be paused

IF CPA < Break-Even CPA:
  -> Profitable per conversion
  -> Scale if volume is available

IF CPA > Break-Even CPA:
  -> Losing money per conversion
  -> Optimize or pause
```
