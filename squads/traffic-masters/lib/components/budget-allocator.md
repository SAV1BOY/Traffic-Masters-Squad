# Budget Allocator Component

## Purpose
Reusable logic for allocating, distributing, and adjusting paid traffic budgets across channels, campaigns, and funnel stages.

---

## Allocation Frameworks

### 70-20-10 Rule

| Category | Allocation | Description | Risk Level |
|---|---|---|---|
| **Proven (70%)** | 70% of budget | Campaigns with established, consistent performance | Low |
| **Iterative (20%)** | 20% of budget | Variations on proven campaigns -- new audiences, angles, copy | Medium |
| **Experimental (10%)** | 10% of budget | Net-new concepts, channels, formats, or strategies | High |

**Example:** $10,000 monthly budget
- Proven: $7,000 across top-performing campaigns
- Iterative: $2,000 testing new audiences on proven creative
- Experimental: $1,000 testing a new platform or format

---

### Funnel-Stage Allocation

| Funnel Stage | Suggested Range | Objective | Primary Metrics |
|---|---|---|---|
| **Top of Funnel (TOFU)** | 50-70% | Awareness, reach, new traffic | CPM, Reach, Thumb-Stop Rate |
| **Middle of Funnel (MOFU)** | 15-25% | Engagement, consideration, nurture | CPC, CTR, Video View Rate |
| **Bottom of Funnel (BOFU)** | 15-30% | Conversion, retargeting, closing | CPA, ROAS, CVR |
| **Retention** | 5-10% | Upsell, cross-sell, win-back | Repeat Purchase Rate, LTV |

**Adjustment Triggers:**
- If BOFU audiences are small (< 5,000), shift more to TOFU to build the pool
- If ROAS is strong at BOFU but volume is limited, increase TOFU to feed the funnel
- If CPA at TOFU is unsustainable, tighten to proven MOFU/BOFU audiences

---

### Channel Allocation Model

| Factor | Weight | How to Score |
|---|---|---|
| Historical ROAS | 30% | Higher ROAS = higher allocation |
| Volume Potential | 25% | Larger addressable audience = higher allocation |
| Marginal CPA Trend | 20% | Stable/declining marginal CPA = higher allocation |
| Strategic Importance | 15% | Brand building, new market entry = bonus weight |
| Data Quality | 10% | Better attribution/tracking = higher allocation |

**Scoring Formula:**
```
Channel Score = (ROAS_Score x 0.30) + (Volume_Score x 0.25) + (Marginal_CPA_Score x 0.20) + (Strategic_Score x 0.15) + (Data_Score x 0.10)

Allocation % = Channel Score / Sum of All Channel Scores x 100
```

---

## Budget Setting Methods

### Method 1: Target-Back (Recommended for Performance Campaigns)
```
Required Budget = Target Conversions x Target CPA
```
**Example:** 200 conversions x $50 CPA = $10,000 budget needed

### Method 2: Revenue-Based
```
Budget = Target Revenue / Target ROAS
```
**Example:** $50,000 revenue / 5.0x ROAS = $10,000 budget needed

### Method 3: Percentage of Revenue
```
Budget = Gross Revenue x Ad Spend Ratio
```
- **Typical Ratios:** 5-15% for established brands, 15-30% for growth-stage, 30-50% for launches
- **Example:** $200,000 monthly revenue x 10% = $20,000 budget

### Method 4: Competitive Parity
```
Budget = Estimated Competitor Spend x Market Share Target
```
- Use tools like SEMrush, SpyFu, or Meta Ad Library for estimates

---

## Daily Budget Calculation

### From Monthly Budget
```
Daily Budget = Monthly Budget / Days in Month
```
**Example:** $10,000 / 30 = $333.33/day

### With Weekend Adjustment
If performance varies by day of week, apply day-of-week coefficients:

| Day | Typical Index | Adjusted Daily Budget (from $333 base) |
|---|---|---|
| Monday | 1.05 | $350 |
| Tuesday | 1.10 | $367 |
| Wednesday | 1.10 | $367 |
| Thursday | 1.05 | $350 |
| Friday | 0.95 | $317 |
| Saturday | 0.85 | $283 |
| Sunday | 0.90 | $300 |

**Note:** Adjust coefficients based on actual account data. B2B typically peaks mid-week; ecommerce often peaks on weekends.

---

## Budget Scaling Rules

### Safe Scaling Increments

| Current Daily Budget | Max Increase | Rationale |
|---|---|---|
| $0 - $100 | 50-100% | Small budgets can absorb larger jumps |
| $100 - $500 | 20-30% | Moderate caution to preserve learning |
| $500 - $2,000 | 15-20% | Algorithm stability matters more |
| $2,000+ | 10-15% | Preserve optimization, avoid resetting learning |

### Scaling Decision Tree
```
IF CPA < Target CPA AND ROAS > Target ROAS for 3+ consecutive days:
  -> Increase budget by 15-20%
  -> Wait 3-4 days before next increase
  -> Monitor marginal CPA after increase

IF CPA = Target CPA (within 10%) AND volume is consistent:
  -> Hold current budget
  -> Focus on creative/audience optimization instead

IF CPA > Target CPA by 20%+:
  -> Do NOT increase budget
  -> Diagnose root cause before any changes
  -> Consider reducing budget by 10-20% if no improvement in 48 hours
```

### Budget Decrease Protocol
1. Never cut more than 25% at once (can trigger re-learning)
2. Prefer pausing underperforming ad sets over cutting campaign budget
3. If cutting, do it at the start of a new day (platform timezone)
4. Document the reason for every decrease

---

## Reallocation Triggers

### When to Reallocate Between Channels

| Trigger | Action | Threshold |
|---|---|---|
| Channel ROAS diverges significantly | Shift 10-15% from low to high ROAS | > 30% ROAS gap |
| One channel hits diminishing returns | Cap spend, redirect to expanding channel | Marginal CPA > 2x avg CPA |
| New channel proves viable | Graduate from experimental to iterative budget | 2+ weeks of data, CPA within target |
| Seasonal shift | Pre-allocate based on historical patterns | 2-4 weeks before peak |
| Creative fatigue on one channel | Reduce spend while refreshing, boost others | CTR decline > 25% from peak |

### Reallocation Calculation
```
Reallocation Amount = Min(
  Underperforming Channel Spend x 20%,
  Receiving Channel Capacity (based on audience size and saturation)
)
```

---

## Budget Pacing Monitor

### Pacing Formula
```
Pacing Index = (% of Budget Spent) / (% of Period Elapsed)
```

| Pacing Index | Status | Action |
|---|---|---|
| > 1.10 | Over-pacing | Reduce daily budgets by (Index - 1.0) x 100% |
| 0.95 - 1.10 | On-track | No action needed |
| 0.80 - 0.95 | Slightly under-pacing | Increase budgets modestly or launch held campaigns |
| < 0.80 | Significantly under-pacing | Investigate delivery issues, expand targeting, increase bids |

### End-of-Month Catch-Up
```
Required Daily Spend (remaining days) = Remaining Budget / Remaining Days
```
If required daily > 150% of current daily, flag for discussion rather than forcing spend.

---

## Template: Budget Allocation Worksheet

```
TOTAL MONTHLY BUDGET: ${{TOTAL}}

CHANNEL ALLOCATION:
  Meta Ads:        ${{}} ({{}}%)
  Google Search:   ${{}} ({{}}%)
  Google Shopping:  ${{}} ({{}}%)
  YouTube:         ${{}} ({{}}%)
  TikTok:          ${{}} ({{}}%)
  Other:           ${{}} ({{}}%)
  Reserve/Testing: ${{}} ({{}}%)

FUNNEL ALLOCATION:
  TOFU (Prospecting): ${{}} ({{}}%)
  MOFU (Nurture):     ${{}} ({{}}%)
  BOFU (Retargeting): ${{}} ({{}}%)
  Retention:          ${{}} ({{}}%)

RISK ALLOCATION:
  Proven (70%):       ${{}}
  Iterative (20%):    ${{}}
  Experimental (10%): ${{}}

DAILY BUDGET TARGET: ${{}} / day
PACING CHECK DATES: {{7th}}, {{14th}}, {{21st}}, {{28th}}
```
