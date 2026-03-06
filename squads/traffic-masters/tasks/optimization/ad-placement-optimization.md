# Ad Placement Optimization

> **Type**: Task
> **Category**: optimization
> **Agents**: Traffic Chief, Kusmich, Mandalia
> **Frameworks**: Placement Performance Framework, Platform-Native Optimization Model
> **Checklists**: optimization-checklist, placement-analysis-checklist
> **Output template**: templates/optimization-report-document.md

## Objective
Otimizar os posicionamentos de anúncios (placements) e configurar exclusões estratégicas para concentrar budget nos placements que entregam melhor custo por resultado.

## Inputs
- Relatórios de performance por placement das campanhas ativas (últimos 30 dias)
- Breakdown por placement: Feed, Stories, Reels, Search, Display, YouTube, Audience Network
- Dados de CTR, CPC, CPM, CPA e ROAS por placement
- Criativos ativos e seus formatos por placement
- Benchmarks de performance por placement do setor

## Steps
1. Extrair relatórios de breakdown por placement em todas as plataformas ativas
2. Analisar CTR, CPC, CPM, CPA e conversion rate por placement individual
3. Identificar placements com CPA >50% acima da média da campanha
4. Identificar placements high-performers que merecem budget incremental
5. Avaliar se os criativos estão otimizados para cada placement (aspect ratio, duração, copy length)
6. Excluir placements de baixa qualidade: Audience Network (se CPA alto), apps, in-article (caso a caso)
7. Testar placement-specific campaigns para isolar performance dos top placements
8. Configurar bid adjustments por placement no Google Ads (Display, YouTube, Search Partners)
9. Avaliar a performance de Advantage+ placements vs. manual placements no Meta
10. Criar criativos específicos para os top placements (ex: Reels-specific, Stories-specific)
11. Documentar a lista de exclusões e recomendações de placement por tipo de campanha

## Output
Relatório de placement optimization contendo: análise de performance por placement, lista de exclusões implementadas, recomendações de placement por objetivo, e plano de teste de placement-specific campaigns.

## Quality Gate
- Análise de pelo menos 30 dias de dados por placement para relevância estatística
- Placements com CPA >50% acima da média excluídos ou justificados (awareness)
- Criativos adequados disponíveis para os top placements selecionados
- Impacto das exclusões monitorado por 7-14 dias pós-implementação
- Traffic Chief aprova as exclusões e mudanças de alocação por placement

## Duration
3-4 horas para análise e implementação; 1-2 semanas para monitoramento pós-otimização
