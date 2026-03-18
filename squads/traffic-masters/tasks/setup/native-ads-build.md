# Native Ads Build

> **Type**: Task
> **Category**: setup
> **Agents**: Traffic Chief, Deiss, Mandalia
> **Frameworks**: Deiss Customer Value Journey, Native Advertising Best Practices
> **Checklists**: setup-checklist, campaign-launch-checklist
> **Output template**: templates/campaign-build-document.md

## ROUTING

> **Agents**: media-buyer, pixel-specialist
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Configurar campanhas de native advertising nas plataformas Taboola e Outbrain, gerando tráfego qualificado através de conteúdo promovido em publishers premium com alto volume de impressões.

## Inputs
- Contas Taboola e/ou Outbrain ativas e aprovadas
- Pixels de tracking instalados e validados em ambas plataformas
- Headlines e thumbnails otimizados para native ads (curiosity-driven)
- Artigos, landing pages ou advertorials preparados como destino
- Budget aprovado e objetivos de campanha (tráfego, leads, conversões)
- Lista de publishers para whitelist/blacklist

## Steps
1. Configurar os pixels de tracking de Taboola e Outbrain e validar os eventos de conversão
2. Criar as campanhas definindo objetivo (awareness, traffic, conversions)
3. Configurar targeting: geo, device, OS, hora do dia, dia da semana
4. Definir a estratégia de bidding: Smart Bid, Target CPA, ou Fixed Bid
5. Criar variações de ads com diferentes combinações de headline + thumbnail (mínimo 5-10 variações)
6. Escrever headlines com foco em curiosity gap e relevância editorial
7. Selecionar thumbnails que pareçam editoriais (evitar look de banner ad)
8. Configurar publisher whitelist com sites premium e relevantes para o público-alvo
9. Criar publisher blacklist para sites de baixa qualidade ou irrelevantes
10. Definir budget diário e campaign schedule
11. Realizar QA: tracking, links de destino, qualidade dos publishers, billing
12. Lançar e monitorar CTR, CPC e quality score nas primeiras 72 horas

## Output
Campanhas native ads configuradas e lançadas, incluindo: estrutura de conta documentada, variações de headlines/thumbnails, publisher whitelist/blacklist, e plano de otimização inicial.

## Quality Gate
- Pixels de tracking disparando corretamente em ambas as plataformas
- Mínimo de 5 variações de ad por campanha para teste A/B eficiente
- Publisher whitelist configurada com sites relevantes e de qualidade
- Headlines aprovadas sem clickbait excessivo (compliance com políticas)
- Traffic Chief aprova a estrutura e os criativos antes do lançamento

## Duration
4-6 horas para setup de ambas as plataformas; 2 horas para QA e lançamento
