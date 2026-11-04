# T3 - Tarefa 03 - Integração Contínua (CI) e SonarQube

**Turma:** DCT2302 — 2026.2-TIND (Ensino Individualizado)  
**Discente:** Artur Morais Candeia  
**Publicação:** 27/10/2026  
**Data limite de envio:** 10/11/2026  

Para responder às questões abaixo você deve utilizar um **fork** do repositório **engenharia-software** no GitHub: [https://github.com/tacianosilva/engenharia-software](https://github.com/tacianosilva/engenharia-software). Acesse o Guia Básico de Markdown: [https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown](https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown)

---

### Instruções no Repositório da Disciplina

1. Cadastre uma tarefa (issue) para você com o título **“Tarefa 03 — DCT2302 — 2026.2-TIND — Integração Contínua (CI) e SonarQube \<nomedodiscente\>”** no repositório da disciplina.
2. No seu clone local do fork do `engenharia-software`, atualize sua branch `main` com o repositório original (*upstream/main*).
3. Crie uma branch específica para a tarefa: `git checkout -b task/issueID` (substituindo `issueID` pelo número da sua issue cadastrada).
4. Dentro do diretório `tarefas/2026.2-TIND/<username>/`, crie o arquivo **`tarefa03.md`** e adicione o link para ele no seu **`README.md`**.
5. No arquivo **`tarefa03.md`**, inclua:
   - **Título:** “Tarefa 03 — Integração Contínua (CI) e SonarQube”;
   - **Identificação:** Seu nome completo, usuário GitHub e e-mail;
   - **Links de Entrega:** Link do repositório do projeto SIGAEX, link do Pull Request no projeto e link da análise no SonarQube do LABENS.
6. Para resolver as questões teóricas e práticas, faça commits atômicos com *Conventional Commits* referenciando o ID da issue (`#<id_issue>`). Ao final da atividade, faça push para o seu fork e abra o **Pull Request** para a branch `main` do repositório da disciplina.

---

### Questões da Tarefa

7. **Pesquisa Teórica sobre CI e Análise Estática:**  
   Crie uma seção no seu `tarefa03.md` respondendo aos seguintes tópicos de pesquisa:
   1. O que é **Integração Contínua (CI)**? Explique seu conceito, benefícios e como ela apoia o desenvolvimento ágil em equipe.
   2. Faça uma comparação sucinta entre três ferramentas populares de CI/CD: **GitHub Actions**, **GitLab CI** e **Jenkins**.
   3. O que é **Análise Estática de Código**? Explique os conceitos de *bugs*, *vulnerabilidades*, *code smells*, *dívida técnica* e *Quality Gate*.
   4. Explique a arquitetura e o funcionamento do **SonarQube** (SonarScanner, servidor e base de dados), detalhando como o cálculo de cobertura de código (*code coverage*) é gerado e integrado ao relatório.

8. **Implementação Prática no Projeto SIGAEX:**  
   No repositório do projeto SIGAEX (backend ou frontend):
   1. Cadastre uma issue no repositório do projeto (ex.: "Configurar CI com GitHub Actions e SonarQube") e crie uma branch nomeada com o ID da issue.
   2. **Workflow de Integração Contínua no GitHub Actions:**  
      - Crie ou atualize o workflow em `.github/workflows/` disparado em eventos de `push` e `pull_request`.
      - O workflow deve contemplar, no mínimo:
        - Checkout do repositório;
        - Configuração do ambiente (Python/Django ou Node.js/Vue);
        - Instalação de dependências do projeto;
        - Execução automatizada da suíte de testes com ferramenta de cobertura (`pytest` com `pytest-cov` ou `vitest --coverage`);
        - Geração de relatório de cobertura em formato compatível com o SonarQube (ex.: XML de cobertura ou lcov).
   3. **Configuração e Execução do SonarQube:**  
      - Crie o arquivo `sonar-project.properties` na raiz do projeto com as configurações apropriadas (`sonar.projectKey`, `sonar.sources`, caminhos de testes e de cobertura).
      - Configure o step do **SonarQube Scanner** no GitHub Actions apontando para o servidor do LABENS ([https://labens.dct.ufrn.br/sonarqube/](https://labens.dct.ufrn.br/sonarqube/)), utilizando os segredos (`SONAR_TOKEN` e `SONAR_HOST_URL`) cadastrados nos Secrets do repositório. Consulte o [Guia de Configuração do SonarQube](https://github.com/tacianosilva/engenharia-software/blob/main/docs/sonarqube/config.md).
      - Demonstre a execução bem-sucedida do workflow (pipeline verde) com prints e links das *Actions runs*.
   4. **Inspeção de Resultados e Correção de Débitos Técnicos:**  
      - Apresente o dashboard do projeto no SonarQube do LABENS com os percentuais de cobertura obtidos e métricas de qualidade.
      - Selecione pelo menos **2 problemas** apontados pela análise do SonarQube (sejam code smells, vulnerabilidades ou bugs) e realize a correção no código-fonte, referenciando os commits de correção no `tarefa03.md`.
      - Abra o Pull Request no repositório do projeto integrando a configuração de CI e as correções realizadas.

---

### Boas Práticas

1. Atualizar seu fork a partir do original antes de iniciar.
2. Criar branches específicas para as tarefas.
3. Fazer commits pequenos e atômicos seguindo **Conventional Commits** referenciando a issue (`#<id_issue>`).
4. Abrir Pull Requests com título claro e descrição completa das mudanças.
