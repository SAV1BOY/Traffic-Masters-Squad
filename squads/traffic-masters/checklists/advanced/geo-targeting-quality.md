# Geographic Targeting and Bid Adjustments Quality
> **Type**: Quality Gate
> **Domain**: Advanced — Targeting
> **Reviewed by**: Media Buyer / Data Analyst

## Purpose
Garante que o targeting geografico e os bid adjustments por localizacao estejam configurados com precisao, baseados em dados de performance, e alinhados com a estrategia de negocio do cliente.

## Checklist

### Analise de Dados Geograficos
- [ ] Performance por regiao/estado/cidade analisada com dados de pelo menos 30 dias
- [ ] Metricas por geo incluem CPA, ROAS, CVR e volume de conversoes
- [ ] Dados cruzados com informacoes de negocio (areas de atuacao, shipping, estoque)
- [ ] Geo-performance comparada entre plataformas para consistencia
- [ ] Volume minimo de conversoes por geo garantido para significancia estatistica
- [ ] Diferenca de custo de midia (CPM) por regiao mapeada

### Configuracao de Targeting
- [ ] Geo-targeting configurado no nivel correto (pais, estado, cidade, raio, CEP)
- [ ] Opcao de targeting correta selecionada (people IN this location vs people INTERESTED in)
- [ ] Areas de exclusao geografica configuradas quando necessario
- [ ] Radius targeting configurado com precisao para negocios locais
- [ ] Geos de teste separados em ad sets dedicados quando necessario

### Bid Adjustments
- [ ] Bid adjustments por geo baseados em dados de performance reais
- [ ] Adjustments calculados com formula documentada (ex: target CPA / geo CPA)
- [ ] Range de bid adjustments razoavel (evitar extremos como +300% ou -90%)
- [ ] Bid adjustments nao estao limitando volume excessivamente em geos importantes
- [ ] Adjustments revisados e atualizados na frequencia definida (quinzenal ou mensal)

### Alinhamento Estrategico
- [ ] Targeting geografico alinhado com areas de atuacao e logistica do cliente
- [ ] Prioridades de expansao geografica refletidas na configuracao
- [ ] Campanhas locais com creative e copy adaptados por regiao
- [ ] Promocoes ou ofertas regionais refletidas no targeting
- [ ] Budget alocado proporcionalmente ao potencial de cada regiao

### Monitoramento e Validacao
- [ ] Dashboard de performance por geo configurado e atualizado
- [ ] Alertas para anomalias de performance geografica configurados
- [ ] Impacto dos bid adjustments monitorado apos implementacao
- [ ] Re-analise agendada para atualizar adjustments (mensal)
- [ ] Geos com baixa performance em monitoramento para possivel exclusao

## Pass/Fail Criteria
Todos os itens de configuracao de targeting e alinhamento estrategico devem ser aprovados. Bid adjustments so devem ser aplicados com base em dados estatisticamente significativos.

## If Failed
Reverter bid adjustments para valores neutros. Corrigir configuracoes de targeting e re-validar antes de reativar. Geos incorretos podem causar desperdicio significativo de budget.

## Related
- `dayparting-analysis-quality.md`
- `audience-suppression-quality.md`
- `../campaign-build-quality.md`
