# Audience Component

## Purpose
Standardized format for defining and documenting audience segments.

## Component Fields
- `audience_id`: Identifier
- `name`: Descriptive name
- `platform`: Where this audience is deployed
- `type`: Cold / Warm / Hot / Lookalike / Custom
- `funnel_stage`: TOFU / MOFU / BOFU / Retention

## Audience Definition Template

### Demographics
- Age range, gender, location, language, income level

### Interests & Behaviors
- Platform-specific interest targeting
- Purchase behaviors, device usage

### Custom Audiences
- Source: website visitors, email list, video viewers, engagers
- Window: 1-day, 7-day, 30-day, 90-day, 180-day
- Event: page view, add to cart, purchase, lead

### Lookalike Audiences
- Source audience and quality
- Percentage: 1%, 2-5%, 5-10%
- Country/region

## Audience Layering Strategy

| Layer | Audience | Funnel Stage | Expected CPA |
|-------|----------|-------------|-------------|
| 1 | Broad / Interest | TOFU | Highest |
| 2 | Lookalike 1-3% | TOFU | Medium-High |
| 3 | Engagers / Visitors | MOFU | Medium |
| 4 | ATC / Leads | BOFU | Low |
| 5 | Customers | Retention | Lowest |

## Exclusion Rules
- Always exclude existing customers from prospecting
- Exclude converters from lead gen campaigns
- Exclude recent purchasers (window depends on repurchase cycle)
