# Attribution Setup Project

## Objective
Implement a multi-source attribution system for accurate cross-channel measurement.

## Timeline: 3-4 Weeks

### Week 1: Assessment
- [ ] Document current attribution setup
- [ ] Identify data gaps and blind spots
- [ ] Define attribution requirements and goals
- [ ] Evaluate third-party attribution tools
- [ ] Plan server-side tracking enhancements

### Week 2: Platform Attribution
- [ ] Configure platform-specific attribution settings
  - [ ] Meta: CAPI + offline conversions
  - [ ] Google: Enhanced Conversions + consent mode
  - [ ] TikTok: Events API
- [ ] Set attribution windows appropriate to sales cycle
- [ ] Enable data-driven attribution where available
- [ ] Configure offline conversion imports

### Week 3: Independent Attribution
- [ ] Implement third-party attribution tool (if selected)
- [ ] Set up UTM framework for consistent tracking
- [ ] Configure GA4 as cross-channel source of truth
- [ ] Build blended metrics dashboard (MER, nCAC)
- [ ] Set up incrementality test framework

### Week 4: Validation & Documentation
- [ ] Cross-check data between sources
- [ ] Validate accuracy of attribution models
- [ ] Document attribution methodology and limitations
- [ ] Train team on reading attribution data
- [ ] Set up ongoing monitoring and QA

## Attribution Triangulation
1. **Platform data:** Each platform's reported conversions
2. **Independent tool:** Third-party attribution (Northbeam, Triple Whale)
3. **Blended metrics:** MER (total revenue / total marketing spend)
4. **Incrementality:** Geo-based or holdout tests for causal measurement

## Success Criteria
- All platforms tracked with server-side implementation
- Cross-channel dashboard operational
- Blended metrics calculated and monitored
- Team trained on attribution methodology
- First incrementality test planned
