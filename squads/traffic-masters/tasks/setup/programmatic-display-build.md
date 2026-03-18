# Programmatic Display Build

> **Type**: Task
> **Category**: setup
> **Agents**: Traffic Chief, Deiss, Kusmich
> **Frameworks**: Kusmich Audience Architecture, Programmatic Media Framework
> **Checklists**: setup-checklist, campaign-launch-checklist
> **Output template**: templates/campaign-build-document.md

## ROUTING

> **Agents**: media-buyer, pixel-specialist
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Configurar campanhas de display programático via DV360 (Display & Video 360) ou The Trade Desk (TTD), alcançando audiências em escala através de inventário premium com controle granular de targeting e brand safety.

## Inputs
- Acesso a DSP configurada (DV360 ou The Trade Desk)
- Pixels e floodlight tags instalados e validados
- Criativos em múltiplos formatos de display (300x250, 728x90, 160x600, 320x50, etc.)
- Audiências first-party e third-party definidas
- Budget aprovado e objetivos de campanha
- Brand safety guidelines e lista de categorias sensíveis

## Steps
1. Configurar a estrutura de conta no DSP: Advertiser → Campaign → Insertion Order → Line Item
2. Instalar e validar os pixels de tracking (Floodlight tags no DV360, Universal Pixel no TTD)
3. Criar as audiências: first-party (CRM lists, website visitors), third-party (data segments)
4. Configurar contextual targeting e keyword targeting para relevância
5. Definir a estratégia de inventory: Open Exchange, Private Marketplace (PMP), Programmatic Guaranteed
6. Configurar brand safety: bloqueio de categorias sensíveis, keyword exclusions, domain blacklist
7. Definir viewability targets (mínimo 70% viewable) e fraud prevention settings
8. Subir criativos em todos os formatos necessários incluindo HTML5 e responsive ads
9. Configurar bidding strategy: CPM fixo, vCPM, CPA target ou custom algorithm
10. Definir frequency caps por usuário (impressões/dia, /semana)
11. Realizar QA completo: tracking, criativos renderizando em todos os tamanhos, brand safety
12. Lançar e monitorar delivery, viewability e brand safety nas primeiras 72 horas

## Output
Campanhas programáticas configuradas e lançadas, incluindo: estrutura de conta documentada, configurações de brand safety, audiências ativadas, specs dos criativos, e plano de monitoramento.

## Quality Gate
- Tracking pixels validados com conversões registrando corretamente
- Brand safety configurada conforme guidelines do cliente
- Viewability settings ativados com target mínimo de 70%
- Fraud prevention ativa (IAS, DoubleVerify ou similar)
- Criativos renderizando corretamente em todos os formatos
- Traffic Chief aprova a estrutura e as configurações de brand safety

## Duration
6-8 horas para setup completo do DSP; 2-3 horas para QA e lançamento
