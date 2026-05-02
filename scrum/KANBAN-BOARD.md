# Kanban Board — Desafio FCG3

**Projeto:** Plataforma Academica com Chatbot WhatsApp  
**Sprint:** Sprint 2 (01/05 - 05/05)  
**Ultima atualizacao:** 2026-05-01 (inicio da sprint)  

---

## Legenda

| Coluna | Significado | WIP Limit |
|--------|-------------|-----------|
| **Backlog** | Tarefa identificada, ainda nao iniciada | Sem limite |
| **To Do** | Comprometida na sprint, pronta para iniciar | 10 |
| **In Progress** | Alguem esta trabalhando ativamente | 6 (1 por membro) |
| **In Review** | Aguardando validacao/teste por outro membro | 4 |
| **Done** | Atende todos os criterios da DoD | Sem limite |
| **Blocked** | Impedimento externo, nao pode avancar | — |

---

## Board Estado Atual (01/05/2026)

### DONE (Sprint 1 — completas)

| ID | Tarefa | Responsavel | Concluida |
|----|--------|-------------|-----------|
| T-001 a T-059 | **59 tarefas da Sprint 1** (ver Sprint Backlog para detalhes) | Tech Lead | 30/04 |

> **Resumo Sprint 1 Done:**
> - Infraestrutura Docker (4 containers, migrations, seed) 
> - Autenticacao completa (OTP, JWT, roles, middleware) 
> - 35 endpoints REST (7 feature slices) 
> - MCP Server (16 tools, logging, retry, student_id injection) 
> - AI Service (ReAct agent, RAG pipeline, ingest, memoria) 
> - WhatsApp Webhook (HMAC, dedup, background tasks, chat visibility) 

---

### BLOCKED

| ID | Tarefa | Responsavel | Bloqueio | Acao |
|----|--------|-------------|----------|------|
| — | (nenhuma tarefa bloqueada no inicio da sprint) | — | — | — |

---

### IN PROGRESS

| ID | Tarefa | Responsavel | Iniciada | Notas |
|----|--------|-------------|----------|-------|
| — | (sprint inicia agora — nenhuma tarefa em andamento ainda) | — | — | — |

---

### TO DO — Tech Lead (Integracao + Deploy)

| ID | Tarefa | Prioridade | Estimativa | Dia Alvo |
|----|--------|-----------|------------|----------|
| T-060 | Adicionar RAG_SIMILARITY_THRESHOLD ao config.py (default 0.45) | Critica | 1h | 01/05 |
| T-061 | Refatorar rag.py para aceitar threshold como parametro | Critica | 1h | 01/05 |
| T-062 | Passar settings.RAG_SIMILARITY_THRESHOLD no agent.py | Critica | 0.5h | 01/05 |
| T-063 | Atualizar/criar testes do RAG threshold | Critica | 1h | 01/05 |
| T-064 | Adicionar gen_random_uuid() no INSERT de mcp_action_logs | Critica | 0.5h | 01/05 |
| T-065 | Atualizar testes do middleware MCP | Critica | 0.5h | 01/05 |
| T-066 | Testar RAG end-to-end (ingest + query) | Alta | 1h | 01/05 |
| T-067 | Instalar Docker e Docker Compose no servidor | Alta | 2h | 01-02/05 |
| T-068 | Clonar repo e configurar .env no servidor | Alta | 1h | 02/05 |
| T-069 | Executar docker compose up no servidor | Alta | 2h | 02/05 |
| T-070 | Configurar DNS/ngrok para webhook WhatsApp | Alta | 3h | 03-04/05 |
| T-071 | Rodar alembic upgrade + seed + ingest no servidor | Alta | 1h | 02/05 |
| T-072 | Teste end-to-end WhatsApp -> servidor -> resposta | Alta | 2h | 04-05/05 |

---

### TO DO — Membro 1 (Frontend Login)

| ID | Tarefa | Prioridade | Estimativa | Dia Alvo |
|----|--------|-----------|------------|----------|
| T-073 | Criar tela de input de email (UI) | Alta | 3h | 01/05 |
| T-074 | Implementar chamada POST /auth/request-code | Alta | 2h | 01-02/05 |
| T-075 | Criar tela de input de OTP (6 digitos) | Alta | 3h | 02/05 |
| T-076 | Implementar chamada POST /auth/verify-code | Alta | 2h | 02-03/05 |
| T-077 | Armazenar JWT (flutter_secure_storage) | Media | 2h | 03/05 |
| T-078 | Navegacao pos-login para Dashboard | Media | 1h | 03/05 |
| T-079 | Tratamento de erros (codigo invalido, expirado) | Media | 2h | 04/05 |
| T-080 | Loading states e feedback visual | Baixa | 2h | 04-05/05 |

---

### TO DO — Membro 2 (Frontend Dashboard)

| ID | Tarefa | Prioridade | Estimativa | Dia Alvo |
|----|--------|-----------|------------|----------|
| T-081 | Criar tela Dashboard com layout (AppBar + body) | Alta | 3h | 01/05 |
| T-082 | Implementar chamada GET /students/{id}/academic-summary | Alta | 2h | 01-02/05 |
| T-083 | Card de resumo academico (semestre, CRA, status) | Alta | 2h | 02/05 |
| T-084 | Lista de disciplinas disponiveis | Alta | 3h | 02-03/05 |
| T-085 | Lista de notas | Alta | 3h | 03/05 |
| T-086 | Botao de logout (POST /auth/logout + limpar storage) | Media | 1h | 03/05 |
| T-087 | Tratamento de erros e token expirado (redirect login) | Media | 2h | 04/05 |
| T-088 | Loading states e pull-to-refresh | Baixa | 2h | 04-05/05 |

---

### TO DO — Membro 3 (Knowledge Base + RAG Testing)

| ID | Tarefa | Prioridade | Estimativa | Dia Alvo |
|----|--------|-----------|------------|----------|
| T-089 | Escrever/revisar matricula.md (regras reais do curso) | Alta | 3h | 01/05 |
| T-090 | Escrever/revisar faq.md (15-20 perguntas) | Alta | 3h | 01-02/05 |
| T-091 | Escrever/revisar calendario.md (datas academicas) | Alta | 2h | 02/05 |
| T-092 | Escrever/revisar curriculo.md (grade completa) | Alta | 2h | 02-03/05 |
| T-093 | Rodar ingest e validar que chunks foram criados | Alta | 1h | 03/05 |
| T-094 | Testar 10 queries no RAG e documentar resultados | Alta | 3h | 03-04/05 |
| T-095 | Testar privacidade: aluno A nao acessa dados de B | Media | 2h | 04/05 |
| T-096 | Documentar score de similaridade por query (planilha) | Media | 2h | 04-05/05 |

---

### TO DO — Membro 4 (Prompt Engineering + Guardrails)

| ID | Tarefa | Prioridade | Estimativa | Dia Alvo |
|----|--------|-----------|------------|----------|
| T-097 | Revisar system prompt atual do agente | Alta | 2h | 01/05 |
| T-098 | Adicionar instrucoes anti-injection no system prompt | Alta | 3h | 01-02/05 |
| T-099 | Adicionar instrucoes de escopo (so academico) | Alta | 2h | 02/05 |
| T-100 | Testar 10 cenarios de prompt injection | Alta | 3h | 02-03/05 |
| T-101 | Testar tom e linguagem (PT-BR institucional) | Media | 2h | 03/05 |
| T-102 | Testar cenarios de privacidade via prompt | Media | 2h | 03-04/05 |
| T-103 | Documentar limitacoes conhecidas do chatbot | Media | 2h | 04/05 |
| T-104 | Criar "perguntas seguras" para demo (roteiro) | Alta | 1h | 05/05 |

---

### TO DO — Membro 5 (Scrum + Apresentacao)

| ID | Tarefa | Prioridade | Estimativa | Dia Alvo |
|----|--------|-----------|------------|----------|
| T-105 | Montar Product Backlog visual (Trello/Notion) | Alta | 3h | 01/05 |
| T-106 | Montar Sprint Backlog visual com horas | Alta | 2h | 01/05 |
| T-107 | Criar Kanban Board em ferramenta visual | Alta | 2h | 01-02/05 |
| T-108 | Criar Burndown Chart grafico (Google Sheets) | Alta | 3h | 02/05 |
| T-109 | Escrever Definition of Done formal | Media | 1h | 02/05 |
| T-110 | Montar slides da apresentacao | Alta | 4h | 03-04/05 |
| T-111 | Escrever roteiro da demo (passo a passo) | Alta | 2h | 04/05 |
| T-112 | Ensaio da apresentacao com o time | Alta | 2h | 05/05 |

---

## Fluxo de Trabalho

```
+----------+     +--------+     +-------------+     +-----------+     +------+
|          |     |        |     |             |     |           |     |      |
| BACKLOG  | --> | TO DO  | --> | IN PROGRESS | --> | IN REVIEW | --> | DONE |
|          |     |        |     |             |     |           |     |      |
+----------+     +--------+     +-------------+     +-----------+     +------+
                                       |
                                       v
                                 +---------+
                                 | BLOCKED |
                                 +---------+
```

### Regras de Transicao

| De → Para | Condicao |
|-----------|----------|
| Backlog → To Do | Comprometida na Sprint Planning |
| To Do → In Progress | Membro assume a tarefa |
| In Progress → In Review | Codigo pronto, precisa validacao |
| In Review → Done | Validacao OK, atende DoD |
| In Review → In Progress | Feedback: precisa de ajuste |
| Qualquer → Blocked | Impedimento externo identificado |
| Blocked → In Progress | Impedimento resolvido |

---

## Metricas do Board

| Metrica | Valor Atual | Meta |
|---------|-------------|------|
| Tarefas em To Do | 53 | 0 ao final da sprint |
| Tarefas In Progress | 0 | Max 6 simultaneas |
| Tarefas Done (Sprint 2) | 0 | 53 ao final |
| Lead Time medio | — | < 1 dia |
| Cycle Time medio | — | < 4 horas |
| Tarefas Blocked | 0 | 0 |

---

## Instrucoes para Uso

1. **Cada membro** move suas tarefas quando mudar de estado
2. **Atualizar diariamente** (ao final do dia ou no inicio do dia seguinte)
3. **Se bloqueado**, mover para Blocked E avisar no grupo imediatamente
4. **WIP limit**: nao pegar nova tarefa se ja tem 1 In Progress (foco!)
5. **Code review**: so mover para Done apos outro membro validar (pode ser verbal)

### Ferramentas Sugeridas para Board Visual

| Ferramenta | Preco | Recomendacao |
|-----------|-------|------|
| **Trello** | Gratis | Mais simples, bom para times pequenos |
| **GitHub Projects** | Gratis | Integrado com o repo |
| **Notion** | Gratis (edu) | Mais flexivel, bom para docs tambem |
| **Jira** | Gratis (10 users) | Mais completo mas mais complexo |

**Recomendacao:** Usar **Trello** ou **GitHub Projects** por simplicidade. O Membro 5 deve replicar este board em uma dessas ferramentas no Dia 1.
