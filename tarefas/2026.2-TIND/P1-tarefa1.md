# P1 — Iniciação e Planejamento do Projeto (Individual · YP-Agentic)

**Disciplina:** Engenharia de Software II — DCT2302
**Turma:** 2026.2-TIND (Ensino Individualizado)
**Processo:** [YP-Agentic](../../yp-agentic/manual-passo-a-passo.md)
**Iteração:** 1 · Fases 1–3 (Conversa com o Cliente, Inicialização e Planejamento de Releases)
**Prazo:** **29/09/2026**
**Discente:** Artur Morais Candeia

## 1. Contexto

Você dá continuidade ao projeto **SIGAEX** em regime individual, acumulando os papéis de **Analista, Líder Técnico, Desenvolvedor e Testador**, com apoio de agentes de IA conforme o processo **YP-Agentic**.

- **Backend:** https://github.com/labens-ufrn/sigaex-backend
- **Frontend:** https://github.com/labens-ufrn/sigaex-frontend

Antes de começar, **leia obrigatoriamente** o `yp-agentic/manual-passo-a-passo.md`, depois `processo/glossario.md` e `processo/artefatos.md`. O **Anexo A** informa o estado atual do SIGAEX — use-o como ponto de partida (não recrie do zero: **revise e atualize** documentos existentes).

## 2. Entregáveis (todos em Markdown na pasta `docs/` dos repositórios do projeto)

Na fase 1 (também chamada de "Conversa com o Cliente"), na Fase 2 (Inicialização) e na Fase 3 (Planejamento de Releases), você deve produzir os seguintes artefatos:

### 2.1 Documento de Visão — `backend/docs/documento-de-visao.md`
Revisar/atualizar conforme `templates/doc-visao.md`:
- Problema e Oportunidade; Solução Proposta.
- Stakeholders e Perfis de Usuários.
- Requisitos Funcionais de alto nível **priorizados (P0/P1/P2)** e Requisitos Não Funcionais.
- Restrições, Riscos e Critérios de Sucesso.

### 2.2 PRD — `backend/docs/prd.md`
Criar conforme `templates/prd.md` (documento central de produto, **substitui as listas avulsas de RFs**):
- Personas; Problema/Solução; Cenário atual.
- Funcionalidades priorizadas (P0/P1/P2) com justificativas.
- Critérios de Sucesso (KPIs); In/Out Scope; Roadmap de Release.

### 2.3 Lista de User Stories — `backend/docs/doc-userstories.md`
Criar o **backlog consolidado e priorizado**, agrupado por **épicos funcionais** (Cadastro de Eventos, Usuários/Perfil, Inscrições, Check-in/Presença, Certificados, Relatórios/Dashboard, Divulgação). Reaproveite as USs já documentadas (ex.: `docs/cadastroEvento.md` US-01..04, `docs/US-inscricoes.md`, `docs/palestrasMinistrantes.md`, `docs/preseCheck.md`). Para cada US informe: ID, épico, story (Como…/quero…/para…), prioridade, release/iteração prevista.

### 2.4 Especificação de User Stories — `backend/docs/esp-userstories.md`
Detalhar **pelo menos as USs da Release 1 (US-01 a US-04 — Gestão de Eventos)** conforme `templates/esp-userstories.md`:
- Contexto de negócio; Requisitos internos; Regras de Negócio.
- Fluxos principal/alternativo/erro; Diagramas Mermaid (classes e sequência).
- **Critérios de aceitação em BDD/Gherkin** (Dado/Quando/Então) para cada cenário.
- Protótipo de tela (link Figma ou descrição).

### 2.5 Documento de Modelos — `backend/docs/doc-modelos.md`
Criar conforme `templates/doc-modelos.md`:
- **Modelo conceitual** (diagrama de classes de domínio em Mermaid).
- **DER** (diagrama entidade-relacionamento em Mermaid), coerente com os models Django atuais (`Usuario`, `TipoEvento`, `TipoCheckin`, `Evento`, `Inscricao`, `Checkin`) e apontando lacunas.
- **Dicionário de dados** (atributos, tipos, restrições).

### 2.6 Termo de Abertura do Projeto — `backend/docs/termo-abertura.md`
Conforme `templates/termo-abertura.md`: objetivo, escopo, papéis (você acumula todos, com agentes de IA de suporte), riscos iniciais e critérios de saída.

### 2.7 Documento de Agentes — `backend/docs/doc-agentes.md`
Conforme `templates/doc-agentes.md`: defina os **agentes de IA especializados** que você usará (Requisitos/Produto, Modelagem/Arquitetura, Programação em Par, Testes/Qualidade, Revisão de Processo), com ferramentas, personas e instruções.

### 2.8 Planos de Testes e de Release/Iteração — `backend/docs/plano-geral-testes.md` e `backend/docs/plano-iteracao.md`
- Plano geral de testes (níveis: unidade, integração, aceitação; ferramentas: pytest/REST Framework test, Vitest; critérios de cobertura por iteração).
- Plano de release/iteração: Release 1 = **Gestão de Eventos**; fatie a iteração 1 em USs com BDD.

## 3. Fluxo Git/GitHub

- Crie **uma issue por artefato** (documento) nos repositórios do projeto.
- Trabalhe em branches nomeadas com o ID da issue (ex.: `feature/#12-documento-de-visao`).
- Faça **commits pequenos** com Conventional Commits referenciando a issue (ex.: `docs: adiciona PRD do SIGAEX #14`).
- Abra **Pull Request** com descrição adequada e `Closes #<id>`.

## 4. Critérios (10,0 pontos)

Conforme `P1-criterios.md`.

---

## Anexo A — Estado Atual do SIGAEX (baseline para o P1)

### Backend (sigaex-backend — Django 5.0.7 + DRF)
- **Models implementados:** `Usuario` (login por e-mail; validações CPF/CEP/UF/telefone), `TipoEvento`, `TipoCheckin`, `Evento` (hierarquia `evento_pai`, modalidade, organizador), `Inscricao` (única por participante/evento), `Checkin` (único por evento; GPS/código/QR) + serviço de CEP (IBGE/ViaCEP).
- **API exposta:** somente **CRUD de Eventos** (`EventoViewSet`, `AllowAny`). Auth JWT (login/refresh/verify/blacklist) e Swagger/ReDoc configurados.
- **Não expostos via API:** Usuario, TipoEvento, TipoCheckin, Inscricao, Checkin (só models).
- **Testes:** ~110 testes de modelo/unidade (`django.test.TestCase`); **sem testes de API/endpoint**; sem `pytest`/`coverage` no `requirements.txt`; sem relatório de cobertura.
- **CI:** apenas `.github/workflows/sonarqube.yml` (roda `coverage` e SonarQube com secrets).
- **Docs:** `docs/documento-de-visao.md` (estilo antigo, sem PRD), US parciais (`cadastroEvento.md` US-01..04, `US-inscricoes.md`, `palestrasMinistrantes.md`, `preseCheck.md`, `infoGraficoGestao.md`, `gerarChachasAut.md`, etc.); `README.md`, `GUIA_DESENVOLVIMENTO_EVENTOS.md` e `RESUMO_CRUD_EVENTOS.md` **desatualizados** (referem a antiga app `eventos`).

### Frontend (sigaex-frontend — Vue 3 + Vite + TypeScript + Vuetify + Pinia + Vitest)
- Estrutura **quase scaffold**: rotas/páginas placeholder (Início, Home, Gestão de Eventos, Detalhes, Dashboard, Perfil, Desenvolvedores, Selecionar Atividades), componente `StatCard`, store `counter.ts`, HTMLs estáticos antigos na raiz.
- **Sem integração com a API** (sem axios consumer).
- **Testes:** apenas `src/__tests__/example.test.ts` (placeholder); Vitest + coverage configurados.

### Testes de Sistema/Aceitação
- **Inexistentes** em backend e frontend.

### Conclusões para o P1
1. Os documentos de visão e US existentes devem ser **revisados/atualizados** para os templates YP-Agentic (não descartados).
2. É necessário criar o **PRD**, a **lista consolidada de US**, a **especificação BDD**, os **modelos**, o **TAP**, o **doc-agentes** e os **planos**.
3. A modelagem deve refletir os models Django atuais e sinalizar lacunas (ex.: entidades de Palestrante/Ministrante, Certificado e Presença ainda não modeladas).