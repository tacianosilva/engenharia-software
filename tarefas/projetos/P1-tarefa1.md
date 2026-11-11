# P1 — Iniciação e Planejamento do Projeto (Grupo)

**Disciplina:** Engenharia de Software II — DCT2302
**Iteração:** 1
**Metodologia:** Desenvolvimento Ágil com GitFlow

## 1. Infraestrutura e Configuração

- **Repositório Git:** Criar o repositório oficial da equipe no GitHub/GitLab.
- **Configuração Inicial:**
  - Adicionar o arquivo `.gitignore` correspondente à linguagem/framework escolhido (ex: Python, Java, Node).
  - Configurar as branches iniciais seguindo o fluxo **GitFlow** (`main` e `develop`).
- **README.md:** O arquivo principal do repositório deve conter:
  - Nome do projeto e objetivo.
  - Links para tutoriais das tecnologias utilizadas.
  - Links para os artefatos de documentação dentro da pasta `/docs`.

## 2. Documento de Visão

O documento deve ser criado em Markdown na pasta `/docs` e conter:

- **Problema:** Descrição sucinta do problema que o software resolve.
- **Requisitos Funcionais (RF):** Lista inicial (mínimo de 2 ou 3 entidades por membro da equipe).
- **Requisitos Não Funcionais (RNF):** Restrições técnicas, usabilidade, desempenho e segurança.
- **Perfis de Usuários:** Quem são os atores que interagem com o sistema.
- **Tabela de Riscos:** Identificação de possíveis impedimentos e ações de mitigação.

Utilize o modelo apresentado no documento [`docs/doc-visao.md`](/docs/doc-visao.md).

## 3. Modelagem de Dados e Persistência

- **Diagrama de Entidades:** Criar um **Diagrama de Classes UML** ou **Diagrama Entidade-Relacionamento (DER)** utilizando a sintaxe **Mermaid** diretamente no Markdown.
- **Dicionário de Dados:** Documento detalhando os atributos (nome, tipo, restrições) das entidades para persistência.

Utilize o modelo apresentado no documento [`docs/doc-modelos.md`](/docs/doc-modelos.md).

## 4. Lista de User Stories (Versão 1)

Tabela contendo o planejamento inicial das funcionalidades:

| ID | Título do User Story | Requisitos Funcionais Relacionados | Responsável pelo Detalhamento |
| :--- | :--- | :--- | :--- |
| US01 | Manter Cadastro de Usuários | RF01, RF02 | Nome do Membro A |
| US02 | Gerenciar Estoque | RF03, RF04 | Nome do Membro B |

Utilize o modelo apresentado no documento [`docs/doc-userstories.md`](/docs/doc-userstories.md).

## 5. Entrega

- Link do repositório com o histórico de commits seguindo o padrão de **Conventional Commits**.
- Link dos documentos (artefatos) no repositório.
- Criar artefatos do projeto no [AcademicDevFlow](https://labens.dct.ufrn.br/academicflow/).
- Todos os documentos devem estar integrados ao repositório.

## 6. Links e Dicas

- Versionamento Semântico — <https://semver.org/lang/pt-BR/>
- Conventional Commits — <https://www.conventionalcommits.org/pt-br/v1.0.0/>
- AcademicDevFlow — <https://labens.dct.ufrn.br/academicflow/>

Acesse o sistema AcademicDevFlow e crie uma conta. Navegue pelo sistema e cadastre pelo menos um feedback. O Líder Técnico deve criar o Projeto no sistema e vincular os membros da equipe.
