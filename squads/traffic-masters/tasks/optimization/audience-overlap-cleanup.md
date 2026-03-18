# Audience Overlap Cleanup

> **Type**: Task
> **Category**: optimization
> **Agents**: Kusmich, Traffic Chief, Mandalia
> **Frameworks**: Kusmich Audience Architecture, Audience Hygiene Protocol
> **Checklists**: optimization-checklist, audience-overlap-checklist
> **Output template**: templates/optimization-report-document.md

## ROUTING

> **Agents**: media-buyer, performance-analyst
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Identificar e resolver sobreposição de audiências entre ad sets e campanhas, eliminando competição interna nos leilões que inflaciona custos e reduz eficiência de entrega.

## Inputs
- Estrutura de campanhas ativa em todas as plataformas
- Meta Ads Audience Overlap tool
- Relatórios de delivery e frequency por ad set
- Mapeamento de audiências e segmentos ativos
- Dados de CPM e CPA por ad set nas últimas 4 semanas

## Steps
1. Exportar a lista completa de audiências ativas por campanha e ad set em cada plataforma
2. Usar o Meta Audience Overlap tool para mensurar % de sobreposição entre todos os pares de audiência
3. Identificar ad sets com overlap >30% que estão competindo no mesmo leilão
4. Analisar o impacto da sobreposição: comparar CPM e delivery dos ad sets sobrepostos
5. Criar exclusões de audiência: excluir custom audiences de ad sets que não devem alcançá-las
6. Consolidar ad sets com audiências muito similares em um único ad set com budget combinado
7. Implementar a estrutura de exclusão em cascata: Buyers excluídos de Leads, Leads excluídos de Cold
8. Verificar audience overlap em Google Ads entre campanhas de Search e Display
9. Ajustar negative audiences no Google Ads para evitar canibalização
10. Documentar o mapa de exclusões final e monitorar o impacto nas métricas pós-cleanup
11. Criar um protocolo de revisão mensal de audience overlap

## Output
Relatório de audience overlap cleanup contendo: mapa de sobreposição antes/depois, exclusões implementadas, ad sets consolidados, impacto estimado em CPM/CPA, e protocolo de manutenção mensal.

## Quality Gate
- Todas as audiências com overlap >30% resolvidas (exclusão ou consolidação)
- Estrutura de exclusão em cascata implementada e documentada
- Nenhum ad set competindo consigo mesmo no leilão
- Redução mensurável em CPM após o cleanup (monitorar por 7-14 dias)
- Traffic Chief valida as mudanças antes e depois da implementação

## Duration
3-5 horas para análise e implementação; 1 hora para documentação
