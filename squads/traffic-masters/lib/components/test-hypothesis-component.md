# Test Hypothesis Component

## Purpose
Standardized format for writing and evaluating test hypotheses.

## Hypothesis Formula
"If we [change X], then [metric Y] will [improve/decrease] by [amount Z] because [reason/evidence]."

## Component Fields
- `hypothesis_id`: Identifier
- `statement`: Full hypothesis text
- `variable`: What is being changed
- `metric`: What is being measured
- `expected_impact`: Direction and magnitude
- `rationale`: Why we believe this
- `evidence`: Data or precedent supporting belief
- `priority`: High / Medium / Low
- `effort`: Low / Medium / High
- `impact_potential`: Low / Medium / High

## Prioritization Matrix

| | Low Effort | High Effort |
|---|-----------|------------|
| **High Impact** | DO FIRST | Plan & execute |
| **Low Impact** | Quick wins | Skip/defer |

## Hypothesis Quality Checklist
- [ ] Is the variable specific and isolated?
- [ ] Is the metric clearly defined?
- [ ] Is the expected impact measurable?
- [ ] Is the rationale evidence-based (not just opinion)?
- [ ] Can we reach statistical significance within budget?
- [ ] Is the test duration realistic?

## Common Hypothesis Categories
1. **Hook:** Does a new hook improve CTR/hook rate?
2. **Angle:** Does a different angle lower CPA?
3. **Audience:** Does a new segment perform better?
4. **Bid Strategy:** Does changing bid approach improve efficiency?
5. **Landing Page:** Does a page change improve conversion rate?
6. **Offer:** Does modifying the offer improve response?
7. **Format:** Does a different creative format perform better?
