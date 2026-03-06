# Incrementality Test Design and Execution Quality
> **Type**: Quality Gate
> **Domain**: Advanced — Measurement
> **Reviewed by**: Data Analyst / Media Lead

## Purpose
Garante que testes de incrementalidade sejam desenhados e executados com rigor metodologico, produzindo resultados confiaveis para decisoes de alocacao de budget e avaliacao de impacto real das campanhas.

## Checklist

### Design do Teste
- [ ] Hipotese do teste claramente definida e documentada
- [ ] Metrica primaria de sucesso definida (incremental conversions, incremental revenue, iROAS)
- [ ] Tipo de teste selecionado com justificativa (geo-split, ghost ads, PSA holdout, conversion lift)
- [ ] Grupos de controle e tratamento definidos com criterios claros
- [ ] Tamanho amostral calculado para significancia estatistica (power analysis)
- [ ] Duracao do teste definida com base no volume de conversoes esperado

### Configuracao Tecnica
- [ ] Grupos de teste configurados na plataforma corretamente
- [ ] Randomizacao dos grupos validada (sem vies de selecao)
- [ ] Holdout configurado com porcentagem adequada (tipicamente 10-20%)
- [ ] Tracking diferenciado entre controle e tratamento funcionando
- [ ] Contaminacao cruzada entre grupos prevenida

### Execucao e Monitoramento
- [ ] Teste lancado conforme cronograma sem alteracoes nas campanhas durante o periodo
- [ ] Monitoramento diario para identificar anomalias ou quebras no setup
- [ ] Nenhuma otimizacao ou mudanca de budget feita durante o teste (lock period)
- [ ] Fatores externos (sazonalidade, promocoes, competidores) documentados
- [ ] Dados coletados na granularidade necessaria para analise

### Analise de Resultados
- [ ] Significancia estatistica alcancada antes de tirar conclusoes
- [ ] Incremental lift calculado com intervalo de confianca
- [ ] iROAS (incremental ROAS) calculado quando aplicavel
- [ ] Resultados segmentados por variaveis relevantes (plataforma, audiencia, geo)
- [ ] Fatores confundidores identificados e controlados na analise
- [ ] Resultados comparados com benchmarks historicos e expectativas

### Documentacao e Acao
- [ ] Relatorio de resultados documentado com metodologia, dados e conclusoes
- [ ] Recomendacoes de budget reallocation baseadas nos resultados
- [ ] Proximo teste planejado com base nos aprendizados
- [ ] Resultados compartilhados com stakeholders relevantes

## Pass/Fail Criteria
Todos os itens de design e configuracao tecnica devem ser validados antes do lancamento do teste. Resultados so sao considerados validos se significancia estatistica for alcancada.

## If Failed
Nao tomar decisoes de budget com base em testes inconclusivos. Redesenhar o teste corrigindo os problemas identificados e re-executar.

## Related
- `media-mix-model-quality.md`
- `cross-channel-attribution-quality.md`
- `../budget-pacing-quality.md`
