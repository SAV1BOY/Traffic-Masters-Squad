# Audience Expansion Pattern

## Purpose
Systematic pattern for expanding audience reach while maintaining performance targets. Provides a structured approach to moving from narrow, proven audiences to broader reach without sacrificing efficiency.

---

## Expansion Stages

```
STAGE 1: FOUNDATION (Proven Core)
    |
    v
STAGE 2: ADJACENT (Similar Audiences)
    |
    v
STAGE 3: EXTENDED (Broader Reach)
    |
    v
STAGE 4: OPEN (Maximum Scale)
```

---

## Stage 1: Foundation -- Establish the Core

### Goal
Identify and validate 2-3 core audiences that consistently hit KPI targets.

### Actions
1. Launch with your strongest audience signals:
   - Lookalike 1% based on purchasers or highest-value customers
   - Retargeting (website visitors 0-30 days)
   - Customer list custom audiences
2. Run for 2-3 weeks minimum with sufficient budget
3. Establish baseline CPA, ROAS, and CVR for each audience

### Graduation Criteria
- CPA within target for 7+ consecutive days
- Minimum 50 conversions recorded
- ROAS above break-even threshold
- Performance stable (not carried by a single spike day)

### Output
```
Core Audience 1: {{NAME}} -- CPA: ${{}} -- ROAS: {{}}x -- Volume: {{CONV}}/week
Core Audience 2: {{NAME}} -- CPA: ${{}} -- ROAS: {{}}x -- Volume: {{CONV}}/week
Core Audience 3: {{NAME}} -- CPA: ${{}} -- ROAS: {{}}x -- Volume: {{CONV}}/week
```

---

## Stage 2: Adjacent -- Expand to Similar

### Goal
Test audiences that are logically close to proven winners. Expect 10-30% higher CPA than core.

### Expansion Tactics

| Tactic | Description | Expected CPA Impact |
|---|---|---|
| **Lookalike expansion** | Move from 1% to 2-3% lookalikes | +10-20% CPA |
| **New lookalike seeds** | Create lookalikes from different sources (leads, ATC, email openers) | +10-25% CPA |
| **Interest stacking** | Combine 3-5 related interests that overlap with your buyer profile | +15-25% CPA |
| **Behavioral targeting** | Target purchase behaviors, device types, or engagement patterns | +10-20% CPA |
| **Retargeting expansion** | Extend retargeting window (30d to 60-90d) | +15-25% CPA |
| **Engaged audience expansion** | Social engagers 60-180 days, video viewers broader windows | +20-30% CPA |

### Testing Protocol
- Allocate 15-20% of total budget to Stage 2 testing
- Run each new audience for minimum 7 days
- Compare CPA and ROAS to core audience benchmarks
- Graduate audiences that achieve CPA < 130% of core audience CPA

### Decision Matrix

| Result | Action |
|---|---|
| CPA < 110% of core | Promote to "Core" -- increase budget |
| CPA 110-130% of core | Keep active -- monitor for 2 more weeks |
| CPA 130-150% of core | Reduce budget -- iterate on creative or targeting |
| CPA > 150% of core | Pause -- try different creative or different adjacent audience |

---

## Stage 3: Extended -- Broaden the Reach

### Goal
Reach audiences beyond your obvious targeting, accepting 20-50% higher CPA for incremental volume.

### Expansion Tactics

| Tactic | Description | Expected CPA Impact |
|---|---|---|
| **Lookalike 5-10%** | Much broader similarity pools | +25-40% CPA |
| **Broad interest categories** | Single broad interests (e.g., "Fitness" instead of "CrossFit") | +20-35% CPA |
| **Competitor targeting** | Audiences interested in competitor brands | +20-40% CPA |
| **New demographics** | Expand age, gender, or location parameters | +15-30% CPA |
| **New geographies** | Expand to new regions or countries | +20-50% CPA |
| **In-market audiences** | Google/YouTube audiences actively researching your category | +15-30% CPA |
| **Life events** | Target people experiencing relevant life changes | +25-40% CPA |

### Budget Allocation
- Stage 3 should not exceed 20% of total budget until validated
- Use the 70-20-10 rule: 70% proven, 20% iterative, 10% experimental

### Creative Considerations
- Broader audiences often need different creative than core audiences
- Cold audiences need more education, social proof, and trust signals
- Test hooks that resonate with a wider audience (less niche-specific)
- UGC and testimonial content often performs well with extended audiences

---

## Stage 4: Open -- Maximum Scale

### Goal
Leverage platform algorithms with minimal targeting restrictions, letting the algorithm find converters within the broadest possible pool.

### Approach
- **Meta:** Advantage+ Shopping Campaigns (ASC) or broad targeting with no interest/behavioral restrictions
- **Google:** Performance Max (PMax) or broad match search campaigns
- **TikTok:** Broad targeting with strong creative (no interest restrictions)

### When to Deploy Stage 4
- Core audiences are saturated (frequency > 4.0, rising CPA)
- You have 50+ conversions per week per campaign (strong signal for algorithm)
- Creative is strong and varied (minimum 5-10 active creatives)
- Budget is sufficient ($100+/day minimum for broad campaigns)

### Success Criteria for Broad/Open Targeting
- CPA within 150% of core audience CPA
- Volume significantly higher than any single targeted audience
- ROAS above break-even (even if below core audience ROAS)
- Incremental conversions (not cannibalizing targeted campaigns)

---

## Audience Overlap Management

### Check Before Expanding
Before launching a new audience, verify it does not significantly overlap with existing audiences.

| Audience A | Audience B | Overlap % | Action |
|---|---|---|---|
| `{{}}` | `{{}}` | `{{}}`% | `{{OK if <25% / CONSOLIDATE if >25%}}` |

### Overlap Rules
- **< 15% overlap:** Safe to run both
- **15-25% overlap:** Monitor for auction competition, consider consolidating
- **> 25% overlap:** Consolidate into one audience or use exclusions

### Overlap Resolution
1. Merge into a single ad set (let the algorithm optimize)
2. Use exclusions to create non-overlapping segments
3. Consolidate into an Advantage+ or PMax campaign

---

## Expansion Velocity

| Monthly Ad Spend | Recommended Expansion Pace | New Audiences per Month |
|---|---|---|
| < $5,000 | Slow (1 new audience every 2 weeks) | 2 |
| $5,000 - $20,000 | Moderate (1 new audience per week) | 4 |
| $20,000 - $100,000 | Fast (2-3 new audiences per week) | 8-12 |
| > $100,000 | Aggressive (continuous testing pipeline) | 12+ |

---

## Tracking Expansion Performance

| Stage | Audience | Launch Date | Spend | Conv. | CPA | vs. Core CPA | ROAS | Status |
|---|---|---|---|---|---|---|---|---|
| Core | `{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | Baseline | `{{}}`x | Active |
| Adjacent | `{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | +`{{}}`% | `{{}}`x | `{{}}` |
| Extended | `{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | +`{{}}`% | `{{}}`x | `{{}}` |
| Open | `{{}}` | `{{}}` | $`{{}}` | `{{}}` | $`{{}}` | +`{{}}`% | `{{}}`x | `{{}}` |

---

## Anti-Patterns

- **Do not** expand before core audiences are proven and stable
- **Do not** expand all stages simultaneously -- go sequentially
- **Do not** compare extended audience CPA to core audience CPA and declare failure (different expectations per stage)
- **Do not** ignore creative when expanding (broader audiences need tailored messaging)
- **Do not** expand audiences without checking for overlap
- **Do not** keep expanding if overall blended CPA exceeds target
