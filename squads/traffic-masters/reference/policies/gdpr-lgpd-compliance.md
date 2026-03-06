# GDPR & LGPD Compliance Guide for Advertisers

> Practical compliance reference for paid traffic professionals handling data across EU (GDPR) and Brazilian (LGPD) markets.

---

## 1. Overview

| Aspect | GDPR (EU) | LGPD (Brazil) |
|--------|-----------|---------------|
| **Effective** | May 2018 | September 2020 |
| **Authority** | National DPAs (Data Protection Authorities) | ANPD (Autoridade Nacional de Protecao de Dados) |
| **Scope** | EU/EEA residents' data, regardless of where processor is located | Brazilian residents' data, regardless of where processor is located |
| **Max fine** | 4% of global annual revenue or EUR 20M (whichever is higher) | 2% of Brazilian revenue, capped at BRL 50M per violation |
| **Extraterritorial** | Yes | Yes |
| **Data breach notification** | 72 hours to DPA | "Reasonable time" to ANPD |

---

## 2. Key Concepts for Advertisers

### Personal Data
Any information relating to an identified or identifiable person:
- Names, email addresses, phone numbers
- IP addresses, device IDs, cookie IDs
- Advertising IDs (IDFA, GAID)
- Behavioral data (browsing history, purchase history)
- Location data
- Hashed emails/phone numbers (still personal data under both laws)
- Pixel/tracking data collected from website visitors

### Legal Bases for Processing (Advertising Context)

| Legal Basis | GDPR | LGPD | Advertising Use Case |
|-------------|------|------|---------------------|
| **Consent** | Yes (must be freely given, specific, informed, unambiguous) | Yes (similar requirements) | Cookie tracking, email marketing, pixel-based retargeting |
| **Legitimate interest** | Yes (requires balancing test) | Yes (similar) | First-party analytics, CRM-based audiences (with assessment) |
| **Contract performance** | Yes | Yes | Transactional emails to customers |
| **Legal obligation** | Yes | Yes | Tax/financial record-keeping |

**For advertising specifically**: Consent is the safest legal basis for tracking, retargeting, and cross-site data collection. Legitimate interest may apply for some first-party data use but requires documentation.

---

## 3. Consent Management for Advertising

### What Valid Consent Looks Like

**Must be**:
- **Freely given**: No pre-ticked boxes; no "accept or leave" for non-essential cookies
- **Specific**: Separate consent for different purposes (analytics vs. advertising vs. functional)
- **Informed**: Clear explanation of what data is collected and why
- **Unambiguous**: Requires affirmative action (click, toggle, checkbox)
- **Revocable**: User must be able to withdraw consent at any time, as easily as they gave it

**Must NOT be**:
- Bundled with terms of service acceptance
- Implied by continued browsing (cookie walls that force acceptance are challenged under GDPR)
- Obtained through dark patterns (misleading button colors/sizes, confusing language)

### Consent Management Platform (CMP) Implementation

A CMP is essential for managing user consent across advertising tags:

**Recommended CMPs**: OneTrust, Cookiebot, Usercentrics, Osano, TrustArc

**Integration with ad platforms**:
1. CMP fires BEFORE any tracking tags
2. Tags only fire after appropriate consent is obtained
3. Google Consent Mode v2: Required for Google Ads in the EU since March 2024
4. Meta: Supports Consent Mode for limited data use without full consent
5. TikTok: Evolving consent integration

### Google Consent Mode v2

Required for all advertisers using Google tags in the EU/EEA:

```javascript
// Default state - deny all until user consents
gtag('consent', 'default', {
  'ad_storage': 'denied',
  'ad_user_data': 'denied',
  'ad_personalization': 'denied',
  'analytics_storage': 'denied',
  'wait_for_update': 500
});

// After user grants consent
gtag('consent', 'update', {
  'ad_storage': 'granted',
  'ad_user_data': 'granted',
  'ad_personalization': 'granted',
  'analytics_storage': 'granted'
});
```

**Key consent signals**:
- `ad_storage`: Controls cookies for advertising (required for conversion tracking)
- `ad_user_data`: Controls sending user data to Google for advertising purposes
- `ad_personalization`: Controls whether data can be used for ad personalization (remarketing)
- `analytics_storage`: Controls analytics cookies

**Impact on advertising**: Without consent, Google uses modeled conversions (estimated data). Expect 15-40% data loss in EU campaigns compared to non-consent markets.

---

## 4. Impact on Advertising Operations

### Tracking & Pixels

| Tracking Method | GDPR Requirement | LGPD Requirement |
|----------------|------------------|-------------------|
| **Meta Pixel** | Consent required before firing | Consent required before firing |
| **Google Ads tag** | Consent Mode v2 required | Consent recommended |
| **TikTok Pixel** | Consent required before firing | Consent required before firing |
| **Server-side tracking** | Still requires consent for personal data | Still requires consent |
| **Google Analytics 4** | Consent for analytics_storage | Consent recommended |
| **Hashed email uploads** | Consent for ad_user_data sharing | Consent or legitimate interest |

### Retargeting & Remarketing

**Requirements**:
- User must have consented to advertising cookies/tracking
- Privacy policy must disclose retargeting practices
- Must honor opt-out requests promptly
- Retargeting lists must exclude users who withdrew consent
- Cross-device tracking requires additional consent
- Retention periods: Do not retarget indefinitely; 30-180 day windows recommended

**Practical impact**:
- EU retargeting audiences are typically 30-60% smaller than equivalent US audiences
- Server-side tracking helps maintain some signal but still requires consent
- Contextual targeting does not require consent (no personal data involved)

### Custom Audiences & Lookalikes

**Customer list uploads (Meta, Google, TikTok)**:
- Must have consent from each individual for their data to be shared with the ad platform
- Privacy policy must disclose this data sharing
- Data Processing Agreement (DPA) must be in place with the platform
- Hashed data is still personal data under GDPR/LGPD
- Must offer opt-out mechanism

**Website visitor audiences**:
- Based on pixel/cookie data, so subject to consent requirements
- Consent Mode helps maintain some audience building with modeled data

### Email Marketing & Lead Generation

- Opt-in required for marketing emails (double opt-in recommended under GDPR)
- Lead gen forms must include privacy policy link and consent checkbox
- Cannot pre-check marketing consent boxes
- Must process unsubscribe requests within 10 business days (GDPR); promptly (LGPD)
- Co-registration (sharing leads with partners) requires specific consent for each partner

---

## 5. Data Processing Agreements (DPAs)

You need DPAs with every ad platform and tool that processes personal data on your behalf:

### Required DPAs for Typical Ad Stack

| Service | DPA Location |
|---------|-------------|
| Meta (Facebook) | `facebook.com/legal/terms/dataprocessing` |
| Google Ads | `privacy.google.com/businesses/processorterms` |
| TikTok | Available in TikTok Business Center settings |
| LinkedIn | `linkedin.com/legal/l/dpa` |
| Google Analytics | Covered under Google DPA |
| HubSpot | `legal.hubspot.com/dpa` |
| Mailchimp | `mailchimp.com/legal/data-processing-addendum` |
| Your CRM | Check your contract |

### What a DPA Must Include
- Nature and purpose of processing
- Types of personal data processed
- Duration of processing
- Rights and obligations of both parties
- Sub-processor list and notification obligations
- Data breach notification procedures
- Data deletion/return obligations upon termination

---

## 6. Privacy Policy Requirements for Advertisers

Your website privacy policy must disclose:

- [ ] **What data is collected** (cookies, device IDs, behavioral data, form data)
- [ ] **Why it is collected** (advertising, analytics, personalization)
- [ ] **Legal basis** for each processing activity
- [ ] **Third parties** receiving data (Meta, Google, analytics providers)
- [ ] **Retention periods** for each data category
- [ ] **User rights** (access, deletion, portability, objection)
- [ ] **How to exercise rights** (contact details, process)
- [ ] **International transfers** (if data leaves EU/Brazil)
- [ ] **Cookie policy** (types of cookies, purposes, durations)
- [ ] **Automated decision-making** (if applicable, such as algorithmic ad targeting)

### LGPD-Specific Requirements
- Must appoint a DPO (Data Protection Officer / "Encarregado")
- DPO contact information must be publicly available
- Privacy policy must be available in Portuguese
- Must maintain Records of Processing Activities (ROPA)

---

## 7. Data Subject Rights & Advertising Impact

### Right to Access
- Users can request all data you hold about them
- This includes audience segments, tracking data, and ad interaction history
- Must respond within 30 days (GDPR) or 15 days (LGPD)

### Right to Deletion ("Right to Be Forgotten")
- Users can request deletion of their personal data
- Must remove from CRM, email lists, Custom Audiences, and tracking systems
- Must notify third parties (ad platforms) to delete data
- Some exceptions apply (legal obligations, legitimate interests)

### Right to Object to Processing
- Users can object to processing for direct marketing at any time
- Must stop processing immediately upon objection
- Includes objection to profiling for advertising purposes

### Right to Data Portability
- Users can request their data in a structured, machine-readable format
- Must provide within 30 days (GDPR) or 15 days (LGPD)

### Practical Implementation
- Set up a dedicated email or form for data subject requests (e.g., privacy@yourdomain.com)
- Build internal processes to handle requests within the legal timeframe
- Maintain a log of all requests and responses
- Automate where possible (e.g., automatic removal from email lists upon request)

---

## 8. Cross-Border Data Transfers

### EU to Non-EU Transfers (GDPR)
- **Adequacy decisions**: Some countries (UK, Japan, South Korea, etc.) have adequacy status
- **US transfers**: EU-US Data Privacy Framework (DPF) adopted 2023; companies must self-certify
- **Standard Contractual Clauses (SCCs)**: Required for transfers to non-adequate countries without DPF
- **Transfer Impact Assessment (TIA)**: Must assess whether the destination country provides adequate protection

### Brazil to Other Countries (LGPD)
- ANPD developing adequacy assessments
- Standard contractual clauses accepted
- Must ensure receiving country provides adequate protection
- Consent can be used as a legal basis for international transfers

### Ad Platform Data Locations
- Meta: Processes data primarily in the US (DPF participant)
- Google: Processes data globally; DPF participant
- TikTok: Data residency varies; European data increasingly stored in EU (Project Clover)
- LinkedIn (Microsoft): DPF participant

---

## 9. Compliance Checklist for Ad Campaigns

### Before Launching Campaigns in EU/Brazil

- [ ] CMP implemented and tested on all website pages
- [ ] Google Consent Mode v2 configured (required for EU Google Ads)
- [ ] All tracking tags conditional on consent (no tags firing before CMP)
- [ ] Privacy policy updated with all ad platform disclosures
- [ ] DPAs in place with all ad platforms and data processors
- [ ] Cookie banner provides granular consent options (not just "Accept All")
- [ ] Opt-out mechanism working and tested
- [ ] Data subject request process established
- [ ] Records of Processing Activities (ROPA) documented
- [ ] Legitimate Interest Assessments completed (where using legitimate interest)
- [ ] Data retention periods defined and enforced
- [ ] Team trained on compliance procedures
- [ ] Server-side tracking configured to strip unnecessary personal data
- [ ] Lead gen forms include consent checkboxes and privacy policy links
- [ ] Custom Audience uploads based on properly consented data

### Ongoing Compliance

- [ ] Monthly audit of consent rates and data collection
- [ ] Quarterly review of data processing activities
- [ ] Annual privacy policy review and update
- [ ] Respond to data subject requests within legal timeframes
- [ ] Monitor regulatory changes and platform policy updates
- [ ] Test CMP functionality after any website or tag changes
- [ ] Review and update DPAs when changing service providers

---

## 10. Impact on Campaign Performance

### Expected Data Loss from Consent Requirements

| Metric | Typical Impact in EU |
|--------|---------------------|
| Conversion tracking | 20-40% underreporting |
| Retargeting audiences | 30-60% smaller |
| Analytics data | 15-30% less traffic recorded |
| Attribution accuracy | Reduced; more modeled data |
| Custom Audiences (uploads) | 10-20% smaller after consent filtering |

### Mitigation Strategies

1. **Google Consent Mode v2**: Enables modeled conversions to partially recover lost data
2. **Server-side tracking with consent**: Improves data quality for consented users
3. **Conversion modeling**: Use platform modeling features (Meta's Aggregated Event Measurement)
4. **First-party data strategy**: Invest in building consented first-party data assets
5. **Contextual targeting**: Does not require consent; viable alternative to behavioral targeting
6. **Broad targeting**: Let platform algorithms optimize with available signals
7. **Marketing Mix Modeling (MMM)**: Aggregate analysis that does not rely on individual-level tracking

---

*Last updated: March 2026. Privacy regulations are actively evolving. This guide covers GDPR and LGPD but similar laws exist in many jurisdictions (CCPA/CPRA in California, POPIA in South Africa, PDPA in Thailand, etc.). Consult with a privacy attorney for jurisdiction-specific compliance.*
