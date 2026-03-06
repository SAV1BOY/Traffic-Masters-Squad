# Form and Lead Capture Optimization Quality Gate

> Quality gate for form design and lead capture optimization. Must pass before forms are deployed on landing pages or lead gen campaigns.

## Section 1: Form Design and Layout
- [ ] Form is visually prominent on the page (above the fold or easily accessible via anchor link)
- [ ] Number of form fields is minimized: 3-5 fields for top-of-funnel, 5-8 for bottom-of-funnel (each added field reduces conversions)
- [ ] Field labels are clear and positioned above the input field (not inside as placeholder-only text)
- [ ] Required fields are clearly marked (asterisk or explicit label)
- [ ] Form width is appropriate: single-column layout for mobile, two-column for desktop if space permits
- [ ] Submit button text is specific and action-oriented ("Get My Free Demo", not "Submit" or "Send")

## Section 2: Field Selection and Optimization
- [ ] Only essential fields are included (justify each field: is it needed for qualification or follow-up?)
- [ ] Email field uses type="email" for mobile keyboard optimization
- [ ] Phone field uses type="tel" for numeric keyboard on mobile
- [ ] Dropdown menus are used instead of free-text fields where options are limited and predefined
- [ ] Multi-step forms are used for complex lead capture (break into 2-3 steps with progress indicator)
- [ ] Hidden fields capture UTM parameters, landing page URL, and timestamp for attribution

## Section 3: Validation and Error Handling
- [ ] Real-time inline validation is implemented (errors show next to the field, not in a summary at top)
- [ ] Error messages are specific and helpful ("Please enter a valid email address", not "Invalid input")
- [ ] Form validates on the client side before server submission (prevents unnecessary round trips)
- [ ] Server-side validation is also implemented as a fallback (client-side only is insufficient)
- [ ] Successfully submitted fields retain their values if the form needs to be corrected

## Section 4: Submission and Post-Conversion
- [ ] Form submission redirects to a dedicated thank-you page (not just an inline message) for conversion tracking
- [ ] Thank-you page fires all conversion pixels (Meta, Google, TikTok, LinkedIn, GA4)
- [ ] Auto-responder email is sent within 5 minutes of form submission
- [ ] Lead data is delivered to the CRM or sales team in real-time (via webhook, Zapier, or direct integration)
- [ ] Double-opt-in is implemented where required by regulation (GDPR, LGPD for email marketing consent)

## Section 5: Anti-Spam and Data Quality
- [ ] CAPTCHA or honeypot field is implemented to prevent bot submissions
- [ ] Email validation rejects obviously fake addresses (test@test.com, asdf@asdf.com)
- [ ] Phone number validation ensures correct format for the target country
- [ ] Duplicate submission prevention is in place (disable button after click, or server-side dedup)
- [ ] Form submission data is reviewed weekly for spam patterns and data quality issues

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: cro-specialist-agent + tracking-specialist-agent
- **Escalation**: Missing conversion tracking on thank-you page or broken CRM integration are hard blocks; form must not receive paid traffic until resolved
