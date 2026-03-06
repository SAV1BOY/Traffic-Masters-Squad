# Pixel and CAPI Setup

> **Type**: Task
> **Category**: tracking
> **Agents**: Pixel Specialist
> **Frameworks**: Server-Side Tracking Architecture, Event Deduplication
> **Checklists**: pixel-capi-setup-checklist
> **Output template**: templates/tracking-documentation.md

## Objective
Set up browser-side pixels and server-side Conversions API (CAPI) for all advertising platforms with proper deduplication to maximize event match quality and ensure reliable conversion data despite browser privacy restrictions.

## Inputs
- Event map with platform-specific event definitions
- Platform pixel IDs: Meta, TikTok, Google, LinkedIn, etc.
- Server-side endpoint or partner integration details
- Website platform and technical capabilities (Shopify, WordPress, custom)
- GTM server-side container (if applicable)
- Access tokens and API credentials for each platform

## Steps
1. Install browser-side pixels for each platform via GTM or direct code
2. Verify browser pixel fires correctly for all mapped events using platform debug tools
3. Set up server-side CAPI for Meta: configure access token, test events, verify match keys
4. Set up server-side tracking for Google: enhanced conversions, offline conversion import
5. Set up TikTok Events API with proper event matching
6. Configure event deduplication using event_id parameter matching between browser and server
7. Maximize event match quality: pass email, phone, IP, user agent, fbp, fbc parameters
8. Test deduplication by verifying events are not double-counted in platform dashboards
9. Configure consent-aware firing: only send user data when consent is granted
10. Set up monitoring alerts for tracking failures or significant event volume drops
11. Document the complete tracking architecture with data flow diagrams

## Output
Tracking documentation containing: pixel installation details per platform, CAPI configuration specs, deduplication logic, match quality scores, consent integration details, monitoring setup, data flow diagram, and troubleshooting guide.

## Quality Gate
- Pixel CAPI setup checklist confirms all platforms configured with server-side tracking
- Event match quality score above 6.0 for Meta (good or great rating)
- Deduplication verified: no double-counting in any platform's event manager

## Duration
6-10 hours for full setup across platforms; 2-3 hours for testing and documentation
