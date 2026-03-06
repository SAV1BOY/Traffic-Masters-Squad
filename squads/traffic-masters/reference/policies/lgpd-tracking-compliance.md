# LGPD Tracking Compliance Guide
> **Category**: Data Privacy and Tracking (Brazil)
> **Last Updated**: 2026-03

## Overview
The LGPD (Lei Geral de Protecao de Dados) is Brazil's data protection law, effective since 2020. It governs how personal data is collected, processed, and stored, directly impacting tracking and advertising activities.

## Key Principles
- Consent must be freely given, informed, and specific
- Data collection must have a clear, documented legal basis
- Users must be able to access, correct, and delete their data
- Data processing activities must be documented and justified
- Data breaches must be reported to the ANPD (National Data Protection Authority)

## Legal Bases for Tracking
1. **Consent**: User explicitly agrees (cookie banner, opt-in form)
2. **Legitimate Interest**: Advertiser has justified business interest (must be documented)
3. **Contract Execution**: Data needed to fulfill a service the user requested

## Tracking Implementation Requirements
- **Cookie Consent Banner**: Required on all websites collecting data from Brazilian users
- **Privacy Policy**: Must describe all tracking technologies used and their purposes
- **Data Processing Record**: Document all data collection activities, tools, and processors
- **Opt-Out Mechanism**: Users must be able to revoke consent at any time
- **Data Retention Policy**: Define how long tracking data is stored

## Platform-Specific Considerations
- **Meta Pixel**: Consent required before firing pixel; implement consent mode
- **Google Tags**: Google Consent Mode v2 compatible with LGPD requirements
- **Server-Side Tracking**: Still requires consent for personal data processing
- **CRM Integration**: Imported data must have documented consent from collection point

## Compliance Checklist
- [ ] Cookie consent banner implemented with granular controls
- [ ] Privacy policy updated with all tracking technologies listed
- [ ] Data processing record (ROPA) maintained and current
- [ ] DPO (Data Protection Officer) designated or documented as not required
- [ ] User data access/deletion request process documented
- [ ] Third-party data processors (platforms, tools) listed with agreements
- [ ] Consent records stored as evidence of compliance

## Key Takeaways
- LGPD applies to any data collection from users in Brazil, regardless of company location
- Consent mode implementation is essential for compliant tracking
- Document everything — the burden of proof is on the data controller
- Review compliance quarterly as ANPD enforcement evolves
- Server-side tracking does not bypass LGPD — consent is still required
