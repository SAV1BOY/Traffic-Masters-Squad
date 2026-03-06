# New Channel Test Plan

## Test Metadata

| Field | Value |
|---|---|
| **Client / Account** | `{{CLIENT_NAME}}` |
| **New Channel** | `{{CHANNEL_NAME}}` (ex: TikTok Ads, Pinterest, Reddit, etc.) |
| **Prepared By** | `{{STRATEGIST_NAME}}` |
| **Test Start Date** | `{{START_DATE}}` |
| **Test End Date** | `{{END_DATE}}` |
| **Test Duration** | `{{WEEKS}}` semanas |
| **Test Budget** | $`{{TOTAL_TEST_BUDGET}}` |
| **Decision Date** | `{{DECISION_DATE}}` |

---

## Strategic Rationale

### Por que testar este canal?
`{{RATIONALE}}`

### Hipotese
> "Acreditamos que [canal] pode gerar [metrica] de [valor] porque [razao baseada em dados/research]."

`{{HYPOTHESIS}}`

### Riscos Identificados
| Risco | Probabilidade | Mitigacao |
|---|---|---|
| `{{}}` | Alta/Media/Baixa | `{{}}` |
| `{{}}` | `{{}}` | `{{}}` |

---

## Success Criteria

### Metricas de Sucesso (definir ANTES de lancar)

| Metrica | Target Minimo | Target Ideal | Deal-Breaker |
|---|---|---|---|
| CPA / CPL | $`{{}}` | $`{{}}` | > $`{{}}` |
| ROAS | `{{}}`x | `{{}}`x | < `{{}}`x |
| CTR | `{{}}`% | `{{}}`% | < `{{}}`% |
| Volume de Conversoes | `{{}}` / semana | `{{}}` / semana | < `{{}}` / semana |
| Lead Quality (se lead gen) | `{{}}`% SQL rate | `{{}}`% | < `{{}}`% |

### Decision Framework
| Resultado | Acao |
|-----------|------|
| Todas metricas acima do target minimo | Escalar gradualmente (2x budget por semana) |
| Mix de acima/abaixo do target | Extender teste por 2 semanas com otimizacoes |
| Todas abaixo do target minimo | Pausar e documentar learnings |
| Deal-breaker atingido | Kill imediato |

---

## Test Setup

### Account e Tracking
- [ ] Conta de ads criada e verificada
- [ ] Pixel / conversion tag instalado
- [ ] Eventos de conversao configurados e testados
- [ ] CAPI / server-side tracking implementado (se disponivel)
- [ ] UTMs padronizados para o novo canal

### Campaign Structure

| Campaign | Objective | Audience | Daily Budget | Duration |
|---|---|---|---|---|
| `{{}}` | `{{}}` | `{{}}` | $`{{}}` | `{{}}` |
| `{{}}` | `{{}}` | `{{}}` | $`{{}}` | `{{}}` |

### Creative Plan
| Creative | Format | Specs | Adaptacao Necessaria |
|---|---|---|---|
| `{{}}` | `{{}}` | `{{}}` | `{{ADAPTAR_DE_OUTRO_CANAL / CRIAR_NOVO}}` |
| `{{}}` | `{{}}` | `{{}}` | `{{}}` |

---

## Learning Agenda

> Alem de performance, o que queremos aprender com este teste?

- [ ] Qual audience responde melhor neste canal?
- [ ] Qual formato de creative performa melhor?
- [ ] Qual e o CPM medio e como se compara aos canais atuais?
- [ ] O canal gera conversoes incrementais ou canibaliza canais existentes?
- [ ] `{{ADDITIONAL_LEARNING_QUESTION}}`

---

## Reporting Cadence

| Frequencia | Report | Destinatario |
|---|---|---|
| Diario | Quick check (spend, CPA, anomalias) | Media Buyer |
| Semanal | Performance summary vs targets | Traffic Chief |
| Final do Teste | Full test report com recomendacao | Stakeholders |

---

## Post-Test Deliverables

- [ ] Test results report completo
- [ ] Go / No-Go recommendation com justificativa
- [ ] Se Go: scaling plan com budget phasing
- [ ] Se No-Go: documentacao de learnings para futuro
- [ ] Creative learnings transferiveis para outros canais

---

*Template version 1.0 — Traffic Masters Squad*
