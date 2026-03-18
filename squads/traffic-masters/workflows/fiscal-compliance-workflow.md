# Fiscal Compliance Workflow (Brazil Context)
> **Type**: Workflow
> **Duration**: Ongoing (monthly cycle)
> **Agents involved**: fiscal, traffic-chief, media-buyer

## Trigger
Monthly fiscal close, new ad account setup, or audit request from finance/tax authority.

## Steps
1. Invoice Collection → Agent: fiscal → Framework: NF Tracking → Output: All platform invoices (Notas Fiscais) collected for the period
2. Spend Reconciliation → Agent: fiscal → Framework: Three-Way Match → Output: Platform spend matched against NFs and bank statements
3. Currency Reconciliation → Agent: fiscal → Framework: BRL/USD Matching → Output: Exchange rate variations documented and reconciled
4. Tax Classification → Agent: fiscal → Framework: Brazilian Tax Code → Output: Ad spend properly classified (ISS, IOF for international payments)
5. LGPD Compliance Check → Agent: fiscal → Framework: LGPD Audit → Output: Data processing activities verified against LGPD requirements
6. Platform Billing Review → Agent: media-buyer → Framework: Billing Health Check → Output: Payment methods verified, no overdue balances, credit lines adequate
7. Report Generation → Agent: fiscal → Framework: Fiscal Report Template → Output: Monthly fiscal compliance report with all documentation
8. Archive → Agent: fiscal → Framework: Document Retention → Output: All documents archived per legal retention requirements (5+ years)

## Quality Gates
- [ ] All NFs received and verified for the period
- [ ] Spend reconciled within 2% tolerance
- [ ] Currency conversions documented with source rates
- [ ] Tax obligations identified and communicated to accounting
- [ ] LGPD consent mechanisms verified on all tracking
- [ ] No outstanding platform billing issues
- [ ] All documents archived in compliant format

## Output
Monthly fiscal compliance package ready for accounting.
LGPD compliance verification document.
Reconciliation report with any discrepancies noted and resolved.

## Key Brazilian Compliance Items
- NF-e (Nota Fiscal Eletronica) for all service payments
- ISS (Imposto Sobre Servicos) on digital advertising services
- IOF on international credit card transactions (Meta, Google)
- LGPD compliance for all pixel/tracking data collection
- Consent banners required on all tracked landing pages

## Notes
- Meta and Google bill in USD; reconcile at actual exchange rate, not commercial rate
- Keep copies of all platform Terms of Service changes
- LGPD requires documented legal basis for each data processing activity
- Annual compliance review with legal counsel recommended
- Maintain updated record of all data processors (platforms, tools, partners)

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
