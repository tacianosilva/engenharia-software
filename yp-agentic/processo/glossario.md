# Glossário de Termos e Documentos — YP-Agentic

Este documento define os principais termos conceituais e os artefatos (documentos) que compõem o processo **YP-Agentic**, explicitando seu propósito, origem, responsáveis e relacionamento com os demais artefatos.

---

## 1. Glossário de Termos

- **Agente de IA:** Entidade de software autônoma ou semi-autônoma baseada em Modelos de Linguagem (LLMs) capaz de executar tarefas de engenharia de software (como elaboração de requisitos, modelagem, geração de código, testes e revisões) sob orientação humana e por meio de ferramentas estruturadas.
- **Iteração:** Ciclo curto de desenvolvimento com tempo fixo (*timebox*, tipicamente 2 semanas), no qual uma fatia planejada de funcionalidades é implementada, testada e integrada.
- **Release:** Marco que agrupa um conjunto de iterações e incrementos funcionais entregáveis a clientes ou usuários finais.
- **Incremento:** Resultado funcional, executável e testado produzido ao final de uma iteração ou release, que se soma ao que já foi desenvolvido anteriormente.
- **Épico (Epic):** Grande necessidade, capacidade de negócio ou macrofuncionalidade que é ampla demais para ser implementada em uma única iteração (ciclo de 2 semanas). Serve como agrupador temático de alto nível e deve ser fatiado/decomposto em múltiplas **User Stories** menores, independentes e estimáveis.
  - *Origem:* Conceito originado e difundido nas metodologias ágeis (ecossistema XP e Scrum, formalizado por Mike Cohn em 2004 e adotado pelo SAFe). No XP, referia-se a "histórias grandes demais para caber em uma iteração".
  - *Equivalências em outros métodos:* **Feature / Macrofuncionalidade** (no FDD e na gestão de produtos moderna), **Tema (Theme) / Capability** (no Scrum/SAFe), **Pacote de Casos de Uso / Caso de Uso de Alto Nível** (no RUP/UML) e **Macro-requisito / Módulo Funcional** (na Engenharia de Requisitos tradicional em cascata).
- **User Story (História de Usuário):** Descrição sucinta de uma necessidade ou funcionalidade do ponto de vista do usuário final, escrita no formato: *"Como um [ator], quero [ação], para que [benefício]"*.
- **Critério de Aceitação:** Conjunto de condições e regras verificáveis que uma User Story deve satisfazer para ser considerada concluída e aceita pelos stakeholders.
- **Teste de Aceitação:** Teste formal (manual ou automatizado, frequentemente estruturado em BDD/Gherkin) que valida se os critérios de aceitação foram cumpridos.
- **PRD (Product Requirements Document):** Documento central de definição e decisão do produto, detalhando visão funcional, personas, requisitos priorizados, critérios de sucesso e escopo (in/out scope).
  - *Origem e Relação Tradicional:* O PRD moderniza a tradicional **Especificação de Requisitos de Software (SRS / ERS - Software Requirements Specification, padrão IEEE 830)** e a antiga Especificação Funcional em cascata. Enquanto a SRS tradicional era exaustiva e rígida, o PRD ágil organiza decisões de produto com foco em valor de negócio, métricas mensuráveis (KPIs), priorização clara (P0/P1/P2) e delimitação de escopo (*in/out scope*).
- **Persona:** Representação arquetípica e semi-fictícia do usuário ideal do sistema, descrevendo características, dores, necessidades e comportamentos.
- **Requisito Funcional (RF):** Declaração do comportamento, serviço ou funcionalidade que o sistema deve fornecer aos usuários.
- **Requisito Não-Funcional (RNF):** Declaração de restrições, padrões de qualidade ou atributos arquiteturais que o sistema deve cumprir (ex.: desempenho, segurança, disponibilidade, usabilidade).
- **Modelo Conceitual (Modelo de Domínio):** Representação de alto nível das entidades do negócio, seus atributos fundamentais e as relações entre elas, focada no vocabulário e regras do problema no mundo real, independente de tecnologia ou banco de dados específico (frequentemente expresso por Diagramas de Classes de Domínio UML).
- **Modelo de Dados:** Representação estruturada e lógica dos dados que serão persistidos pelo sistema (frequentemente expressa por Diagramas Entidade-Relacionamento - DER), especificando chaves primárias, chaves estrangeiras, tipos e restrições de integridade.
- **Dicionário de Dados:** Catálogo detalhado que descreve o significado, formato, tipo de dado, restrições, valores permitidos e finalidade de cada entidade, tabela, atributo ou coluna presente no sistema.
- **Extreme Programming (XP):** Metodologia ágil criada por Kent Beck na década de 1990, focada em entregar software com alta qualidade técnica e responder de forma flexível e ágil a mudanças nos requisitos.
- **Scrum:** Estrutura de gestão ágil usada para organizar e gerenciar o desenvolvimento de produtos complexos por meio de ciclos curtos e colaborativos (sprints/iterações).
- **Timeboxing (Tempo Fixo):** Prática de fixar a duração de um ciclo (iteração), variando o escopo entregue para garantir previsibilidade e cadência.
- **Design System (DESIGN.md):** conjunto de padrões de identidade visual (cores, tipografia, componentes, padrões de tela) que padroniza as interfaces do produto. Gerado no Planejamento de Releases (Fase 3) e referenciado pela Especificação de User Stories (§7) e pelo Projeto Arquitetural.

---

## 2. Glossário de Documentos (Artefatos)

Abaixo é descrito o papel de cada artefato no processo, seus produtores e como ele combina, substitui ou alimenta outros documentos:

### 2.1 Product Requirements Document (PRD) — `templates/prd.md`
- **Propósito:** Documento central de decisão de produto. **Moderniza a tradicional Especificação de Requisitos de Software (SRS / IEEE 830) e substitui a tradicional lista avulsa de requisitos funcionais (RFs)** do easYProcess original, organizando funcionalidades priorizadas (P0, P1, P2), personas, objetivos de negócio, métricas de sucesso e limites de escopo (*in/out scope*).
- **Quando é gerado:** Fase de Concepção / Início da Elaboração.
- **Quem produz:** Product Owner / Engenheiro de Requisitos com suporte do Agente de Requisitos.
- **Relacionamento:** É contextualizado pelo Documento de Visão e **alimenta diretamente** a *Lista de Histórias de Usuário* e a *Especificação de User Stories*.

### 2.2 Documento de Visão — `templates/doc-visao.md`
- **Propósito:** Documento mestre de contextualização estratégica e escopo do projeto, descrevendo oportunidade, problema e partes interessadas.
- **Flexibilidade:** Por padrão, o Documento de Modelos é mantido separado. Contudo, o Líder Técnico do projeto possui flexibilidade para unificar o modelo conceitual e requisitos gerais dentro do Documento de Visão se julgar mais adequado ao porte do projeto.
- **Quando é gerado:** Fase de Concepção.
- **Quem produz:** Gerente de Projeto / Líder Técnico em conjunto com os stakeholders.
- **Relacionamento:** Precede o PRD e orienta o Termo de Abertura.

### 2.3 Lista de User Stories (Backlog) — `templates/doc-userstories.md`
- **Propósito:** Lista consolidada de todas as User Stories priorizadas (ex.: MoSCoW), agrupadas por **Épicos funcionais** ou entidades de domínio (CRUDs e regras operacionais).
- **Quando é gerado:** Fase de Elaboração e refinado a cada planejamento de release/iteração.
- **Quem produz:** Equipe de Desenvolvimento e Product Owner assistidos por Agente de IA.
- **Relacionamento:** **Derivada do PRD e do Documento de Visão**; alimenta o *Plano de Iteração* e a *Especificação de User Stories*.

### 2.4 Especificação de User Stories — `templates/esp-userstories.md`
- **Propósito:** Detalhamento individual de cada história de usuário, contendo regras de negócio, critérios de aceite em formato BDD/Gherkin, fluxos de exceção, protótipos e diagramas de apoio (classes, sequência).
- **Quando é gerado:** Durante a Elaboração e no início de cada Iteração de Construção.
- **Quem produz:** Engenheiros de Requisitos e Desenvolvedores em colaboração com Agente de IA.
- **Relacionamento:** É alimentada pela *Lista de User Stories* e pelo *PRD*, e **alimenta a codificação e a criação de testes automatizados**.

### 2.5 Documento de Modelos — `templates/doc-modelos.md`
- **Propósito:** Registro dos modelos estruturais e comportamentais do sistema. É mantido como **documento separado por padrão**, contendo:
  - **Modelo Conceitual (Domínio):** Diagramas conceituais e de classes de domínio que descrevem os conceitos do negócio;
  - **Modelo de Dados (DER / Lógico):** Diagrama Entidade-Relacionamento e esquemas lógicos de persistência;
  - **Dicionário de Dados:** Descrição tabular detalhada de cada entidade, atributo, tipos e restrições;
  - **Diagramas de Sequência/Comportamento:** Fluxos de interação críticos.
- **Flexibilidade:** O líder técnico tem a liberdade de unificar este conteúdo no Documento de Visão caso prefira uma documentação centralizada para projetos menores.
- **Quando é gerado:** Fase de Elaboração e atualizado incrementalmente na Construção.
- **Quem produz:** Arquiteto de Software e Modelador de Dados com Agente de Modelagem.
- **Relacionamento:** Rastreia as entidades descritas no PRD e nas User Stories, alimentando o *Documento de Arquitetura* e a implementação de banco/código.

### 2.6 Documento de Arquitetura — `templates/doc-arquitetura.md`
- **Propósito:** Consolidação das decisões arquiteturais (ADRs), padrões técnicos, visão de componentes (C4 Model), infraestrutura e segurança.
- **Quando é gerado:** Fase de Elaboração e refinado durante a Construção.
- **Quem produz:** Arquiteto de Software com Agente de Arquitetura.
- **Relacionamento:** Baseia-se no *Documento de Modelos* e no *PRD* (requisitos não-funcionais), direcionando a estrutura do código-fonte.

### 2.7 Especificação e Configuração de Agentes — `templates/doc-agentes.md`
- **Propósito:** Formaliza os system prompts, ferramentas, papéis especializados e protocolos de validação humana dos agentes de IA adotados.
- **Quando é gerado:** Fase de Elaboração / Configuração Inicial.
- **Quem produz:** Equipe técnica / Líder de IA.
- **Relacionamento:** Guia as instruções presentes no diretório `prompts/` e `AGENTS.md`.

### 2.8 Termo de Abertura do Projeto (TAP) — `templates/termo-abertura.md`
- **Propósito:** Formaliza o início do projeto, objetivos acadêmicos, equipe e marcos macros no limite de 60 horas.
- **Quando é gerado:** Início da Fase de Concepção.
- **Relacionamento:** Alinhado com o *Documento de Visão*.

### 2.9 Termo de Encerramento do Projeto (TEP) — `templates/termo-encerramento.md`
- **Propósito:** Registra o encerramento do projeto, escopo realizado vs. planejado, métricas de qualidade e lições aprendidas.
- **Quando é gerado:** Fase de Transição / Encerramento.
- **Relacionamento:** Consolida os resultados obtidos em todas as releases e iterações.

### 2.10 Artefatos Operacionais de Ciclo
- **Plano de Release / Plano de Iteração:** Define o subconjunto de User Stories a serem construídas no ciclo e a alocação do time.
- **Plano de Testes e Relatório de Testes:** Planejamento e evidências de cobertura dos testes unitários, de integração e de aceitação executados.
- **Atas de Reunião:** Registros sucintos das decisões e alinhamentos semanais da equipe.

- Regra de decisão — quando especificar uma User Story: para CRUD simples sobre entidades com Design System maduro, o PRD + Lista de User Stories são suficientes para a implementação. A Especificação de User Stories é OBRIGATÓRIA quando a US possui regra de negócio complexa, fluxo não-linear, cálculo, integração externa ou alto risco.
