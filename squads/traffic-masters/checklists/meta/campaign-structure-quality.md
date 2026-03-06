# Meta Campaign Structure Quality Gate

> Quality gate for Meta campaign structure setup (CBO/ABO, ad sets, naming conventions). Must pass before campaign is published to Meta Ads Manager.

## Section 1: Campaign Objective Alignment
- [ ] Campaign objective (Awareness, Traffic, Engagement, Leads, App Promotion, Sales) matches the business goal documented in the brief
- [ ] Buying type (Auction vs. Reach & Frequency) is appropriate for the campaign goal
- [ ] Special Ad Category declarations (Credit, Employment, Housing, Social Issues) are applied when legally required
- [ ] Campaign spending limits are configured if required by the budget plan

## Section 2: Budget Optimization Strategy
- [ ] CBO (Campaign Budget Optimization) vs. ABO (Ad Set Budget Optimization) choice is justified and documented
- [ ] CBO minimum/maximum spend limits per ad set are configured to prevent budget starvation
- [ ] ABO daily or lifetime budgets per ad set align with the media plan allocations
- [ ] Bid strategy (Lowest Cost, Cost Cap, Bid Cap, ROAS Goal) matches the performance target
- [ ] Bid cap or cost cap values are set based on historical CPA/ROAS benchmarks

## Section 3: Ad Set Configuration
- [ ] Number of ad sets does not exceed 6 per campaign to avoid audience fragmentation
- [ ] Each ad set has a clearly differentiated purpose (audience, placement, or creative test)
- [ ] Ad set start and end dates match the campaign flight dates in the media plan
- [ ] Delivery optimization event aligns with the funnel stage (e.g., Purchase for bottom-funnel, Landing Page Views for mid-funnel)
- [ ] Attribution window is set correctly (7-day click / 1-day view default; adjusted only with justification)

## Section 4: Naming Conventions
- [ ] Campaign name follows the naming convention: [Client]_[Objective]_[Funnel Stage]_[Date]_[Version]
- [ ] Ad set names follow: [Audience Type]_[Targeting Detail]_[Placement]_[Optimization]
- [ ] Ad names follow: [Format]_[Creative Concept]_[Variant]_[CTA]
- [ ] No duplicate names exist within the same campaign
- [ ] Names are free of special characters that may break reporting tools or UTM parameters

## Section 5: Structural Integrity
- [ ] No single ad set contains more than 6 active ads (to allow adequate delivery per creative)
- [ ] Campaign structure supports clean A/B comparison (one variable changed per test)
- [ ] Draft campaign has been reviewed in Ads Manager preview before publishing
- [ ] All ad sets have at least one active ad assigned

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: If fewer than 20 items pass, campaign must be restructured and re-reviewed before launch
