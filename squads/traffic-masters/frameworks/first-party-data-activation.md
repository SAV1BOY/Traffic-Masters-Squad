# First-Party Data Activation
> **Type**: Data Strategy Framework
> **Used by agents**: Pixel Specialist, Media Buyer, Traffic Chief, CRM Specialist

## Overview
Framework para coletar, organizar e ativar first-party data em campanhas de paid media. Com a erosao de third-party cookies e tracking restrictions, first-party data e o ativo mais valioso de um anunciante. Este framework transforma dados proprios em vantagem competitiva de targeting e otimizacao.

## When to Use
- Estruturacao de estrategia de dados para qualquer account
- Quando retargeting pools estao diminuindo por restricoes de privacidade
- Implementacao de CAPI, Enhanced Conversions, ou Customer Match
- Integracao de CRM data com plataformas de ads

## The Framework

### O Que e First-Party Data
- Dados coletados diretamente do usuario com consentimento
- **Exemplos:** email, telefone, historico de compras, comportamento no site, preferencias declaradas
- **Diferente de:** Third-party data (comprado de data brokers), second-party data (parceiro compartilha)
- **Vantagem:** Mais preciso, compliant, e exclusivo (competidores nao tem acesso)

### Layer 1: Coleta de Dados

#### Pontos de Coleta
| Ponto | Dados Coletados | Valor para Ads |
|-------|----------------|----------------|
| Email signup | Email, nome | Customer Match audiences |
| Purchase | Email, produto, valor, frequencia | Value-based audiences, LTV prediction |
| Quiz/assessment | Preferencias, perfil | Segmentacao por interesse/necessidade |
| Account creation | Dados demograficos, interesses | Lookalike seed de alta qualidade |
| Customer service | Feedback, issues | Churn prediction, win-back triggers |
| Loyalty program | Frequency, tier, pontos | High-value customer identification |

#### Principios de Coleta
1. **Value exchange:** Sempre oferecer algo em troca (desconto, conteudo, utilidade)
2. **Transparencia:** Explicar como os dados serao usados
3. **Consentimento:** LGPD/GDPR compliant — opt-in explicito
4. **Minimalismo:** Coletar apenas o necessario — menos fields = mais completions

### Layer 2: Organizacao e Enriquecimento

#### Data Warehouse / CDP
- Centralizar todos os dados em um unico sistema (BigQuery, Segment, RudderStack)
- Unificar identidade do cliente (email como key identifier cross-platform)
- Calcular metricas derivadas: LTV, RFM score, churn probability

#### Segmentacao
| Segmento | Criterio | Uso em Ads |
|----------|---------|------------|
| High-LTV Customers | Top 20% por revenue lifetime | Lookalike seed, exclusao de prospeccao |
| Recent Purchasers (0-30d) | Comprou nos ultimos 30 dias | Upsell/cross-sell, excluir de aquisicao |
| At-Risk Customers | Nao comprou em 60-90d | Win-back campaigns |
| Engaged Non-Buyers | Alta interacao, zero compras | Conversion-focused campaigns |
| VIP / Advocates | 5+ compras ou referrals ativos | Referral campaigns, UGC requests |

### Layer 3: Ativacao em Plataformas

#### Meta Ads
- **Custom Audiences:** Upload de listas (email/phone) para remarketing direto
- **Lookalike Audiences:** Criar lookalikes de segmentos high-value (1%, 2%, 5%)
- **Conversions API (CAPI):** Enviar eventos server-side com dados de cliente hashados
- **Advantage+ Audience Signals:** Usar listas como signals para targeting amplo

#### Google Ads
- **Customer Match:** Upload de listas para Search, Shopping, YouTube, Gmail
- **Enhanced Conversions:** Enviar dados hashados para melhorar match rate
- **RLSA:** Ajustar bids para usuarios conhecidos em Search
- **Similar Audiences:** (Deprecated) Substituido por Audience Signals em PMax

#### TikTok / Other Platforms
- **Custom Audiences:** Upload via hashed email/phone
- **Events API:** Equivalent ao CAPI para envio server-side

### Layer 4: Medicao e Iteracao
- Monitorar match rates (% de emails que matcham com usuarios da plataforma)
- Comparar performance de first-party audiences vs broad targeting
- A/B test: campanha com first-party signals vs campanha sem
- Atualizar listas automaticamente (sync semanal minimo)

## Match Rate Benchmarks
| Plataforma | Match Rate Esperado | Como Melhorar |
|-----------|--------------------|--------------|
| Meta | 50-70% | Enviar email + phone + nome |
| Google | 40-60% | Enhanced Conversions + Customer Match |
| TikTok | 30-50% | Email + phone combinados |

## Integration
- Feeds into: Audience Strategy, Targeting, Value-Based Bidding, Lookalike Creation
- Receives from: CRM, E-commerce Platform, CDP, Email Tool
- Pairs with: Privacy-First Targeting, Audience Lifecycle Management

## Output
- First-party data collection strategy document
- Data flow architecture (sources -> warehouse -> platforms)
- Audience segment definitions e refresh schedule
- Match rate monitoring dashboard
- CAPI / Enhanced Conversions implementation checklist
