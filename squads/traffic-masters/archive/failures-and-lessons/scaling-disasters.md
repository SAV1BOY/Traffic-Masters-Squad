# Scaling Disasters — Lessons Learned

## Purpose
Document common scaling failures and how to avoid them.

## Disaster 1: Budget Shock
- **What happened:** Budget doubled overnight; CPA tripled
- **Cause:** Algorithm re-entered learning phase, bid competition spiked
- **Lesson:** Never increase budget more than 20-30% per change
- **Prevention:** Gradual scaling, monitor for 48hrs after each increase

## Disaster 2: Creative Fatigue at Scale
- **What happened:** Scaled to $50K/month; performance collapsed after 3 weeks
- **Cause:** Only 2 creatives running, frequency exceeded 5.0
- **Lesson:** Creative pipeline must match spend velocity
- **Prevention:** 3-5 new creatives per week at scale, fatigue monitoring

## Disaster 3: Audience Saturation
- **What happened:** CPA rose 60% over 4 weeks despite stable creative
- **Cause:** Narrow audience of 500K exhausted
- **Lesson:** Audience size must support spend level
- **Prevention:** Calculate reach vs spend ratio, expand before saturation

## Disaster 4: Platform Dependency
- **What happened:** 95% of budget on Meta; iOS 14 hit; revenue dropped 40%
- **Cause:** No platform diversification
- **Lesson:** No single platform should exceed 70% of total spend
- **Prevention:** Cross-platform strategy from day one

## Disaster 5: Scaling Without Tracking
- **What happened:** Scaled to $100K/month; discovered tracking was broken
- **Cause:** Pixel changes during site update broke conversion events
- **Lesson:** Verify tracking before and during scaling
- **Prevention:** Weekly tracking QA, automated monitoring

## Key Principles
1. Scale gradually, not suddenly
2. Creative pipeline must match spend level
3. Diversify across platforms and audiences
4. Verify tracking at every stage
5. Monitor marginal CPA, not just average CPA
