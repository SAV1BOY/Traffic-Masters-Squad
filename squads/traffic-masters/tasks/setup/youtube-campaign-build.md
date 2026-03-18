# YouTube Campaign Build

> **Type**: Task
> **Category**: setup
> **Agents**: Breeze, Media Buyer
> **Frameworks**: YouTube Ads Architecture, ADUCATE Script Framework
> **Checklists**: youtube-campaign-build-checklist
> **Output template**: templates/youtube-build-sheet.md

## ROUTING (from config.yaml)

> **Config key**: `routing.youtube-campaign-build`
> **Agents**: [tom-breeze](../../agents/tom-breeze.md), [media-buyer](../../agents/media-buyer.md)
> **Frameworks**: `breeze-aducate`, `breeze-3-acts`, `breeze-5as-readiness`, `youtube-ads-structure`
> **Checklists**: `campaign-build-quality`, `youtube/yt-campaign-setup-quality`, `youtube/yt-creative-hook-5s`, `breeze/breeze-aducate-script-audit`
> **Templates**: `ads/youtube-ad-script-aducate`, `briefs/video-ad-brief`
> **Registry**: `data/registries/campaigns-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Build YouTube advertising campaigns with proper format selection, targeting configuration, video creative assignments, bidding strategy, and companion elements to drive awareness, consideration, or direct response actions.

## Inputs
- Video creative assets: skippable in-stream, bumper, in-feed, Shorts
- Audience definitions: custom intent, affinity, in-market, remarketing, placements
- Landing page URLs with tracking parameters
- Budget allocation for YouTube campaigns
- Conversion tracking setup verified for video campaigns
- Companion banner assets (300x60 for in-stream)

## Steps
1. Select campaign sub-types based on objectives: Video reach, Video views, or Video action
2. Create campaign structure separating prospecting from retargeting
3. Build ad groups with audience targeting: custom intent keywords, affinity, in-market, placements
4. Configure placement targeting for relevant YouTube channels and videos (if applicable)
5. Upload video ads and associate with proper ad groups
6. Create companion banners for in-stream ads
7. Set bidding strategy: target CPV for awareness, target CPA for action campaigns
8. Configure frequency capping to prevent over-exposure
9. Apply content exclusion settings for brand safety
10. Set up remarketing audiences from video interactions: viewers, subscribers, likes
11. Configure UTM parameters and tracking templates for all destination URLs
12. Set geographic, demographic, and device targeting per campaign

## Output
Live YouTube campaigns with: campaign structure documentation, audience targeting specs, video creative assignments, bidding configuration, frequency caps, brand safety settings, and remarketing audience setup.

## Quality Gate
- YouTube campaign build checklist confirms all elements configured
- Breeze validates video creative meets platform best practices (hook in first 5 seconds)
- Conversion tracking verified for all campaign action types

## Duration
3-5 hours for build; 1-2 hours for QA and verification
