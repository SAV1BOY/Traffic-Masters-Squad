# MarTech/AdTech Tool Stack Audit
> **Type**: Quality Gate
> **Domain**: Operations — Infrastructure
> **Reviewed by**: Tech Lead / Media Lead

## Purpose
Garante que o stack de ferramentas de marketing e publicidade esteja atualizado, integrado corretamente e sendo utilizado de forma eficiente. Ferramentas desatualizadas ou mal configuradas comprometem dados e produtividade.

## Checklist

### Inventario de Ferramentas
- [ ] Lista completa de todas as ferramentas em uso documentada
- [ ] Responsavel (owner) definido para cada ferramenta
- [ ] Custo mensal/anual de cada ferramenta registrado
- [ ] Plano/tier de cada ferramenta documentado com limites de uso
- [ ] Ferramentas em trial ou POC identificadas com data de decisao

### Acessos e Seguranca
- [ ] Todos os usuarios ativos revisados — contas inativas desabilitadas
- [ ] Niveis de permissao adequados para cada funcao (admin, editor, viewer)
- [ ] MFA habilitado em todas as ferramentas que suportam
- [ ] SSO configurado quando disponivel
- [ ] Politica de rotacao de senhas seguida
- [ ] Acessos de ex-colaboradores revogados

### Integracoes
- [ ] Integracoes entre ferramentas mapeadas e documentadas (ex: CRM > Ad Platform)
- [ ] Fluxo de dados entre ferramentas validado end-to-end
- [ ] APIs e webhooks funcionando sem erros
- [ ] Dados sincronizando na frequencia esperada
- [ ] Fallback ou alerta configurado para falhas de integracao

### Performance e Utilizacao
- [ ] Taxa de utilizacao de cada ferramenta avaliada (justifica o custo?)
- [ ] Features criticas sendo usadas ou subutilizadas identificadas
- [ ] Overlap de funcionalidades entre ferramentas mapeado
- [ ] Oportunidades de consolidacao identificadas
- [ ] SLAs de uptime e suporte avaliados

### Compliance e Dados
- [ ] Data processing agreements (DPA) assinados com fornecedores relevantes
- [ ] Ferramentas em compliance com LGPD/GDPR
- [ ] Retencao de dados configurada conforme politica da empresa
- [ ] Backup de dados criticos configurado
- [ ] Plano de contingencia documentado para ferramentas criticas

## Pass/Fail Criteria
Todos os itens de seguranca e compliance devem estar em conformidade. Itens de performance e utilizacao sao recomendacoes para otimizacao de custos.

## If Failed
Criar plano de acao com prazos para correcao. Itens de seguranca devem ser resolvidos em ate 48h. Itens de compliance em ate 30 dias.

## Related
- `platform-migration-quality.md`
- `sop-compliance-quality.md`
- `../tracking-plan-quality.md`
