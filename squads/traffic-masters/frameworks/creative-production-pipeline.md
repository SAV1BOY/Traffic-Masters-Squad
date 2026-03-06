# Creative Production Pipeline

> **Type**: Internal
> **Domain**: Creative Operations — Production Workflow
> **Used by agents**: Ad Midas, Creative Analyst, Breeze, Traffic Chief, Media Buyer

## Overview

A stage-gated production pipeline that takes creative concepts from research through launch. Defines timelines, roles, quality gates, and volume targets. Creative is the primary lever in modern paid media — algorithms optimize delivery, but creative determines who engages. This pipeline ensures consistent output at the volume required for testing and scaling.

## When to Use

- Monthly creative production cycles (ongoing)
- New client onboarding — first creative batch
- Creative refresh when fatigue is detected
- Scaling phases requiring increased creative volume
- New platform or format expansion requiring net-new assets

## The Framework

### Pipeline Stages

| Stage | Duration | Owner | Output |
|-------|----------|-------|--------|
| 1. Research | 5-7 days | Ad Midas, Creative Analyst | Insights document, angle opportunities |
| 2. Brief | 1 day | Ad Midas | Creative briefs (one per concept) |
| 3. Concept | 2 days | Ad Midas, Breeze | Concept decks with hook, angle, format, CTA |
| 4. Production | 3-5 days | Creative team / UGC creators | Raw assets — video, images, copy |
| 5. Variations | 2 days | Creative team | Format adaptations, text overlays, cuts |
| 6. QA | 1 day | Creative Analyst, Ads Analyst | Policy check, brand check, tech spec check |
| 7. Launch | 1 day | Media Buyer | Upload, configure tracking, activate |

**Total Cycle**: 15-19 days from research start to live ads.

### Stage 1: Research (Days 1-7)

**Activities**:
- Review competitor ads (Meta Ad Library, Google Ads Transparency).
- Analyze top-performing existing ads (by CTR, CVR, ROAS).
- Review customer feedback, reviews, support tickets for language mining.
- Check `hook-library-system.md` for proven patterns.
- Identify trending formats on target platforms.
- Populate `creative-angle-matrix.md` with new concepts.

**Output**: Research document with competitive landscape, performance insights, customer language goldmine, and recommended angles.

### Stage 2: Brief (Day 8)

**Brief Template**:
- Objective (awareness / consideration / conversion)
- Target audience segment
- Angle and hook (from matrix)
- Key message and supporting points
- Format and platform specifications
- CTA and destination URL
- Policy risk classification (Green / Yellow / Red)
- Reference assets or inspiration
- Mandatory brand elements

One brief per concept. Minimum 10 briefs per production cycle.

### Stage 3: Concept (Days 9-10)

**Activities**:
- Develop full concept from brief — storyboard for video, layout for static.
- Write scripts (video) or copy variations (static).
- Select format: UGC, produced video, static, carousel, motion graphic.
- Internal review — Ad Midas and Breeze align on creative direction.
- Policy pre-check on any Yellow/Red classified concepts.

**Output**: Concept deck with visual mockups, scripts, and production notes.

### Stage 4: Production (Days 11-15)

**Activities**:
- Video shooting or UGC creator production (per `ugc-creator-framework.md`).
- Graphic design for static and carousel assets.
- Copywriting for all text elements — headlines, primary text, descriptions.
- Voiceover recording if applicable.
- Stock footage/image sourcing if needed.

**Volume Target**: Minimum 10 concepts per month per client. Each concept generates 3-5 variations.

### Stage 5: Variations (Days 16-17)

**Activities**:
- Aspect ratio adaptations: 1:1, 4:5, 9:16, 16:9.
- Text overlay variations (different hooks on same visual).
- Thumbnail variations for video.
- Copy variations — 3 primary text versions per ad.
- Headline variations — 5 per ad minimum.
- CTA button testing versions.

**Output**: Full asset package per concept — minimum 3 variations ready for testing.

### Stage 6: QA (Day 18)

**QA Checklist**:
- [ ] Policy risk classification confirmed — no Red without approval
- [ ] Brand guidelines followed (colors, fonts, logos, tone)
- [ ] Technical specifications met (file size, resolution, duration, aspect ratio)
- [ ] Copy proofread — no typos, broken URLs, or placeholder text
- [ ] CTA matches landing page destination
- [ ] Tracking parameters (UTMs) embedded in all destination URLs
- [ ] Mobile preview checked — text readable, CTA visible
- [ ] Sound-off test for video — message clear without audio
- [ ] Disclaimers present where required

### Stage 7: Launch (Day 19)

**Activities**:
- Upload assets to ad platforms.
- Configure ad-level settings (tracking, CTA buttons, display URLs).
- Verify pixel firing on destination pages.
- Set up naming conventions per account structure framework.
- Activate campaigns and confirm delivery within 2 hours.

## Key Concepts

- **Creative Velocity**: The number of new concepts tested per month. Minimum target: 10 concepts/month for accounts spending $10K+/month. Scale to 20+ for $50K+/month.
- **Iteration Over Invention**: 70% of production should be variations on proven concepts. 30% net-new exploration.
- **The 3x Rule**: Every concept needs minimum 3 variations to generate statistically meaningful test data.
- **Format Diversification**: Each production cycle should include at least 3 different formats (video, static, carousel, UGC).

## Decision Rules

1. No creative launches without completing QA stage — zero exceptions.
2. Research stage cannot be skipped even under time pressure — shorten to 3 days minimum.
3. Brief approval required from Ad Midas before production begins.
4. If production falls behind schedule, reduce concept count rather than skipping stages.
5. UGC content follows parallel timeline per `ugc-creator-framework.md`.
6. Emergency creative (reactive to trends or competitor moves) follows expedited 5-day pipeline.

## Common Mistakes

- Skipping research and briefing — producing creative based on assumptions.
- Not creating enough variations — launching single versions and declaring winners/losers prematurely.
- Ignoring QA — typos, wrong URLs, and policy violations damage account health.
- Producing all one format — algorithm and audience fatigue set in faster with homogeneous assets.
- Not tracking production volume against targets — falling behind without realizing.
- Treating production as a one-time event instead of a continuous monthly cycle.

## Integration

- Research phase draws from `creative-angle-matrix.md` and `hook-library-system.md`.
- UGC production follows `ugc-creator-framework.md`.
- Policy review at QA stage uses `policy-risk-classification.md`.
- Launched creative tracked via `pacing-and-guardrails.md` and `optimization-layer.md`.
- Testing methodology connects to `dynamic-creative-optimization.md`.
- Fits within `creative-layer.md` stack layer for strategic context.

## Output

- Monthly production calendar with stage dates and owners.
- Creative brief library (archived for future reference).
- Asset inventory with naming, specs, and platform deployment status.
- QA pass/fail log with revision notes.
- Monthly creative velocity report: concepts produced, variations generated, tests launched.
