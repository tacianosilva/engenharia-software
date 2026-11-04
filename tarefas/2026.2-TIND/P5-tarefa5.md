# P5 - Projeto 05 - Conteinerização com Docker, CI/CD e Implantação

**Disciplina:** Engenharia de Software II — DCT2302  
**Turma:** 2026.2-TIND (Ensino Individualizado)  
**Iteração:** 4  
**Foco:** Conteinerização com Docker, Deploy, Qualidade Máxima e Consolidação  
**Discente:** Artur Morais Candeia  
**Publicação:** 17/11/2026  
**Data limite de envio:** **08/12/2026**  

---

## 1. Revisão e Atualização dos Documentos Finais

Revisar e consolidar na pasta `docs/` dos repositórios do SIGAEX:

- **Documento de Visão e PRD:** Conclusão dos requisitos atendidos e roadmap futuro.
- **Documento de Modelos:** Modelo conceitual, DER final e dicionário de dados atualizados.
- **Documento Lista de User Stories:** Registro de todas as USs entregues e backlog residual.
- **Documento de Projeto Arquitetural:** Diagrama C4 ou arquitetural final contemplando a conteinerização e deploy.
- **Plano de Iteração e Release:** Histórico completo de iterações e releases geradas.

---

## 2. Implementação Final de User Stories

- Implementar **pelo menos 2 User Stories funcionais** (da tela ao banco de dados no SIGAEX).
- Implementar suíte de testes automatizados correspondente para manter a integridade das funcionalidades.

---

## 3. Conteinerização e Orientações para Deploy (Docker e Docker Compose)

Para a entrega final do sistema, o projeto SIGAEX deve estar 100% conteinerizado e pronto para execução e implantação:

1. **`Dockerfile` do Backend (`sigaex-backend`):**
   - Imagem base Python oficial (`python:3.12-slim`).
   - Instalação das dependências do sistema e do projeto (`requirements.txt`).
   - Coleta de arquivos estáticos (`collectstatic`).
   - Script de inicialização (`entrypoint.sh`) aplicando migrações pendentes e subindo o servidor WSGI (ex.: Gunicorn).
2. **`Dockerfile` do Frontend (`sigaex-frontend`):**
   - Estrutura multi-stage build:
     - Estágio de build com Node.js (`npm run build`).
     - Estágio de produção com Nginx leve (`nginx:alpine`) servindo a aplicação SPA (Vite/Vue 3) e configurado para roteamento HTML5.
3. **Orquestração com `docker-compose.yml`:**
   - Criar arquivo `docker-compose.yml` na raiz que orquestre:
     - Serviço de backend;
     - Serviço de frontend (com proxy das chamadas de API para o backend);
     - Banco de dados relacional e volumes persistentes.
   - Todo o sistema deve subir integrado com um único comando: `docker compose up --build`.
4. **Manuais de Orientação em Markdown:**
   - `docs/manual-execucao-desenvolvimento.md`: Guia passo a passo com comandos para clonar, configurar variáveis de ambiente (`.env.example`), executar localmente via Docker e rodar suítes de testes.
   - `docs/manual-implantacao-producao.md`: Orientações completas para implantação em servidor de produção (configuração de portas, certificados SSL, volumes persistentes, backups e boas práticas de segurança).

---

## 4. Qualidade e Cobertura de Código

- Executar a análise estática no **SonarQube do LABENS** regularmente (mín. 2x/semana).
- Atingir a meta final da disciplina de no mínimo **80% de cobertura de código** nos testes automatizados.
- Resolução comprovada de vulnerabilidades de segurança e débitos técnicos críticos apontados pelo SonarQube.

---

## 5. Entrega e Defesa da Iteração Final

- Enviar link dos repositórios atualizados, das releases SemVer finais e do dashboard do SonarQube.
- Gravar **vídeo de defesa final (10 a 15 min)** demonstrando:
  1. A execução do sistema integrado via `docker compose up`;
  2. O funcionamento das principais funcionalidades no navegador;
  3. A execução dos testes automatizados e o pipeline de CI;
  4. Apresentação das métricas de cobertura e qualidade no SonarQube;
  5. Conclusões e aprendizados do projeto individual.
