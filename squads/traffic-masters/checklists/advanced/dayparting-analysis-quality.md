# Dayparting/Scheduling Optimization Quality
> **Type**: Quality Gate
> **Domain**: Advanced — Optimization
> **Reviewed by**: Media Buyer / Data Analyst

## Purpose
Garante que analises de dayparting e ajustes de scheduling sejam baseados em dados robustos e implementados corretamente, maximizando a eficiencia do budget ao longo do dia e da semana.

## Checklist

### Coleta e Analise de Dados
- [ ] Dados de performance por hora do dia coletados (minimo 30 dias)
- [ ] Dados de performance por dia da semana coletados
- [ ] Volume de conversoes por periodo suficiente para significancia estatistica
- [ ] Metricas analisadas incluem CPA, ROAS, CVR e volume (nao apenas CTR)
- [ ] Dados segmentados por campanha, plataforma e tipo de audiencia
- [ ] Efeitos de timezone considerados (usuario vs conta)

### Identificacao de Padroes
- [ ] Horarios de pico de conversao identificados com confianca estatistica
- [ ] Horarios de baixa performance identificados
- [ ] Padroes de dia da semana mapeados (ex: B2B mais forte em dias uteis)
- [ ] Diferencas de padrao entre plataformas documentadas
- [ ] Sazonalidades e outliers removidos da analise base
- [ ] Padroes comparados com dados de Google Analytics (sessoes, bounce rate)

### Implementacao de Schedule
- [ ] Ad scheduling configurado conforme analise na plataforma
- [ ] Bid adjustments por horario aplicados com valores justificados
- [ ] Bid adjustments por dia da semana configurados quando relevante
- [ ] Budget distribution ajustada para priorizar periodos de melhor performance
- [ ] Periodos de blackout (zero delivery) configurados apenas com justificativa forte

### Validacao e Monitoramento
- [ ] Performance pos-implementacao monitorada por pelo menos 2 semanas
- [ ] Comparacao before/after com mesmas metricas da analise original
- [ ] Impacto no volume total de conversoes avaliado (trade-off eficiencia vs escala)
- [ ] Ajustes de schedule nao estao limitando excessivamente o delivery
- [ ] Re-analise agendada para validar que os padroes se mantem (mensal)

### Documentacao
- [ ] Analise de dayparting documentada com dados, graficos e conclusoes
- [ ] Bid adjustments aplicados registrados com rationale
- [ ] Schedule configurado por campanha documentado
- [ ] Resultado da validacao pos-implementacao registrado

## Pass/Fail Criteria
Todos os itens de coleta de dados e identificacao de padroes devem ser completados antes da implementacao. Ajustes de schedule so sao validos se baseados em dados com significancia estatistica.

## If Failed
Reverter ajustes de schedule para configuracao anterior. Coletar mais dados antes de tentar novamente. Nao aplicar dayparting com menos de 30 dias de dados.

## Related
- `geo-targeting-quality.md`
- `../budget-pacing-quality.md`
- `incrementality-test-quality.md`
