# Retargeting Overhaul Project

## Objective
Rebuild and optimize the retargeting strategy across all platforms.

## Timeline: 3 Weeks

### Week 1: Audit & Redesign
- [ ] Audit current retargeting setup (audiences, creative, performance)
- [ ] Map customer journey touchpoints
- [ ] Define retargeting windows by intent level
- [ ] Design audience exclusion architecture
- [ ] Plan creative sequence by stage

### Week 2: Build & Launch
- [ ] Create retargeting audiences by window
  - [ ] 1-3 day (hot): Cart/checkout abandoners
  - [ ] 7 day (warm): Site visitors, product viewers
  - [ ] 14 day (consideration): Engagers, video viewers
  - [ ] 30 day (nurture): Content consumers
  - [ ] 60+ day (re-engage): Lapsed visitors
- [ ] Develop stage-specific creative
- [ ] Set up dynamic product ads (ecommerce)
- [ ] Configure frequency caps
- [ ] Launch sequenced retargeting campaigns

### Week 3: Optimize
- [ ] Monitor frequency and performance by window
- [ ] Optimize budget allocation across windows
- [ ] Test messaging variations per stage
- [ ] Verify exclusion lists working correctly
- [ ] Compare performance to pre-overhaul baseline

## Retargeting Architecture
Reference: `lib/patterns/retargeting-sequence-patterns.md`

## Creative Per Stage

| Window | Message Type | Creative Format |
|--------|-------------|-----------------|
| 1-3 day | Reminder + incentive | Product-focused DPA |
| 7 day | Social proof | Testimonial video |
| 14 day | Objection handling | FAQ carousel |
| 30 day | Fresh angle | New creative concept |
| 60+ day | Re-education | Value-first content |

## Success Criteria
- Retargeting ROAS improved vs baseline
- Frequency controlled below 4.0 per window
- Clear performance differentiation by window
- No audience overlap issues
