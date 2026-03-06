# Meta Audience Targeting Quality Gate

> Quality gate for Meta audience targeting configuration (custom audiences, lookalikes, broad, exclusions). Must pass before ad sets are activated.

## Section 1: Custom Audience Setup
- [ ] Custom audiences are built from verified, high-quality source data (CRM lists, pixel events, app activity)
- [ ] Customer list audiences have a match rate above 50%; if below, data quality has been investigated
- [ ] Website custom audiences use correct pixel events and appropriate lookback windows (30/60/90/180 days)
- [ ] Engagement custom audiences specify the correct source (Instagram, Facebook Page, Video, Lead Form)
- [ ] Custom audience refresh cadence is documented (auto-updating for pixel-based; manual upload schedule for CRM)

## Section 2: Lookalike Audience Configuration
- [ ] Lookalike source audience contains at least 1,000 users in the source country
- [ ] Lookalike percentage is appropriate: 1-2% for prospecting precision, 3-5% for scale, 6-10% only with justification
- [ ] Lookalike audiences are based on high-value seed audiences (purchasers, high-LTV customers) rather than broad engagement
- [ ] Multiple lookalike tiers are not overlapping within the same campaign without exclusions
- [ ] Lookalike country selection matches the geo-targeting in the media plan

## Section 3: Interest and Behavioral Targeting
- [ ] Interest-based targeting uses validated, relevant interest categories (not overly broad)
- [ ] Detailed targeting expansion is intentionally enabled or disabled with documented rationale
- [ ] Audience size estimate falls within the recommended range (not below 500K for conversion campaigns, not above 50M without justification)
- [ ] Behavioral targeting layers (purchase behavior, device usage) are consistent with the buyer persona

## Section 4: Exclusions and Overlap Prevention
- [ ] Existing customers / past purchasers are excluded from prospecting campaigns
- [ ] Retargeting audiences exclude users who already converted within the attribution window
- [ ] Audience overlap between ad sets is below 30% (checked via Audience Overlap tool)
- [ ] Suppression lists (employees, competitors, existing subscribers) are applied where applicable
- [ ] Negative audiences are refreshed on the same cadence as positive audiences

## Section 5: Compliance and Privacy
- [ ] All custom audiences comply with Meta's Custom Audience Terms of Service
- [ ] Data sources used for audience creation have proper user consent (GDPR/LGPD compliant)
- [ ] No sensitive personal data categories are used in audience targeting (health, race, religion, political affiliation)
- [ ] Audience sharing permissions between ad accounts are documented and authorized

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: If audience overlap exceeds 30% or compliance items fail, targeting must be revised before activation
