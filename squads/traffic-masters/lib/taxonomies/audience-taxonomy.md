# Audience Taxonomy

## Purpose
Classification system for audience segments across platforms.

## Temperature-Based Classification

### 1. Cold Audiences (Never interacted)
- **1.1 Broad** — No targeting restrictions, platform AI
- **1.2 Interest-Based** — Platform interest/behavior targeting
- **1.3 Lookalike** — Modeled from seed audience
- **1.4 Custom Segment** — Search terms, URLs, apps (Google)
- **1.5 Demographic** — Job title, company, seniority (LinkedIn)

### 2. Warm Audiences (Some interaction)
- **2.1 Video Viewers** — 25%, 50%, 75%, 95% viewers
- **2.2 Engagers** — Liked, commented, shared, saved
- **2.3 Page/Profile Visitors** — Visited brand page
- **2.4 Website Visitors** — Browsed but no conversion action
- **2.5 Content Consumers** — Blog readers, resource downloaders

### 3. Hot Audiences (High intent)
- **3.1 Add to Cart** — Added product but didn't purchase
- **3.2 Checkout Initiated** — Started checkout, abandoned
- **3.3 Lead Form Started** — Began but didn't submit
- **3.4 Pricing Page Visitors** — Viewed pricing/plans
- **3.5 Repeat Visitors** — 3+ visits in 7 days

### 4. Customer Audiences (Purchased)
- **4.1 New Customers** — First purchase, last 30 days
- **4.2 Repeat Customers** — 2+ purchases
- **4.3 VIP Customers** — Top 20% by LTV
- **4.4 Lapsed Customers** — No purchase in 90+ days
- **4.5 Churned Customers** — Cancelled or no purchase 180+ days

## Tagging Convention
Use format: `AUD-[Temp].[Sub#]` (e.g., AUD-COLD.3 for Lookalike)

## Exclusion Rules
- BOFU campaigns exclude customers (4.x)
- MOFU campaigns exclude hot (3.x) to avoid cannibalization
- Always exclude converted users from their originating funnel
