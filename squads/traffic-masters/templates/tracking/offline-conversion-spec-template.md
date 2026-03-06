# Offline Conversion Import Specification

## Spec Metadata

| Field | Value |
|---|---|
| **Client / Account** | `{{CLIENT_NAME}}` |
| **Prepared By** | `{{SPECIALIST_NAME}}` |
| **Date** | `{{DATE}}` |
| **Platforms** | `{{PLATFORMS}}` (Google Ads / Meta / TikTok / LinkedIn) |
| **CRM / Source System** | `{{CRM_NAME}}` (HubSpot / Salesforce / Pipedrive / Custom) |
| **Import Method** | Manual Upload / API / Zapier / Native Integration |
| **Import Frequency** | `{{DAILY / WEEKLY / REAL-TIME}}` |

---

## Purpose

> Documentacao tecnica para importar conversoes offline (vendas fechadas, ligacoes, visitas a loja) de volta para as plataformas de ads, permitindo que os algoritmos otimizem para resultados de negocio reais em vez de proxy events.

---

## Data Schema — Campos Obrigatorios

### Google Ads (Offline Conversion Import)

| Campo | Tipo | Obrigatorio | Descricao | Exemplo |
|---|---|---|---|---|
| `gclid` | String | Sim (click import) | Google Click ID capturado na URL | `CjwKCAjw...` |
| `conversion_name` | String | Sim | Nome da acao de conversao no Google Ads | `Qualified_Lead` |
| `conversion_time` | DateTime | Sim | Data/hora da conversao offline | `2026-03-01 14:30:00-03:00` |
| `conversion_value` | Float | Recomendado | Valor monetario da conversao | `2500.00` |
| `conversion_currency` | String | Recomendado | Codigo da moeda | `BRL` |
| `external_attribution_credit` | Float | Opcional | Credito fracionado (0-1) | `0.5` |

### Meta Ads (Offline Conversions via CAPI)

| Campo | Tipo | Obrigatorio | Descricao | Exemplo |
|---|---|---|---|---|
| `event_name` | String | Sim | Nome do evento (Purchase, Lead, etc.) | `Purchase` |
| `event_time` | Unix Timestamp | Sim | Timestamp da conversao | `1709312400` |
| `user_data.em` | String (SHA256) | Sim* | Email hashado | `a1b2c3d4...` |
| `user_data.ph` | String (SHA256) | Recomendado | Telefone hashado (+55...) | `e5f6g7h8...` |
| `user_data.fn` | String (SHA256) | Recomendado | Primeiro nome hashado | `i9j0k1l2...` |
| `user_data.fbc` | String | Recomendado | Facebook Click ID (do cookie `_fbc`) | `fb.1.1709...` |
| `user_data.fbp` | String | Recomendado | Facebook Browser ID (do cookie `_fbp`) | `fb.1.1709...` |
| `custom_data.value` | Float | Recomendado | Valor da conversao | `2500.00` |
| `custom_data.currency` | String | Recomendado | Moeda | `BRL` |
| `action_source` | String | Sim | Origem da acao | `system_generated` |

> *Minimo um identificador de usuario obrigatorio (email, telefone, ou fbc/fbp)

---

## Mapeamento CRM -> Plataforma

### Eventos de Conversao

| Evento no CRM | Stage no Pipeline | Google Ads Conversion | Meta Event | Valor Atribuido |
|---|---|---|---|---|
| `{{CRM_STAGE_1}}` | `{{PIPELINE_STAGE}}` | `{{CONVERSION_NAME}}` | `{{EVENT_NAME}}` | $`{{VALUE}}` |
| `{{CRM_STAGE_2}}` | `{{}}` | `{{}}` | `{{}}` | $`{{}}` |
| `{{CRM_STAGE_3}}` | `{{}}` | `{{}}` | `{{}}` | $`{{}}` |
| `{{CRM_STAGE_4}}` | `{{}}` | `{{}}` | `{{}}` | $`{{}}` |

### Exemplo de Mapeamento Tipico

| Evento no CRM | Stage | Google Conversion | Meta Event | Valor |
|---|---|---|---|---|
| Lead Criado | New Lead | `New_Lead` | `Lead` | R$50 |
| MQL | Qualified | `MQL` | `Lead` (custom param) | R$200 |
| SQL | Sales Accepted | `SQL` | `Lead` (custom param) | R$500 |
| Proposta Enviada | Proposal | `Proposal_Sent` | `InitiateCheckout` | R$1000 |
| Venda Fechada | Closed Won | `Closed_Won` | `Purchase` | Valor real do deal |

---

## Requisitos Tecnicos

### Captura de Click IDs
- [ ] `gclid` capturado na URL e armazenado no CRM (Google Ads)
- [ ] `fbclid` capturado ou cookies `_fbc` / `_fbp` armazenados (Meta)
- [ ] `ttclid` capturado (TikTok, se aplicavel)
- [ ] Click IDs persistem no CRM ate o momento da conversao offline

### Hashing (Meta CAPI)
- [ ] Emails em lowercase antes de hash SHA256
- [ ] Telefones no formato E.164 (+5511999998888) antes de hash
- [ ] Nomes em lowercase, sem acentos, antes de hash
- [ ] Hash feito server-side, nunca client-side

### Timing e Janela
- Upload maximo 90 dias apos o click (Google) / 7 dias recomendado (Meta)
- Quanto mais rapido o upload, melhor para otimizacao do algoritmo
- Real-time via API/webhook e ideal; daily batch e aceitavel

---

## Validation Checklist

- [ ] Dados de teste enviados e verificados na plataforma
- [ ] Match rate acima de 40% (Meta) / conversoes aparecendo (Google)
- [ ] Valores de conversao corretos na moeda certa
- [ ] Deduplicacao implementada (evitar dupla contagem)
- [ ] Erro handling configurado (logs de falha de upload)
- [ ] Monitoramento de match rate semanal
- [ ] Documentacao de fluxo acessivel a equipe tecnica e de ads

---

*Spec version 1.0 — Traffic Masters Squad*
