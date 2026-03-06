# Media Mix Modeling Quality Gate
> **Type**: Quality Gate
> **Domain**: Advanced — Measurement
> **Reviewed by**: Data Analyst / Media Lead

## Purpose
Garante que modelos de media mix (MMM) sejam construidos com dados de qualidade, metodologia solida e produzam outputs confiaveis para decisoes de alocacao de budget entre canais.

## Checklist

### Coleta e Preparacao de Dados
- [ ] Dados de investimento por canal coletados com granularidade adequada (diaria ou semanal)
- [ ] Dados de receita/conversoes coletados da mesma fonte e periodo
- [ ] Minimo de 2 anos de dados historicos disponivel (ideal: 3 anos)
- [ ] Variaveis externas coletadas (sazonalidade, feriados, promocoes, preco, competidores)
- [ ] Dados limpos — outliers identificados e tratados com justificativa
- [ ] Consistencia temporal validada (sem gaps ou mudancas de definicao)

### Modelagem
- [ ] Variavel dependente definida corretamente (vendas, receita, leads)
- [ ] Transformacoes de adstock aplicadas (carry-over effect) com decay rates justificados
- [ ] Curvas de saturacao (diminishing returns) modeladas por canal
- [ ] Multicolinearidade entre canais avaliada e tratada
- [ ] Baseline (vendas organicas) separado do impacto incremental de midia
- [ ] Variaveis de controle incluidas (sazonalidade, trend, preco, macro-economia)

### Validacao do Modelo
- [ ] R-squared e MAPE dentro de ranges aceitaveis
- [ ] Coeficientes de cada canal tem sinal e magnitude plausivel
- [ ] Out-of-sample validation realizada (holdout period)
- [ ] Comparacao com resultados de incrementality tests quando disponivel
- [ ] Sensibilidade do modelo a mudancas nos inputs avaliada
- [ ] Modelo revisado por um segundo analista

### Outputs e Recomendacoes
- [ ] ROI por canal calculado com intervalos de confianca
- [ ] Curvas de resposta por canal geradas para orientar budget allocation
- [ ] Cenarios de otimizacao de budget simulados (what-if analysis)
- [ ] Recomendacoes praticas de realocacao de budget documentadas
- [ ] Limitacoes do modelo explicitamente documentadas

### Governanca e Atualizacao
- [ ] Modelo documentado com metodologia, premissas e fontes de dados
- [ ] Frequencia de refresh do modelo definida (trimestral, semestral)
- [ ] Processo de incorporacao de novos canais documentado
- [ ] Stakeholders alinhados sobre como interpretar e usar os outputs

## Pass/Fail Criteria
Todos os itens de coleta de dados e validacao do modelo devem ser aprovados. Outputs nao podem ser usados para decisoes de budget sem validacao completa.

## If Failed
Identificar gaps nos dados ou na modelagem, corrigir e re-treinar o modelo. Nao tomar decisoes de realocacao de budget com base em modelos nao validados.

## Related
- `incrementality-test-quality.md`
- `cross-channel-attribution-quality.md`
- `../budget-pacing-quality.md`
