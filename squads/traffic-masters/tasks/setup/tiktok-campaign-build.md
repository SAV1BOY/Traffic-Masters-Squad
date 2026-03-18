# TikTok Campaign Build

> **Type**: Task
> **Category**: setup
> **Agents**: Media Buyer, Ad Midas
> **Frameworks**: TikTok Native Creative Strategy, Spark Ads Framework
> **Checklists**: tiktok-campaign-build-checklist
> **Output template**: templates/tiktok-build-sheet.md

## ROUTING (from config.yaml)

> **Config key**: `routing.tiktok-campaign-build`
> **Agents**: [media-buyer](../../agents/media-buyer.md), [ad-midas](../../agents/ad-midas.md)
> **Frameworks**: `creative-angle-matrix`
> **Checklists**: `campaign-build-quality`, `tiktok/tiktok-creative-native-quality`, `tiktok/tiktok-event-tracking-quality`
> **Templates**: `ads/tiktok-ugc-ad-template`
> **Registry**: `data/registries/campaigns-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Build TikTok advertising campaigns with native-feeling creative, proper event setup, audience targeting, and bidding configuration to reach younger and engaged audiences through platform-native content formats.

## Inputs
- TikTok-native video creative assets (vertical 9:16)
- TikTok Business Center and Ads Manager access
- TikTok pixel and Events API setup confirmation
- Audience definitions: interests, behaviors, custom audiences, lookalikes
- Budget allocation for TikTok campaigns
- Landing page URLs optimized for mobile

## Steps
1. Set up TikTok pixel and Events API with proper event mapping
2. Create campaign structure: separate prospecting and retargeting campaigns
3. Select campaign objective: traffic, conversions, lead generation, or app installs
4. Build ad groups with interest and behavior targeting aligned to avatar
5. Configure custom audiences from pixel data, customer lists, and engagement
6. Create lookalike audiences from converters at 1-5% similarity ranges
7. Upload native creative assets emphasizing authenticity and platform style
8. Set up Spark Ads using organic posts with strong engagement (if available)
9. Configure bidding: lowest cost for learning phase, then cost cap for efficiency
10. Set frequency and budget pacing controls
11. Apply UTM parameters and tracking templates to all destination URLs
12. Enable TikTok-specific features: dynamic creative optimization, automated creative optimization

## Output
Live TikTok campaigns with: campaign structure documentation, event tracking verification, audience targeting specs, creative assignments with native format validation, bidding settings, and Spark Ads configuration.

## Quality Gate
- TikTok campaign build checklist confirms all elements configured
- Ad Midas validates creative feels native to TikTok platform style
- Pixel and Events API verified with test events before launch

## Duration
3-5 hours for build; 1-2 hours for QA and creative review
