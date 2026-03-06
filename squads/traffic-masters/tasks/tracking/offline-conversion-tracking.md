# Offline Conversion Tracking

> **Type**: Task
> **Category**: tracking
> **Agents**: Traffic Chief, Deiss, Kusmich
> **Frameworks**: Offline Conversion Import Framework, Full-Funnel Attribution Model
> **Checklists**: tracking-checklist, offline-conversion-checklist
> **Output template**: templates/tracking-setup-document.md

## Objective
Configurar pipelines de importação de conversões offline nas plataformas de ads, conectando dados de CRM e vendas presenciais ao tracking digital para otimização com dados completos de funil.

## Inputs
- CRM com dados de vendas/conversões offline (Salesforce, HubSpot, Pipedrive, etc.)
- Google Click ID (GCLID) e Facebook Click ID (FBCLID) sendo capturados nos formulários
- Acesso às APIs das plataformas de ads
- Mapeamento do ciclo de vendas e tempo médio de conversão offline
- Dados históricos de conversões offline dos últimos 90 dias

## Steps
1. Configurar a captura de GCLID e FBCLID em todos os formulários e landing pages
2. Armazenar os click IDs no CRM junto com os dados do lead/cliente
3. Definir quais estágios do funil de vendas serão importados como conversões (SQL, Opportunity, Closed Won)
4. Configurar o Google Ads Offline Conversion Import via upload manual ou API
5. Configurar o Meta Conversions API (CAPI) para envio de eventos offline server-side
6. Criar o pipeline automatizado de importação: CRM → transformação de dados → upload para plataformas
7. Definir a frequência de importação (diária recomendada, mínimo semanal)
8. Configurar enhanced conversions for leads no Google Ads com dados hasheados
9. Testar o pipeline completo com dados de teste antes de ativar em produção
10. Validar que as conversões offline estão atribuindo corretamente às campanhas de origem
11. Documentar o pipeline, troubleshooting guide e processo de manutenção

## Output
Pipeline de offline conversion tracking configurado e validado, incluindo: documentação técnica do pipeline, mapeamento de eventos offline, evidências de atribuição correta, e guia de manutenção/troubleshooting.

## Quality Gate
- GCLID e FBCLID sendo capturados em 100% dos formulários
- Pipeline de importação testado e validado com dados reais
- Match rate de conversões offline >50% (idealmente >70%)
- Latência de importação dentro do acceptable window de cada plataforma (90 dias Google, 7 dias Meta)
- Traffic Chief valida que os dados offline estão melhorando a otimização das campanhas

## Duration
6-10 horas para setup técnico completo; 2-3 horas para testes e documentação
