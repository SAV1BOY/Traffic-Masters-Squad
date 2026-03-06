# Audience Suppression and Exclusion Quality
> **Type**: Quality Gate
> **Domain**: Advanced — Audience Management
> **Reviewed by**: Media Buyer / Data Analyst

## Purpose
Garante que listas de supressao e exclusao de audiencia estejam configuradas corretamente em todas as plataformas, evitando desperdicio de budget em usuarios ja convertidos, overlap entre campanhas e violacoes de privacidade.

## Checklist

### Listas de Supressao
- [ ] Clientes existentes excluidos de campanhas de prospecting/aquisicao
- [ ] Leads ja convertidos excluidos de campanhas de lead generation
- [ ] Usuarios que optaram por opt-out excluidos de todas as campanhas
- [ ] Listas de supressao atualizadas na frequencia adequada (diaria ou semanal)
- [ ] Tamanho das listas de supressao monitorado para detectar anomalias

### Configuracao por Plataforma
- [ ] Custom audiences de supressao carregadas corretamente em cada plataforma
- [ ] Match rate das listas verificado e dentro do esperado
- [ ] Audiences de supressao aplicadas no nivel correto (campaign ou ad set)
- [ ] Exclusoes de retargeting configuradas para evitar overlap com prospecting
- [ ] Exclusoes de lookalike audiences configuradas para remover seed list

### Overlap e Frequencia
- [ ] Audience overlap entre ad sets analisado e minimizado
- [ ] Exclusoes entre ad sets aplicadas para prevenir competicao interna de leilao
- [ ] Frequency cap configurado por campanha e por conta quando possivel
- [ ] Usuarios com alta frequencia (>X impressoes) suprimidos de campanhas de awareness

### Segmentacao Negativa
- [ ] Negative keywords atualizadas e revisadas para campanhas de search
- [ ] Placement exclusions configuradas (sites, apps, categorias de conteudo)
- [ ] Brand safety exclusions aplicadas em todas as campanhas
- [ ] Topic e category exclusions relevantes ativadas

### Compliance e Privacidade
- [ ] Listas de supressao tratadas conforme LGPD/GDPR (dados pessoais protegidos)
- [ ] Processos de opt-out respeitados em todas as plataformas
- [ ] Retencao de dados nas listas de supressao conforme politica de privacidade
- [ ] Hashing aplicado em dados PII antes do upload (SHA256)
- [ ] Audit trail de uploads e atualizacoes de listas mantido

## Pass/Fail Criteria
Todos os itens de listas de supressao e compliance sao obrigatorios. Itens de overlap e segmentacao negativa devem ter compliance minima de 90%.

## If Failed
Corrigir exclusoes imediatamente para evitar desperdicio de budget. Violacoes de privacidade devem ser escaladas para o DPO em ate 24h.

## Related
- `privacy-compliance-quality.md`
- `../campaign-build-quality.md`
- `geo-targeting-quality.md`
