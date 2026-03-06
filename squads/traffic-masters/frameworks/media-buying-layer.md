# Media Buying Layer

> **Type**: Stack Layer
> **Domain**: Campaign Execution and Deployment
> **Used by agents**: Media Buyer, Pixel Specialist, Traffic Chief

## Overview

The Media Buying Layer is where strategy and creative become live campaigns. This layer covers account setup, campaign building, audience configuration, ad upload, tracking verification, and launch quality assurance. Execution precision at this layer directly impacts data quality, learning phase efficiency, and initial performance. A misconfigured campaign wastes both budget and time.

## When to Use

- New client campaign builds (following Strategy and Creative layers)
- New campaign type additions to existing accounts
- Account restructures based on optimization findings
- Platform expansion to new channels
- Seasonal campaign deployments (BFCM, product launches)

## The Framework

### Pre-Launch Checklist

#### Account Setup (Day 1)
**Owner**: Media Buyer, Pixel Specialist

**Meta**:
- [ ] Business Manager configured with proper admin access
- [ ] Ad account created or access verified
- [ ] Pixel installed and events verified via Events Manager
- [ ] Conversions API (CAPI) configured and sending events
- [ ] Payment method added with sufficient limit
- [ ] Account spending limit set (2x daily target as safety net)
- [ ] Custom conversions created if needed
- [ ] Domain verified for attribution
- [ ] Aggregated Event Measurement configured (iOS priority events)

**Google**:
- [ ] Google Ads account created or access verified
- [ ] Conversion tracking installed (Google tag + enhanced conversions)
- [ ] GA4 linked to Google Ads
- [ ] Google Merchant Center connected (ecommerce)
- [ ] Product feed uploaded and approved (Shopping/PMax)
- [ ] Billing configured
- [ ] Conversion goals set with proper attribution window
- [ ] Audiences imported from GA4

#### Campaign Build (Days 1-3)
**Owner**: Media Buyer

Follow account structure per `account-structure-meta.md` or `account-structure-google.md`.

**Campaign Level**:
- Campaign objective aligned with strategy (Conversions, Sales, Leads)
- Budget type selected (CBO or ABO per framework rules)
- Daily or lifetime budget set
- Campaign naming convention applied
- Bid strategy configured (lowest cost, cost cap, or target ROAS)
- Campaign-level exclusions set

**Ad Set / Ad Group Level**:
- Audience configured per `audience-building-system.md`
- Placements selected (Advantage+ or manual per strategy)
- Age, gender, location targeting set
- Exclusions applied (existing customers, other audience overlaps)
- Schedule set (if dayparting specified in strategy)
- Ad set naming convention applied

**Ad Level**:
- Creative assets uploaded (correct format, resolution, aspect ratio)
- Primary text, headline, description copy entered
- CTA button selected
- Destination URL with UTM parameters verified
- Tracking pixel confirmed on destination page
- Ad naming convention applied
- Dynamic creative configured if applicable per `dynamic-creative-optimization.md`

#### Audience Configuration (Day 2)
**Owner**: Media Buyer

- Custom audiences created from seed data
- Lookalike audiences generated from priority seeds
- Interest/in-market audiences configured
- Exclusion audiences applied across campaigns
- Audience overlap checked and resolved
- Retargeting windows configured per `retargeting-sequence-system.md`

#### Tracking Verification (Days 2-3)
**Owner**: Pixel Specialist, Media Buyer

- Submit test conversion through entire funnel
- Verify event firing in platform Events Manager
- Confirm UTM parameters pass to CRM/analytics
- Check CAPI event delivery and deduplication
- Verify Google Ads conversion import from GA4
- Test on multiple devices (desktop, mobile, tablet)
- Confirm landing page load time under 3 seconds
- Validate thank-you/confirmation page tracking

### Launch Protocol

#### Pre-Launch QA (Day 3-4)

**Final Verification Checklist**:
- [ ] All ads reviewed for policy compliance
- [ ] All destination URLs functional and fast-loading
- [ ] All tracking pixels firing correctly (verified in last 24 hours)
- [ ] Budget and bid settings confirmed against strategy document
- [ ] Audience exclusions verified — no overlap between prospecting and retargeting
- [ ] Naming conventions consistent across all campaign elements
- [ ] Creative QA passed — per `creative-production-pipeline.md`
- [ ] Emergency contacts and escalation path confirmed

#### Launch Day (Day 4-5)

1. Activate campaigns during business hours (not overnight or weekend).
2. Monitor delivery within first 2 hours — confirm impressions flowing.
3. Check for ad rejections within first 4 hours — resolve immediately.
4. Verify conversion tracking is recording live events (not just test events).
5. Confirm budget pacing — daily spend rate on track.
6. Document launch time, initial observations, and any issues in campaign log.

#### Post-Launch Monitoring (Days 5-7)

- **Hour 1-4**: Confirm delivery, check rejections, verify tracking.
- **Day 1**: Review spend pacing, CPM range, initial engagement metrics.
- **Day 2**: First performance check — CTR, CPC, delivery consistency.
- **Day 3**: Early performance assessment — conversion tracking verified, initial CPA/ROAS.
- **Day 5-7**: Learning phase assessment — are ad sets exiting learning? Sufficient conversion volume?

## Key Concepts

- **Learning Phase**: Meta requires ~50 conversions per ad set per week. Google requires ~30 conversions per campaign per month. Do not make changes during learning (first 3-7 days).
- **Launch Window**: Launch Tuesday through Thursday for best initial data. Avoid Friday launches (weekend behavior differs, team coverage reduced).
- **Naming Discipline**: Naming conventions are not optional. They are the foundation of reporting and analysis. Inconsistent naming makes optimization impossible at scale.
- **Budget Buffer**: Set account spending limits 2x above daily target. This catches runaway spend without being so tight that it pauses campaigns during high-performance periods.

## Decision Rules

1. No campaign goes live without completed tracking verification — non-negotiable.
2. Launch only during business hours when team can monitor for 4+ hours post-launch.
3. Do not make bid or budget changes during learning phase (Days 1-7) unless emergency.
4. All ad rejections must be addressed within 4 hours of detection.
5. If more than 30% of ads are rejected, halt launch and audit creative/landing pages.
6. Post-launch monitoring follows `pacing-and-guardrails.md` alert protocols.

## Common Mistakes

- Launching without verifying tracking end-to-end with a test conversion.
- Setting budgets too low for ad sets to exit learning phase.
- Forgetting audience exclusions, causing prospecting and retargeting to compete.
- Launching on Friday evening or weekends with no monitoring coverage.
- Not checking mobile rendering of ads and landing pages.
- Copying campaigns without updating UTMs, causing attribution errors.
- Skipping the QA checklist because "everything looks fine."

## Integration

- Receives strategy from `strategy-layer.md` and creative from `creative-layer.md`.
- Account structure follows `account-structure-meta.md` and `account-structure-google.md`.
- Audience configuration per `audience-building-system.md`.
- Retargeting setup per `retargeting-sequence-system.md`.
- Tracking requirements defined in `tracking-layer.md`.
- Post-launch monitoring transitions to `optimization-layer.md`.
- Performance data feeds `pacing-and-guardrails.md`.

## Output

- Campaign build documentation (structure, settings, audiences, creative assignments).
- Pre-launch QA checklist (completed and signed off).
- Launch log with timestamps, initial observations, and issues.
- Post-launch monitoring report (Days 1-7).
- Handoff to optimization layer with baseline performance data.
