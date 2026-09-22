# Instruções para Agentes de IA — YP-Agentic

## 1. Contexto do Repositório
O **YP-Agentic** é um processo de desenvolvimento acadêmico concebido pelo **LABENS/UFRN** para o curso de Sistemas de Informação do **CERES/UFRN**, sendo uma modernização e evolução do **easYProcess (UFCG, 2003)** voltada para disciplinas de Engenharia de Software (carga horária típica de 60 horas), com foco em **desenvolvimento de software assistido por agentes de IA**.
> **Aviso de Identidade:** O nome "YP-X" foi definitivamente descontinuado. Utilize exclusivamente o termo **YP-Agentic**.

---

## 2. Leitura Obrigatória de Fundamentos, Glossário e Mapa de Posse
- Antes de gerar, analisar ou revisar qualquer documento, o agente **DEVE consultar obrigatoriamente**:
  1. [`processo/glossario.md`](processo/glossario.md) — definições formais dos termos ágeis (XP, Scrum, timeboxing, incrementos, épicos) e relações entre os artefatos;
  2. [`processo/mapa-posse.md`](processo/mapa-posse.md) — mapa de posse da informação: quem é o documento dono de cada informação e quais documentos apenas LINKAM (sem repetir conteúdo), além das regras de ouro de rastreabilidade.

---

## 3. Relação e Sequência dos Artefatos de Requisitos
Os agentes devem respeitar rigorosamente a cadeia de valor e papéis dos documentos:
1. **Documento de Visão (`doc-visao.md`):** Responde ao **"Por quê"** e **"Para quem"** (problema, oportunidade, stakeholders e limites estratégicos).
2. **PRD - Product Requirements Document (`prd.md`):** É o elo de decisão de produto que responde ao **"O quê"** priorizado e **"Como saberemos que deu certo"** (personas, features P0/P1/P2, KPIs, in/out scope, roadmap e regras de negócio). Moderniza a SRS/IEEE 830 e substitui a lista de RFs avulsos.
3. **Lista de User Stories (`doc-userstories.md`):** Fatiamento ágil das features do PRD em unidades operacionais agrupadas por entidade (CRUD) ou épicos para planejamento de releases e iterações.
4. **Especificação de User Stories (`esp-userstories.md`):** Detalhamento de execução de cada US com regras de negócio, diagramas Mermaid (classes e sequência), link do protótipo no Figma e critérios de aceite BDD (Gherkin).

---

## 4. Regras Gerais do Agente
- **Idioma Padrão:** Todo o conteúdo gerado, revisões e diálogos devem ser estritamente em **português do Brasil** (pt-BR).
- **Uso Obrigatório de Templates e Prompts:** Utilize exclusivamente os templates localizados na pasta `templates/` e as diretrizes e prompts fornecidos na pasta `prompts/`.
- **Regra da Posse da Informação:** Cada informação tem UM documento dono (fonte única). Não duplique conteúdo que já existe em outro documento — apenas **linke** para o dono, conforme [`processo/mapa-posse.md`](processo/mapa-posse.md).
- **Natureza Iterativa Incremental:** O processo avança em ciclos curtos (iterações de 2 semanas) com tempo fixo e escopo variável, entregando incrementos executáveis.
- **Proibição de Alucinação / Invenção de Dados:** Nunca invente requisitos, atores, regras de negócio ou métricas inexistentes. Sempre que uma informação for desconhecida ou pendente de decisão do usuário/equipe, marque expressamente como `[A definir]`.
- **Identificadores Estáveis:** IDs (US, RF, RNF, CT, Reunião) são referências estáveis — use-os nos links entre documentos e nunca renumere sem atualizar todos os vínculos.
- **Diagramas em Mermaid:** Priorize diagramas estruturais e comportamentais em sintaxe Mermaid editável.
- **Rastreabilidade e Consistência:** Mantenha alinhamento rigoroso entre Documento de Visão, PRD, Histórias de Usuário, Modelos, Arquitetura e Código.

---

## 5. Como Iniciar um Novo Projeto
Ao iniciar um novo projeto acadêmico sob o YP-Agentic:
1. **Copiar Templates:** Copie os arquivos da pasta `templates/` para a pasta de documentação do projeto-alvo.
2. **Aplicar Prompts:** Use os prompts correspondentes em `prompts/` como entrada e instrução para estruturar cada artefato incrementalmente (iniciando pela Visão, seguindo para o PRD e depois User Stories).
3. **Seguir o Fluxo:** Consulte [`processo/fluxo.md`](processo/fluxo.md), [`processo/glossario.md`](processo/glossario.md) e [`processo/mapa-posse.md`](processo/mapa-posse.md) para executar as fases, marcos e iterações recomendadas.

---

## 6. Como Revisar e Corrigir Documentos Existentes
1. Analise o documento existente em relação ao seu respectivo template em `templates/` e critérios do processo em `processo/artefatos.md`, `processo/glossario.md` e `processo/mapa-posse.md`.
2. Verifique se há inconsistências, campos faltantes, informações fora do padrão ou duplicação de conteúdo entre documentos.
3. Não reescreva decisões tomadas pela equipe humana; apenas aponte lacunas e realize ajustes estruturais preservando o conteúdo existente.
4. Destaque pontos que necessitem de validação humana com `[A definir]`.

---

## 7. Como Registrar Alterações no Processo
- Qualquer ajuste nas regras, papéis, fluxos ou templates do processo deve ser registrado no arquivo [`processo/historico.md`](processo/historico.md), contendo data, autor/agente, versão e descrição da modificação.