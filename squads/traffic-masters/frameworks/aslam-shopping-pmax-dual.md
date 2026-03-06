# Shopping + PMax Dual Strategy Framework
> **Author**: Kasim Aslam / Google Shopping & PMax
> **Domain**: Google Ads, E-commerce, Shopping Campaigns
> **Used by agents**: google-ads-agent, ecommerce-agent, media-buyer-agent

## Overview
Run Standard Shopping and Performance Max campaigns simultaneously. Standard Shopping
provides control and transparency. PMax provides reach and automation. They serve
different purposes and should not be treated as either/or. Different ROAS targets
prevent cannibalization, and brand exclusions keep PMax honest.

## When to Use
- E-commerce accounts with product feeds
- When PMax alone lacks transparency and control
- When Standard Shopping alone misses incremental reach
- Scaling e-commerce ad spend beyond a single campaign type

## The Framework
### Standard Shopping Campaign
- Role: Control campaign — your foundation
- Targeting: Product groups with manual bids or tROAS
- ROAS target: Higher than PMax (e.g., 400% if PMax is 300%)
- Benefits: Full search term visibility, product-level control, bid transparency
- Structure: Segment by product category, margin tier, or performance tier
- Priority: High priority setting to capture traffic first

### Performance Max Campaign
- Role: Amplifier campaign — incremental reach
- Targeting: Automated across all Google surfaces
- ROAS target: Lower than Shopping (accepts wider funnel traffic)
- Benefits: Access to YouTube, Display, Discover, Gmail, Maps
- Structure: Group by product theme or audience signal
- Brand exclusion: Exclude brand terms from PMax (critical)

### Dual Strategy Rules
- Shopping captures high-intent search traffic with control
- PMax captures everything else across Google's network
- Different ROAS targets prevent them from competing for the same traffic
- Brand exclusion from PMax ensures brand conversions credit Shopping
- Monitor overlap: if Shopping volume drops after PMax launch, adjust

## Key Concepts
- PMax without Shopping is flying blind — no search term data
- Shopping without PMax misses YouTube, Display, and Discovery traffic
- Brand traffic in PMax inflates its reported performance
- The dual strategy gives you both control (Shopping) and scale (PMax)
- Product feed quality is critical for both — invest in feed optimization
- Asset groups in PMax need strong creative signals to perform

## Decision Rules
- IF launching e-commerce ads → start with Shopping, add PMax after 30 days
- IF PMax ROAS looks too good → check if brand terms are included
- IF Shopping volume drops after PMax launch → PMax is cannibalizing
- IF total account ROAS meets target → dual strategy is working
- IF budget is limited → prioritize Shopping over PMax
- IF product catalog is large (500+) → segment Shopping by margin tier

## Common Mistakes
- Running PMax without brand exclusions and celebrating inflated ROAS
- Replacing Standard Shopping entirely with PMax (losing control)
- Setting the same ROAS target for both (causes cannibalization)
- Not monitoring overlap between the two campaign types
- Poor product feed quality undermining both campaign types
- Ignoring asset group creative quality in PMax

## Integration
- Feeds into: Aslam You vs. Google (PMax is Google's preferred — question it)
- Pairs with: Aslam Manual CPC First (Shopping can start manual)
- Complements: Aslam 4 Core Campaign Types (Shopping+PMax = part of structure)
- Source data: Tracking Stack Standard (conversion accuracy for ROAS)

## Output
- A dual campaign structure with Shopping and PMax specifications
- ROAS targets differentiated by campaign type
- Brand exclusion list for PMax
- Product feed optimization checklist
- Overlap monitoring dashboard requirements
