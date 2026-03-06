# Incrementality / Lift Test Report

## Test Metadata

| Field | Value |
|---|---|
| **Test Name** | `{{TEST_NAME}}` |
| **Channel Tested** | `{{CHANNEL_NAME}}` |
| **Test Type** | Geo Lift / Holdout / Platform Lift Study / Budget On-Off |
| **Prepared By** | `{{ANALYST_NAME}}` |
| **Test Period** | `{{START_DATE}}` to `{{END_DATE}}` |
| **Test Duration** | `{{WEEKS}}` semanas |
| **Test Budget (Spend During Test)** | $`{{TEST_SPEND}}` |
| **Client / Account** | `{{CLIENT_NAME}}` |

---

## Hypothesis

> "Acreditavamos que [canal/campanha] gera [X]% de conversoes incrementais, ou seja, conversoes que NAO teriam acontecido sem o ad."

`{{HYPOTHESIS}}`

---

## Test Design

### Metodologia
`{{TEST_TYPE_DETAIL}}`

### Grupo Teste vs Controle

| | Grupo Teste | Grupo Controle |
|---|---|---|
| **Definicao** | `{{}}` | `{{}}` |
| **Tamanho / Geos** | `{{}}` | `{{}}` |
| **Exposicao ao Ad** | Sim | Nao |
| **Match Score** | `{{}}`% similaridade pre-teste |

### Variaveis Controladas
- [ ] Nenhuma mudanca de preco durante o teste
- [ ] Nenhuma promocao exclusiva para teste/controle
- [ ] Outros canais mantidos constantes
- [ ] Nenhuma mudanca de landing page
- [ ] Sazonalidade similar entre grupos

---

## Results

### Metricas Principais

| Metrica | Grupo Teste | Grupo Controle | Diferenca | Lift % |
|---|---|---|---|---|
| Conversoes | `{{}}` | `{{}}` | `{{}}` | `{{}}`% |
| Revenue | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| Conversion Rate | `{{}}`% | `{{}}`% | `{{}}`pp | `{{}}`% |

### Incremental Metrics

| Metrica | Valor |
|---|---|
| **Incremental Conversions** | `{{TESTE_CONV - CONTROLE_CONV}}` |
| **Incremental Revenue** | $`{{TESTE_REV - CONTROLE_REV}}` |
| **iCPA (Incremental CPA)** | $`{{SPEND / INCREMENTAL_CONVERSIONS}}` |
| **iROAS (Incremental ROAS)** | `{{INCREMENTAL_REVENUE / SPEND}}`x |
| **Incrementality Rate** | `{{INCREMENTAL_CONV / TOTAL_TEST_CONV}}`% |

### Statistical Significance

| Metric | Value |
|---|---|
| **p-value** | `{{P_VALUE}}` |
| **Confidence Level** | `{{}}`% |
| **Confidence Interval** | `{{LOWER_BOUND}}` to `{{UPPER_BOUND}}` |
| **Statistically Significant?** | Sim / Nao |

---

## Platform-Reported vs Incremental Comparison

| Metrica | Platform-Reported | Incremental (Teste) | Inflation Factor |
|---|---|---|---|
| Conversoes | `{{}}` | `{{}}` | `{{}}`x |
| ROAS | `{{}}`x | `{{}}`x | `{{}}`x |
| CPA | $`{{}}` | $`{{}}` | `{{}}`x |

> **Inflation Factor** = Platform-Reported / Incremental. Acima de 1.0x significa que a plataforma sobre-reporta.

---

## Analysis e Insights

### Conclusao Principal
`{{MAIN_CONCLUSION}}`

### Insights Adicionais
- `{{INSIGHT_1}}`
- `{{INSIGHT_2}}`
- `{{INSIGHT_3}}`

### Limitacoes do Teste
- `{{LIMITATION_1}}`
- `{{LIMITATION_2}}`

---

## Recommendation

| Resultado | Recomendacao | Impacto Esperado |
|---|---|---|
| `{{RESULTADO_RESUMIDO}}` | `{{ACAO_RECOMENDADA}}` | `{{IMPACTO}}` |

### Budget Implication
`{{BUDGET_RECOMMENDATION}}`

---

## Next Steps

- [ ] `{{TASK}}` -- Owner: `{{OWNER}}` -- Due: `{{DATE}}`
- [ ] `{{TASK}}` -- Owner: `{{OWNER}}` -- Due: `{{DATE}}`
- [ ] `{{TASK}}` -- Owner: `{{OWNER}}` -- Due: `{{DATE}}`

---

*Report generated at `{{TIMESTAMP}}`. Test methodology: `{{METHODOLOGY}}`. Statistical model: `{{MODEL_USED}}`.*
