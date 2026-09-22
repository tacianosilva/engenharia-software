# Artefatos do Processo — YP-Agentic

## 1. Visão Geral dos Artefatos
Os artefatos no YP-Agentic são documentos vivos, versionados no repositório, que mantêm a rastreabilidade desde a concepção da ideia até o código final entregue.

> **Consulte o Glossário:** Para a definição formal de cada artefato, seus relacionamentos (o que combina, substitui e alimenta) e quando são gerados, consulte [`processo/glossario.md`](glossario.md).

---

## 2. Catálogo de Artefatos pelas 8 Fases

### 2.1 Fase 1 — Conversa com o Cliente
- **Documento de Visão (`doc-visao.md`):** Define o "porquê" e "para quem", problemas, oportunidades, stakeholders e limites estratégicos.
- **Product Requirements Document (`prd.md`):** Artefato central de decisão que substitui a lista de RFs, definindo personas, features priorizadas (P0/P1/P2), KPIs e escopo.
- **Lista de User Stories (`doc-userstories.md`):** Backlog de histórias de usuário organizadas por entidade de domínio (CRUD) e priorizadas.
- **Documento de Modelos (`doc-modelos.md`):** Modelo Conceitual (UML), Modelo de Dados (ER) e Dicionário de Dados.
- **Projeto Arquitetural (`doc-arquitetura.md`):** Visão de alto nível (HLD), componentes, tecnologias, mecanismos e ADRs.

### 2.2 Fase 2 — Inicialização
- **Termo de Abertura do Projeto - TAP (`termo-abertura.md`):** Autorização formal, objetivos, equipe e cronograma macro (60h).
- **Documento de Agentes de IA (`doc-agentes.md`):** Governança dos agentes de IA, ferramentas, limites, fluxo e critérios de revisão.

### 2.3 Fase 3 — Planejamento de Releases
- **Plano de Release (`plano-release.md`):** Distribuição das US pelas iterações da release e critérios de aceitação.
- **Plano Geral de Testes (`plano-geral-testes.md`):** Estratégia de testes por RNF, níveis (unidade, integração, aceitação) e ferramentas.
- **Especificação de User Stories (`esp-userstories.md`):** Detalhamento opcional para US com regras complexas, com fluxos, diagramas Mermaid, telas e BDD.

### 2.4 Fase 4 — Planejamento de Iteração
- **Plano de Iteração (`plano-iteracao.md`):** Fatiamento do timebox de 2 semanas, tarefas por US, responsáveis e cronograma.
- **Plano de Teste da Iteração (`plano-teste-iteracao.md`):** Matriz de casos de teste de aceitação (CT) e critérios de entrada/saída.

### 2.5 Fase 5 — Implementação
- **Atas de Reunião:** Registros semanais de alinhamento e acompanhamento.
- **Versão Incremental do Produto:** Código-fonte implementado, refatorado e testado.

### 2.6 Fase 6 — Implantação
- **Relatório de Testes (`relatorio-testes.md`):** Resultados consolidados da execução dos testes, evidências e bugs.
- **Deploy Funcional:** Aplicação disponibilizada em ambiente de homologação/produção.

### 2.7 Fase 7 — Fim da Iteração
- **Incremento Validado:** Avaliação formal dos testes de aceitação e ativação dos loops (*Próxima Iteração → Fase 4; Próxima Release → Fase 3*).

### 2.8 Fase 8 — Finalização
- **Termo de Encerramento do Projeto - TEP (`termo-encerramento.md`):** Formalização da conclusão, resultados alcançados, lições aprendidas e homologação.
- **Entrega Final:** Pacote final do produto e documentação consolidada.

---

## 3. Critérios de Qualidade e Rastreabilidade
- **Regra da Posse da Informação:** Não duplicar informações entre documentos; cada informação tem sua fonte de verdade e os demais artefatos referenciam via links.
- **Rastreabilidade Bidirecional:** Visão ──► PRD ──► Lista de US ──► Especificação BDD ──► Código & Testes.
- **Validação Humana:** Decisões de negócio, produto, arquitetura e aceite final permanecem exclusivamente sob responsabilidade humana.
