# Strategy Layer

> **Type**: Stack Layer
> **Domain**: Strategic Planning and Architecture
> **Used by agents**: Traffic Chief, Pittman, Burns, Performance Analyst

## Overview

The Strategy Layer transforms Discovery Layer intelligence into an actionable campaign architecture. This is where the funnel is designed, channels are selected, budgets are allocated, measurement is planned, and creative strategy is defined. Every decision at this layer cascades through the entire stack — a strategic error here compounds into wasted spend downstream.

## When to Use

- Immediately following completed Discovery Layer
- Quarterly strategic reviews and pivots
- Significant budget changes (up or down 30%+)
- New channel or platform expansion decisions
- When performance plateaus despite optimization efforts

## The Framework

### Strategy Components

#### 1. Funnel Architecture
**Owner**: Traffic Chief, Pittman
**Duration**: 1-2 days

Design the conversion funnel from first touch to purchase/conversion:

| Funnel Stage | Purpose | Content Type | Primary Channel |
|-------------|---------|-------------|----------------|
| Awareness | Introduce brand/problem | Video, educational, entertaining | YouTube, Meta (broad), Display |
| Consideration | Build interest and trust | Case studies, demos, UGC, testimonials | Meta (interest), Search (non-brand), In-feed |
| Conversion | Drive action | Direct response, offers, DPA | Meta (retargeting), Search (brand), Shopping |
| Retention | Repeat purchase, LTV | Email, cross-sell, loyalty | Email, Meta (customer match), RLSA |

Funnel type selection:
- **Direct Response Funnel**: Ad > Landing Page > Purchase/Lead. For proven offers with strong market fit.
- **Content Funnel**: Ad > Content > Retarget > Landing Page > Conversion. For complex/high-ticket offers.
- **Webinar/VSL Funnel**: Ad > Registration > Webinar/VSL > Application > Sale. For high-ticket services.
- **Ecommerce Funnel**: Ad > Product Page / Collection > Cart > Purchase. With DPA retargeting layer.

#### 2. Channel Strategy
**Owner**: Traffic Chief, Burns
**Duration**: 1 day

Select channels based on discovery insights:

| Channel | Best For | Minimum Budget | Maturity Required |
|---------|---------|---------------|-------------------|
| Meta (FB/IG) | Visual products, DTC, lead gen, broad audiences | $3K/month | None — start here |
| Google Search | High-intent buyers, services, B2B | $2K/month | None — start here |
| Google Shopping | Ecommerce with product feed | $3K/month | Product feed ready |
| YouTube | Demonstration products, brand building, education | $5K/month | Video assets required |
| TikTok | Younger demos, trend-driven, impulse purchases | $3K/month | UGC-style assets required |
| PMax | Scale play, all Google surfaces | $5K/month | 50+ conversions/month existing |

**Channel Sequencing**: Start with 1-2 primary channels. Add channels only after primary channels are profitable and stable. Never launch on 4+ channels simultaneously.

#### 3. Budget Allocation
**Owner**: Traffic Chief
**Duration**: 0.5 days

**Allocation Model**:
- **Testing Phase (Month 1-2)**: 60% on primary channel, 30% testing/creative, 10% secondary channel.
- **Growth Phase (Month 3-6)**: 50% proven campaigns, 25% scaling experiments, 15% new channel, 10% testing.
- **Scale Phase (Month 6+)**: 40% core performers, 30% scaling, 20% diversification, 10% innovation.

**Budget Floor Rules**:
- Minimum $50/day per ad set on Meta for meaningful data.
- Minimum $30/day per campaign on Google Search.
- Never allocate less than 10% of total budget to creative testing.
- Reserve 5% for emergency/opportunistic deployment.

#### 4. Measurement Plan
**Owner**: Burns, Performance Analyst
**Duration**: 1 day

Define what success looks like before spending:

| Level | Metrics | Reporting Cadence |
|-------|---------|-------------------|
| Business | Revenue, profit, LTV, CAC payback period | Monthly |
| Campaign | ROAS, CPA, conversion volume, spend | Weekly |
| Ad Set | CTR, CVR, frequency, CPM, audience saturation | Weekly |
| Ad | Hook rate, hold rate, CTR, CVR | Daily during testing |

**Attribution Model**: Default to platform-reported conversions for optimization decisions. Use CRM/backend data for business truth. Reconcile monthly per `client-ops-handoff.md`.

**North Star Metric**: Define one primary metric the entire team optimizes toward. Typically: Target CPA for lead gen, Target ROAS for ecommerce, or Blended CAC for subscription.

#### 5. Creative Strategy
**Owner**: Pittman, Traffic Chief
**Duration**: 1-2 days

Based on discovery insights, define:

- **Primary angles** to test first (top 3-5 from `creative-angle-matrix.md`)
- **Format mix**: % video, % static, % carousel, % UGC
- **Volume targets**: concepts per month based on budget level
- **Platform-specific adaptations**: what changes between Meta, Google, YouTube
- **Brand voice guidelines**: tone, language boundaries, visual identity in ads

#### 6. Timeline
**Owner**: Traffic Chief
**Duration**: 0.5 days

| Phase | Duration | Key Milestone |
|-------|----------|---------------|
| Discovery | Weeks 1-2 | Discovery synthesis complete |
| Strategy | Week 3 | Strategy document approved |
| Creative Production | Weeks 4-5 | First creative batch ready |
| Account Setup + Tracking | Week 4-5 (parallel) | Accounts live, tracking verified |
| Launch | Week 6 | Campaigns activated |
| Learning Phase | Weeks 6-8 | Baseline data collected |
| Optimization | Weeks 8-10 | First optimization cycle |
| Scaling Decision | Week 10+ | Scale, pivot, or expand |

## Key Concepts

- **Pittman Methodology**: Structure creative strategy around emotional triggers and audience psychology. Every ad must connect to a human truth.
- **Burns Measurement Philosophy**: If you cannot measure it, you cannot improve it. Measurement plan precedes media plan.
- **Strategy Debt**: Launching without a strategy creates technical and strategic debt that compounds monthly. Fix strategy before fixing tactics.
- **Channel-Market Fit**: Not every channel works for every offer. Let discovery data guide channel selection, not assumptions.

## Decision Rules

1. Strategy document requires Traffic Chief sign-off before any campaign builds begin.
2. Never launch on more than 2 channels simultaneously for new clients.
3. Budget allocation must include testing budget — minimum 10% always reserved.
4. North star metric must be agreed upon with client before launch.
5. Creative strategy must include minimum 3 distinct angles — never bet on one.
6. Timeline must be realistic — rushing strategy to meet arbitrary deadlines is prohibited.

## Common Mistakes

- Skipping strategy and jumping straight to campaign building.
- Allocating all budget to proven tactics with nothing reserved for testing.
- Choosing channels based on team preference rather than data.
- Setting measurement plans that only look at platform metrics, ignoring business outcomes.
- Creating strategy in isolation without incorporating discovery findings.
- Overcomplicating the funnel — start simple, add complexity as data justifies it.

## Integration

- Receives inputs from `discovery-layer.md` — all strategy decisions are evidence-based.
- Outputs feed `creative-layer.md` for creative production direction.
- Budget allocation guides `media-buying-layer.md` campaign setup.
- Measurement plan defines `tracking-layer.md` implementation requirements.
- Timeline coordinates all downstream layers.
- Performance benchmarks set foundation for `pacing-and-guardrails.md`.

## Output

- Strategy document with funnel architecture, channel plan, budget allocation, measurement plan, creative strategy, and timeline.
- North star metric definition with target ranges.
- Channel-specific tactical briefs for Media Buyer.
- Creative strategy brief for Ad Midas and Breeze.
- Client-facing strategy presentation for alignment and approval.
- Risk register with mitigation plans for identified strategic risks.
