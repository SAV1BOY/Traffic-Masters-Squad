# Google Ads Account Structure Quality Gate

> Quality gate for Google Ads account structure and organization. Must pass before new campaigns are built or during account restructuring.

## Section 1: Account-Level Configuration
- [ ] Billing country, currency, and time zone are correct and match the client's requirements
- [ ] Auto-tagging is enabled for Google Analytics integration (GCLID appended to URLs)
- [ ] Account-level automated extensions are reviewed and unwanted ones are disabled
- [ ] Cross-account conversion tracking is configured if using an MCC (Manager account)
- [ ] Account access levels are appropriate: Admin, Standard, Read-Only assigned per role

## Section 2: Campaign Organization
- [ ] Campaigns are organized by: objective (Brand vs. Non-Brand), funnel stage, product/service line, or geography
- [ ] No more than 20-30 active campaigns per account (to maintain manageable oversight)
- [ ] Each campaign has a single clear objective (not mixing Search and Display goals)
- [ ] Campaign names follow a consistent naming convention: [Client]_[Channel]_[Objective]_[Targeting]_[Date]
- [ ] Campaign labels are applied for cross-cutting categorization (e.g., "Q1-2026", "Promo-BlackFriday")

## Section 3: Budget Architecture
- [ ] Shared budgets are used only for campaigns with similar goals and CPAs
- [ ] Brand campaigns have dedicated budgets separate from non-brand campaigns
- [ ] Budget allocation follows the 70/20/10 rule: 70% proven, 20% scaling, 10% testing
- [ ] Monthly budget pacing is tracked against the media plan (daily spend x days remaining)
- [ ] Budget alerts are configured at the account and campaign level

## Section 4: Conversion Goal Architecture
- [ ] Primary conversion actions are defined and assigned to the correct campaigns
- [ ] Secondary (observation-only) conversion actions are marked as "Secondary" to avoid polluting bidding
- [ ] Conversion action sets are used to assign different goals to different campaigns
- [ ] Micro-conversions (Add to Cart, Form Start) are tracked as secondary actions
- [ ] Conversion value rules are configured for audience-based value adjustments (if applicable)

## Section 5: Audience and Asset Libraries
- [ ] Remarketing lists are created and shared across relevant campaigns (All Visitors, Cart Abandoners, Purchasers)
- [ ] Customer Match lists are uploaded and refreshed on a regular schedule
- [ ] Combined audiences (AND/OR/NOT logic) are built for precise targeting
- [ ] Shared negative keyword lists are maintained and applied to appropriate campaigns
- [ ] Asset library contains approved images, logos, and videos for Responsive ads and extensions

## Section 6: Governance and Hygiene
- [ ] Change history is reviewed weekly for unauthorized or unintended changes
- [ ] Recommendations tab auto-apply settings are reviewed (most should be disabled)
- [ ] Account-level IP exclusions are configured to block known invalid traffic sources
- [ ] Third-party tool integrations (SA360, scripts, APIs) are documented and access is controlled

## Approval
- **Minimum pass rate**: 21/25 items (84%)
- **Reviewer**: media-buyer-agent + account-manager-agent
- **Escalation**: Incorrect billing/currency settings or missing conversion goal architecture are hard blocks; must be fixed before any campaign activation
