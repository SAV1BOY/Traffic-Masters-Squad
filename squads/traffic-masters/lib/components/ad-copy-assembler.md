# Ad Copy Assembler Component

## Purpose
Reusable framework for assembling ad copy across formats and platforms. Provides modular building blocks (hooks, body, CTAs) that can be mixed and matched to create high-performing ad variations.

---

## Copy Architecture

Every ad follows this structure:

```
[HOOK] -> [BRIDGE] -> [BODY] -> [PROOF] -> [CTA]
```

| Block | Purpose | Length | Priority |
|---|---|---|---|
| **Hook** | Stop the scroll, capture attention | 1-2 lines | Critical -- determines if ad gets read |
| **Bridge** | Connect hook to value proposition | 1 line | Important -- maintains momentum |
| **Body** | Deliver the value proposition and key benefits | 2-5 lines | Core message |
| **Proof** | Build credibility and trust | 1-2 lines | Overcomes skepticism |
| **CTA** | Tell them exactly what to do next | 1 line | Drives action |

---

## Hook Library

### Question Hooks
```
"Are you still {{DOING_OLD_WAY}}?"
"What if you could {{DESIRED_OUTCOME}} without {{PAIN_POINT}}?"
"Why do {{AUDIENCE}} struggle with {{PROBLEM}}?"
"Did you know {{SURPRISING_FACT}}?"
"Want to know the #1 reason {{NEGATIVE_OUTCOME}}?"
"Ready to {{DESIRED_RESULT}} in {{TIMEFRAME}}?"
```

### Bold Statement Hooks
```
"{{PRODUCT}} changed the way I {{ACTIVITY}}. Here's why."
"Stop {{COMMON_MISTAKE}}. There's a better way."
"This is the most important thing about {{TOPIC}} nobody talks about."
"{{NUMBER}} people switched to {{PRODUCT}} last month. Here's why."
"I {{ACHIEVED_RESULT}} in {{TIMEFRAME}} and here's how."
"The {{INDUSTRY}} doesn't want you to know this."
```

### Statistical Hooks
```
"{{PERCENTAGE}}% of {{AUDIENCE}} make this mistake with {{TOPIC}}."
"{{NUMBER}}+ {{PEOPLE/BUSINESSES}} already {{ACHIEVED_RESULT}}."
"We tested {{NUMBER}} {{VARIABLES}} and found {{INSIGHT}}."
"In just {{TIMEFRAME}}, our customers see {{RESULT}}."
"{{STAT}} -- and that's why we built {{PRODUCT}}."
```

### Call-Out Hooks
```
"Attention {{SPECIFIC_AUDIENCE}}:"
"{{AUDIENCE}} who {{SPECIFIC_BEHAVIOR}} -- this is for you."
"If you're a {{ROLE}} who {{SITUATION}}, read this."
"To every {{AUDIENCE}} tired of {{FRUSTRATION}}:"
"This is for the {{AUDIENCE}} who {{DESCRIPTION}}."
```

### Testimonial Hooks
```
"'{{QUOTE}}' - {{NAME}}, {{TITLE}}"
"I was skeptical until {{RESULT_HAPPENED}}."
"My {{ROLE}} recommended {{PRODUCT}} and it changed everything."
"After trying {{NUMBER}} {{ALTERNATIVES}}, I finally found {{PRODUCT}}."
"{{CUSTOMER_NAME}} went from {{BEFORE}} to {{AFTER}} using {{PRODUCT}}."
```

### Controversy / Pattern Interrupt Hooks
```
"Unpopular opinion: {{CONTRARIAN_TAKE}}."
"Everything you know about {{TOPIC}} is wrong."
"I stopped {{COMMON_PRACTICE}} and here's what happened."
"{{PRODUCT}} is NOT for everyone. Here's who it's for."
"Don't {{COMMON_ACTION}} until you read this."
```

---

## Bridge Templates

```
"Here's the thing..."
"The problem is..."
"But there's good news..."
"That's exactly why we created..."
"After {{RESEARCH/TESTING}}, we discovered..."
"The truth is..."
"It doesn't have to be this way."
"What most people don't realize is..."
```

---

## Body Copy Templates

### Problem-Solution Body
```
{{PROBLEM_DESCRIPTION}}.
{{AGITATE -- WHY IT'S WORSE THAN THEY THINK}}.
{{INTRODUCE_SOLUTION}}.
{{KEY_BENEFIT_1}}.
{{KEY_BENEFIT_2}}.
{{KEY_BENEFIT_3}}.
```

### Feature-Benefit Body
```
With {{PRODUCT}}, you get:
- {{FEATURE_1}} so you can {{BENEFIT_1}}
- {{FEATURE_2}} which means {{BENEFIT_2}}
- {{FEATURE_3}} giving you {{BENEFIT_3}}
```

### Before-After Body
```
Before {{PRODUCT}}: {{PAIN_STATE}}.
After {{PRODUCT}}: {{DESIRED_STATE}}.
The difference? {{KEY_DIFFERENTIATOR}}.
```

### Story Body
```
{{CHARACTER}} was dealing with {{PROBLEM}}.
They tried {{FAILED_SOLUTIONS}}.
Then they discovered {{PRODUCT}}.
Now {{POSITIVE_OUTCOME}}.
```

### Social Proof Body
```
{{NUMBER}}+ {{CUSTOMERS}} trust {{PRODUCT}} to {{OUTCOME}}.
Rated {{RATING}} on {{PLATFORM}}.
Featured in {{PUBLICATIONS}}.
{{SPECIFIC_TESTIMONIAL}}.
```

---

## Proof Elements

### Types of Proof

| Proof Type | Example | Strength |
|---|---|---|
| **Numbers** | "10,000+ customers" | Strong |
| **Ratings** | "4.8/5 stars from 2,000+ reviews" | Strong |
| **Testimonials** | Direct quotes from customers | Very Strong |
| **Authority** | "As seen in Forbes, Inc., etc." | Strong |
| **Case Studies** | "Company X increased revenue by 40%" | Very Strong |
| **Guarantees** | "30-day money-back guarantee" | Moderate (reduces risk) |
| **Certifications** | "FDA approved", "ISO certified" | Strong for regulated industries |
| **Time in Business** | "Trusted since 2010" | Moderate |
| **Awards** | "Best {{CATEGORY}} 2025" | Moderate |
| **Specificity** | "Save exactly 4.2 hours per week" | Strong (specific > vague) |

---

## CTA Library

### Direct CTAs
```
"Shop Now"
"Get Started"
"Sign Up Free"
"Book Your Demo"
"Claim Your Offer"
"Start Your Free Trial"
"Download Now"
"Learn More"
"Get [X]% Off Today"
"Order Now"
```

### Urgency CTAs
```
"Limited time -- Shop Now"
"Offer ends {{DATE}} -- Get Yours"
"Only {{NUMBER}} left at this price"
"Don't miss out -- Sign Up Today"
"Prices go up {{DATE}} -- Lock in your rate"
```

### Low-Commitment CTAs
```
"See How It Works"
"Watch the Demo"
"Take the Quiz"
"Get Your Free Guide"
"See Pricing"
"Compare Options"
```

### Value-Reinforcing CTAs
```
"Yes, I want {{BENEFIT}}"
"Start saving today"
"Get my free {{RESOURCE}}"
"Join {{NUMBER}}+ {{PEOPLE}} who {{OUTCOME}}"
"Unlock {{BENEFIT}}"
```

---

## Platform-Specific Copy Specs

### Meta Ads (Facebook / Instagram)

| Field | Character Limit | Best Practice |
|---|---|---|
| Primary Text | 125 (before "See More") | Front-load key message in first 125 chars |
| Headline | 40 characters | Clear, benefit-driven |
| Description | 30 characters | Supporting info or urgency |
| Full Primary Text | 2,200 max | Use for long-form storytelling |

### Google Search Ads

| Field | Character Limit | Best Practice |
|---|---|---|
| Headline 1-15 | 30 chars each | Include keyword, benefit, or CTA |
| Description 1-4 | 90 chars each | Expand on value, include CTA |
| Display Path | 15 chars each (2 paths) | Keyword or category-relevant |

### TikTok Ads

| Field | Character Limit | Best Practice |
|---|---|---|
| Ad Text | 100 characters | Short, punchy, native tone |
| Display Name | 40 characters | Brand name |

### LinkedIn Ads

| Field | Character Limit | Best Practice |
|---|---|---|
| Intro Text | 150 (before truncation) | Professional tone, value-first |
| Headline | 70 characters | Clear proposition |
| Description | 100 characters | Supporting detail |

---

## Copy Assembly Worksheet

```
CAMPAIGN: {{CAMPAIGN_NAME}}
AUDIENCE: {{TARGET_AUDIENCE}} | Temperature: {{COLD/WARM/HOT}}
ANGLE: {{ANGLE}}
OFFER: {{OFFER}}
PLATFORM: {{PLATFORM}}

HOOK:
{{SELECTED_HOOK}}

BRIDGE:
{{SELECTED_BRIDGE}}

BODY:
{{ASSEMBLED_BODY}}

PROOF:
{{SELECTED_PROOF_ELEMENTS}}

CTA:
{{SELECTED_CTA}}

HEADLINE (if applicable):
{{HEADLINE}}

DESCRIPTION (if applicable):
{{DESCRIPTION}}

---
FULL AD COPY:

{{HOOK}}

{{BRIDGE}}

{{BODY}}

{{PROOF}}

{{CTA}}
---
```

---

## Variation Matrix

Create multiple ad variations by mixing components:

| Variant | Hook Type | Body Type | Proof Type | CTA Type |
|---|---|---|---|---|
| V1 | Question | Problem-Solution | Testimonial | Direct |
| V2 | Statistic | Feature-Benefit | Numbers | Urgency |
| V3 | Call-Out | Before-After | Rating | Value-Reinforcing |
| V4 | Bold Statement | Story | Authority | Low-Commitment |
| V5 | Testimonial | Social Proof | Case Study | Direct |

This generates 5 distinct ad copy variations from the same core message, ideal for A/B testing.

---

## Copy Quality Checklist

- [ ] Hook is attention-grabbing and relevant to audience
- [ ] Message is clear within the first 2 lines
- [ ] Benefits are stated, not just features
- [ ] Proof element is included
- [ ] CTA is clear and specific
- [ ] Copy matches the audience temperature (cold vs. warm vs. hot)
- [ ] Tone matches the platform (native feel)
- [ ] Character limits respected for the target platform
- [ ] No prohibited claims or policy violations
- [ ] Spelling and grammar reviewed
