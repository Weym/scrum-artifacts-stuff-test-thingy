# Sprint Backlog — Desafio FCG3

**Projeto:** Plataforma Academica com Chatbot WhatsApp  
**Scrum Master:** [Nome]  
**Equipe:** 6 membros  
**Sprints:** 3 (Planejamento + Execucao + Demonstracao)  
**Periodo total:** 08/04/2026 a 05/05/2026  
**Ultima atualizacao:** 2026-05-01  

---

## Sprint 1 — Planejamento (Retroativa)

**Periodo:** 08/04/2026 a 23/04/2026 (16 dias)  
**Sprint Goal:** Definir escopo, requisitos, arquitetura e planos de execucao detalhados para todas as 6 fases do backend + AI + MCP.  
**Velocidade realizada:** 0 SP (planning sprint — no code delivered)  
**Status:** Concluida

### Tarefas Sprint 1

| # | Tarefa | Responsavel | Status |
|---|--------|-------------|--------|
| T-001 | Pesquisa de ecossistema e dominio | Equipe | Done |
| T-002 | Definicao de 69 requisitos (REQUIREMENTS.md) | Equipe | Done |
| T-003 | Roadmap com 6 fases (ROADMAP.md) | Equipe | Done |
| T-004 | 44 planos de execucao detalhados | Tech Lead | Done |
| T-005 | Validacao de arquitetura e threat models | Tech Lead | Done |
| T-006 | Contexto das 6 fases capturado | Equipe | Done |

**Total Sprint 1:** 6 entregas de planejamento | 0 SP entregues

---

## Sprint 2 — Execucao (Retroativa)

**Periodo:** 23/04/2026 a 30/04/2026 (8 dias)  
**Sprint Goal:** Implementar todo o backend (API REST, MCP Server, AI Service, WhatsApp Webhook) com o fluxo end-to-end funcional em ambiente Docker local.  
**Velocidade realizada:** 193 SP em 8 dias = 24.1 SP/dia  
**Equipe ativa:** 1 membro (Tech Lead)  
**Status:** Concluida (com 1 gap remanescente no RAG threshold)

### Tarefas Sprint 2

| # | Tarefa | User Story | Responsavel | Estimativa (h) | Real (h) | Status |
|---|--------|-----------|-------------|---------------|---------|--------|
| T-001 | Definir docker-compose.yml com 4 servicos e healthchecks | US-001 | Tech Lead | 4 | 3 | Done |
| T-002 | Configurar redes app-network e data-network | US-001 | Tech Lead | 2 | 1 | Done |
| T-003 | Criar hot-reload com bind mounts para desenvolvimento | US-001 | Tech Lead | 2 | 2 | Done |
| T-004 | Configurar Alembic com async engine | US-002 | Tech Lead | 4 | 3 | Done |
| T-005 | Migration #001: extensao pgvector | US-002 | Tech Lead | 1 | 0.5 | Done |
| T-006 | Migrations #002-#009: todas as tabelas da aplicacao | US-002 | Tech Lead | 8 | 6 | Done |
| T-007 | Criar index HNSW em knowledge_base_chunks.embedding | US-002 | Tech Lead | 1 | 0.5 | Done |
| T-008 | Documentar variaveis de ambiente em .env.example | US-003 | Tech Lead | 2 | 2 | Done |
| T-009 | Criar settings.py com Pydantic BaseSettings | US-003 | Tech Lead | 2 | 2 | Done |
| T-010 | Implementar script seed destrutivo (curriculo + fixtures) | US-004 | Tech Lead | 4 | 3 | Done |
| T-011 | Criar endpoint POST /auth/request-code | US-005 | Tech Lead | 3 | 2 | Done |
| T-012 | Integrar Resend SDK para envio de email OTP | US-005 | Tech Lead | 2 | 2 | Done |
| T-013 | Implementar rate limiting com SlowAPI | US-005 | Tech Lead | 2 | 2 | Done |
| T-014 | Criar endpoint POST /auth/verify-code | US-006 | Tech Lead | 4 | 3 | Done |
| T-015 | Implementar logica de tentativas (3 max + invalidacao) | US-006 | Tech Lead | 3 | 2 | Done |
| T-016 | Gerar JWT com role + jti + sessao no banco | US-006 | Tech Lead | 3 | 2 | Done |
| T-017 | Criar endpoint POST /auth/logout + revogacao por jti | US-007 | Tech Lead | 2 | 1.5 | Done |
| T-018 | Criar endpoint GET /auth/me | US-008 | Tech Lead | 1 | 0.5 | Done |
| T-019 | Implementar middleware get_current_user + require_role | US-009 | Tech Lead | 3 | 2 | Done |
| T-020 | Implementar dependency require_service_token | US-009 | Tech Lead | 2 | 1 | Done |
| T-021 | CRUD de alunos (list, create, update, soft-delete) | US-010 | Tech Lead | 6 | 5 | Done |
| T-022 | Endpoint resumo academico com calculo de CRA | US-011 | Tech Lead | 4 | 4 | Done |
| T-023 | Endpoint disciplinas disponiveis com filtro de pre-requisitos | US-012 | Tech Lead | 4 | 3 | Done |
| T-024 | Listagem de disciplinas + detalhe + arvore CTE recursiva | US-013 | Tech Lead | 6 | 5 | Done |
| T-025 | Corrigir bug de ciclo na arvore de pre-requisitos | US-013 | Tech Lead | 3 | 2 | Done |
| T-026 | Fluxo completo de matricula (draft -> confirm -> lock) | US-014 | Tech Lead | 8 | 7 | Done |
| T-027 | Validacoes: periodo ativo, pre-requisitos, duplicatas | US-014 | Tech Lead | 4 | 3 | Done |
| T-028 | Check constraint migration para status 'locked' | US-014 | Tech Lead | 2 | 2 | Done |
| T-029 | CRUD periodos de matricula (staff) | US-015 | Tech Lead | 3 | 2 | Done |
| T-030 | Endpoints de notas por disciplina/periodo + historico | US-016 | Tech Lead | 4 | 3 | Done |
| T-031 | Endpoint staff lancar/atualizar notas | US-017 | Tech Lead | 3 | 2 | Done |
| T-032 | Endpoints documentos: solicitar, listar, detalhe | US-018 | Tech Lead | 4 | 3 | Done |
| T-033 | Endpoint staff atualizar status documento | US-019 | Tech Lead | 2 | 1.5 | Done |
| T-034 | Endpoints agendamento: slots, booking (SELECT FOR UPDATE), cancel | US-020 | Tech Lead | 6 | 5 | Done |
| T-035 | Endpoint staff criar slots | US-021 | Tech Lead | 2 | 1.5 | Done |
| T-036 | Dashboard staff com KPIs agregados | US-022 | Tech Lead | 3 | 2 | Done |
| T-037 | Scaffold MCP Server com FastMCP | US-023 | Tech Lead | 4 | 3 | Done |
| T-038 | Implementar 7 tools read-only (Group A) | US-023 | Tech Lead | 6 | 4 | Done |
| T-039 | Implementar 9 tools write/action (Group B) | US-023 | Tech Lead | 8 | 6 | Done |
| T-040 | Implementar injecao de student_id por sessao | US-024 | Tech Lead | 4 | 3 | Done |
| T-041 | Implementar middleware de logging (mcp_action_logs) | US-025 | Tech Lead | 3 | 2 | Done |
| T-042 | Validacao X-Service-Token no MCP | US-026 | Tech Lead | 2 | 1 | Done |
| T-043 | Logica de retry (1x para 5xx, nenhum para 4xx) | US-027 | Tech Lead | 2 | 1.5 | Done |
| T-044 | Scaffold AI Service (FastAPI + config + LLM factory) | US-028 | Tech Lead | 4 | 3 | Done |
| T-045 | Implementar agente ReAct com MCP tool binding | US-028 | Tech Lead | 6 | 5 | Done |
| T-046 | Endpoint /chat com persistencia de mensagens | US-028 | Tech Lead | 4 | 3 | Done |
| T-047 | Implementar memoria de conversa (k=20) do banco | US-029 | Tech Lead | 3 | 2 | Done |
| T-048 | Implementar RAG pipeline com PGVector | US-030 | Tech Lead | 4 | 3 | Done |
| T-049 | Script de ingest (chunking + embeddings) | US-031 | Tech Lead | 4 | 3 | Done |
| T-050 | Webhook GET (challenge verification) | US-033 | Tech Lead | 1 | 0.5 | Done |
| T-051 | Webhook POST (HMAC validation + message parsing) | US-033 | Tech Lead | 4 | 3 | Done |
| T-052 | Background task com asyncio.create_task + done_callback | US-034 | Tech Lead | 3 | 2 | Done |
| T-053 | Per-session lock + retry + fallback response | US-034 | Tech Lead | 3 | 2 | Done |
| T-054 | Handler de mensagens de midia (resposta padrao) | US-035 | Tech Lead | 2 | 1 | Done |
| T-055 | Deduplicacao por whatsapp_message_id + indice parcial | US-036 | Tech Lead | 2 | 1.5 | Done |
| T-056 | Endpoints staff: chat sessions, messages, MCP logs | US-037 | Tech Lead | 4 | 3 | Done |
| T-057 | Testes automatizados webhook (HMAC, dedup, midia) | US-047 | Tech Lead | 4 | 3 | Done |
| T-058 | Testes automatizados service token e IDOR | US-047 | Tech Lead | 3 | 2 | Done |
| T-059 | Gap closures diversos (imports, Docker, credentials) | — | Tech Lead | 12 | 12 | Done |

**Total Sprint 2:** 59 tarefas | Estimado: 207h | Real: ~163h

---

## Sprint 3 — Demonstracao (Atual)

**Periodo:** 01/05/2026 a 05/05/2026 (5 dias uteis)  
**Sprint Goal:** Tornar o sistema demonstravel — fix do RAG, frontend minimo, deploy no servidor, guardrails do chatbot, e todos os artefatos Scrum completos para apresentacao do dia 06/05.  
**Capacidade estimada:** 40 SP / 6 membros / 5 dias = ~6.5 SP/membro  
**Status:** Em andamento

### Tarefas Sprint 3

| # | Tarefa | User Story | Responsavel | Estimativa (h) | Status | Dia |
|---|--------|-----------|-------------|---------------|--------|-----|
| **RAG + MCP Fix (Tech Lead)** |
| T-060 | Adicionar RAG_SIMILARITY_THRESHOLD ao config.py (default 0.45) | US-030 | Tech Lead | 1 | To Do | 1 |
| T-061 | Refatorar rag.py para aceitar threshold como parametro | US-030 | Tech Lead | 1 | To Do | 1 |
| T-062 | Passar settings.RAG_SIMILARITY_THRESHOLD no agent.py | US-030 | Tech Lead | 0.5 | To Do | 1 |
| T-063 | Atualizar/criar testes do RAG threshold | US-030 | Tech Lead | 1 | To Do | 1 |
| T-064 | Adicionar gen_random_uuid() no INSERT de mcp_action_logs | US-032 | Tech Lead | 0.5 | To Do | 1 |
| T-065 | Atualizar testes do middleware MCP | US-032 | Tech Lead | 0.5 | To Do | 1 |
| T-066 | Testar RAG end-to-end (ingest + query) | US-030 | Tech Lead | 1 | To Do | 1 |
| **Deploy (Tech Lead)** |
| T-067 | Instalar Docker e Docker Compose no servidor | US-043 | Tech Lead | 2 | To Do | 1-2 |
| T-068 | Clonar repo e configurar .env no servidor | US-043 | Tech Lead | 1 | To Do | 2 |
| T-069 | Executar docker compose up no servidor | US-043 | Tech Lead | 2 | To Do | 2 |
| T-070 | Configurar DNS/ngrok para webhook WhatsApp | US-043 | Tech Lead | 3 | To Do | 3-4 |
| T-071 | Rodar alembic upgrade + seed + ingest no servidor | US-043 | Tech Lead | 1 | To Do | 2 |
| T-072 | Teste end-to-end WhatsApp -> servidor -> resposta | US-044 | Tech Lead | 2 | To Do | 4-5 |
| **Frontend Login (Membro 1)** |
| T-073 | Criar tela de input de email (UI) | US-038 | Membro 1 | 3 | To Do | 1 |
| T-074 | Implementar chamada POST /auth/request-code | US-038 | Membro 1 | 2 | To Do | 1-2 |
| T-075 | Criar tela de input de OTP (6 digitos) | US-038 | Membro 1 | 3 | To Do | 2 |
| T-076 | Implementar chamada POST /auth/verify-code | US-038 | Membro 1 | 2 | To Do | 2-3 |
| T-077 | Armazenar JWT (flutter_secure_storage) | US-038 | Membro 1 | 2 | To Do | 3 |
| T-078 | Navegacao pos-login para Dashboard | US-038 | Membro 1 | 1 | To Do | 3 |
| T-079 | Tratamento de erros (codigo invalido, expirado) | US-038 | Membro 1 | 2 | To Do | 4 |
| T-080 | Loading states e feedback visual | US-040 | Membro 1 | 2 | To Do | 4-5 |
| **Frontend Dashboard (Membro 2)** |
| T-081 | Criar tela Dashboard com layout (AppBar + body) | US-039 | Membro 2 | 3 | To Do | 1 |
| T-082 | Implementar chamada GET /students/{id}/academic-summary | US-039 | Membro 2 | 2 | To Do | 1-2 |
| T-083 | Card de resumo academico (semestre, CRA, status) | US-039 | Membro 2 | 2 | To Do | 2 |
| T-084 | Lista de disciplinas disponiveis (GET /students/{id}/available-courses) | US-039 | Membro 2 | 3 | To Do | 2-3 |
| T-085 | Lista de notas (GET /students/{id}/grades) | US-039 | Membro 2 | 3 | To Do | 3 |
| T-086 | Botao de logout (POST /auth/logout + limpar storage) | US-039 | Membro 2 | 1 | To Do | 3 |
| T-087 | Tratamento de erros e token expirado (redirect login) | US-040 | Membro 2 | 2 | To Do | 4 |
| T-088 | Loading states e pull-to-refresh | US-040 | Membro 2 | 2 | To Do | 4-5 |
| **Knowledge Base (Membro 3)** |
| T-089 | Escrever/revisar matricula.md (regras reais do curso) | US-031 | Membro 3 | 3 | To Do | 1 |
| T-090 | Escrever/revisar faq.md (15-20 perguntas) | US-031 | Membro 3 | 3 | To Do | 1-2 |
| T-091 | Escrever/revisar calendario.md (datas academicas) | US-031 | Membro 3 | 2 | To Do | 2 |
| T-092 | Escrever/revisar curriculo.md (grade completa) | US-031 | Membro 3 | 2 | To Do | 2-3 |
| T-093 | Rodar ingest e validar que chunks foram criados | US-031 | Membro 3 | 1 | To Do | 3 |
| T-094 | Testar 10 queries no RAG e documentar resultados | US-030 | Membro 3 | 3 | To Do | 3-4 |
| T-095 | Testar privacidade: aluno A nao acessa dados de B | US-042 | Membro 3 | 2 | To Do | 4 |
| T-096 | Documentar score de similaridade por query (planilha) | US-030 | Membro 3 | 2 | To Do | 4-5 |
| **Prompt Engineering (Membro 4)** |
| T-097 | Revisar system prompt atual do agente | US-041 | Membro 4 | 2 | To Do | 1 |
| T-098 | Adicionar instrucoes anti-injection no system prompt | US-041 | Membro 4 | 3 | To Do | 1-2 |
| T-099 | Adicionar instrucoes de escopo (so academico) | US-041 | Membro 4 | 2 | To Do | 2 |
| T-100 | Testar 10 cenarios de prompt injection | US-041 | Membro 4 | 3 | To Do | 2-3 |
| T-101 | Testar tom e linguagem (PT-BR institucional) | US-041 | Membro 4 | 2 | To Do | 3 |
| T-102 | Testar cenarios de privacidade via prompt | US-042 | Membro 4 | 2 | To Do | 3-4 |
| T-103 | Documentar limitacoes conhecidas do chatbot | US-041 | Membro 4 | 2 | To Do | 4 |
| T-104 | Criar "perguntas seguras" para demo (roteiro) | US-041 | Membro 4 | 1 | To Do | 5 |
| **Scrum + Apresentacao (Membro 5)** |
| T-105 | Montar Product Backlog visual (Trello/Notion) | — | Membro 5 | 3 | To Do | 1 |
| T-106 | Montar Sprint Backlog visual com horas | — | Membro 5 | 2 | To Do | 1 |
| T-107 | Criar Kanban Board com todas as tarefas | — | Membro 5 | 2 | To Do | 1-2 |
| T-108 | Criar Burndown Chart (retroativo + sprint 3) | — | Membro 5 | 3 | To Do | 2 |
| T-109 | Escrever Definition of Done formal | — | Membro 5 | 1 | To Do | 2 |
| T-110 | Montar slides da apresentacao | — | Membro 5 | 4 | To Do | 3-4 |
| T-111 | Escrever roteiro da demo (passo a passo) | — | Membro 5 | 2 | To Do | 4 |
| T-112 | Ensaio da apresentacao com o time | — | Membro 5 | 2 | To Do | 5 |

**Total Sprint 3:** 53 tarefas | Estimado: ~110h (distribuidas em 6 pessoas x 5 dias x ~4h/dia)

---

## Resumo por Membro (Sprint 3)

| Membro | Tarefas | Horas Estimadas | SP |
|--------|---------|-----------------|-----|
| Tech Lead | 13 tarefas | ~17h | 16 |
| Membro 1 (Flutter Login) | 8 tarefas | ~17h | 8 |
| Membro 2 (Flutter Dashboard) | 8 tarefas | ~18h | 11 |
| Membro 3 (Knowledge Base) | 8 tarefas | ~18h | 8 |
| Membro 4 (Prompt/Guardrails) | 8 tarefas | ~17h | 8 |
| Membro 5 (Scrum/Apresentacao) | 8 tarefas | ~19h | — |

---

## Dependencias Criticas (Sprint 3)

```
T-060/T-064 (RAG fix) ──> T-093 (ingest) ──> T-094 (teste RAG)
                                            ──> T-100 (teste injection)

T-069 (deploy servidor) ──> T-070 (webhook DNS) ──> T-072 (E2E test)

T-078 (nav pos-login) ──> depende de T-081 (dashboard pronto)

T-104 (perguntas demo) ──> T-111 (roteiro demo) ──> T-112 (ensaio)
```

---

## Impedimentos Conhecidos

| # | Impedimento | Impacto | Responsavel | Status |
|---|-------------|---------|-------------|--------|
| IMP-01 | Docker pode nao estar no servidor do Kenji | Bloqueia deploy | Tech Lead | A resolver dia 1 |
| IMP-02 | Chave OpenAI para embeddings pode nao funcionar | Bloqueia ingest | Tech Lead | Validar dia 1 |
| IMP-03 | Meta webhook verification pode falhar sem HTTPS | Bloqueia E2E | Tech Lead | Plano B: ngrok |
