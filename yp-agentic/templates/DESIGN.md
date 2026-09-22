# Design System (DESIGN.md)

**Projeto:** [Nome do Projeto]  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  

> **Documentos de entrada:** [Projeto Arquitetural](link) (tecnologias de frontend) e [PRD](link) (funcionalidades priorizadas). Este documento é a fonte única da identidade visual e dos componentes de interface — não repita conteúdo de outros documentos, apenas linke.
> **Quando gerar:** Planejamento de Releases (Fase 3), antes da primeira iteração. Pode começar enxuto (v1) e evoluir a cada release.

## 1. Visão Geral
[Propósito do Design System: padronizar as interfaces do produto, acelerar a implementação das User Stories e garantir consistência visual entre telas.]

## 2. Fundamentos

### 2.1 Cores
| Token | Valor (Hex) | Uso |
|---|---|---|
| [cor-primaria] | [#XXXXXX] | [Botões principais, links, destaques] |
| [cor-secundaria] | [#XXXXXX] | [Elementos secundários] |
| [cor-neutra-clara] | [#XXXXXX] | [Fundos, superfícies] |
| [cor-neutra-escura] | [#XXXXXX] | [Textos, ícones] |
| [cor-sucesso] | [#XXXXXX] | [Mensagens de sucesso] |
| [cor-erro] | [#XXXXXX] | [Mensagens de erro, validações] |
| [cor-alerta] | [#XXXXXX] | [Avisos] |

### 2.2 Tipografia
| Elemento | Fonte | Tamanho | Peso | Uso |
|---|---|---|---|---|
| [Título H1] | [Fonte] | [Xpx] | [Bold] | [Título de página] |
| [Título H2] | [Fonte] | [Xpx] | [Bold] | [Título de seção] |
| [Texto base] | [Fonte] | [Xpx] | [Regular] | [Corpo de texto] |
| [Legenda] | [Fonte] | [Xpx] | [Regular] | [Textos auxiliares] |

### 2.3 Espaçamento e Bordas
- [Escala de espaçamento: ex. 4, 8, 12, 16, 24, 32px]
- [Raio de borda padrão: ex. 8px]
- [Sombras: níveis de elevação]

## 3. Componentes
| Componente | Descrição | Estados | Referência |
|---|---|---|---|
| [Botão] | [Ação primária/secundária] | [Padrão, hover, desabilitado, loading] | [Link Figma ou imagem] |
| [Input/Formulário] | [Campos de entrada] | [Padrão, foco, erro, desabilitado] | [Link] |
| [Tabela] | [Exibição de listas] | [Padrão, vazio, loading] | [Link] |
| [Modal] | [Diálogos e confirmações] | [Aberto, fechado] | [Link] |
| [Card] | [Agrupamento de conteúdo] | [Padrão, selecionado] | [Link] |
| [Navegação] | [Menu, tabs, breadcrumbs] | [Ativo, inativo] | [Link] |
| [Feedback] | [Toast, alertas, validação] | [Sucesso, erro, alerta] | [Link] |

## 4. Padrões de Tela
- [Layout e grid: ex. 12 colunas, margens]
- [Responsividade: breakpoints e comportamento mobile]
- [Estados de tela: carregando, vazio, erro, sucesso]
- [Formulários: padrão de validação e mensagens]

## 5. Acessibilidade
- [Contraste mínimo AA]
- [Foco visível em todos os elementos interativos]
- [Textos alternativos para imagens]
- [Navegação por teclado]

## 6. Referências
- [Projeto Arquitetural](link) — tecnologias de frontend
- [PRD](link) — funcionalidades que as telas atendem
- [Especificação de User Stories](link) — protótipos e componentes por US