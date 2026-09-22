# YP-Agentic

Processo de desenvolvimento acadêmico **YP-Agentic**, uma atualização do **easYProcess (UFCG, 2003)** adaptada pelo **LABENS/UFRN** para disciplinas de Engenharia de Software (60h, um semestre) do curso de Sistemas de Informação do **CERES/UFRN**, sob coordenação do Prof. Taciano Silva, com foco em **desenvolvimento assistido por agentes de IA**.

O processo é explicitamente **iterativo e incremental**, combinando a qualidade técnica e testes contínuos do **XP (Extreme Programming)** com a gestão ágil de eventos e papéis do **Scrum**.

---

## 📁 Estrutura do Repositório

```text
yp-agentic/
├── README.md                 # Visão geral e guia de uso do repositório
├── AGENTS.md                 # Instruções de governança para agentes de IA
├── LICENSE                   # Licença Creative Commons CC BY-SA 4.0
├── docs/                     # Manuais e guias práticos de apoio
│   └── manual-uso-doc-visao.md # Manual de elicitação da Visão até o PRD
├── processo/                 # Definição formal do processo
│   ├── fluxo.md              # 8 fases formais, loops de feedback e fundamentos ágeis
│   ├── papeis.md             # Perfis Docente × Discente × Agentes de IA e Matriz RACI
│   ├── artefatos.md          # Catálogo e rastreabilidade dos artefatos
│   ├── glossario.md          # Glossário formal de termos e documentos
│   └── historico.md          # Histórico de alterações e evolução do processo
├── prompts/                  # Prompts de elicitação padronizados
│   ├── README.md             # Catálogo de prompts
│   ├── doc-visao.md          # Prompt para Documento de Visão
│   ├── prd.md                # Prompt para Product Requirements Document (PRD)
│   ├── doc-userstories.md    # Prompt para Lista de User Stories (Backlog)
│   ├── esp-userstories.md    # Prompt para Especificação de User Stories (BDD)
│   ├── plano-geral-testes.md       # Prompt para Plano Geral de Testes
│   ├── plano-release.md      # Prompt para Plano de Release
│   ├── plano-iteracao.md     # Prompt para Plano de Iteração
│   ├── plano-teste-iteracao.md # Prompt para Plano de Teste da Iteração
│   ├── atas-reuniao.md        # Prompt para Atas de Reunião
│   ├── relatorio-testes.md   # Prompt para Relatório de Testes
│   ├── termo-abertura.md     # Prompt para Termo de Abertura de Projeto (TAP)
│   ├── doc-modelos.md        # Prompt para Documento de Modelos
│   ├── doc-arquitetura.md    # Prompt para Projeto Arquitetural
│   ├── doc-agentes.md        # Prompt para Documento de Agentes de IA
│   └── termo-encerramento.md # Prompt para Termo de Encerramento (TEP)
│   └── DESIGN.md             # Prompt para Design System (Figma/CSS/imagens)
├── templates/                # Templates oficiais dos artefatos
│   ├── README.md             # Catálogo de templates
│   ├── doc-visao.md          # Template do Documento de Visão
│   ├── prd.md                # Template de PRD
│   ├── doc-userstories.md    # Template da Lista de User Stories
│   ├── esp-userstories.md    # Template de Especificação de User Stories
│   ├── plano-geral-testes.md       # Template do Plano Geral de Testes
│   ├── plano-release.md      # Template do Plano de Release
│   ├── plano-iteracao.md     # Template do Plano de Iteração
│   ├── plano-teste-iteracao.md # Template do Plano de Teste da Iteração
│   ├── atas-reuniao.md        # Template da Ata de Reunião
│   ├── relatorio-testes.md   # Template do Relatório de Testes
│   ├── termo-abertura.md     # Template do Termo de Abertura de Projeto (TAP)
│   ├── doc-modelos.md        # Template do Documento de Modelos
│   ├── doc-arquitetura.md    # Template do Projeto Arquitetural
│   ├── doc-agentes.md        # Template do Documento de Agentes de IA
│   └── termo-encerramento.md # Template do Termo de Encerramento de Projeto (TEP)
│   └── DESIGN.md             # Template do Design System (Transversal)
├── assets/                   # Recursos visuais e diagramas
│   ├── fluxo-yp-agentic.png  # Diagrama visual do fluxo
│   └── fluxo-yp-agentic.mmd  # Fonte Mermaid editável das 8 fases e loops
└── exemplos/                 # Exemplos práticos desenvolvidos na disciplina
    └── README.md
```

---

## 🚀 Fluxo de Uso

Para aplicar o **YP-Agentic** em seu projeto acadêmico:

1. **Copiar Templates:** Copie os arquivos da pasta `templates/` para a pasta de documentação do seu projeto.
2. **Aplicar Prompts:** Utilize os prompts correspondentes em `prompts/` no chat de IA (junto a eventuais notas prévias/brainstorm) para gerar os documentos no template oficial.
3. **Seguir o Fluxo:** Consulte [`processo/fluxo.md`](processo/fluxo.md) e [`processo/glossario.md`](processo/glossario.md) para executar as 8 fases, respeitando os loops iterativos de 2 semanas.
- Consulte o [Mapa de Posse da Informação](processo/mapa-posse.md) antes de gerar ou revisar qualquer documento — ele define o dono de cada informação e evita repetição entre documentos.
