# Tracking Audit Script — Automation Script

> Tracking implementation audit automation for verifying data integrity across all touchpoints.

---

## Purpose

Systematically verify that all tracking implementations are functioning correctly, data is flowing accurately, and attribution is properly configured. Data integrity is the foundation of all performance decisions.

---

## Trigger / Schedule

- **Scheduled trigger:** Monthly (or quarterly for stable accounts)
- **Event trigger:** New account onboarding, platform migration, website changes
- **Alert trigger:** Conversion data discrepancy > 20%, sudden drop in reported conversions
- **Duration:** 1-2 hours per account
- **Owner:** Tracking Agent
- **Supporting Agents:** Launch Agent, Diagnostics Agent

---

## Pre-Conditions

- [ ] Access to ad platform accounts
- [ ] Access to website / analytics backend
- [ ] Access to tag management system (GTM or equivalent)
- [ ] Access to analytics tool (GA4 or equivalent)
- [ ] Test transaction capability (ability to trigger conversion events)
- [ ] Tracking Audit Checklist available

---

## Step-by-Step Workflow

### Step 1: Pixel / Tag Presence Verification (15 minutes)

```yaml
action: Verify tracking code is present on all required pages
check_method: "Browser developer tools, platform pixel helper, GTM preview"
pages_to_check:
  - Homepage
  - Primary landing pages (all active campaign destinations)
  - Product / service pages
  - Cart / checkout pages (e-commerce)
  - Form pages (lead gen)
  - Thank you / confirmation pages
  - Key content pages
for_each_page:
  verify:
    - [ ] Base pixel code is present and loading
    - [ ] No JavaScript errors blocking pixel execution
    - [ ] Pixel loads before user can interact (not deferred too late)
    - [ ] Correct pixel ID is referenced
    - [ ] Cookie consent integration works (pixel respects consent state)
output: Page-by-page pixel presence report
```

### Step 2: Conversion Event Verification (20 minutes)

```yaml
action: Verify all conversion events fire correctly
for_each_conversion_event:
  events_to_test:
    - PageView (all pages)
    - ViewContent (product/service pages)
    - AddToCart (cart addition)
    - InitiateCheckout (checkout start)
    - Purchase (order confirmation)
    - Lead (form submission)
    - CompleteRegistration (sign-up)
    - Custom events (account-specific)
  test_method:
    - Trigger each event through a test transaction
    - Verify event appears in platform's event manager
    - Confirm event parameters are correct
  parameters_to_verify:
    - Event name (matches platform expected name)
    - Value (correct currency amount)
    - Currency (correct ISO code)
    - Content ID / Content Type (if applicable)
    - Custom parameters (if configured)
  decision:
    event_fires_correctly: "Mark as verified"
    event_missing_or_broken: "Flag as critical, document issue"
    parameters_incorrect: "Flag as high priority, document discrepancy"
```

### Step 3: Server-Side Tracking Verification (15 minutes)

```yaml
action: Verify server-side tracking (CAPI) if implemented
checks:
  - [ ] CAPI is sending events to the platform
  - [ ] Events match client-side events (no duplication without deduplication)
  - [ ] Deduplication is working (event_id matching)
  - [ ] Event match quality score is acceptable (Meta: aim for Good or Great)
  - [ ] All required parameters are being sent server-side
  - [ ] Latency is within acceptable range (events sent within minutes)
if_not_implemented:
  recommendation: "Implement CAPI to recover data lost to ad blockers and browser privacy"
  estimated_data_recovery: "10-30% improvement in conversion data match rate"
```

### Step 4: UTM Parameter Audit (15 minutes)

```yaml
action: Verify UTM consistency across all active campaigns
checks:
  for_each_active_campaign:
    - [ ] utm_source is correct and consistent
    - [ ] utm_medium is correct and consistent
    - [ ] utm_campaign matches campaign naming convention
    - [ ] utm_content identifies the specific creative
    - [ ] utm_term identifies the keyword or audience (if applicable)
    - [ ] No formatting errors (proper ?/& usage, no spaces, no duplicate ?)
    - [ ] UTMs are not stripped by redirects
  verification:
    - Click through active ads and verify UTMs appear in browser URL
    - Check analytics platform for "(not set)" or unexpected values
    - Compare UTM values against the documented convention
output: UTM audit report with discrepancies flagged
```

### Step 5: Cross-Platform Data Reconciliation (15 minutes)

```yaml
action: Compare conversion data across platforms
comparison:
  for_each_platform:
    metrics:
      - Platform-reported conversions (last 7 days)
      - Analytics-reported conversions attributed to that platform
      - CRM-reported conversions attributed to that platform
    calculate:
      - Discrepancy percentage (platform vs. analytics)
      - Discrepancy percentage (platform vs. CRM)
    evaluate:
      acceptable: "Discrepancy < 20% (expected due to attribution differences)"
      concerning: "Discrepancy 20-40% (investigate cause)"
      critical: "Discrepancy > 40% (likely tracking issue, escalate)"
  common_discrepancy_causes:
    - Different attribution windows
    - View-through conversions included in platform, not analytics
    - Ad blockers preventing client-side tracking
    - Cross-domain tracking misconfiguration
    - Cookie consent blocking
output: Cross-platform reconciliation report with explanations
```

### Step 6: Attribution Configuration Review (10 minutes)

```yaml
action: Verify attribution settings are correct and documented
review:
  for_each_platform:
    - [ ] Attribution window matches strategy (e.g., 7d click, 1d view)
    - [ ] Attribution model is documented
    - [ ] Any recent changes to attribution settings are noted
    - [ ] Impact of attribution settings on reported data is understood
  documentation:
    - Record current attribution settings for each platform
    - Note any differences between platforms
    - Flag if settings have changed since last audit
```

### Step 7: Documentation and Remediation Plan (10 minutes)

```yaml
action: Compile findings and create remediation plan
output:
  tracking_audit_report:
    - Summary of findings (pass/fail per check)
    - Critical issues requiring immediate fix
    - High-priority issues to fix within the week
    - Medium-priority recommendations
    - Discrepancy baselines for ongoing monitoring
  remediation_plan:
    for_each_issue:
      - Issue description
      - Severity (critical / high / medium / low)
      - Recommended fix
      - Owner
      - Target fix date
      - Verification method after fix
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Pixel missing on conversion page | Critical: fix immediately, pause affected campaigns |
| Event parameters incorrect | High: fix within 24 hours |
| CAPI not implemented | Medium: recommend implementation, estimate data recovery |
| UTM inconsistencies | Medium: fix in next optimization cycle |
| Discrepancy > 40% | Critical: investigate and resolve immediately |
| Attribution settings changed | Document impact, recalibrate benchmarks |

---

## Output / Deliverables

- Tracking audit report (pass/fail per check)
- Cross-platform data reconciliation report
- UTM audit report
- Remediation plan with priorities and owners
- Updated attribution documentation
- Baseline discrepancy measurements

---

## Post-Conditions

- [ ] All tracking touchpoints verified
- [ ] All conversion events tested
- [ ] UTM parameters audited across active campaigns
- [ ] Cross-platform discrepancies measured and documented
- [ ] Attribution settings verified and documented
- [ ] Critical issues escalated for immediate fix
- [ ] Remediation plan created and assigned
- [ ] Next audit date scheduled
