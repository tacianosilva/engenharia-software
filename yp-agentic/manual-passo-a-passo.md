# Manual Passo a Passo — YP-Agentic na DCT2302 · 2026.2-TIND

> **Turma:** DCT2302 — 2026.2-TIND (Ensino Individualizado)
> **Discente:** Artur Morais Candeia (GitHub: `ArturCandeia`)
> **Projeto:** SIGAEX — `https://github.com/labens-ufrn/sigaex-backend` e `https://github.com/labens-ufrn/sigaex-frontend`
> **Processo:** YP-Agentic (veja `processo/` e `assets/fluxo-yp-agentic.png`)
> **Objetivo:** orientar a aplicação do processo YP-Agentic de forma **individual**, acumulando os papéis de Analista, Líder Técnico, Desenvolvedor e Testador, com apoio intensivo de agentes de IA.

---

## 1. Visão Geral do Processo

O YP-Agentic organiza o desenvolvimento em **8 fases** com **iterações de 2 semanas** (tempo fixo, escopo variável). Cada iteração entrega um **incremento executável e testado**.

| Fase | O que faz | Artefatos |
|:---:|:---|:---|
| 1 | Conversa com o Cliente | `doc-visao.md`, `prd.md`, `doc-userstories.md`, `doc-modelos.md`, `doc-arquitetura.md` |
| 2 | Inicialização | `termo-abertura.md`, `doc-agentes.md` |
| 3 | Planejamento de Releases | `plano-geral-testes.md`, `esp-userstories.md`, Plano de Release |
| 4 | Planejamento de Iteração | `plano-iteracao.md`, Testes de Aceitação (BDD) |
| 5 | Implementação | Atas de Reunião, Incremento (código + testes) |
| 6 | Implantação (Deploy) | `relatorio-testes.md`, deploy funcional |
| 7 | Fim da Iteração | Incremento validado → loop p/ Fase 4 ou 3 |
| 8 | Finalização | `termo-encerramento.md`, entrega final |

> **Leitura obrigatória ANTES de começar:** `processo/glossario.md` e `processo/artefatos.md`.

---

## 2. Ambiente e Ferramentas

- **Ferramentas Git:** `git` + `gh` CLI. Nada de AcademicDevFlow nesta turma.
- **Ferramentas de IA:** agente de codificação/CLI (ex.: opencode, Claude Code) conforme `doc-agentes.md`.
- **Backend:** Python 3.12 + Django 5 + DRF (venv no repos SIGAEX).
- **Frontend:** Node + Vue 3 + Vite + Vuetify + Vitest.
- **Qualidade:** SonarQube (backend e frontend) mínimo **2x/semana**; cobertura conforme critério da iteração (25% P3, 65% P4, 80% P5).

---

## 3. Fluxo Git/GitHub (vale para todos os repos SIGAEX)

1. **Issue por unidade de trabalho** — uma issue por artefato (P1) ou por US/bug (P2+), com título claro e descrição.
2. **Branch** a partir de `main` (ou `develop`): `feature/#<id_issue>-<nome>`, ex.: `feature/#12-gestao-de-eventos`.
3. **Commits pequenos** seguindo Conventional Commits, sempre referenciando a issue:
   - `feat: implementa listagem de eventos #12`
   - `docs: adiciona PRD #05`
   - `test: adiciona testes de aceitação da US-02 #14`
4. **Pull Request** com descrição (resumo + evidências) e `Closes #<id>`.
5. **Revisão pelo professor** → merge para `main`.

---

## 4. Como Usar Prompts e Templates

1. **Copie os templates** de `yp-agentic/templates/` para a pasta `docs/` do repositório do projeto (backend: `sigaex-backend/docs/`; algo de frontend: `sigaex-frontend/docs/`).
2. **Use o prompt correspondente** de `yp-agentic/prompts/` como entrada do seu agente de IA para preencher cada artefato:
   - Ordem: `doc-visao.md` → `prd.md` → `doc-userstories.md` → `esp-userstories.md` → `doc-modelos.md` → `doc-arquitetura.md` → `doc-agentes.md`.
3. **Nunca invente dados**: marque como `[A definir]` o que depender de decisão sua/cliente.
4. **Idioma:** todo artefato em **português do Brasil**.
5. **Diagramas:** use sintaxe **Mermaid** (classes, sequência, DER, C4).

---

## 5. Passo a Passo por Tarefa da Disciplina

### T1 — Git, GitFlow, GitHub e Markdown (prazo: 01/09)
- Issue de tarefa no repo da disciplina; branch `tarefa01`; commits por item.
- Conteúdo do `tarefa01.md` conforme enunciado (inclui Tags, comandos de inspeção, SemVer, automação de versões).

### P1 — Iniciação e Planejamento (Fases 1–3 · prazo: 29/09)
1. **Visão + PRD:** rode `prompts/doc-visao.md` e `prompts/prd.md` com o material existente do SIGAEX (`docs/documento-de-visao.md` e os `docs/*.md` das USs) — revise e atualize; o PRD **substitui a lista avulsa de RFs**.
2. **Backlog de User Stories:** rode `prompts/doc-userstories.md`; agrupe por épicos (Cadastro de Eventos, Usuários/Perfil, Inscrições, Check-in/Presença, Certificados, Relatórios, Divulgação); priorize P0/P1/P2.
3. **Especificações (esp-userstories):** rode `prompts/esp-userstories.md` para as USs da Release 1 (mínimo US-01 a US-04) com critérios **BDD/Gherkin**.
4. **Modelos:** rode `prompts/doc-modelos.md` → conceitual (classes de domínio) + DER + dicionário de dados, coerentes com os models Django atuais.
5. **TAP + Agentes:** `termo-abertura.md` e `doc-agentes.md` (quais agentes de IA serão usados, em quais fases).
6. **Planos:** `plano-geral-testes.md` e plano de release/iteração (Release 1 = Gestão de Eventos).
7. **Git:** uma issue por artefato; commits `docs:` por documento; PR(s) para revisão.

### P2 — Detalhamento, Arquitetura e primeira implementação (Fases 4–6 · prazo: 06/10)
1. **Arquitetura + ADRs:** `prompts/doc-arquitetura.md` → camadas (Vue3/Vite ↔ DRF ↔ BD), tabela de tecnologias, decisões arquiteturais.
2. **Plano de Iteração** com as USs da fatia **Gestão de Eventos** e cenários BDD.
3. **Implementação da fatia vertical "Gestão de Eventos"** (da tela ao banco):
   - Backend: finalizar CRUD de Eventos (permissões JWT, endpoints), testes `APITestCase`, cobertura, SonarQube.
   - Frontend: páginas `GestaoEventos`/`DetalhesEvento` consumindo a API (axios), testes Vitest + Vue Test Utils.
4. **Testes de aceitação:** executar os cenários BDD; registrar `docs/relatorio-testes.md` e **issues de bugs**.
5. **Fora de escopo no P2:** Usuário, Inscrição e Check-in (ficam para P3/P4).

### P3 — Implementação e Testes de Unidade (Iteração 2 · prazo: 27/10)
- 3 USs novas/continuadas da tela ao banco; testes de unidade/integração; APF; SonarQube ≥ 25%.

### P4 — Evolução e Testes de Aceitação (Iteração 3 · prazo: 17/11)
- 2 USs novas; testes de aceitação com relatório; cobertura ≥ 65%.

### P5 — IC e Implantação (Iteração 4 · prazo: 08/12)
- Docker, CI/CD, deploy local; 2 USs novas; cobertura ≥ 80%; vídeo de defesa.

---

## 6. Check-Lists por Entrega

### Check-list P1 (29/09)
- [ ] `docs/doc-visao.md` revisado (problema, oportunidade, stakeholders, perfis, RFs P0/P1/P2, RNFs, riscos, critérios de sucesso)
- [ ] `docs/prd.md` (personas, funcionalidades priorizadas, KPIs, in/out scope, roadmap)
- [ ] `docs/doc-userstories.md` (backlog agrupado por épicos, priorizado)
- [ ] `docs/esp-userstories.md` (US-01..04 com BDD/Gherkin)
- [ ] `docs/doc-modelos.md` (conceitual + DER + dicionário de dados)
- [ ] `docs/termo-abertura.md` e `docs/doc-agentes.md`
- [ ] `docs/plano-geral-testes.md` e plano de release/iteração
- [ ] Issues por artefato; commits `docs:`; PR(s)

### Check-list P2 (06/10)
- [ ] `docs/doc-arquitetura.md` + ADRs
- [ ] Plano de iteração com fatia Gestão de Eventos
- [ ] Backend: CRUD Eventos com permissões + testes `APITestCase`
- [ ] Frontend: `GestaoEventos` + `DetalhesEvento` integradas (axios) + testes
- [ ] Cobertura reportada (SonarQube / coverage)
- [ ] `docs/relatorio-testes.md` (aceitação) + issues de bugs
- [ ] PRs com `Closes #id` e Conventional Commits

---

## 7. Dicas de Uso dos Agentes de IA

- Comece **sempre** lendo o `processo/glossario.md` e o prompt da fase.
- Dê ao seu agente **material já existente** (docs atuais do SIGAEX) para ele **revisar/atualizar**, não recriar do zero.
- Exija **Mermaid** nos diagramas e **Gherkin** nos critérios de aceite.
- Peça ao agente para marcar `[A definir]` em vez de inventar requisitos, atores ou métricas.
- Ao final de cada fase, rode uma **revisão de conformidade** contra o template antes de abrir o PR.

---

## 8. Referências

- Repositório do processo: `https://github.com/EngSoft-BSI-Hub/yp-agentic` (fonte original).
- Processo local nesta disciplina: pasta [`yp-agentic/`](../yp-agentic/).
- Enunciados: [`tarefas/2026.2-TIND/`](../tarefas/2026.2-TIND/).