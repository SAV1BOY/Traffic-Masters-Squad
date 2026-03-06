# Platform Migration Quality
> **Type**: Quality Gate
> **Domain**: Operations — Migration
> **Reviewed by**: Media Lead / Tech Lead

## Purpose
Garante que migracoes entre plataformas de ads, tracking ou analytics sejam executadas com seguranca, preservando dados historicos, tracking e performance das campanhas.

## Checklist

### Planejamento Pre-Migracao
- [ ] Escopo da migracao documentado (o que migra, o que nao migra)
- [ ] Inventario completo de campanhas, ad sets e ads ativos na plataforma de origem
- [ ] Mapeamento de audiences e custom audiences a serem recriadas
- [ ] Timeline de migracao com janelas de downtime planejadas
- [ ] Rollback plan documentado caso a migracao falhe

### Backup de Dados
- [ ] Export de todas as campanhas ativas com configuracoes detalhadas
- [ ] Export de historico de performance (ultimos 6-12 meses)
- [ ] Backup de audiences, custom conversions e eventos
- [ ] Screenshots das configuracoes criticas como evidencia
- [ ] Dados de billing e faturas historicas arquivados

### Configuracao na Nova Plataforma
- [ ] Conta criada com estrutura organizacional correta
- [ ] Permissoes e acessos configurados para todos os membros do time
- [ ] Pixels e tags de conversao instalados e verificados
- [ ] CAPI / server-side tracking reconfigurado e testado
- [ ] Audiences recriadas e validadas (tamanho e composicao)
- [ ] Naming conventions aplicadas na nova plataforma

### Validacao e Teste
- [ ] Test campaign lancada com budget minimo para validar tracking
- [ ] Conversoes verificadas end-to-end (click > pixel > platform > analytics)
- [ ] UTM parameters validados nos reports de analytics
- [ ] Dados de custo aparecendo corretamente nos dashboards
- [ ] Comparacao de dados entre plataforma antiga e nova (reconciliation)

### Pos-Migracao
- [ ] Campanhas na plataforma antiga pausadas ou desativadas
- [ ] Comunicacao enviada para stakeholders sobre a conclusao
- [ ] Documentacao atualizada com novos IDs, acessos e configuracoes
- [ ] Monitoramento intensivo nas primeiras 72h pos-migracao
- [ ] Retrospectiva agendada para documentar aprendizados

## Pass/Fail Criteria
Todos os itens de backup, configuracao e validacao devem ser completados antes de desativar a plataforma de origem. A migracao so e considerada concluida apos 72h de monitoramento sem incidentes.

## If Failed
Executar rollback plan imediatamente. Reativar campanhas na plataforma de origem e investigar a causa raiz antes de tentar novamente.

## Related
- `new-account-onboarding-quality.md`
- `tool-stack-audit.md`
- `../tracking-plan-quality.md`
