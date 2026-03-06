# Attribution Strategy

> **Type**: Task
> **Category**: strategy
> **Agents**: Pixel Specialist, Performance Analyst
> **Frameworks**: Attribution Modeling Framework, Multi-Touch Attribution
> **Checklists**: attribution-strategy-checklist
> **Output template**: templates/attribution-plan.md

## Objective
Plan the attribution approach including model selection, tool configuration, cross-platform reconciliation methods, and truth-source definition to ensure accurate credit assignment and informed budget decisions.

## Inputs
- Measurement plan with event taxonomy
- Platform list with native attribution capabilities
- Customer journey complexity: single vs multi-touch, cross-device behavior
- Available attribution tools: GA4, platform native, third-party (Triple Whale, Northbeam, etc.)
- Business model: impulse vs considered purchase, B2C vs B2B

## Steps
1. Assess customer journey complexity: average touchpoints, time to conversion, cross-device behavior
2. Evaluate attribution models: last-click, first-click, linear, time-decay, position-based, data-driven
3. Select primary attribution model with documented rationale
4. Define the truth source for conversion data: backend CRM, Shopify, or analytics platform
5. Plan platform-to-backend reconciliation: how to compare Meta reported vs actual conversions
6. Configure attribution windows per platform to align with the sales cycle
7. Design a blended ROAS or blended CPA calculation methodology
8. Plan incrementality testing approach: holdout tests, geo-lift studies, or on/off tests
9. Define the reporting hierarchy: which numbers leadership sees vs media buyers use
10. Set up cross-platform deduplication rules to prevent double-counting
11. Document known attribution gaps and their expected impact on reported numbers

## Output
Attribution plan containing: model selection with rationale, truth-source definition, reconciliation methodology, attribution window settings, blended metrics formulas, incrementality testing roadmap, reporting hierarchy, and known limitations documentation.

## Quality Gate
- Attribution strategy checklist confirms all components defined
- Reconciliation methodology tested with sample data
- Performance Analyst validates blended metrics calculation is sound

## Duration
3-4 hours for strategy and model selection; 1-2 hours for documentation
