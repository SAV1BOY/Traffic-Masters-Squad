# Twitter/X Campaign Build

> **Type**: Task
> **Category**: setup
> **Agents**: Traffic Chief, Kusmich, Mandalia
> **Frameworks**: Kusmich Audience Architecture, Twitter/X Ads Best Practices
> **Checklists**: setup-checklist, campaign-launch-checklist
> **Output template**: templates/campaign-build-document.md

## ROUTING

> **Agents**: media-buyer, pixel-specialist
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Configurar e lançar campanhas no Twitter/X Ads, aproveitando o contexto conversacional e de real-time para gerar awareness, engajamento e conversões em audiências de alta intenção.

## Inputs
- Conta Twitter/X Ads ativa e verificada
- Twitter/X Pixel instalado e validado
- Criativos otimizados para a plataforma (imagens, vídeos, carrossel, text ads)
- Audiências definidas no plano de segmentação
- Budget aprovado e objetivos de campanha definidos
- Landing pages otimizadas

## Steps
1. Verificar a instalação do Twitter/X Pixel e configurar os conversion events (Purchase, Lead, Add to Cart)
2. Configurar as tailored audiences: website visitors, lista de emails, app activity
3. Mapear os conversation topics e keywords relevantes para targeting
4. Criar campanhas por objetivo: Reach, Engagement, Website Traffic, Conversions
5. Configurar ad groups com targeting: followers lookalike, interests, keywords, conversation topics
6. Subir os criativos seguindo as specs (1200x675px para imagem, 15-30s para vídeo)
7. Configurar bid strategy: automatic bid, maximum bid ou target cost
8. Definir os placements: Home Timeline, Search Results, Profiles, Replies
9. Configurar frequency caps para evitar ad fatigue
10. Realizar QA completo: tracking, criativos, links, audiências, billing
11. Lançar e monitorar delivery e pacing nas primeiras 48 horas

## Output
Campanhas Twitter/X configuradas e lançadas, incluindo: documentação de estrutura, configurações de targeting, checklist de QA, e plano de monitoramento inicial.

## Quality Gate
- Twitter/X Pixel disparando corretamente com todos os eventos mapeados
- Criativos aprovados sem policy violations
- Targeting configurado com exclusões adequadas para evitar desperdício
- Frequency caps definidos para cada campaign objective
- Traffic Chief aprova a estrutura e revisa as primeiras métricas pós-lançamento

## Duration
3-4 horas para setup completo; 1-2 horas para QA e lançamento
