# Optimization Loop Pattern

## Purpose
Continuous optimization cycle for paid traffic campaigns. Provides a repeatable loop that systematically improves performance over time through structured review, testing, and implementation.

---

## The Optimization Loop

```
    +---> MONITOR (Observe performance data)
    |         |
    |         v
    |     IDENTIFY (Find optimization opportunities)
    |         |
    |         v
    |     PRIORITIZE (Rank by impact and effort)
    |         |
    |         v
    |     EXECUTE (Implement the top priority change)
    |         |
    |         v
    |     MEASURE (Evaluate the impact of the change)
    |         |
    |         v
    +---- LEARN (Document findings, update playbook)
```

**Cycle Frequency:**
- Micro-loop: Daily (monitoring + quick fixes)
- Standard loop: Weekly (full cycle)
- Strategic loop: Monthly (comprehensive review + strategic changes)

---

## Phase 1: Monitor

### Daily Monitoring Dashboard

| Metric | Today | Yesterday | 7-Day Avg | Target | Status |
|---|---|---|---|---|---|
| Spend | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}` |
| Conversions | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` |
| CPA | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}` |
| ROAS | `{{}}`x | `{{}}`x | `{{}}`x | `{{}}`x | `{{}}` |
| CTR | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}` |
| CVR | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}` |

### Alert Triggers (Automatic Flags)

| Condition | Severity | Response Time |
|---|---|---|
| CPA > 150% of target | High | Within 4 hours |
| Zero conversions for 24+ hours | High | Within 4 hours |
| Budget underspend > 30% | Medium | Within 24 hours |
| CTR dropped > 25% vs. 7-day avg | Medium | Within 24 hours |
| Frequency > 3.5 (prospecting) | Low | Within 48 hours |
| ROAS below break-even | High | Within 4 hours |

---

## Phase 2: Identify Opportunities

### Optimization Categories

| Category | What to Look For | Typical Impact |
|---|---|---|
| **Budget** | Under/over-spending, misallocation between performers/non-performers | High |
| **Audience** | Saturation, overlap, underperforming segments, expansion opportunities | High |
| **Creative** | Fatigue, winning elements to iterate on, underperformers to pause | High |
| **Bidding** | Bid strategy mismatch, target CPA/ROAS adjustments needed | Medium |
| **Funnel** | Drop-off points, landing page issues, checkout friction | High |
| **Targeting** | Placement performance, device splits, geo performance | Medium |
| **Schedule** | Day-of-week and time-of-day patterns | Low-Medium |

### Opportunity Identification Questions

1. **Budget:** Which campaigns deserve more budget? Which are wasting it?
2. **Creative:** Which creatives are fatiguing? Which elements drive the best results?
3. **Audience:** Are any audiences saturated? Are there untested segments?
4. **Funnel:** Where is the biggest drop-off? Has conversion rate changed?
5. **Structure:** Are campaigns structured efficiently? Any audience overlap?
6. **Testing:** What is the next highest-impact variable to test?

---

## Phase 3: Prioritize

### Impact-Effort Matrix

| Priority | Criteria | Examples |
|---|---|---|
| **P0 (Emergency)** | Performance crisis, tracking broken | Fix broken pixel, pause hemorrhaging campaign |
| **P1 (Quick Win)** | High impact, low effort | Pause underperforming ad sets, shift budget to winners |
| **P2 (Strategic)** | High impact, medium effort | Launch new creative, test new audience |
| **P3 (Incremental)** | Medium impact, low effort | Adjust bids, refine targeting |
| **P4 (Investment)** | High impact, high effort | Rebuild campaign structure, launch new channel |

### Scoring Model

```
Priority Score = Impact Score (1-5) x Confidence (1-5) / Effort Score (1-5)
```

| Opportunity | Impact (1-5) | Confidence (1-5) | Effort (1-5) | Score | Priority |
|---|---|---|---|---|---|
| `{{OPP_1}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` |
| `{{OPP_2}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` |
| `{{OPP_3}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` |

**Rule:** Execute no more than 2-3 changes per optimization cycle. More than that makes it impossible to attribute improvements.

---

## Phase 4: Execute

### Execution Rules

1. **One change at a time** per campaign (so you can measure impact)
2. **Document every change** (what, when, why, expected impact)
3. **Set a review date** (48-72 hours for quick changes, 7 days for structural changes)
4. **Do not stack changes** (wait for one to stabilize before making another)

### Change Log Template

```
Date: {{DATE}}
Time: {{TIME}}
Campaign: {{CAMPAIGN}}
Change Made: {{DESCRIPTION}}
Rationale: {{WHY}}
Expected Impact: {{PREDICTION}}
Review Date: {{DATE}}
Pre-Change Metrics:
  CPA: ${{}} | ROAS: {{}}x | CTR: {{}}% | Daily Spend: ${{}}
```

### Common Optimization Actions

| Action | When to Apply | How |
|---|---|---|
| Pause underperformer | CPA > 2x target with 20+ conversions | Pause ad set, not entire campaign |
| Increase winner budget | CPA < target for 5+ days | Increase 15-20%, wait 3 days |
| Launch new creative | Creative fatigue detected | Add to existing ad set or create new |
| Shift budget | One channel outperforms another | Reduce loser by 15%, increase winner by same |
| Tighten targeting | CPM too high, audience too broad | Add exclusions or narrow demographics |
| Expand targeting | Frequency too high, audience saturated | Expand lookalike %, add interests, go broad |
| Adjust bid target | CPA consistently above/below target | Raise target CPA by 10% if under-spending |
| Refresh landing page | CVR declining despite stable traffic quality | Test new headline, layout, or offer |

---

## Phase 5: Measure

### Post-Change Evaluation

| Metric | Before Change | After Change (48h) | After Change (7d) | Impact |
|---|---|---|---|---|
| CPA | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| ROAS | `{{}}`x | `{{}}`x | `{{}}`x | `{{}}`% |
| CTR | `{{}}`% | `{{}}`% | `{{}}`% | `{{}}`% |
| Volume | `{{}}` conv/day | `{{}}` conv/day | `{{}}` conv/day | `{{}}`% |
| Spend | $`{{}}`/day | $`{{}}`/day | $`{{}}`/day | `{{}}`% |

### Evaluation Criteria

| Result | Criteria | Action |
|---|---|---|
| **Positive** | Primary metric improved > 10% and held for 48+ hours | Keep change, document as proven tactic |
| **Neutral** | No meaningful change (< 5% either direction) | Keep for now, deprioritize this lever |
| **Negative** | Primary metric worsened > 10% for 48+ hours | Revert the change, analyze why |
| **Mixed** | Primary metric improved but secondary metric worsened | Evaluate net impact, decide case-by-case |

---

## Phase 6: Learn

### Learning Documentation

```
Optimization: {{WHAT_WAS_CHANGED}}
Date: {{DATE}}
Result: {{POSITIVE / NEUTRAL / NEGATIVE}}
Key Learning: {{WHAT_WE_LEARNED}}
Applicable To: {{OTHER_CAMPAIGNS / CLIENTS / SITUATIONS}}
Added to Playbook: {{YES / NO}}
```

### Knowledge Accumulation

Over time, build a library of proven optimizations:

| Optimization | Times Tested | Win Rate | Avg. Impact | Confidence |
|---|---|---|---|---|
| Pausing ad sets with CPA > 2x target | 12 | 83% | -18% CPA | High |
| Launching UGC vs. polished creative | 8 | 62% | -12% CPA | Medium |
| Expanding LAL from 1% to 3% | 6 | 50% | +15% volume, +10% CPA | Medium |
| Switching to CBO | 5 | 60% | -8% CPA | Medium |

---

## Optimization Cadence Summary

### Daily (15-30 minutes)
- Review key metrics vs. targets
- Flag anomalies
- Quick fixes only (pause/unpause, minor budget shifts)

### Weekly (1-2 hours)
- Full performance review across all campaigns
- Identify 2-3 optimization opportunities
- Execute highest-priority change
- Review previous week's changes
- Document learnings

### Monthly (3-4 hours)
- Comprehensive performance analysis
- Strategic budget reallocation
- Creative refresh planning
- Audience expansion assessment
- Test roadmap for next month
- Update playbook with learnings

---

## Anti-Patterns

- **Constant tinkering:** Making daily changes without waiting for results
- **Optimization without documentation:** Changes without records lead to repeated mistakes
- **Chasing daily fluctuations:** Reacting to normal variation as if it were a trend
- **Ignoring secondary metrics:** Improving CPA while CTR collapses means creative is dying
- **Over-optimizing for efficiency at the expense of volume:** Perfect CPA with 2 conversions/day is not success
- **Copying competitor tactics without testing:** What works for them may not work for your account
