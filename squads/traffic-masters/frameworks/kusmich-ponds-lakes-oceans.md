# Ponds-Lakes-Oceans

> **Author**: Nicholas Kusmich
> **Domain**: Audience Scaling and Pixel Maturity
> **Used by agents**: media-buyer, performance-analyst, strategy-orchestrator
> **Checklists**: scaling-checklist, pixel-maturity-checklist

## Overview

Ponds-Lakes-Oceans is Nicholas Kusmich's progressive scaling framework based on pixel maturity. The core insight: advertising platforms learn who your ideal customer is by accumulating conversion data. You must start with small, highly targeted audiences (ponds) to train the pixel, then expand to medium audiences (lakes) as data accumulates, and finally scale to broad audiences (oceans) once the pixel is mature. Jumping to oceans with an immature pixel wastes budget on unqualified impressions.

## When to Use

- Launching a brand-new ad account with no pixel data
- Planning audience expansion strategy for a scaling campaign
- When broad targeting is underperforming (pixel may not be mature enough)
- Diagnosing why a campaign works at low budget but fails at high budget
- Setting realistic scaling timelines based on current pixel maturity

## The Framework

### Stage 1: Ponds (Small Audiences — Pixel Training)
1. **Audience size**: 50,000-500,000 people
2. **Audience types**: Custom audiences, lookalike 1%, hyper-specific interests, customer list matches
3. **Budget**: Low — $20-50/day per ad set
4. **Purpose**: Feed the pixel high-quality conversion data
5. **Duration**: Until you have 50-100+ conversions tracked by the pixel
6. **Optimization**: Optimize for the conversion event closest to purchase you can sustain
7. **Creative**: Test multiple concepts; the audience is forgiving of imperfection because targeting is precise
8. **Metrics**: CPA (likely high initially), conversion volume (more important than CPA at this stage)
9. **Key rule**: Quality over quantity — every conversion teaches the pixel who to find

### Stage 2: Lakes (Medium Audiences — Pixel Has Data)
1. **Audience size**: 500,000-5,000,000 people
2. **Audience types**: Lookalike 2-5%, broader interest stacks, combined interests, engagement audiences
3. **Budget**: Medium — $50-200/day per ad set
4. **Duration**: Until you have 200-500+ total conversions and CPA is stabilized
5. **Optimization**: Optimize for purchase or primary conversion event
6. **Creative**: Proven winners from Ponds stage — do not test unproven creative here
7. **Metrics**: CPA (should be improving), ROAS (should be approaching target), consistency (day-to-day stability)
8. **Key rule**: The pixel has learned from Ponds. Let it work with slightly broader data.

### Stage 3: Oceans (Broad Audiences — Pixel Is Mature)
1. **Audience size**: 5,000,000+ people, or fully broad (no targeting)
2. **Audience types**: Lookalike 10%+, broad interest categories, broad/open targeting, country-wide
3. **Budget**: High — $200-1,000+/day per ad set
4. **Duration**: Ongoing — this is the scaling engine
5. **Optimization**: Optimize for purchase with the pixel doing the heavy lifting
6. **Creative**: Only top-performing creative that has proven through Ponds and Lakes
7. **Metrics**: CPA at scale, ROAS, volume, incremental lift
8. **Key rule**: The mature pixel can find your ideal customer in a broad audience. Trust it.

### Pixel Maturity Indicators
- **Immature** (0-50 conversions): Platform is guessing. Stay in Ponds.
- **Learning** (50-200 conversions): Platform has directional data. Move to Lakes cautiously.
- **Competent** (200-500 conversions): Platform can find buyers reliably. Lakes are safe.
- **Mature** (500+ conversions): Platform has robust data. Oceans are viable.
- **Expert** (1,000+ conversions): Platform can operate with minimal targeting. Broad scales well.

### Transition Process
1. Do not abandon the previous stage when moving to the next
2. Ponds continue running as testing grounds even when Oceans are active
3. Each transition should be gradual — test one Lake ad set before moving all budget
4. Monitor CPA during transitions — a spike is normal for 3-5 days, but sustained spikes mean the pixel is not ready
5. If Ocean performance is poor, retreat to Lakes and gather more data

## Key Concepts

- **Pixel learning is sequential**: You cannot skip Ponds and go straight to Oceans
- **Data quality matters more than data volume**: 50 high-quality conversions beat 200 junk conversions
- **Broad is not better — mature broad is better**: Broad targeting only works when the pixel knows who to find
- **Patience is a competitive advantage**: Most advertisers rush to Oceans and waste budget
- **The pixel is your best audience researcher**: Given enough quality data, it outperforms manual targeting

## Decision Rules

- IF you have fewer than 50 conversions THEN stay in Ponds regardless of other pressures
- IF CPA is stable in Ponds and you have 100+ conversions THEN test one Lake audience
- IF Lake CPA is within 1.5x of Pond CPA THEN the pixel is learning well — expand Lakes
- IF Lake CPA is 2x+ Pond CPA THEN the pixel needs more Pond data — retreat
- IF Ocean targeting shows improving CPA over 7+ days THEN the pixel is mature — scale confidently
- IF Ocean targeting never stabilizes THEN the pixel may have been trained on low-quality conversions — restart Ponds with better conversion events

## Common Mistakes

- Jumping to broad targeting on day one with a brand-new pixel
- Optimizing for a top-of-funnel event (link clicks) and expecting the pixel to learn about buyers
- Not giving Ponds enough time or budget to accumulate meaningful data
- Abandoning Ponds when moving to Lakes (Ponds are your testing lab forever)
- Blaming the platform when Ocean campaigns fail — the pixel was not ready
- Training the pixel on discount/freebie conversions and wondering why it finds non-buyers

## Integration

- Connects to: mandalia-scaling-recipes (H-Scale is horizontal expansion through pond-to-lake-to-ocean logic)
- Connects to: mandalia-graduation-testing (graduation happens within the Ponds stage)
- Connects to: mandalia-4-funnel-system (Funnel 1 audiences start as Ponds and expand)
- Connects to: kusmich-targeting-trifecta (Trifecta builds the Pond audiences)
- Connects to: kusmich-4ms (Market M starts in Ponds and expands as pixel matures)

## Output

- Pixel maturity assessment with current conversion count and quality score
- Audience stage classification (Pond/Lake/Ocean) for each active ad set
- Transition readiness report: which audiences are ready to move to the next stage
- Scaling timeline estimate based on current conversion velocity
- Audience architecture showing Ponds (testing), Lakes (proving), and Oceans (scaling) simultaneously
