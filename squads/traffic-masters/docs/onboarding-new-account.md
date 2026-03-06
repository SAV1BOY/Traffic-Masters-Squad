# Onboarding a New Ad Account

> Step-by-step guide for onboarding a new advertising account into the Traffic Masters Squad system.

---

## Onboarding Timeline

| Phase | Duration | Activities |
|-------|----------|-----------|
| Phase 1: Intake | Days 1-2 | Information gathering, access setup |
| Phase 2: Audit | Days 3-5 | Account audit, tracking audit |
| Phase 3: Strategy | Days 5-8 | Strategy development, KPI setting |
| Phase 4: Setup | Days 8-12 | Campaign configuration, tracking, creative |
| Phase 5: Launch | Days 12-15 | Campaign activation, monitoring setup |
| Phase 6: Stabilization | Days 15-30 | Initial optimization, baseline establishment |

---

## Phase 1: Intake (Days 1-2)

### Step 1.1: Complete Onboarding Questionnaire

Gather the following information from the client or stakeholder:

**Business Information**
- Company name, industry, and business model
- Products/services being advertised
- Revenue model (e-commerce, lead gen, SaaS, services)
- Average order value / deal size / customer lifetime value
- Current monthly revenue and growth targets

**Marketing Context**
- Previous advertising history and results
- Current marketing channels and performance
- Existing brand guidelines and creative assets
- Competitive landscape awareness
- Seasonal patterns and key dates

**Goals & KPIs**
- Primary business objective (revenue, leads, awareness)
- Target KPIs (CPA, ROAS, CPL, volume targets)
- Budget (monthly/quarterly/annual)
- Timeline and key milestones
- How success will be measured

**Audience Information**
- Target customer profile (demographics, psychographics)
- Existing customer data availability (CRM, email lists)
- Geographic targeting requirements
- Known high-value customer characteristics
- Current website traffic volume

### Step 1.2: Set Up Platform Access

- [ ] Request and verify access to all ad platform accounts
- [ ] Confirm access levels (admin vs. analyst vs. read-only)
- [ ] Request access to analytics tools (GA4, etc.)
- [ ] Request access to CRM or customer data platform
- [ ] Request access to landing page / website backend (if needed)
- [ ] Verify all access is working

### Step 1.3: Initialize Registries

- [ ] Create campaign registry entries for existing campaigns (if any)
- [ ] Assign account ID in config.yaml
- [ ] Set up naming conventions (or confirm client preferences)
- [ ] Create initial entries in decisions log

---

## Phase 2: Audit (Days 3-5)

### Step 2.1: Account Audit

Run the full Account Audit Checklist. Document findings across:

**Structure Assessment**
- How many campaigns exist and how are they organized?
- Are naming conventions consistent?
- Is the campaign-to-objective mapping logical?
- Are there dormant or redundant campaigns?

**Performance Assessment**
- What are the current KPI levels (CPA, ROAS, CTR, etc.)?
- What are the trends over the last 30/60/90 days?
- Which campaigns/audiences/creatives are top and bottom performers?
- How does performance compare to industry benchmarks?

**Audience Assessment**
- What audiences are currently targeted?
- Is there audience overlap between campaigns?
- Are exclusions properly configured?
- What is the current frequency across audiences?

**Creative Assessment**
- How many active creatives are running?
- What is the creative diversity (formats, hooks, angles)?
- Are there signs of creative fatigue?
- When was the last creative refresh?

**Budget Assessment**
- How is budget currently allocated?
- Is pacing accurate?
- Are there obvious reallocation opportunities?

### Step 2.2: Tracking Audit

Run the full Tracking Audit Checklist:

- [ ] Verify pixel/tag installation on all pages
- [ ] Confirm conversion events are firing correctly
- [ ] Validate event parameters (value, currency, content ID)
- [ ] Check server-side tracking (CAPI) status
- [ ] Measure platform vs. analytics data discrepancy
- [ ] Audit UTM implementation
- [ ] Document attribution window settings
- [ ] Test cross-domain tracking (if applicable)
- [ ] Verify cookie consent compliance

### Step 2.3: Compile Audit Report

Produce an Account Audit Report with:
- Executive summary of findings
- Prioritized issue list with severity ratings
- Baseline metric documentation
- Recommended action plan

---

## Phase 3: Strategy (Days 5-8)

### Step 3.1: Define KPI Framework

Based on audit findings and business goals:
- Set primary KPI targets (CPA, ROAS, CPL)
- Set secondary KPI targets (CTR, CPC, conversion rate)
- Define benchmark comparisons (industry, historical, competitive)
- Configure thresholds and alerts in config.yaml

### Step 3.2: Develop Campaign Strategy

- Define full-funnel campaign architecture
- Map audiences to funnel stages
- Select platforms and placement strategy
- Create media plan with budget allocation
- Define creative strategy and format mix
- Establish testing roadmap

### Step 3.3: Plan Initial Campaigns

For each planned campaign:
- Complete a Campaign Brief
- Define audience targeting specifications
- Outline creative requirements
- Set budget and bid strategy
- Define tracking and attribution approach

---

## Phase 4: Setup (Days 8-12)

### Step 4.1: Fix Critical Issues

Address any critical findings from the audit:
- Fix broken tracking
- Correct misconfigured settings
- Pause wasteful campaigns
- Implement missing exclusions

### Step 4.2: Build Audiences

- Create new audience segments per strategy
- Build lookalike audiences from best customer data
- Configure retargeting audiences with appropriate windows
- Set up exclusion lists
- Register all audiences in the audience registry

### Step 4.3: Prepare Creative

- Develop creative briefs for initial campaigns
- Produce or request ad copy
- Source or produce creative assets
- Ensure brand compliance
- Register all creatives in the creative registry

### Step 4.4: Configure Campaigns

- Set up campaign structure per strategy
- Configure targeting, bidding, and scheduling
- Input creative assets and copy
- Set up UTM parameters
- Complete Pre-Launch Checklist for each campaign

### Step 4.5: Verify Tracking

- Confirm all tracking is firing on test transactions
- Verify UTMs are capturing correctly in analytics
- Test conversion event triggering
- Confirm attribution windows are set correctly

---

## Phase 5: Launch (Days 12-15)

### Step 5.1: Pre-Launch Review

- All Pre-Launch Checklists completed
- Stakeholder approval obtained
- Monitoring plan established
- Alert thresholds configured
- Team notified of launch schedule

### Step 5.2: Activate Campaigns

- Launch campaigns in planned sequence
- Confirm delivery begins within expected timeframe
- Verify spend pacing
- Confirm tracking is recording conversions
- Check for ad disapprovals

### Step 5.3: 72-Hour Monitoring

Follow the Post-Launch Monitoring Checklist:
- Monitor every 4 hours for the first 24 hours
- Check twice daily for days 2-3
- Flag any anomalies for immediate investigation
- Document initial performance observations

---

## Phase 6: Stabilization (Days 15-30)

### Step 6.1: Initial Optimization

- Allow campaigns to exit learning phase (do not make major changes)
- Monitor performance trends
- Make minor adjustments only if critical issues arise
- Begin building performance baselines

### Step 6.2: Establish Baselines

After 14+ days of data:
- Document baseline metrics for all primary and secondary KPIs
- Compare baselines to targets and benchmarks
- Identify early winners and underperformers

### Step 6.3: Set Up Recurring Workflows

- Activate daily monitoring routine
- Schedule weekly optimization cycle
- Schedule first monthly report
- Plan first creative refresh cycle
- Set up the reporting cadence with stakeholders

### Step 6.4: 30-Day Review

At the 30-day mark:
- Compile first monthly performance report
- Compare results to initial targets and audit baseline
- Assess strategy effectiveness
- Develop optimization and testing roadmap for month 2+
- Present findings and plan to stakeholders

---

## Onboarding Completion Criteria

The account is considered fully onboarded when:

- [ ] All platform access is verified
- [ ] Tracking is verified and accurate
- [ ] Config.yaml is fully configured for the account
- [ ] All registries have initial entries
- [ ] At least one campaign is live and delivering
- [ ] Performance baselines are documented
- [ ] Recurring workflows are scheduled
- [ ] First reporting cadence is established
- [ ] Stakeholder alignment meeting completed
- [ ] 30-day review is scheduled
