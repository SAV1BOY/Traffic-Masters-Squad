# Creative Layer

> **Type**: Stack Layer
> **Domain**: Creative Production and Asset Management
> **Used by agents**: Ad Midas, Creative Analyst, Breeze, Traffic Chief

## Overview

The Creative Layer is where strategy becomes tangible. This layer governs the production of all advertising assets — from concept development through final QA. Creative is the single largest lever in modern paid media: platforms have commoditized targeting and bidding, making creative quality the primary differentiator between winning and losing campaigns. This layer systematizes creative output to deliver volume, variety, and quality.

## When to Use

- Following completion of Strategy Layer (standard workflow)
- Monthly creative refresh cycles
- When creative fatigue is detected (CTR decline, frequency increase)
- Scaling phases requiring increased creative volume
- New platform or format expansion requiring new asset types

## The Framework

### Creative Production Workflow

#### Phase 1: Angle Development (Days 1-3)
**Owner**: Ad Midas, Creative Analyst

- Review strategy brief and discovery documents.
- Populate `creative-angle-matrix.md` with angle-segment combinations.
- Prioritize top 10-15 concepts based on audience insight depth and competitive gap.
- Map angles to temperature levels (cold, warm, hot traffic).
- Assign format recommendations per angle (video, static, carousel, UGC).

**Output**: Prioritized angle list with format assignments.

#### Phase 2: Hook Development (Days 2-4)
**Owner**: Ad Midas, Breeze

- Generate 3-5 hooks per prioritized angle.
- Cross-reference `hook-library-system.md` for proven patterns.
- Classify hooks by type (question, statement, statistic, story open, etc.).
- Score hooks for policy risk per `policy-risk-classification.md`.
- Select top 2-3 hooks per concept for production.

**Output**: Hook sheet with selected hooks, type tags, and risk classification.

#### Phase 3: Script and Copy Writing (Days 3-6)
**Owner**: Ad Midas, Breeze

**For Video**:
- Full script with hook, body, and CTA sections.
- Breeze methodology applied: pattern interrupt opening, emotional resonance in body, clear directive CTA.
- Multiple hook takes written (minimum 3 per script).
- Visual direction notes for each section.
- Timing targets: 15s, 30s, 60s versions where applicable.

**For Static/Carousel**:
- Primary text variations (3 per ad minimum).
- Headline variations (5 per ad minimum).
- Description variations (3 per ad minimum).
- Visual direction: imagery, layout, text overlay content.

**For UGC**:
- Creator brief following `ugc-creator-framework.md`.
- Talking points (not scripts) with hook requirements.
- Tone and authenticity guidelines.

**Output**: Script/copy document package per concept.

#### Phase 4: Asset Production (Days 5-10)
**Owner**: Creative team, UGC creators

- Video production: shooting, editing, motion graphics, sound design.
- Static design: graphic design, photography, composition.
- Carousel creation: multi-frame narrative with visual continuity.
- UGC creator content: filmed per brief, reviewed per framework.
- All assets produced in required aspect ratios: 1:1, 4:5, 9:16, 16:9.

**Volume Targets by Budget Level**:
| Monthly Ad Spend | Concepts/Month | Variations/Concept | Total Assets |
|-----------------|---------------|-------------------|-------------|
| $5K-15K | 8-10 | 3 | 24-30 |
| $15K-50K | 12-15 | 4 | 48-60 |
| $50K-100K | 18-22 | 5 | 90-110 |
| $100K+ | 25+ | 5+ | 125+ |

#### Phase 5: Variations and Adaptations (Days 9-12)
**Owner**: Creative team

- Format adaptations across aspect ratios.
- Hook swaps: same body with different opening hooks.
- CTA variations: different offers or urgency levels.
- Text overlay variations for video thumbnails.
- Platform-specific adjustments (Meta vs YouTube vs TikTok).
- Copy variations for A/B testing in ad setup.

#### Phase 6: Quality Assurance (Days 11-13)
**Owner**: Creative Analyst, Ads Analyst

Full QA checklist from `creative-production-pipeline.md`:
- Policy compliance review.
- Brand guideline adherence.
- Technical specification verification.
- Copy proofreading.
- Mobile rendering check.
- Sound-off comprehension test for video.
- UTM and tracking parameter verification on destination URLs.

**Output**: QA report with pass/fail per asset and revision notes.

### Creative Testing Methodology

#### Testing Hierarchy

1. **Angle Test**: Which persuasion angle resonates? (Pain vs Desire vs Proof)
2. **Hook Test**: Which opening captures attention? (Within winning angle)
3. **Format Test**: Which format delivers? (Video vs static vs carousel)
4. **Copy Test**: Which supporting text converts? (Within winning format)
5. **CTA Test**: Which call-to-action drives action? (Within winning copy)

Test in this order. Do not test CTA before you have a winning angle.

#### Testing Structure

- Dedicate 10-20% of campaign budget to creative testing.
- Test maximum 3-5 variables simultaneously (one variable type at a time).
- Minimum $50/day per test variation for 3-5 days before declaring winner.
- Statistical significance: minimum 100 clicks per variation before comparison.
- Use ABO (equal budget distribution) for clean testing. Not CBO.

## Key Concepts

- **Breeze Methodology**: Video creative must follow pattern interrupt principles — disruption in first 3 seconds, emotional resonance through the body, and unavoidable CTA at close. Every frame earns the next frame.
- **Creative Decay**: All creative has a half-life. Average lifespan: 2-4 weeks before performance degrades. Production must be continuous, not batch-and-forget.
- **The 80/20 of Creative**: 80% of performance comes from 20% of creative assets. Identify winners fast, scale them, and replace losers faster.
- **Format Diversity**: Audiences respond differently to different formats. A video winner and a static winner should coexist — they reach different people.

## Decision Rules

1. No campaign launch without minimum 3 distinct creative concepts.
2. Creative testing budget is protected — never reallocate testing budget to scaling.
3. QA stage cannot be bypassed, even under time pressure.
4. UGC and brand creative should both be active — they serve different algorithm paths.
5. Winning creative is scaled for maximum 4 weeks before mandatory fresh variation is tested alongside it.
6. Creative Analyst reviews all performance data weekly and flags fatigue within 24 hours of detection.

## Common Mistakes

- Launching with one creative concept and hoping it works.
- Not producing enough variations — one version per concept is insufficient for testing.
- Skipping the angle hierarchy and jumping to CTA tests.
- Producing all video or all static — format diversity is critical.
- Not tracking creative performance at the individual asset level.
- Waiting for creative to die before starting next production cycle — pipeline must be continuous.

## Integration

- Receives strategy brief from `strategy-layer.md`.
- Angle development uses `creative-angle-matrix.md`.
- Hook generation uses `hook-library-system.md`.
- UGC production follows `ugc-creator-framework.md`.
- Policy compliance via `policy-risk-classification.md`.
- QA process from `creative-production-pipeline.md`.
- Finished assets delivered to `media-buying-layer.md` for campaign build.
- Testing results feed `optimization-layer.md` for performance improvement.
- DCO testing per `dynamic-creative-optimization.md`.

## Output

- Complete creative asset package per production cycle.
- Creative testing plan with hypothesis, structure, and success criteria.
- QA certification for all assets before handoff.
- Creative performance tracker updated weekly.
- Monthly creative velocity report.
- Next-cycle production brief based on current cycle learnings.
