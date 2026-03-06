# Pinterest Campaign Setup Quality
> **Type**: Quality Gate
> **Domain**: Campaign Setup — Pinterest
> **Reviewed by**: Media Buyer

## Purpose
Garante que toda campanha criada no Pinterest Ads esteja configurada corretamente antes de ser ativada. Erros na configuracao desperdicam budget, comprometem dados e atrasam a otimizacao.

## Checklist

### Estrutura da Campanha
- [ ] Objetivo da campanha (awareness, consideration, conversions) alinhado com a estrategia documentada
- [ ] Nome da campanha segue a naming convention do time
- [ ] Estrutura de ad groups reflete o plano de teste aprovado
- [ ] Campaign spending limit configurado como rede de seguranca
- [ ] Status da campanha configurado como "paused" antes da revisao final

### Configuracao de Audience
- [ ] Targeting por interests alinhado com a persona documentada
- [ ] Keywords adicionadas e revisadas (broad match vs exact match)
- [ ] Actalike audiences criadas a partir das seed lists corretas
- [ ] Customer lists carregadas e matched corretamente
- [ ] Exclusoes de audiencia aplicadas para evitar overlap entre ad groups
- [ ] Targeting demografico (idade, genero, localizacao) conforme estrategia

### Budget e Bidding
- [ ] Budget diario ou lifetime corresponde ao plano aprovado
- [ ] Bid strategy selecionada com justificativa documentada (automatic, custom, target cost)
- [ ] Minimum budget por ad group atende aos requisitos de aprendizado da plataforma
- [ ] Pacing configurado corretamente (standard vs accelerated)

### Criativos e Destino
- [ ] Pins atendem as especificacoes de formato (standard, video, carousel, idea)
- [ ] Aspect ratio correto para cada formato (2:3 para standard pins)
- [ ] Destination URLs funcionais e com UTM parameters corretos
- [ ] Rich pins habilitados quando aplicavel
- [ ] Ad copy revisado e sem erros ortograficos

### Tracking e Medicao
- [ ] Pinterest Tag instalada e disparando corretamente
- [ ] Eventos de conversao configurados (checkout, add to cart, signup, lead)
- [ ] Enhanced match habilitado para melhorar match rate
- [ ] Conversion window configurada conforme plano de medicao
- [ ] Test conversions verificadas no Events Manager

## Pass/Fail Criteria
Todos os itens devem ser aprovados antes da campanha ir ao ar. Itens de tracking e audience nao possuem excecao.

## If Failed
Pausar a campanha caso ja esteja ativa. Documentar o erro, corrigir e re-verificar com um segundo revisor antes de reativar.

## Related
- `campaign-build-quality.md`
- `creative-specs-quality.md`
- `tracking-plan-quality.md`
