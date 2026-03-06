# Snapchat Campaign Setup Quality
> **Type**: Quality Gate
> **Domain**: Campaign Setup — Snapchat
> **Reviewed by**: Media Buyer

## Purpose
Garante que toda campanha no Snapchat Ads Manager esteja configurada corretamente antes da ativacao. Configuracoes incorretas causam desperdicio de budget, dados corrompidos e atrasos na otimizacao.

## Checklist

### Estrutura da Campanha
- [ ] Objetivo da campanha selecionado corretamente (awareness, app installs, conversions, leads, catalog sales)
- [ ] Nome da campanha segue a naming convention do time
- [ ] Ad sets organizados conforme plano de teste documentado
- [ ] Campaign spending limit configurado como safety net
- [ ] Split test configurado corretamente quando aplicavel

### Configuracao de Audience
- [ ] Demographic targeting (idade 13+, genero, idioma) conforme estrategia
- [ ] Geo-targeting configurado com precisao (pais, estado, cidade, raio)
- [ ] Predefined audiences (lifestyles, behaviors) alinhadas com a persona
- [ ] Custom audiences (Snap Audience Match) carregadas e processadas
- [ ] Lookalike audiences baseadas nas seed lists corretas
- [ ] Audience exclusions aplicadas para separar prospecting de retargeting
- [ ] Device targeting (iOS, Android, todos) configurado conforme plano

### Placement e Delivery
- [ ] Placements selecionados (Stories, Spotlight, Content, Lens, etc.) conforme estrategia
- [ ] Delivery type configurado (standard vs accelerated)
- [ ] Frequency cap definido para evitar ad fatigue
- [ ] Schedule (start/end dates e dayparting) correto

### Budget e Bidding
- [ ] Budget diario ou lifetime alinhado com o plano aprovado
- [ ] Bid strategy selecionada (auto-bid, target cost, max bid) com justificativa
- [ ] Goal-based bidding event configurado corretamente (swipe up, purchase, install)
- [ ] Minimum budget por ad set atende requisitos de learning phase

### Tracking e Conversao
- [ ] Snap Pixel instalado e verificado no site/app
- [ ] Eventos de conversao mapeados (purchase, add to cart, sign up, page view)
- [ ] Conversions API (CAPI) configurada e enviando eventos
- [ ] Attribution window configurada conforme plano de medicao
- [ ] Test conversions verificadas no Events Manager

## Pass/Fail Criteria
Todos os itens devem ser verificados antes do lancamento. Itens de tracking e audience sao bloqueantes — nao ha excecoes.

## If Failed
Pausar a campanha imediatamente. Registrar o problema, corrigir e obter validacao de um segundo revisor antes de reativar.

## Related
- `creative-specs-quality.md`
- `../campaign-build-quality.md`
- `../tracking-plan-quality.md`
