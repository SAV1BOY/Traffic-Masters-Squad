# Media Buying Layer
> **Type**: Stack Layer
> **Used by agents**: Media Buyer, Pixel Specialist

## Overview
The Media Buying Layer is where strategy and creative become live campaigns. This layer covers account setup, campaign building, audience configuration, creative upload, tracking verification, and launch QA. Execution precision directly impacts data quality, learning phase efficiency, and initial performance. Duration: 2-5 days.

## When to Use
- New client campaign builds (following Strategy and Creative layers)
- New campaign type additions to existing accounts
- Account restructures based on optimization findings
- Platform expansion to new channels
- Seasonal campaign deployments

## The Framework

### Account Setup (Day 1)
- Business Manager / Ad account access verified
- Pixel installed and events verified
- Conversions API configured and sending events
- Payment method added with sufficient limit
- Account spending limit set (2x daily target as safety)
- Domain verified, AEM configured (Meta)
- GA4 linked to Google Ads (Google)
- Product feed uploaded (ecommerce)

### Campaign Build (Days 1-3)
- **Campaign Level**: Objective aligned with strategy, budget type (CBO/ABO), bid strategy, naming convention applied, exclusions set
- **Ad Set / Ad Group Level**: Audience configured, placements selected, targeting set, exclusions applied, naming convention applied
- **Ad Level**: Creative assets uploaded (correct format/resolution/ratio), copy entered, CTA selected, destination URL with UTMs verified, tracking confirmed

### Audience Configuration (Day 2)
- Custom audiences from seed data
- Lookalike audiences from priority seeds
- Interest/in-market audiences configured
- Exclusion audiences applied across campaigns
- Audience overlap checked and resolved
- Retargeting windows configured per Retargeting Architecture

### Tracking Verification (Days 2-3)
- Submit test conversion through entire funnel
- Verify event firing in platform Events Manager
- Confirm UTM parameters pass to CRM/analytics
- Check CAPI event delivery and deduplication
- Test on multiple devices (desktop, mobile, tablet)
- Confirm landing page load time under 3 seconds

### Launch QA (Day 3-4)
- All ads reviewed for policy compliance
- All destination URLs functional and fast-loading
- All tracking pixels firing correctly (verified in last 24 hours)
- Budget and bid settings confirmed against strategy document
- Audience exclusions verified — no overlap between prospecting and retargeting
- Naming conventions consistent across all elements

### Launch Day Protocol
1. Activate campaigns during business hours (not overnight or weekend)
2. Monitor delivery within first 2 hours
3. Check for ad rejections within first 4 hours
4. Verify conversion tracking recording live events
5. Confirm budget pacing on track

## Key Concepts
- Learning phase: Meta needs ~50 conversions/ad set/week, Google needs ~30/campaign/month
- Launch Tuesday-Thursday for best initial data
- Naming discipline is the foundation of reporting
- No campaign goes live without completed tracking verification

## Decision Rules
1. No campaign activates without end-to-end tracking verification
2. Launch only during business hours with 4+ hours monitoring coverage
3. Do not change bids or budgets during learning phase (Days 1-7) unless emergency
4. All ad rejections addressed within 4 hours
5. If >30% of ads rejected, halt launch and audit creative/landing pages

## Integration
- Receives strategy from Strategy Layer and creative from Creative Layer
- Tracking requirements defined in Tracking Layer
- Post-launch monitoring transitions to Optimization Layer
- Account structure follows platform-specific frameworks

## Output
- Campaign build documentation (structure, settings, audiences, creative)
- Pre-launch QA checklist (completed and signed off)
- Launch log with timestamps, observations, and issues
- Post-launch monitoring report (Days 1-7)
- Handoff to Optimization Layer with baseline performance data
