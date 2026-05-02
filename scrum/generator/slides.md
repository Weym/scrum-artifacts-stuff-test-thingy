---
marp: true
theme: default
paginate: true
style: |
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');
  section {
    font-family: 'Inter', sans-serif;
    color: #374151;
  }
  section.lead {
    background: linear-gradient(135deg, #6C3FE0 0%, #00C9A7 100%);
    color: white;
  }
  section.lead h1 { color: white; }
  section.lead h2 { color: rgba(255,255,255,0.9); }
  section.lead strong { color: white; }
  h1 { color: #6C3FE0; font-weight: 800; }
  h2 { color: #111827; font-weight: 700; }
  strong { color: #6C3FE0; }
  table { font-size: 0.8em; }
  th { background: #F9FAFB; }
---

<!-- _class: lead -->

# Plataforma Academica

## Artefatos Scrum — Sprint Review

**Equipe de 6 membros** | Ciencia da Computacao

Maio 2026

---

# O Projeto

Plataforma academica com chatbot WhatsApp para alunos de Ciencia da Computacao.

- **Auth OTP** — Login seguro via email com codigo de verificacao
- **API REST** — 35 endpoints cobrindo todo o dominio academico
- **AI Chatbot** — Agente inteligente com RAG para atendimento via WhatsApp

**Arquitetura — 4 Servicos**

| FastAPI `:8000` | LangChain `:8001` | MCP Server `:8002` | PostgreSQL `:5432` |
|:---:|:---:|:---:|:---:|
| API Central | Agente IA | Proxy + Logs | Dados + Vetores |

---

# Metodologia

## Como aplicamos Scrum

| Sprint | Foco | Duracao | Membros | Story Points |
|--------|------|---------|---------|-------------|
| Sprint 1 | Planejamento | 16 dias | 1 | -- |
| Sprint 2 | Execucao | 8 dias | 1 | 193 SP |
| Sprint 3 | Demonstracao | 5 dias | 6 | 40 SP |

**Cerimonias realizadas:**
- Planning, Daily (via texto), Review, Retrospectiva

**Papeis definidos:**
- Product Owner, Scrum Master, Dev Team (6 membros)

---

# Product Backlog — 47 User Stories

| Epico | SP |
|-------|---:|
| Autenticacao e Gestao de Sessoes | 26 |
| Gestao de Perfil | 8 |
| Consulta de Notas e Historico | 18 |
| Matricula em Disciplinas | 44 |
| Solicitacao de Documentos | 34 |
| Chatbot WhatsApp (IA) | 34 |
| RAG e Base de Conhecimento | 18 |
| Notificacoes Push (FCM) | 21 |
| Agendamento de Atendimento | 18 |
| Painel Administrativo | 12 |
| **Total** | **233 SP** |

**Priorizacao:** MoSCoW (Must / Should / Could)
Todas as US com criterios de aceitacao e clausula "para que..."

---

# Sprint 1 — Planejamento

**Periodo:** 08/04 - 23/04 (16 dias)
**Goal:** Definir escopo, requisitos, arquitetura e planos de execucao

| Entrega | Quantidade |
|---------|-----------|
| Requisitos funcionais e nao-funcionais | 69 |
| Planos de execucao detalhados | 44 |
| Commits | 39 |
| Documentos de arquitetura | 5 |

**Metricas:**
- **39 commits**, **69 requisitos**, **44 planos**
- Backlog completo com 47 US priorizadas

> "Planning detalhado = execucao rapida"

---

# Burndown — Sprint 2 (Execucao)

**193 SP em 8 dias** | Velocidade: **24.1 SP/dia**

| Dia | SP Entregues | Fases |
|-----|:-----------:|-------|
| 24/04 | **104 SP** | Phase 1 + Phase 2 (Auth, Perfil, Notas, Matricula) |
| 25/04 | **70 SP** | Phase 3 + Phase 4 (Documentos, Chatbot, RAG) |
| 27/04 | **13 SP** | Phase 5 (Notificacoes, Agendamento) |
| 30/04 | **6 SP** | Phase 6 (Admin, Integracao) |

**Total acumulado:** 193/193 SP (100%)

> "Viabilizado por planejamento detalhado + desenvolvimento assistido por IA"

---

# Kanban Board — Sprint 3 (Atual)

**6 membros | 5 dias | 40 SP target | WIP Limit: 1 por membro**

| To Do (7) | In Progress (0) | In Review (0) | Done (59) |
|-----------|----------------|---------------|-----------|
| Frontend telas | -- | -- | API completa |
| Deploy Docker | -- | -- | Chatbot funcional |
| Guardrails IA | -- | -- | RAG pipeline |
| Fix RAG chunks | -- | -- | Auth OTP |
| Testes E2E | -- | -- | 47 US entregues |
| Documentacao | -- | -- | CI/CD base |
| Apresentacao | -- | -- | Banco + migrations |

---

# Definition of Done

## 3 Niveis de Validacao

**Tarefa:**
- Codigo implementado e funcional
- Sem erros de lint ou tipo

**User Story:**
- Todos os criterios de aceitacao atendidos
- Endpoint testavel via HTTP (Postman/curl)
- Documentacao de API atualizada

**Incremento:**
- Servico executa sem erros em ambiente local
- Integracao entre servicos validada

**Trade-offs aceitos para o prazo:**
- Cobertura de testes unitarios minima (foco em testes de integracao)
- Deploy automatizado adiado para Sprint 3

---

# Retrospectiva — Sprint 2

| Start | Stop | Continue |
|-------|------|----------|
| Pair programming nas tarefas complexas | Subestimar tempo de integracao | Planning detalhado antes de codar |
| Code review antes de merge | Trabalhar sem breaks longos | Desenvolvimento assistido por IA |
| Documentar decisoes tecnicas no momento | Deixar testes para o final | Comunicacao diaria via texto |

**Licao principal:**

> "Planning detalhado antes de codar = execucao em 5 dias efetivos"

Sprint 2 entregou **193 SP** com **1 desenvolvedor** porque cada tarefa ja tinha plano de execucao completo.

---

<!-- _class: lead -->

# Resumo

**233 SP** | **47 US** | **316 commits** | **3 Sprints** | **6 membros**

**Artefatos completos:**
Backlog, Sprint Backlog, DoD, DoR, Kanban, Burndown,
Planning, Review, Retro, BDD, Personas

##

**Obrigado — Perguntas?**
