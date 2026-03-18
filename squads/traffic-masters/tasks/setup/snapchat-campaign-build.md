# Snapchat Campaign Build

> **Type**: Task
> **Category**: setup
> **Agents**: Traffic Chief, Kusmich, Mandalia
> **Frameworks**: Kusmich Audience Architecture, Snapchat Ads Best Practices
> **Checklists**: setup-checklist, campaign-launch-checklist
> **Output template**: templates/campaign-build-document.md

## ROUTING

> **Agents**: media-buyer, pixel-specialist
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Configurar e lançar campanhas no Snapchat Ads, atingindo audiências mais jovens (Gen Z e Millennials) com formatos imersivos full-screen e custos de CPM competitivos.

## Inputs
- Conta Snapchat Business Manager configurada
- Snap Pixel instalado e validado
- Criativos verticais otimizados (9:16, 1080x1920px)
- Audiências definidas no plano de segmentação
- Budget aprovado e objetivos de campanha
- Landing pages mobile-first otimizadas

## Steps
1. Verificar a instalação do Snap Pixel e configurar os eventos de conversão (Purchase, Sign Up, Add to Cart)
2. Configurar Snap Audience Match: upload de listas de clientes e criação de custom audiences
3. Criar lookalike audiences baseadas nos melhores segmentos de clientes
4. Configurar campanhas por objetivo: Awareness, App Installs, Web Conversions, Catalog Sales
5. Definir targeting: demographics, interests, Snap Lifestyle Categories, custom audiences
6. Criar os ad sets com bid strategy adequada (auto-bid, target cost, max bid)
7. Subir criativos nos formatos: Single Image/Video, Collection Ads, Story Ads, AR Lenses (se aplicável)
8. Configurar os placements: Between Content, Between Stories, Spotlight
9. Definir budget diário, schedule e delivery optimization
10. Realizar QA completo: pixel firing, criativos, deep links, audiências
11. Lançar e monitorar o delivery e spend pacing nas primeiras 48-72 horas

## Output
Campanhas Snapchat configuradas e lançadas, incluindo: documentação de estrutura de conta, specs dos criativos utilizados, checklist de QA, e plano de monitoramento inicial.

## Quality Gate
- Snap Pixel validado com todos os eventos disparando corretamente
- Criativos em formato vertical (9:16) e aprovados pela plataforma
- Landing pages otimizadas para mobile com load time <3 segundos
- Audiências com tamanho mínimo viável para a plataforma
- Traffic Chief aprova a estrutura e os criativos antes do lançamento

## Duration
3-5 horas para setup completo; 1-2 horas para QA e lançamento
