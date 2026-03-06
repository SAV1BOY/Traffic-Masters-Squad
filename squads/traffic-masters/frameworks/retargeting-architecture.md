# Retargeting Architecture
> **Type**: Audience Strategy Framework
> **Used by agents**: Media Buyer, Performance Analyst, Ad Midas

## Overview
A structured approach to retargeting with defined time windows, audience exclusions, message sequencing, and frequency caps. Divides retargeting audiences into six windows (1-3d, 4-7d, 8-14d, 15-30d, 31-60d, 61-180d) with progressively different messaging as recency decreases.

## When to Use
- Setting up retargeting campaigns on any platform
- When retargeting is a single catch-all audience with one message
- Improving retargeting ROAS through better segmentation
- Reducing ad fatigue from overexposure

## The Framework

### Window 1: 1-3 Days (Hottest)
- **Audience**: Recent visitors, cart abandoners, form starters
- **Message**: Urgency, reminder, direct offer
- **Frequency Cap**: Up to 3 impressions/day
- **Creative**: Product-focused, testimonial, limited time offer

### Window 2: 4-7 Days
- **Audience**: Past-week visitors, content consumers
- **Message**: Social proof, testimonials, case studies
- **Frequency Cap**: Up to 2 impressions/day

### Window 3: 8-14 Days
- **Audience**: Two-week visitors, partial engagers
- **Message**: Education, objection handling, deeper content
- **Frequency Cap**: 1-2 impressions/day

### Window 4: 15-30 Days
- **Audience**: Monthly visitors, declining engagement
- **Message**: Re-engagement, new angle, different value proposition
- **Frequency Cap**: 1 impression/day maximum

### Window 5: 31-60 Days
- **Audience**: Older visitors who did not convert
- **Message**: Brand reinforcement, new content, soft re-engagement
- **Frequency Cap**: 3-5 impressions/week maximum

### Window 6: 61-180 Days
- **Audience**: Very old visitors, likely need re-warming
- **Message**: Treat as near-cold; lead with value, not product
- **Frequency Cap**: 2-3 impressions/week maximum

### Exclusion Rules
- Exclude purchasers from all windows (or move to upsell sequence)
- Exclude each window from the next (no overlap)
- Exclude all retargeting audiences from prospecting campaigns
- Exclude users seen >15 times without converting

### Sequencing Logic
- Window 1-2: Conversion-focused (they showed intent)
- Window 3-4: Trust-building (they need more convincing)
- Window 5-6: Re-warming (they have gone cold, start over gently)
- Refresh creative in each window every 2-3 weeks

## Key Concepts
- Recency is the strongest predictor of retargeting conversion
- Message must match the recency window
- Frequency caps prevent fatigue and negative brand sentiment
- Exclusions are as important as inclusions for efficient spend

## Decision Rules
- IF retargeting ROAS declines — check frequency and creative freshness
- IF Window 1 CVR is low — the offer or landing page needs work
- IF Windows 5-6 produce no conversions — reduce budget or stop
- IF audience pools are small — combine windows (1-7d, 8-30d, 31-180d)

## Integration
- Feeds into: Full-Funnel Ads Strategy (retargeting = MOFU/BOFU)
- Pairs with: Traffic Temperature Framework (window = temperature indicator)
- Source data: Tracking Stack Standard (audience data for window creation)

## Output
- Six retargeting audience definitions with time windows
- Message and creative specifications per window
- Frequency cap settings per window
- Exclusion rules and audience flow diagram
