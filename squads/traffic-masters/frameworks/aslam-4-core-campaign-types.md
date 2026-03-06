# 4 Core Campaign Types Framework
> **Author**: Kasim Aslam / Google Ads Structure
> **Domain**: Google Ads, Campaign Architecture, Budget Allocation
> **Used by agents**: google-ads-agent, campaign-planner-agent, media-buyer-agent

## Overview
A non-negotiable campaign structure for Google Ads accounts. Every account should have
four campaign types with specific budget allocations: Brand (10%), Competitor (15%),
Remarketing (25%), and General (50%). This structure ensures coverage across all intent
levels while protecting brand terms and capturing competitor traffic.

## When to Use
- Setting up a new Google Ads account from scratch
- Restructuring an underperforming account
- Auditing existing campaign architecture
- Scaling an account that currently runs only one or two campaign types

## The Framework
### 1. Brand Campaigns (10% of budget)
- Target: Your own brand name and variations
- Match types: Exact and phrase match on brand terms
- Purpose: Protect brand traffic from competitors, control messaging
- Expected CPC: Lowest in account
- Expected CVR: Highest in account
- Non-negotiable: Always run brand campaigns, even with strong organic

### 2. Competitor Campaigns (15% of budget)
- Target: Competitor brand names and product names
- Match types: Exact match on competitor terms
- Purpose: Intercept prospects actively comparing solutions
- Expected CPC: Higher than brand, lower than general
- Expected CVR: Moderate — these prospects are shopping
- Note: Ad copy cannot use competitor trademarks — focus on differentiation

### 3. Remarketing Campaigns (25% of budget)
- Target: Past visitors, cart abandoners, video viewers, email lists
- Audience segments: 1-7 day, 8-14 day, 15-30 day, 31-90 day
- Purpose: Re-engage warm audiences with tailored messaging
- Expected CPC: Moderate
- Expected CVR: High — these audiences already know you
- Key: Frequency cap and message sequencing by recency

### 4. General Campaigns (50% of budget)
- Target: Non-branded, high-intent search terms
- Match types: Start exact/phrase, expand to broad with data
- Purpose: Capture new demand from prospects searching for solutions
- Expected CPC: Highest in account
- Expected CVR: Lowest but highest volume potential
- Key: Aggressive negative keyword management

## Key Concepts
- This structure is non-negotiable — all four types must exist
- Budget percentages are starting points; adjust based on data after 30 days
- Brand campaigns are cheap insurance — never cut them to save budget
- Competitor campaigns require careful ad copy to avoid trademark violations
- General campaigns are where most new customer acquisition happens
- Remarketing is the highest-ROI campaign type in most accounts

## Decision Rules
- IF account is new → launch all four types simultaneously
- IF budget is very limited (<$1000/mo) → prioritize Brand + Remarketing first
- IF brand CPCs spike → check for competitor bidding on your terms
- IF General CVR is too low → tighten match types and add negatives
- IF Remarketing frequency is too high → adjust caps and refresh creative

## Common Mistakes
- Running only General campaigns and ignoring Brand protection
- Not separating Competitor campaigns from General — muddies data
- Allocating too much budget to General before Remarketing is optimized
- Using the same ad copy across all four campaign types
- Cutting Brand campaigns because organic ranking is strong

## Integration
- Feeds into: Aslam Manual CPC First (bidding strategy per campaign type)
- Pairs with: Aslam You vs. Google (structured independence from defaults)
- Complements: Retargeting Architecture (Remarketing campaign structure)
- Source data: KPI Tree Acquisition (performance benchmarks per type)

## Output
- A four-campaign account structure with budget allocation
- Keyword lists and match type assignments per campaign type
- Ad copy guidelines specific to each campaign type
- Performance benchmarks and optimization triggers per type
