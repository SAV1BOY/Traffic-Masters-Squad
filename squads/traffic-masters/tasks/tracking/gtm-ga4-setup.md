# GTM and GA4 Setup

> **Type**: Task
> **Category**: tracking
> **Agents**: Pixel Specialist
> **Frameworks**: GTM Container Architecture, GA4 Event Model
> **Checklists**: gtm-ga4-setup-checklist
> **Output template**: templates/gtm-config.md

## ROUTING (from config.yaml)

> **Config key**: `routing.gtm-ga4-setup`
> **Agents**: [pixel-specialist](../../agents/pixel-specialist.md)
> **Frameworks**: `tracking-stack-standard`
> **Checklists**: `tracking/gtm-ga4-event-quality`
> **Templates**: `tracking/gtm-container-template`
> **Registry**: `data/registries/pixels-and-events-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Set up Google Tag Manager containers and GA4 property with proper event configuration, data streams, custom dimensions, and conversion definitions to serve as the central tracking infrastructure.

## Inputs
- Event map with all events and parameters defined
- Website URLs and technical architecture
- GA4 property access and data stream details
- GTM container access (web and server-side if applicable)
- Cross-domain tracking requirements (if applicable)
- Consent management platform details

## Steps
1. Create or audit GTM web container with proper workspace structure
2. Set up the data layer with standardized push events matching the event map
3. Create GTM variables: data layer variables, constant variables, lookup tables
4. Build GTM triggers for each event: page view, click, form submission, custom events
5. Create GA4 configuration tag with proper measurement ID and settings
6. Build GA4 event tags for each custom event with parameter mapping
7. Configure GA4 property: data streams, data retention, cross-domain, referral exclusions
8. Set up custom dimensions and metrics in GA4 for business-specific parameters
9. Define GA4 conversions: mark key events as conversions with proper counting method
10. Configure enhanced measurement settings: scrolls, outbound clicks, site search, video engagement
11. Set up GTM consent mode integration with the consent management platform
12. Publish GTM container to staging for testing before production deployment

## Output
GTM configuration documentation containing: container structure, tag inventory, trigger definitions, variable list, GA4 property settings, custom dimension/metric definitions, consent mode configuration, and deployment checklist.

## Quality Gate
- GTM GA4 setup checklist confirms all tags, triggers, and variables configured
- All events verified firing correctly in GTM preview mode
- GA4 DebugView confirms events arriving with correct parameters

## Duration
4-6 hours for setup; 2-3 hours for testing and documentation
