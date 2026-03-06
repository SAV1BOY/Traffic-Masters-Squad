# Diagnostics Pattern

## Purpose
Structured pattern for diagnosing performance issues in paid traffic campaigns. Provides a systematic approach to identifying root causes rather than guessing.

---

## Diagnostic Framework

```
DETECT (Identify the problem signal)
    |
    v
ISOLATE (Narrow down where in the funnel the problem occurs)
    |
    v
ANALYZE (Determine root cause)
    |
    v
HYPOTHESIZE (Form testable theory)
    |
    v
FIX (Apply targeted solution)
    |
    v
VERIFY (Confirm the fix worked)
```

---

## Step 1: Detect -- What Changed?

### Initial Triage Questions

| Question | Answer | Implication |
|---|---|---|
| When did performance change? | `{{DATE/TIME}}` | Narrows cause to a specific event |
| Was it gradual or sudden? | `{{GRADUAL/SUDDEN}}` | Gradual = fatigue/market. Sudden = change/error |
| Which metric changed first? | `{{METRIC}}` | Points to the funnel stage where the issue originates |
| Which campaigns are affected? | `{{ALL/SPECIFIC}}` | All = platform/market. Specific = campaign-level |
| Were any changes made? | `{{YES/NO}}` | If yes, likely cause is the change |
| Any external events? | `{{YES/NO}}` | Holidays, competitor moves, platform updates |

### Signal Classification

| Signal | Possible Category |
|---|---|
| CPA increasing | Auction, creative fatigue, audience saturation, funnel issue |
| CTR declining | Creative fatigue, audience mismatch, increased competition |
| Spend dropping | Budget exhaustion, bid too low, audience too small, ad rejection |
| Conversions declining | Tracking issue, funnel problem, landing page issue, offer fatigue |
| CPM increasing | Auction competition, seasonal demand, audience saturation |
| ROAS declining | AOV decrease, CPA increase, or both |

---

## Step 2: Isolate -- Where in the Funnel?

### Funnel Stage Diagnostic

Check each stage sequentially. The FIRST stage showing a problem is likely the root cause.

| Stage | Metric | Current | Benchmark | Status | Investigation |
|---|---|---|---|---|---|
| **Delivery** | Impressions, Spend | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Is the ad delivering? |
| **Attention** | CTR, Thumb-Stop Rate | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Is the creative capturing attention? |
| **Traffic** | CPC, LP View Rate | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Are clicks reaching the landing page? |
| **Engagement** | Bounce Rate, Time on Page | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Are visitors engaging with the page? |
| **Action** | ATC Rate, Lead Rate | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Are visitors taking the desired action? |
| **Conversion** | CVR, Purchase Rate | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Are they completing the conversion? |
| **Tracking** | Event firing, attribution | `{{}}` | `{{}}` | `{{OK/ISSUE}}` | Is tracking working correctly? |

---

## Step 3: Analyze -- Common Root Causes

### Delivery Issues (Impressions/Spend Declining)

| Possible Cause | How to Confirm | Fix |
|---|---|---|
| Budget capped | Check budget vs. spend | Increase budget |
| Bid too low | Check bid strategy, auction insights | Increase bid or switch strategy |
| Audience too small | Check audience size | Expand targeting |
| Ad disapproved | Check ad status in platform | Fix compliance issue, resubmit |
| Account issue | Check billing, policy notifications | Resolve account-level issue |
| Learning phase | Check learning status | Wait, do not make changes |
| Audience exhaustion | Check frequency (> 4.0) | Refresh creative or expand audience |

### Creative Issues (CTR Declining)

| Possible Cause | How to Confirm | Fix |
|---|---|---|
| Creative fatigue | CTR declining over time, frequency increasing | Launch new creative variations |
| Hook not working | Low thumb-stop rate (< 20%) | Test new hooks |
| Ad-audience mismatch | CTR varies by audience segment | Tailor creative to audience |
| Competitor has better creative | Check ad library for competitor ads | Improve creative quality/angle |
| Seasonal irrelevance | Content feels outdated for current season | Update seasonal messaging |

### Traffic Quality Issues (CPC Rising, LP View Rate Declining)

| Possible Cause | How to Confirm | Fix |
|---|---|---|
| Landing page slow | Test with PageSpeed Insights | Optimize page speed (target < 3s) |
| Mobile experience poor | Test on multiple devices | Fix mobile UX |
| Redirect chain | Check for multiple redirects in URL | Simplify URL path |
| UTM parameter issues | Check URL is not broken by params | Fix URL structure |
| Wrong destination URL | Click through the ad yourself | Fix destination URL |

### Funnel Issues (Conversions Declining Despite Good Traffic)

| Possible Cause | How to Confirm | Fix |
|---|---|---|
| Landing page changed | Compare current vs. previous version | Revert or fix LP |
| Offer fatigue | Conversion rate declining over time | Refresh offer or angle |
| Pricing issue | Check if prices changed | Adjust pricing or messaging |
| Checkout friction | Test checkout flow yourself | Fix friction points |
| Out of stock | Check product availability | Pause ads for OOS products |
| Form broken | Test form submission | Fix form |
| Payment processor issue | Test payment flow | Contact payment provider |
| Trust deficit | High cart abandonment rate | Add reviews, guarantees, trust badges |

### Tracking Issues (Conversions Not Matching Reality)

| Possible Cause | How to Confirm | Fix |
|---|---|---|
| Pixel removed or broken | Check Events Manager / Tag Assistant | Reinstall pixel |
| CAPI disconnected | Check CAPI event quality score | Reconnect server-side tracking |
| iOS/privacy changes | Check event match quality | Implement CAPI, use Conversions API |
| Attribution window changed | Check attribution settings | Restore correct window |
| Conversion event misconfigured | Verify event fires on correct page | Fix event setup |
| Double-counting | Check for duplicate events | Deduplicate events |
| Cross-domain tracking broken | Check multi-domain setup | Fix cross-domain tracking |

---

## Step 4: Hypothesize

### Hypothesis Template
```
OBSERVATION: {{WHAT_WE_SEE}} (e.g., CPA increased 40% over the past 7 days)
ISOLATION: The issue appears at the {{STAGE}} stage (e.g., CTR declined first)
HYPOTHESIS: The most likely cause is {{CAUSE}} because {{EVIDENCE}}.
TEST: To confirm, we will {{ACTION}} and expect to see {{EXPECTED_RESULT}}.
```

---

## Step 5: Fix -- Apply Targeted Solutions

### Fix Prioritization

| Priority | Fix Type | When |
|---|---|---|
| **P0** | Tracking broken, ads disapproved, billing failed | Fix immediately |
| **P1** | CPA > 2x target, ROAS below break-even | Fix within 24 hours |
| **P2** | Performance declining 20-50% from baseline | Fix within 48 hours |
| **P3** | Minor efficiency loss (< 20%) | Address in next optimization cycle |

### Fix Rules
- Change ONE thing at a time (isolate the variable)
- Document what you changed and when
- Set a review date (48-72 hours later)
- If the fix does not work, revert and try the next hypothesis

---

## Step 6: Verify -- Confirm the Fix

### Verification Checklist

| Check | Status |
|---|---|
| Affected metric returned to benchmark? | `{{YES/NO/IMPROVING}}` |
| No negative side effects on other metrics? | `{{YES/NO}}` |
| Fix has held for 48+ hours? | `{{YES/NO}}` |
| Root cause documented for future reference? | `{{YES/NO}}` |

---

## Quick Diagnostic Cheat Sheet

```
CPA SPIKING?
  -> Check CTR first. If CTR dropped -> creative issue
  -> If CTR fine, check CVR -> funnel issue
  -> If CVR fine, check CPM -> auction/competition issue
  -> If all fine, check tracking -> measurement issue

NO SPEND?
  -> Ad approved? -> If no, fix compliance
  -> Budget set? -> If no, set budget
  -> Audience size ok? -> If small, expand
  -> Bid competitive? -> If low, increase

ZERO CONVERSIONS?
  -> Clicks coming in? -> If no, creative/delivery issue
  -> LP loading? -> If no, page speed/URL issue
  -> Events firing? -> If no, tracking issue
  -> Conversions in analytics? -> If yes but not in platform, attribution issue
```

---

## Diagnostic Log Template

```
Date: {{DATE}}
Campaign: {{CAMPAIGN}}
Issue Detected: {{DESCRIPTION}}
Metric Affected: {{METRIC}} changed from {{BEFORE}} to {{AFTER}}
Duration: {{DAYS}} days
Funnel Stage: {{STAGE}}
Root Cause: {{CAUSE}}
Fix Applied: {{FIX}}
Fix Date: {{DATE}}
Result: {{OUTCOME}}
Learning: {{WHAT_WE_LEARNED}}
```
