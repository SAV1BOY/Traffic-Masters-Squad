# Project Template: New Account Setup

## Project Overview

Setting up a new advertising account from scratch, including platform configuration, tracking implementation, audience building, initial campaign structure, and launch. This template covers the complete process from access provisioning to first campaigns going live.

---

## Objectives

1. Configure ad accounts on all required platforms with proper business verification
2. Implement complete tracking infrastructure (pixels, CAPI, conversion events)
3. Build initial audience assets (custom audiences, exclusion lists)
4. Create and launch initial campaign structure
5. Establish reporting and monitoring dashboards
6. Achieve first conversions within the first week of launch

---

## Timeline

**Total Duration:** 2-4 weeks

| Phase | Duration | Milestone |
|---|---|---|
| Phase 1: Access and Configuration | Days 1-3 | Accounts created and verified |
| Phase 2: Tracking Setup | Days 3-7 | All tracking live and verified |
| Phase 3: Audience and Creative Prep | Days 5-10 | Audiences built, creative ready |
| Phase 4: Campaign Build | Days 8-12 | Campaigns built and reviewed |
| Phase 5: Launch and Monitor | Days 12-14+ | Campaigns live, first data collected |

---

## Team (Agents Involved)

| Role | Responsibility |
|---|---|
| Media Buyer (Lead) | Account structure, campaign build, launch oversight |
| Tracking Specialist | Pixel, CAPI, GTM implementation, QA |
| Creative Strategist | Initial creative direction and asset preparation |
| Creative Producer | Ad creative production (video, static, copy) |
| Account Manager | Client communication, timeline management |
| Analytics Lead | Dashboard setup, baseline measurement |

---

## Phases and Deliverables

### Phase 1: Access and Configuration (Days 1-3)

**Deliverables:**
- [ ] Business Manager / MCC / ad account access provisioned
- [ ] Business verification completed (Meta Business Verification, Google merchant verification)
- [ ] Payment methods configured
- [ ] Team member access granted with appropriate permission levels
- [ ] Platform-specific settings configured (time zone, currency, account spending limits)
- [ ] Domain verification completed (Meta)
- [ ] Merchant Center setup (Google, if e-commerce)
- [ ] Product feed connected and approved (if applicable)

**Quality Gate:** All accounts accessible, verified, and configured. Team members have appropriate access levels.

### Phase 2: Tracking Setup (Days 3-7)

**Deliverables:**
- [ ] Base pixel/tag installed on all pages (Meta Pixel, Google Ads tag, TikTok pixel)
- [ ] Conversion events configured (purchase, lead, add to cart, initiate checkout, page view)
- [ ] Server-side tracking implemented (Meta CAPI, Google Enhanced Conversions)
- [ ] Event deduplication configured and tested
- [ ] Google Tag Manager container set up (if applicable)
- [ ] GA4 property configured with ad platform linking
- [ ] Conversion value passing verified (dynamic values for e-commerce)
- [ ] Test conversions fired and verified in each platform
- [ ] UTM parameter strategy defined and implemented

**Quality Gate:** All conversion events firing correctly, verified via platform diagnostics, tag assistant, and test transactions. Server-side events matching client-side events. Event match quality score above 6/10 (Meta).

### Phase 3: Audience and Creative Prep (Days 5-10)

**Deliverables:**
- [ ] Customer email/phone list uploaded as Custom Audience (Meta, Google, TikTok)
- [ ] Website visitor audiences created (all visitors, key page visitors, time-based segments)
- [ ] Purchaser/lead exclusion audiences created
- [ ] Lookalike/similar audiences built from customer lists
- [ ] Initial creative assets produced (minimum 5 static, 3 video, 3 ad copy variants)
- [ ] Creative assets formatted for all required placements (feed, stories, reels, search)
- [ ] Ad copy written and reviewed (headlines, primary text, descriptions)
- [ ] Landing pages reviewed and approved for conversion readiness

**Quality Gate:** Minimum viable audience portfolio created. Minimum 5 creative assets ready for launch. Landing pages loading correctly with all tracking firing.

### Phase 4: Campaign Build (Days 8-12)

**Deliverables:**
- [ ] Campaign structure built per account architecture plan
- [ ] Prospecting campaigns configured (broad, interest, lookalike as appropriate)
- [ ] Retargeting campaigns configured (website visitors, engagers)
- [ ] Search campaigns built (branded, non-branded, shopping if applicable)
- [ ] Bidding strategies selected and configured
- [ ] Budget allocation set across campaigns
- [ ] Ad creative assigned to appropriate campaigns/ad sets
- [ ] Targeting settings reviewed (geo, age, gender, placements, exclusions)
- [ ] Campaign naming conventions applied
- [ ] Internal review completed (second set of eyes on all settings)

**Quality Gate:** All campaigns reviewed and approved. Budget allocation confirmed. Campaign settings match strategy document. No conflicting audiences or budget errors.

### Phase 5: Launch and Monitor (Days 12-14+)

**Deliverables:**
- [ ] Campaigns launched in staged sequence (tracking campaigns first, then prospecting)
- [ ] First 24-hour performance check completed
- [ ] First 48-hour performance check completed
- [ ] Tracking verified with live traffic (conversions appearing in platforms)
- [ ] Initial performance report shared with stakeholders
- [ ] Monitoring schedule established (daily check-ins for first 2 weeks)
- [ ] First optimization actions documented
- [ ] Week 1 performance summary delivered

**Quality Gate:** Campaigns delivering impressions. Conversion tracking confirmed with real conversions. No critical errors in targeting, budget, or creative. Stakeholders briefed on initial performance.

---

## Success Metrics

| Metric | Target | Measurement |
|---|---|---|
| Account setup completion | All platforms live | Checklist completion |
| Tracking accuracy | 95%+ event match rate | Platform diagnostics |
| Time to first conversion | Within 7 days of launch | Platform reporting |
| Initial CPA | Within 150% of target CPA | Platform reporting (acceptable for learning phase) |
| Creative asset count | 5+ unique assets live | Ad-level count |
| Audience portfolio | 5+ audiences built | Platform audience manager |

---

## Risk Register

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Business verification delays | Medium | High (blocks launch) | Start verification day 1; have backup documents ready |
| Tracking implementation issues | High | High | Test thoroughly before launch; have tracking specialist QA |
| Product feed disapprovals | Medium | Medium | Review product data against platform policies before submission |
| Creative not ready on time | Medium | Medium | Begin creative production in parallel with Phase 1 |
| Payment method issues | Low | High | Set up backup payment method; verify billing before launch |
| Domain/website issues | Low | High | Audit website for policy compliance before account setup |

---

## Dependencies

| Dependency | Owner | Required By |
|---|---|---|
| Website/landing page access | Client / Web team | Phase 2 |
| Customer email/phone lists | Client / CRM team | Phase 3 |
| Product feed (e-commerce) | Client / Dev team | Phase 1 |
| Creative assets (brand guidelines, logos, product images) | Client / Brand team | Phase 3 |
| Budget approval | Client / Finance | Phase 4 |
| Payment method setup | Client / Finance | Phase 1 |
| Google Merchant Center access | Client | Phase 1 |
| Domain DNS access (for verification) | Client / IT | Phase 1 |

---

*Last updated: 2026-03-06*
