# Dayparting Optimization

> **Type**: Task
> **Category**: optimization
> **Agents**: Traffic Chief, Kusmich, Deiss
> **Frameworks**: Time-Based Optimization Framework, Budget Efficiency Model
> **Checklists**: optimization-checklist, dayparting-checklist
> **Output template**: templates/optimization-report-document.md

## ROUTING

> **Agents**: media-buyer, performance-analyst
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Otimizar o agendamento de anúncios (ad scheduling) e dayparting para concentrar a entrega de ads nos horários e dias com melhor custo por resultado, reduzindo desperdício em períodos de baixa performance.

## Inputs
- Relatórios de performance por hora do dia e dia da semana (últimos 30-60 dias)
- Dados de conversão com timestamp para análise de padrões temporais
- Google Analytics time-of-day reports
- Dados de CPC, CPM, CPA e conversion rate por hora e dia
- Fusos horários dos mercados ativos
- Horários de funcionamento do time de vendas (se aplicável para leads)

## Steps
1. Extrair relatórios de performance por hora do dia (0-23h) e dia da semana (Dom-Sáb) de todas as plataformas
2. Criar heatmap de CPA/ROAS por hora x dia da semana para visualizar padrões
3. Identificar as golden hours: horários com CPA abaixo da média e volume de conversão significativo
4. Identificar os dead zones: horários com CPA >40% acima da média consistentemente
5. Analisar se os padrões variam entre plataformas, campanhas e tipos de audiência
6. Considerar o horário de operação do time de vendas para campanhas de lead gen (resposta rápida)
7. Configurar ad scheduling no Google Ads com bid adjustments por hora e dia
8. Implementar regras automatizadas no Meta Ads para pausar/ativar por horário (via Rules)
9. Testar dayparting vs. delivery always-on em um experiment controlado
10. Ajustar os bid modifiers gradualmente (máximo 20% por iteração)
11. Monitorar o impacto no delivery volume total (dayparting pode limitar o reach)
12. Documentar o schedule otimizado e criar processo de revisão mensal

## Output
Relatório de dayparting optimization contendo: heatmap de performance por hora/dia, golden hours e dead zones identificados, configurações de ad scheduling aplicadas, e impacto projetado em CPA/ROAS.

## Quality Gate
- Mínimo de 30 dias de dados analisados para relevância estatística
- Heatmap validado com dados de pelo menos 2 fontes (platform + analytics)
- Dead zones com volume suficiente de dados para conclusão estatística
- Experiment de dayparting vs. always-on rodado por pelo menos 2 semanas
- Traffic Chief valida o schedule antes da implementação definitiva

## Duration
3-4 horas para análise e configuração; 2 semanas para teste e validação
