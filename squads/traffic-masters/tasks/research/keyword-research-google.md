# Keyword Research for Google

> **Type**: Task
> **Category**: research
> **Agents**: Aslam, Ads Analyst
> **Frameworks**: Google Keyword Strategy, Search Intent Mapping
> **Checklists**: keyword-research-checklist
> **Output template**: templates/keyword-map.md

## ROUTING (from config.yaml)

> **Config key**: `routing.keyword-research-google`
> **Agents**: [kasim-aslam](../../agents/kasim-aslam.md), [ads-analyst](../../agents/ads-analyst.md)
> **Frameworks**: `aslam-4-core-campaign-types`
> **Checklists**: `aslam/aslam-search-query-hygiene`
> **Templates**: N/A
> **Registry**: `data/research/keyword-research`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Conduct comprehensive keyword research for Google Ads campaigns covering search volume, intent classification, competition analysis, cost estimates, and negative keyword identification to build a structured keyword map.

## Inputs
- Product or service descriptions and key features
- Competitor domain list for auction insights
- Landing page URLs for relevance mapping
- Business goals: target CPA, ROAS, or lead volume
- Geographic targeting parameters

## Steps
1. Brainstorm seed keywords from product features, benefits, and customer language
2. Expand seed list using Google Keyword Planner, competitor analysis, and autocomplete suggestions
3. Pull search volume, CPC estimates, and competition level for all keywords
4. Classify each keyword by intent: informational, navigational, commercial, transactional
5. Group keywords into thematic ad groups based on intent and topic similarity
6. Identify high-value long-tail keywords with strong commercial intent
7. Research competitor keyword coverage using auction insights and SERP analysis
8. Build negative keyword list from irrelevant terms, informational queries, and competitor brand terms
9. Map keywords to landing pages ensuring relevance alignment
10. Estimate budget requirements based on volume and CPC data
11. Prioritize keyword groups by expected ROI and strategic importance

## Output
Keyword map containing: keyword groups with volume and CPC data, intent classifications, ad group structure recommendations, negative keyword list, keyword-to-landing-page mapping, budget estimates per group, and priority rankings.

## Quality Gate
- Keyword research checklist confirms minimum coverage thresholds met
- All keywords classified by intent with ad group assignments
- Aslam validates keyword grouping logic and negative keyword completeness

## Duration
4-6 hours for research and classification; 1-2 hours for mapping and documentation
