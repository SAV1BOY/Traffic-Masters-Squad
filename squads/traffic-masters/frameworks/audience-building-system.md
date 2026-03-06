# Audience Building System

> **Type**: Internal
> **Domain**: Targeting — Audience Architecture
> **Used by agents**: Media Buyer, Traffic Chief, Performance Analyst, Kusmich

## Overview

A systematic approach to building, organizing, and managing audiences across paid media platforms. Audiences are constructed in layers from highest fidelity (seed data) to broadest reach (open targeting), with each layer serving a specific funnel role. Proper audience architecture prevents overlap waste, ensures clean testing, and enables predictable scaling.

## When to Use

- New client account setup — build foundational audience architecture
- Campaign launch — select and configure targeting
- Scaling phase — expand audience layers systematically
- Performance diagnosis — identify audience saturation or overlap
- Platform expansion — adapt audiences to new channels

## The Framework

### Audience Layers (High to Low Fidelity)

#### Layer 1: Seed Audiences (Highest Value)
- **CRM Lists**: Customer email/phone lists. Minimum 1,000 records for Meta, 1,000 for Google Customer Match. Segment by LTV, purchase recency, product category.
- **Website Custom Audiences**: Pixel-based. Segment by page visited, time on site, events triggered. Windows: 30d, 60d, 90d, 180d.
- **Engagement Audiences**: Video viewers (25/50/75/100%), page/profile engagers, lead form openers, ad clickers. Platform-specific.
- **App Audiences**: Install, in-app events, purchase. If applicable.

#### Layer 2: Lookalike / Similar Audiences (LAL)
- **1% LAL**: Closest match to seed. Highest quality, smallest reach. Use for initial prospecting.
- **2-5% LAL**: Broader reach, slightly lower match quality. Use for scaling after 1% performs.
- **5-10% LAL**: Widest LAL. Use for broad prospecting or when smaller LALs saturate.
- **Source Priority**: LTV-based customer list > All purchasers > Add to cart > Website visitors > Engagers.
- **Refresh Cadence**: Update source lists monthly. LALs auto-update on Meta but verify freshness.

#### Layer 3: Interest / In-Market Audiences
- **Meta Interests**: Stack 3-5 related interests per ad set. Test narrow (single interest) vs stacked.
- **Google In-Market**: Users actively researching a category. Layer with demographics.
- **Google Custom Intent**: Build from competitor URLs and search terms. 10-15 signals per audience.
- **Affinity Audiences**: Broad lifestyle categories. Use for awareness, not direct response.

#### Layer 4: Broad / Open Targeting
- **Meta Broad**: No interest targeting. Rely on pixel data and creative to find buyers. Requires 50+ conversions/week for algorithm to optimize.
- **Google Broad**: Broad match keywords with Smart Bidding. Requires conversion history.
- **When to Deploy**: Only after Layers 1-3 are established and pixel has sufficient learning data.

### Exclusion Architecture

| Audience | Exclude From |
|----------|-------------|
| All purchasers (180d) | Prospecting campaigns |
| Website visitors (30d) | Cold prospecting |
| Retargeting audiences | Other retargeting windows |
| Existing customers | New customer acquisition campaigns |
| Converted leads | Lead generation campaigns |

### Overlap Management

- Use Meta Audience Overlap tool before launching parallel ad sets.
- Maximum acceptable overlap: 20%. Above this, consolidate or exclude.
- Google: Use Audience Insights to verify distinctness between campaigns.
- Name audiences clearly to identify overlap risk at a glance.

## Key Concepts

- **Audience Saturation**: When frequency rises above 3x/week and CTR drops, the audience is saturated. Expand to next layer or refresh creative.
- **Seed Quality > Seed Size**: A 2,000-person list of top 10% LTV customers creates better LALs than 50,000 mixed-quality emails.
- **Platform Parity**: Build equivalent audiences on both Meta and Google. Same seed lists, same segmentation logic.
- **Refresh Cadence**: CRM lists — monthly. Website audiences — auto-refresh (verify). LALs — recreate quarterly from updated seeds.

## Decision Rules

1. Always start with Layer 1 seeds before building LALs. No seeds, no LALs — use interests until data accumulates.
2. Test 1% LAL against interest stacks in parallel. Winner gets budget priority.
3. Never run broad targeting without minimum 50 conversions/week on the pixel.
4. Exclude purchasers from all prospecting — non-negotiable.
5. Maximum 3 LAL sources tested simultaneously per campaign to maintain clean data.
6. Refresh CRM uploads every 30 days. Stale lists degrade LAL quality.

## Common Mistakes

- Building LALs from low-quality seeds (all website visitors vs purchasers).
- Not excluding audiences, causing overlap and self-competition.
- Testing too many audiences at once without sufficient budget per ad set.
- Ignoring audience refresh — 6-month-old LALs from stale seeds underperform.
- Jumping to broad targeting before pixel has learning data.
- Using the same audience windows across all campaign types.

## Integration

- Feeds directly into `account-structure-meta.md` and `account-structure-google.md` for ad set configuration.
- Retargeting audiences detailed in `retargeting-sequence-system.md`.
- Audience performance monitored via `pacing-and-guardrails.md`.
- Scaling audience layers follows `scaling-playbook.md` horizontal expansion protocols.
- Kusmich methodology informs audience empathy mapping and avatar depth.

## Output

- Audience architecture document per client with all layers defined.
- Audience naming convention sheet.
- Exclusion map showing what is excluded from what.
- Monthly audience health report: size, saturation, overlap scores.
- Quarterly audience refresh schedule with responsible agent assigned.
