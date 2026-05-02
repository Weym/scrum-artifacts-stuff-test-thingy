# Sprint Planning — Desafio FCG3

**Projeto:** Plataforma Academica com Chatbot WhatsApp  
**Ultima atualizacao:** 2026-05-01  

---

## Sprint 1 Planning — Planejamento

**Data da Planning:** 08/04/2026  
**Participantes:** Tech Lead (1 membro)  
**Duracao da Sprint:** 16 dias (08/04 - 23/04)  
**Capacidade:** 1 pessoa x 16 dias x 4h/dia = 64h disponiveis  

### Sprint Goal

> Definir escopo completo, requisitos validados, arquitetura documentada, e 44 planos de execucao detalhados — prontos para implementacao sem ambiguidade.

### Itens Selecionados do Product Backlog

Nenhum SP comprometido (sprint de planejamento). Os entregaveis sao documentacao:

- Pesquisa de dominio e ecossistema
- REQUIREMENTS.md (69 requisitos)
- ROADMAP.md (6 fases)
- 44 execution plans across 6 phases
- Validation strategies + threat models
- Architecture and database documentation

### Criterios de Sucesso da Sprint 1

1. Todos os requisitos escritos com criterios de aceitacao claros
2. Todas as 6 fases possuem planos de execucao detalhados
3. Cada plano tem task breakdown, dependencias e passos de verificacao
4. Threat models cobrem autenticacao e padroes de acesso a dados

### Riscos Identificados na Planning

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|------|---------|-----------|
| Scope creep durante planejamento | Media | Alto | Timebox rigido por documento |
| Over-engineering dos planos | Media | Medio | Foco em MVP — cortar complexidade especulativa |

---

## Sprint 2 Planning — Execucao

**Data da Planning:** 23/04/2026  
**Participantes:** Tech Lead (1 membro)  
**Duracao da Sprint:** 8 dias (23/04 - 30/04)  
**Capacidade:** 1 pessoa x 8 dias x 8h/dia = 64h disponiveis (intensivo)  

### Sprint Goal

> Implementar todo o backend (API REST, MCP Server, AI Service, WhatsApp Webhook) com o fluxo end-to-end funcional em ambiente Docker local.

### Itens Selecionados do Product Backlog

| Epico | User Stories | SP Total |
|-------|-------------|----------|
| 1. Infraestrutura | US-001 a US-004 | 24 |
| 2. Autenticacao | US-005 a US-009 | 26 |
| 3. Gestao Academica | US-010 a US-022 | 78 |
| 4. MCP Server | US-023 a US-027 | 32 |
| 5. AI Service | US-028 a US-031 | 34 |
| 6. WhatsApp Webhook | US-033 a US-037 | 24 |
| **Total comprometido** | **30 User Stories** | **193 SP** |

*Nota: SP alto viavel devido ao planejamento completo na Sprint 1 + desenvolvimento assistido por IA.*

### Criterios de Sucesso da Sprint 2

1. `docker compose up` sobe 4 containers saudaveis
2. Todos os 35 endpoints REST respondem corretamente
3. MCP Server chama tools e loga acoes
4. AI Service responde perguntas em portugues usando tools + RAG
5. Webhook WhatsApp recebe e responde mensagens

### Riscos Identificados na Planning Sprint 2

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|------|---------|-----------|
| Complexidade de integracao entre 4 servicos | Alta | Alto | Resolver infraestrutura primeiro (Phase 1) |
| PGVector + LangChain podem ter incompatibilidades | Media | Medio | Pesquisa previa documentada |
| SELECT FOR UPDATE + async pode gerar deadlocks | Media | Medio | Testes focados em concorrencia |
| OpenAI API pode ter mudancas/instabilidade | Baixa | Alto | Implementar provider agnostico |

---

## Sprint 3 Planning — Demonstracao

**Data da Planning:** 01/05/2026  
**Participantes:** 6 membros (Tech Lead + 5)  
**Duracao da Sprint:** 5 dias (01/05 - 05/05)  
**Capacidade:** 6 pessoas x 5 dias x 3.5h/dia = 105h disponiveis  
*(3.5h/dia considerando que o time e junior e trabalha parcialmente no projeto)*

### Sprint Goal

> Tornar o sistema demonstravel para a apresentacao do dia 06/05 — com frontend minimo funcional, chatbot WhatsApp respondendo ao vivo, guardrails de seguranca testados, e todos os artefatos Scrum completos.

### Itens Selecionados do Product Backlog

| Epico | User Stories | SP Total | Responsavel |
|-------|-------------|----------|-------------|
| 5. AI Service (gap) | US-030, US-032 | 11 | Tech Lead |
| 7. Frontend | US-038, US-039, US-040 | 16 | Membro 1 + 2 |
| 8. Guardrails | US-041, US-042 | 8 | Membro 4 |
| 9. Deploy | US-043, US-044 | 10 | Tech Lead |
| — Scrum/Apresentacao | (nao mapeado em SP) | — | Membro 5 |
| — Knowledge Base | (suporte a US-030/031) | — | Membro 3 |
| **Total comprometido** | **8 User Stories** | **40 SP** |

### Capacidade por Membro

| Membro | Horas Disponiveis | Tarefas | SP Alvo |
|--------|-------------------|---------|---------|
| Tech Lead | 5 x 5h = 25h | 13 | 19 |
| Membro 1 | 5 x 3.5h = 17.5h | 8 | 8 |
| Membro 2 | 5 x 3.5h = 17.5h | 8 | 11 |
| Membro 3 | 5 x 3.5h = 17.5h | 8 | 5 (+suporte) |
| Membro 4 | 5 x 3.5h = 17.5h | 8 | 8 |
| Membro 5 | 5 x 3.5h = 17.5h | 8 | — (scrum) |

### Criterios de Sucesso da Sprint 3

1. RAG retorna chunks relevantes com threshold 0.45 (fix validado)
2. Frontend Flutter: login OTP + dashboard com dados reais funcionam
3. Deploy no servidor: `docker compose up` funciona remotamente
4. WhatsApp webhook aponta pro servidor e responde ao vivo
5. System prompt rejeita prompt injection (testado)
6. Artefatos Scrum completos e visiveis (Backlog, DoD, Kanban, Burndown)
7. Demo ensaiada com roteiro definido

### Riscos Identificados na Planning Sprint 3

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|------|---------|-----------|
| Docker nao funciona no servidor | Media | Critico | Plano B: ngrok local |
| Time junior nao entrega frontend a tempo | Media | Alto | Telas minimas (2-3 apenas) |
| WhatsApp webhook nao verifica sem HTTPS | Alta | Alto | Usar ngrok com HTTPS |
| RAG threshold 0.45 ainda filtra demais | Baixa | Medio | Pode baixar para 0.35 |
| Perguntas na demo saem do escopo | Media | Media | Roteiro com "perguntas seguras" |

### Acordos do Time

1. **Daily standup:** Quick update diario no grupo (texto, nao chamada) — o que fez, o que vai fazer, bloqueios
2. **WIP limit:** 1 tarefa por pessoa de cada vez
3. **Comunicacao de bloqueio:** Avisar IMEDIATAMENTE se travou (nao esperar daily)
4. **Code review:** Revisao rapida (pode ser verbal/screen share)
5. **Deadline real:** Tudo deve estar pronto ate 05/05 as 22h para permitir ajustes
6. **Plano B da demo:** Gravar video ate 04/05 caso algo falhe ao vivo

---

## Definicao de "Pronto para Planning"

Um item do Product Backlog esta pronto para ser selecionado na Sprint quando:

- [ ] User Story escrita com criterios de aceitacao claros
- [ ] Dependencias tecnicas identificadas
- [ ] Estimativa em SP atribuida
- [ ] Acesso/ferramentas necessarias disponíveis
- [ ] Nenhum impedimento externo conhecido

---

## Sprint Planning Checklist

- [x] Product Backlog revisado e priorizado
- [x] Sprint Goal definida
- [x] Capacidade do time calculada
- [x] Itens selecionados e comprometidos
- [x] Tarefas quebradas (Sprint Backlog)
- [x] Dependencias mapeadas
- [x] Riscos identificados
- [x] Acordos do time registrados
- [x] DoD revisada e aceita pelo time
