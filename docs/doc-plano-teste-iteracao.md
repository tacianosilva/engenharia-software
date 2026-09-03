# Plano de Teste da Iteração

**Projeto:** [Nome do Projeto]  
**Iteração:** [Número / Nome da Iteração, ex.: Iteração 02]  
**Período:** DD/MM/AAAA a DD/MM/AAAA  
**Membros Responsáveis:** [Nome dos Papéis de Teste da Iteração do easYProcess]  

---

## 1. Objetivos da Iteração
[Descrever resumidamente o objetivo de negócio e técnico desta iteração.]

---

## 2. User Stories (US) Abordadas na Iteração
| ID US | Título da User Story | Requisitos Envolvidos | Tamanho Funcional | Prioridade |
| :--- | :--- | :--- | :--- | :--- |
| **US01** | Cadastrar Usuário | RF01, RF03 | 3 | Alta |
| **US02** | Recuperar Senha | RF02 | 2 | Média |

---

## 3. Matriz de Casos de Teste de Aceitação da Iteração

> **Nota:** Os cenários descritos aqui detalham os Critérios de Aceitação descritos no documento de User Story, preparando o roteiro de homologação com o cliente.

### US01 - [Título da US01]
* **Requisitos Associados:** [ex.: RF01, RNF02]
* **Pré-condições:** [O que deve estar configurado antes da execução do teste]

| ID Caso de Teste | Cenário de Teste / Descrição | Passos para Execução | Dados de Entrada | Resultado Esperado | Tipo de Teste (Manual / Auto) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **CT01.01** | Cadastro com dados válidos | 1. Acessar tela de cadastro<br>2. Preencher campos obrigatórios<br>3. Clicar em 'Salvar' | Nome: "Ana"<br>Email: "ana@email.com"<br>Senha: "123456" | Exibir mensagem de sucesso e redirecionar para tela de Login. | Manual / Aceitação |
| **CT01.02** | Tentativa de cadastro com e-mail já existente | 1. Acessar tela de cadastro<br>2. Informar e-mail já cadastrado<br>3. Clicar em 'Salvar' | Email: "existente@email.com" | Exibir alerta: "E-mail já cadastrado no sistema". | Automatizado |

---

### US02 - [Título da US02]
* **Requisitos Associados:** [ex.: RF02]
* **Pré-condições:** [Condições prévias para os testes]

| ID Caso de Teste | Cenário de Teste / Descrição | Passos para Execução | Dados de Entrada | Resultado Esperado | Tipo de Teste (Manual / Auto) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **CT02.01** | Solicitar recuperação para e-mail cadastrado | 1. Acessar 'Esqueci Senha'<br>2. Digitar e-mail válido<br>3. Clicar em 'Enviar' | Email: "usuario@email.com" | Mensagem informando envio de link para o e-mail. | Manual / Aceitação |

---

## 4. Critérios de Entrada e Saída da Iteração

### 4.1. Critérios de Entrada (Quando os testes de aceitação podem iniciar?)
- [ ] Código-fonte da User Story mergeado na branch de homologação/staging.
- [ ] Testes de Unidade executados com 100% de aprovação no ambiente CI/CD.
- [ ] Ambiente de testes/homologação atualizado e funcional.

### 4.2. Critérios de Saída (Quando a Iteração é considerada Aceita pelo Cliente?)
- [ ] 100% dos Casos de Teste de Aceitação planejados foram executados.
- [ ] NENHUM bug de prioridade **Alta** ou **Crítica** em aberto.
- [ ] Homologação / Validação formal do Cliente / Product Owner realizada nos testes de Aceitação.

---

## 5. Cronograma de Execução na Iteração
| Atividade | Responsável (YP) | Data Início | Data Fim |
| :--- | :--- | :--- | :--- |
| Mapeamento dos Casos de Teste | [Membro do YP] | DD/MM/AAAA | DD/MM/AAAA |
| Execução dos Testes Automatizados | [Membro do YP] | DD/MM/AAAA | DD/MM/AAAA |
| Sessão de Testes de Aceitação (com Cliente) | [Membro do YP / Cliente] | DD/MM/AAAA | DD/MM/AAAA |
