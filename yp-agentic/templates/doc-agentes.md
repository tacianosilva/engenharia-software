# Documento de Agentes

**Projeto:** [Nome do Projeto]  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  

> **Documentos de entrada:** [Termo de Abertura de Projeto](link) e [Documento de Visão](link) validados. Este documento define como os agentes de IA atuam no projeto — não repita conteúdo do Termo, da Visão ou do PRD, apenas linke.

## 1. Visão Geral do Uso de Agentes
[Como os agentes de IA serão utilizados no projeto: objetivo geral, princípios (agente auxilia, humano decide) e contexto.]

## 2. Agentes e Ferramentas
| Agente/Ferramenta | Tarefas Principais | Fases do YP-Agentic | Observações |
|---|---|---|---|
| [OpenCode] | Implementação de US, geração de testes | Fase 5, Fase 6 | [Observação] |
| [Claude] | Apoio à especificação, revisão de código | Fase 3, Fase 5 | [Observação] |
| [Gemini] | [Tarefa] | [Fase] | [Observação] |

## 3. Papéis dos Agentes
| Papel do Agente | Descrição | Ferramenta | Interação com a Equipe |
|---|---|---|---|
| [Implementador] | Implementa CRUD e funcionalidades das US | [Ferramenta] | Recebe US da Lista, entrega código para revisão |
| [Gerador de Testes] | Gera testes unitários e de integração | [Ferramenta] | Valida com o Testador |
| [Revisor] | Revisa código e aponta problemas | [Ferramenta] | Reporta ao Líder Técnico |

## 4. Prompts-Base
> Os prompts-base são versionados no repositório (ex.: AGENTS.md, pasta prompts/). Aqui registre apenas a referência e o propósito.

| Prompt | Propósito | Local de Versionamento |
|---|---|---|
| [Prompt de implementação de CRUD] | Gerar código de CRUD no padrão do projeto | [AGENTS.md / prompts/] |
| [Prompt de geração de testes] | Gerar testes unitários com cobertura mínima | [AGENTS.md / prompts/] |
| [Prompt de revisão] | Revisar código segundo padrões definidos | [AGENTS.md / prompts/] |

## 5. Limites e Restrições
- [Agentes NÃO decidem arquitetura — decisão exclusiva do Líder Técnico]
- [Agentes NÃO alteram escopo ou prioridades — decisão do cliente/equipe]
- [Agentes NÃO fazem commit direto na main — sempre via revisão]
- [Código gerado por agente exige revisão humana antes de integrar]
- [Dados sensíveis não são compartilhados com agentes externos]

## 6. Fluxo de Trabalho com Agentes
| Fase do YP-Agentic | Atividade | Agente Envolvido | Responsável Humano |
|---|---|---|---|
| Fase 3 — Planejamento de Releases | Apoio à especificação de US | [Agente] | Analista |
| Fase 5 — Implementação | Implementação das US | [Agente] | Desenvolvedor |
| Fase 6 — Implantação | Geração/execução de testes | [Agente] | Testador |
| Fase 7 — Fim da Iteração | Apoio à verificação | [Agente] | Líder Técnico |

## 7. Critérios de Qualidade e Revisão
- [Revisão humana obrigatória de todo código gerado por agente]
- [Testes obrigatórios antes da integração (ver Plano Geral de Testes)]
- [Cobertura mínima de [X]% nas regras de negócio]
- [Código segue os padrões definidos no Projeto Arquitetural e DESIGN.md]
- [US só é aceita após critérios de aceitação verificados]

## 8. Responsabilidades Exclusivas da Equipe
- [Validação com o cliente]
- [Priorização de funcionalidades (P0/P1/P2)]
- [Decisões de arquitetura]
- [Aceite de User Stories]
- [Homologação final]

## 9. Registro do Uso de Agentes
[Como o uso dos agentes será documentado ao longo do projeto: atas de reunião, relatórios de iteração, histórico de prompts alterados.]

## 10. Referências
- [Termo de Abertura de Projeto](link)
- [Documento de Visão](link)
- [PRD](link)
- [Projeto Arquitetural](link)
- [Plano Geral de Testes](link)
- [AGENTS.md do repositório](link)
