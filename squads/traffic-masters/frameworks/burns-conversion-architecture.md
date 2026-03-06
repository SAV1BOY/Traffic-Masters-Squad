# Conversion Architecture - 24-Point CRO Checklist

> **Author**: Ralph Burns
> **Domain**: Conversion Rate Optimization & Funnel Design
> **Used by agents**: cro-specialist, funnel-architect, landing-page-designer
> **Checklists**: 24-point-cro-checklist, funnel-audit-scorecard

## Overview

Conversion Architecture is Ralph Burns' 24-point CRO checklist covering the entire funnel -- pre-click, on-page, and post-conversion. Every point has a pass/fail criteria. Most advertisers audit their ads but never systematically audit what happens after the click. This framework ensures that every stage of the conversion journey is optimized, not just the ad.

## When to Use

- Launching a new funnel or landing page (run the checklist before going live)
- Diagnosing high CPC but low conversion rate (the funnel is leaking)
- Quarterly funnel audits for active campaigns
- Onboarding a new client (baseline CRO assessment)
- After significant changes to offers, pricing, or messaging

## The Framework

### Section A: Pre-Click (Points 1-8)

These points ensure that the transition from ad to page is seamless and that technical foundations are solid.

**1. Ad-to-Page Congruence**
The headline, imagery, and offer on the landing page must directly match the ad that drove the click. If the ad promises "Free Guide to Facebook Ads," the page headline must reference that exact guide.
Pass: First-glance match between ad and page. Fail: Visitor has to search for what the ad promised.

**2. Page Load Speed**
Page must load in under 3 seconds on mobile. Every additional second loses approximately 10% of visitors.
Pass: Under 3 seconds (Google PageSpeed score 70+). Fail: Over 3 seconds.

**3. Mobile Optimization**
Page must be fully responsive with tap-friendly buttons, readable text without zooming, and no horizontal scrolling.
Pass: Clean mobile experience on 3 device sizes. Fail: Any element breaks on mobile.

**4. URL and Tracking Parameters**
UTM parameters, pixel fires, and conversion events must be configured and verified before launch.
Pass: Test conversion fires correctly in platform. Fail: Any tracking gap.

**5. SSL Certificate**
Page must load on HTTPS. Browsers flag non-secure pages and visitors bounce.
Pass: HTTPS with valid certificate. Fail: HTTP or certificate error.

**6. No Competing Navigation**
Landing page should have no top navigation, sidebar links, or footer links that lead away from the conversion action.
Pass: Single path to conversion. Fail: Any exit link other than the CTA.

**7. Messaging Alignment Across Funnel Steps**
If the funnel has multiple steps (ad, landing page, checkout, thank you), messaging must be consistent throughout.
Pass: Consistent promise and language across all steps. Fail: Messaging contradicts or confuses between steps.

**8. Audience-Specific Pages**
Different audience segments or traffic temperatures should land on different pages, not a generic one-size-fits-all page.
Pass: At least warm/cold variants exist. Fail: One page for all traffic.

### Section B: On-Page (Points 9-18)

These points optimize the page itself for maximum conversion.

**9. Headline Clarity**
The headline must communicate what the visitor gets and why it matters in under 5 seconds of reading.
Pass: A stranger can explain the offer after reading only the headline. Fail: Headline is vague or clever without clarity.

**10. Proof Stack**
Multiple forms of proof visible without scrolling: testimonials, logos, numbers, case studies, media mentions.
Pass: 3+ forms of proof above the fold. Fail: No proof or proof buried below the fold.

**11. Clear CTA**
One primary call-to-action that tells the visitor exactly what to do. Button text should describe the action and outcome.
Pass: "Get My Free Guide" or "Start My Trial." Fail: "Submit" or "Learn More."

**12. CTA Visibility**
The primary CTA must be visible above the fold and repeated at logical intervals throughout the page.
Pass: CTA above fold and at least 2 more times on page. Fail: CTA only at the bottom.

**13. Form Friction**
Forms should ask for the minimum information needed. Every additional field reduces conversion rate by approximately 5-10%.
Pass: Lead gen forms have 3 or fewer fields. Fail: Asking for phone, address, or company on a lead magnet form.

**14. Trust Signals**
Security badges, privacy statements, money-back guarantees, and recognized brand logos reduce perceived risk.
Pass: Trust signals near the CTA and form. Fail: No trust signals or trust signals far from conversion point.

**15. Visual Hierarchy**
The eye should flow naturally from headline to proof to CTA. Use size, color, contrast, and whitespace to guide attention.
Pass: Clear visual path to conversion. Fail: Cluttered layout with competing visual elements.

**16. Benefit-Driven Copy**
Copy should lead with benefits (what the customer gets) not features (what the product does).
Pass: Every bullet point answers "so what?" from the customer's perspective. Fail: Feature lists without benefit framing.

**17. Objection Handling**
The page must address the top 3-5 objections the audience has about taking action (price, time, trust, complexity, relevance).
Pass: FAQ section or in-line objection handling for top objections. Fail: Objections unaddressed.

**18. Social Proof Specificity**
Testimonials must be specific and credible -- names, photos, specific results, before/after context.
Pass: "Sarah M. generated 47 leads in her first week." Fail: "Great product! -- S.M."

### Section C: Post-Conversion (Points 19-24)

These points optimize what happens after the visitor converts.

**19. Thank You Page Optimization**
The thank you page is not a dead end. It should confirm the action, set expectations, and present the next step (share, upsell, book a call).
Pass: Thank you page includes next-step CTA. Fail: Generic "Thanks, check your email" with no next action.

**20. Confirmation Email**
Immediate automated email confirming the conversion, delivering the promised asset, and reinforcing the relationship.
Pass: Email sends within 2 minutes with clear subject line and delivery. Fail: Delayed or missing confirmation.

**21. Welcome/Nurture Sequence**
Automated email sequence following conversion: welcome, value delivery, story/proof, soft offer progression.
Pass: 5+ email sequence mapped to buyer journey. Fail: Single confirmation email with no follow-up.

**22. Onboarding Experience**
For product/service purchases, a structured onboarding process that gets the customer to "first value" as quickly as possible.
Pass: Clear onboarding steps with progress tracking. Fail: Customer left to figure it out alone.

**23. Retargeting Alignment**
Post-conversion retargeting must reflect the new relationship stage. Do not show the same lead magnet ad to someone who already downloaded it.
Pass: Exclusion audiences and next-step retargeting configured. Fail: Converted users seeing the same ads.

**24. Feedback Loop**
Mechanism to collect post-conversion feedback and route it back to marketing for creative and offer improvement.
Pass: Survey, NPS, or feedback mechanism within 7 days of conversion. Fail: No post-conversion feedback collection.

## Key Concepts

- **The funnel is a system**: Optimizing one section while ignoring others creates bottlenecks
- **Pass/fail clarity**: Every point has a binary assessment -- no ambiguity
- **Mobile-first**: Over 70% of social traffic is mobile. Design for mobile, verify on desktop
- **Congruence is king**: The experience from ad to page to email must feel like one continuous conversation
- **Post-conversion is undervalued**: The thank you page and email sequence are high-intent touchpoints most marketers ignore

## Decision Rules

- IF more than 3 points in Section A fail THEN do not launch until fixed (pre-click issues waste ad spend)
- IF conversion rate is below benchmark but traffic metrics are strong THEN focus on Section B
- IF customer LTV is low or refunds are high THEN focus on Section C
- IF a page scores below 18/24 THEN prioritize fixes before increasing ad spend
- IF all 24 points pass but conversion is still low THEN the offer itself needs work (see pittman-offer-formula.md)

## Common Mistakes

- Auditing ads without auditing the landing page -- the page converts, not the ad
- Ignoring mobile experience while running mobile-heavy traffic platforms
- Using "Submit" as CTA text -- the most expensive single word in marketing
- Skipping the thank you page -- leaving money and relationship-building on the table
- Setting and forgetting post-conversion email sequences -- they need regular updates
- Not running the 24-point checklist before launch -- fixing live pages costs more than preventing issues

## Integration

- Pre-click section connects to ad creation in **pittman-ad-grid-7-steps.md**
- On-page section connects to offer structure in **pittman-offer-formula.md**
- Post-conversion connects to operations in **burns-caamp.md** System 3
- CRO is Pillar 3 of **burns-conversion-engine.md**
- All 24 points are assessed during the **burns-sgp-30-60-90.md** 111-point audit
- Performance metrics connect to **burns-mpi.md**

## Output

- Completed 24-point scorecard with pass/fail for each point
- Prioritized fix list ranked by conversion impact
- Before/after documentation for each fix implemented
- Quarterly re-audit schedule to maintain standards
