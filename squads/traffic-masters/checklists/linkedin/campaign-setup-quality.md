# LinkedIn Campaign Setup Quality Gate

> Quality gate for LinkedIn campaign setup and configuration. Must pass before the campaign is launched in LinkedIn Campaign Manager.

## Section 1: Campaign Objective and Type
- [ ] Campaign objective matches the business goal: Brand Awareness, Website Visits, Engagement, Video Views, Lead Generation, Website Conversions, Job Applicants
- [ ] Campaign group is selected or created for proper organization and budget management
- [ ] Ad format is appropriate for the objective: Single Image, Carousel, Video, Message, Conversation, Text, Spotlight, Follower, Document, Event
- [ ] LinkedIn Audience Network is intentionally enabled or disabled (disabled recommended for B2B precision)
- [ ] Campaign name follows convention: [Client]_[Objective]_[Audience]_[Format]_[Date]

## Section 2: Budget and Bidding
- [ ] Daily or total budget matches the approved media plan (minimum $10/day per campaign)
- [ ] Bid strategy is selected: Maximum Delivery (recommended for most), Cost Cap, or Manual Bidding
- [ ] Manual CPC bids are set above the minimum suggested bid to ensure delivery
- [ ] Budget is sufficient for the audience size (LinkedIn CPMs are $30-80+ for B2B; plan accordingly)
- [ ] Campaign schedule (start and end dates) matches the flight plan

## Section 3: Ad Creative Configuration
- [ ] Ad creative meets LinkedIn specifications: Single Image (1200x628px), Carousel (1080x1080px per card), Video (MP4, 3s-30min)
- [ ] Introductory text is under 150 characters for optimal display (max 600; truncated at ~150 on mobile)
- [ ] Headline is under 70 characters (max 200)
- [ ] CTA button is selected from LinkedIn's options (Learn More, Sign Up, Download, Register, etc.)
- [ ] Destination URL is live, loads within 3 seconds, and is mobile-optimized
- [ ] UTM parameters are appended to all destination URLs

## Section 4: Lead Gen Forms (if applicable)
- [ ] Lead Gen Form is created with appropriate fields (minimize fields: name, email, company, job title)
- [ ] Privacy policy URL is included and links to a live page
- [ ] Thank you message and destination URL are configured post-submission
- [ ] Form pre-fill is tested to ensure LinkedIn auto-populates correctly
- [ ] CRM integration or Zapier webhook is configured for real-time lead delivery

## Section 5: Pre-Launch Validation
- [ ] All ads have been previewed in Campaign Manager across desktop and mobile
- [ ] Conversion tracking (LinkedIn Insight Tag) is verified on the landing page
- [ ] Campaign has been reviewed by a second team member before activation
- [ ] A/B test structure is documented if testing variations
- [ ] Campaign complies with LinkedIn's Advertising Policies

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: Missing Insight Tag or Lead Gen Form misconfiguration are hard blocks; must be resolved before launch
