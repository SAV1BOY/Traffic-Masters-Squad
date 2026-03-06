# Data Model Documentation

> Documentation of the data structures used across registries, metrics, and configuration files in the Traffic Masters Squad.

---

## Overview

The data model consists of three primary layers:

1. **Registries** — Structured records of all managed entities (campaigns, creatives, audiences, etc.)
2. **Metrics** — Performance data snapshots at various cadences
3. **Configuration** — System settings, thresholds, and preferences

---

## Registry Data Models

### Campaign Registry (`data/registries/campaigns-registry.yaml`)

```yaml
campaigns:
  - id: "CMP-001"
    name: "META_CONV_US_TOFU_FreeTrial_2026Q1"
    platform: "meta"
    account_id: "act_123456789"
    objective: "conversions"
    funnel_stage: "tofu"
    status: "active"                    # active | paused | completed | archived
    geo: "US"
    offer: "FreeTrial"
    budget:
      type: "daily"                     # daily | lifetime
      amount: 500.00
      currency: "USD"
    bid_strategy: "cost_cap"
    bid_target: 30.00
    start_date: "2026-01-15"
    end_date: "2026-03-31"
    kpi_targets:
      cpa: 45.00
      roas: null
      cpl: null
    audiences:
      - "AUD-001"
      - "AUD-003"
    creatives:
      - "CRE-001"
      - "CRE-002"
      - "CRE-005"
    landing_page: "LP-001"
    utm_campaign: "meta-conv-us-tofu-freetrial-2026q1"
    tags:
      - "q1-2026"
      - "free-trial"
      - "prospecting"
    notes: "Initial prospecting campaign for Q1 free trial offer"
    created_date: "2026-01-10"
    created_by: "Strategy Agent"
    last_modified: "2026-02-15"
```

**Required Fields:** `id`, `name`, `platform`, `objective`, `status`, `budget`
**Optional Fields:** All others (though completeness is encouraged)

---

### Creative Registry (`data/registries/creatives-registry.yaml`)

```yaml
creatives:
  - id: "CRE-001"
    name: "VID_QuestionHook_PainAngle_v1"
    format: "video"                     # video | static | carousel | collection | gif
    hook_type: "question"
    angle: "pain"
    version: 1
    status: "active"                    # active | paused | retired | testing
    campaigns:
      - "CMP-001"
    dimensions: "1080x1080"
    duration_seconds: 30                # for video only
    file_path: "assets/vid-questionhook-painangle-v1.mp4"
    copy:
      headline: "Are you still wasting ad spend on cold audiences?"
      primary_text: "Most brands lose 40% of their budget..."
      cta: "Learn More"
    performance:
      lifetime_spend: 2450.00
      lifetime_impressions: 125000
      lifetime_clicks: 1875
      lifetime_conversions: 42
      ctr: 1.50
      cpa: 58.33
      peak_ctr: 2.10
      days_running: 35
    fatigue_status: "healthy"           # healthy | watch | fatigued | retired
    created_date: "2026-01-15"
    retired_date: null
    tags:
      - "ugc-style"
      - "pain-point"
```

---

### Audience Registry (`data/registries/audiences-registry.yaml`)

```yaml
audiences:
  - id: "AUD-001"
    name: "LAL1_Purchasers180d_tCPA30"
    platform: "meta"
    type: "lookalike"                   # lookalike | interest | custom | crm | broad | retargeting
    source: "Purchasers last 180 days"
    lookalike_percentage: 1
    geo: "US"
    age_range: "25-65"
    gender: "all"
    estimated_size: 2100000
    status: "active"                    # active | paused | archived | expired
    campaigns:
      - "CMP-001"
    exclusions:
      - "AUD-010"                       # Existing customers
      - "AUD-011"                       # Recent converters (30d)
    refresh_schedule: "monthly"
    last_refreshed: "2026-02-01"
    performance:
      lifetime_spend: 5000.00
      lifetime_conversions: 120
      cpa: 41.67
      avg_frequency: 2.3
    created_date: "2026-01-10"
    tags:
      - "prospecting"
      - "high-value-seed"
```

---

### Experiments Registry (`data/registries/experiments-registry.yaml`)

```yaml
experiments:
  - id: "EXP-001"
    name: "Hook Type Test: Question vs. Statistic"
    hypothesis: "Question hooks will generate higher CTR than statistic hooks for TOFU audiences"
    type: "a_b_test"                    # a_b_test | multivariate | holdout | incrementality
    status: "completed"                 # planned | running | completed | inconclusive
    variable: "hook_type"
    control:
      name: "Statistic Hook"
      creative_id: "CRE-003"
    challenger:
      name: "Question Hook"
      creative_id: "CRE-001"
    primary_metric: "ctr"
    secondary_metrics:
      - "cpa"
      - "conversion_rate"
    target_sample_size: 5000            # per variant
    actual_sample_size_control: 5200
    actual_sample_size_challenger: 5100
    start_date: "2026-02-01"
    end_date: "2026-02-14"
    results:
      control_value: 1.20
      challenger_value: 1.85
      lift_pct: 54.2
      statistical_significance: 97.3
      winner: "challenger"
    conclusion: "Question hooks significantly outperform statistic hooks for CTR in TOFU campaigns"
    next_steps: "Adopt question hooks as primary hook type; test question variations"
    learnings_applied: true
    campaign_ids:
      - "CMP-001"
    created_date: "2026-01-28"
    created_by: "Experimentation Agent"
```

---

### Decisions Log (`data/registries/decisions-log.yaml`)

```yaml
decisions:
  - id: "DEC-001"
    date: "2026-02-15"
    type: "budget_change"               # budget_change | strategy_change | creative_change | audience_change | platform_change | process_change
    description: "Increased CMP-001 daily budget from $300 to $500"
    rationale: "CPA has been stable at $38 for 14 days, below $45 target. Marginal efficiency analysis supports scale."
    impact_expected: "Additional 4-5 conversions per day at similar CPA"
    impact_actual: "4.2 additional conversions per day, CPA rose to $41"
    decision_maker: "Budget Agent"
    approved_by: "Account Manager"
    related_entities:
      - "CMP-001"
    status: "implemented"               # proposed | approved | implemented | reversed
    review_date: "2026-02-22"
```

---

### Lessons Learned Registry (`data/registries/lessons-learned-registry.yaml`)

```yaml
lessons:
  - id: "LES-001"
    date: "2026-02-14"
    source: "EXP-001"
    category: "creative"                # creative | audience | budget | tracking | platform | strategy
    lesson: "Question-based hooks consistently outperform statistic hooks for TOFU audiences on Meta"
    evidence: "54% higher CTR with 97.3% statistical significance"
    applicability: "All TOFU prospecting campaigns on Meta"
    action_taken: "Updated creative brief template to prioritize question hooks for TOFU"
    tags:
      - "hooks"
      - "creative-testing"
      - "meta"
      - "tofu"
```

---

## Metrics Data Models

### Weekly Scorecard (`data/metrics/weekly-scorecards.md`)

```yaml
weekly_scorecards:
  - week: "2026-W10"
    date_range: "2026-03-02 to 2026-03-08"
    account_level:
      total_spend: 12500.00
      total_impressions: 580000
      total_clicks: 8700
      total_conversions: 195
      blended_ctr: 1.50
      blended_cpc: 1.44
      blended_cpa: 64.10
      blended_roas: 3.8
      total_revenue: 47500.00
    by_platform:
      meta:
        spend: 8500.00
        conversions: 140
        cpa: 60.71
        roas: 4.1
      google_ads:
        spend: 4000.00
        conversions: 55
        cpa: 72.73
        roas: 3.2
    vs_targets:
      cpa: { target: 65.00, actual: 64.10, status: "on_target" }
      roas: { target: 3.5, actual: 3.8, status: "above_target" }
    alerts: []
    notes: "Strong week driven by new creative batch launched 2026-02-28"
```

---

## Entity Relationships

```
Campaign (CMP) ----< has many >---- Creatives (CRE)
Campaign (CMP) ----< has many >---- Audiences (AUD)
Campaign (CMP) ----< has one  >---- Landing Page (LP)
Campaign (CMP) ----< has many >---- Experiments (EXP)
Experiment (EXP) ---< has many >---- Creatives (CRE)
Decision (DEC) ----< references >--- Any entity
Lesson (LES) ------< sourced from >- Experiment (EXP) or Decision (DEC)
```

---

## Data Governance

### Data Integrity Rules
1. **IDs are unique and immutable** — Once assigned, an ID never changes or gets reused
2. **Status transitions are forward-only** — Active -> Paused -> Completed -> Archived (no reverse)
3. **All changes are logged** — Every modification to a registry entry creates a decisions log entry
4. **Cross-references must resolve** — If a campaign references AUD-001, AUD-001 must exist
5. **Dates use ISO 8601** — All dates follow YYYY-MM-DD format

### Data Freshness
| Data Type | Update Frequency | Responsibility |
|-----------|-----------------|----------------|
| Campaign registry | On change | Launch / Optimization Agent |
| Creative registry | On change + weekly performance update | Creative Strategist Agent |
| Audience registry | Monthly refresh | Audience Agent |
| Experiments registry | On change | Experimentation Agent |
| Decisions log | On decision | Deciding agent |
| Weekly scorecard | Weekly | Reporting Agent |
| Lessons learned | On discovery | Any agent |

### Data Retention
- **Active data:** Maintained in registries indefinitely
- **Archived data:** Moved to archive after 90 days of inactivity
- **Performance snapshots:** Retained for 24 months minimum
- **Experiment data:** Retained permanently for knowledge base
