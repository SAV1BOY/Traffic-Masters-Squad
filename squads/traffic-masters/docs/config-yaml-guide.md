# Guide to Understanding and Modifying config.yaml

> Detailed reference for every configuration option in the Traffic Masters Squad config.yaml file.

---

## File Location

```
squads/traffic-masters/config.yaml
```

---

## Configuration Sections

### 1. Squad Identity

```yaml
squad:
  name: "Traffic Masters Squad"
  version: "1.0.0"
  description: "AI-powered paid media management system"
  owner: "Media Team"
  created: "2026-01-01"
  last_updated: "2026-03-06"
```

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Display name of the squad |
| `version` | semver | Current version following semantic versioning |
| `description` | string | Brief description of the squad's purpose |
| `owner` | string | Team or individual responsible |
| `created` | date | Date the squad was created |
| `last_updated` | date | Date of last configuration change |

---

### 2. Platform Configuration

```yaml
platforms:
  meta:
    enabled: true
    account_ids:
      - "act_123456789"
    currency: "USD"
    timezone: "America/New_York"
    attribution_window: "7d_click_1d_view"
    default_objective: "CONVERSIONS"

  google_ads:
    enabled: true
    account_ids:
      - "123-456-7890"
    currency: "USD"
    timezone: "America/New_York"
    attribution_window: "30d_click"
    default_objective: "CONVERSIONS"

  tiktok:
    enabled: false
    account_ids: []
    currency: "USD"
    timezone: "America/New_York"
    attribution_window: "7d_click_1d_view"
    default_objective: "CONVERSIONS"
```

| Field | Type | Description |
|-------|------|-------------|
| `enabled` | boolean | Whether this platform is actively managed |
| `account_ids` | list | Platform-specific account identifiers |
| `currency` | string | ISO 4217 currency code |
| `timezone` | string | IANA timezone string |
| `attribution_window` | string | Default attribution window for the platform |
| `default_objective` | string | Default campaign objective |

**Supported Platforms:** `meta`, `google_ads`, `tiktok`, `linkedin`, `snapchat`, `pinterest`, `twitter`, `programmatic`

---

### 3. KPI Targets

```yaml
kpi_targets:
  primary:
    cpa: 45.00
    roas: 3.5
    cpl: 25.00

  secondary:
    ctr: 1.5
    cpc: 2.50
    conversion_rate: 3.0
    frequency_cap: 4.0

  efficiency:
    budget_utilization_min: 85
    budget_utilization_max: 105
    learning_phase_min_conversions: 50
```

| Field | Type | Description |
|-------|------|-------------|
| `cpa` | float | Target cost per acquisition in account currency |
| `roas` | float | Target return on ad spend (multiplier) |
| `cpl` | float | Target cost per lead |
| `ctr` | float | Target click-through rate (percentage) |
| `cpc` | float | Target cost per click |
| `conversion_rate` | float | Target landing page conversion rate (percentage) |
| `frequency_cap` | float | Maximum average frequency before fatigue alert |
| `budget_utilization_min` | integer | Minimum acceptable budget utilization (percentage) |
| `budget_utilization_max` | integer | Maximum acceptable budget utilization (percentage) |
| `learning_phase_min_conversions` | integer | Minimum conversions needed to exit learning |

**How to modify:** Adjust targets based on account maturity, industry benchmarks, and business goals. Review quarterly.

---

### 4. Thresholds & Alerts

```yaml
thresholds:
  performance_alerts:
    cpa_increase_pct: 25         # Alert if CPA increases by this %
    roas_decrease_pct: 20        # Alert if ROAS decreases by this %
    ctr_decrease_pct: 30         # Alert if CTR decreases by this %
    spend_overpace_pct: 20       # Alert if spend paces this % over budget
    spend_underpace_pct: 30      # Alert if spend paces this % under budget
    consecutive_days: 3          # Days of sustained change before alert

  creative_fatigue:
    ctr_decline_from_peak_pct: 20
    frequency_threshold: 3.5
    min_days_running: 7
    max_days_without_refresh: 45

  audience_health:
    overlap_threshold_pct: 30
    saturation_frequency: 5.0
    min_audience_size: 10000

  scaling:
    max_budget_increase_pct: 30
    min_stable_days: 14
    max_cpa_degradation_pct: 15
```

| Section | Purpose |
|---------|---------|
| `performance_alerts` | Defines when performance alerts trigger |
| `creative_fatigue` | Defines creative fatigue detection thresholds |
| `audience_health` | Defines audience quality thresholds |
| `scaling` | Defines scaling guardrails |

**How to modify:** Tighten thresholds for sensitive accounts; loosen for accounts with more tolerance for variance. Never set alert thresholds wider than business-impacting levels.

---

### 5. Workflow Configuration

```yaml
workflows:
  daily_check:
    enabled: true
    schedule: "09:00"
    timezone: "America/New_York"
    accounts: "all"

  weekly_optimization:
    enabled: true
    day: "monday"
    schedule: "10:00"
    timezone: "America/New_York"

  monthly_report:
    enabled: true
    day: 3                        # Day of month
    schedule: "09:00"
    timezone: "America/New_York"
    template: "monthly-performance-report"

  creative_rotation:
    enabled: true
    cadence_days: 30
    auto_pause_fatigued: false    # Manual review required

  budget_review:
    enabled: true
    cadence: "weekly"
    auto_reallocate: false        # Manual approval required
```

| Field | Description |
|-------|-------------|
| `enabled` | Whether this workflow runs automatically |
| `schedule` | Time of day to trigger (24h format) |
| `day` | Day of week (for weekly) or day of month (for monthly) |
| `auto_*` | Whether the workflow can take action without approval |

---

### 6. Naming Convention Configuration

```yaml
naming:
  campaign_format: "[PLATFORM]_[OBJECTIVE]_[GEO]_[FUNNEL]_[OFFER]_[PERIOD]"
  adset_format: "[AUDIENCE]_[TARGETING]_[BID]"
  ad_format: "[FORMAT]_[HOOK]_[ANGLE]_[VERSION]"
  utm_lowercase: true
  utm_separator: "-"
  file_separator: "-"
  registry_id_padding: 3
```

---

### 7. Reporting Configuration

```yaml
reporting:
  default_comparison: "previous_period"   # previous_period | same_period_last_year
  include_benchmarks: true
  currency_display: "symbol"              # symbol ($) | code (USD)
  decimal_places: 2
  percentage_decimal_places: 1
  date_format: "YYYY-MM-DD"
  week_start: "monday"
```

---

### 8. Integration Configuration

```yaml
integrations:
  copy_squad:
    enabled: true
    shared_assets_path: "../copy-squad/shared/"
    sync_frequency: "daily"

  brand_squad:
    enabled: true
    brand_guidelines_path: "../brand-squad/guidelines/"
    voice_sync: true

  analytics:
    platform: "ga4"
    property_id: "123456789"
    data_stream: "web"
```

---

### 9. Agent Configuration

```yaml
agents:
  diagnostics:
    audit_depth: "comprehensive"         # quick | standard | comprehensive
    auto_severity_classification: true

  optimization:
    min_data_days: 7                     # Minimum days of data before optimizing
    max_changes_per_cycle: 10            # Limit changes per optimization cycle
    learning_phase_protection: true       # Prevent changes during learning

  creative_strategist:
    fatigue_check_frequency: "daily"
    auto_pause_threshold: false

  budget:
    reallocation_min_amount: 50          # Minimum reallocation in currency
    require_approval_above: 1000         # Require approval for changes above this
```

---

## Modification Guidelines

### When to Modify
- **Account onboarding:** Set platform config, KPI targets, and naming conventions
- **KPI changes:** When business goals shift or benchmarks are updated
- **Threshold tuning:** When alerts are too sensitive or not sensitive enough
- **Workflow adjustments:** When cadence or automation preferences change
- **New platform:** When adding a new advertising platform

### How to Modify Safely
1. **Back up the current config** before making changes
2. **Change one section at a time** to isolate the impact of changes
3. **Document the reason** for every change in the changelog
4. **Test with a dry run** when possible (workflows, alerts)
5. **Review with the team** before deploying changes to live operations

### Common Mistakes to Avoid
- Setting KPI targets without industry benchmark context
- Making alert thresholds too tight (excessive false positives)
- Enabling auto-actions (auto_reallocate, auto_pause) without sufficient testing
- Forgetting to update timezone when managing accounts in different regions
- Not updating config when platforms change their attribution defaults
