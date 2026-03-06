# Project Template: Retargeting Overhaul

## Project Overview

Rebuilding the retargeting architecture across all platforms to improve efficiency, reduce audience overlap, implement proper segmentation, establish incrementality measurement, and align retargeting strategy with current platform best practices and privacy constraints.

---

## Objectives

1. Audit and restructure retargeting audiences for maximum efficiency
2. Implement proper audience segmentation by intent level and recency
3. Align retargeting creative with audience stage
4. Establish incrementality measurement for retargeting
5. Cap retargeting investment at an appropriate share of total budget
6. Improve true incremental ROAS from retargeting campaigns

---

## Timeline

**Total Duration:** 4-5 weeks

| Phase | Duration | Milestone |
|---|---|---|
| Phase 1: Audit | Days 1-5 | Current retargeting architecture documented |
| Phase 2: Strategy and Design | Days 5-10 | New architecture approved |
| Phase 3: Build | Days 10-17 | New campaigns built |
| Phase 4: Launch and Test | Days 17-28 | New architecture live, incrementality test running |
| Phase 5: Optimize and Report | Days 28-35 | Optimized based on data, report delivered |

---

## Team (Agents Involved)

| Role | Responsibility |
|---|---|
| Media Buyer (Lead) | Retargeting strategy, campaign architecture, optimization |
| Tracking Specialist | Audience pixel events, custom audience configuration |
| Creative Strategist | Stage-specific creative development |
| Creative Producer | Retargeting creative production |
| Analytics Lead | Incrementality testing, cross-channel analysis |
| Account Manager | Client communication |

---

## Phases and Deliverables

### Phase 1: Audit (Days 1-5)

**Deliverables:**
- [ ] Current retargeting architecture mapped:
  - All retargeting audiences listed (per platform)
  - Audience sizes documented
  - Overlap between retargeting audiences calculated
  - Retargeting budget as % of total budget
  - Retargeting frequency analysis (how often are users seeing retargeting ads?)
  - Retargeting creative inventory reviewed
  - Current retargeting CPA/ROAS documented
- [ ] Performance analysis:
  - Retargeting ROAS compared to prospecting ROAS
  - Retargeting contribution to total conversions
  - Time-to-conversion analysis (how quickly do retargeted users convert?)
  - Overlap with email/SMS touchpoints
  - Retargeting spend efficiency by audience segment
- [ ] Issues identified:
  - Audience overlap and cannibalization
  - Over-frequency on specific segments
  - Misaligned creative (same messaging for all retargeting audiences)
  - Budget imbalance (too much or too little in retargeting)
  - Attribution over-claiming (retargeting taking credit for organic returns)
- [ ] Audit summary with key findings and recommendations

**Quality Gate:** Complete audit of current retargeting across all platforms. Key issues documented. Ready to design new architecture.

### Phase 2: Strategy and Design (Days 5-10)

**Deliverables:**
- [ ] New retargeting architecture designed:

  | Segment | Audience | Window | Message | Priority |
  |---|---|---|---|---|
  | Hot | Cart/checkout abandoners | 1-3 days | Recovery, urgency | Highest |
  | Warm-High | Product page viewers | 1-7 days | Benefits, proof | High |
  | Warm-Mid | Category/collection viewers | 1-14 days | Education, variety | Medium |
  | Warm-Low | Blog/content engagers | 1-14 days | Value, trust | Medium |
  | Engagement | Video viewers (50%+) | 1-14 days | Deeper content, offers | Medium |
  | Social | Social engagers | 1-30 days | Community, proof | Lower |
  | Lapsed | Past customers (90+ days) | 90-180 days | Win-back, new products | Variable |

- [ ] Exclusion strategy defined:
  - Recent purchasers excluded from acquisition retargeting (7-30 day window)
  - Higher-intent audiences excluded from lower-intent segments (prevent overlap)
  - Frequency caps set per segment
- [ ] Creative strategy per segment:
  - Cart abandoners: reminder + incentive (if applicable)
  - Product viewers: benefits, testimonials, social proof
  - Category viewers: broader value proposition, product range
  - Content engagers: educational + soft CTA
  - Video viewers: deeper content, demonstration
  - Lapsed customers: new products, win-back offers
- [ ] Budget allocation:
  - Retargeting capped at 15-25% of total ad budget
  - Budget distributed by segment priority
  - Remainder allocated to prospecting
- [ ] Incrementality test design:
  - Holdout group methodology (random 10-20% excluded from retargeting)
  - Geographic holdout methodology (alternative)
  - Success criteria defined
  - Test duration determined (minimum 2 weeks)
- [ ] Architecture approved by stakeholders

**Quality Gate:** New architecture designed with clear segmentation, creative strategy, and budget allocation. Incrementality test plan approved.

### Phase 3: Build (Days 10-17)

**Deliverables:**
- [ ] New audiences created per architecture:
  - Custom audiences built with correct parameters and windows
  - Exclusions configured between segments
  - Audience sizes verified (sufficient for delivery)
  - Naming conventions applied consistently
- [ ] Retargeting creative produced:
  - Minimum 2-3 creative assets per segment
  - Messaging aligned with segment intent level
  - Formats appropriate for platforms (feed, stories, display)
  - Dynamic product ads configured (if e-commerce)
- [ ] Campaign structure built:
  - Campaigns organized by intent tier
  - Ad sets configured with correct audiences and exclusions
  - Budget allocated per strategy
  - Bidding strategies selected (may vary by segment)
  - Frequency caps configured
- [ ] Incrementality test configured:
  - Holdout group or geographic exclusion set up
  - Measurement tracking in place
  - Baseline metrics documented
- [ ] Internal QA review completed

**Quality Gate:** All campaigns built and reviewed. Audiences correctly segmented with proper exclusions. Creative matched to segments. Incrementality test ready to launch.

### Phase 4: Launch and Test (Days 17-28)

**Deliverables:**
- [ ] New retargeting architecture launched
- [ ] Old retargeting campaigns paused (or transitioned gradually)
- [ ] Monitoring during transition:
  - Day 1-3: verify delivery, check for audience issues
  - Day 3-7: initial performance comparison vs. old architecture
  - Day 7-14: performance stabilization, initial optimization
- [ ] Incrementality test running:
  - Holdout group data collecting
  - Conversion tracking for both test and control groups
  - No contamination between groups
- [ ] Performance by segment tracked:
  - CPA/ROAS by retargeting segment
  - Frequency by segment
  - Creative performance within each segment
  - Budget utilization by segment
- [ ] First optimization cycle:
  - Underperforming creative swapped
  - Budget shifted between segments based on performance
  - Frequency adjustments if needed

**Quality Gate:** New architecture delivering for 14+ days. No critical issues. Incrementality test running clean.

### Phase 5: Optimize and Report (Days 28-35)

**Deliverables:**
- [ ] Incrementality analysis completed:
  - Comparison of holdout group vs. retargeted group conversion rates
  - True incremental lift calculated
  - Incremental CPA/ROAS calculated (may differ significantly from reported)
  - Recommendation for retargeting budget based on true incrementality
- [ ] Performance optimization:
  - Top-performing segments identified and prioritized
  - Underperforming segments adjusted or paused
  - Creative refresh based on 2-week performance data
  - Budget rebalanced based on incremental contribution
- [ ] Final retargeting architecture report:
  - Before vs. after performance comparison
  - Segment-level performance analysis
  - Incrementality test results
  - Optimized budget allocation
  - Ongoing management recommendations
  - Creative refresh schedule
- [ ] Handoff to ongoing management:
  - Updated audience management procedures
  - Creative refresh cadence documented
  - Incrementality testing schedule (recommended quarterly)
  - Monitoring dashboards configured

**Quality Gate:** Incrementality results documented. Architecture optimized based on data. Ongoing management plan established. Report delivered to stakeholders.

---

## Success Metrics

| Metric | Target | Measurement |
|---|---|---|
| Retargeting as % of total budget | 15-25% (down from higher if over-invested) | Budget analysis |
| Incremental conversion rate lift | Measurable lift vs. holdout group | Incrementality test |
| Audience overlap reduction | <10% overlap between segments | Platform overlap tool |
| Frequency management | <5x/week per user | Platform frequency reports |
| Retargeting incremental ROAS | Positive incremental return | Incrementality test |
| Segment-level performance | CPA varies by segment (hot > warm > cold) | Platform reporting |

---

## Risk Register

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Short-term performance dip during transition | High | Medium | Transition gradually; do not pause old campaigns until new ones are stable |
| Audience sizes too small for some segments | Medium | Medium | Combine similar segments if individual sizes are insufficient |
| Incrementality test shows low lift | Medium | High | This is valuable data; use it to right-size retargeting budget |
| Dynamic product ads disapproved | Medium | Medium | Review product feed for policy compliance before launch |
| Cross-channel retargeting overlap | Medium | Medium | Document retargeting across platforms; manage total frequency |

---

## Dependencies

| Dependency | Owner | Required By |
|---|---|---|
| Pixel events for all audience types | Tracking specialist | Phase 3 |
| Product feed for dynamic ads | Client / E-commerce team | Phase 3 |
| Segment-specific creative assets | Creative team | Phase 3 |
| Incrementality test budget approval | Client / Finance | Phase 2 |
| Email/SMS coordination (avoid overlap) | Client / Email team | Phase 4 |

---

*Last updated: 2026-03-06*
