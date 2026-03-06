# nCAC Method - New Customer Acquisition Cost

> **Author**: Ralph Burns
> **Domain**: Marketing Metrics & Financial Optimization
> **Used by agents**: data-analyst, media-buyer, traffic-strategist, finance-liaison
> **Checklists**: ncac-calculation-worksheet, roas-to-ncac-migration-checklist

## Overview

The nCAC (New Customer Acquisition Cost) Method is Ralph Burns' 5-step replacement for ROAS as the primary optimization metric. The core insight: "ROAS sucks." ROAS is a vanity metric that does not account for customer quality, returns, refunds, chargebacks, or lifetime value. A 5x ROAS campaign that acquires customers who refund at 30% is worse than a 2x ROAS campaign acquiring customers who stay for 3 years. nCAC connects ad spend to actual business profitability.

## When to Use

- Setting up or resetting campaign optimization targets
- Evaluating whether a campaign is truly profitable (not just ROAS-positive)
- Comparing performance across channels with different purchase behaviors
- Building financial models for scaling decisions
- Convincing stakeholders to move beyond ROAS as the primary KPI

## The Framework

### Step 1: Calculate True ROAS

Before replacing ROAS, understand what your current ROAS actually means when you account for reality.

**Standard ROAS**: Revenue / Ad Spend
Example: $50,000 revenue / $10,000 spend = 5.0x ROAS

**True ROAS adjustments**:
- Subtract returns: -$5,000
- Subtract refunds: -$2,500
- Subtract chargebacks: -$500
- Subtract COGS: -$15,000
- Adjusted revenue: $27,000

**True ROAS**: $27,000 / $10,000 = 2.7x (not the 5.0x on your dashboard)

**Action**: Calculate True ROAS for the last 90 days across all channels. This is your reality check.

### Step 2: Calculate LTV by Cohort

Customer Lifetime Value is not a single number. It varies by acquisition source, time period, and customer segment.

**Cohort definition**: Group customers by acquisition month and source.

**LTV calculation per cohort**:
- 30-day LTV: Revenue from customer in first 30 days (initial purchase + upsells)
- 60-day LTV: Cumulative revenue through day 60 (add repeat purchases, subscriptions)
- 90-day LTV: Cumulative revenue through day 90
- 12-month LTV: Full annual value

**Example cohort analysis**:
- Meta Jan cohort: 30-day LTV = $85, 90-day LTV = $142, 12-month LTV = $310
- Google Jan cohort: 30-day LTV = $120, 90-day LTV = $165, 12-month LTV = $280
- Meta acquires cheaper customers but Google acquires higher immediate value. At 12 months, Meta wins.

**Action**: Build LTV curves for each acquisition channel for the last 4 cohorts.

### Step 3: Determine Acceptable nCAC

Based on LTV and your business's payback period requirements, calculate the maximum you can afford to pay for a new customer.

**The nCAC formula**:
Acceptable nCAC = LTV x Target Margin - Fixed Costs Per Customer

**Payback period consideration**:
- If you need to break even in 30 days: nCAC must be less than 30-day LTV minus COGS
- If you can wait 90 days: nCAC can be up to 90-day LTV minus COGS
- If you have funding/cash reserves: nCAC can stretch toward 12-month LTV

**Example**:
- 90-day LTV: $142
- COGS per customer: $35
- Gross margin per customer: $107
- Target profit margin: 30%
- Acceptable nCAC: $107 x 0.70 = $74.90

**Action**: Define acceptable nCAC at 30, 60, and 90-day payback periods.

### Step 4: Set nCAC Targets by Channel

Each channel acquires different quality customers at different costs. Set channel-specific targets.

**Channel target framework**:
- Meta (Prospecting): nCAC target based on cold traffic LTV cohort
- Meta (Retargeting): Lower nCAC target (warmer audience, should convert cheaper)
- Google Search (Brand): Lowest nCAC target (highest intent)
- Google Search (Non-Brand): nCAC target based on search-acquired LTV cohort
- YouTube: nCAC target based on video-acquired LTV cohort
- TikTok: nCAC target based on TikTok-acquired LTV cohort

**Important**: Do not apply the same nCAC target to all channels. A channel that acquires higher-LTV customers deserves a higher nCAC allowance.

**Action**: Set specific nCAC targets for each active channel based on cohort LTV data.

### Step 5: Optimize to nCAC, Not ROAS

Shift your optimization lens from ROAS to nCAC.

**Daily/weekly optimization**:
- Monitor nCAC by channel against targets
- If nCAC is below target: scale spend (the channel is acquiring profitably)
- If nCAC is at target: maintain spend and test for improvement
- If nCAC is above target: diagnose cause (creative fatigue, audience saturation, funnel leak)

**Reporting shift**:
- Replace ROAS dashboard with nCAC dashboard
- Include LTV projections alongside current nCAC
- Track nCAC trend over time (is it rising, stable, or falling?)
- Compare nCAC across channels for budget allocation decisions

**Blended nCAC**:
Total ad spend across all channels / Total new customers acquired = Blended nCAC.
This is your north star metric for overall acquisition health.

## Key Concepts

- **ROAS is a vanity metric**: It does not account for returns, refunds, COGS, or customer quality
- **nCAC connects to profitability**: It answers "how much does it actually cost to acquire a customer who stays?"
- **LTV by cohort is essential**: Average LTV hides critical differences between channels and time periods
- **Payback period matters**: A business with 12-month cash reserves can accept higher nCAC than one needing 30-day payback
- **Channel-specific targets**: Different channels deserve different nCAC targets based on the customer quality they deliver

## Decision Rules

- IF ROAS looks great but refund rate exceeds 10% THEN calculate True ROAS before celebrating
- IF nCAC is below target THEN increase budget by 20% and monitor for 5 days
- IF nCAC is above target for 7+ days THEN diagnose: is it creative fatigue, audience saturation, or funnel leak?
- IF one channel has 2x the nCAC of another THEN compare LTV cohorts before cutting -- it may still be profitable
- IF blended nCAC is rising month-over-month THEN audit the highest-spend channels first
- IF you do not have LTV data THEN start tracking now and use 30-day proxy data until you have 90+ days

## Common Mistakes

- Optimizing to ROAS and celebrating campaigns that acquire low-quality customers
- Using a single nCAC target across all channels -- channels have different customer profiles
- Not accounting for returns and refunds in acquisition cost calculations
- Ignoring payback period -- acquiring profitably at 12-month LTV means nothing if you run out of cash at month 3
- Setting nCAC targets once and never updating them as LTV data matures
- Conflating new customer acquisition with returning customer revenue in ROAS calculations

## Integration

- nCAC targets feed optimization decisions in **pittman-traffic-engine-9-steps.md** Step 8
- LTV by cohort informs budget allocation in **burns-conversion-engine.md** Pillar 2
- nCAC is a lagging indicator in **burns-mpi.md**
- True ROAS calculation is part of the **burns-sgp-30-60-90.md** 111-point audit
- Post-purchase quality connects to **burns-caamp.md** System 3 (Operations)
- Customer quality by source informs audience strategy in **pittman-traffic-temperature.md**

## Output

- True ROAS calculation replacing dashboard ROAS
- LTV cohort analysis by channel for last 4 acquisition periods
- Acceptable nCAC targets at 30, 60, and 90-day payback periods
- Channel-specific nCAC targets with justification
- nCAC tracking dashboard replacing or supplementing ROAS dashboard
- Monthly nCAC trend report with scaling or diagnostic actions
