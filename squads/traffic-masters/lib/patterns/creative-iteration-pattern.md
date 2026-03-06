# Creative Iteration Pattern

## Purpose
Systematic pattern for iterating on creative assets in paid traffic campaigns. Ensures continuous creative improvement through structured testing, analysis, and refinement cycles.

---

## Iteration Cycle

```
ANALYZE (Current Performance)
    |
    v
HYPOTHESIZE (What Could Improve)
    |
    v
CREATE (New Variations)
    |
    v
TEST (Deploy and Measure)
    |
    v
EVALUATE (Winners and Learnings)
    |
    v
SCALE (Roll Out Winners)
    |
    v  (Repeat)
ANALYZE ...
```

**Cycle Duration:** 1-2 weeks per iteration (depending on traffic volume)

---

## Phase 1: Analyze Current Performance

### Creative Performance Audit

For each active creative, collect:

| Creative | Format | Age (Days) | Spend | CTR | CPA | ROAS | Frequency | Trend | Status |
|---|---|---|---|---|---|---|---|---|---|
| `{{}}` | `{{}}` | `{{}}` | $`{{}}` | `{{}}`% | $`{{}}` | `{{}}`x | `{{}}` | `{{}}` | `{{}}` |

### Identify Patterns

**What is working:**
- Which format performs best? (video vs. static vs. carousel vs. UGC)
- Which angle drives the lowest CPA? (pain vs. benefit vs. social proof)
- Which hook type generates the highest CTR?
- Which CTA drives the best conversion rate?
- What visual style resonates? (polished vs. native vs. editorial)

**What is not working:**
- Which creatives have CPA > 150% of target?
- Which creatives have CTR below benchmark?
- Which creatives show fatigue signals (declining CTR, rising CPA)?

### Fatigue Detection

| Signal | Threshold | Action |
|---|---|---|
| CTR dropped > 20% from peak | Warning | Prepare replacement |
| CTR dropped > 40% from peak | Fatigued | Replace immediately |
| CPA increased > 30% from first-week baseline | Warning | Monitor for 48 hours |
| Frequency > 3.0 (prospecting) | Warning | Expand audience or refresh |
| Frequency > 6.0 (retargeting) | Critical | Refresh creative now |

---

## Phase 2: Hypothesize Improvements

### Iteration Types (Smallest to Largest Change)

| Level | What Changes | Risk | Speed | Example |
|---|---|---|---|---|
| **Micro-Iteration** | One element only | Very Low | Fast | Change headline text only |
| **Minor Iteration** | 2-3 elements | Low | Fast | New hook + new CTA on same video |
| **Moderate Iteration** | Core creative element | Medium | Medium | New angle on same format |
| **Major Iteration** | Format or concept | High | Slow | Switch from static to UGC video |
| **Net-New** | Entirely new concept | High | Slow | New creative concept from scratch |

### Hypothesis Template
```
IF we change {{ELEMENT}} from {{CURRENT}} to {{NEW}},
THEN we expect {{METRIC}} to improve by {{AMOUNT}},
BECAUSE {{RATIONALE based on data or insight}}.
```

### Common Iteration Hypotheses

| Element to Iterate | Hypothesis Pattern |
|---|---|
| **Hook** | Different opening line/visual will improve thumb-stop and CTR |
| **Body Copy** | Shorter/longer copy or different benefit order will improve CVR |
| **CTA** | Stronger/different CTA will improve click-to-conversion rate |
| **Visual** | Different imagery, color, or style will improve CTR |
| **Format** | Video will outperform static (or vice versa) for this audience |
| **Angle** | Pain-point approach will outperform benefit-led for cold audience |
| **Length** | 15-second video will outperform 30-second for prospecting |
| **Talent** | Different speaker/model will improve trust and engagement |
| **Offer Presentation** | Different way to frame the offer will improve perceived value |
| **Social Proof** | Adding testimonial or rating will improve credibility and CVR |

---

## Phase 3: Create New Variations

### Minimum Viable Test Set

For each iteration cycle, produce:
- **2-3 iterations** of the top-performing creative (micro/minor changes)
- **1-2 new angles** or formats (moderate/major changes)
- **1 net-new concept** (if in the experimental budget)

### Iteration Worksheet

```
Base Creative: {{WINNING_CREATIVE_ID}}
Performance: CTR {{CTR}}%, CPA ${{CPA}}, ROAS {{ROAS}}x

Variation 1: {{DESCRIPTION}}
  Change: {{WHAT_CHANGED}}
  Hypothesis: {{HYPOTHESIS}}

Variation 2: {{DESCRIPTION}}
  Change: {{WHAT_CHANGED}}
  Hypothesis: {{HYPOTHESIS}}

Variation 3: {{DESCRIPTION}}
  Change: {{WHAT_CHANGED}}
  Hypothesis: {{HYPOTHESIS}}
```

### Creative Production Rules
- Always keep the winning element from the original (e.g., if the hook works, keep it)
- Change only ONE major variable per variation for clear learnings
- Maintain consistent branding elements (logo placement, brand colors)
- Match platform specifications exactly (aspect ratio, length, file size)

---

## Phase 4: Test Deployment

### Test Structure
- Add new variations to the SAME ad set as the control (or use A/B test tool)
- Ensure even distribution (platform DCO or manual split)
- Set minimum budget per variation: enough for 1,000+ impressions per creative
- Run for minimum 5-7 days or until statistical significance

### Test Parameters

| Parameter | Recommended Setting |
|---|---|
| Test duration | 7-14 days |
| Minimum impressions per variant | 1,000+ |
| Minimum conversions per variant | 20+ for CPA evaluation |
| Confidence threshold | 90%+ for winner declaration |
| Budget per variant | Equal distribution |

---

## Phase 5: Evaluate Results

### Winner Declaration Criteria
- Variant has lower CPA (or higher ROAS) than control
- Difference is statistically significant at 90%+ confidence
- Variant has sufficient sample size (20+ conversions minimum)
- Performance is consistent (not driven by a single day spike)

### Evaluation Template

| Variant | Spend | Impressions | CTR | CPA | ROAS | vs. Control | Significant? | Verdict |
|---|---|---|---|---|---|---|---|---|
| Control | $`{{}}` | `{{}}` | `{{}}`% | $`{{}}` | `{{}}`x | -- | -- | Baseline |
| Var 1 | $`{{}}` | `{{}}` | `{{}}`% | $`{{}}` | `{{}}`x | `{{}}`% | `{{YES/NO}}` | `{{WINNER/LOSER/INCONCLUSIVE}}` |
| Var 2 | $`{{}}` | `{{}}` | `{{}}`% | $`{{}}` | `{{}}`x | `{{}}`% | `{{YES/NO}}` | `{{}}` |
| Var 3 | $`{{}}` | `{{}}` | `{{}}`% | $`{{}}` | `{{}}`x | `{{}}`% | `{{YES/NO}}` | `{{}}` |

### Document Learnings
```
Test: {{TEST_NAME}}
Winner: {{VARIANT_NAME}}
Key Learning: {{WHAT_WE_LEARNED}}
Applicable To: {{OTHER_CAMPAIGNS_OR_AUDIENCES}}
Next Iteration: {{WHAT_TO_TEST_NEXT_BASED_ON_THIS_LEARNING}}
```

---

## Phase 6: Scale Winners

### Rollout Process
1. Pause or reduce spend on losing variants
2. Increase budget allocation to winning variant gradually (15-20% per increase)
3. Deploy winning elements across other campaigns/audiences where applicable
4. Use winning creative as the new control for the next iteration cycle
5. Begin next iteration cycle within 1-2 weeks

### Creative Lifespan Planning

| Creative Volume (Monthly) | Expected Lifespan | Refresh Cadence |
|---|---|---|
| < $5K spend | 4-8 weeks | Bi-monthly |
| $5K - $20K spend | 2-4 weeks | Bi-weekly |
| $20K - $50K spend | 1-3 weeks | Weekly |
| > $50K spend | 1-2 weeks | Weekly or more |

---

## Iteration Cadence Template

| Week | Monday | Wednesday | Friday |
|---|---|---|---|
| Week 1 | Analyze current performance | Brief new variations | Creatives in production |
| Week 2 | Launch new variations | Monitor delivery | Preliminary data check |
| Week 3 | Evaluate results | Declare winners/losers | Document learnings |
| Week 4 | Scale winners | Begin next analysis | Brief next iteration |

---

## Anti-Patterns (What NOT to Do)

- **Do not** change the winning creative -- iterate around it
- **Do not** test more than one major variable per variant
- **Do not** declare winners with fewer than 20 conversions per variant
- **Do not** kill creatives based on CTR alone (low CTR can still have strong CPA)
- **Do not** stop iterating when you find a winner (fatigue is inevitable)
- **Do not** iterate without documenting learnings (you will repeat mistakes)
