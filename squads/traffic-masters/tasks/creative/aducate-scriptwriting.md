# ADUCATE Scriptwriting

> **Type**: Task
> **Category**: creative
> **Agents**: Breeze, Ad Midas
> **Frameworks**: ADUCATE Script Framework (Attention, Disruption, Unconventional, Credibility, Action, Transformation, Engagement)
> **Checklists**: scriptwriting-checklist
> **Output template**: templates/video-scripts.md

## ROUTING (from config.yaml)

> **Config key**: `routing.aducate-scriptwriting`
> **Agents**: [tom-breeze](../../agents/tom-breeze.md), [ad-midas](../../agents/ad-midas.md)
> **Frameworks**: `breeze-aducate`, `breeze-3-acts`, `breeze-6cs-aducational`
> **Checklists**: `video-ad-quality`, `breeze/breeze-aducate-script-audit`, `breeze/breeze-3-acts-structure`
> **Templates**: `ads/youtube-ad-script-aducate`
> **Registry**: `data/registries/creatives-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Write YouTube and video ad scripts using the ADUCATE framework to create compelling video content that captures attention in the first five seconds, builds credibility, and drives specific viewer actions.

## Inputs
- Hook and angle bank with prioritized combinations
- ICP and avatar document with real customer language
- Offer details and key selling points
- Brand voice guidelines
- Video length targets per placement: 15s bumper, 30s short, 60-90s standard, 3-5min long-form
- Competitor video ad analysis from swipe mining

## Steps
1. Select the top hook-angle combinations prioritized for video format
2. Apply the ADUCATE framework to structure each script:
   - Attention: Write the opening hook (first 3-5 seconds) that stops the scroll
   - Disruption: Introduce an unexpected element that breaks patterns
   - Unconventional: Present the solution in a way competitors have not used
   - Credibility: Insert proof elements (data, testimonials, demonstrations)
   - Action: Define the clear CTA with urgency or reason to act now
   - Transformation: Paint the after-state the viewer will achieve
   - Engagement: Include elements that drive comments, shares, or rewatches
3. Write multiple script variants per angle to enable testing
4. Include visual direction notes: B-roll suggestions, text overlay cues, transition notes
5. Time each script to ensure it fits the target duration
6. Mark the skip point (5-second mark) to verify the hook is complete before it
7. Write companion ad copy for the video description and CTA overlay
8. Review scripts against avatar language to ensure authenticity

## Output
Video scripts containing: ADUCATE-structured scripts per angle, visual direction notes, timing annotations, hook variants, CTA options, and companion ad copy for each script.

## Quality Gate
- Scriptwriting checklist confirms ADUCATE elements present in every script
- Breeze validates scripts meet YouTube best practices and timing requirements
- Ad Midas confirms hook strength and creative differentiation

## Duration
3-5 hours for script writing; 1-2 hours for review and revision
