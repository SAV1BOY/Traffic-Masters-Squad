# Creative Production Sprint

> **Type**: Task
> **Category**: creative
> **Agents**: Ad Midas, Creative Analyst
> **Frameworks**: Kaizen Kreative, Creative Sprint Methodology
> **Checklists**: creative-production-checklist
> **Output template**: templates/creative-assets.md

## ROUTING (from config.yaml)

> **Config key**: `routing.creative-production-sprint`
> **Agents**: [ad-midas](../../agents/ad-midas.md), [creative-analyst](../../agents/creative-analyst.md)
> **Frameworks**: `creative-production-pipeline`, `burns-kaizen-kreative`, `creative-angle-matrix`
> **Checklists**: `creative-brief-quality`, `creative/thumb-first-frame-quality`, `creative/claim-proof-compliance`
> **Templates**: `briefs/creative-brief`, `briefs/ugc-creator-brief`
> **Registry**: `data/registries/creatives-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Execute a focused creative production sprint to produce a batch of ad creative assets across multiple formats and angles, ready for campaign deployment and testing.

## Inputs
- Creative strategy with prioritized backlog
- Approved scripts and UGC briefs
- Brand assets: logos, fonts, colors, product images, lifestyle photos
- Platform-specific format requirements and specs
- Hook and angle combinations to produce
- Performance data from previous creatives (for iteration sprints)

## Steps
1. Select sprint scope: number of creatives, formats, and angles to produce
2. Pull briefs from the creative backlog prioritized by strategic importance
3. Produce static image ads: design variations with headline, visual, and CTA testing
4. Produce carousel ads: multi-frame storytelling with consistent visual theme
5. Produce motion graphics: animated versions of top static concepts
6. Edit video ads from raw footage or UGC submissions per approved scripts
7. Create platform-specific adaptations: resize, reformat, adjust for Meta, TikTok, YouTube, Stories
8. Apply text overlays, captions, and CTAs to video assets
9. Build ad copy variations for each creative: primary text, headline, description
10. Run internal creative review against brand guidelines and policy requirements
11. Organize assets with naming conventions: angle_format_variant_platform
12. Upload to shared asset library with metadata tags for searchability

## Output
Creative assets batch containing: final production files per format and platform, ad copy document with variations, asset naming reference, metadata tags, and production notes for iteration guidance.

## Quality Gate
- Creative production checklist confirms all assets meet platform specs
- Creative Analyst reviews for brand consistency and message clarity
- All assets pass policy pre-check before campaign upload

## Duration
1-3 days per sprint depending on volume; review cycle adds 2-4 hours
