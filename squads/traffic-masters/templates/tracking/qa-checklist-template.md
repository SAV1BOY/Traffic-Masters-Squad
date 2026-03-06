# QA Checklist Template

> **Type**: Template
> **Category**: tracking
> **Used by tasks**: tracking-qa, pre-launch-verification, debugging
> **Filled by agents**: tracking-agent, qa-agent

## Purpose
Provides a step-by-step QA checklist to verify that all tracking pixels, CAPI events, deduplication, UTM parameters, GA4 events, and platform conversions are firing correctly before a campaign goes live.

## Template

### QA Metadata
**Project / client**: [name]
**QA performed by**: [person or agent]
**QA date**: [date]
**Environment tested**: [production / staging]
**Browser(s) tested**: [Chrome, Safari, Firefox, mobile Safari, mobile Chrome]
**Tools used**: [Meta Pixel Helper, GTM Preview, GA4 DebugView, browser DevTools]

### 1. Verify Pixel Fires
| Check | Status | Notes |
|---|---|---|
| [ ] Meta Pixel loads on all pages | [pass/fail] | [notes] |
| [ ] Meta PageView fires on page load | [pass/fail] | [notes] |
| [ ] Meta ViewContent fires on product/content pages | [pass/fail] | [notes] |
| [ ] Meta AddToCart fires on button click | [pass/fail] | [notes] |
| [ ] Meta InitiateCheckout fires on checkout load | [pass/fail] | [notes] |
| [ ] Meta Purchase fires on confirmation page only | [pass/fail] | [notes] |
| [ ] Meta Lead fires on form submission | [pass/fail] | [notes] |
| [ ] Google Ads remarketing tag fires on all pages | [pass/fail] | [notes] |
| [ ] Google Ads conversion tag fires on conversion page | [pass/fail] | [notes] |
| [ ] TikTok Pixel loads on all pages | [pass/fail] | [notes] |
| [ ] TikTok events fire at correct triggers | [pass/fail] | [notes] |
| [ ] LinkedIn Insight Tag loads on all pages | [pass/fail] | [notes] |
| [ ] No duplicate pixel fires on single page load | [pass/fail] | [notes] |
| [ ] Pixels fire only once per trigger (no double-fires on click) | [pass/fail] | [notes] |

### 2. Check CAPI Events
| Check | Status | Notes |
|---|---|---|
| [ ] CAPI endpoint is configured and reachable | [pass/fail] | [notes] |
| [ ] CAPI events appear in Meta Events Manager Test Events | [pass/fail] | [notes] |
| [ ] CAPI events include required parameters (event_id, user data) | [pass/fail] | [notes] |
| [ ] CAPI event names match browser pixel event names | [pass/fail] | [notes] |
| [ ] CAPI events include hashed user data (email, phone, IP) | [pass/fail] | [notes] |
| [ ] Event match quality score is acceptable (above 6.0) | [pass/fail] | [notes] |
| [ ] CAPI fires for all required events (not just Purchase) | [pass/fail] | [notes] |

### 3. Confirm Deduplication
| Check | Status | Notes |
|---|---|---|
| [ ] event_id is generated and passed in both browser and CAPI events | [pass/fail] | [notes] |
| [ ] event_id is unique per event occurrence | [pass/fail] | [notes] |
| [ ] event_id matches between browser pixel and CAPI for same event | [pass/fail] | [notes] |
| [ ] Meta Events Manager shows deduplicated event count (not doubled) | [pass/fail] | [notes] |
| [ ] Purchase events use order_id for cross-platform dedup | [pass/fail] | [notes] |
| [ ] Page refresh does not re-fire conversion events | [pass/fail] | [notes] |

### 4. Test UTM Parameters
| Check | Status | Notes |
|---|---|---|
| [ ] UTM parameters are present in landing page URL | [pass/fail] | [notes] |
| [ ] UTM source matches platform naming standard | [pass/fail] | [notes] |
| [ ] UTM medium matches paid type naming standard | [pass/fail] | [notes] |
| [ ] UTM campaign matches campaign naming convention | [pass/fail] | [notes] |
| [ ] UTM content identifies the specific creative | [pass/fail] | [notes] |
| [ ] UTM term identifies keyword or audience | [pass/fail] | [notes] |
| [ ] UTMs persist through redirects (no parameter stripping) | [pass/fail] | [notes] |
| [ ] UTMs are captured in hidden form fields for lead attribution | [pass/fail] | [notes] |
| [ ] UTMs appear correctly in GA4 real-time reports | [pass/fail] | [notes] |

### 5. Validate GA4
| Check | Status | Notes |
|---|---|---|
| [ ] GA4 config tag fires on all pages | [pass/fail] | [notes] |
| [ ] Events appear in GA4 DebugView | [pass/fail] | [notes] |
| [ ] Event parameters contain correct values | [pass/fail] | [notes] |
| [ ] Enhanced measurement events fire (scroll, outbound click) | [pass/fail] | [notes] |
| [ ] Ecommerce events follow GA4 ecommerce schema | [pass/fail] | [notes] |
| [ ] Custom dimensions and metrics are receiving data | [pass/fail] | [notes] |
| [ ] Conversions are marked in GA4 admin settings | [pass/fail] | [notes] |
| [ ] User properties are set correctly | [pass/fail] | [notes] |

### 6. Check Platform Conversions
| Check | Status | Notes |
|---|---|---|
| [ ] Meta conversion events appear in Events Manager (last 24h) | [pass/fail] | [notes] |
| [ ] Google Ads conversion actions show "Recording conversions" | [pass/fail] | [notes] |
| [ ] TikTok Events Manager shows received events | [pass/fail] | [notes] |
| [ ] Conversion values are passed correctly (not $0 or null) | [pass/fail] | [notes] |
| [ ] Currency codes are correct (USD, EUR, etc.) | [pass/fail] | [notes] |
| [ ] Attribution windows are set correctly in each platform | [pass/fail] | [notes] |

### QA Sign-Off
**All checks passed**: [yes / no]
**Critical failures**: [list any blocking issues]
**Non-critical issues**: [list any minor issues with workarounds]
**Approved for launch**: [yes / no]
**Approved by**: [name]
**Date**: [date]
**Retest required**: [yes / no - if yes, retest date]

## Usage Notes
- Run this checklist in full before every campaign launch.
- Re-run after any tracking changes, platform updates, or site deploys.
- Use GTM Preview mode and Meta Pixel Helper Chrome extension simultaneously.

## Example
Pre-launch QA for an ecommerce campaign: all 6 sections verified across Chrome and mobile Safari. One CAPI dedup issue found and fixed. Retested and approved for launch.

## Related
- event-map-template.md
- gtm-container-template.md
- tracking-brief.md
