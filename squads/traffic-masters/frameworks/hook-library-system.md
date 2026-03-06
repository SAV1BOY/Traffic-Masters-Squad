# Hook Library System

> **Type**: Internal
> **Domain**: Creative Strategy — Hook Management
> **Used by agents**: Ad Midas, Creative Analyst, Breeze, Media Buyer

## Overview

A structured system for cataloging, tagging, retrieving, and evaluating ad hooks across all platforms and formats. Hooks are the single most important element in paid media creative — they determine whether the audience engages or scrolls. This system ensures institutional memory of what works, eliminates redundant testing, and accelerates creative production.

## When to Use

- Creative production phase — pull proven hooks for new concepts
- Hook brainstorming sessions — review what has been tested and results
- Performance analysis — identify hook patterns that outperform
- New platform expansion — adapt proven hooks to new formats
- Onboarding new creative team members — library as training resource

## The Framework

### Hook Entry Structure

Each hook in the library is stored with the following metadata:

```
Hook ID: [Auto-incremented]
Hook Text/Description: [The actual hook — first line, first 3 seconds, thumbnail text]
Platform: [Meta | Google | YouTube | TikTok | Email | Landing Page]
Format: [Video | Static | Carousel | UGC | Story | Reel | Shorts]
Hook Type: [Question | Statement | Statistic | Command | Story Open | Pattern Interrupt | Contrast | List]
Temperature: [Cold | Warm | Hot]
Angle: [Pain | Desire | Objection | Proof | Mechanism | Authority | Social Proof | Curiosity | Controversy | Story]
Client/Niche: [Client name or industry vertical]
Performance Data:
  - CTR: [%]
  - Hook Rate (3-sec video view %): [%]
  - Hold Rate (ThruPlay %): [%]
  - Conversion Rate: [%]
  - Spend: [$]
  - Status: [Winner | Performer | Average | Loser | Untested]
Date Added: [YYYY-MM-DD]
Date Retired: [YYYY-MM-DD or Active]
Context Notes: [Why it worked/failed, audience response, iteration history]
```

### Hook Type Taxonomy

| Hook Type | Description | Example |
|-----------|------------|---------|
| **Question** | Opens a curiosity loop via question | "What if everything you know about X is wrong?" |
| **Statement** | Bold declarative claim | "This changed my business in 30 days." |
| **Statistic** | Data-driven opening | "93% of marketers fail at this one thing." |
| **Command** | Direct instruction | "Stop scrolling if you want to..." |
| **Story Open** | Narrative beginning | "6 months ago, I was about to give up." |
| **Pattern Interrupt** | Visual or verbal disruption | "DELETE this ad before your competitor sees it." |
| **Contrast** | Before/after or us vs them | "Most people do X. Top performers do Y." |
| **List** | Numbered or structured promise | "3 things I wish I knew before spending $100k on ads." |

### Tagging System

Every hook receives tags across five dimensions:
1. **Platform tags** — where it was deployed
2. **Format tags** — asset type
3. **Hook type tags** — from taxonomy above
4. **Temperature tags** — audience awareness level
5. **Performance tags** — Winner / Performer / Average / Loser / Untested

### Retrieval Protocol

When building new creatives, query the library by:
1. Filter by niche/client similarity
2. Filter by platform and format
3. Sort by performance status (Winners first)
4. Cross-reference with `creative-angle-matrix.md` for angle alignment
5. Adapt — never copy verbatim across clients. Modify for voice, offer, and audience.

## Key Concepts

- **Hook Rate**: Percentage of impressions that result in 3-second video views. Benchmark: 25-40% is good, 40%+ is exceptional.
- **Hook Iteration**: A winning hook should spawn 3-5 variations before retiring the concept. Change one variable at a time.
- **Cross-Pollination**: Hooks that work on Meta often work on YouTube Shorts and TikTok with minor adaptation. Track cross-platform performance.
- **Seasonal Decay**: Some hooks are time-sensitive (urgency, seasonal). Tag accordingly and sunset.

## Decision Rules

1. Every new creative must reference the hook library before writing new hooks from scratch.
2. Minimum 5 hook variations per creative concept at testing phase.
3. A hook is classified as "Winner" only after $500+ spend with CTR above niche benchmark.
4. Retired hooks remain in library with performance data — they inform future decisions.
5. Monthly library audit: archive stale entries, promote new winners, identify gaps.
6. Cross-client hook sharing allowed for patterns/structures, never for specific copy.

## Common Mistakes

- Storing hooks without performance data — the library becomes a junk drawer.
- Not updating hook status after campaigns run — stale data leads to bad decisions.
- Copying winning hooks verbatim across different niches without adaptation.
- Ignoring hook type diversity — testing only Questions when Statements may outperform.
- Failing to iterate on winners — one hook test is not enough, variations unlock the ceiling.

## Integration

- Hooks generated from `creative-angle-matrix.md` angle-segment intersections.
- Used during `creative-production-pipeline.md` Research and Brief phases.
- UGC hooks documented per `ugc-creator-framework.md` briefing standards.
- Performance data feeds `optimization-layer.md` creative refresh triggers.
- Policy-sensitive hooks flagged per `policy-risk-classification.md`.

## Output

- Maintained hook library database (spreadsheet, Notion, or Airtable).
- Monthly hook performance report with top 10 winners and bottom 10 losers.
- Hook pattern analysis — which types/angles/temperatures trend upward.
- New hook generation queue for upcoming production cycles.
- Cross-platform adaptation log showing hook migration success rates.
