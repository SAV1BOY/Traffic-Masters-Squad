# iOS Privacy Adaptation Framework
> **Author**: Universal / Privacy & Tracking
> **Domain**: iOS 14.5+, Privacy, Data Strategy, Tracking Adaptation
> **Used by agents**: analytics-agent, media-buyer-agent, strategist-agent

## Overview
A framework for adapting to the iOS 14.5+ privacy changes that fundamentally altered
digital advertising. Covers ATT (App Tracking Transparency), SKAN (SKAdNetwork),
Aggregated Event Measurement, and Modeled Conversions. The core philosophy: accept
the data loss, invest in first-party data, and build measurement systems that do not
depend on perfect tracking.

## When to Use
- Setting up or auditing tracking in a post-iOS 14.5 environment
- When platform-reported conversions are significantly lower than actual
- Planning data strategy that accounts for privacy-first future
- Training teams on the new measurement reality

## The Framework
### Impact Assessment
- iOS users represent 25-55% of traffic in most markets
- ATT opt-in rates average 20-35% globally
- This means 65-80% of iOS users are not trackable via traditional pixels
- Conversion reporting is delayed (up to 72 hours on Meta)
- Event measurement is limited to 8 prioritized conversion events

### Adaptation Layer 1: Technical
- **Conversions API (CAPI)**: Server-side tracking to supplement pixel
- **Aggregated Event Measurement (AEM)**: Prioritize 8 conversion events
- **Domain Verification**: Verify domains on all platforms
- **SKAdNetwork (SKAN)**: iOS-specific attribution for app campaigns
- **Enhanced Conversions (Google)**: First-party data for conversion matching

### Adaptation Layer 2: Strategic
- **Accept imperfect data**: Stop chasing pre-iOS accuracy — it is not coming back
- **First-party data investment**: Email, phone, CRM, loyalty programs
- **Broader targeting**: Let algorithms work with less signal (use broad audiences)
- **Creative as targeting**: When audience signals weaken, creative does the targeting
- **Longer attribution windows**: Look at 7-day and 28-day windows, not just 1-day

### Adaptation Layer 3: Measurement
- **Modeled Conversions**: Trust platform modeling as directional guidance
- **MER as North Star**: Total Revenue / Total Spend bypasses attribution gaps
- **Geo Testing**: Measure incrementality without user-level tracking
- **Blended ROAS**: Combine platform data with backend data for truth
- **Cohort Analysis**: Track customer cohorts instead of individual users

### First-Party Data Strategy
- Capture email and phone at every opportunity
- Build owned audiences (email lists, customer databases, CRM segments)
- Use customer match audiences for targeting and lookalikes
- Create value exchanges: content, tools, quizzes in exchange for contact info
- First-party data is the new competitive moat

## Key Concepts
- Privacy changes are permanent and will expand (Google's Privacy Sandbox is next)
- Businesses that adapt thrive; those that fight the change waste resources
- First-party data replaces third-party signals as the foundation of targeting
- Creative quality matters more than ever when targeting precision decreases
- Measurement must evolve from deterministic (exact) to probabilistic (modeled)
- The businesses with the best first-party data will win in the privacy era

## Decision Rules
- IF iOS traffic is >30% of total → CAPI implementation is mandatory
- IF reported conversions are 30%+ below actual → CAPI is not configured properly
- IF broad targeting outperforms detailed targeting → lean into it (platform signal)
- IF measurement gaps are large → use MER as primary strategic metric
- IF first-party data is weak → invest in data capture before scaling spend
- IF planning for future → assume more privacy restrictions, not fewer

## Common Mistakes
- Waiting for "things to go back to normal" (they will not)
- Relying on pixel-only tracking in a post-ATT world
- Not prioritizing the 8 conversion events correctly for AEM
- Ignoring CAPI because "the pixel still works" (it works less every month)
- Fighting broad targeting instead of embracing it with strong creative
- Not investing in first-party data infrastructure

## Integration
- Feeds into: Tracking Stack Standard (privacy-adapted tracking setup)
- Pairs with: Attribution and Incrementality (new measurement approaches)
- Complements: MER Marketing Efficiency Ratio (privacy-resilient measurement)
- Impacts: All platform-specific targeting and measurement strategies

## Output
- Privacy impact assessment for the specific business and audience
- Technical implementation checklist (CAPI, AEM, domain verification)
- First-party data strategy with capture mechanisms and value exchanges
- Measurement adaptation plan moving from deterministic to probabilistic
