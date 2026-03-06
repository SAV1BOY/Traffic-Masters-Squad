# Tracking QA Runner — Script Guide

## Purpose
Verify that all tracking elements are firing correctly before and after campaign launch.

## Pre-Launch QA Checklist

### Pixel Verification
- [ ] Meta Pixel fires on all pages
- [ ] Google Tag fires on all pages
- [ ] TikTok Pixel fires on all pages (if applicable)
- [ ] LinkedIn Insight Tag fires (if applicable)

### Event Verification
- [ ] PageView fires on every page load
- [ ] ViewContent fires on product/service pages
- [ ] AddToCart fires on cart actions
- [ ] InitiateCheckout fires on checkout start
- [ ] Purchase/Lead fires on conversion
- [ ] Custom events fire as configured

### Server-Side Verification
- [ ] CAPI events sending successfully (Meta)
- [ ] Enhanced Conversions active (Google)
- [ ] Event deduplication working (no double-counting)
- [ ] Event match quality > 6.0 (Meta)

### UTM Verification
- [ ] UTM parameters present in landing page URL
- [ ] UTMs visible in GA4 acquisition reports
- [ ] No broken or malformed parameters
- [ ] Parameters match naming conventions

## QA Tools
- Meta Events Manager (test events tool)
- Google Tag Assistant
- TikTok Pixel Helper
- GA4 DebugView
- Browser developer console (Network tab)
- Charles Proxy / Fiddler (for server-side)

## Post-Launch Monitoring
- Check conversion data matches between platform and GA4
- Monitor event match quality daily for first 48 hours
- Verify attribution is working across all campaigns
- Compare platform-reported vs GA4-reported conversions

## Issue Response
1. Document the issue (what's broken, when noticed)
2. Assess impact (which campaigns affected)
3. Fix or escalate to tracking team
4. Re-QA after fix
5. Log in decisions log
