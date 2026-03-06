# Client Ops Handoff

> **Type**: Internal
> **Domain**: Operations — Traffic-to-Client Integration
> **Used by agents**: Traffic Chief, Performance Analyst, Media Buyer, Client Operations

## Overview

Defines the communication, data exchange, and operational handoff protocols between the traffic team and client operations. The most common failure point in paid media is not the ads — it is the disconnect between traffic generation and lead handling, sales follow-up, and revenue attribution. This framework prevents silos and ensures closed-loop feedback.

## When to Use

- New client onboarding — establish all handoff protocols from day one
- When lead quality complaints arise from either side
- CRM integration setup or changes
- Attribution discrepancies between ad platform and client data
- Weekly sync meetings — this framework is the agenda template

## The Framework

### Lead Quality Feedback Loop

| Component | Owner | Frequency | Method |
|-----------|-------|-----------|--------|
| Lead delivery confirmation | Traffic Team | Real-time | CRM integration / webhook |
| Lead quality score | Client Ops | Within 48 hours | CRM status update or shared sheet |
| Lead disposition | Client Ops | Weekly | Categorized: Qualified / Unqualified / No Contact / Converted |
| Feedback review | Traffic Team | Weekly | Adjust targeting, creative, or offer based on disposition data |
| Revenue attribution | Client Ops | Monthly | Matched back to campaign/ad set/ad level |

### Quality Scoring Definitions

- **A-Lead (Hot)**: Matches ICP, budget confirmed, decision timeline under 30 days.
- **B-Lead (Warm)**: Matches ICP, budget unclear or timeline 30-90 days.
- **C-Lead (Cool)**: Partial ICP match, needs nurturing, timeline 90+ days.
- **D-Lead (Unqualified)**: Does not match ICP, wrong contact info, spam, or bot.

Traffic team must maintain D-Lead rate below 15%. If exceeded, investigate landing page, targeting, and offer alignment.

### SLA (Service Level Agreements)

| Process | SLA | Escalation |
|---------|-----|-----------|
| Lead response time (client to lead) | Under 5 minutes for hot leads, under 1 hour for all | Traffic Chief flags if response time data shows > 1 hour average |
| Lead quality feedback to traffic team | Within 48 hours of lead delivery | Performance Analyst follows up if no feedback by Day 3 |
| Campaign change requests (client to traffic) | Acknowledged within 4 hours, executed within 24 hours | Traffic Chief if blocked |
| Performance reporting | Weekly report by Monday EOD | Traffic Chief if delayed |
| Budget change requests | Acknowledged within 2 hours, implemented within 12 hours | Immediate escalation if budget-critical |
| Emergency (account issues, major errors) | Response within 1 hour | Direct to Traffic Chief and client stakeholder |

### CRM Integration

**Required Data Flow**:
1. UTM parameters captured on every lead form and purchase event.
2. UTM structure: `utm_source / utm_medium / utm_campaign / utm_content / utm_term`
3. Lead source mapped to campaign and ad set in CRM.
4. Conversion events pushed back to ad platforms via offline conversion import or CAPI.
5. Revenue data associated with lead source for ROAS calculation.

**CRM Sync Checklist**:
- [ ] UTM parameters passing correctly to CRM fields
- [ ] Lead source field populated on every record
- [ ] Duplicate detection active to prevent inflated counts
- [ ] Conversion event firing back to Meta CAPI and Google Ads
- [ ] Revenue field populated and mapped for offline conversion value
- [ ] Test lead submitted and verified end-to-end before campaign launch

### Attribution Reconciliation

Platform-reported conversions will never match CRM data exactly. Acceptable variance: 10-20%.

| Source | Tends to Report | Why |
|--------|----------------|-----|
| Meta Ads Manager | Higher | View-through attribution, modeled conversions, cross-device |
| Google Ads | Higher | Data-driven attribution, conversion modeling |
| CRM / Backend | Lower | Direct, verifiable data. No modeling. |

**Reconciliation Protocol**:
- Monthly comparison of platform-reported vs CRM-reported conversions.
- If variance exceeds 25%, investigate: tracking gaps, UTM breakage, conversion window mismatches.
- Use CRM data as source of truth for revenue. Use platform data for optimization signals.

### Weekly Sync Agenda

1. **Performance Overview** (5 min): Spend, leads, CPA, ROAS vs target.
2. **Lead Quality Report** (10 min): Disposition breakdown, quality trends, feedback on specific campaigns.
3. **Attribution Review** (5 min): Platform vs CRM variance, any discrepancies flagged.
4. **Client Ops Feedback** (10 min): Sales team feedback, market changes, offer adjustments needed.
5. **Action Items** (10 min): What changes this week — creative, targeting, budget, landing page.
6. **Forward Look** (5 min): Upcoming promotions, inventory changes, seasonal adjustments.

## Key Concepts

- **Closed-Loop Reporting**: Traffic generates leads. Ops qualifies them. Revenue is attributed back. This loop must be unbroken.
- **Speed to Lead**: Research shows lead contact within 5 minutes has 10x higher qualification rate than 30-minute response. Traffic team must advocate for client speed.
- **Garbage In, Garbage Out**: If lead quality feedback is not provided, traffic team optimizes on volume, not value. Feedback is non-negotiable.

## Decision Rules

1. No campaign launches without confirmed CRM integration and UTM tracking.
2. Weekly sync meetings are mandatory for the first 90 days. Bi-weekly after if both parties agree.
3. Lead quality feedback must be provided within 48 hours or traffic team escalates.
4. Attribution reconciliation happens monthly — discrepancies over 25% trigger investigation.
5. Budget changes above 20% require 48-hour advance notice from client.
6. Traffic team does not make offer or pricing changes without client written approval.

## Common Mistakes

- Launching campaigns without verifying end-to-end tracking through CRM.
- Client ops team not providing lead quality feedback, leaving traffic team blind.
- Blaming traffic for poor results when lead response time is 4+ hours.
- Not reconciling attribution monthly — small drift becomes large disconnect over time.
- Skipping weekly syncs — problems compound silently.
- Traffic team optimizing for platform metrics instead of business outcomes.

## Integration

- Tracking infrastructure defined in `tracking-layer.md`.
- Performance metrics monitored per `pacing-and-guardrails.md`.
- Lead quality data informs audience refinement in `audience-building-system.md`.
- Reporting structure feeds `optimization-layer.md` and `governance-layer.md`.
- Client communication cadence aligns with `strategy-layer.md` planning.

## Output

- CRM integration checklist (completed at onboarding).
- Weekly sync meeting notes with action items and owners.
- Monthly attribution reconciliation report.
- Lead quality trend report with D-Lead rate tracking.
- SLA compliance tracker updated weekly.
