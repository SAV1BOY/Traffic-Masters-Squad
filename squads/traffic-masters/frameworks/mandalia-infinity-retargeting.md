# Infinity Retargeting

> **Author**: Depesh Mandalia
> **Domain**: Retargeting Strategy and Automation
> **Used by agents**: media-buyer, funnel-strategist, performance-analyst
> **Checklists**: retargeting-setup-checklist, anti-fatigue-checklist

## Overview

Infinity Retargeting is Depesh Mandalia's evergreen retargeting system that runs continuously without manual creative refreshes. By layering retargeting windows with stage-appropriate messaging and leveraging Dynamic Creative Optimization (DCO) and Dynamic Product Ads (DPA), the system self-sustains. The "Infinity" name reflects its design: set up correctly, it runs indefinitely with minimal maintenance.

## When to Use

- Setting up retargeting infrastructure for any account
- Replacing manual retargeting that requires constant creative swaps
- When retargeting frequency is too high and performance is declining
- Ecommerce accounts that need automated product-level retargeting
- Building a full-funnel retargeting system from scratch

## The Framework

### Window Architecture

**Window 1: 1-3 Days (Hot — Immediate Recency)**
1. Audience: Website visitors, ATC abandoners, IC abandoners from last 1-3 days
2. Messaging: Reminder-focused, low friction, address immediate objections
3. Urgency level: Moderate — "Still thinking about it?"
4. Creative: Product-focused, social proof, simple CTA
5. Budget allocation: 30-35% of retargeting budget

**Window 2: 4-7 Days (Warm — Considered Interest)**
1. Audience: Visitors from 4-7 days ago, engaged but not converted
2. Messaging: Value reinforcement, benefits recap, testimonials
3. Urgency level: Low-moderate — "Here's what you're missing"
4. Creative: Testimonial-driven, benefit-focused, case studies
5. Budget allocation: 25-30% of retargeting budget

**Window 3: 8-14 Days (Cooling — Needs Re-engagement)**
1. Audience: Visitors from 8-14 days ago who have not returned
2. Messaging: New angle or offer variation, address deeper objections
3. Urgency level: Moderate-high — limited-time incentive if appropriate
4. Creative: Different creative format than Windows 1-2, fresh angles
5. Budget allocation: 20-25% of retargeting budget

**Window 4: 15-30 Days (Cold Retargeting — Last Chance)**
1. Audience: Visitors from 15-30 days ago, fading interest
2. Messaging: Final push, strongest offer, most compelling proof
3. Urgency level: High — "Last chance" or exclusive offer
4. Creative: Strongest performing creative from other windows, repurposed
5. Budget allocation: 15-20% of retargeting budget

### DCO (Dynamic Creative Optimization) Setup
1. Load multiple creative elements: headlines, images, descriptions, CTAs
2. Let the platform dynamically combine elements for each user
3. Ensures creative variety without manual rotation
4. Works across all windows — each window gets its own DCO asset pool
5. Refresh DCO asset pools quarterly, not weekly

### DPA (Dynamic Product Ads) for Ecommerce
1. Connect product catalog to ad platform
2. Automatically show users the exact products they viewed
3. Layer with cross-sell and upsell product sets
4. Apply window-based messaging overlays to DPA templates
5. Use DPA in Windows 1-2 (product recall) and broader catalog in Windows 3-4

### Anti-Fatigue System
1. Rotate messaging by window, not by manual swap
2. As users move from Window 1 to Window 4, they see different messaging naturally
3. DCO provides creative variation within each window
4. Users who convert are excluded from all windows immediately
5. Frequency caps: maximum 2 impressions per day per window

## Key Concepts

- **Window-based rotation**: Creative fatigue is solved structurally, not manually
- **Messaging escalation**: Each window increases urgency and changes angle
- **Exclusion is critical**: Always exclude converters from all retargeting windows
- **DCO is the engine**: It provides variation without manual creative management
- **Set and monitor, not set and forget**: Review performance monthly, refresh assets quarterly

## Decision Rules

- IF Window 1 CPA is high THEN the landing page or checkout has friction — fix the funnel
- IF Window 2 outperforms Window 1 THEN immediate messaging may be too pushy — soften Window 1
- IF Window 4 has zero conversions THEN the 15-30 day audience is too cold — shorten to 15 days or cut
- IF frequency exceeds 4 per window THEN audience pool is too small — combine windows or reduce budget
- IF DPA outperforms DCO THEN product recall is stronger than messaging — lean into catalog-driven retargeting
- IF overall retargeting ROAS drops below target THEN check exclusion rules first (are converters being re-served?)

## Common Mistakes

- Not excluding purchasers/converters from retargeting audiences
- Using the same creative across all windows (defeats the purpose)
- Setting frequency too high and annoying the audience
- Ignoring Window 4 entirely (missing last-chance conversions)
- Manually swapping creative weekly instead of using DCO
- Not segmenting ATC/IC abandoners from general visitors (different intent levels)

## Integration

- Depends on: mandalia-4-funnel-system (Infinity Retargeting maps to Funnels 2 and 3)
- Connects to: mandalia-punisher-method (punish underperforming windows)
- Connects to: kusmich-3cs-invisible-influence (retargeting is the Capture-to-Convert bridge)
- Connects to: kusmich-milestone-content (window messaging aligns with milestone progression)

## Output

- A fully configured 4-window retargeting system with audience definitions
- DCO asset pools for each window with messaging guidelines
- DPA configuration for ecommerce accounts
- Frequency cap settings and exclusion rules documented
- Monthly review template for retargeting performance assessment
