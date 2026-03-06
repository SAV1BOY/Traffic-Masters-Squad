# Bid Strategy Optimization

> **Type**: Task
> **Category**: optimization
> **Agents**: Traffic Chief, Kusmich, Deiss
> **Frameworks**: Bidding Optimization Framework, Value-Based Bidding Model
> **Checklists**: optimization-checklist, bidding-strategy-checklist
> **Output template**: templates/optimization-report-document.md

## Objective
Otimizar as estratégias de bidding nas plataformas de ads para alinhar os lances com os objetivos reais de negócio, maximizando conversões ou ROAS dentro do budget disponível.

## Inputs
- Dados de performance das campanhas ativas (últimos 30-60 dias)
- Metas de CPA e ROAS por campanha/produto
- Conversion value data configurado
- Relatórios de auction insights e competitive metrics
- Budget constraints por campanha
- Histórico de mudanças de bid strategy e seus impactos

## Steps
1. Auditar as bid strategies atuais de todas as campanhas ativas (Manual CPC, Maximize Conversions, Target CPA, Target ROAS)
2. Analisar o desempenho de cada bid strategy: CPA real vs. target, ROAS real vs. target, delivery pacing
3. Identificar campanhas onde a bid strategy está sub-otimizada (CPA >20% acima do target, ROAS abaixo)
4. Avaliar se as campanhas têm dados suficientes de conversão para bid strategies automatizadas (mínimo 30 conversões/mês)
5. Criar um roadmap de migração: Manual → Maximize Clicks → Maximize Conversions → Target CPA → Target ROAS
6. Implementar ajustes graduais nos targets (máximo 15-20% por vez para não resetar o learning)
7. Configurar portfolio bid strategies no Google Ads para campanhas com objetivos similares
8. Testar bid adjustments por device, hora do dia, audiência e localização
9. Analisar o impacto dos bid modifiers e remover os que não estão gerando lift
10. Configurar experiments/drafts no Google Ads para A/B test de bid strategies
11. Monitorar a learning phase após cada mudança (7-14 dias sem interferir)
12. Documentar os resultados e criar um playbook de bidding por tipo de campanha

## Output
Relatório de bid strategy optimization contendo: auditoria das estratégias atuais, roadmap de migração, resultados dos testes, bid adjustments aplicados, e playbook de bidding por tipo de campanha.

## Quality Gate
- Todas as campanhas com bid strategy alinhada ao volume de dados disponível
- Nenhuma mudança de bid >20% de uma vez para preservar learning
- Experiments configurados para testar antes de aplicar mudanças em larga escala
- Learning phase respeitada após cada ajuste (mínimo 7 dias)
- Traffic Chief revisa e aprova cada mudança de bid strategy

## Duration
4-6 horas para análise e implementação; 2 semanas para monitoramento dos resultados
