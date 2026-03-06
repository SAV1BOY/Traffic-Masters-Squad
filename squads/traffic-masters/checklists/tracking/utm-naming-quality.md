# UTM Parameter and Naming Convention Quality Gate

> Quality gate for UTM parameter strategy and naming conventions. Must pass before campaign URLs are distributed to any advertising platform.

## Section 1: UTM Strategy Documentation
- [ ] A master UTM naming convention document exists and is accessible to all team members
- [ ] UTM taxonomy covers all five parameters: utm_source, utm_medium, utm_campaign, utm_term, utm_content
- [ ] Naming convention uses lowercase only (no mixed case; analytics tools are case-sensitive)
- [ ] Word separators are standardized: hyphens (-) or underscores (_) used consistently (never mixed)
- [ ] The UTM document includes examples for each active advertising platform

## Section 2: utm_source and utm_medium Standards
- [ ] utm_source identifies the traffic source: facebook, google, tiktok, linkedin, email, direct (not brand names like "Meta")
- [ ] utm_medium identifies the marketing medium: cpc, cpm, paid-social, organic-social, email, display, video, affiliate
- [ ] utm_medium values align with GA4 default channel grouping definitions to ensure correct channel attribution
- [ ] Source/medium combinations are documented for all active channels: facebook/paid-social, google/cpc, tiktok/paid-social
- [ ] No custom utm_medium values break GA4 channel grouping (e.g., "paidsocial" would be unassigned; use "paid-social")

## Section 3: utm_campaign Naming
- [ ] utm_campaign follows a structured format: [client]_[objective]_[audience]_[date] or similar documented pattern
- [ ] Campaign names are descriptive enough to identify the initiative without cross-referencing
- [ ] Date formats are standardized (YYYY-MM or YYYYQ1 format recommended)
- [ ] Promotional campaigns include the promotion name (e.g., blackfriday2026, spring-sale)
- [ ] A/B test campaigns include a variant identifier in the campaign name

## Section 4: utm_term and utm_content Standards
- [ ] utm_term is used for keyword-level tracking in paid search campaigns
- [ ] utm_content differentiates ad creatives or content variants within the same campaign
- [ ] utm_content follows a structured format: [format]_[concept]_[variant] (e.g., video_testimonial_v2)
- [ ] Dynamic UTM parameters are used where supported ({campaign_name}, {adset_name}, {ad_name} in Meta; {campaignid}, {adgroupid} in Google)
- [ ] Dynamic parameters are tested to confirm they resolve correctly (not passing literal {placeholders})

## Section 5: Quality Assurance and Governance
- [ ] A UTM builder tool or spreadsheet is used to generate URLs (preventing manual typos)
- [ ] All generated URLs are tested before deployment (click-through confirms correct landing page and UTM pass-through)
- [ ] UTM parameters do not break the landing page functionality (no encoding issues with special characters)
- [ ] Redirect chains do not strip UTM parameters (verified with redirect checker)
- [ ] Regular UTM audits are scheduled (monthly review of GA4 source/medium report for anomalies or inconsistencies)
- [ ] Team members are trained on the UTM naming convention and use the approved builder tool

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: analytics-agent + media-buyer-agent
- **Escalation**: Broken UTM pass-through or inconsistent naming that corrupts GA4 channel grouping must be fixed before campaign URLs go live
