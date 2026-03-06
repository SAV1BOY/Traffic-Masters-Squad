# Lookalike Expansion

> **Type**: Task
> **Category**: scaling
> **Agents**: Kusmich, Traffic Chief, Mandalia
> **Frameworks**: Kusmich Audience Architecture, Progressive Scaling Framework
> **Checklists**: scaling-checklist, lookalike-expansion-checklist
> **Output template**: templates/scaling-report-document.md

## Objective
Expandir audiências lookalike progressivamente de 1% para 3% e 5%, aumentando o volume de conversões mantendo o CPA dentro dos limites aceitáveis através de um processo controlado de scaling.

## Inputs
- Lookalike audiences existentes (1%) com performance validada
- Dados de performance das campanhas de lookalike atuais (CPA, ROAS, CVR)
- Seed audiences segmentadas por valor (purchasers, high-LTV, leads qualificados)
- Budget incremental aprovado para scaling
- CPA ceiling e ROAS floor definidos como guardrails

## Steps
1. Auditar a performance atual das lookalike 1% em todas as plataformas (CPA, ROAS, volume)
2. Identificar as seed audiences com melhor performance para priorizar a expansão
3. Criar lookalike 2-3% a partir das seed audiences top-performing
4. Lançar as lookalike 3% em ad sets separados com budget controlado (50% do budget da 1%)
5. Excluir a lookalike 1% da lookalike 3% para testar apenas o incremento
6. Monitorar a performance por 7-14 dias comparando CPA da 3% vs. 1%
7. Se a 3% performar dentro do CPA ceiling (+20% máximo), expandir para lookalike 5%
8. Criar lookalike 5% excluindo 1% e 3% para isolar o incremento
9. Testar broad targeting (sem lookalike) como controle para comparar com lookalike expandida
10. Consolidar os learnings: qual % de lookalike oferece o melhor equilíbrio volume vs. CPA
11. Implementar a estrutura final de lookalike em produção com budgets proporcionais
12. Documentar o playbook de lookalike expansion com critérios de go/no-go por tier

## Output
Relatório de lookalike expansion contendo: performance comparativa por tier (1%, 3%, 5%), análise de CPA incremental, recomendação de estrutura final, budget allocation por tier, e playbook de expansão.

## Quality Gate
- Cada tier de lookalike testado por mínimo de 7 dias com budget suficiente para significância
- CPA da tier expandida não ultrapassa o ceiling em mais de 20%
- Exclusões entre tiers configuradas corretamente para evitar overlap
- Broad targeting testado como controle
- Traffic Chief aprova cada fase de expansão antes de prosseguir para o próximo tier

## Duration
2-3 horas para setup de cada tier; 4-6 semanas para ciclo completo de teste e validação
