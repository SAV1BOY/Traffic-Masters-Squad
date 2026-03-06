# Conversion Value Setup

> **Type**: Task
> **Category**: tracking
> **Agents**: Traffic Chief, Deiss, Kusmich
> **Frameworks**: Value-Based Bidding Framework, Deiss Customer Value Journey
> **Checklists**: tracking-checklist, conversion-setup-checklist
> **Output template**: templates/tracking-setup-document.md

## Objective
Configurar conversion values e value-based bidding nas plataformas de ads, permitindo que os algoritmos otimizem para o valor real de cada conversão e maximizem o ROAS.

## Inputs
- Dados de valor de conversão por produto/serviço (ticket médio, LTV, margem)
- Acesso às plataformas de ads (Google Ads, Meta Ads, TikTok Ads)
- GTM (Google Tag Manager) configurado
- Mapeamento de eventos de conversão existentes
- Dados históricos de vendas segmentados por canal e produto

## Steps
1. Mapear todos os eventos de conversão e atribuir valores monetários baseados em dados reais
2. Definir a hierarquia de conversion values: Purchase (valor real), Lead (valor estimado), Add to Cart (valor ponderado)
3. Configurar dynamic conversion values no Google Ads via tag de conversão com valor variável
4. Implementar value parameters no Meta Pixel para eventos de Purchase com valor dinâmico
5. Configurar conversion value rules no Google Ads (ajustes por audiência, device, localização)
6. Criar calculated metrics para estimar o valor de conversões intermediárias (leads, trials)
7. Configurar o enhanced conversions para melhorar a atribuição com dados first-party
8. Testar os valores sendo passados corretamente via GTM Debug Mode e plataforma de ads
9. Migrar as campanhas de Target CPA para Target ROAS onde aplicável
10. Documentar a tabela de conversion values e a lógica de cálculo para cada evento

## Output
Setup de conversion values completo, incluindo: tabela de valores por evento, configurações documentadas por plataforma, evidências de teste (screenshots de debug), e guia de migração para value-based bidding.

## Quality Gate
- Todos os eventos de conversão passando valores corretos (validado via debug tools)
- Valores baseados em dados reais de vendas, não estimativas arbitrárias
- Enhanced conversions configurado e validado
- Período de teste de 2 semanas antes de migrar para value-based bidding
- Traffic Chief revisa e aprova a tabela de valores e a estratégia de migração

## Duration
4-6 horas para configuração técnica; 1-2 horas para testes e documentação
