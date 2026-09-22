# Manual de Uso — Prompt Gerador do Documento de Visão (YP-Agentic)

## 1. Contexto e Caráter Iterativo Incremental
O **YP-Agentic** é um processo acadêmico de desenvolvimento de software (LABENS/UFRN, 60h) focado em **desenvolvimento assistido por agentes de IA**, combinando a qualidade técnica e testes contínuos do **XP** com os ciclos curtos e gestão colaborativa do **Scrum**.

O processo é explicitamente **iterativo e incremental**: o avanço se dá em ciclos de tempo fixo (*timebox*, tipicamente 2 semanas) com escopo variável, onde cada iteração entrega um incremento funcional executável. Os loops de retorno (*Próxima Iteração → Planejamento de Iteração* e *Próxima Release → Planejamento de Releases*) constituem o núcleo dinâmico do processo.

---

## 2. Objetivo do Manual
Orientar o Engenheiro de Software, Analista de Sistemas ou Desenvolvedor na condução da elicitação (via entrevista direta ou processamento de material prévio/brainstorm) para gerar o **Documento de Visão** no padrão oficial do YP-Agentic, pronto para validação e para servir de base ao **PRD (Product Requirements Document)**.

---

## 3. Pré-requisitos
- Repositório do projeto configurado com a pasta `templates/` (copiada de `yp-agentic`).
- Equipe e papéis definidos: Analista, Líder Técnico, Desenvolvedor, Testador.
- Cliente ou professor/orientador identificado.
- Chat com IA aberto (Adapta ONE, Claude Code, Cursor, OpenCode ou outro).
- Prompt de elicitação disponível em `prompts/doc-visao.md`.
- Template oficial disponível em `templates/doc-visao.md`.

---

## 4. Passo a Passo de Execução

### Passo 1 — Preparação
1. Abra uma nova sessão no chat de IA.
2. Copie e cole as instruções contidas no arquivo `prompts/doc-visao.md`.

### Passo 2 — Entrada do Material Prévio (Opcional, mas Recomendado)
Se a equipe já realizou reuniões preliminares, dinâmicas de brainstorm ou possui anotações de conversas com o cliente:
1. Envie esse material em texto **junto ou logo após o prompt**, antes da primeira pergunta da IA.
2. A IA irá:
   - Extrair as informações já existentes;
   - Apresentar um resumo estruturado (em bullets) do que foi compreendido;
   - Filtrar a entrevista para perguntar **apenas as lacunas e pontos ambíguos**.

### Passo 3 — Entrevista Complementar
1. Se não houver material prévio, a IA iniciará a entrevista completa, fazendo **uma pergunta por vez**.
2. Responda de forma direta e objetiva.
3. Caso alguma informação ainda não esteja definida ou seja desconhecida, responda *"não sei"* ou *"a definir"*. A IA registrará expressamente como `[A definir]` no template.

### Passo 4 — Consolidação e Revisão
1. Ao concluir os tópicos, o agente de IA apresentará o **Documento de Visão** preenchido na estrutura de `templates/doc-visao.md`.
2. A equipe deve revisar:
   - Alinhamento do problema, oportunidade e solução proposta;
   - Perfis de usuário e responsabilidades;
   - Requisitos funcionais e não-funcionais de alto nível;
   - Restrições, riscos e critérios de sucesso mensuráveis.
3. *Nota de Escopo:* Conforme o porte do projeto, o Documento de Visão pode absorver o modelo conceitual de domínio preliminar ou manter essa responsabilidade a cargo do Documento de Modelos (`templates/doc-modelos.md`).

### Passo 5 — Validação com Cliente e Stakeholders
1. Apresente o Documento de Visão consolidado ao cliente/professor.
2. Obtenha aprovação formal ou registre os ajustes solicitados. Este documento funciona como o acordo inicial de escopo e proposta de valor do projeto.

### Passo 6 — Salvamento no Repositório
1. Salve a versão aprovada no repositório do projeto no caminho `docs/doc-visao.md` (ou `templates/doc-visao.md`).
2. Registre o artefato e suas versões conforme as diretrizes do projeto.

---

## 5. Próximos Passos: Da Entrevista até o PRD

O Documento de Visão e o PRD desempenham papéis complementares e sequenciais no fluxo do YP-Agentic:

| Dimensão | Documento de Visão (`doc-visao.md`) | PRD (`prd.md`) |
|---|---|---|
| **Pergunta Central** | *Por que* e *Para quem* construir? | *O que* construir e *Como saberemos que deu certo*? |
| **Foco Principal** | Problema, oportunidade, stakeholders e limites gerais | Funcionalidades priorizadas, personas, métricas e escopo detalhado |
| **Papel no Processo** | Acordo estratégico de negócio | Artefato de decisão que substitui a lista de RFs avulsos |
| **Alimenta** | O próprio PRD e o Termo de Abertura (TAP) | Lista de User Stories (`doc-userstories.md`) e Especificações (`esp-userstories.md`) |

### Trilha Sequencial até as User Stories:
```text
[Brainstorm / Entrevista]
         │
         ▼
[Documento de Visão] ──(Validação com Cliente)──► [Termo de Abertura / TAP]
         │
         ▼
[Definição de Personas e Cenários]
         │
         ▼
[Funcionalidades de Alto Nível (Features)]
         │
         ▼
[Priorização P0 / P1 / P2 (MoSCoW)]
         │
         ▼
[Critérios de Sucesso Mensuráveis & Limites In/Out Scope]
         │
         ▼
[Redação e Validação do PRD]
         │
         ▼
[Derivação da Lista de User Stories e Especificações BDD]
         │
         ▼
[Planejamento de Releases e Iterações (Ciclos de 2 semanas)]
```
