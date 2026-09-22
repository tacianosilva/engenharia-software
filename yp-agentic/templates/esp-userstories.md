# Especificação de User Story — US01 [Nome da Entidade]

> **Quando usar:** este documento é opcional. Use-o quando a User Story tiver regra de negócio complexa, fluxo não-linear, cálculo, integração externa ou alto risco. Para CRUD simples, o PRD + Lista de User Stories são suficientes.

## 1. Identificação

| Campo | Valor |
|---|---|
| **Projeto** | [Nome do projeto] |
| **Data** | DD/MM/AAAA |
| **Versão** | 1.0 |
| **US** | US01 — [Nome curto e descritivo] |
| **Story** | Como [papel], quero [ação], para [benefício]. |
| **Prioridade** | [P0 / P1 / P2] |
| **Analista** | [Nome] |
| **Desenvolvedor** | [Nome] |
| **Testador** | [Nome] |
| **Release / Iteração** | [Ex.: R1 / I2] |
| **Esforço** | [P / M / G ou Story Points] |

## 2. Contexto de Negócio

[Valor de negócio da US: por que ela existe, qual persona atende e qual dor resolve.]

## 3. Requisitos Internos

| ID | Descrição | Prioridade |
|---|---|---|
| RF01 | [Cadastrar ...] | P0 |
| RF02 | [Listar ...] | P0 |
| RF03 | [Atualizar ...] | P1 |
| RF04 | [Excluir ...] | P1 |

## 4. Regras de Negócio

- **RN01:** [Validação, cálculo, restrição ou estado obrigatório]
- **RN02:** [Descrição da regra]
- **RN03:** [Descrição da regra]

## 5. Fluxos

### 5.1 Fluxo Principal
1. [Passo 1 — ação do usuário]
2. [Passo 2 — resposta do sistema]
3. [Passo 3 — resultado esperado]

### 5.2 Fluxos Alternativos e de Erro
- **FA01 — [Nome]:** [Descrição do caminho alternativo]
- **FE01 — [Nome]:** [Descrição do erro e mensagem exibida]

## 6. Diagramas

### 6.1 Diagrama de Classes (Mermaid)
[Inserir diagrama aqui — Mermaid ou imagem]

### 6.2 Diagrama de Sequência (Mermaid) — Cenário Principal
[Inserir diagrama aqui — Mermaid ou imagem]

### 6.3 Diagrama de Estados (opcional — se houver máquina de estados)
[Inserir diagrama aqui — Mermaid ou imagem]

## 7. Protótipo e Design
- **Protótipo:** [Link Figma ou imagem]
- **Componentes do DESIGN.md:** [Ex.: botão primário, tabela, modal, formulário — referência ao arquivo DESIGN.md do projeto]
- **Descrição da tela:** [O que o usuário vê e faz nesta tela]

## 8. Critérios de Aceitação (Gherkin)

```gherkin
Cenário: 1 — [Nome do cenário feliz]
  Dado que [estado inicial]
  Quando [ação do usuário]
  Então [resultado esperado]

Cenário: 2 — [Nome do cenário alternativo]
  Dado que [estado inicial]
  Quando [ação do usuário]
  Então [resultado esperado]

Cenário: 3 — [Nome do cenário de erro]
  Dado que [estado inicial]
  Quando [ação que causa o erro]
  Então [mensagem de erro exibida e estado mantido]
```

## 9. Dependências
- [US02 — Manter Matrícula depende desta US]
- [Integração com serviço X, definida no DESIGN.md ou Projeto Arquitetural]

## 10. Referências
- PRD — [link]
- Lista de User Stories — [link]
- Documento de Modelos — [link]
- Design System (DESIGN.md) — [link]
- Projeto Arquitetural — [link]
