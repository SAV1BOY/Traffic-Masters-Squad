# Tracking Setup and QA
> **Type**: Workflow
> **Duration**: 2-3 business days
> **Agents involved**: Tracking Specialist, Media Buyer, QA Analyst

## Trigger
New campaign launch, new landing page, platform migration, or tracking discrepancy detected.

## Steps
1. Requirements Gathering → Agent: Tracking Specialist → Framework: Event Mapping → Output: Conversion event list with priority (primary, secondary, micro)
2. Pixel Installation → Agent: Tracking Specialist → Framework: GTM Implementation → Output: Base pixels installed for all platforms (Meta, Google, TikTok)
3. Event Configuration → Agent: Tracking Specialist → Framework: DataLayer Spec → Output: Custom events configured with correct parameters and values
4. CAPI Setup → Agent: Tracking Specialist → Framework: Server-Side Protocol → Output: Conversions API connected with deduplication keys
5. UTM Framework → Agent: Tracking Specialist → Framework: UTM Naming Convention → Output: UTM builder configured with standard parameters
6. GA4 Configuration → Agent: Tracking Specialist → Framework: GA4 Event Model → Output: GA4 events, conversions marked, audiences created
7. Testing Round 1 → Agent: QA Analyst → Framework: Test Conversion Protocol → Output: Test events verified in all platforms with parameter check
8. Testing Round 2 → Agent: QA Analyst → Framework: Cross-Browser/Device → Output: Events firing on Chrome, Safari, Firefox, mobile, desktop
9. Documentation → Agent: Tracking Specialist → Framework: Tracking Doc Template → Output: Complete tracking document with event map and pixel IDs
10. Validation Sign-off → Agent: Media Buyer → Framework: Pre-Launch Check → Output: Confirmed tracking ready for campaign launch

## Quality Gates
- [ ] All conversion events firing with correct values
- [ ] CAPI events matching browser events (deduplication working)
- [ ] UTM parameters appending correctly to all ad URLs
- [ ] GA4 receiving data and conversions marked
- [ ] Event match quality score above 6.0 (Meta)
- [ ] Cross-device and cross-browser testing passed
- [ ] Cookie consent/LGPD compliance verified
- [ ] Documentation complete and accessible

## Output
Fully validated tracking setup with documentation.
Test conversion log showing all events verified.
Tracking health baseline for ongoing monitoring.

## Common Issues Checklist
- Double-firing events (check deduplication)
- Missing currency/value parameters on purchase events
- GTM container not published
- CAPI token expired or misconfigured
- iOS 14+ attribution gaps
- Ad blockers preventing pixel fire

## Notes
- Always test with Meta Pixel Helper and Google Tag Assistant
- Server-side tracking preferred for high-value conversions
- Re-validate tracking after any website changes
- Keep a backup of GTM container before major changes
