# Naming Convention Compliance Audit
> **Type**: Quality Gate
> **Domain**: Operations — Governance
> **Reviewed by**: Media Buyer / Account Manager

## Purpose
Garante que todas as campanhas, ad sets, ads, audiences e UTMs sigam a naming convention padronizada do time. Nomenclatura inconsistente compromete reporting, filtragem e analise de dados.

## Checklist

### Campaign Level
- [ ] Nome da campanha contem todos os campos obrigatorios (plataforma, objetivo, produto, data)
- [ ] Separadores consistentes utilizados (underscore, pipe ou hifen conforme padrao)
- [ ] Sem caracteres especiais, acentos ou espacos desnecessarios
- [ ] Abreviacoes seguem o glossario documentado do time
- [ ] Campanhas de teste claramente identificadas com prefixo ou sufixo padrao

### Ad Set / Ad Group Level
- [ ] Nome do ad set contem informacao de audience e targeting
- [ ] Diferenciacao clara entre prospecting e retargeting no nome
- [ ] Variantes de teste (A/B) identificadas no nome
- [ ] Funnel stage (TOF/MOF/BOF) presente na nomenclatura
- [ ] Geo-targeting refletido no nome quando aplicavel

### Ad Level
- [ ] Nome do ad contem identificador do criativo (creative ID ou descricao)
- [ ] Formato do criativo indicado (image, video, carousel, etc.)
- [ ] Variante de copy identificada quando em teste
- [ ] Versao do criativo rastreavel pelo nome

### UTM Parameters
- [ ] utm_source corresponde a plataforma correta e em lowercase
- [ ] utm_medium segue o padrao definido (cpc, cpm, paid_social, etc.)
- [ ] utm_campaign e identico ao nome da campanha ou segue mapeamento documentado
- [ ] utm_content utilizado para diferenciar criativos
- [ ] utm_term utilizado para keywords (quando aplicavel)
- [ ] Sem UTMs duplicados, quebrados ou com espacos

### Audiences e Custom Conversions
- [ ] Custom audiences nomeadas com tipo, fonte e data de criacao
- [ ] Lookalike audiences incluem porcentagem e seed audience no nome
- [ ] Custom conversions nomeadas de forma descritiva e padronizada
- [ ] Eventos personalizados seguem naming convention no codigo

## Pass/Fail Criteria
Compliance minima de 95% em todos os niveis. Qualquer campanha com naming incorreto deve ser corrigida em ate 24h apos identificacao.

## If Failed
Gerar lista de itens fora de compliance, corrigir e re-auditar. Campanhas com UTMs incorretos devem ser priorizadas para evitar corrupcao de dados no analytics.

## Related
- `../campaign-build-quality.md`
- `sop-compliance-quality.md`
- `new-account-onboarding-quality.md`
