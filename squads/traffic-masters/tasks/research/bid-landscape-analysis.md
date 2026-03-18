# Bid Landscape Analysis

> **Type**: Task
> **Category**: research
> **Agents**: Traffic Chief, Mandalia, Deiss
> **Frameworks**: Auction Insights Framework, Competitive Intelligence Model
> **Checklists**: research-checklist, bid-analysis-checklist
> **Output template**: templates/bid-landscape-document.md

## ROUTING

> **Agents**: traffic-chief, ads-analyst
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Analisar o cenário competitivo de lances (bids) nas principais plataformas de ads, mapeando CPCs, CPMs e dinâmicas de leilão para informar estratégias de bidding mais eficientes.

## Inputs
- Acesso às contas de ads ativas (Google Ads, Meta Ads, TikTok Ads)
- Relatórios de Auction Insights do Google Ads
- Ferramentas de inteligência competitiva (SEMrush, SpyFu, iSpionage)
- Histórico de performance das campanhas (últimos 90 dias)
- Lista de principais concorrentes diretos e indiretos

## Steps
1. Extrair relatórios de Auction Insights do Google Ads para as campanhas principais
2. Analisar impression share, overlap rate e position above rate dos concorrentes
3. Levantar CPCs médios por keyword category usando Google Keyword Planner e SEMrush
4. Mapear CPMs médios por audiência e posicionamento no Meta Ads (Feed, Stories, Reels)
5. Avaliar tendências de custo por período (mensal, trimestral) para identificar inflação de lances
6. Identificar os horários e dias com maior competição e variação de custo
7. Analisar o bid landscape do TikTok e outras plataformas secundárias utilizadas
8. Comparar custo por resultado (CPA, ROAS) entre plataformas e segmentos de audiência
9. Documentar oportunidades de arbitragem (canais/horários/audiências com custo abaixo do benchmark)
10. Criar recomendações de bidding strategy baseadas nos findings

## Output
Relatório de bid landscape contendo: mapa competitivo por canal, análise de CPCs/CPMs por segmento, tendências de custo, oportunidades de arbitragem, e recomendações de bid strategy por plataforma.

## Quality Gate
- Dados de pelo menos 90 dias analisados para relevância estatística
- Análise cobre no mínimo 2 plataformas principais
- Oportunidades de otimização identificadas e quantificadas
- Traffic Chief revisa e valida as recomendações de bidding

## Duration
4-6 horas para extração e análise; 2 horas para documentação
