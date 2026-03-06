# ARCHITECTURE — Traffic Masters Squad

## Visao Geral do Sistema

O Traffic Masters Squad opera como um **sistema de agentes interconectados** onde cada tarefa e roteada pelo `config.yaml` para os agentes, frameworks, checklists e templates corretos.

```
                    ┌─────────────────┐
                    │  TRAFFIC CHIEF  │ ← Orquestrador
                    │  (Governanca)   │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────┴───┐  ┌──────┴─────┐  ┌────┴────────┐
     │  RESEARCH   │  │  STRATEGY  │  │  EXECUTION  │
     │  LAYER      │  │  LAYER     │  │  LAYER      │
     └────────┬───┘  └──────┬─────┘  └────┬────────┘
              │              │              │
              └──────────────┼──────────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────┴───┐  ┌──────┴─────┐  ┌────┴────────┐
     │  CREATIVE   │  │  TRACKING  │  │  ANALYSIS   │
     │  LAYER      │  │  LAYER     │  │  LAYER      │
     └────────┬───┘  └──────┬─────┘  └────┬────────┘
              │              │              │
              └──────────────┼──────────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────┴───┐  ┌──────┴─────┐  ┌────┴────────┐
     │  OPTIMIZE   │  │   SCALE    │  │  GOVERNANCE │
     │  LAYER      │  │   LAYER    │  │  LAYER      │
     └─────────────┘  └────────────┘  └─────────────┘
```

## Fluxo Principal

```
Research → Strategy → Creative → Setup → Launch → Optimize → Scale → Report
   │          │          │         │        │         │         │        │
   ▼          ▼          ▼         ▼        ▼         ▼         ▼        ▼
 Avatar    Funnel     Angles    Build    Go-Live   Diagnose  Budget   Learnings
 ICP       Budget     Hooks     Track    QA        Cut/Add   Expand   Decisions
 Offer     Channel    Scripts   Pixel    Monitor   Iterate   Diversif Report
```

## Camadas de Execucao (Stack)

### 1. Discovery Layer (`frameworks/discovery-layer.md`)
- Pesquisa de mercado, avatar, concorrencia, oferta
- **Agents**: depesh-mandalia, nicholas-kusmich, traffic-chief
- **Frameworks**: mandalia-5w-avatar, kusmich-targeting-trifecta, icp-and-avatar

### 2. Strategy Layer (`frameworks/strategy-layer.md`)
- Funil, canal, metas, unit economics
- **Agents**: traffic-chief, molly-pittman, ralph-burns
- **Frameworks**: pittman-traffic-engine-9-steps, burns-caamp, ltv-cac-unit-economics

### 3. Creative Layer (`frameworks/creative-layer.md`)
- Angulos, hooks, scripts, assets
- **Agents**: ad-midas, creative-analyst, ralph-burns, tom-breeze
- **Frameworks**: burns-kaizen-kreative, creative-angle-matrix, breeze-aducate

### 4. Media Buying Layer (`frameworks/media-buying-layer.md`)
- Estrutura, segmentacao, bidding, pacing
- **Agents**: media-buyer, kasim-aslam, molly-pittman, pedro-sobral
- **Frameworks**: account-structure-meta, aslam-4-core-campaign-types

### 5. Tracking Layer (`frameworks/tracking-layer.md`)
- Eventos, UTMs, validacao e governanca
- **Agents**: pixel-specialist
- **Frameworks**: tracking-stack-standard

### 6. Optimization Layer (`frameworks/optimization-layer.md`)
- Diagnostico, cortes, realocacao, iteracao
- **Agents**: performance-analyst, media-buyer, depesh-mandalia
- **Frameworks**: mandalia-punisher-method, sobral-geco-ana

### 7. Scaling Layer (`frameworks/scaling-layer.md`)
- Estabilidade, diversificacao, novos canais
- **Agents**: scale-optimizer, depesh-mandalia, nicholas-kusmich
- **Frameworks**: mandalia-scaling-recipes, kusmich-ponds-lakes-oceans

### 8. Governance Layer (`frameworks/governance-layer.md`)
- Politicas, compliance, financas, auditoria
- **Agents**: traffic-chief, fiscal, ads-analyst
- **Frameworks**: policy-risk-classification

## Diagrama de Dependencias

```
Agent → Framework → Checklist → Template → Registry
  │         │           │           │          │
  │         │           │           │          └── data/registries/*.yaml
  │         │           │           └── templates/**/*.md
  │         │           └── checklists/**/*.md
  │         └── frameworks/*.md
  └── agents/*.md
```

### Regra de Ouro
Toda tarefa no squad segue este ciclo:
1. **Agent** recebe a tarefa (via config.yaml routing)
2. **Framework** define o "como" (metodologia)
3. **Checklist** valida a qualidade (quality gate)
4. **Template** formata o output (padrao)
5. **Registry** registra o resultado (memoria)
6. **Metrics** mede o impacto (aprendizado)

## Mapa de Agentes por Dominio

```
┌─────────────────────────────────────────────────────────┐
│                    TRAFFIC CHIEF                         │
│              (Orquestrador / Governanca)                 │
├─────────────┬────────────────┬──────────────────────────┤
│  RESEARCH   │    CREATIVE    │      EXECUTION           │
│             │                │                          │
│ Mandalia    │  Ad Midas      │  Media Buyer             │
│ Kusmich     │  Creative      │  Pixel Specialist        │
│ Ads Analyst │  Analyst       │  Pedro Sobral            │
│             │  Tom Breeze    │  Kasim Aslam             │
│             │  Ralph Burns   │  Molly Pittman           │
├─────────────┴────────────────┴──────────────────────────┤
│  OPTIMIZATION          │        GOVERNANCE              │
│                        │                                │
│  Performance Analyst   │  Fiscal                        │
│  Scale Optimizer       │  Traffic Chief (review)        │
│  Depesh Mandalia       │  Ads Analyst (audit)           │
└────────────────────────┴────────────────────────────────┘
```

## Cross-Squad Integration

### Traffic → Copy Squad
- **Envia**: Creative performance data, audience insights, winning hooks
- **Recebe**: Ad copy (headlines, primary text, CTAs), VSL scripts, LP copy

### Traffic → Brand Squad
- **Envia**: Distinctive asset performance, brand awareness metrics
- **Recebe**: Brand voice guide, guidelines visuais, positioning statement

## Principios Arquiteturais

1. **Routing via config.yaml** — Toda tarefa e roteada; nenhum agente age "sozinho"
2. **Quality gates obrigatorios** — Nenhum output sai sem passar por pelo menos 1 checklist
3. **Registry on completion** — Todo resultado e registrado em data/registries/
4. **Learnings-first** — Metricas e learnings alimentam decisoes futuras
5. **Modularidade** — Cada arquivo e autocontido e referenciavel

## Ciclo de Maturidade

```
Level 1: Setup        → Agents + Frameworks + Config
Level 2: Operational  → Checklists + Templates + Tasks + Workflows
Level 3: Data-Rich    → Reference + Swipe + Registries + Metrics
Level 4: Mature       → Lib + Voice + Archive + Authority + Docs
```
