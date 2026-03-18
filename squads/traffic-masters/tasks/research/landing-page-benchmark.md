# Landing Page Benchmark

> **Type**: Task
> **Category**: research
> **Agents**: Creative Analyst, Ads Analyst
> **Frameworks**: LP Analysis Framework, Conversion Architecture
> **Checklists**: lp-benchmark-checklist
> **Output template**: templates/lp-benchmark-report.md

## ROUTING (from config.yaml)

> **Config key**: `routing.landing-page-benchmark`
> **Agents**: [creative-analyst](../../agents/creative-analyst.md), [ads-analyst](../../agents/ads-analyst.md)
> **Frameworks**: `creative-angle-matrix`
> **Checklists**: `landing-page-quality`, `cro/landing-page-speed-quality`
> **Templates**: `reports/competitor-ads-analysis-report`
> **Registry**: `data/research/competitor-ads`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Benchmark competitor landing pages to evaluate conversion architecture, messaging hierarchy, trust elements, page speed, and mobile experience, producing actionable insights for landing page optimization.

## Inputs
- Competitor list with landing page URLs
- Ads linking to competitor landing pages from swipe mining
- Industry conversion rate benchmarks
- Current landing page(s) for comparison
- Device split data from analytics (mobile vs desktop)

## Steps
1. Collect landing page URLs from competitor ads across all platforms
2. Screenshot and archive each landing page in full-page captures (desktop and mobile)
3. Analyze above-the-fold content: headline, subheadline, hero image, CTA placement
4. Document messaging hierarchy: order of arguments, proof placement, objection handling
5. Catalog trust elements: testimonials, logos, certifications, guarantees, security badges
6. Evaluate form design: field count, friction points, progressive disclosure
7. Test page speed using PageSpeed Insights and document Core Web Vitals scores
8. Assess mobile experience: tap targets, scroll depth, load time, readability
9. Map conversion architecture: CTA count, placement, urgency and scarcity elements
10. Score each landing page on: clarity, relevance, trust, urgency, friction, speed
11. Identify best practices to adopt and mistakes to avoid from the benchmark set

## Output
LP benchmark report containing: competitor LP screenshots and archives, scoring matrix across all criteria, best practice examples with annotations, common mistakes identified, speed and mobile benchmarks, and prioritized recommendations for own landing pages.

## Quality Gate
- LP benchmark checklist confirms minimum eight competitor pages analyzed
- All scoring criteria applied consistently across pages
- Creative Analyst validates recommendations are actionable and prioritized

## Duration
3-5 hours for analysis; 1-2 hours for report compilation
