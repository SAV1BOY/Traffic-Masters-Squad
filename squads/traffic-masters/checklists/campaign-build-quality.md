# Campaign Build Quality
> **Type**: Quality Gate
> **Domain**: Campaign Setup
> **Reviewed by**: Media Buyer

## Purpose
Ensures every campaign is built correctly in the ad platform before going live. Misconfigured campaigns waste budget, corrupt data, and delay optimization.

## Checklist

### Naming Conventions
- [ ] Campaign name follows the team naming convention format
- [ ] Ad set or ad group names follow the naming convention
- [ ] Ad names include creative variant identifiers
- [ ] UTM parameters in URLs match the naming convention
- [ ] Naming allows for easy filtering and reporting in the platform

### Campaign Structure
- [ ] Campaign structure matches the documented strategy (TOF/MOF/BOF split)
- [ ] Campaign objective aligns with the actual goal (conversions, leads, traffic)
- [ ] Number of ad sets matches the testing plan
- [ ] Number of ads per ad set follows best practices (3-5 per ad set)
- [ ] No duplicate campaigns or ad sets exist from copy errors

### Audience Configuration
- [ ] Target audiences match the strategy document exactly
- [ ] Lookalike audiences are built from the correct seed lists
- [ ] Custom audiences use the correct source and recency window
- [ ] Interest and behavior targeting is documented and intentional
- [ ] Geographic and language targeting is correct

### Exclusions
- [ ] Existing customers or converters are excluded from prospecting
- [ ] Audiences across ad sets are properly excluded to prevent overlap
- [ ] Negative keywords are applied (for search campaigns)
- [ ] Placement exclusions are set where appropriate

### Budget Configuration
- [ ] Daily or lifetime budget matches the approved budget plan
- [ ] Budget distribution across ad sets is intentional
- [ ] Minimum budget per ad set meets platform learning requirements
- [ ] Campaign spending limits are set as a safety net

### Bidding Strategy
- [ ] Bid strategy is documented with rationale (auto, manual, cap, target)
- [ ] Cost cap or bid cap values are set based on unit economics
- [ ] Bid strategy aligns with campaign maturity and data volume
- [ ] Bid adjustments are applied where relevant (device, location, time)

### Tracking Verification
- [ ] Pixel or conversion tag fires correctly on all conversion events
- [ ] CAPI events are sending and matching with pixel events
- [ ] UTM parameters are present and correct in all destination URLs
- [ ] Test conversions have been verified in the platform events manager
- [ ] Attribution settings match the measurement plan

### Creative Approval
- [ ] All creatives have been reviewed and approved by the strategist
- [ ] Creative assets meet platform specifications (size, format, duration)
- [ ] Ad copy has been proofread and is error-free
- [ ] Destination URLs are correct and functional
- [ ] Dynamic creative elements are correctly configured if used

## Pass/Fail Criteria
All checklist items must pass before the campaign goes live. No exceptions for tracking or audience configuration items.

## If Failed
Pause the campaign if already live. Document the misconfiguration, fix it, and re-verify with a second reviewer before reactivating.

## Related
- `creative-brief-quality.md`
- `tracking-plan-quality.md`
- `pixel-and-capi-quality.md`
- `budget-pacing-quality.md`
