# Policy Risk Scan

> **Type**: Task
> **Category**: research
> **Agents**: Ads Analyst, Fiscal
> **Frameworks**: Policy Compliance Framework
> **Checklists**: policy-risk-checklist
> **Output template**: templates/risk-assessment.md

## ROUTING (from config.yaml)

> **Config key**: `routing.policy-risk-scan`
> **Agents**: [ads-analyst](../../agents/ads-analyst.md), [fiscal](../../agents/fiscal.md)
> **Frameworks**: `policy-risk-classification`
> **Checklists**: `compliance-ad-policies-quality`
> **Templates**: N/A
> **Registry**: `data/research/policy-risk`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Scan for advertising policy risks across all planned platforms by evaluating claims, targeting methods, content types, and industry-specific restrictions to prevent ad rejections, account suspensions, and compliance violations.

## Inputs
- Planned advertising platforms list
- Product or service details and health/financial claims
- Draft ad copy and creative concepts
- Landing page URLs and content
- Target audience details including special categories
- Industry vertical classification

## Steps
1. Review each platform's advertising policies for the specific vertical (Meta, Google, TikTok, etc.)
2. Identify special ad categories that apply: housing, credit, employment, politics, health, crypto
3. Audit planned claims against platform-specific claim policies and substantiation requirements
4. Review targeting plan for restricted targeting in special categories
5. Scan landing page content for policy violations: misleading claims, missing disclosures, prohibited content
6. Check creative concepts for restricted content: before/after, personal attributes, sensationalism
7. Evaluate data collection practices against platform privacy policies and regional regulations
8. Assess trademark usage risks in ad copy and keywords
9. Document each risk with severity level (high, medium, low) and recommended mitigation
10. Create a compliance action list with required changes before launch

## Output
Risk assessment report containing: policy risk inventory by platform, severity ratings, specific violations identified, required mitigations, compliance action list with owners and deadlines, and ongoing monitoring recommendations.

## Quality Gate
- Policy risk checklist confirms all platforms and content types scanned
- All high-severity risks have documented mitigation plans
- Fiscal confirms regulatory compliance for financial and tax implications

## Duration
2-4 hours depending on number of platforms and complexity of vertical
