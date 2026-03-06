# Incrementality Testing
> **Type**: Testing Framework
> **Used by agents**: Performance Analyst, Traffic Chief, Data Analyst

## Overview
Framework para planejar e executar testes de incrementalidade que respondem a pergunta mais importante em paid media: "Esta conversao teria acontecido sem o ad?" Cobre geo tests, holdout tests, e platform-native lift studies com metodologia rigorosa.

## When to Use
- Validar o valor real de um canal com spend significativo
- Quando platform-reported ROAS parece "bom demais pra ser verdade"
- Antes de decisoes de budget allocation que movem 20%+ do spend
- Trimestralmente como disciplina de measurement

## The Framework

### Por Que Incrementality Importa
- Attribution diz QUEM tocou a conversao. Incrementality diz SE o ad CAUSOU a conversao.
- Sem incrementality testing, voce pode estar pagando por conversoes que aconteceriam organicamente
- Estudo Meta: em media, 20-40% das conversoes atribuidas a paid NAO sao incrementais

### Tipos de Teste

#### 1. Geo Lift Test (Recomendado)
- **Como funciona:** Selecionar regioes similares. Ligar ads em grupo teste, desligar no controle.
- **Duracao:** 2-4 semanas minimo (mais para ciclos de venda longos)
- **Vantagem:** Nao depende de tracking user-level — funciona pos-iOS 14.5
- **Desvantagem:** Requer volume suficiente por geo; contaminacao de spill-over
- **Ferramentas:** GeoLift (Meta open-source), CausalImpact (Google)

#### 2. Holdout / Ghost Ads Test
- **Como funciona:** Grupo controle veria o ad mas nao recebe. Comparar conversion rates.
- **Duracao:** 2-4 semanas
- **Vantagem:** Controle mais preciso que geo test
- **Desvantagem:** Requer integracao tecnica; nem toda plataforma suporta nativamente

#### 3. Platform Conversion Lift Study
- **Meta Conversion Lift:** Teste nativo que cria holdout group automaticamente
- **Google Brand/Conversion Lift:** Estudo nativo para medir incremento
- **Vantagem:** Facil de implementar, sem setup tecnico complexo
- **Desvantagem:** A plataforma testa a si mesma — potencial bias

#### 4. Budget On/Off Test (Simples)
- **Como funciona:** Desligar completamente um canal por 2 semanas. Observar impacto no revenue total.
- **Vantagem:** Extremamente simples de executar
- **Desvantagem:** Risco de perda de dados de learning; nao isola variaveis
- **Quando usar:** Channels com spend menor (<15% do total)

### Metodologia Step-by-Step

#### Passo 1: Definir Hipotese
- "Canal X gera [Y]% de incremento em conversoes vs baseline organico"
- Ser especifico sobre a metrica e o threshold de sucesso

#### Passo 2: Design do Teste
- Selecionar tipo de teste baseado na situacao
- Definir grupo teste e grupo controle (minimo 90% match em caracteristicas)
- Calcular sample size necessario para significancia estatistica (p < 0.05)
- Definir duracao minima baseada no conversion cycle

#### Passo 3: Execucao
- Documentar TUDO — settings, datas, budget, external factors
- Nao fazer outras mudancas durante o teste (creative, landing page, preco)
- Monitorar diariamente para anomalias (sem intervir nos resultados)

#### Passo 4: Analise
- **Incremental Lift** = (Conversoes Teste - Conversoes Controle) / Conversoes Controle
- **iROAS** = Receita Incremental / Spend durante o teste
- **Significancia:** p-value < 0.05 para confianca
- Comparar iROAS com platform-reported ROAS — a diferença e o "inflation factor"

#### Passo 5: Decisao
| Resultado | Acao |
|-----------|------|
| iROAS > Target | Manter ou aumentar budget |
| iROAS positivo mas < Target | Otimizar antes de escalar |
| iROAS ~0 | Canal nao e incremental — realocar budget |
| iROAS negativo | Desligar canal imediatamente |

## Common Pitfalls
- Teste muito curto (< 2 semanas) — dados insuficientes
- Contaminacao entre grupos (geo overlap, cross-device)
- Fazer mudancas durante o teste — invalida resultados
- Testar canal de baixo spend — sem volume para significancia

## Integration
- Feeds into: Budget Allocation, Channel Strategy, Attribution Calibration
- Receives from: Revenue Data, Platform Data, Geo Data
- Pairs with: Attribution and Incrementality, Cross-Channel Measurement

## Output
- Incrementality test plan document
- Test results report com iROAS e significancia
- Platform ROAS vs iROAS comparison
- Budget reallocation recommendation baseada em resultados
