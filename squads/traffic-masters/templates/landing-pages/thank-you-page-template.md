# Thank You Page Template

> **Type**: Template
> **Category**: landing-pages
> **Used by tasks**: funnel-build, post-conversion-optimization, upsell-setup
> **Filled by agents**: copywriter-agent, funnel-builder-agent, tracking-agent

## Purpose
Structures the post-conversion thank you page to confirm the action, set expectations, present an additional offer or upsell, encourage social sharing, and ensure all tracking pixels fire correctly.

## Template

### Page Metadata
**Page URL**: [/thank-you or /confirmation]
**Conversion type**: [lead / registration / purchase / application]
**Traffic arrives from**: [form submission redirect from previous page]
**Upsell enabled**: [yes / no]
**Access restriction**: [only accessible via redirect, not direct URL]

### Section 1: Confirmation
**Headline**: "[Confirmation message: 'You're In!' / 'Thank You!' / 'Order Confirmed!']"
**Subheadline**: "[Specific confirmation: 'Your [resource/order/registration] is confirmed.']"
**Confirmation details**:
- For leads: "Check your email at [dynamic email] for your [resource name]."
- For registrations: "You're registered for [event] on [date] at [time]."
- For purchases: "Order #[dynamic order number] has been received."
**Visual**: [Checkmark icon, celebration graphic, or product preview image]

### Section 2: Next Steps
**Step 1**: "[Immediate action: 'Check your inbox (and spam folder) for the confirmation email.']"
**Step 2**: "[Preparation: 'While you wait, here's how to get the most out of [resource/product]...']"
**Step 3**: "[Community: 'Join our [Facebook group / Slack / community] for [benefit].']"
**Format**: Numbered list with icons for clarity
**Notes**: Reduce buyer's remorse by giving them something productive to do immediately.

### Section 3: Expectation Setting
**Delivery timeline**: "[Your [resource] will arrive in your inbox within [X] minutes.]"
**What happens next**: "[Our team will review your application within [X] business days.]"
**Support contact**: "[Questions? Email [support@email.com] or call [number].]"
**Calendar**: "[Add this event to your calendar: [calendar link]]" (for registrations)
**Notes**: Clarity here prevents support tickets and no-shows.

### Section 4: Additional Offer / Upsell
**Offer type**: [one-time offer / tripwire / upsell / cross-sell / next step in funnel]
**Headline**: "[Exclusive offer: 'Wait! Here's a special one-time offer just for you.']"
**Offer description**: "[Describe what they get and why it's valuable]"
**Price**: [Discounted price with original price strikethrough]
**Urgency**: "[This offer expires in [countdown timer] and won't be available again.]"
**CTA button**: [Add This to My Order / Upgrade Now / Get Instant Access]
**Decline link**: "[No thanks, I'll pass on this exclusive deal.]"
**Notes**: Upsell should be complementary to what they just got. Do not distract from the confirmation.

### Section 5: Social Sharing
**Headline**: "[Share with a friend who needs this]"
**Share buttons**: [Facebook / Twitter / LinkedIn / Email / Copy Link]
**Pre-written share text**: "[I just signed up for [resource/event]. Check it out: [URL]]"
**Referral incentive**: "[Share with 3 friends and get [bonus item/discount/upgrade].]"
**Notes**: People are most enthusiastic right after conversion. Capture that energy.

### Section 6: Tracking Pixel Fires
**Purpose**: This page is where conversion events must fire for accurate attribution.

**Meta Pixel**:
- Event: [Lead / Purchase / CompleteRegistration / Schedule]
- Parameters: { value: [X], currency: 'USD', content_name: '[offer name]' }

**Google Ads**:
- Conversion action: [conversion label]
- Value: [dynamic or static]

**GA4**:
- Event: [generate_lead / purchase / sign_up]
- Parameters: { method: '[form/checkout]', value: [X] }

**TikTok Pixel**:
- Event: [CompleteRegistration / CompletePayment / SubmitForm]

**CAPI**:
- Server-side event fires: [yes / no]
- Dedup event_id: [matches browser pixel event_id]

**Notes**: Test all pixel fires in debug mode before launching traffic. Double-check that events fire once (not on page refresh).

### Page Design Guidelines
**Layout**: Clean, celebratory, focused
**Hero area**: Confirmation message with visual feedback (checkmark, confetti)
**No navigation**: Keep the user on this page; remove menu links
**Mobile**: All elements must be readable and tappable on mobile
**Page speed**: Fast load required; delayed pixel fires cause lost attribution
**Redirect protection**: Return 404 or redirect to home if accessed directly

### Post-Page Automation
**Email sequence trigger**: [trigger email automation on conversion event]
**CRM update**: [update lead status or deal stage in CRM]
**Slack notification**: [notify sales team for high-intent leads]
**Retargeting audience**: [add to purchaser/lead exclusion list]

## Usage Notes
- Test the full funnel end-to-end before launching traffic.
- Verify pixel fires using browser developer tools and platform debuggers.
- A/B test the upsell offer; even a 10% take rate adds significant revenue.

## Example
After a webinar registration: confirmation with calendar link, next steps to prepare, one-time offer for a related mini-course at 50% off with 15-minute countdown, social sharing buttons, and Meta Lead event firing.

## Related
- leadgen-landing-template.md
- webinar-registration-template.md
- event-map-template.md
- qa-checklist-template.md
