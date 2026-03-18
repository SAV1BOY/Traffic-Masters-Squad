# Creative Reporting Deep Dive

> **Type**: Task
> **Category**: reporting
> **Agents**: Mandalia, Traffic Chief, Kusmich
> **Frameworks**: Mandalia Creative Matrix, Creative Performance Analysis Framework
> **Checklists**: reporting-checklist, creative-analysis-checklist
> **Output template**: templates/reporting-document.md

## ROUTING

> **Agents**: performance-analyst, traffic-chief
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Realizar análise profunda da performance criativa across todas as dimensões (formato, angle, copy, visual, placement), identificando padrões de sucesso e oportunidades de iteração para melhorar resultados.

## Inputs
- Dados de performance de todos os criativos ativos e pausados (últimos 30-90 dias)
- Breakdown por creative asset: impressions, CTR, CPC, CPM, CPA, ROAS, thumbstop rate, hold rate
- Naming convention que permita filtrar por angle, formato e variação
- Dados de DCO performance por asset individual
- Benchmarks internos e do setor por formato criativo

## Steps
1. Exportar dados completos de performance criativa de todas as plataformas ativas
2. Segmentar a análise por dimensão: formato (imagem vs. vídeo vs. carrossel), angle, copy variation
3. Calcular o creative win rate: % de criativos que atingem CPA target por batch de produção
4. Identificar os top 10% criativos por CPA e analisar os atributos em comum
5. Identificar os bottom 10% e documentar os padrões de falha
6. Analisar a curva de fadiga criativa: em quantos dias/impressões o CPA começa a subir
7. Avaliar performance por placement (Feed vs. Stories vs. Reels) para cada formato
8. Analisar a correlação entre thumbstop rate (primeiros 3s) e conversão final
9. Comparar performance de UGC vs. branded vs. product-focused por etapa do funil
10. Cruzar copy performance: quais hooks, CTAs e messaging frameworks geram melhor resultado
11. Criar o creative scorecard com ranking de atributos que predizem sucesso
12. Documentar as recomendações para o próximo ciclo de produção criativa

## Output
Relatório de creative deep dive contendo: ranking de criativos por performance, análise de padrões de sucesso/falha, curva de fadiga criativa, creative scorecard, e brief de recomendações para próximo ciclo de produção.

## Quality Gate
- Análise baseada em dados de pelo menos 30 dias para relevância
- Mínimo de 1000 impressões por criativo para inclusão na análise
- Padrões identificados com suporte de pelo menos 5 criativos por cluster
- Recomendações actionable e conectadas diretamente aos dados
- Traffic Chief revisa e valida as conclusões e recomendações

## Duration
4-6 horas para análise completa; 2 horas para documentação e apresentação
