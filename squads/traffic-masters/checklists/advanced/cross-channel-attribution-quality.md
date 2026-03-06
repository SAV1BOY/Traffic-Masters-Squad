# Cross-Channel Attribution Quality
> **Type**: Quality Gate
> **Domain**: Advanced — Measurement
> **Reviewed by**: Data Analyst / Media Lead

## Purpose
Garante que o modelo de atribuicao cross-channel esteja configurado corretamente, produzindo uma visao unificada e confiavel da contribuicao de cada canal na jornada de conversao, evitando double-counting e decisoes baseadas em dados enviesados.

## Checklist

### Modelo de Atribuicao
- [ ] Modelo de atribuicao selecionado com justificativa documentada (last click, linear, time decay, data-driven, custom)
- [ ] Mesmo modelo aplicado consistentemente em todos os reports e dashboards
- [ ] Lookback window definida e padronizada entre canais (7d click, 1d view, etc.)
- [ ] Limitacoes do modelo escolhido documentadas e comunicadas aos stakeholders
- [ ] Modelo revisado periodicamente conforme evolucao da estrategia

### Coleta de Dados
- [ ] UTM parameters padronizados e implementados em todos os canais pagos
- [ ] Tracking server-side (CAPI) configurado nas plataformas que suportam
- [ ] Google Analytics 4 configurado como hub central de atribuicao
- [ ] Eventos de conversao identicos configurados em todas as plataformas
- [ ] User ID ou cross-device tracking implementado quando possivel
- [ ] Consent mode configurado para respeitar preferencias de privacidade

### Reconciliacao de Dados
- [ ] Conversoes de cada plataforma comparadas com fonte de verdade (GA4, CRM, backend)
- [ ] Discrepancias entre plataformas documentadas e explicadas
- [ ] Double-counting identificado e corrigido (conversoes atribuidas a multiplos canais)
- [ ] Organic vs paid claramente separados na atribuicao
- [ ] Direct/none traffic investigado e reclassificado quando possivel

### Dashboards e Reporting
- [ ] Dashboard unificado cross-channel criado e funcional
- [ ] Metricas padronizadas entre canais (CPA, ROAS, CPL usando mesma fonte)
- [ ] Contribution report mostra share de cada canal por etapa do funnel
- [ ] Assisted conversions rastreadas alem de last-click conversions
- [ ] Path analysis configurado para entender jornadas multi-touch

### Validacao e Calibracao
- [ ] Atribuicao cross-channel comparada com resultados de incrementality tests
- [ ] Resultados de MMM usados para calibrar a atribuicao digital
- [ ] Consistencia entre atribuicao reportada e resultados de negocio validada
- [ ] Anomalias investigadas (ex: um canal com atribuicao desproporcional)
- [ ] Stakeholders treinados para interpretar corretamente os reports de atribuicao

## Pass/Fail Criteria
Todos os itens de coleta de dados e reconciliacao devem ser validados. Reports so devem ser compartilhados apos reconciliacao completa entre fontes. O modelo de atribuicao deve ser revisado a cada trimestre.

## If Failed
Nao tomar decisoes de realocacao de budget com base em dados nao reconciliados. Corrigir tracking e reconciliar dados antes de gerar reports cross-channel.

## Related
- `incrementality-test-quality.md`
- `media-mix-model-quality.md`
- `../tracking-plan-quality.md`
