# New Market Testing

> **Type**: Task
> **Category**: scaling
> **Agents**: Traffic Chief, Deiss, Mandalia
> **Frameworks**: Market Testing Protocol, Deiss Customer Value Journey, Geo-Testing Framework
> **Checklists**: scaling-checklist, market-testing-checklist
> **Output template**: templates/scaling-report-document.md

## ROUTING

> **Agents**: scale-optimizer, traffic-chief
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Testar novos mercados geográficos com budgets controlados, validando a viabilidade de expansão antes de alocar investimento significativo, seguindo um protocolo estruturado de teste.

## Inputs
- Geo expansion strategy aprovada com mercados priorizados
- Budget de teste aprovado (5-10% do budget total)
- Criativos adaptados para os mercados-alvo
- Landing pages localizadas (se necessário)
- Benchmarks de performance dos mercados existentes
- Critérios de go/no-go definidos na estratégia de expansão

## Steps
1. Selecionar os mercados Tier 1 para o primeiro ciclo de testes (máximo 3 mercados simultâneos)
2. Calcular o budget mínimo por mercado para atingir significância estatística (mínimo 50 conversões)
3. Adaptar criativos e copy para relevância local (referências regionais, moeda, idioma)
4. Criar campanhas isoladas por mercado para atribuição limpa (não misturar com mercados existentes)
5. Replicar a estrutura de campanha que funciona nos mercados existentes como baseline
6. Configurar tracking dedicado para isolar os dados de cada novo mercado
7. Lançar com bid strategy conservadora (manual ou maximize conversions sem target CPA)
8. Monitorar diariamente nas primeiras 2 semanas: CPC, CTR, CVR, CPA
9. Comparar performance do novo mercado vs. mercados existentes usando os mesmos KPIs
10. Aplicar os critérios de go/no-go ao final do período de teste (3-4 semanas)
11. Para mercados aprovados: criar plano de scaling com budget progressivo
12. Para mercados reprovados: documentar learnings e reavaliar em 3-6 meses

## Output
Relatório de market testing contendo: resultados por mercado testado, comparativo vs. mercados existentes, decisão go/no-go fundamentada, plano de scaling para mercados aprovados, e learnings dos mercados reprovados.

## Quality Gate
- Cada mercado testado por mínimo de 3 semanas com budget suficiente
- Mínimo de 50 conversões por mercado para significância estatística
- Critérios de go/no-go aplicados objetivamente (CPA ceiling, ROAS floor, volume mínimo)
- Mercados testados de forma isolada sem contaminar dados dos mercados existentes
- Traffic Chief aprova as decisões de go/no-go e os planos de scaling

## Duration
1-2 horas para setup por mercado; 3-4 semanas para ciclo de teste; 2 horas para análise e documentação
