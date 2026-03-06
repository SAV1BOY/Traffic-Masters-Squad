# Privacy/Consent Compliance Quality (LGPD/GDPR)
> **Type**: Quality Gate
> **Domain**: Advanced — Privacy & Compliance
> **Reviewed by**: Media Lead / DPO / Legal

## Purpose
Garante que todas as operacoes de midia paga estejam em conformidade com legislacoes de privacidade (LGPD, GDPR) e respeitem o consentimento dos usuarios, evitando multas, danos a reputacao e violacoes legais.

## Checklist

### Consentimento e Opt-in
- [ ] Consent banner (CMP) implementado e funcionando corretamente no site
- [ ] Categorias de consentimento configuradas (necessario, analytics, marketing, personalizacao)
- [ ] Pixels e tags de ads so disparam apos consentimento explicito do usuario
- [ ] Google Consent Mode v2 implementado e configurado
- [ ] Registro de consentimento armazenado com timestamp e versao da politica
- [ ] Mecanismo de revogacao de consentimento funcional e acessivel

### Tratamento de Dados Pessoais
- [ ] Dados PII hasheados (SHA256) antes de upload para plataformas de ads
- [ ] Customer lists enviadas via canais seguros (upload direto, nao email)
- [ ] Retencao de dados pessoais em listas de audiencia conforme politica definida
- [ ] Processo de exclusao de dados pessoais (right to be forgotten) implementado
- [ ] Dados de menores de idade excluidos de custom audiences

### Plataformas de Ads
- [ ] Data Processing Agreements (DPA) assinados com todas as plataformas utilizadas
- [ ] Configuracoes de privacidade de cada plataforma revisadas e adequadas
- [ ] Limited Data Use (LDU) habilitado no Meta quando necessario
- [ ] Restricted Data Processing habilitado no Google quando necessario
- [ ] Funcionalidades de Enhanced Conversions / Advanced Matching em compliance

### Tracking e Medicao
- [ ] Cookies de terceiros nao sao utilizados sem consentimento
- [ ] Server-side tracking (CAPI) configurado para reduzir dependencia de cookies
- [ ] Conversion modeling habilitado para preencher gaps de dados com consentimento
- [ ] First-party data strategy implementada como base do tracking
- [ ] Privacy sandbox / Topics API avaliado e implementado quando disponivel

### Documentacao e Governanca
- [ ] Politica de privacidade do site atualizada e referencia todas as plataformas de ads
- [ ] ROPA (Record of Processing Activities) inclui atividades de midia paga
- [ ] DPIA (Data Protection Impact Assessment) realizada para novas atividades de alto risco
- [ ] Processo de notificacao de incidentes de dados documentado
- [ ] Time treinado em boas praticas de privacidade aplicadas a midia paga
- [ ] Auditoria de compliance agendada (semestral)

### Compliance Regional
- [ ] Requisitos da LGPD atendidos para operacoes no Brasil
- [ ] Requisitos do GDPR atendidos para operacoes na Europa (quando aplicavel)
- [ ] CCPA/CPRA compliance para operacoes nos EUA (quando aplicavel)
- [ ] Regulacoes locais adicionais mapeadas e atendidas

## Pass/Fail Criteria
Todos os itens de consentimento, tratamento de dados pessoais e documentacao sao obrigatorios e bloqueantes. Nenhuma campanha pode ser lancada sem compliance verificada. Violacoes devem ser escaladas imediatamente.

## If Failed
Pausar imediatamente qualquer atividade em non-compliance. Escalar para DPO e jurídico em ate 24h. Documentar o incidente e implementar correcoes antes de retomar operacoes.

## Related
- `audience-suppression-quality.md`
- `../tracking-plan-quality.md`
- `../pixel-and-capi-quality.md`
