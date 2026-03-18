# Campaign Launch End-to-End
> **Type**: Workflow
> **Duration**: 5-7 business days
> **Agents involved**: traffic-chief, media-buyer, ad-midas, pixel-specialist, ads-analyst

## Trigger
New campaign brief approved by client or internal stakeholder.

## Steps
1. Strategy Definition → Agent: traffic-chief → Framework: GECO → Output: Campaign strategy document with objectives, audiences, budget allocation
2. Audience Research → Agent: traffic-chief → Framework: Sobral Audience Matrix → Output: Audience segments with temperature mapping (cold/warm/hot)
3. Creative Production → Agent: ad-midas → Framework: Hook-Story-Offer → Output: Ad creatives in all required formats and placements
4. Campaign Build → Agent: media-buyer → Framework: Mandalia BPM → Output: Campaigns structured in platform with proper naming conventions
5. Tracking Setup → Agent: pixel-specialist → Framework: UTM + CAPI → Output: Pixels fired, CAPI configured, UTMs appended, test conversions verified
6. Internal QA → Agent: ads-analyst → Framework: Pre-Launch Checklist → Output: QA sign-off document
7. Go-Live → Agent: media-buyer → Framework: Soft Launch Protocol → Output: Campaigns live at minimum viable budget
8. Post-Launch Monitor → Agent: media-buyer → Framework: GECO-ANA → Output: First 24-48h performance snapshot

## Quality Gates
- [ ] Strategy document reviewed and approved
- [ ] All creatives meet platform specs and policies
- [ ] Tracking pixels firing correctly on all events
- [ ] UTM parameters consistent with naming convention
- [ ] Budget matches approved allocation
- [ ] Landing page load time under 3 seconds
- [ ] All links tested and functional
- [ ] Naming conventions followed in ad platform

## Output
Live campaign with verified tracking, documented strategy, and initial performance baseline.
Stored in: `/campaigns/{client}/{campaign-name}/launch-docs/`

## Rollback Plan
If critical issues found within first 24h, pause campaigns, diagnose, fix, and re-launch.
Document all issues in the campaign log for future reference.

## Notes
- Always soft-launch at 50% budget for first 24-48h
- Notify cross-squad (Copy, Brand) at least 48h before go-live
- Brazilian campaigns require NF compliance check before spend

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
