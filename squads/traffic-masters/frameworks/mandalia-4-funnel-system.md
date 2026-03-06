# 4-Funnel System

> **Author**: Depesh Mandalia
> **Domain**: Account Structure and Campaign Architecture
> **Used by agents**: media-buyer, strategy-orchestrator, funnel-strategist
> **Checklists**: account-structure-checklist, funnel-audit-checklist

## Overview

The 4-Funnel System is Depesh Mandalia's account structure framework that organizes campaigns by customer journey stage. Rather than mixing cold prospecting with retargeting in the same campaign, each funnel has its own budget, creative strategy, optimization goals, and KPIs. This creates clarity, prevents budget leakage between stages, and ensures each audience segment receives stage-appropriate messaging.

## When to Use

- Setting up a new ad account from scratch
- Restructuring a messy account with no clear organization
- When retargeting budget is being cannibalized by prospecting campaigns
- Account audit reveals no clear separation between cold, warm, and hot audiences
- Scaling requires clear visibility into performance by funnel stage

## The Framework

### Funnel 1: Cold Prospecting
1. **Audience**: Broad targeting, lookalike audiences, interest-based targeting
2. **Purpose**: Introduce the brand to new potential customers
3. **Creative strategy**: Education, entertainment, value-first content, awareness ads
4. **Optimization goal**: Link clicks, landing page views, or top-of-funnel conversions
5. **Budget allocation**: 50-60% of total ad budget
6. **KPIs**: CPM, CTR, CPC, cost per landing page view, cost per new visitor
7. **Exclusions**: Exclude all website visitors, email lists, past purchasers
8. **Testing**: This is where graduation testing happens — new creative enters here

### Funnel 2: Warm Engagement
1. **Audience**: Website visitors (non-converters), video viewers (25-95%), page engagers, post engagers
2. **Purpose**: Deepen relationship with people who have shown interest
3. **Creative strategy**: Social proof, testimonials, deeper education, behind-the-scenes
4. **Optimization goal**: Content views, engagement, add-to-cart, lead form opens
5. **Budget allocation**: 15-20% of total ad budget
6. **KPIs**: Engagement rate, cost per engagement, website return rate, ATC rate
7. **Exclusions**: Exclude purchasers/converters, exclude Funnel 3 audiences
8. **Note**: This funnel builds the retargeting pool for Funnel 3

### Funnel 3: Hot Conversion
1. **Audience**: Add-to-cart, initiate checkout, lead form submitters, pricing page visitors
2. **Purpose**: Close the deal with high-intent prospects
3. **Creative strategy**: Urgency, scarcity, risk reversal, direct offers, objection handling
4. **Optimization goal**: Purchases, completed leads, sign-ups
5. **Budget allocation**: 15-20% of total ad budget
6. **KPIs**: CPA, ROAS, conversion rate, cost per purchase
7. **Exclusions**: Exclude purchasers/converters
8. **Note**: Infinity Retargeting system operates primarily in Funnels 2 and 3

### Funnel 4: Post-Purchase
1. **Audience**: Past purchasers, existing customers, subscribers
2. **Purpose**: Maximize lifetime value through upsells, cross-sells, retention, referrals
3. **Creative strategy**: Loyalty content, exclusive offers, new product announcements, referral programs
4. **Optimization goal**: Repeat purchases, upsell conversions, referral actions
5. **Budget allocation**: 5-10% of total ad budget
6. **KPIs**: Repeat purchase rate, LTV increase, referral rate, upsell conversion rate
7. **Segmentation**: Segment by purchase recency, frequency, and value (RFV)
8. **Note**: Most neglected funnel — often delivers the highest ROAS

### Account Structure Rules
- Each funnel is a separate campaign (or campaign group)
- Never mix funnel audiences within the same campaign
- Exclusions between funnels prevent audience overlap and self-competition
- Budget allocation ratios can shift as the account matures (more to Funnel 4 over time)

## Key Concepts

- **Budget isolation**: Each funnel controls its own budget — no leakage between stages
- **Stage-appropriate messaging**: Cold audiences need education, hot audiences need urgency
- **Exclusion hygiene**: Without proper exclusions, you pay to show retargeting ads as prospecting (inflated metrics)
- **Funnel 4 is the profit center**: Selling to existing customers is 5-7x cheaper than acquiring new ones
- **Pipeline flow**: Funnel 1 feeds Funnel 2, which feeds Funnel 3, which feeds Funnel 4

## Decision Rules

- IF Funnel 1 CPM is rising sharply THEN audiences are saturated — refresh targeting or expand
- IF Funnel 2 is not generating enough ATC/IC volume THEN Funnel 1 traffic quality is poor
- IF Funnel 3 conversion rate is low THEN either the offer is weak or Funnel 2 did not warm them enough
- IF Funnel 4 has no budget allocated THEN you are leaving the highest-ROAS opportunity untapped
- IF overall CPA is too high THEN check Funnel 1 allocation — it may be consuming too much without converting downstream
- IF Funnel 2 and 3 audiences are tiny THEN Funnel 1 budget needs to increase to fill the pipeline

## Common Mistakes

- Running all audiences in one campaign and letting the algorithm allocate (it will favor cheap clicks, not conversions)
- No exclusions between funnels (paying prospecting CPMs for retargeting audiences)
- Ignoring Funnel 4 entirely (missing the cheapest conversions in the account)
- Using the same creative across all funnels (message mismatch kills conversion)
- Allocating too little to Funnel 1 (starving the top of the pipeline)
- Not updating audience definitions as website and engagement data grows

## Integration

- Depends on: mandalia-bpm-method (Funnel 1 has more Brand weight, Funnels 2-3 are Performance-heavy)
- Feeds into: mandalia-scaling-recipes (each funnel scales using different recipes)
- Feeds into: mandalia-infinity-retargeting (Funnels 2 and 3 are the retargeting layer)
- Connects to: kusmich-ponds-lakes-oceans (Funnel 1 audience size maps to pond/lake/ocean)
- Connects to: kusmich-milestone-content (content milestones map to funnel stages)

## Output

- Complete account structure with campaigns organized by funnel
- Audience definitions and exclusion rules for each funnel
- Budget allocation plan with ratios and absolute amounts
- KPI dashboard organized by funnel with appropriate metrics per stage
- Creative brief for each funnel specifying messaging tone and strategy
