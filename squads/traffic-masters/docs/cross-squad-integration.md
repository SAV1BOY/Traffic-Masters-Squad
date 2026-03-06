# Cross-Squad Integration Guide

> Guide to integrating Traffic Masters Squad with Copy Squad, Brand Squad, and other squads in the ecosystem.

---

## Overview

Traffic Masters Squad does not operate in isolation. It relies on and contributes to other squads for content, brand consistency, and strategic alignment. This guide defines the integration points, data flows, and coordination protocols.

---

## Squad Ecosystem

```
                    Brand Squad
                   (Brand identity,
                    guidelines, voice)
                        |
                        v
Copy Squad <------> Traffic Masters Squad
(Content,               (Paid media,
 messaging,              campaigns,
 copywriting)            optimization)
```

---

## Integration with Copy Squad

### What Copy Squad Provides to Traffic Masters
| Asset | Description | Location |
|-------|-------------|----------|
| Brand messaging frameworks | Core messages, value propositions, positioning statements | `copy-squad/messaging/` |
| Long-form copy | Email sequences, landing page copy, blog content for promotion | `copy-squad/content/` |
| Copy testing results | Learnings from copy tests that inform ad copy | `copy-squad/data/test-results/` |
| Tone and voice guidelines | Writing style, do's and don'ts, vocabulary | `copy-squad/voice/` |

### What Traffic Masters Provides to Copy Squad
| Asset | Description | Location |
|-------|-------------|----------|
| Ad copy performance data | Which hooks, headlines, and CTAs perform best | `traffic-masters/data/metrics/` |
| Audience insights | What resonates with different audience segments | `traffic-masters/data/registries/` |
| Top-performing ad copy | Winning ad copy for repurposing in other channels | `traffic-masters/swipe/` |
| Conversion data | Which messages drive actual conversions vs. just clicks | `traffic-masters/data/metrics/` |

### Coordination Protocol
1. **Weekly sync:** Share top-performing copy and audience insights
2. **Creative briefs:** Traffic Masters submits creative briefs to Copy Squad for ad copy production
3. **Test alignment:** Coordinate copy testing so ad tests and content tests don't conflict
4. **Shared phrase library:** Maintain shared access to `phrases/` for consistent terminology

### Workflow Integration Points
- **New campaign launch:** Copy Squad produces ad copy based on Traffic Masters' creative brief
- **Creative refresh:** Traffic Masters requests new copy variations when fatigue is detected
- **Landing page optimization:** Both squads collaborate on message match between ads and pages
- **Reporting:** Traffic Masters shares performance data on Copy Squad-produced assets

---

## Integration with Brand Squad

### What Brand Squad Provides to Traffic Masters
| Asset | Description | Location |
|-------|-------------|----------|
| Brand guidelines | Visual identity, logo usage, color palette, typography | `brand-squad/guidelines/` |
| Brand voice | Tone, personality, communication principles | `brand-squad/voice/` |
| Approved imagery | Brand-approved photos, illustrations, templates | `brand-squad/assets/` |
| Brand strategy | Positioning, differentiation, brand architecture | `brand-squad/strategy/` |

### What Traffic Masters Provides to Brand Squad
| Asset | Description | Location |
|-------|-------------|----------|
| Brand perception data | How audiences respond to brand messaging in ads | `traffic-masters/data/metrics/` |
| Competitive brand intelligence | How competitors position themselves in paid media | `traffic-masters/data/competitive/` |
| Creative performance by brand element | Which brand elements (colors, imagery, tone) perform best | `traffic-masters/data/metrics/` |
| Audience brand sentiment signals | Engagement and response patterns indicating brand perception | `traffic-masters/data/registries/` |

### Coordination Protocol
1. **Brand compliance review:** All ad creative passes through Brand Squad approval before launch
2. **Quarterly brand alignment:** Review ad creative for brand consistency each quarter
3. **Brand evolution input:** Traffic Masters provides data to inform brand guideline updates
4. **Asset requests:** Formal process for requesting new brand assets for ad campaigns

### Workflow Integration Points
- **Creative development:** Brand guidelines are referenced in every creative brief
- **Compliance review:** Brand Squad reviews creative before launch (part of Creative Review Checklist)
- **Campaign reporting:** Brand lift and sentiment metrics shared with Brand Squad
- **Competitive intelligence:** Brand positioning insights shared through Intelligence Agent

---

## Data Flow Architecture

### Outbound Data (Traffic Masters -> Other Squads)
```yaml
outbound:
  - type: performance_data
    destination: copy_squad
    frequency: weekly
    format: summary_report
    content: top_performing_copy, audience_insights, conversion_data

  - type: brand_insights
    destination: brand_squad
    frequency: monthly
    format: insight_brief
    content: brand_perception, creative_performance_by_brand_element

  - type: competitive_intelligence
    destination: brand_squad, copy_squad
    frequency: quarterly
    format: competitive_report
    content: competitor_messaging, competitor_creative, market_trends
```

### Inbound Data (Other Squads -> Traffic Masters)
```yaml
inbound:
  - type: brand_guidelines
    source: brand_squad
    frequency: on_update
    format: guideline_document
    usage: creative_review, creative_brief

  - type: ad_copy
    source: copy_squad
    frequency: per_request
    format: copy_document
    usage: ad_creation, creative_testing

  - type: messaging_framework
    source: copy_squad
    frequency: quarterly
    format: framework_document
    usage: campaign_strategy, creative_brief
```

---

## Shared Resources

### Shared Directories
| Path | Owner | Shared With | Contents |
|------|-------|-------------|----------|
| `shared/phrases/` | Traffic Masters | Copy Squad | Phrase libraries |
| `shared/brand-assets/` | Brand Squad | Traffic Masters, Copy Squad | Approved imagery and templates |
| `shared/voice-guidelines/` | Brand Squad | Traffic Masters, Copy Squad | Tone and voice documents |
| `shared/performance-data/` | Traffic Masters | Copy Squad | Anonymized performance metrics |

### Shared Conventions
- All squads use the same naming conventions for shared assets
- Dates follow ISO 8601 format (YYYY-MM-DD)
- Currency values include the currency code
- Metric definitions are standardized across squads (see `docs/glossary.md`)

---

## Escalation & Conflict Resolution

### Common Conflicts
| Conflict | Resolution |
|----------|-----------|
| Brand guidelines restrict high-performing creative | Discuss with Brand Squad; test compliant variations |
| Copy Squad deliverables delayed | Use phrase libraries for interim copy; flag delay in weekly sync |
| Inconsistent messaging across squads | Integration Agent aligns all parties to messaging framework |
| Data interpretation disagreements | Refer to standardized metric definitions and attribution model |

### Escalation Path
1. **Agent-level resolution:** Integration Agent coordinates between squad agents
2. **Squad lead discussion:** Squad owners discuss and resolve
3. **Stakeholder decision:** Escalate to shared stakeholder for final decision

---

## Setting Up a New Integration

1. **Identify touchpoints** — Map where the squads interact and what data flows between them
2. **Define protocols** — Agree on cadence, format, and responsibility for each touchpoint
3. **Configure shared access** — Set up shared directories and permissions
4. **Establish sync schedule** — Set recurring meetings or async check-ins
5. **Document in config.yaml** — Update the integrations section of the config
6. **Test the flow** — Run through one complete cycle to validate the integration
7. **Monitor and adjust** — Review integration effectiveness quarterly
