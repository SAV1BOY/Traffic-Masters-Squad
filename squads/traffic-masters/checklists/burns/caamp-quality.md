# CaAMP Methodology Quality Gate

> Quality gate for Depesh Mandalia and Charley T. Burns' CaAMP (Campaign, Audience, Ad, Metrics, Platform) methodology. Must pass before campaign architecture is considered complete.

## Section 1: Campaign Layer
- [ ] Campaign objective is selected based on the desired business outcome, not vanity metrics
- [ ] Campaign structure follows the CaAMP hierarchy (Campaign > Ad Set > Ad)
- [ ] Campaign budget optimization (CBO) vs. ad set budget optimization (ABO) decision is documented with rationale
- [ ] Campaign naming convention encodes objective, date, and test variable
- [ ] Only one objective per campaign (no mixed-objective campaigns)

## Section 2: Audience Layer
- [ ] Audiences are segmented into prospecting (cold) and retargeting (warm/hot) campaigns
- [ ] Prospecting audiences use a mix of interests, lookalikes, and broad targeting
- [ ] Retargeting audiences are built with meaningful engagement windows (not arbitrary)
- [ ] Audience overlap is checked using the platform's overlap tool before launch
- [ ] Exclusion audiences prevent retargeting users from appearing in prospecting campaigns
- [ ] Audience sizes are large enough to support the allocated budget without saturation

## Section 3: Ad Layer
- [ ] Each ad set contains 3-5 ad variations for adequate testing
- [ ] Ad variations test one variable at a time (hook, creative format, CTA)
- [ ] Ad creative includes a strong pattern interrupt in the first 3 seconds (video) or visual (static)
- [ ] Ad copy structure follows hook > story > offer > CTA framework
- [ ] Dynamic creative testing (DCT) is considered for rapid iteration in early testing

## Section 4: Metrics Layer
- [ ] Primary KPI is defined and tied to revenue (CPA, ROAS, cost per lead)
- [ ] Secondary KPIs are tracked but not used for premature optimization (CTR, CPM, CPC)
- [ ] Metric thresholds for winner/loser decisions are set before launch
- [ ] Learning phase exit criteria are documented (50 conversions per week per ad set)
- [ ] Attribution model is selected and consistent across all campaigns

## Section 5: Platform Layer
- [ ] Platform selection is based on where the target audience spends time
- [ ] Platform-specific best practices are applied (aspect ratios, copy lengths, placements)
- [ ] Cross-platform measurement is in place if running on multiple platforms
- [ ] Platform API or CAPI is configured for server-side tracking accuracy

## Approval
- **Minimum pass rate**: 18/22 items (82%)
- **Reviewer**: burns-performance-strategist
- **Escalation**: If audience or metrics layers fail, pause and reconfigure before launching any spend
