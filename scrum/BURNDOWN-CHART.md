# Burndown Chart — Desafio FCG3

**Projeto:** Plataforma Academica com Chatbot WhatsApp  
**Ultima atualizacao:** 2026-05-01  

---

## Sprint 1: Planejamento (08/04 a 23/04)

**Tipo:** Sprint de planejamento  
**Duracao:** 16 dias  
**Story Points entregues:** 0 (output e documentacao, nao codigo)  
**Commits totais:** 39  
**Resultado:** Todos os artefatos de planejamento criados e validados

### Entregas de Planejamento

| Data | Entrega | Commits |
|------|---------|---------|
| 08/04 | Repositorio criado | 1 |
| 13/04 | Planejamento inicial | 1 |
| 14/04 | Revisao e expansao do planejamento | 1 |
| 15/04 | Pesquisa de ecossistema + requisitos + roadmap | 7 |
| 20/04 | Contexto das 6 fases capturado | 8 |
| 22/04 | Contexto fases 5-6 | 2 |
| 23/04 | Todos os 44 plans criados + validacao | 19 |

### Grafico de Progresso Sprint 1 (Artefatos de Planejamento)

```
Commits (acumulado)
 39  |                                                    *
     |                                                   /
 35  |                                                  /
     |                                                 /
 30  |                                                /
     |                                               /
 25  |                                              /
     |                                             /
 20  |                                  *---------*
     |                                 /
 15  |                                /
     |                          *----*
 10  |                    *----*
     |                   /
  5  |                  /
     |            *    /
  2  |     *--*--*
  1  |  *
  0  |___________________________________________________
     08   13   14   15   16   17   18   19   20   21   22   23
                              Abril 2026

     * Commits acumulados por dia
```

### Analise Sprint 1

| Metrica | Valor |
|---------|-------|
| **Duracao** | 16 dias (08/04 - 23/04) |
| **Story Points** | 0 (sprint de planejamento) |
| **Commits** | 39 |
| **Artefatos gerados** | 44 plans de execucao + requisitos + roadmap |
| **Dias ativos** | 7 de 16 |
| **Padrao observado** | Crescimento progressivo — pesquisa inicial, depois captura massiva de contexto |

---

## Sprint 2: Execucao (23/04 a 30/04)

**Total planejado:** 193 Story Points  
**Duracao:** 8 dias  
**Entregue:** 193 SP  
**Resultado:** Sprint Goal atingida — backend completo com todas as 6 fases implementadas

### Dados Diarios (Story Points Restantes)

| Data | SP Restantes | SP Entregues no Dia | Ideal | Commits | Observacao |
|------|-------------|--------------------|---------|---------|----|
| 23/04 (Inicio) | 193 | 0 | 193 | (planning commits) | Inicio da sprint |
| 24/04 | 89 | 104 | 169 | 106 | Phase 1 + Phase 2 + inicio Phase 3 |
| 25/04 | 19 | 70 | 145 | 110 | Phase 3 completa + Phase 4 completa |
| 26/04 | 19 | 0 | 121 | 6 | Estabilizacao |
| 27/04 | 6 | 13 | 97 | 20 | Phase 5 fixes (embedding, UUID, OpenRouter) |
| 28/04 | 6 | 0 | 72 | 0 | — |
| 29/04 | 6 | 0 | 48 | 1 | Config ajuste .env.example |
| 30/04 | 0 | 6 | 0 | 34 | Phase 6 completa + UAT final |

### Grafico Burndown Sprint 2

```
SP Restantes
200 |*
    | \  Ideal
180 |  - .
    |    - .
160 |      - .
    |        - .
140 |          - .
    |            - .
120 |              - .
    |                - .
100 |           *      - .
    |            \       - .
 80 |             \        - .
    |              \         - .
 60 |               \          - .
    |                \           - .
 40 |                 \            - .
    |                  *---*         - .
 20 |                       \          - .
    |                        *--*--*     - .
  0 |________________________________________*
    23   24   25   26   27   28   29   30
                   Abril 2026

    --- Ideal (linear)     * Real
```

### Analise Sprint 2

| Metrica | Valor |
|---------|-------|
| **Velocidade total** | 193 SP / 8 dias = 24.1 SP/dia |
| **Dias efetivos de codigo** | 4 dias (24, 25, 27, 30) |
| **Velocidade efetiva** | 48.25 SP/dia em dias de codigo |
| **Maior dia** | 24/04 — 104 SP (Phase 1 + 2 + inicio Phase 3) |
| **Padrao observado** | Execucao concentrada apos planejamento detalhado |
| **Burst pattern** | 90% do trabalho concluido nos dias 24-25 (174 de 193 SP) |
| **Risco materializado** | RAG threshold (gap tecnico descoberto no UAT dia 30) |

---

## Sprint 3: Demonstracao (01/05 a 05/05)

**Total planejado:** 40 Story Points  
**Status:** Em andamento  
**Membros:** 6  
**Meta:** Sistema demonstravel com frontend + WhatsApp + artefatos Scrum

### Dados Diarios (Story Points Restantes) — Projecao

| Data | SP Restantes (Ideal) | SP Restantes (Projecao) | Observacao |
|------|---------------------|------------------------|-----|
| 01/05 (Inicio) | 40 | 40 | Inicio da sprint |
| 01/05 (Fim dia) | 32 | 34 | RAG fix + inicio frontend |
| 02/05 (Fim dia) | 24 | 26 | Deploy + frontend avancando |
| 03/05 (Fim dia) | 16 | 18 | Frontend pronto + KB pronta |
| 04/05 (Fim dia) | 8 | 10 | Guardrails + integracao |
| 05/05 (Fim dia) | 0 | 2 | E2E test + ensaio demo (buffer) |

### Grafico Burndown Sprint 3 (Projecao)

```
SP Restantes
 40  |*
     | \.
     |  \ .
 34  |   *  .  (projecao ligeiramente atras do ideal)
     |    \  .
     |     \  .
 26  |      *  .
     |       \  .
     |        \  .
 18  |         *  .
     |          \  .
     |           \  .
 10  |            *  .
     |             \  .
     |              \  .
  2  |               *  .
  0  |_______________....*
     01    02    03    04    05
              Maio 2026

     * Projecao real     . Ideal (linear)
```

### Distribuicao de SP por Dia (Sprint 3)

| Dia | SP Alvo | Tarefas Principais |
|-----|---------|-------------------|
| 01/05 (Qui) | 6 SP | RAG fix + MCP UUID + Docker no servidor + inicio frontend |
| 02/05 (Sex) | 8 SP | Deploy funcional + Frontend login avancando + KB docs |
| 03/05 (Sab) | 8 SP | Frontend dashboard + RAG testado + Prompt hardening |
| 04/05 (Dom) | 8 SP | Guardrails validados + E2E parcial + Slides |
| 05/05 (Seg) | 10 SP | E2E final + Ensaio demo + Ultimos ajustes |

### Nota sobre Sprint 3

A projecao mostra a equipe ligeiramente atras do ideal — isso e realista para uma equipe junior em primeira sprint colaborativa. O buffer de 2 SP no dia final absorve imprevistos.

---

## Burndown Acumulado (Projeto Completo)

### Progresso Total: 233 SP (meta)

| Fase | Data | SP Acumulado |
|------|------|-------------|
| Sprint 1 end | 23/04 | 0 (planning only) |
| Sprint 2 start | 23/04 | 0 |
| Sprint 2 day 2 | 24/04 | 104 |
| Sprint 2 day 3 | 25/04 | 174 |
| Sprint 2 day 5 | 27/04 | 187 |
| Sprint 2 end | 30/04 | 193 |
| Sprint 3 end | 05/05 | 233 (target) |

### Grafico Acumulado

```
SP Entregues (acumulado)
 240 |                                              *  (meta)
     |                                           /
 220 |                                        /
     |                                     /
 200 |                                  *
     |                                 /
 180 |                              *
     |                             /
 160 |                            /
     |                           /
 140 |                          /
     |                         /
 120 |                        /
     |                       /
 100 |                    *
     |                   /
  80 |                  /
     |                 /
  60 |                /
     |               /
  40 |              /
     |             /
  20 |            /
     |           /
   0 |*--------*...............* - - - - - - - - - - *
     08   13   15   20   23   24   25   26   27   28   29   30   01   05
     |------- Sprint 1 -------|------- Sprint 2 ---------|-- Sprint 3 --|
              Abril                                            Maio
```

---

## Metricas de Velocidade

| Metrica | Sprint 1 | Sprint 2 | Sprint 3 (projecao) |
|---------|----------|----------|-------------------|
| **Duracao** | 16 dias | 8 dias | 5 dias |
| **Story Points** | 0 | 193 | 40 (planejado) |
| **Membros ativos** | 1 (Tech Lead) | 1 (Tech Lead) | 6 |
| **Velocidade (SP/dia)** | N/A (planning) | 24.1 | 8.0 (necessario) |
| **Commits totais** | 39 | 277 | — |

---

## Observacoes para a Apresentacao

1. **Sprint 1 nao possui burndown tradicional** — e uma sprint de planejamento onde o output sao artefatos de documentacao (44 plans, requisitos, roadmap). O progresso e medido por entregas de planejamento, nao story points.

2. **O burndown da Sprint 2 mostra um padrao "burst"** — 90% do trabalho entregue nos dias 24-25 (174 de 193 SP). Isso e resultado direto do planejamento pesado da Sprint 1. Uma unica pessoa executou apos ter planos detalhados para cada fase.

3. **Sprint 3 tem distribuicao mais uniforme** porque ha 6 pessoas trabalhando em paralelo em dominios diferentes (frontend, backend, KB, prompt, scrum).

4. **A velocidade de 8 SP/dia na Sprint 3 e viavel** dado que:
   - O trabalho mais complexo (backend) ja esta feito
   - As tarefas restantes sao mais independentes
   - Ha 6 membros vs 1 nas Sprints 1 e 2

5. **A separacao em 3 sprints reflete a realidade do projeto:**
   - Sprint 1: Planejamento solo (1 pessoa, 0 SP, 39 commits de docs)
   - Sprint 2: Execucao solo (1 pessoa, 193 SP, 277 commits de codigo)
   - Sprint 3: Demonstracao colaborativa (6 pessoas, 40 SP planejados)

6. **Recomendacao para o grafico visual:** usar ferramenta como Google Sheets ou Notion com chart para gerar um grafico mais bonito para os slides.
