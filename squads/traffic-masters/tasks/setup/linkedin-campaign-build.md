# LinkedIn Campaign Build

> **Type**: Task
> **Category**: setup
> **Agents**: Media Buyer
> **Frameworks**: LinkedIn B2B Campaign Architecture, ABM Targeting Strategy
> **Checklists**: linkedin-campaign-build-checklist
> **Output template**: templates/linkedin-build-sheet.md

## ROUTING (from config.yaml)

> **Config key**: `routing.linkedin-campaign-build`
> **Agents**: [media-buyer](../../agents/media-buyer.md)
> **Frameworks**: `omnichannel-media-strategy`
> **Checklists**: `campaign-build-quality`, `linkedin/linkedin-targeting-quality`, `linkedin/linkedin-leadgen-forms-quality`
> **Templates**: `ads/linkedin-b2b-ad-template`
> **Registry**: `data/registries/campaigns-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Build LinkedIn advertising campaigns with B2B-specific targeting, lead form integration, professional creative formats, and bidding strategy to reach decision-makers and generate qualified B2B leads.

## Inputs
- LinkedIn Campaign Manager account access
- B2B audience definitions: job titles, seniority, industries, company sizes
- Creative assets: single image, carousel, video, document ads
- Lead gen form configuration or landing page URLs
- Budget allocation for LinkedIn campaigns
- LinkedIn Insight Tag installed and verified

## Steps
1. Install and verify LinkedIn Insight Tag for conversion tracking
2. Create campaign structure by objective: brand awareness, lead generation, website conversions
3. Build audience targeting using LinkedIn-specific facets: job title, function, seniority, industry, company size
4. Create matched audiences from website visitors, contact lists, and account lists for ABM
5. Build lookalike audiences from customer lists or high-value converters
6. Configure Lead Gen Forms with progressive profiling fields
7. Upload creative assets optimized for LinkedIn feed: professional tone, value-driven messaging
8. Set up sponsored content, message ads, or conversation ads per campaign objective
9. Configure bidding strategy: manual CPC for control, or automated bidding for scale
10. Set daily budgets and campaign duration with pacing monitoring
11. Apply audience exclusions: existing customers, competitors, internal employees
12. Set up UTM parameters and CRM integration for lead tracking

## Output
Live LinkedIn campaigns with: campaign structure documentation, B2B audience targeting specs, lead form configurations, creative assignments, bidding settings, CRM integration details, and audience exclusion rules.

## Quality Gate
- LinkedIn campaign build checklist confirms all B2B targeting elements configured
- Lead Gen Forms tested with sample submissions reaching CRM
- Insight Tag verified firing on all relevant pages

## Duration
3-5 hours for build; 1-2 hours for QA and CRM integration testing
