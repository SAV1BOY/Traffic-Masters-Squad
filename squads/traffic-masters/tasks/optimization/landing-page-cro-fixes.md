# Landing Page CRO Fixes

> **Type**: Task
> **Category**: optimization
> **Agents**: Creative Analyst, Performance Analyst
> **Frameworks**: CRO Analysis Framework, Conversion Architecture
> **Checklists**: cro-fixes-checklist
> **Output template**: templates/cro-fixes.md

## ROUTING (from config.yaml)

> **Config key**: `routing.landing-page-cro-fixes`
> **Agents**: [creative-analyst](../../agents/creative-analyst.md), [performance-analyst](../../agents/performance-analyst.md)
> **Frameworks**: `burns-conversion-architecture`
> **Checklists**: `landing-page-quality`, `cro/landing-page-speed-quality`, `cro/form-friction-quality`, `cro/post-click-consistency`
> **Templates**: N/A
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Identify and fix conversion rate optimization issues on landing pages by analyzing user behavior data, heatmaps, and funnel drop-off points to improve the conversion rate and reduce cost per acquisition.

## Inputs
- Landing page URLs with current conversion rates
- Analytics data: bounce rate, time on page, scroll depth, exit rate
- Heatmap and session recording data (Hotjar, Microsoft Clarity)
- Funnel drop-off analysis from GA4 or platform data
- LP benchmark report with competitor comparison
- A/B testing tool access (if available)

## Steps
1. Analyze landing page conversion rates against benchmarks and identify underperformers
2. Review heatmap data: click maps, scroll maps, and attention maps for each page
3. Watch session recordings to identify user confusion, hesitation, or abandonment patterns
4. Analyze form analytics: field-level drop-off, time to complete, error rates
5. Check page speed: Core Web Vitals, mobile load time, render-blocking resources
6. Audit above-the-fold content: headline clarity, value proposition visibility, CTA prominence
7. Evaluate message match: does the landing page deliver what the ad promised
8. Check mobile experience: tap targets, text readability, form usability, scroll behavior
9. Identify trust element gaps: missing testimonials, unclear guarantees, absent security badges
10. Prioritize fixes by expected impact and implementation effort (ICE scoring)
11. Create fix specifications with before/after mockups for each recommended change
12. Set up A/B tests for significant changes to validate improvements before full rollout

## Output
CRO fixes document containing: issue inventory with severity, prioritized fix list with ICE scores, fix specifications with mockups, A/B test plan for major changes, and expected conversion rate improvement projections.

## Quality Gate
- CRO fixes checklist confirms all data sources analyzed
- Fixes prioritized by impact with clear implementation specs
- Performance Analyst validates expected improvement projections are realistic

## Duration
3-5 hours for analysis; 1-2 hours for fix specification and documentation
