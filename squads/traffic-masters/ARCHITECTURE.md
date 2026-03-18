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

---

## HRM Governance Model

```
┌─────────────────────────────────────────────────────────────┐
│                    HRM CENTRAL COMMAND                       │
│              (Cross-Squad Orchestration)                     │
├─────────────────────────────────────────────────────────────┤
│                    TRAFFIC CHIEF                             │
│              (Squad-Level Authority)                         │
│  Decides: task priority, budget allocation, go/no-go        │
│  Approves: strategy, scaling, new channels, final outputs   │
│  Escalates to: HRM Central when cross-squad conflict        │
├──────────┬──────────┬──────────┬──────────┬────────────────┤
│ RESEARCH │ CREATIVE │EXECUTION │  OPTIM.  │  GOVERNANCE    │
│  TEAM    │  TEAM    │  TEAM    │  TEAM    │    TEAM        │
│          │          │          │          │                │
│ Lead:    │ Lead:    │ Lead:    │ Lead:    │ Lead:          │
│ traffic- │ ad-midas │ media-   │ perf-    │ traffic-chief  │
│ chief    │          │ buyer    │ analyst  │                │
│          │          │          │          │                │
│ Members: │ Members: │ Members: │ Members: │ Members:       │
│ mandalia │ creative-│ pixel-   │ scale-   │ fiscal         │
│ kusmich  │ analyst  │ spec.    │ optimizer│ ads-analyst    │
│ ads-     │ breeze   │ aslam    │ mandalia │                │
│ analyst  │ burns    │ pittman  │          │                │
│          │          │ sobral   │          │                │
└──────────┴──────────┴──────────┴──────────┴────────────────┘
```

### Decision Rights Matrix

| Decision Type | Agent Level | Team Lead | Traffic Chief | HRM Central |
|---------------|:-----------:|:---------:|:-------------:|:-----------:|
| Creative angle selection | ✅ Decide | — | — | — |
| Budget micro-adjustment (<5%) | ✅ Decide | — | — | — |
| Campaign pause/resume | — | ✅ Decide | Informed | — |
| Budget reallocation (>10%) | — | Recommend | ✅ Decide | Informed |
| New channel launch | — | — | ✅ Decide | Informed |
| Strategy pivot | — | — | ✅ Decide | Approve |
| Cross-squad SLA change | — | — | Recommend | ✅ Decide |
| Squad scope expansion | — | — | Recommend | ✅ Decide |

### Approval Chains

1. **Standard task output**: Agent → Team Lead review → Done
2. **Strategy deliverable**: Agent → Team Lead → Traffic Chief approval → Done
3. **Client-facing output**: Agent → Team Lead → Traffic Chief → Client approval
4. **Cross-squad handoff**: Agent → Traffic Chief → Counterpart Squad Chief → Done
5. **Budget change >20%**: Agent → Traffic Chief → Fiscal validation → HRM Central

---

## Rework & Quality Loop Protocol

```
Task Output
    │
    ▼
Quality Gate Check
    │
    ├── PASS → Registry update → Next step
    │
    └── FAIL → Feedback with specific failure reasons
              │
              ▼
         Agent Revision (Attempt 1)
              │
              ▼
         Quality Gate Re-check
              │
              ├── PASS → Continue
              │
              └── FAIL → Escalate to Team Lead
                        │
                        ▼
                   Team Lead Direction
                        │
                        ▼
                   Agent Revision (Attempt 2)
                        │
                        ▼
                   Quality Gate Re-check
                        │
                        ├── PASS → Continue
                        │
                        └── FAIL → Escalate to Traffic Chief
                                  │
                                  ▼
                             Chief Decision:
                             a) Approve with documented exceptions
                             b) Reassign to different agent
                             c) Restructure the approach entirely
```

### Rework Rules
- **Max iterations**: 3 per quality gate
- **Timeout**: 4h per iteration (standard), 1h (urgent)
- **Documentation**: Every rework cycle is logged in `data/registries/decisions-log.yaml`
- **Pattern detection**: If the same gate fails on 3+ consecutive tasks, the framework or checklist is reviewed for recalibration

---

## Ambiguity Resolution Protocol

When a task arrives with incomplete or ambiguous information:

1. **Classify the ambiguity**:
   - **Missing data**: Required inputs not provided → Request from task originator with specific questions
   - **Unclear objective**: Goal is vague → Traffic Chief clarifies with stakeholder before assigning
   - **Conflicting priorities**: Multiple valid approaches → Use decision matrix (ICE score: Impact × Confidence × Ease)
   - **Out-of-scope elements**: Task contains work for another squad → Split task, delegate the cross-squad portion

2. **Default behaviors when information is missing**:
   - Budget not specified → Use `defaults.budget_model` (70/20/10)
   - Attribution window not specified → Use `defaults.attribution_window` (7d click, 1d view)
   - Platform not specified → Default to Meta (largest channel), expand based on results
   - KPI not specified → Use CAC/ROAS as primary, with MER as blended check

3. **Escalation on ambiguity**:
   - Agent cannot resolve → Team Lead
   - Team Lead cannot resolve → Traffic Chief
   - Traffic Chief cannot resolve → HRM Central + stakeholder consultation

---

## Out-of-Scope Handling

### Scope Boundaries

The Traffic Masters Squad handles:
- Paid media strategy, setup, optimization, and scaling
- Creative strategy and briefing (not production)
- Tracking and attribution setup
- Performance analysis and reporting
- Budget management and financial reconciliation

The Traffic Masters Squad does NOT handle:
- Organic content creation → Content Squad
- Long-form copywriting → Copy Squad
- Brand identity design → Brand Squad
- CRM/sales pipeline management → Sales Squad
- Data warehouse/BI infrastructure → Analytics Squad
- Product pricing/feature decisions → Product Squad

### Delegation Protocol

```
1. Agent identifies out-of-scope element
2. Agent flags to Traffic Chief with:
   - What is out of scope
   - Which squad should handle it
   - What Traffic Masters needs back (output spec)
   - By when (SLA request)
3. Traffic Chief creates handoff using `workflows/cross-squad-handoff-workflow.md`
4. Handoff logged in `data/registries/decisions-log.yaml`
5. Traffic Chief monitors SLA compliance
6. On delivery, Traffic Chief validates output meets spec
7. If output inadequate → return with specific feedback + new SLA
```

---

## Memory & Learning System

### How the Squad Learns

```
Task Execution → Output → Registry Update → Metrics Collection
                                                    │
                                                    ▼
                                          Learnings Analysis
                                          (weekly review)
                                                    │
                                                    ▼
                                     ┌──────────────┼──────────────┐
                                     │              │              │
                              Framework      Checklist      Strategy
                              Refinement     Update         Adjustment
```

### Registry Feedback Loop (Kaizen)

1. **Every task completion** updates the relevant registry in `data/registries/`
2. **Weekly review** (Traffic Chief + Performance Analyst) analyzes:
   - `data/metrics/weekly-scorecards.md` for trend detection
   - `data/registries/lessons-learned-registry.yaml` for pattern recognition
   - `data/registries/experiments-registry.yaml` for hypothesis validation
3. **Monthly deep-dive** produces:
   - Updated benchmarks in `data/research/platform-benchmarks/`
   - Framework refinements if patterns suggest methodology gaps
   - New checklist items if recurring quality failures detected
4. **Quarterly calibration** triggers:
   - Full review of all quality gate thresholds
   - Agent capability assessment
   - Cross-squad SLA performance review
   - Maturity score update in `data/metrics/maturity-score-history.md`

### Decision Traceability

Every significant decision is recorded in `data/registries/decisions-log.yaml` with:
- Context and alternatives considered
- Chosen approach and rationale
- Expected outcome and actual outcome (updated post-execution)
- Review date for reassessment

This creates an institutional memory that prevents repeated mistakes and enables new team members to understand historical context.

---

## Conflict Resolution

### Between Agents (Same Squad)

| Conflict Type | Resolution |
|---------------|------------|
| Methodology disagreement (e.g., broad vs. interest targeting) | Data decides: run A/B test, let metrics determine winner |
| Priority conflict (two tasks competing for same agent) | Traffic Chief prioritizes using ICE score |
| Quality standard disagreement | Checklist is authoritative; if checklist is unclear, Traffic Chief arbitrates |
| Resource allocation (budget split between channels) | Performance data + Traffic Chief decision |

### Between Squads

| Conflict Type | Resolution |
|---------------|------------|
| SLA breach by another squad | Traffic Chief escalates to counterpart Chief; if unresolved in 24h → HRM Central |
| Contradictory guidance (Brand says X, Traffic data says Y) | Joint review meeting; data-informed compromise; Traffic Chief + Brand Chief decide |
| Scope overlap (both squads claim a task) | HRM Central defines ownership based on primary value driver |
| Resource contention (shared assets/tools) | HRM Central allocates based on business priority |

---

## Cross-Document Reference Map

### Core Navigation

| Starting Point | Connects To |
|----------------|-------------|
| `config.yaml` | All agents, frameworks, checklists, templates, registries |
| `ARCHITECTURE.md` | System overview, team structure, governance model |
| `agents/*.md` | Tasks, frameworks, checklists, templates (via FILE REFERENCES section) |
| `tasks/**/*.md` | Agents, frameworks, checklists, templates, registries (via ROUTING section) |
| `workflows/*.md` | Tasks, agents, quality gates, handoffs |
| `docs/quality-gates-guide.md` | All checklists, all workflows |
| `docs/cross-squad-integration.md` | Cross-squad handoffs, shared assets |
| `data/registries/*.yaml` | Task outputs, decisions, learnings |
| `data/metrics/*.md` | KPIs, scorecards, performance tracking |

### Dependency Chain

```
config.yaml (routing brain)
    → agents/*.md (who executes)
        → frameworks/*.md (how they execute)
            → checklists/*.md (quality validation)
                → templates/*.md (output format)
                    → data/registries/*.yaml (memory storage)
                        → data/metrics/*.md (performance measurement)
                            → workflows/*.md (end-to-end orchestration)
                                → docs/*.md (governance and guides)
```
