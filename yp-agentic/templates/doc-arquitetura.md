# Projeto Arquitetural

**Projeto:** [Nome do Projeto]  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  

> **Documentos de entrada:** [Documento de Visão](link) e [PRD](link) validados. Este documento descreve a arquitetura do sistema — não repita conteúdo da Visão, do PRD ou do Documento de Modelos, apenas linke.

## 1. Visão Geral da Arquitetura
[Descrição sucinta da arquitetura de alto nível: estilo adotado (monolítica, camadas, cliente-servidor, microsserviços), componentes principais e como se relacionam.]

### 1.1 Diagrama de Visão Geral (HLD)
[Inserir diagrama aqui — Mermaid ou imagem]

## 2. Componentes e Módulos
| Componente | Responsabilidade | Comunicação |
|---|---|---|
| [Frontend] | [Interface com o usuário] | [HTTP/REST com a API] |
| [API] | [Regras de negócio e exposição de endpoints] | [JDBC/ORM com o banco] |
| [Banco de Dados] | [Persistência] | [Conexão direta] |

## 3. Tecnologias e Ferramentas
| Camada | Tecnologia | Justificativa |
|---|---|---|
| Frontend | [Ex.: React, Vue] | [Motivo da escolha] |
| Backend | [Ex.: Java/Spring, Python/Django] | [Motivo da escolha] |
| Banco de Dados | [Ex.: PostgreSQL, MySQL] | [Motivo da escolha] |
| Infraestrutura | [Ex.: Docker, Vercel] | [Motivo da escolha] |

## 4. Mecanismos Arquiteturais
| Mecanismo | Abordagem |
|---|---|
| Persistência | [ORM, migrations, conexão] |
| Segurança | [Autenticação, autorização, hash de senha] |
| Logging | [Ferramenta e nível de log] |
| Tratamento de erros | [Padrão de exceções, mensagens] |
| Integrações externas | [APIs consumidas, contratos] |

## 5. Requisitos Não Funcionais e Impacto na Arquitetura
> Os RNFs são definidos no [Documento de Visão §4.2](link). Aqui registre apenas o impacto de cada um na arquitetura.

| RNF | Impacto na Arquitetura |
|---|---|
| [RNF01 — Desempenho] | [Ex.: exige cache e otimização de queries] |
| [RNF02 — Segurança] | [Ex.: exige HTTPS, hash e controle de acesso] |

## 6. Padrões e Boas Práticas
- [Padrão de projeto adotado, ex.: MVC, Repository, DTO]
- [Padrão de código e organização de pastas]
- [Convenções de API (REST, versionamento)]

## 7. Decisões de Arquitetura (ADR)
| Decisão | Motivo | Alternativa Descartada |
|---|---|---|
| [Ex.: usar PostgreSQL] | [Ex.: recursos do time e requisitos] | [Ex.: MongoDB] |
| [Ex.: monólito em camadas] | [Ex.: simplicidade para o semestre] | [Ex.: microsserviços] |

## 8. Diagramas Complementares
### 8.1 Diagrama de Componentes
[Inserir diagrama aqui — Mermaid ou imagem]

### 8.2 Diagrama de Implantação (opcional)
[Inserir diagrama aqui — Mermaid ou imagem]

## 9. Referências
- [Documento de Visão](link)
- [PRD](link)
- [Documento de Modelos](link)
- [Lista de User Stories](link)
- [Especificação de User Stories](link)
- [Design System (DESIGN.md)](link)
