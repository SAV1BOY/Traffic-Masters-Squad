# Campaign Launch Pattern

## Purpose
Reusable step-by-step pattern for launching paid traffic campaigns with proper structure, validation, and monitoring protocols.

---

## Pattern Overview

```
PRE-LAUNCH (Days -7 to -1)
    |
    v
LAUNCH DAY (Day 0)
    |
    v
LEARNING PHASE (Days 1-7)
    |
    v
EARLY OPTIMIZATION (Days 8-14)
    |
    v
STEADY STATE (Day 15+)
```

---

## Phase 1: Pre-Launch (Days -7 to -1)

### Strategy Validation
- [ ] Campaign objective defined and aligned with business goals
- [ ] Target KPIs set (CPA target, ROAS target, volume targets)
- [ ] Budget allocated and approved
- [ ] Timeline and flight dates confirmed

### Account Setup
- [ ] Campaign structure designed (campaign > ad set > ad hierarchy)
- [ ] Naming conventions applied per standard
- [ ] Bid strategy selected and configured
- [ ] Budget set at campaign or ad set level as appropriate

### Audience Setup
- [ ] Target audiences built and validated (size checks)
- [ ] Exclusions applied (existing customers, internal traffic, past converters)
- [ ] Audience overlap checked (avoid competing ad sets)
- [ ] Geographic and demographic targeting confirmed

### Creative Preparation
- [ ] Minimum 3-5 creative variations per ad set
- [ ] All formats and sizes prepared per platform spec
- [ ] Ad copy reviewed and approved
- [ ] Creative briefs completed and signed off

### Tracking and Measurement
- [ ] Pixel / CAPI events verified (test events firing correctly)
- [ ] Conversion events mapped to campaign objectives
- [ ] UTM parameters built and tested
- [ ] Attribution window configured
- [ ] Analytics goals/events confirmed in GA4 or analytics platform
- [ ] Baseline metrics documented for comparison

### Landing Page / Destination
- [ ] Landing page live and tested across devices
- [ ] Page load speed < 3 seconds
- [ ] Form / checkout working correctly
- [ ] Message match between ad and landing page confirmed
- [ ] Thank you / confirmation page tracking fires

### Compliance
- [ ] Ad content reviewed for platform policy compliance
- [ ] Required disclaimers included
- [ ] Image/video text ratio checked (Meta < 20% text recommended)
- [ ] Special ad category selected if applicable (housing, credit, employment)

---

## Phase 2: Launch Day (Day 0)

### Launch Sequence

1. **Final check:** Review all settings one more time before publishing
2. **Publish campaigns:** Set to active (or schedule for optimal time)
3. **Verify delivery:** Within 1-2 hours, confirm impressions are being served
4. **Check tracking:** Verify conversion events are firing in real-time
5. **Monitor spend:** Ensure budget is pacing as expected
6. **Document:** Log launch time, initial settings, and any notes

### Launch Day Monitoring Checklist

| Check | Time | What to Look For |
|---|---|---|
| Delivery started | +1 hour | Impressions > 0, spend accumulating |
| Ads approved | +2 hours | All ads approved by platform (no rejections) |
| Tracking firing | +2 hours | Test conversion events in Events Manager / GA4 |
| Spend pacing | +4 hours | Spend on track for daily budget |
| No errors | +4 hours | No ad rejections, billing issues, or policy flags |
| End of day review | End of day | CTR, CPC, CPM in expected range |

### If Issues Arise on Launch Day

| Issue | Action |
|---|---|
| Ads not delivering | Check audience size, bid, budget, ad approval status |
| Ads rejected | Review rejection reason, edit and resubmit or appeal |
| Spend too fast | Check bid caps, verify budget is daily not lifetime |
| Spend too slow | Increase budget slightly, broaden audience, check bid |
| No conversions tracking | Verify pixel, CAPI, event mapping in test mode |
| High CPM | Normal for learning phase; monitor but don't react yet |

---

## Phase 3: Learning Phase (Days 1-7)

### Key Rules During Learning

1. **Do NOT make changes** during the first 3-5 days (let the algorithm learn)
2. **Do NOT judge performance** based on < 50 conversion events
3. **Monitor but resist optimizing** unless there is a critical issue
4. **Document observations** daily for use in optimization phase

### Daily Monitoring During Learning

| Metric | What to Watch | Action Trigger |
|---|---|---|
| Spend | Is it spending the full daily budget? | If < 50% of budget, investigate |
| CPM | Is it in expected range for platform/audience? | If 3x+ benchmark, check audience overlap |
| CTR | Is creative generating clicks? | If < 0.3% (Meta feed), creative may be weak |
| CPC | Is traffic cost reasonable? | Monitor, don't act yet |
| Conversions | Are conversions starting to come in? | If zero after 3 days with 1,000+ clicks, check funnel |
| CPA | What is initial CPA trending toward? | Do not react until 20+ conversions |

### Exit Criteria for Learning Phase
- Campaign has exited platform "Learning" status
- OR 50+ conversion events have been recorded
- OR 7 full days have elapsed
- Minimum: 1,000 impressions per ad, 50+ clicks per ad set

---

## Phase 4: Early Optimization (Days 8-14)

### Assessment

| Question | If Yes | If No |
|---|---|---|
| CPA within target? | Continue, consider scaling | Diagnose: creative, audience, or funnel issue? |
| ROAS above break-even? | Continue, monitor trend | Check AOV, CVR, and funnel drop-offs |
| CTR above benchmark? | Creative is working | Test new hooks and angles |
| Sufficient volume? | Maintain or scale | Expand audiences or increase budget |

### Optimization Actions (Priority Order)

1. **Pause losers:** Turn off ad sets with CPA > 2x target (if 20+ conversions)
2. **Identify winners:** Note top-performing creative and audience combinations
3. **Creative iteration:** Launch 2-3 new variations inspired by top performers
4. **Budget shift:** Move budget from underperformers to winners
5. **Audience refinement:** Narrow or expand based on data

### What NOT to Do
- Do not change multiple variables simultaneously
- Do not increase budget more than 20% at once
- Do not change bid strategy mid-flight without reason
- Do not add/remove audiences from performing ad sets

---

## Phase 5: Steady State (Day 15+)

### Ongoing Cadence

| Frequency | Activity |
|---|---|
| Daily | Check spend pacing, CPA/ROAS, flag anomalies |
| 2-3x/week | Review creative performance, pause fatigued creatives |
| Weekly | Full performance review, optimization adjustments |
| Bi-weekly | Launch new creative variations |
| Monthly | Full campaign assessment, budget reallocation, strategy review |

### Scaling Criteria
Before scaling, confirm:
- [ ] CPA has been stable or declining for 5+ days
- [ ] ROAS is above target for 5+ days
- [ ] Creative is not showing fatigue signals
- [ ] Audience is not saturated (frequency < 3.0)

### Scaling Method
- Increase budget by 15-20% maximum per increment
- Wait 3-4 days between increases
- Monitor marginal CPA after each increase
- If CPA spikes > 25% after increase, revert and stabilize

---

## Launch Pattern Checklist (Summary)

```
PRE-LAUNCH:
  [ ] Strategy and KPIs defined
  [ ] Account structure built
  [ ] Audiences configured with exclusions
  [ ] Creatives prepared (3-5 per ad set)
  [ ] Tracking verified
  [ ] Landing page tested
  [ ] Compliance reviewed

LAUNCH DAY:
  [ ] Campaigns activated
  [ ] Delivery confirmed
  [ ] Tracking verified live
  [ ] Pacing checked
  [ ] No rejections or errors

LEARNING (Days 1-7):
  [ ] Hands-off (no major changes)
  [ ] Daily monitoring logged
  [ ] Waiting for 50+ conversions

EARLY OPTIMIZATION (Days 8-14):
  [ ] Losers paused
  [ ] Winners identified
  [ ] New creative launched
  [ ] Budget shifted to performers

STEADY STATE (Day 15+):
  [ ] Regular monitoring cadence
  [ ] Creative refresh cycle active
  [ ] Scaling when criteria met
```
