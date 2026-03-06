# Retargeting Sequence System

> **Type**: Internal
> **Domain**: Media Buying — Retargeting Strategy
> **Used by agents**: Media Buyer, Performance Analyst, Ad Midas, Traffic Chief

## Overview

A window-based retargeting system that serves different messaging sequences based on time since last interaction. Rather than blasting the same ad to all past visitors, this framework segments by recency and matches creative to the psychological state of the prospect at each stage. Frequency management prevents fatigue. DPA layers automate ecommerce retargeting at scale.

## When to Use

- Any campaign with sufficient traffic to populate retargeting pools (500+ visitors/week minimum)
- Ecommerce accounts with product catalogs
- Lead generation funnels with multi-step conversion paths
- Post-launch optimization when prospecting generates traffic but conversions lag
- Whenever CPA on cold traffic is acceptable but overall ROAS needs improvement

## The Framework

### Window-Based Sequence

| Window | Days Since Visit | Message Theme | Creative Approach | Frequency Cap |
|--------|-----------------|--------------|-------------------|---------------|
| **Window 1** | 1-3 days | "Forgot Something" | Reminder, urgency, cart recovery | 2x/day |
| **Window 2** | 4-7 days | Social Proof | Testimonials, reviews, case studies | 1x/day |
| **Window 3** | 8-14 days | New Angle | Different value prop, objection handling, education | 1x/day |
| **Window 4** | 15-30 days | Special Offer | Discount, bonus, limited-time incentive | 1x/day |
| **Window 5** | 31-60 days | Last Chance | Final offer, scarcity, brand story recap | 3x/week |
| **Window 6** | 61-180 days | Re-engagement | New product, brand update, seasonal | 2x/week |

### Window 1: "Forgot Something" (Days 1-3)

- **Psychology**: Highest intent. They were just there. Life interrupted.
- **Creative**: Product-specific reminder. Cart abandonment. "Still thinking about it?"
- **Format**: DPA (ecommerce), static with product image (lead gen), carousel of viewed items.
- **CTA**: Direct — "Complete your purchase" / "Finish your application."
- **Budget**: 30-40% of retargeting budget. Highest ROAS window.

### Window 2: Social Proof (Days 4-7)

- **Psychology**: Interest confirmed but not convinced. Needs validation.
- **Creative**: Customer testimonials, star ratings, case study highlights, UGC reviews.
- **Format**: Video testimonials, screenshot reviews in carousel, before/after.
- **CTA**: Trust-building — "See what others are saying" / "Join 10,000+ customers."
- **Budget**: 20-25% of retargeting budget.

### Window 3: New Angle (Days 8-14)

- **Psychology**: Original message did not convert. Try a different persuasion vector.
- **Creative**: Address top objections, explain mechanism, show different use case, education content.
- **Format**: Long-form video, infographic, comparison chart, FAQ-style.
- **CTA**: Value-add — "Here's what makes us different" / "Watch how it works."
- **Budget**: 15-20% of retargeting budget.

### Window 4: Special Offer (Days 15-30)

- **Psychology**: Fading interest. Needs an incentive to re-engage.
- **Creative**: Discount code, free shipping, bonus item, extended trial, bundle offer.
- **Format**: Bold static with offer, countdown timer graphic, promotional video.
- **CTA**: Urgency — "Your exclusive offer expires in 48 hours."
- **Budget**: 15-20% of retargeting budget.

### Frequency Management

- Track frequency at the ad set level, not campaign level.
- If frequency exceeds cap for 3+ consecutive days, pause and rotate creative.
- Use frequency-based rules in Meta Ads Manager automated rules.
- Google Display: Set frequency cap at campaign level in campaign settings.
- Monitor "negative feedback" signals on Meta (hide ad, report ad).

### DPA (Dynamic Product Ads) for Ecommerce

- **Catalog Setup**: Full product feed with accurate pricing, availability, images.
- **Template Design**: Custom frames, overlay text ("Back in stock", "Limited qty").
- **Segmentation**: Viewed product, added to cart, initiated checkout — different templates per action.
- **Cross-sell**: Show complementary products to recent purchasers (separate campaign, 7-30 day window).
- **Exclusions**: Purchased products excluded for 30 days minimum.

## Key Concepts

- **Recency Decay**: Conversion probability drops exponentially with time. Day 1-3 retargeting converts 3-5x better than Day 15-30.
- **Sequential Storytelling**: Each window builds on the last. Do not repeat the same message.
- **Creative Exclusion**: Ensure users in Window 3 do not see Window 1 creative. Use audience exclusions between windows.
- **Value Ladder**: Move from reminder to proof to education to offer. Do not lead with discounts.

## Decision Rules

1. Never offer discounts in Window 1-2. Earn the sale first, incentivize later.
2. DPA is mandatory for ecommerce accounts with 50+ SKUs.
3. If retargeting pool is under 500 users, consolidate into one window (1-14 days).
4. Rotate creative within each window every 2 weeks maximum.
5. Retargeting budget should be 15-25% of total ad spend. Adjust based on traffic volume.
6. Exclude all converters from all retargeting windows immediately upon conversion.

## Common Mistakes

- Running one retargeting campaign with a 180-day window and generic creative.
- Leading with discount offers to recent visitors — trains audience to wait for deals.
- Not excluding between windows, creating overlap and budget waste.
- Ignoring frequency — showing the same ad 10+ times destroys brand perception.
- Forgetting to exclude purchasers — wasting budget showing ads for already-bought products.
- Not refreshing DPA templates — "dynamic" does not mean "set and forget."

## Integration

- Audience windows built per `audience-building-system.md` Layer 1 definitions.
- Creative for each window produced via `creative-production-pipeline.md`.
- Angle diversity across windows informed by `creative-angle-matrix.md`.
- Account structure houses retargeting campaigns per `account-structure-meta.md` and `account-structure-google.md`.
- Pacing and frequency monitored via `pacing-and-guardrails.md`.

## Output

- Retargeting sequence map per client showing windows, messaging, and creative assignments.
- Frequency monitoring dashboard with automated alerts.
- DPA template library with seasonal and promotional variants.
- Monthly retargeting performance report by window with ROAS and frequency metrics.
- Creative rotation calendar aligned to window refresh cycles.
