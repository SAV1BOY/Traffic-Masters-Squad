# Budget Graduation

> **Type**: Task
> **Category**: scaling
> **Agents**: Traffic Chief, Deiss, Kusmich
> **Frameworks**: Graduation Testing Framework, Budget Scaling Protocol, Deiss Customer Value Journey
> **Checklists**: scaling-checklist, budget-graduation-checklist
> **Output template**: templates/scaling-report-document.md

## Objective
Graduar budgets de campanhas do estágio de teste para o estágio de scale seguindo o Graduation Testing framework, garantindo que apenas campanhas validadas recebem investimento incremental.

## Inputs
- Campanhas em estágio de teste com pelo menos 2-4 semanas de dados
- KPIs de graduation definidos (CPA target, ROAS minimum, CVR threshold)
- Budget total disponível para scaling
- Dados de performance segmentados por campanha, ad set e criativo
- Histórico de scaling anterior e seus resultados

## Steps
1. Definir os critérios de graduation claros: CPA ≤ target por X dias consecutivos, ROAS ≥ minimum, CVR ≥ threshold
2. Auditar todas as campanhas em teste e classificar: Ready to Graduate, Needs More Data, Kill
3. Para campanhas "Kill": pausar e documentar os learnings para futuras iterações
4. Para campanhas "Ready to Graduate": iniciar o processo de budget increase controlado
5. Aplicar a regra do 20%: aumentar budget em no máximo 20% a cada 3-4 dias
6. Monitorar o CPA/ROAS após cada incremento de budget (não deixar sair do target por >48h)
7. Se o CPA subir >20% após incremento: pausar o aumento e estabilizar por 5-7 dias
8. Implementar automated rules para alertar quando métricas saírem dos guardrails
9. Atingindo o budget target: manter e monitorar estabilidade por 2 semanas
10. Documentar a curva de scaling de cada campanha (budget x CPA ao longo do tempo)
11. Criar o budget allocation final entre campanhas graduadas
12. Estabelecer o protocolo de manutenção: revisão semanal de performance vs. guardrails

## Output
Relatório de budget graduation contendo: classificação de campanhas (graduate/kill), curva de scaling documentada, budget allocation final, automated rules configuradas, e protocolo de manutenção.

## Quality Gate
- Critérios de graduation objetivos e aplicados consistentemente
- Incrementos de budget não ultrapassando 20% por vez
- CPA/ROAS mantidos dentro dos guardrails durante todo o processo de scaling
- Automated rules ativas para proteção contra deterioração
- Traffic Chief aprova cada fase de graduation e o budget allocation final
- Período de estabilização de 2 semanas validado pós-scaling

## Duration
1-2 horas para auditoria e classificação; 3-6 semanas para o ciclo completo de graduation
