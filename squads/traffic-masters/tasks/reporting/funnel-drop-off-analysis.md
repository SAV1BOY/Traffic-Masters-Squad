# Funnel Drop-Off Analysis

> **Type**: Task
> **Category**: reporting
> **Agents**: Deiss, Traffic Chief, Kusmich
> **Frameworks**: Deiss Customer Value Journey, Funnel Analysis Framework, CRO Diagnostic Model
> **Checklists**: reporting-checklist, funnel-analysis-checklist
> **Output template**: templates/reporting-document.md

## Objective
Analisar os pontos de drop-off no funil de conversão, quantificando as perdas em cada etapa e recomendando ações corretivas para melhorar a taxa de conversão end-to-end das campanhas pagas.

## Inputs
- Dados de Google Analytics 4 (funnel exploration, path analysis)
- Dados de eventos de conversão das plataformas de ads
- Heatmaps e session recordings (Hotjar, Microsoft Clarity)
- Dados de formulários e checkout (abandonment rates)
- Landing page performance (bounce rate, time on page, scroll depth)
- Dados de CRM para conversões downstream (lead → sale)

## Steps
1. Mapear o funil completo de conversão: Ad Click → Landing Page → Engagement → Lead/Add to Cart → Conversion → Post-Purchase
2. Calcular a taxa de passagem (pass-through rate) entre cada etapa do funil
3. Identificar os maiores pontos de drop-off: onde a perda percentual é mais significativa
4. Analisar o drop-off por segmento: device (mobile vs. desktop), source, audiência, geo
5. Usar heatmaps para identificar problemas de UX nas landing pages (onde param de scrollar, onde clicam)
6. Analisar session recordings dos usuários que abandonaram vs. os que converteram
7. Verificar a velocidade de carregamento das landing pages (Core Web Vitals) e seu impacto no bounce rate
8. Analisar o checkout/formulário: quais campos causam mais abandono, multi-step vs. single-step
9. Calcular o impacto financeiro de cada ponto de drop-off (receita perdida estimada)
10. Priorizar as correções usando a matriz ICE (Impact x Confidence x Ease)
11. Criar hipóteses de teste A/B para cada ponto de drop-off priorizado
12. Documentar o relatório com visualizações de funil e recomendações priorizadas

## Output
Relatório de funnel drop-off contendo: visualização do funil com taxas por etapa, identificação dos top 5 pontos de perda, análise por segmento, impacto financeiro estimado, recomendações priorizadas (ICE), e hipóteses de teste A/B.

## Quality Gate
- Funil mapeado com dados de pelo menos 30 dias e volume estatisticamente relevante
- Drop-offs validados com pelo menos 2 fontes de dados (analytics + heatmap/recordings)
- Impacto financeiro calculado para cada ponto de perda identificado
- Recomendações priorizadas com framework ICE e estimativa de lift
- Traffic Chief e stakeholders revisam as conclusões e aprovam o plano de ação

## Duration
5-8 horas para análise completa; 2-3 horas para documentação e recomendações
