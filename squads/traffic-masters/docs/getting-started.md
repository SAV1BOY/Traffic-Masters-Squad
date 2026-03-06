# Getting Started with Traffic Masters Squad

> A comprehensive guide for new users to understand, configure, and begin using the Traffic Masters Squad system.

---

## What Is Traffic Masters Squad?

Traffic Masters Squad is a structured system of AI-powered agents, frameworks, templates, and workflows designed to manage, optimize, and scale paid media campaigns across platforms. It provides:

- **16 specialized agents** that handle distinct aspects of campaign management
- **Frameworks** for strategic decision-making at every stage of the campaign lifecycle
- **Checklists** to ensure consistency and quality across all operations
- **Templates** for reporting, analysis, and communication
- **Workflows** that coordinate multi-step processes across agents
- **Phrase libraries** for ready-to-use copy and communication standards

---

## Prerequisites

Before getting started, ensure you have:

1. **Platform access** — Active ad accounts on the platforms you intend to manage (Meta, Google, TikTok, YouTube, LinkedIn)
2. **Analytics access** — GA4, platform analytics, and any third-party measurement tools
3. **Tracking setup** — Pixels, conversion APIs, or tag management systems properly installed
4. **Historical data** — Access to at least 30 days of campaign history (if managing existing accounts)
5. **Brand assets** — Access to brand guidelines, approved creative assets, and messaging frameworks
6. **Business context** — Clear understanding of business goals, KPIs, target audiences, and budget parameters
7. **Communication channels** — Access to project management and team communication tools

---

## Quick Start (5 Steps)

### Step 1: Understand the Squad Structure

- Review `docs/squad-overview.md` for mission, scope, and principles
- Review `docs/agent-catalog.md` for the complete list of 16 agents and their capabilities
- Familiarize yourself with the folder structure:

```
Traffic Masters Squad
|
|-- agents/              # 16 specialized AI agents
|-- frameworks/          # Strategic decision frameworks
|   |-- lib/components/  # Reusable building blocks
|   |-- lib/patterns/    # Proven campaign patterns
|   |-- lib/utilities/   # Decision-making tools
|-- checklists/          # Quality assurance checklists
|-- templates/           # Report and analysis templates
|-- tasks/               # Defined task types with routing
|-- workflows/           # Multi-step coordinated processes
|-- phrases/             # Language libraries for copy and comms
|-- voice/               # Tone and communication standards
|-- scripts/             # Automation routine scripts
|-- swipe/               # Swipe files organized by platform
|-- docs/                # Documentation (you are here)
|-- data/
|   |-- registries/      # Campaign, creative, audience registries
|   |-- metrics/         # Scorecards and performance data
|-- config.yaml          # System configuration
```

### Step 2: Learn the Frameworks

- Browse `lib/components/` for reusable building blocks
- Study `lib/patterns/` for proven campaign patterns
- Review `lib/utilities/` for decision-making tools
- See `docs/framework-catalog.md` for a complete index with when-to-use guidance

### Step 3: Set Up Your Environment

Review and customize the `config.yaml` file to match your specific setup:

```yaml
# Example configuration areas
platforms:
  - meta
  - google_ads
  - tiktok

account_settings:
  currency: USD
  timezone: America/New_York
  attribution_window: 7d_click_1d_view

kpi_targets:
  cpa: 45.00
  roas: 3.5
  ctr: 1.5
```

Additional setup:
- Review `docs/naming-conventions.md` for standard naming
- See `docs/config-yaml-guide.md` for detailed configuration instructions
- Ensure access to all required platforms and tools

### Step 4: Review Active Campaigns

- Check `data/registries/campaigns-registry.yaml` for active campaigns
- Review `data/metrics/weekly-scorecards.md` for current performance
- Understand active experiments in `data/registries/experiments-registry.yaml`
- Run a diagnostic audit using the Diagnostics Agent for baseline assessment

### Step 5: Start Contributing

- Follow `docs/workflow-guide.md` for daily/weekly routines
- Use `docs/checklist-usage-guide.md` for standard operating procedures
- Log decisions in `data/registries/decisions-log.yaml`
- Document learnings in `data/registries/lessons-learned-registry.yaml`

---

## Key Concepts

### Agents
Agents are specialized units that handle specific domains. Each agent has defined capabilities, inputs, outputs, and quality gates. Agents can be invoked individually or coordinated through workflows. See `docs/agent-catalog.md`.

### Frameworks
Frameworks provide structured decision-making models for strategic situations (e.g., budget allocation, creative testing, audience expansion). They define the criteria, decision tree, and expected outcomes. See `docs/framework-catalog.md`.

### Quality Gates
Quality gates are checkpoints that must be passed before work advances to the next stage. They ensure consistency, accuracy, and adherence to standards. See `docs/quality-gates-guide.md`.

### Workflows
Workflows coordinate multiple agents and tasks in sequence. They define triggers, steps, decision points, and outputs. Workflows can be triggered manually or by system events. See `docs/workflow-catalog.md`.

### Registries
Registries are structured records of campaigns, creatives, audiences, and other entities. They provide a single source of truth for the current state of all managed assets. See `docs/data-model.md`.

### Tasks
Tasks are defined units of work with clear inputs, outputs, and routing to the appropriate agent. See `docs/task-catalog.md`.

---

## Common Tasks

| Task | Agent | Description |
|------|-------|-------------|
| Campaign audit | Diagnostics | Full health check of an ad account |
| Weekly report | Reporting | Generate weekly performance summary |
| Creative review | Creative Strategist | Evaluate creative performance and recommend refresh |
| Budget optimization | Budget | Reallocate budget based on marginal efficiency |
| Audience analysis | Audience | Analyze audience performance and recommend changes |
| Campaign launch | Strategy + Launch | Plan and execute a new campaign launch |
| Performance diagnosis | Diagnostics | Investigate a specific performance issue |
| Competitor analysis | Intelligence | Analyze competitor ad activity |

---

## Establishing Your Workflow Cadence

Set up the recurring workflows that keep campaigns healthy:

| Cadence | Workflow | Script | Purpose |
|---------|----------|--------|---------|
| Daily | Morning check | `scripts/daily-check-routine.md` | Monitor for anomalies and quick wins |
| Weekly | Optimization cycle | `scripts/weekly-optimization-routine.md` | Systematic optimization across all campaigns |
| Monthly | Performance report | `scripts/monthly-reporting-routine.md` | Comprehensive performance reporting |
| Monthly | Creative rotation | `scripts/creative-rotation-script.md` | Refresh creative assets |
| Quarterly | Business review | — | Strategic review and planning |

---

## Key Resources

| Resource | Location | Purpose |
|----------|----------|---------|
| Swipe files | `swipe/` | Organized by platform for creative inspiration |
| Phrase libraries | `phrases/` | Ready-to-use copy for ads, reports, and comms |
| Voice guidelines | `voice/` | Tone and communication standards |
| Scripts | `scripts/` | Operational automation routines |
| Templates | `templates/` | Report and analysis templates |
| Checklists | `checklists/` | Quality assurance procedures |

---

## Getting Help

- **Troubleshooting:** See `docs/troubleshooting.md` for common issues and solutions
- **FAQ:** See `docs/faq.md` for frequently asked questions
- **Glossary:** See `docs/glossary.md` for term definitions
- **Contributing:** See `docs/contributing.md` for how to improve the system
- **Cross-squad integration:** See `docs/cross-squad-integration.md` for working with Copy Squad and Brand Squad

---

## Next Steps

1. Read the `docs/agent-catalog.md` to understand all 16 agent capabilities
2. Review the `docs/framework-catalog.md` to see available strategic frameworks
3. Run your first diagnostic audit on an active account
4. Set up your daily, weekly, and monthly routines using the scripts
5. Begin managing campaigns with structured, repeatable processes
6. Review `docs/onboarding-new-account.md` when adding a new ad account
