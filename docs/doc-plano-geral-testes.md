# Plano Geral de Testes de Software

**Projeto:** [Nome do Projeto]  
**Equipe/Grupo:** [Nome do Grupo]  
**Processo:** easYProcess (YP)  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  

---

## 1. Visão Geral do Sistema
[Breve resumo do software extraído do Documento de Visão, explicitando seu propósito principal, público-alvo e contexto de uso no mercado/organização.]

---

## 2. Escopo do Plano de Testes
### 2.1. Itens no Escopo (O que será testado)
- Testes Unitários e de Integração dos componentes do sistema.
- Testes dos Requisitos Funcionais (validados via User Stories / Casos de Uso nas iterações).
- Testes dos Requisitos Não Funcionais (RNF) definidos na documentação do sistema.

### 2.2. Itens Fora do Escopo (O que NÃO será testado)
- [Listar serviços externos de terceiros não simulados, infraestrutura fora do controle da equipe, etc.]

---

## 3. Estratégia de Testes por Requisitos Não Funcionais (RNF)

| Identificador RNF | Tipo / Categoria | Descrição do Requisito | Abordagem / Estratégia de Teste | Critério de Aceitação / Métrica |
| :--- | :--- | :--- | :--- | :--- |
| **RNF01** | Desempenho / Carga | O sistema deve suportar N requisições concorrentes. | Teste de Carga automatizado utilizando ferramentas como JMeter/k6. | Tempo de resposta menor que X segundos para 95% das requisições. |
| **RNF02** | Segurança | As senhas devem ser salvas com hash seguro e dados trafegados via HTTPS. | Teste estático de código (SAST) e testes de penetração/análise de vulnerabilidades. | Nenhuma vulnerabilidade de nível alto/crítico no relatório final. |
| **RNF03** | Usabilidade | Interface responsiva para dispositivos móveis e desktops. | Avaliação heurística e testes de usabilidade com amostragem de usuários. | Taxa de conclusão de tarefas > 90% sem auxílio externo. |
| **RNF04** | Portabilidade / Compatibilidade | Deve funcionar nos navegadores Chrome, Firefox e Edge. | Testes de renderização cross-browser automatizados ou manuais. | Comportamento e layout consistentes em todos os browsers suportados. |

---

## 4. Tipos e Níveis de Teste

### 4.1. Testes de Unidade (Unit)
- **Foco:** Funções, classes e métodos isolados.
- **Responsável:** Desenvolvedor.
- **Ferramentas:** [ex.: JUnit, PyTest, Jest].
- **Métrica Esperada:** Cobertura de código mínima de [X]% nas regras de negócio.

### 4.2. Testes de Integração
- **Foco:** Comunicação entre módulos, persistência de dados (BD) e consumo de APIs externas.
- **Responsável:** Desenvolvedor / Tester.
- **Ferramentas:** [ex.: Postman, Supertest, Testcontainers].

### 4.3. Testes de Sistema e Aceitação
- **Foco:** Validação do fluxo de ponta a ponta baseado em User Stories e Casos de Uso com participação/validação do cliente (PO/Cliente).
- **Responsável:** Equipe de Teste / Cliente (Product Owner).

---

## 5. Ambiente de Testes
- **Hardware/Servidores:** [Descrever servidor de staging/homologação]
- **Banco de Dados:** Banco de dados de testes alimentado com *fixtures* ou dados sintéticos.
- **Sistemas / APIs Externas:** Mocks ou stubs para serviços terceirizados.

---

## 6. Ferramentas Utilizadas
| Categoria | Ferramenta Escolhida | Finalidade |
| :--- | :--- | :--- |
| Gestão de Testes | GitHub / Issues | Registro de casos e defeitos |
| Automação Unit/Integração | [ex.: JUnit / Jest] | Execução automatizada de código |
| Testes de Carga/RNF | [ex.: JMeter / k6] | Simulação de acessos simultâneos |
| Análise Estática | [ex.: SonarQube] | Análise de cobertura e dívida técnica |

---

## 7. Riscos e Contingências
| Risco Identificado | Impacto no Teste | Ação Mitigatória / Contingência |
| :--- | :--- | :--- |
| Indisponibilidade do ambiente de homologação | Alto | Utilizar containers Docker locais replicando o ambiente. |
| Atraso na entrega dos módulos para desenvolvimento | Alto | Antecipar a escrita dos Casos de Teste (Módulos em paralelo). |
