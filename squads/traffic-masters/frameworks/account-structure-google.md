# Account Structure — Google Ads

> **Type**: Internal
> **Domain**: Media Buying — Google Ads
> **Used by agents**: Media Buyer, Traffic Chief, Aslam, Performance Analyst

## Overview

Defines the organizational blueprint for Google Ads accounts across Search, Shopping, Display, and YouTube. Structure follows the Aslam 4 Core methodology: campaigns organized by intent level and buyer journey stage. Proper structure ensures budget flows to highest-intent traffic first and enables granular optimization.

## When to Use

- New client onboarding (Google channel)
- Account audits and restructures
- Expanding from Search-only to full Google ecosystem
- Migrating from Smart campaigns to manual/hybrid control

## The Framework

### Campaign Types by Intent

| Priority | Campaign Type | Intent Level | Typical ROAS | Budget Share |
|----------|--------------|-------------|-------------|-------------|
| 1 | Brand Search | Highest | 10-30x | 5-10% |
| 2 | Shopping (Standard) | High | 4-8x | 25-35% |
| 3 | Non-Brand Search (General) | Medium-High | 2-5x | 20-30% |
| 4 | Competitor Search | Medium | 1-3x | 5-10% |
| 5 | Performance Max (PMax) | Mixed | 3-6x | 15-25% |
| 6 | Display / YouTube | Low-Medium | 1-3x | 10-15% |

### Search Structure

- **Brand Campaign**: Exact match brand terms. Low CPC, high conversion. Always on. Separate mobile bid adjustments.
- **Competitor Campaign**: Competitor brand terms. Higher CPC, lower CVR. Monitor trademark policy. Use comparison-style ad copy.
- **General (Non-Brand) Search**: Organized by product/service category. Each ad group = one tight theme (SKAG or STAG approach). Minimum 3 responsive search ads per ad group.

### Match Type Strategy

- **Exact Match**: Primary driver. Highest control, best quality scores.
- **Phrase Match**: Secondary expansion. Monitor search terms weekly.
- **Broad Match**: Only with Smart Bidding (tCPA/tROAS) and sufficient conversion data (30+/month per campaign). Never broad match without automated bidding.

### Shopping Structure

- **Standard Shopping**: Tiered by priority — High (best sellers), Medium (catalog), Low (catch-all). Product group segmentation by category, margin, performance.
- **Performance Max (PMax)**: Asset groups by product category or theme. Provide audience signals (not restrictions). Feed quality is paramount — optimize titles, descriptions, images.

### Ad Group Granularity

- One core theme per ad group. No more than 15-20 keywords per ad group.
- Negative keyword lists shared at campaign and account level.
- Single Keyword Ad Groups (SKAGs) for top 20% revenue-driving terms.

## Key Concepts

- **Aslam 4 Core Connection**: Structure maps to the four pillars — Capture (Brand/Search), Create (Display/YouTube), Convert (Shopping/Retargeting), Keep (RLSA/Customer Match).
- **Naming Convention**: `[Client]_[Network]_[Campaign Type]_[Category]_[Geo]` for campaigns. Ad groups: `[Theme]_[Match Type]`.
- **Shared Budgets**: Avoid. Each campaign gets dedicated budget for clear performance signals.

## Decision Rules

1. Brand campaigns launch first. Non-negotiable — protect brand terms from competitors.
2. Standard Shopping before PMax. Establish baseline data, then layer PMax for incremental reach.
3. Never launch Broad match keywords without 30+ conversions/month in the campaign.
4. Competitor campaigns require dedicated landing pages with comparison content.
5. Display/YouTube are upper-funnel — do not judge on last-click ROAS alone.
6. PMax asset groups: minimum 5 headlines, 5 descriptions, 5 images, 1 video per group.

## Common Mistakes

- Letting PMax cannibalize brand traffic without brand exclusions.
- Running too many match types for the same keyword in one ad group.
- Ignoring search term reports — bleeding budget on irrelevant queries.
- Poor product feed quality tanking Shopping performance.
- Using shared budgets, which obscure individual campaign performance.
- Not segmenting mobile vs desktop when performance differs significantly.

## Integration

- Aligns with Aslam 4 Core methodology for strategic direction.
- Tracking setup defined in `tracking-layer.md` — GA4, GTM, conversion imports.
- Budget pacing monitored via `pacing-and-guardrails.md`.
- YouTube campaigns detailed further in `youtube-ads-structure.md`.
- Scaling protocols in `scaling-playbook.md` apply to horizontal expansion.

## Output

- Complete account map document with campaign hierarchy.
- Keyword architecture spreadsheet with match types and negatives.
- Shopping feed optimization checklist.
- PMax asset group inventory with audience signals.
- Monthly structure review cadence in project management tool.
