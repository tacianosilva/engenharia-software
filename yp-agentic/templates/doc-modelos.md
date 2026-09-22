# Documento de Modelos

**Projeto:** [Nome do Projeto]  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  

> **Documentos de entrada:** [Documento de Visão](link) e [PRD](link) validados. Este documento descreve o modelo conceitual e de dados do sistema — não repita conteúdo da Visão ou do PRD, apenas linke. Dependendo do porte do projeto, este conteúdo pode ser incorporado como seção do Documento de Visão.

## 1. Visão Geral dos Modelos
[Descrição sucinta dos modelos: entidades principais, nível de detalhe adotado e relação com as funcionalidades do PRD.]

## 2. Modelo Conceitual (UML)

### 2.1 Diagrama de Classes
[Inserir diagrama aqui — Mermaid ou imagem]

### 2.2 Descrição das Entidades
| Entidade | Descrição | Atributos Principais |
|---|---|---|
| [Entidade] | [Quem é e qual papel desempenha] | [atributos] |
| [Entidade] | [O que representa no domínio] | [atributos] |

## 3. Modelo de Dados (ER)

### 3.1 Diagrama Entidade-Relacionamento
[Inserir diagrama aqui — Mermaid ou imagem]

### 3.2 Tabelas e Campos
| Tabela | Campo | Tipo | PK/FK | Obrigatório | Observação |
|---|---|---|---|---|---|
| [Tabela] | [Campo] | [Tipo] | [PK/FK] | [Sim/Não] | [Observação] |

## 4. Dicionário de Dados
| Campo | Tipo | Tamanho | Formato | Validação | Valores Permitidos |
|---|---|---|---|---|---|
| [Campo] | [Tipo] | [Tamanho] | [Formato] | [Validação] | [Valores] |

## 5. Regras de Integridade
- [Chave primária de cada tabela]
- [Chaves estrangeiras e ações de exclusão (CASCADE/RESTRICT)]
- [Campos únicos (UK)]
- [Restrições de unicidade e validações de domínio]

## 6. Contratos de API (opcional)
> Se os endpoints forem definidos aqui, liste-os; caso contrário, linke para a Especificação de User Stories onde são detalhados.

| Endpoint | Método | Descrição | Entrada | Saída |
|---|---|---|---|---|
| [Endpoint] | [Método] | [Descrição] | [Entrada] | [Saída] |

## 7. Decisão de Estrutura
[Registrar se o modelo ficou neste documento separado ou como seção do Documento de Visão, e o motivo da decisão.]

## 8. Referências
- [Documento de Visão](link)
- [PRD](link)
- [Lista de User Stories](link)
- [Especificação de User Stories](link)
- [Projeto Arquitetural](link)
