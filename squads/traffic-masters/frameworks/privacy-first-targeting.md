# Privacy-First Targeting
> **Type**: Targeting Strategy Framework
> **Used by agents**: Media Buyer, Pixel Specialist, Traffic Chief

## Overview
Framework para estrategias de targeting que funcionam no mundo pos-iOS 14.5, pos-cookies e com regulamentacoes de privacidade (LGPD, GDPR). Foco em first-party data, contextual targeting, broad audiences e server-side tracking como fundacao de performance sustentavel.

## When to Use
- Planejamento de targeting para qualquer campanha digital
- Quando attribution gaps estao impactando otimizacao
- Migracao de estrategias dependentes de third-party cookies
- Adaptacao a mudancas de privacidade em plataformas (Meta, Google, Apple)

## O Contexto de Privacidade

### O Que Mudou
1. **iOS 14.5+ (ATT):** Opt-in para tracking caiu para ~25% dos usuarios iOS
2. **Cookie deprecation:** Chrome eliminando third-party cookies (timeline estendida mas inevitavel)
3. **LGPD/GDPR:** Consentimento explicito necessario para coleta de dados pessoais
4. **Platform restrictions:** Janelas de atribuicao menores, dados agregados, SKAdNetwork

### Impacto no Targeting
- Lookalike audiences menores e menos precisos
- Retargeting pools encolheram 30-50%
- Conversion data incompleto afeta otimizacao de algoritmo
- Cross-device tracking quebrado

## The Framework

### Layer 1: First-Party Data Foundation
- Coletar dados com consentimento direto (email, telefone, preferencias)
- Implementar Conversions API (CAPI) / Enhanced Conversions
- Construir Customer Data Platform (CDP) ou warehouse unificado
- Hash e match de dados proprios com plataformas (Customer Match, Custom Audiences)

### Layer 2: Contextual and Interest Targeting
- Targeting por contexto de pagina/conteudo (nao por usuario)
- Google Topics API como substituto de cookies
- Placement targeting manual em sites relevantes
- Content adjacency — aparecer ao lado de conteudo alinhado ao produto

### Layer 3: Broad + Algorithmic Targeting
- Advantage+ / Broad targeting com creative como targeting
- Performance Max com signals (nao restricoes)
- Deixar o algoritmo encontrar o audience — fornecer creative diversificado
- Machine learning precisa de volume de dados — consolide campanhas

### Layer 4: Modeled and Probabilistic Data
- Conversion modeling (Meta, Google) para preencher gaps
- Marketing Mix Modeling (MMM) para medir impacto sem user-level data
- Geo-based incrementality tests como alternativa a user-level attribution
- Aggregated Event Measurement (AEM) para priorizar eventos

## Decision Matrix
| Situacao | Abordagem Recomendada |
|----------|----------------------|
| Retargeting pool < 1000 | Broad + creative segmentation |
| Ecommerce com catalogo | Advantage+ Shopping com CAPI |
| B2B com CRM robusto | Customer Match + RLSA |
| Brand awareness | Contextual + broad com video |
| Lead gen sem CAPI | Priorizar implementacao de CAPI imediatamente |

## Checklist de Implementacao
- [ ] CAPI / Enhanced Conversions implementado e validado
- [ ] Consent management platform (CMP) ativo e compliant
- [ ] First-party data collection strategy definida
- [ ] Customer Match audiences atualizados (weekly sync)
- [ ] Evento prioritario definido no Aggregated Event Measurement
- [ ] Creative strategy adaptada para broad targeting (creative = targeting)
- [ ] Conversion modeling ativado nas plataformas

## Key Concepts
- No mundo privacy-first, **creative e o novo targeting** — quem ve o ad se auto-seleciona pelo messaging
- First-party data e o ativo mais valioso — invista em coleta com consentimento
- Broad targeting com bom creative frequentemente supera targeting granular com creative mediano
- Server-side tracking (CAPI) e obrigatorio, nao opcional

## Integration
- Feeds into: Attribution Model, Audience Strategy, Campaign Structure
- Receives from: Tracking Stack, Consent Management, CRM Data
- Pairs with: First-Party Data Activation Framework, Creative Velocity System

## Output
- Privacy-first targeting playbook para o account
- CAPI implementation checklist e validation report
- Audience migration plan (de third-party para first-party)
- Consent rate monitoring dashboard
