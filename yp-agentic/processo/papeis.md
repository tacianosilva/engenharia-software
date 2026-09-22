# Papéis e Responsabilidades — YP-Agentic

## 1. Visão Geral dos Papéis
No modelo **YP-Agentic**, as equipes de disciplinas acadêmicas de Engenharia de Software (60h, um semestre) combinam responsabilidades desempenhadas por perfis docentes, discentes e agentes de IA especializados.

---

## 2. Perfis Docentes
- **Professor da Disciplina:** Define as diretrizes pedagógicas, marcos avaliativos, prazos das releases e critérios de avaliação do processo.
- **Professor Cliente / Cliente Externo:** Atua como o stakeholder de negócio, fornecendo a visão inicial, validando o Documento de Visão, o PRD e homologando os incrementos ao fim de cada release.
- **Orientador / Monitor:** Auxilia no acompanhamento técnico da equipe, revisão de código e governança do processo.

---

## 3. Perfis Discentes (Equipe de Desenvolvimento)
- **Analista de Requisitos:** Responsável por conduzir a elicitação de requisitos (prompts de Visão, PRD e User Stories), intermediar com o cliente e validar os critérios de aceite (BDD).
- **Líder Técnico / Arquiteto:** Responsável pelas decisões arquiteturais (ADRs), modelo conceitual e de dados, definição da stack tecnológica e configuração/governança dos agentes de IA.
- **Desenvolvedor:** Responsável pela implementação das histórias de usuário, codificação assistida por IA, refatoração contínua e escrita de testes unitários.
- **Testador (QA Engineer):** Responsável pelo planejamento e execução dos testes de aceitação automatizados, verificação de critérios Gherkin e emissão dos relatórios de testes.

---

## 4. Papéis de Agentes de IA Especializados
- **Agente de Requisitos e Produto:** Auxilia na elicitação e redação estruturada da Visão, PRD e fatiamento das User Stories.
- **Agente de Modelagem e Arquitetura:** Auxilia na geração de diagramas conceituais, lógicos (DER) e arquiteturais em sintaxe Mermaid.
- **Agente de Programação em Par (Coding Assistant):** Auxilia na implementação das classes, componentes e funções a partir das especificações de US.
- **Agente de Testes e Qualidade:** Auxilia na escrita de cenários Gherkin, geração de testes de unidade e automação de testes de aceitação.
- **Agente de Revisão e Auditoria de Processo:** Verifica a conformidade dos artefatos com os templates oficiais e critérios do processo YP-Agentic.

---

## 5. Matriz de Responsabilidades (RACI)

| Atividade / Artefato | Analista | Líder Técnico | Desenvolvedor | Testador | Agentes de IA | Docente / Cliente |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **Documento de Visão** | **R** | C | I | I | S | **A** |
| **PRD (Decisão de Produto)** | **R** | C | I | C | S | **A** |
| **Lista de User Stories** | **R** | C | C | C | S | I |
| **Especificação de US (BDD)** | **R** | C | **R** | C | S | I |
| **Modelos (Conceitual / DER)** | C | **R** | C | I | S | I |
| **Projeto Arquitetural** | I | **R** | C | I | S | I |
| **Documento de Agentes** | I | **R** | C | C | S | I |
| **Implementação e Testes Unitários** | I | C | **R** | C | S | I |
| **Testes de Aceitação / Deploy** | I | C | C | **R** | S | I |
| **Homologação e Termo de Encerramento** | C | **R** | C | C | S | **A** |

*Legenda:* **R** = Responsável (quem faz); **A** = Aprovador (quem valida); **C** = Consultado; **I** = Informado; **S** = Suporte (Agente de IA).
