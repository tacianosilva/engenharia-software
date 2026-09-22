# Fluxo de Desenvolvimento — YP-Agentic

## 1. Visão Geral do Fluxo (8 Fases)
O fluxo do **YP-Agentic** é organizado em 8 fases iterativas e incrementais, adaptadas para a dinâmica de disciplinas de Engenharia de Software (60h, um semestre) com suporte intensivo de agentes de IA:

1. **Fase 1 — Conversa com o Cliente:** Elicitação e definição estratégica inicial.
   - *Artefatos:* Documento de Visão, PRD (Product Requirements Document), Lista de User Stories, Modelo Conceitual e de Dados, Projeto Arquitetural.
2. **Fase 2 — Inicialização:** Formalização do projeto e governança dos agentes.
   - *Artefatos:* Termo de Abertura do Projeto (TAP), Documento de Agentes de IA.
3. **Fase 3 — Planejamento de Releases:** Organização macro dos incrementos e estratégias de validação.
   - *Artefatos:* Plano Geral de Testes, Especificação de User Stories, Plano de Release.
4. **Fase 4 — Planejamento de Iteração:** Fatiamento do ciclo de 2 semanas (*timebox*).
   - *Artefatos:* Testes de Aceitação, Plano de Iteração.
5. **Fase 5 — Implementação:** Codificação assistida por agentes, refatoração contínua e integração.
   - *Artefatos:* Atas de Reunião, Versão Incremental do Produto.
6. **Fase 6 — Implantação (Deploy):** Disponibilização e execução de testes automatizados em ambiente de homologação/produção.
   - *Artefatos:* Relatórios de Testes, Deploy funcional.
7. **Fase 7 — Fim da Iteração:** Verificação dos critérios de aceitação e ativação dos loops de feedback.
   - *Atividades:* Homologação com stakeholders e avaliação do incremento;
   - *Loop de Próxima Iteração:* Retorna à **Fase 4 (Planejamento de Iteração)**;
   - *Loop de Próxima Release:* Retorna à **Fase 3 (Planejamento de Releases)**;
   - *Saída:* Produto Final / Incremento validado.
8. **Fase 8 — Finalização:** Encerramento formal do projeto.
   - *Artefatos:* Termo de Encerramento do Projeto (TEP), Entrega Final.

---

## 2. Caráter Iterativo Incremental
O **YP-Agentic** é um processo explicitamente **iterativo e incremental**:
- O desenvolvimento avança em ciclos curtos e regulares (com iterações típicas de **duas semanas**), onde cada iteração entrega um **incremento executável e funcional do produto**.
- **Tempo é fixo (*timeboxed*); escopo é variável**: os prazos das iterações e releases não são estendidos; ajusta-se o escopo planejado com base na velocidade real da equipe e na produtividade assistida pelos agentes de IA.
- A essência do processo reside nos seus loops de retorno contínuos:
  - **Loop de Próxima Iteração (Fase 7 → Fase 4):** ao concluir uma iteração e avaliar a entrega com os testes de aceitação, a equipe retorna ao *Planejamento de Iteração* para selecionar e especificar o próximo conjunto de Histórias de Usuário.
  - **Loop de Próxima Release (Fase 7 → Fase 3):** ao atingir o conjunto de incrementos previsto para uma release, a equipe retorna ao *Planejamento de Releases* para replanejar entregas futuras ou ajustar prioridades no PRD.

---

## 3. Fundamentação Ágil

O YP-Agentic combina práticas consagradas das duas principais abordagens ágeis da engenharia de software moderna:

- **XP (Extreme Programming):** Metodologia ágil criada por Kent Beck na década de 1990, focada em entregar software com alta qualidade técnica e responder de forma flexível e rápida a mudanças nos requisitos. Do XP, o YP-Agentic herda:
  - Uso de **User Stories** como unidade fundamental de requisito;
  - **Testes contínuos** (testes de unidade e de aceitação automatizados em BDD);
  - **Refatoração constante** e código coletivo mantido com auxílio de agentes de IA;
  - **Cliente e avaliador próximos do time**, com feedback contínuo.
- **Scrum:** Estrutura de gestão ágil usada para organizar e gerenciar o desenvolvimento de produtos complexos por meio de ciclos curtos e colaborativos (sprints/iterações). Do Scrum, o YP-Agentic herda:
  - **Ciclos de iteração com tempo fixo** (*timeboxing* de 2 semanas);
  - **Reuniões de planejamento e acompanhamento**;
  - **Revisão e demonstração de entregas funcionais** a cada ciclo;
  - **Papéis bem definidos** entre liderança, equipe técnica e agentes de IA especializados.

---

## 4. Rastreabilidade dos Artefatos pelas Fases

| Fase | Entradas | Atividades Principais | Artefatos de Saída |
|---|---|---|---|
| **1. Conversa com o Cliente** | Necessidades do cliente, brainstorm | Elicitação, definição de personas, escopo e prioridades | `doc-visao.md`, `prd.md`, `doc-userstories.md`, `doc-modelos.md`, `doc-arquitetura.md` |
| **2. Inicialização** | Visão aprovada, escopo base | Formalização acadêmica e configuração dos agentes | `termo-abertura.md`, `doc-agentes.md` |
| **3. Planejamento de Releases** | PRD, Backlog de US | Estruturação de releases, testes e detalhamento de US complexas | `Plano de Release`, `Plano Geral de Testes`, `esp-userstories.md` |
| **4. Planejamento de Iteração** | Backlog de US da Release | Seleção do timebox de 2 semanas e critérios BDD | `Plano de Iteração`, `Testes de Aceitação` |
| **5. Implementação** | US especificadas, critérios de aceite | Programação assistida por IA, TDD, refatoração | `Atas de Reunião`, `Código/Versão Incremental` |
| **6. Implantação** | Build aprovado | Deploy e execução de bateria de testes automatizados | `Relatórios de Testes`, `Ambiente Deployado` |
| **7. Fim da Iteração** | Relatório de testes, incremento | Homologação com cliente e decisão do próximo loop | `Incremento Validado` → *Loop Fase 4 ou Fase 3* |
| **8. Finalização** | Release final homologada | Consolidação de lições aprendidas e encerramento | `termo-encerramento.md`, `Entrega Final` |
