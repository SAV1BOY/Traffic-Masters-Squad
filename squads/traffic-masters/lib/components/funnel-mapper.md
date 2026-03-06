# Funnel Mapper Component

## Purpose
Reusable funnel mapping framework for visualizing, analyzing, and optimizing the customer journey from first ad impression through conversion and beyond.

---

## Standard Funnel Stages

### Full-Funnel Model

```
AWARENESS (Top of Funnel - TOFU)
    |
    v  [Ad Impression -> Click]
INTEREST (Upper Mid-Funnel)
    |
    v  [Landing Page View -> Engagement]
CONSIDERATION (Lower Mid-Funnel - MOFU)
    |
    v  [Lead Capture / Add to Cart]
INTENT (Bottom of Funnel - BOFU)
    |
    v  [Initiate Checkout / Request Demo]
DECISION
    |
    v  [Purchase / Conversion]
RETENTION (Post-Conversion)
    |
    v  [Repeat Purchase / Upsell / Referral]
```

---

## Funnel Stage Definitions

| Stage | User State | Key Events | Metrics | Campaign Type |
|---|---|---|---|---|
| **Awareness** | Does not know the brand | Impression, Video View, Reach | CPM, Reach, Frequency, Thumb-Stop Rate | Prospecting broad, Video views |
| **Interest** | Aware, exploring | Click, LP View, Content View | CPC, CTR, LP View Rate, Bounce Rate | Prospecting targeted, Content |
| **Consideration** | Evaluating options | Add to Cart, Lead Form, Sign Up | CPL, ATC Rate, Cost per ATC | Retargeting warm, Lead gen |
| **Intent** | Ready to act | Initiate Checkout, Book Call, Request Quote | IC Rate, Cost per IC | Retargeting hot, Urgency |
| **Decision** | Converting | Purchase, Form Submit, Demo Booked | CPA, CVR, ROAS, Revenue | BOFU retargeting, Offers |
| **Retention** | Existing customer | Repeat Purchase, Upsell, Review | Repeat Rate, LTV, CAC Payback | CRM, Email, Loyalty ads |

---

## Funnel Mapping Template

### Step 1: Map the Journey

```
Stage 1: {{AWARENESS_TOUCHPOINT}}
  Platform: {{PLATFORM}}
  Ad Type: {{AD_TYPE}}
  Content: {{WHAT_USER_SEES}}
  Action: {{WHAT_USER_DOES}}
  Metric: {{KEY_METRIC}}
  Target: {{TARGET_VALUE}}
    |
    v
Stage 2: {{INTEREST_TOUCHPOINT}}
  Platform: {{PLATFORM}}
  Content: {{LANDING_PAGE / VIDEO / CONTENT}}
  Action: {{WHAT_USER_DOES}}
  Metric: {{KEY_METRIC}}
  Target: {{TARGET_VALUE}}
    |
    v
Stage 3: {{CONSIDERATION_TOUCHPOINT}}
  Platform: {{PLATFORM}}
  Content: {{RETARGETING_AD / EMAIL / OFFER}}
  Action: {{WHAT_USER_DOES}}
  Metric: {{KEY_METRIC}}
  Target: {{TARGET_VALUE}}
    |
    v
Stage 4: {{CONVERSION_TOUCHPOINT}}
  Platform: {{PLATFORM / WEBSITE}}
  Content: {{CHECKOUT / FORM / BOOKING}}
  Action: {{PURCHASE / SUBMIT / BOOK}}
  Metric: {{CPA / ROAS}}
  Target: {{TARGET_VALUE}}
```

### Step 2: Calculate Stage Rates

| From Stage | To Stage | Volume In | Volume Out | Conversion Rate | Cost Per Stage | Benchmark |
|---|---|---|---|---|---|---|
| Impression | Click | `{{IMPRESSIONS}}` | `{{CLICKS}}` | `{{CTR}}`% | $`{{CPC}}` | `{{}}`% |
| Click | LP View | `{{CLICKS}}` | `{{LP_VIEWS}}` | `{{LP_RATE}}`% | $`{{CPLPV}}` | `{{}}`% |
| LP View | Lead/ATC | `{{LP_VIEWS}}` | `{{LEADS_ATC}}` | `{{RATE}}`% | $`{{CPL}}` | `{{}}`% |
| Lead/ATC | Checkout | `{{LEADS_ATC}}` | `{{CHECKOUTS}}` | `{{RATE}}`% | $`{{CPIC}}` | `{{}}`% |
| Checkout | Purchase | `{{CHECKOUTS}}` | `{{PURCHASES}}` | `{{RATE}}`% | $`{{CPA}}` | `{{}}`% |

### Step 3: Identify Drop-Off Points

| Drop-Off Point | Rate | Healthy Range | Status | Likely Cause | Fix |
|---|---|---|---|---|---|
| Click to LP View | `{{}}`% | 70-90% | `{{OK/WARNING/CRITICAL}}` | `{{}}` | `{{}}` |
| LP View to Lead/ATC | `{{}}`% | 5-20% | `{{}}` | `{{}}` | `{{}}` |
| Lead/ATC to Checkout | `{{}}`% | 40-70% | `{{}}` | `{{}}` | `{{}}` |
| Checkout to Purchase | `{{}}`% | 50-80% | `{{}}` | `{{}}` | `{{}}` |

---

## Common Funnel Types

### Direct-to-Consumer (DTC) E-commerce Funnel

```
Ad (TOFU) -> Product Page -> Add to Cart -> Checkout -> Purchase
    |                                                      |
    +---------- Retargeting (Cart Abandon) -------<--------+
    |                                                      |
    +---------- Email Follow-up -------<-------------------+
```

**Key Metrics:** CTR, LP View Rate, ATC Rate, Checkout Rate, CVR, AOV, ROAS

### Lead Generation Funnel

```
Ad (TOFU) -> Landing Page -> Lead Form -> Thank You Page -> Sales Follow-Up -> Close
    |                                                                          |
    +---------- Retargeting (Visited, No Submit) ------<-----------------------+
    |                                                                          |
    +---------- Email Nurture Sequence ------<---------------------------------+
```

**Key Metrics:** CTR, LP View Rate, Form Submit Rate, CPL, Lead-to-Close Rate, CAC

### Webinar / Event Funnel

```
Ad -> Registration Page -> Confirmation -> Reminder Sequence -> Live Event -> Offer Page -> Purchase
    |                                                                                        |
    +---------- Retargeting (Registered, No Show) --------<---------------------------------+
    |                                                                                        |
    +---------- Replay Sequence --------<----------------------------------------------------+
```

**Key Metrics:** Cost Per Registration, Show-Up Rate, Offer Conversion Rate, Revenue Per Registrant

### SaaS Free Trial Funnel

```
Ad -> Landing Page -> Sign Up -> Onboarding -> Active Use -> Trial Expiry -> Paid Conversion
    |                                                                             |
    +---------- Retargeting (Visited, No Sign-Up) --------<-----------------------+
    |                                                                             |
    +---------- In-App Messaging / Email Nurture --------<------------------------+
```

**Key Metrics:** Cost Per Trial, Trial-to-Paid Rate, Time-to-Conversion, CAC, LTV:CAC

### Content / Value-First Funnel

```
Ad (Content) -> Blog/Video/Guide -> Pixel + Engage -> Retargeting Ad (Offer) -> Conversion
    |                                                                              |
    +---------- Retargeting (Consumed Content) --------<---------------------------+
```

**Key Metrics:** Cost Per Content View, Engagement Rate, Retargeting CVR, CPA

---

## Funnel Health Diagnostic

### Quick Health Check

| Signal | Healthy | Warning | Critical |
|---|---|---|---|
| CTR (Feed ads) | > 1.0% | 0.5-1.0% | < 0.5% |
| LP View Rate | > 80% | 60-80% | < 60% |
| Bounce Rate | < 40% | 40-60% | > 60% |
| ATC / Lead Rate | > 8% | 3-8% | < 3% |
| Checkout Init Rate | > 50% | 30-50% | < 30% |
| Purchase CVR | > 60% | 40-60% | < 40% |

### Diagnostic Decision Tree

```
High impressions, low clicks? -> Creative problem (hook, visual, copy)
High clicks, low LP views?    -> Page load speed or mobile UX issue
High LP views, low leads/ATC? -> Landing page relevance, offer, or trust issue
High ATC, low checkout?       -> Shipping, pricing, or payment friction
High checkout, low purchase?   -> Checkout UX, payment failures, trust badges
```

---

## Funnel Optimization Priorities

| Priority | Stage | Optimization | Expected Impact |
|---|---|---|---|
| 1 | Biggest drop-off | Fix the stage with the lowest conversion rate vs. benchmark | Highest |
| 2 | Bottom of funnel | Optimize checkout/conversion flow (closest to revenue) | High |
| 3 | Top of funnel | Improve creative/targeting for better quality traffic | Medium |
| 4 | Mid-funnel | Enhance retargeting sequences and nurture | Medium |
| 5 | Post-conversion | Build retention loops for LTV | Long-term |

---

## Multi-Touch Funnel Map

For complex journeys with multiple touchpoints:

```
Touchpoint 1: {{PLATFORM}} - {{AD_TYPE}} -> {{ACTION}} ({{METRIC}})
    |
    v  [{{DAYS_BETWEEN}}]
Touchpoint 2: {{PLATFORM}} - {{AD_TYPE}} -> {{ACTION}} ({{METRIC}})
    |
    v  [{{DAYS_BETWEEN}}]
Touchpoint 3: {{PLATFORM}} - {{AD_TYPE}} -> {{ACTION}} ({{METRIC}})
    |
    v  [{{DAYS_BETWEEN}}]
CONVERSION: {{CONVERSION_EVENT}}

Average Touchpoints to Convert: {{NUMBER}}
Average Days to Convert: {{NUMBER}}
Primary Conversion Path: {{PATH_DESCRIPTION}}
```
