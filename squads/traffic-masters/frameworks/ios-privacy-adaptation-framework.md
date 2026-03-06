# iOS Privacy Adaptation Framework
> **Type**: Privacy and Data Strategy Framework
> **Used by agents**: Pixel Specialist, Media Buyer, Performance Analyst

## Overview
A framework for adapting to the iOS 14.5+ privacy changes that fundamentally altered digital advertising. Covers ATT (App Tracking Transparency), SKAN (SKAdNetwork), Aggregated Event Measurement, and Modeled Conversions. Core philosophy: accept the data loss, invest in first-party data, and build measurement systems that do not depend on perfect tracking.

## When to Use
- Setting up or auditing tracking in a post-iOS 14.5 environment
- When platform-reported conversions are significantly lower than actual
- Planning data strategy that accounts for the privacy-first future
- Training teams on the new measurement reality

## The Framework

### iOS 14.5+ Impact Assessment
- ATT (App Tracking Transparency): Users must opt in to tracking
- ATT opt-in rates average 20-35% globally
- 65-80% of iOS users are not trackable via traditional pixels
- Conversion reporting delayed up to 72 hours on Meta
- Event measurement limited to 8 prioritized events per domain

### SKAN (SKAdNetwork)
- Apple's privacy-preserving attribution framework for app installs
- Provides aggregated, delayed, and limited conversion data
- No user-level data; campaign-level attribution only
- Postback windows: 24-48 hours for initial data

### Aggregated Event Measurement (AEM)
- Meta's response to iOS limitations
- Prioritize 8 conversion events per domain by business value
- Rank: Purchase > Lead > AddToCart > ViewContent
- Domain verification required in Business Manager

### Modeled Conversions
- Platform algorithms estimate conversions they cannot directly observe
- Directional, not exact — use as guidance, not gospel
- Meta and Google both use modeled conversions in reporting
- Gap between modeled and actual narrows with more first-party data signals

### First-Party Data Strategy
- Capture email and phone at every opportunity
- Build owned audiences: email lists, customer databases, CRM segments
- Use customer match audiences for targeting and lookalikes
- Create value exchanges: content, tools, quizzes for contact info
- First-party data is the new competitive moat

### Adaptation Actions
- Implement Conversions API (CAPI) alongside pixel — non-negotiable
- Use broader targeting — let algorithms work with less signal
- Lean into creative as targeting — creative does the job audience data used to do
- Use longer attribution windows (7-day, 28-day, not just 1-day)
- Adopt MER as the strategic north star metric

## Key Concepts
- Privacy changes are permanent and will expand (Google Privacy Sandbox next)
- Businesses that adapt thrive; those that fight the change waste resources
- First-party data replaces third-party signals as the foundation
- Creative quality matters more than ever when targeting precision decreases
- Measurement must evolve from deterministic to probabilistic

## Decision Rules
1. IF iOS traffic is >30% of total — CAPI implementation is mandatory
2. IF reported conversions are 30%+ below actual — CAPI is not configured properly
3. IF broad targeting outperforms detailed — lean into it
4. IF measurement gaps are large — use MER as primary strategic metric
5. IF first-party data is weak — invest in data capture before scaling spend
6. IF planning for future — assume more privacy restrictions, not fewer

## Integration
- Feeds into: Tracking Stack Standard (privacy-adapted tracking setup)
- Pairs with: Attribution and Incrementality (new measurement approaches)
- Complements: MER Marketing Efficiency Ratio (privacy-resilient measurement)

## Output
- Privacy impact assessment for the specific business and audience
- Technical implementation checklist (CAPI, AEM, domain verification)
- First-party data strategy with capture mechanisms and value exchanges
- Measurement adaptation plan from deterministic to probabilistic
