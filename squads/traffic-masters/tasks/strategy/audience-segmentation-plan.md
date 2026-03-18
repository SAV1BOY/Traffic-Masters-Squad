# Audience Segmentation Plan

> **Type**: Task
> **Category**: strategy
> **Agents**: Kusmich, Mandalia, Traffic Chief
> **Frameworks**: Kusmich Audience Architecture, Mandalia 5W Avatar, RFM Segmentation
> **Checklists**: strategy-checklist, segmentation-checklist
> **Output template**: templates/audience-segmentation-document.md

## ROUTING

> **Agents**: traffic-chief, molly-pittman
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Segmentar audiências de forma granular para deployment de campanhas direcionadas, criando camadas de targeting que maximizem relevância e minimizem desperdício de budget.

## Inputs
- ICP e avatar documentados
- Dados de CRM segmentados (RFM analysis)
- Dados de pixel e eventos de conversão
- Pesquisa de lookalike audiences
- Histórico de performance por segmento de audiência
- Mapeamento de interesses e comportamentos por plataforma

## Steps
1. Classificar a base existente usando modelo RFM (Recency, Frequency, Monetary)
2. Criar os tiers de audiência: Ice Cold, Cold, Warm, Hot, Buyer, Repeat Buyer
3. Definir os critérios de cada tier por plataforma (tamanho de janela, eventos, engajamento)
4. Mapear audiências de interesse e comportamento para cada tier de temperatura
5. Criar a estrutura de custom audiences por plataforma (website visitors, engagers, email lists)
6. Definir as exclusões entre segmentos para evitar overlap e canibalização
7. Estabelecer o messaging framework por tier (o que comunicar para cada temperatura)
8. Calcular o tamanho estimado de cada segmento e o budget proporcional
9. Documentar a naming convention padronizada para audiências em todas as plataformas
10. Criar o plano de refresh e manutenção das audiências (frequência de atualização)

## Output
Plano de segmentação contendo: taxonomia de audiências por tier, critérios de segmentação por plataforma, estrutura de custom audiences, mapa de exclusões, messaging framework por segmento, naming convention, e calendário de manutenção.

## Quality Gate
- Todos os tiers de audiência definidos com critérios claros e mensuráveis
- Exclusões mapeadas para evitar overlap entre ad sets
- Naming convention consistente e aplicável a todas as plataformas
- Traffic Chief valida a estrutura antes do setup nas plataformas
- Tamanho mínimo de audiência respeitado por plataforma

## Duration
4-6 horas para desenvolvimento do plano; 1-2 horas para documentação
