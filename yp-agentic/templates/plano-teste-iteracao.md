# Plano de Teste da Iteração

**Projeto:** [Nome do Projeto]  
**Iteração:** [Número / Nome, ex.: Iteração 02]  
**Período:** DD/MM/AAAA a DD/MM/AAAA  
**Data:** DD/MM/AAAA  
**Versão:** 1.0  
**Membros Responsáveis:** [Papéis YP-Agentic de teste da iteração]  

> **Documentos de entrada:** [Plano de Iteração](link) e [Lista de User Stories](link) validados. Estratégia geral de testes: ver [Plano Geral de Testes](link). Não repita dados da Lista de US nem da Especificação — apenas linke.

## 1. Objetivos da Iteração
[Objetivo de negócio e técnico desta iteração.]

## 2. User Stories (US) Abordadas na Iteração
> Dados completos (requisitos, tamanho, prioridade) vivem na [Lista de User Stories](link).

| ID US | Título | Link |
|---|---|---|
| US01 | Cadastrar Usuário | [Lista de US](link) |
| US02 | Recuperar Senha | [Lista de US](link) |

## 3. Matriz de Casos de Teste de Aceitação da Iteração
> Os cenários abaixo operacionalizam os Critérios de Aceitação descritos na [Especificação de User Stories §8](link). Use os IDs de cenário da especificação quando existirem.

### US01 — [Título]
- **Requisitos associados:** [RF01, RNF02]
- **Pré-condições:** [O que deve estar configurado antes da execução]

| ID CT | Cenário | Passos | Dados de Entrada | Resultado Esperado | Tipo |
|---|---|---|---|---|---|
| CT01.01 | Cadastro com dados válidos | 1. Acessar cadastro; 2. Preencher; 3. Salvar | Nome: "Ana"; Email: "ana@email.com" | Mensagem de sucesso e redirecionar para Login | Manual / Aceitação |
| CT01.02 | E-mail já existente | 1. Acessar cadastro; 2. Informar e-mail existente | Email: "ana@email.com" | Mensagem de erro e permanecer na tela | Manual / Aceitação |

### US02 — [Título]
[Repetir o padrão da US01]

## 4. Critérios de Entrada e Saída da Iteração
### 4.1 Critérios de Entrada
- [US planejadas disponíveis na Lista de User Stories]
- [Especificações necessárias aprovadas]

### 4.2 Critérios de Saída (Iteração aceita pelo cliente)
- [ ] 100% dos CT de aceitação planejados executados.
- [ ] Nenhum bug de prioridade Alta ou Crítica em aberto.
- [ ] Homologação formal do cliente nos testes de aceitação.

## 5. Cronograma de Execução na Iteração
| Atividade | Responsável (YP-Agentic) | Data Início | Data Fim |
|---|---|---|---|
| Mapeamento dos casos de teste | [Membro] | DD/MM/AAAA | DD/MM/AAAA |
| Sessão de testes de aceitação (com cliente) | [Membro / Cliente] | DD/MM/AAAA | DD/MM/AAAA |

## 6. Riscos da Iteração
| Risco | Impacto | Ação Mitigatória |
|---|---|---|
| [Risco específico da iteração] | [Alto/Médio/Baixo] | [Ação] |

## 7. Referências
- [Plano Geral de Testes](link)
- [Plano de Iteração](link)
- [Lista de User Stories](link)
- [Especificação de User Stories](link)
- [Relatório de Testes](link)
