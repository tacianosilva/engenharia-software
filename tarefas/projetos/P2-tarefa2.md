# P2 — Detalhamento de Requisitos e Arquitetura (Grupo)

**Disciplina:** Engenharia de Software II — DCT2302
**Iteração:** 1
**Foco:** Análise Técnica e Definição Estrutural

## 1. Atualizações de Análise

- **Documento de Visão:** Revisar e atualizar os requisitos e riscos com base no feedback da primeira etapa.
- **Novas User Stories:** Cada membro da equipe deve acrescentar pelo menos uma nova User Story à lista original para análise.

## 2. Detalhamento dos User Stories

Cada membro, no papel de **Analista de Sistemas**, deve detalhar o User Story sob sua responsabilidade contendo:

- **Descrição:** Narrativa detalhada do valor entregue ao usuário.
- **Regras de Negócio (RN):** Condições lógicas e restrições que devem ser aplicadas (ex: "A idade mínima para cadastro é 18 anos").
- **Mensagens:** Definição das mensagens de sucesso, erro e alertas do sistema.
- **Modelo de Dados Relacionado:** Um trecho do diagrama (fragmento) ou descrição das tabelas impactadas por este US.
- **Lista de Testes de Aceitação:** Critérios objetivos para validar se a funcionalidade está pronta (ex: "Dado que o usuário preencheu o campo X, quando clicar em enviar, então o registro deve ser salvo no banco").

Utilize o modelo apresentado no documento [`docs/doc-userstories.md`](/docs/doc-userstories.md).

## 3. Documento de Arquitetura do Software

Criar um documento `/docs/arquitetura.md` contendo:

- **Visão Geral:** Figura/Diagrama representando as camadas do sistema (Frontend e Backend).
- **Tabela de Tecnologias:**

| Mecanismo de Análise | Tecnologia de Implementação | Justificativa/Responsabilidade |
| :--- | :--- | :--- |
| **Frontend** | Ex: React / Vue.js | Interface responsiva e consumo de API. |
| **Backend** | Ex: Django / Python / Scala | Regras de negócio e API RESTful. |
| **Persistência** | Ex: MariaDB / MongoDB | Armazenamento relacional ou não-relacional. |
| **Containerização** | Ex: Docker | Padronização do ambiente de desenvolvimento. |

- **Implantação (Opcional):** Pequena descrição de como o sistema será publicado ou executado (ex: Docker Compose).

Utilize o modelo apresentado no documento [`docs/doc-arquitetura.md`](/docs/doc-arquitetura.md).

## 4. Padronização e Repositório

- **GitFlow:** Verificação do uso correto de branches `feature/` para cada User Story detalhada.
- **Formato:** Todos os artefatos devem estar rigorosamente em Markdown dentro do repositório.
- **AcademicDevFlow:** Garantir que todos os membros estejam vinculados ao projeto no sistema de acompanhamento.

## 5. Entrega

- Link do repositório atualizado.
- Link dos documentos (artefatos) no repositório.
- Criar artefatos do projeto no [AcademicDevFlow](https://labens.dct.ufrn.br/academicflow/).
- Todos os documentos devem estar integrados ao repositório.
- O arquivo de arquitetura deve estar na raiz da pasta de documentação.

## 6. Links e Dicas

- Versionamento Semântico — <https://semver.org/lang/pt-BR/>
- Conventional Commits — <https://www.conventionalcommits.org/pt-br/v1.0.0/>
- AcademicDevFlow — <https://labens.dct.ufrn.br/academicflow/>
