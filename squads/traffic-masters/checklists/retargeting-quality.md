# Retargeting Quality
> **Type**: Quality Gate
> **Domain**: Audience Strategy
> **Reviewed by**: Media Buyer

## Purpose
Ensures retargeting campaigns are properly segmented, sequenced, and controlled to maximize conversion without annoying or overwhelming prospects. Poor retargeting wastes budget and damages brand perception.

## Checklist

### Window Segmentation
- [ ] Retargeting windows are defined and non-overlapping (e.g., 1-3 days, 4-7 days, 8-14 days, 15-30 days)
- [ ] Each window corresponds to a distinct stage of buyer intent
- [ ] Window definitions are consistent across all platforms
- [ ] Audience sizes per window are viable for delivery (minimum thresholds met)
- [ ] Window strategy is documented with rationale for each segment

### Exclusion Configuration
- [ ] Converters are excluded from retargeting campaigns immediately
- [ ] Each retargeting tier excludes the tiers above it (no audience overlap)
- [ ] Exclusion audiences update dynamically (not stale static lists)
- [ ] Exclusion logic has been tested and verified in platform audience tools
- [ ] Refund or cancellation audiences are handled appropriately

### Messaging Variation
- [ ] Messaging varies based on the prospect's stage and previous interaction
- [ ] Early-stage retargeting focuses on education and trust building
- [ ] Mid-stage retargeting addresses specific objections
- [ ] Late-stage retargeting uses urgency, social proof, and direct offers
- [ ] Messaging does not repeat the exact same ad the prospect already saw

### Frequency Caps
- [ ] Frequency caps are set at the ad set or campaign level
- [ ] Caps are appropriate for each retargeting window (higher for shorter windows)
- [ ] Total cross-campaign frequency for a single user is monitored
- [ ] Frequency cap violations trigger a review of audience size and budget
- [ ] Platform limitations on frequency cap granularity are documented

### Creative Rotation
- [ ] Multiple creative variants are active within each retargeting tier
- [ ] Creatives are rotated to prevent ad blindness
- [ ] Creative format varies (static, video, carousel) within retargeting
- [ ] Winning creatives from prospecting are adapted for retargeting context
- [ ] Creative rotation cadence is faster for small, high-frequency audiences

### DPA Configuration
- [ ] Dynamic Product Ads catalog is connected and synced correctly
- [ ] Product feed is accurate with current prices, availability, and images
- [ ] DPA templates are customized with compelling overlays and text
- [ ] DPA exclusions prevent showing out-of-stock or irrelevant products
- [ ] DPA performance is segmented by product category for optimization

### Sequence Logic
- [ ] Retargeting sequence follows a logical progression toward conversion
- [ ] Each step in the sequence builds on the previous touchpoint
- [ ] Sequence accounts for multiple entry points (ad click, organic visit, email)
- [ ] Users who skip steps are handled gracefully within the sequence
- [ ] Sequence completion rates are tracked for funnel optimization

## Pass/Fail Criteria
All seven sections must pass. Retargeting without proper exclusions and frequency caps risks brand damage and budget waste.

## If Failed
Pause affected retargeting campaigns. Fix exclusion and frequency issues immediately. Review and restructure audience windows before reactivating.

## Related
- `funnel-integrity-quality.md`
- `creative-fatigue-quality.md`
- `campaign-build-quality.md`
