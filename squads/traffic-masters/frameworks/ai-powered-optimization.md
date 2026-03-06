# AI-Powered Campaign Optimization
> **Type**: Optimization Framework
> **Used by agents**: Media Buyer, Performance Analyst, Traffic Chief

## Overview
Framework para usar AI e machine learning como pilares de otimizacao de campanhas. Cobre desde ferramentas nativas das plataformas (Smart Bidding, Advantage+) ate automacoes custom e uso de LLMs para creative e analise. O principio central: AI amplifica o media buyer, nao substitui.

## When to Use
- Otimizacao de campanhas em qualquer plataforma com ML nativo
- Decisoes de bidding strategy e budget allocation
- Geracao e iteracao de creative em escala
- Analise de dados e identificacao de patterns

## The Framework

### Layer 1: Platform-Native AI (Usar como default)

#### Google Ads
- **Smart Bidding:** Target CPA, Target ROAS, Maximize Conversions com value
- **Performance Max:** Campanha unificada com AI alocando budget entre canais
- **Responsive Search Ads:** ML combina headlines e descriptions automaticamente
- **Broad Match + Smart Bidding:** Combinacao que desbloqueia query expansion com safety net

#### Meta Ads
- **Advantage+ Shopping:** AI otimiza targeting, placement e creative delivery
- **Advantage+ Audience:** Expande audiences automaticamente alem dos signals
- **Advantage+ Creative:** Auto-ajusta aspect ratio, brightness, text placement
- **Campaign Budget Optimization (CBO):** Distribui budget entre ad sets por performance

#### TikTok Ads
- **Smart Performance Campaign:** Similar a Performance Max — minima intervencao manual
- **Automated Creative Optimization (ACO):** Combina elementos criativos automaticamente

### Layer 2: AI para Creative Production
- **LLMs (ChatGPT, Claude):** Geracao de copy variations, hooks, angles em volume
- **Image AI (Midjourney, DALL-E):** Conceitos visuais e mockups rapidos
- **Video AI (Runway, Pika):** Prototipagem de video ads antes da producao final
- **Workflow:** AI gera V1 -> humano refina -> teste A/B valida

### Layer 3: AI para Analise e Insights
- **Anomaly detection:** Alertas automaticos para mudancas significativas em KPIs
- **Pattern recognition:** Identificar combinacoes de targeting + creative + timing que performam
- **Forecasting:** Projecao de performance baseada em dados historicos
- **Natural language queries:** Perguntar ao dashboard em linguagem natural

### Layer 4: Custom Automation
- **Rules-based automation:** If CPA > threshold por 3 dias -> pause ad set
- **Script automation:** Google Ads Scripts para bid adjustments, budget pacing, alerts
- **API integrations:** Conectar plataformas com BI tools para decisoes automatizadas
- **N8n/Zapier flows:** Alertas no Slack, reports automaticos, creative requests

## Principios de AI Optimization

### 1. Feed the Algorithm
- Mais dados = melhor otimizacao. Consolide campanhas para volume de conversoes
- Minimo 50 conversoes/semana por campaign para Smart Bidding funcionar bem
- CAPI + pixel tracking combinados dao mais sinal ao ML

### 2. Guardrails, Not Micromanagement
- Defina limites (max CPA, min ROAS) mas deixe o AI operar dentro deles
- Evite mudancas frequentes — cada mudanca reseta o learning period
- Budget changes de no maximo 20% por vez

### 3. Creative e o Input Mais Importante
- AI de otimizacao so pode otimizar o que voce da a ela
- Mais criativos de qualidade = mais opcoes para o algoritmo = melhor performance
- AI nao conserta creative ruim — garbage in, garbage out

### 4. Human-in-the-Loop
- AI otimiza taticas; humanos definem estrategia
- Review semanal de o que o AI esta fazendo (audience shifts, placement allocation)
- Override quando o AI otimiza para metrica errada (ex: clicks vs conversions)

## Anti-Patterns (O Que Evitar)
| Anti-Pattern | Problema | Solucao |
|-------------|----------|---------|
| Mudar bids diariamente | Reset constante de learning | Aguardar 7 dias entre mudancas |
| Muitas campanhas com pouco budget | Dados insuficientes para ML | Consolidar em menos campanhas |
| Confiar em AI sem tracking correto | Otimiza para dados errados | Validar tracking antes de ativar AI |
| Ignorar creative refresh | AI fatiga o melhor creative | Pipeline de novos criativos semanal |

## Integration
- Feeds into: Budget Allocation, Creative Strategy, Reporting
- Receives from: Tracking Stack, Creative Pipeline, Business Goals
- Pairs with: Creative Velocity System, Value-Based Bidding Framework

## Output
- AI optimization playbook por plataforma
- Automation rules documentation
- Weekly AI performance review template
- Creative pipeline requirements para alimentar AI
