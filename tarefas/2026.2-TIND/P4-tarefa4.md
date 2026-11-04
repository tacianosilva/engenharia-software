# P4 - Projeto 04 - Evolução e Testes de Sistema com Selenium

**Disciplina:** Engenharia de Software II — DCT2302  
**Turma:** 2026.2-TIND (Ensino Individualizado)  
**Iteração:** 3  
**Foco:** Evolução, Testes de Sistema (Selenium), Qualidade e Correção de Bugs  
**Discente:** Artur Morais Candeia  
**Publicação:** 03/11/2026  
**Data limite de envio:** **17/11/2026**  

---

## 1. Revisão e Atualização dos Documentos

Revisar e atualizar na pasta `docs/` dos repositórios do projeto:

- **Documento de Visão e PRD:** Refletir o escopo atualizado do SIGAEX.
- **Documento de Modelos:** Atualizar entidades, DER e dicionário de dados.
- **Documento Lista de User Stories:** Atualizar status das USs e prioridades.
- **Documento de Projeto Arquitetural:** Documentar decisões de integração entre backend DRF e frontend Vue 3.
- **Plano de Iteração:** Registrar o planejamento e acompanhamento da Iteração 3.

---

## 2. Implementação de User Stories

- Implementar **pelo menos 2 User Stories funcionais completas** (da tela ao banco de dados no SIGAEX).
- Desenvolver os respectivos **testes de unidade e integração** para as regras de negócio e endpoints implementados.

---

## 3. Testes de Sistema com Selenium e Encaminhamento de Bugs

Pela ementa de Engenharia de Software II, realiza-se uma prática focada de **Testes de Sistema** (com escopo reduzido em relação à disciplina específica de Teste de Software):

1. **Construção de Testes de Sistema Automatizados com Selenium:**
   - Implementar uma suíte de testes de sistema automatizados utilizando **Selenium** (em Python com `pytest` + `selenium`, ou webdriver integrado ao projeto).
   - A suíte deve cobrir os fluxos críticos de ponta a ponta na interface web do SIGAEX integrando frontend e backend (ex.: login/autenticação, cadastro de novo evento pelo organizador e fluxo de inscrição de participante).
2. **Relatório de Resultados dos Testes:**
   - Executar a suíte de testes e gerar o **Relatório de Testes de Sistema** em Markdown (`docs/relatorio-testes-sistema.md`), descrevendo os cenários executados, massa de dados utilizada, evidências de execução (sucesso/falha) e tempo de resposta.
3. **Encaminhamento para Issues de Bugs:**
   - Para cada falha, inconsistência de validação, erro de integração ou oportunidade de ajuste detectada pelos testes de sistema ou de unidade, **cadastrar imediatamente uma issue no GitHub**.
   - As issues devem conter passos para reprodução, comportamento esperado vs. observado, label apropriada (`bug`, `ajuste`, `qa`) e vinculação à milestone da Iteração 3.

---

## 4. Qualidade e Cobertura de Código

- Executar a análise estática no **SonarQube do LABENS** pelo menos duas vezes por semana.
- Atingir no mínimo **65% de cobertura de código** nos testes automatizados.
- O relatório do SonarQube deve refletir a cobertura atualizada e a redução de débitos técnicos.

---

## 5. Entrega e Fluxo Git

- Criar branch temática com o ID da issue para cada entrega (`feature/#<id>-<nome>`).
- Fazer commits atômicos com **Conventional Commits** (`feat:`, `fix:`, `test:`, `docs:`) referenciando a issue.
- Abrir Pull Request descritivo para a branch `main` vinculando a issue correspondente.
- Gerar a **tag/release** semântica da Iteração 3 no repositório.
- Enviar os links na tarefa correspondente no SIGAA.
