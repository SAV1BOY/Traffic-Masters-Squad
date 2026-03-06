# Budget Scaling Pattern

## Purpose
Structured pattern for safely increasing campaign budgets while preserving performance. Prevents common scaling failures such as CPA spikes, learning phase resets, and audience saturation.

---

## Scaling Decision Framework

### Before You Scale, Confirm

| Prerequisite | Threshold | Status |
|---|---|---|
| CPA stable or declining | 5+ consecutive days below target | `{{MET/NOT MET}}` |
| ROAS above target | 5+ consecutive days | `{{}}` |
| Sufficient conversion volume | 50+ conversions in evaluation period | `{{}}` |
| Creative not fatigued | CTR stable, frequency < 3.0 | `{{}}` |
| Audience not saturated | Frequency < 2.5, reach growing | `{{}}` |
| Funnel healthy | No drop-off regressions at any stage | `{{}}` |
| Budget approved | Client/stakeholder approval | `{{}}` |

**Rule:** Do not scale unless at least 5 of 7 prerequisites are met.

---

## Scaling Methods

### Method 1: Gradual Budget Increase (Safest)

**How:** Increase daily budget by 15-20% every 3-4 days.

```
Day 0:  $100/day (baseline)
Day 4:  $120/day (+20%)
Day 8:  $144/day (+20%)
Day 12: $173/day (+20%)
Day 16: $207/day (+20%)
Day 20: $249/day (+20%)
```

**Result:** 2.5x budget in ~20 days with minimal disruption.

**Best for:** Campaigns with strong, stable performance. Works on all platforms.

**Watch for:** CPA increase > 15% after any increment -- pause scaling and stabilize.

### Method 2: Horizontal Scaling (Medium Risk)

**How:** Duplicate winning ad sets into new campaigns with fresh budgets, targeting new audience segments.

```
Campaign A (Original): $100/day - LAL 1% Purchasers
Campaign B (New):      $100/day - LAL 1% Leads
Campaign C (New):      $100/day - Interest Stack A
Campaign D (New):      $100/day - Broad Targeting
```

**Result:** 4x total spend without touching original campaign.

**Best for:** When you want to scale quickly without resetting learning on winners. Good for Meta Ads.

**Watch for:** Audience overlap between campaigns causing auction competition.

### Method 3: CBO Scaling (Platform-Assisted)

**How:** Move winning ad sets into a Campaign Budget Optimization (CBO) campaign with a higher total budget. Let the platform allocate.

```
CBO Campaign Budget: $500/day
  Ad Set 1: Winner A (no ad set budget cap)
  Ad Set 2: Winner B (no ad set budget cap)
  Ad Set 3: New Test Audience
```

**Best for:** Meta Ads. Lets the algorithm find the best distribution.

**Watch for:** Platform may heavily favor one ad set; use minimum spend if needed.

### Method 4: Launch New Campaign (Clean Slate)

**How:** Create an entirely new campaign with the winning creative and audience recipe, starting with a fresh budget.

**Best for:** When the original campaign is too old or has accumulated too much negative signal. Also useful for seasonal pushes.

**Watch for:** New campaign enters learning phase; expect 5-7 days of instability.

### Method 5: Advantage+ / PMax Scaling

**How:** Add budget to Advantage+ Shopping Campaigns (Meta) or Performance Max (Google), which use broad targeting with algorithmic optimization.

**Best for:** Scaling beyond audience targeting limits. Requires strong conversion data (50+ conversions/week).

**Watch for:** Less control over audience targeting; monitor new customer vs. existing customer mix.

---

## Scaling Speed Guide

| Current Daily Budget | Max Single Increase | Wait Period | Max Weekly Increase |
|---|---|---|---|
| $0 - $100 | 50% | 2-3 days | 100% |
| $100 - $500 | 20-30% | 3-4 days | 40-50% |
| $500 - $2,000 | 15-20% | 3-4 days | 30-40% |
| $2,000 - $10,000 | 10-15% | 4-5 days | 20-30% |
| $10,000+ | 10% | 5-7 days | 15-20% |

**Why slower at higher budgets:** Larger absolute dollar increases mean more auction pressure and faster audience saturation.

---

## Monitoring During Scaling

### Daily Checklist During Scale

| Metric | Pre-Scale Baseline | Current | Change | Acceptable Range |
|---|---|---|---|---|
| Daily Spend | $`{{}}` | $`{{}}` | `{{}}`% | Within budget |
| CPA | $`{{}}` | $`{{}}` | `{{}}`% | < +25% from baseline |
| ROAS | `{{}}`x | `{{}}`x | `{{}}`% | > break-even |
| CTR | `{{}}`% | `{{}}`% | `{{}}`% | < -15% from baseline |
| CPM | $`{{}}` | $`{{}}` | `{{}}`% | < +30% from baseline |
| Frequency | `{{}}` | `{{}}` | `{{}}` | < 3.0 (prospecting) |
| Conversion Volume | `{{}}` | `{{}}` | `{{}}`% | Growing proportionally |

### Scaling Abort Triggers

| Signal | Threshold | Action |
|---|---|---|
| CPA increases > 25% for 2+ days | Critical | Revert to previous budget |
| ROAS drops below break-even | Critical | Reduce budget 20%, diagnose |
| CTR drops > 30% | Warning | Check creative fatigue, frequency |
| CPM spikes > 50% | Warning | Check audience saturation, competition |
| Frequency exceeds 4.0 | Warning | Expand audience or launch new creative |
| Conversions don't scale with spend | Warning | Diminishing returns -- cap this audience |

---

## Diminishing Returns Detection

### Marginal CPA Analysis
```
Marginal CPA = Change in Spend / Change in Conversions
```

| Spend Level | Conversions | Avg. CPA | Marginal CPA | Status |
|---|---|---|---|---|
| $100/day | 5 | $20 | $20 | Efficient |
| $150/day | 7 | $21 | $25 | Acceptable |
| $200/day | 8 | $25 | $50 | Diminishing |
| $250/day | 9 | $28 | $50 | At ceiling |

**When marginal CPA exceeds 2x average CPA:** You have likely hit the efficiency ceiling for this audience/campaign. Stop scaling vertically; scale horizontally instead.

---

## Scaling Rollback Protocol

If scaling causes performance degradation:

1. **Reduce budget** to the last stable level (not all the way to original)
2. **Wait 48-72 hours** for the algorithm to re-stabilize
3. **Diagnose** the root cause (saturation, creative fatigue, auction dynamics)
4. **Address the root cause** before attempting to scale again
5. **Re-attempt scaling** only after 5+ days of stable performance at the reduced level

### Rollback Rules
- Never reduce budget by more than 30% in a single move
- Prefer reducing to a mid-point (not the original starting budget)
- Do not make additional changes while rolling back (isolate the variable)

---

## Scaling Playbook by Channel

### Meta Ads
- Gradual increase (20%) is safest
- CBO campaigns scale well when multiple ad sets are performing
- Advantage+ Shopping can absorb large budget increases more gracefully
- At scale, broad targeting often outperforms interest-based targeting

### Google Search
- Scale by adding keywords, increasing bids, or expanding match types
- Budget increases on search are safer than social (intent-based)
- Monitor impression share -- if < 80%, increasing budget captures missed impressions

### Google Shopping / PMax
- PMax absorbs budget increases well due to multi-channel optimization
- Monitor ROAS at each budget tier
- New customer acquisition rate may decline as you scale

### TikTok
- Similar to Meta -- gradual increase is recommended
- Creative volume is critical at scale (need 5-10 active creatives)
- Broad targeting with creative diversity scales best

---

## Scaling Documentation

```
SCALING LOG

Date: {{DATE}}
Campaign: {{CAMPAIGN_NAME}}
Previous Budget: ${{PREVIOUS}}/day
New Budget: ${{NEW}}/day
Change: +{{PERCENT}}%
Reason: {{RATIONALE}}
Pre-Scale CPA: ${{CPA}}
Pre-Scale ROAS: {{ROAS}}x
Expected CPA Impact: +{{}}%
Review Date: {{DATE + 3-4 DAYS}}
Result: {{OUTCOME}}
```
