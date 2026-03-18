# Search Query Mining

> **Type**: Task
> **Category**: optimization
> **Agents**: Aslam, Media Buyer
> **Frameworks**: Search Query Optimization Framework, Negative Keyword Strategy
> **Checklists**: search-query-mining-checklist
> **Output template**: templates/negative-keyword-list.md

## ROUTING (from config.yaml)

> **Config key**: `routing.search-query-mining`
> **Agents**: [kasim-aslam](../../agents/kasim-aslam.md), [media-buyer](../../agents/media-buyer.md)
> **Frameworks**: `aslam-4-core-campaign-types`
> **Checklists**: `aslam/aslam-search-query-hygiene`
> **Templates**: N/A
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Mine search query reports to identify irrelevant queries consuming budget, discover new keyword opportunities, refine match type strategy, and maintain a comprehensive negative keyword list that improves campaign efficiency.

## Inputs
- Google Ads search terms reports for the analysis period
- Microsoft Ads search terms reports (if applicable)
- Current negative keyword lists at campaign and account levels
- Keyword map with intended targeting
- Conversion data linked to search queries
- Budget waste thresholds: cost per query without conversion

## Steps
1. Export search terms reports for all active Search and Shopping campaigns
2. Sort queries by spend to identify highest-cost terms first
3. Flag queries with significant spend but zero conversions for negative keyword review
4. Identify irrelevant query patterns: wrong intent, wrong product, wrong audience
5. Check for brand term leakage into non-brand campaigns and vice versa
6. Discover new converting queries not currently targeted as keywords
7. Analyze query-to-keyword match type behavior: are broad match terms triggering off-topic
8. Build negative keyword additions organized by campaign or shared list
9. Select match type for each negative: exact, phrase, or broad match negative
10. Identify queries suggesting new ad group or campaign opportunities
11. Calculate budget saved from previous negative keyword additions
12. Update the master negative keyword list and apply changes to campaigns

## Output
Negative keyword list update containing: new negatives with match types, query performance analysis, budget waste quantification, new keyword opportunities discovered, match type recommendations, and cumulative savings tracking.

## Quality Gate
- Search query mining checklist confirms all campaigns reviewed for the period
- No high-spend zero-conversion queries left unaddressed
- Aslam validates negative keyword additions will not block valuable traffic

## Duration
1-3 hours depending on campaign volume and query data size
