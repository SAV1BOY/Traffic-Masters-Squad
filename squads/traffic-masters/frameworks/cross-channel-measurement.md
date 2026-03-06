# Cross-Channel Measurement and MMM
> **Type**: Measurement Framework
> **Used by agents**: Performance Analyst, Traffic Chief, Data Analyst

## Overview
Framework para medir o impacto real de cada canal de marketing quando dados user-level estao incompletos. Combina Marketing Mix Modeling (MMM), MER analysis, e testes de incrementalidade para criar uma visao holistica de performance que nao depende de attribution de plataforma.

## When to Use
- Budget allocation entre 3+ canais de midia paga
- Quando a soma de conversoes por plataforma excede total real em 30%+
- Decisoes estrategicas de investimento por canal
- Avaliacao de canais upper-funnel (TV, YouTube, podcasts) que nao tem last-click

## The Framework

### O Problema da Medicao Fragmentada
- Cada plataforma reporta conversoes independentemente
- Meta diz: "Geramos 500 vendas". Google diz: "Geramos 450 vendas". Total real: 600 vendas.
- Overlap de 58% — quase metade das conversoes sao contadas duas vezes
- Decisao baseada em dados de plataforma = budget mal alocado

### Nivel 1: MER (Marketing Efficiency Ratio)
- **Formula:** MER = Total Revenue / Total Marketing Spend
- **Uso:** Metrica estrategica principal para health check geral
- **Vantagem:** Simples, impossivel de inflar, captura todo o funnel
- **Limitacao:** Nao diz QUAL canal esta performando — apenas se o MIX funciona

### Nivel 2: Marginal MER por Canal
- **Metodo:** Alterar spend em UM canal por vez e observar impacto no MER
- **Exemplo:** Aumenta Meta em 20% -> MER total cai de 3.2x para 2.8x -> Meta tem retorno marginal decrescente
- **Timing:** Mudancas de 2 semanas minimo para isolar impacto
- **Limitacao:** Lento, uma variavel por vez, nao escala

### Nivel 3: Marketing Mix Modeling (MMM)
- **O que e:** Modelo estatistico que correlaciona spend por canal com revenue total
- **Inputs:** Spend diario por canal, revenue diario, seasonality, promotions, external factors
- **Outputs:** Contribuicao de cada canal para revenue, marginal ROI por canal, optimal allocation
- **Ferramentas:** Meta Robyn (open-source), Google Meridian, LightweightMMM
- **Requisitos minimos:** 2+ anos de dados, 3+ canais, variacao suficiente em spend

### Nivel 4: Incrementality Testing
- **Geo lift tests:** Ligar/desligar canal em regioes especificas
- **Holdout tests:** Grupo de controle sem exposicao ao canal
- **Platform lift studies:** Meta Conversion Lift, Google Brand Lift
- **Frequencia:** Trimestral para canais de alto spend; semestral para canais menores

### Stack de Medicao Recomendado
```
          [Decisao Estrategica]
                  |
          [MER Blended] ---- health check semanal
                  |
        [MMM / Robyn] ---- recalibracao mensal
                  |
    [Incrementality Tests] ---- validacao trimestral
                  |
     [Platform Attribution] ---- otimizacao diaria in-platform
```

## Implementacao do MMM

### Passo 1: Coleta de Dados
- Spend diario por canal (minimo 2 anos)
- Revenue diario (total, nao atribuido)
- Variaveis externas: feriados, promocoes, seasonality indexes
- Competidor spend (estimado via SimilarWeb, SEMrush)

### Passo 2: Modelagem
- Escolher ferramenta (Robyn recomendado para equipes com R/Python skills)
- Definir adstock transformations (carryover effect de cada canal)
- Rodar modelo e validar com holdout period

### Passo 3: Leitura dos Resultados
- Contribution share: quanto cada canal contribui para revenue total
- Marginal ROI: proximo R$1 investido em cada canal — qual retorna mais?
- Optimal allocation: como redistribuir budget para maximizar revenue

## Decision Rules
1. Platform ROAS serve para otimizar dentro do canal, nunca para comparar entre canais
2. Se MMM e incrementality test concordam sobre um canal, alta confianca na decisao
3. Se discordam, rodar mais testes antes de mover budget
4. MER semanal e o early warning system — se cai, investigar imediatamente
5. Canais com alto contribution mas baixo marginal ROI = saturados

## Integration
- Feeds into: Budget Allocation, Channel Strategy, Forecasting
- Receives from: Revenue Data, Platform Spend Data, External Factors
- Pairs with: Attribution and Incrementality, Incrementality Testing Framework

## Output
- MER dashboard com trending semanal
- MMM model results e optimal allocation recommendations
- Quarterly incrementality test reports
- Cross-channel contribution waterfall chart
