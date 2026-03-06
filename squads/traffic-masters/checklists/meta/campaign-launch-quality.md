# Meta Campaign Launch Readiness Quality Gate

> Quality gate for Meta campaign launch readiness. Must pass before the campaign is set to Active in Ads Manager.

## Section 1: Pre-Launch Strategy Validation
- [ ] Campaign brief is signed off by the client or account manager
- [ ] Media plan budget, flight dates, and KPIs are confirmed and documented
- [ ] Campaign objective in Ads Manager matches the approved media plan
- [ ] Target CPA / ROAS goals are defined and entered as bid strategy constraints (if applicable)
- [ ] Funnel stages are mapped: prospecting, retargeting, retention campaigns are distinct

## Section 2: Campaign Structure Verification
- [ ] Campaign structure quality gate has passed (see campaign-structure-quality.md)
- [ ] Audience targeting quality gate has passed (see audience-targeting-quality.md)
- [ ] Creative specs quality gate has passed (see creative-specs-quality.md)
- [ ] Pixel and events quality gate has passed (see pixel-events-quality.md)
- [ ] All ad sets have correct schedule (start/end dates, dayparting if applicable)

## Section 3: Ad Creative Final Review
- [ ] All ads have been previewed in Ads Manager across Feed, Stories, Reels, and Right Column placements
- [ ] Landing page URLs are live, load in under 3 seconds, and display correctly on mobile
- [ ] UTM parameters are appended to all destination URLs and validated (see utm-naming-quality.md)
- [ ] Dynamic creative elements (if used) have been tested for all possible combinations
- [ ] No broken links, 404 errors, or redirect chains in destination URLs

## Section 4: Tracking and Attribution
- [ ] Pixel Helper confirms all events fire correctly on the landing page and conversion pages
- [ ] Attribution window setting matches the reporting requirements (default: 7-day click, 1-day view)
- [ ] Offline conversion import is scheduled (if applicable)
- [ ] Third-party tracking pixels or impression tags are tested and firing (if applicable)

## Section 5: Budget and Billing
- [ ] Payment method on the ad account is active and has sufficient funds / credit limit
- [ ] Daily or lifetime budget matches the approved media plan (within 5% tolerance)
- [ ] Spending limits at account and campaign levels will not block delivery
- [ ] Currency setting on the ad account matches the billing currency

## Section 6: Final Go/No-Go
- [ ] Campaign has been reviewed by a second team member (four-eyes principle)
- [ ] All checklist gates referenced above show passing status
- [ ] Launch date and time are confirmed (avoid launching on weekends or holidays unless intentional)
- [ ] Monitoring alerts are set up for spend pacing, CPM spikes, and disapproved ads
- [ ] Rollback plan is documented (what to pause/kill if performance is off within first 48 hours)

## Approval
- **Minimum pass rate**: 22/25 items (88%)
- **Reviewer**: media-buyer-agent + account-manager-agent
- **Escalation**: Any hard-block item (tracking, billing, or compliance) must be resolved before launch; no exceptions
