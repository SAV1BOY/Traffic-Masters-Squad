# Webinar Registration Page Template

> **Type**: Template
> **Category**: landing-pages
> **Used by tasks**: webinar-funnel-build, event-promotion, lead-generation
> **Filled by agents**: copywriter-agent, funnel-builder-agent

## Purpose
Structures a webinar or live event registration page that maximizes sign-ups by clearly communicating the event value, speaker credibility, and creating urgency around limited spots or timing.

## Template

### Page Metadata
**Page URL**: [slug]
**Webinar platform**: [Zoom / GoToWebinar / WebinarJam / Demio / custom]
**Event type**: [live / evergreen / hybrid]
**Target registration rate**: [percentage from traffic]
**Target show-up rate**: [percentage from registrants]

### Section 1: Headline
**Event type label**: [FREE LIVE TRAINING / MASTERCLASS / WORKSHOP / WEBINAR]
**Main headline**: "[Outcome-focused: 'How to [achieve result] without [common pain]']"
**Subheadline**: "[Specific detail: 'A [duration] live training for [audience] who want [desire]']"
**Date and time**: [Day, Month Date, Year at HH:MM AM/PM Timezone]
**Duration**: [45 min / 60 min / 90 min]
**CTA button**: [Save My Spot / Register Now / Claim My Seat]
**Notes**: Headline must promise a specific, desirable outcome achievable through attending.

### Section 2: What You'll Learn (3 Bullets)
**Section headline**: "In this [duration] session, you'll discover:"
**Bullet 1**: "[Specific takeaway - start with action verb: 'The exact framework for...']"
**Bullet 2**: "[Specific takeaway - address a pain: 'Why most [audience] fail at [thing] and the simple fix']"
**Bullet 3**: "[Specific takeaway - create curiosity: 'The #1 strategy [authority figures] use to [result]']"
**Bonus bullet (optional)**: "[Extra incentive: 'Plus, a live Q&A where you can get personalized feedback']"
**Notes**: Each bullet should be a standalone reason to attend. Mix outcomes, pain relief, and curiosity.

### Section 3: Speaker Bio
**Speaker photo**: [Professional but approachable headshot]
**Speaker name**: [Full name]
**Speaker title**: [Role, Company]
**Bio paragraph**: "[2-3 sentences covering relevant credentials, results achieved, and why they're qualified to teach this topic. Include specific numbers.]"
**Key credentials**:
- [Credential or achievement 1]
- [Credential or achievement 2]
- [Credential or achievement 3]
**Notes**: Bio should establish authority quickly. Lead with results, not resume.

### Section 4: Social Proof
**Proof type A - Attendee count**: "[X]+ people have attended our trainings"
**Proof type B - Testimonials**:
- "[Quote about value of attending] - [Name, Title]"
- "[Quote about results from applying what they learned] - [Name, Title]"
**Proof type C - Logos**: [Companies whose employees have attended]
**Proof type D - Rating**: "[Average rating] from [X] past attendees"
**Notes**: Focus on proof that this specific event (or similar past events) delivered value.

### Section 5: Registration Form
**Form headline**: "[Register for free / Save your spot]"
**Form fields**:
- First name: [required]
- Email address: [required]
- [Optional: phone number for SMS reminders]
- [Optional: company name for B2B qualification]
**Submit button text**: [Save My Spot / Register Now / Count Me In]
**Privacy note**: "Your information is safe. We will send you event details and reminders only."
**Calendar add**: [Offer .ics download or Google Calendar link after registration]

### Section 6: Urgency Element
**Urgency type**: [limited spots / live-only / bonus for registrants / countdown timer]
**Urgency text**: "[Only [X] spots available / Register before [date] to receive [bonus] / Live attendees get exclusive [resource]]"
**Countdown timer**: [yes / no - counts down to event start or registration deadline]
**Notes**: Urgency must be genuine. Fake scarcity damages trust.

### Reminder Sequence (Post-Registration)
**Immediate**: Confirmation email with event details and calendar link
**24 hours before**: Reminder email with prep tips or teaser content
**1 hour before**: "Starting soon" email with join link
**15 minutes before**: SMS reminder (if phone collected)
**Post-event**: Replay link (if available) + offer follow-up

### Page Design Guidelines
**Layout**: Single column, no navigation menu
**Above the fold**: Headline, date/time, CTA button visible without scrolling
**Color scheme**: Match brand, high-contrast CTA button
**Mobile optimization**: Form must be easy to complete on mobile
**Page speed**: Under 3 seconds load time
**No exit links**: Remove all navigation; only action is registration

### Tracking Requirements
**Pixel fires**: PageView on load, Lead on registration
**GA4 events**: page_view, form_start, registration_complete
**UTM parameters**: Captured in hidden form fields
**Thank you page**: Redirect to confirmation page with next steps

## Usage Notes
- Test headline variations first; they have the highest impact on registration rate.
- Show-up rate matters more than registration rate. Invest in the reminder sequence.
- For evergreen webinars, use "next available session" instead of fixed dates.

## Example
A SaaS founder hosting a live training: "How to Reduce Customer Churn by 40% in 90 Days." 60-minute session, 3 learning bullets, speaker bio with customer retention results, countdown timer, name + email form.

## Related
- leadgen-landing-template.md
- thank-you-page-template.md
- campaign-brief.md
