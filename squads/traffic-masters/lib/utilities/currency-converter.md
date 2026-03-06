# Currency Converter Reference

## Purpose
Reference guide for handling multi-currency campaigns and reporting. Provides conversion guidelines, common currency pairs, and best practices for financial accuracy in global paid traffic campaigns.

---

## Common Advertising Currencies

| Currency | Code | Symbol | Major Markets |
|---|---|---|---|
| US Dollar | USD | $ | United States, global default |
| Euro | EUR | E | Eurozone (Germany, France, Italy, Spain, etc.) |
| British Pound | GBP | L | United Kingdom |
| Canadian Dollar | CAD | C$ | Canada |
| Australian Dollar | AUD | A$ | Australia |
| Brazilian Real | BRL | R$ | Brazil |
| Mexican Peso | MXN | MX$ | Mexico |
| Japanese Yen | JPY | Y | Japan |
| Indian Rupee | INR | Rs | India |
| South Korean Won | KRW | W | South Korea |
| Singapore Dollar | SGD | S$ | Singapore |
| Hong Kong Dollar | HKD | HK$ | Hong Kong |
| Swiss Franc | CHF | CHF | Switzerland |
| Swedish Krona | SEK | kr | Sweden |
| Norwegian Krone | NOK | kr | Norway |
| Danish Krone | DKK | kr | Denmark |
| New Zealand Dollar | NZD | NZ$ | New Zealand |
| South African Rand | ZAR | R | South Africa |
| UAE Dirham | AED | AED | United Arab Emirates |
| Israeli Shekel | ILS | NIS | Israel |

---

## Conversion Principles

### Rule 1: Use Consistent Currency in Reports
All metrics in a single report should use the same currency. Convert all figures to a single reporting currency.

### Rule 2: Document the Exchange Rate
Always note the exchange rate used and the date/source of the rate.

### Rule 3: Use Mid-Market Rates
Unless billing rates are known, use the mid-market rate (average of bid and ask).

### Rule 4: Match Platform Billing Currency
Platform dashboards report in the billing currency of the ad account. This may differ from the client's reporting currency.

---

## Conversion Formulas

### Basic Conversion
```
Amount in Target Currency = Amount in Source Currency x Exchange Rate
```
**Example:** $1,000 USD x 0.92 EUR/USD = EUR 920

### Reverse Conversion
```
Amount in Source Currency = Amount in Target Currency / Exchange Rate
```
**Example:** EUR 920 / 0.92 EUR/USD = $1,000 USD

### Converting Metrics

| Metric | How to Convert |
|---|---|
| **Spend** | Multiply by exchange rate |
| **Revenue** | Multiply by exchange rate |
| **CPA** | Multiply by exchange rate |
| **CPC** | Multiply by exchange rate |
| **CPM** | Multiply by exchange rate |
| **ROAS** | No conversion needed (it is a ratio) |
| **CTR** | No conversion needed (it is a percentage) |
| **CVR** | No conversion needed (it is a percentage) |
| **ROI** | No conversion needed (it is a percentage) |

**Key insight:** Ratios (ROAS, CTR, CVR, ROI) do not require currency conversion. Only absolute monetary values need conversion.

---

## Exchange Rate Sources

| Source | Type | Best For | URL |
|---|---|---|---|
| **XE.com** | Mid-market | Day-to-day reference | xe.com |
| **Google Finance** | Mid-market | Quick checks | google.com/finance |
| **OANDA** | Historical rates | Reconciliation, historical reports | oanda.com |
| **European Central Bank** | Official | EUR-based reporting | ecb.europa.eu |
| **Federal Reserve** | Official | USD-based historical | federalreserve.gov |
| **Platform billing** | Actual billed rate | Invoice reconciliation | Platform billing page |

---

## Platform Currency Handling

### Meta Ads
- Account currency set at account creation (cannot be changed)
- Multi-country campaigns bill in the account currency
- Conversions are reported in the account currency
- Revenue values use the platform's exchange rate at time of conversion

### Google Ads
- Billing currency set at account creation
- Manager accounts can have sub-accounts in different currencies
- Reports can be exported in billing currency or converted
- Currency conversion for reporting uses Google's daily exchange rate

### TikTok Ads
- Account currency set at creation
- Reports are in the account currency
- Cross-border campaigns use TikTok's exchange rates

---

## Multi-Market Campaign Considerations

### Scenario: Managing Campaigns Across Markets

| Market | Account Currency | Reporting Currency | Daily Rate Source | Monthly Avg Rate |
|---|---|---|---|---|
| US | USD | USD (base) | -- | 1.000 |
| UK | GBP | USD | XE.com | `{{RATE}}` |
| EU (Germany) | EUR | USD | XE.com | `{{RATE}}` |
| Canada | CAD | USD | XE.com | `{{RATE}}` |
| Australia | AUD | USD | XE.com | `{{RATE}}` |
| Brazil | BRL | USD | XE.com | `{{RATE}}` |

### Best Practices for Multi-Market Reporting

1. **Choose a base reporting currency** (typically USD or the client's home currency)
2. **Use monthly average rates** for monthly reports (reduces daily fluctuation noise)
3. **Use daily rates** for daily/weekly reports and invoice reconciliation
4. **Note the rate and date** in every report: "Exchange rates as of YYYY-MM-DD from XE.com"
5. **Track FX impact separately** when currency moves > 5% in a month

### FX Impact Calculation
```
FX Impact = Spend in Local Currency x (Current Rate - Previous Rate)
```
**Example:** EUR 10,000 spend. Rate moved from 1.08 to 1.12 USD/EUR.
FX Impact = 10,000 x (1.12 - 1.08) = $400 increase in USD terms (not a performance change).

---

## Reporting Template for Multi-Currency

| Market | Local Spend | FX Rate | USD Spend | Local Rev | USD Revenue | ROAS | CPA (Local) | CPA (USD) |
|---|---|---|---|---|---|---|---|---|
| US | $10,000 | 1.000 | $10,000 | $50,000 | $50,000 | 5.0x | $50 | $50 |
| UK | GBP 5,000 | 1.27 | $6,350 | GBP 25,000 | $31,750 | 5.0x | GBP 25 | $32 |
| DE | EUR 4,000 | 1.09 | $4,360 | EUR 16,000 | $17,440 | 4.0x | EUR 40 | $44 |
| CA | CAD 3,000 | 0.74 | $2,220 | CAD 12,000 | $8,880 | 4.0x | CAD 30 | $22 |
| **Total** | -- | -- | **$22,930** | -- | **$108,070** | **4.7x** | -- | **$42** |

---

## Budget Planning Across Currencies

When setting budgets across markets:

```
Total USD Budget: ${{TOTAL}}

Market Allocation:
  US:  ${{}} USD ({{}}%)
  UK:  GBP {{}} = ${{}} USD at {{RATE}} ({{}}%)
  EU:  EUR {{}} = ${{}} USD at {{RATE}} ({{}}%)
  CA:  CAD {{}} = ${{}} USD at {{RATE}} ({{}}%)

Rate Lock Date: {{DATE}}
Rate Review Frequency: Monthly
FX Risk Buffer: {{5-10%}} of total budget
```

### FX Risk Mitigation
- Include a 5-10% FX buffer in multi-currency budgets
- Review exchange rates monthly and adjust local-currency budgets if rates move > 5%
- Use forward rates for planning if available
- Lock rates at the start of each month for consistent reporting
