# Plano Geral de Testes de Software

**Projeto:** [Nome do Projeto]  
**Equipe/Grupo:** [Nome do Grupo]  
**Processo:** YP-Agentic  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  

> **Documentos de entrada:** [Documento de Visão](link) e [PRD](link) validados. Este documento é a fonte única da estratégia de testes — não repita conteúdo da Visão ou do PRD, apenas linke.

## 1. Visão Geral do Sistema
Ver [Documento de Visão](link) — seção 1 (propósito, público-alvo e contexto). Apenas link, sem resumir o sistema aqui.

## 2. Escopo do Plano de Testes

### 2.1 Itens no Escopo (O que será testado)
- Testes unitários e de integração dos componentes do sistema.
- Testes dos Requisitos Funcionais (validados via User Stories — ver [Lista de User Stories](link)).
- Testes dos Requisitos Não Funcionais (RNFs definidos no [Documento de Visão §4.2](link)).

### 2.2 Itens Fora do Escopo
- [O que não será testado nesta versão]

## 3. Estratégia de Testes por Requisito Não Funcional (RNF)

> A descrição do RNF vive no [Documento de Visão §4.2](link). Aqui registre apenas a abordagem de teste e a métrica — sem repetir a descrição.

| RNF | Tipo / Categoria | Abordagem / Estratégia de Teste | Critério de Aceitação / Métrica |
|---|---|---|---|
| [RNF01](link) | Desempenho / Carga | Teste de carga automatizado (JMeter/k6) | Tempo de resposta < X s para 95% das requisições |
| [RNF02](link) | Segurança | SAST + análise de vulnerabilidades | Nenhuma vulnerabilidade alta/crítica |
| [RNF03](link) | Usabilidade | Avaliação heurística + teste com usuários | Taxa de conclusão > 90% |

## 4. Tipos e Níveis de Teste

### 4.1 Testes de Unidade
- **Foco:** funções, classes e métodos isolados.
- **Responsável:** Desenvolvedor.
- **Ferramentas:** [JUnit, PyTest, Jest...].
- **Métrica:** cobertura mínima de [X]% nas regras de negócio.

### 4.2 Testes de Integração
- **Foco:** comunicação entre módulos, persistência e APIs externas.
- **Responsável:** Desenvolvedor / Testador.
- **Ferramentas:** [Postman, Supertest, Testcontainers...].

### 4.3 Testes de Sistema e Aceitação
- **Foco:** fluxo de ponta a ponta baseado em User Stories, com validação do cliente.
- **Responsável:** Equipe de Teste / Cliente.
- **Detalhamento por iteração:** ver [Plano de Teste da Iteração](link).

## 5. Ferramentas Utilizadas

| Categoria | Ferramenta | Finalidade |
|---|---|---|
| Gestão de Testes | GitHub / Issues | Registro de casos e defeitos |
| Automação Unit/Integração | [JUnit/Jest] | Execução automatizada |
| Análise Estática | [SonarQube] | Cobertura e dívida técnica |

## 6. Riscos e Contingências

| Risco | Impacto | Ação Mitigatória |
|---|---|---|
| Atraso na entrega dos módulos | Alto | Antecipar escrita dos casos de teste |

## 7. Referências
- [Documento de Visão](link)
- [PRD](link)
- [Lista de User Stories](link)
- [Especificação de User Stories](link)
- [Projeto Arquitetural](link)
- [Plano de Teste da Iteração](link)
- [Relatório de Testes](link)
