# Value-Based Bidding
> **Type**: Bidding Strategy Framework
> **Used by agents**: Media Buyer, Performance Analyst, Pixel Specialist

## Overview
Framework para implementar value-based bidding (VBB) em plataformas de ads. Em vez de otimizar para volume de conversoes (todos valem o mesmo), VBB otimiza para VALOR de cada conversao. O algoritmo aprende a priorizar usuarios com maior LTV, AOV ou lead quality score.

## When to Use
- Ecommerce com variacao significativa de AOV (>2x entre menor e maior)
- Lead gen onde quality de leads varia muito (SQL rate de 5% a 50%)
- Quando otimizar para CPA traz volume mas nao revenue/profit
- Accounts com dados de conversao downstream (CRM, revenue, LTV)

## The Framework

### Por Que VBB Supera CPA Bidding
- **CPA Bidding:** "Me traga conversoes pelo menor custo" -> algoritmo busca easiest converts
- **VBB:** "Me traga conversoes de MAIOR VALOR" -> algoritmo busca highest-value customers
- **Resultado:** Mesmo spend, revenue 20-50% maior em muitos casos

### Requisitos para VBB
1. **Dados de valor:** Receita por transacao, lead score, ou LTV estimado
2. **Volume:** Minimo 15-30 conversoes com valor por semana (Google); 50+ (Meta)
3. **Tracking:** Conversion value passado corretamente via pixel + CAPI
4. **Variacao:** Os valores precisam ter range significativo (nao todos iguais)

### Implementacao por Plataforma

#### Google Ads — Target ROAS / Maximize Conversion Value
- **Setup:** Passar `conversion_value` no tag/CAPI com valor real da venda ou lead score
- **Bidding:** Target ROAS (define retorno alvo) ou Max Conversion Value (sem target)
- **Ecommerce:** Usar valor do pedido como conversion value
- **Lead Gen:** Atribuir valores por tipo de lead (ex: Demo Request = R$500, Newsletter = R$10)
- **Advanced:** Importar conversoes offline com valores reais de venda fechada

#### Meta Ads — Value Optimization
- **Setup:** Enviar `value` parameter no Purchase event via pixel + CAPI
- **Bidding:** Selecionar "Maximize value of conversions" no campaign objective
- **Minimum ROAS:** Opcional — define floor de retorno (usar com cuidado, pode limitar volume)
- **Lead Gen:** Usar Conversions API para enviar lead score ou deal value do CRM como conversao

#### TikTok Ads — Value-Based Optimization
- **Setup:** Passar `value` no Complete Payment event
- **Bidding:** "Maximum Delivery" com value optimization
- **Nota:** VBO no TikTok requer volume mais alto — consolidar campanhas

### Hierarquia de Valor para Lead Gen
| Evento | Valor Sugerido | Razao |
|--------|---------------|-------|
| Page View | R$0 | Nao usar como conversao |
| Lead Form Submit | R$10-50 | Baseline, ajustar por historico |
| MQL (Marketing Qualified) | R$100-300 | Lead passou criterio minimo |
| SQL (Sales Qualified) | R$500-1000 | Sales aceita trabalhar o lead |
| Opportunity Created | R$1000-3000 | Deal real no pipeline |
| Closed Won | Valor real do deal | Gold standard |

### Ramp-Up Strategy
1. **Semana 1-2:** Lancar com Maximize Conversions (volume) para coletar dados de valor
2. **Semana 3-4:** Migrar para Maximize Conversion Value (sem target ROAS)
3. **Semana 5+:** Adicionar Target ROAS baseado nos resultados das semanas anteriores
4. **Ongoing:** Ajustar target ROAS em incrementos de 10-20% max por semana

## Metricas de Sucesso VBB
| Metrica | O Que Mede | Target |
|---------|-----------|--------|
| Conv. Value / Cost (ROAS) | Retorno por real investido | Acima do break-even + margem |
| Avg. Conversion Value | Valor medio por conversao | Crescendo vs pre-VBB |
| Revenue per Click | Eficiencia de cada click | Crescendo vs pre-VBB |
| Value/Conv. Spread | Distribuicao dos valores | Range amplo = VBB funcionando |

## Common Pitfalls
- Valores todos iguais — algoritmo nao tem o que otimizar
- Valor inflado artificialmente — distorce o modelo de ML
- Target ROAS muito agressivo cedo demais — restringe volume e learning
- Nao importar conversoes offline — algoritmo otimiza para proxy, nao resultado real

## Integration
- Feeds into: Bidding Strategy, Revenue Optimization, Campaign Structure
- Receives from: CRM Data, Transaction Data, Lead Scoring Model
- Pairs with: First-Party Data Activation, AI-Powered Optimization

## Output
- VBB implementation roadmap por plataforma
- Value assignment table para todos os eventos de conversao
- Pre/post VBB performance comparison
- CRM-to-platform data flow documentation
