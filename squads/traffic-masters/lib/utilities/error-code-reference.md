# Error Code Reference

## Purpose
Quick reference for common advertising platform error codes, disapproval reasons, and troubleshooting steps. Enables fast resolution of campaign delivery issues.

---

## Meta Ads (Facebook / Instagram)

### Ad Disapproval Reasons

| Error / Reason | Description | Fix |
|---|---|---|
| **Policy 1.1 - Misleading Claims** | Ad makes exaggerated or unsubstantiated claims | Remove "guaranteed" language, add disclaimers, tone down claims |
| **Policy 2 - Deceptive Content** | Ad is misleading about product/service | Ensure ad accurately represents what user will see after clicking |
| **Policy 4 - Personal Attributes** | Ad asserts or implies personal attributes (age, race, health) | Remove "Are you overweight?" type language; use general framing |
| **Policy 5 - Adult Content** | Sexually suggestive imagery or text | Replace imagery, tone down suggestive content |
| **Policy 6 - Sensational Content** | Shocking or excessively violent content | Use less provocative imagery and language |
| **Policy 9 - Non-Functional LP** | Landing page does not work or is under construction | Fix landing page, ensure it loads quickly on mobile |
| **Policy 10 - Personal Health** | References specific health conditions | Use general wellness language, avoid medical claims |
| **Policy 13 - Low Quality** | Ad uses engagement bait, clickbait, or sensationalism | Remove "You won't believe..." or similar bait tactics |
| **Policy 14 - Prohibited Content** | Advertising prohibited products (weapons, drugs, etc.) | Cannot advertise this product on Meta |
| **Policy 17 - Cryptocurrency** | Crypto ads require prior written permission | Apply for crypto advertising approval |
| **Special Ad Category Required** | Housing, credit, or employment ads need special category | Select appropriate special ad category in campaign settings |
| **Text in Image > 20%** | Image has too much text (not enforced as hard rule now, but affects delivery) | Reduce text overlay, use the Text Overlay tool to check |
| **Account Disabled** | Ad account has been disabled for policy violations | Submit appeal through Account Quality |

### Delivery Issues

| Issue | Symptom | Diagnosis | Fix |
|---|---|---|---|
| **Learning Limited** | Ad set stuck in "Learning Limited" | Not enough conversions (< 50/week) | Broaden audience, increase budget, simplify conversion event |
| **Not Delivering** | Zero impressions | Multiple possible causes | Check: ad approval, budget, schedule, audience size, billing |
| **Auction Overlap** | Multiple ad sets compete against each other | Overlapping audiences | Consolidate ad sets, use audience exclusions |
| **In Review** | Ad stuck in review for 24+ hours | Normal during high-volume periods | Wait 48 hours, then contact support |
| **Payment Failed** | Billing error stops delivery | Payment method declined | Update payment method, check spending limit |
| **Spending Limit Reached** | Account spending limit hit | Account-level cap reached | Increase or remove spending limit in settings |

### API Error Codes

| Code | Error | Fix |
|---|---|---|
| `1` | Unknown error | Retry request; if persistent, contact support |
| `2` | Service temporarily unavailable | Retry with exponential backoff |
| `4` | Too many API calls | Reduce request frequency, implement rate limiting |
| `17` | User request limit reached | Wait and retry after cooldown period |
| `100` | Invalid parameter | Check API documentation for correct parameters |
| `190` | Invalid access token | Refresh or regenerate access token |
| `200` | Permission error | Check app permissions and user role |
| `2635` | Campaign spending limit reached | Increase campaign spending limit |

---

## Google Ads

### Ad Disapproval Reasons

| Reason | Description | Fix |
|---|---|---|
| **Misleading Content** | Ad does not accurately represent product/landing page | Align ad copy with landing page content |
| **Malicious Software** | Landing page flagged for malware | Scan and clean landing page, request re-review |
| **Destination Not Working** | Landing page returns 404 or error | Fix URL, check server, ensure page is live |
| **Restricted Content** | Product/service has advertising restrictions | Review Google Ads policies for your industry |
| **Trademark** | Using competitor's trademarked term in ad text | Remove trademark from ad copy (can still bid on keyword) |
| **Healthcare-Related Content** | Medical claims or restricted health products | Follow Google's healthcare advertising policies |
| **Financial Services** | Missing required disclosures | Add required financial disclaimers |
| **Counterfeit Goods** | Selling counterfeit products | Cannot advertise counterfeit goods |
| **Missing Information** | Required business information not provided | Complete advertiser verification |
| **Editorial (Punctuation)** | Excessive punctuation, all caps, or gimmicky text | Fix: "BEST DEAL!!!" to "Best Deal" |
| **Editorial (Spacing)** | Unusual spacing in ad text | Use standard spacing |
| **Phone Number in Ad** | Phone number in ad text where not allowed | Use call extensions instead |

### Campaign Issues

| Issue | Symptom | Fix |
|---|---|---|
| **Low Search Volume** | Keywords marked "Low search volume" | Remove or replace with broader keywords |
| **Below First Page Bid** | Ads not showing on first page | Increase bid or improve Quality Score |
| **Quality Score Low (< 5)** | High CPC, low position | Improve ad relevance, CTR, and landing page experience |
| **Budget Constrained** | "Limited by budget" status | Increase daily budget or reduce keyword scope |
| **Bid Strategy Learning** | "Learning" status on Smart Bidding | Wait 1-2 weeks, ensure sufficient conversions |
| **Conversion Tracking Issue** | "No recent conversions" warning | Verify conversion tags, check tag firing |
| **Disapproved Sitelink** | Sitelink extension disapproved | Fix destination URL or editorial issue |

### API Error Codes

| Code | Error | Fix |
|---|---|---|
| `AUTHENTICATION_ERROR` | Invalid credentials | Check OAuth tokens, developer token |
| `AUTHORIZATION_ERROR` | Insufficient permissions | Check access level for the account |
| `INTERNAL_ERROR` | Google internal error | Retry request |
| `QUOTA_ERROR` | Rate limit exceeded | Reduce request frequency |
| `REQUEST_ERROR` | Malformed request | Check request syntax and parameters |
| `MUTATE_ERROR` | Cannot modify resource | Check resource status and constraints |
| `RESOURCE_NOT_FOUND` | Entity does not exist | Verify IDs and resource paths |

---

## TikTok Ads

### Ad Disapproval Reasons

| Reason | Description | Fix |
|---|---|---|
| **Unacceptable Business** | Prohibited product or service | Review TikTok's prohibited industries list |
| **Adult Content** | Sexually suggestive content | Use appropriate imagery and language |
| **Misleading Information** | Exaggerated claims | Substantiate claims, remove absolutes |
| **Poor Ad Quality** | Low-resolution or unprofessional content | Improve video quality, use higher resolution |
| **Landing Page Issues** | LP not accessible or inconsistent with ad | Fix landing page, ensure mobile-friendly |
| **Intellectual Property** | Using copyrighted music or content | Use royalty-free audio, remove copyrighted content |
| **Before/After Images** | Weight loss or cosmetic before/after comparisons | Remove before/after comparisons |
| **Targeting Minors** | Ad content targeting users under 18 | Adjust content and targeting settings |

### Delivery Issues

| Issue | Fix |
|---|---|
| **Under Review** | Wait 24 hours; if still pending, contact support |
| **Not Spending** | Check audience size (minimum 10,000), increase bid, check schedule |
| **Learning Phase** | Wait for 50 conversions; do not make changes |
| **Low Bid** | Increase bid or switch to automatic bidding |

---

## LinkedIn Ads

### Common Disapproval Reasons

| Reason | Fix |
|---|---|
| **Misleading Claims** | Remove unsubstantiated claims; add sources |
| **Grammar/Spelling** | Fix grammatical errors in ad copy |
| **Discriminatory Content** | Remove any content that targets protected classes |
| **Unacceptable LP** | Fix landing page issues (speed, content mismatch) |
| **Adult Content** | Not permitted on LinkedIn |
| **Third-Party Data** | Remove claims about LinkedIn or third-party data usage |

---

## Tracking and Pixel Errors

### Meta Pixel / CAPI

| Issue | Symptom | Fix |
|---|---|---|
| **Pixel Not Firing** | No events in Events Manager | Reinstall pixel code, check for JS errors |
| **Duplicate Events** | Double-counted conversions | Check for multiple pixel installations, add deduplication |
| **Event Match Quality Low** | Low score in Events Manager | Send more customer parameters (email, phone) via CAPI |
| **CAPI Disconnected** | Server events not received | Check server-side integration, API token |
| **Domain Not Verified** | Aggregated Event Measurement issues | Verify domain in Business Manager |
| **Event Configuration Issue** | Wrong events prioritized | Configure event priorities in Events Manager |

### Google Tag / Conversion Tracking

| Issue | Symptom | Fix |
|---|---|---|
| **Tag Not Firing** | No conversions recorded | Use Tag Assistant to debug, check tag placement |
| **Conversion Lag** | Conversions appear days later | Normal for some attribution windows; document |
| **Enhanced Conversions Error** | Low match rate | Ensure hashed user data is being sent correctly |
| **Cross-Domain Tracking Broken** | Sessions splitting across domains | Configure cross-domain tracking in GA4 and GTM |
| **Consent Mode Blocking** | Tags blocked by consent banner | Configure Consent Mode v2 in GTM |

---

## Troubleshooting Workflow

```
1. Identify the error/issue
2. Check this reference for the specific error code or reason
3. Apply the documented fix
4. If fix does not resolve:
   a. Check platform-specific help center
   b. Contact platform support (with error code and account ID)
   c. Document the issue and resolution for team reference
5. Verify the fix worked (ad approved, tracking firing, delivery resumed)
```

---

## Support Contact Channels

| Platform | Support Method | Response Time | How to Access |
|---|---|---|---|
| **Meta** | Business Help Center chat | 24-48 hours | business.facebook.com/help |
| **Google Ads** | Phone, chat, email | Same day (phone) | Support tab in Google Ads |
| **TikTok** | In-platform support | 24-48 hours | Help center in Ads Manager |
| **LinkedIn** | Help center form | 48-72 hours | linkedin.com/help |

**Tip:** When contacting support, always include: Account ID, Campaign/Ad ID, Error code or screenshot, Date/time of issue, Steps already taken.
