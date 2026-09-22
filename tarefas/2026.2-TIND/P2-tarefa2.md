# P2 — Detalhamento, Arquitetura e Implementação Inicial (Individual · YP-Agentic)

**Disciplina:** Engenharia de Software II — DCT2302
**Turma:** 2026.2-TIND (Ensino Individualizado)
**Processo:** [YP-Agentic](../../yp-agentic/manual-passo-a-passo.md)
**Iteração:** 1 · Fases 4–6 (Planejamento de Iteração, Implementação e Implantação)
**Prazo:** **06/10/2026**
**Discente:** Artur Morais Candeia

## 1. Contexto

Continuação da **P1**. Nesta tarefa você detalha a arquitetura, planeja a primeira iteração e entrega a **fatia vertical "Gestão de Eventos"** (da tela ao banco), com testes. Leia novamente o `yp-agentic/manual-passo-a-passo.md` e o Anexo A da P1 (estado atual do SIGAEX).

> **Escopo externo ao P2:** Usuários/Perfil, Inscrições e Check-in/Presença ficam para **P3/P4**.

## 2. Entregáveis

### 2.1 Documento de Arquitetura — `backend/docs/arquitetura.md` (ou `doc-arquitetura.md`)
Conforme `templates/doc-arquitetura.md`:
- Visão geral das camadas (Frontend Vue 3/Vite ↔ Backend Django REST ↔ Banco).
- Diagrama de componentes (Mermaid) e tabela de tecnologias com justificativa.
- **Decisões Arquiteturais (ADRs):** ex., API REST por ViewSets, autenticação JWT + permissões por papel, organização de pastas, estratégia de testes e cobertura.

### 2.2 Plano de Iteração — `backend/docs/plano-iteracao.md`
- Atualizar com a fatia **Gestão de Eventos** (US-01 a US-04), tarefas, critérios BDD e responsáveis (você, com agentes de IA).

### 2.3 Implementação da fatia "Gestão de Eventos"

**Backend (sigaex-backend):**
- Substituir `AllowAny` por permissões coerentes com a autenticação JWT (organizador autenticado cria/edita/remove; leitura pública conforme status).
- Concluir/validar os endpoints do módulo Evento (CRUD + customizados já previstos nos docs: `eventos_ativos`, `proximos_eventos`, `eventos_encerrados`, `estatisticas`, `validar_evento`).
- **Testes de API** com `APITestCase` (Django REST Framework) cobrindo todos os endpoints (criar, listar, recuperar, atualizar, excluir, ações customizadas e validações).
- Cobertura e SonarQube: gerar relatório de cobertura e manter análise estática ativa (ideal: CI de testes + SonarQube).

**Frontend (sigaex-frontend):**
- Integrar a API (ex.: axios) e implementar páginas funcionais **Gestão de Eventos** (listar/criar/editar/excluir) e **Detalhes do Evento**, consumindo os endpoints do backend.
- Limpar placeholders/páginas estáticas antigas (htmls soltos na raiz) e uso de store Pinia para o estado de eventos.
- **Testes unitários de componentes** com Vitest + Vue Test Utils (+ mock de API), com cobertura reportada.

### 2.4 Testes de Aceitação e Relatório — `backend/docs/relatorio-testes.md`
- Executar os cenários **BDD/Gherkin** definidos na P1 (US-01 a US-04).
- Emitir relatório de testes em Markdown com os resultados.
- Cadastrar **issues de bugs** para cada falha encontrada.

### 2.5 Atualizações de Backlog
- Marcar no `doc-userstories.md` as USs concluídas na iteração e atualizar o plano de release/iteração.

## 3. Fluxo Git/GitHub

- Issue por US/tarefa; branch `feature/#<id>-<nome>`; commits Conventional Commits com `#<id>`; PR com descrição e `Closes #<id>`.

## 4. Critérios (10,0 pontos)

Conforme `P2-criterios.md`.