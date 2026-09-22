# Mapa de Posse da Informação — YP-Agentic

**Repositório:** yp-agentic
**Versão:** 1.2
**Data:** DD/MM/AAAA

## 1. Princípio

Cada informação tem UM documento dono (fonte única). Os demais documentos devem apenas LINKAR para o dono, sem repetir o conteúdo. Repetição só é aceita no "extremamente necessário" (ex.: uma frase de contexto), e sempre acompanhada do link para a fonte.

## 2. Documentos do processo (por fase)

| Fase | Documento | Arquivo sugerido |
|---|---|---|
| F1 — Conversa com o Cliente | Documento de Visão | templates/doc-visao.md |
| F1 | PRD | templates/prd.md |
| F1 | Lista de User Stories | templates/doc-userstories.md |
| F1 | Documento de Modelos | templates/doc-modelos.md |
| F1 | Projeto Arquitetural | templates/doc-arquitetura.md |
| F2 — Inicialização | Termo de Abertura de Projeto | templates/termo-abertura.md |
| F2 | Documento de Agentes | templates/doc-agentes.md |
| F3 — Planejamento de Releases | Plano de Release | templates/plano-release.md |
| F3 | Plano Geral de Testes | templates/plano-geral-testes.md |
| F3 | Especificação de User Stories | templates/esp-userstories.md |
| F4 — Planejamento de Iteração | Plano de Iteração | templates/plano-iteracao.md |
| F4 | Plano de Teste da Iteração | templates/plano-teste-iteracao.md |
| F5 — Implementação | Atas de Reunião | templates/atas-reuniao.md |
| F6 — Implantação | Relatório de Testes | templates/relatorio-testes.md |
| F8 — Finalização | Termo de Encerramento de Projeto | templates/termo-encerramento.md |
| Transversal | Design System | templates/DESIGN.md |
| Transversal | Glossário | processo/glossario.md |
| Transversal | AGENTS.md | AGENTS.md |

## 3. Mapa de posse — Informação → Dono → Quem linka

| Informação | Documento dono (fonte) | Documentos que linkam (não repetem) |
|---|---|---|
| Propósito, problema, oportunidade, solução | Documento de Visão (§1–2) | PRD (§1, §3), Termo de Abertura (§3), Plano Geral de Testes (§1) |
| Stakeholders | Documento de Visão (§3.1) | Termo de Abertura (§1) |
| Perfis de usuário | Documento de Visão (§3.2) | PRD (§2 — personas derivam daqui) |
| Requisitos Funcionais (alto nível) | Documento de Visão (§4.1) | PRD (§4 — vira features priorizadas) |
| Requisitos Não Funcionais | Documento de Visão (§4.2) | Projeto Arquitetural (§5), Plano Geral de Testes (§3), PRD |
| Restrições do projeto | Documento de Visão (§5) | Termo de Abertura (§4), Projeto Arquitetural (§3) |
| Riscos do projeto | Documento de Visão (§6) | Termo de Abertura (§6) |
| Critérios de sucesso | Documento de Visão (§7) | PRD (§5), Termo de Abertura (§7), Plano de Release (§5), Termo de Encerramento (§3) |
| Personas | PRD (§2) | Lista de US, Especificação de US (§2) |
| Funcionalidades priorizadas (P0/P1/P2) | PRD (§4) | Lista de US, Plano de Release (§2), Termo de Abertura (§4) |
| Escopo in/out | PRD (§6) | Plano de Release (§2), Termo de Abertura (§4) |
| Roadmap de releases | PRD (§7) | Plano de Release (§1, §4), Termo de Abertura (§5) |
| Regras de negócio | Especificação de US (§4) | Plano de Teste da Iteração (§3) |
| User Stories, RFs internos, prioridade, tamanho | Lista de User Stories | Plano de Release (§3), Plano de Iteração (§2), Plano de Teste da Iteração (§2) |
| Critérios de aceitação (alto nível) | Lista de User Stories (§3) | Especificação de US (§8 — detalha) |
| Critérios de aceitação (Gherkin) | Especificação de US (§8) | Plano de Teste da Iteração (§3) |
| Diagramas de classe/sequência da US | Especificação de US (§6) | — |
| Protótipo/componentes de tela | Especificação de US (§7) | — (linka DESIGN.md) |
| Entidades, atributos, relacionamentos | Documento de Modelos (§2–3) | Especificação de US (§6), Projeto Arquitetural |
| Dicionário de dados | Documento de Modelos (§4) | — |
| Regras de integridade | Documento de Modelos (§5) | — |
| Contratos de API | Documento de Modelos (§6) ou Especificação de US | — |
| Arquitetura (HLD, componentes, tecnologias) | Projeto Arquitetural (§1–3) | Documento de Agentes (§2), Plano Geral de Testes, DESIGN.md |
| Mecanismos arquiteturais | Projeto Arquitetural (§4) | — |
| Decisões de arquitetura (ADR) | Projeto Arquitetural (§7) | — |
| Equipe e papéis YP-Agentic | Termo de Abertura (§2) | Documento de Agentes (§2), Plano de Iteração (§1), Atas de Reunião (§1) |
| Cronograma macro | Termo de Abertura (§5) | Plano de Release (§4) |
| Autorização/assinaturas | Termo de Abertura (§8) | Termo de Encerramento (§8 — encerra) |
| Agentes e ferramentas de IA | Documento de Agentes (§2) | — |
| Prompts-base | Documento de Agentes (§4) | AGENTS.md (versiona) |
| Limites dos agentes | Documento de Agentes (§5) | AGENTS.md |
| Critérios de qualidade da IA | Documento de Agentes (§7) | — |
| US por release | Plano de Release (§3) | Plano de Iteração (§2) |
| Iterações da release | Plano de Release (§4) | Plano de Iteração |
| Critérios de aceitação da release | Plano de Release (§5) | Termo de Encerramento (§4) |
| Riscos da release | Plano de Release (§7) | — |
| Objetivos da iteração | Plano de Iteração (§1) | Plano de Teste da Iteração (§1), Atas de Reunião (§3) |
| Tarefas e responsáveis da iteração | Plano de Iteração (§3) | Atas de Reunião (§3 — status) |
| Cronograma da iteração | Plano de Iteração (§4) | Plano de Teste da Iteração (§5) |
| Riscos da iteração | Plano de Iteração (§5) | — |
| Estratégia de testes (níveis, ferramentas) | Plano Geral de Testes (§4–5) | Plano de Teste da Iteração |
| Estratégia por RNF | Plano Geral de Testes (§3) | — |
| Casos de teste da iteração (IDs CT) | Plano de Teste da Iteração (§3) | Relatório de Testes (§2) |
| Critérios de entrada/saída da iteração | Plano de Teste da Iteração (§4) | Relatório de Testes (§4) |
| Riscos de teste da iteração | Plano de Teste da Iteração (§6) | — |
| Participantes, pauta, decisões e ações das reuniões | Atas de Reunião (§1–5) | — |
| Status das tarefas nas reuniões | Atas de Reunião (§3) | — (linka Plano de Iteração) |
| Pendências entre reuniões | Atas de Reunião (§6) | — |
| Resultados de execução | Relatório de Testes (§2) | Termo de Encerramento (§5 — consolida) |
| Bugs e providências | Relatório de Testes (§3) | — |
| Resultado final entregue | Termo de Encerramento (§2) | — |
| Lições aprendidas | Termo de Encerramento (§6) | — |
| Pendências pós-projeto | Termo de Encerramento (§7) | — |
| Design System (cores, tipografia, componentes) | DESIGN.md | Especificação de US (§7), Projeto Arquitetural |
| Termos e definições | Glossário | Todos os documentos |
| Regras do agente no repositório | AGENTS.md | — |

## 4. Direções de link por documento

### Documento de Visão
- É dono de: problema, oportunidade, stakeholders, perfis, RFs/RNFs, restrições, riscos, critérios de sucesso.
- Linka para: PRD, Lista de US, Documento de Modelos, Projeto Arquitetural, Plano Geral de Testes (referências).

### PRD
- É dono de: personas, funcionalidades priorizadas, KPIs, escopo, roadmap, regras de negócio de produto.
- Linka para: Documento de Visão (problema, RNFs, critérios), Lista de US, Documento de Modelos, Projeto Arquitetural.

### Lista de User Stories
- É dono de: US, RFs internos, prioridade, tamanho, dependências, critérios de aceitação em alto nível.
- Linka para: PRD (funcionalidades), Especificação de US (detalhe).

### Especificação de User Stories
- É dono de: regras de negócio, fluxos, diagramas da US, protótipo, critérios de aceitação Gherkin.
- Linka para: Lista de US, PRD, Documento de Modelos, DESIGN.md.

### Documento de Modelos
- É dono de: entidades, atributos, relacionamentos, dicionário de dados, integridade, contratos de API.
- Linka para: Documento de Visão, PRD, Especificação de US.

### Projeto Arquitetural
- É dono de: arquitetura, componentes, tecnologias, mecanismos, ADRs.
- Linka para: Documento de Visão (RNFs), Documento de Modelos, DESIGN.md.

### Termo de Abertura
- É dono de: equipe/papéis, cronograma macro, autorização.
- Linka para: Documento de Visão (objetivos, riscos, critérios), PRD (escopo), Plano de Release (cronograma), Documento de Agentes.

### Documento de Agentes
- É dono de: agentes, papéis de IA, prompts-base, limites, critérios de qualidade da IA.
- Linka para: Termo de Abertura (equipe), Projeto Arquitetural (tecnologias), AGENTS.md.

### Plano de Release
- É dono de: US por release, iterações da release, critérios de aceitação da release, riscos da release.
- Linka para: PRD (escopo/roadmap), Lista de US, Plano de Iteração.

### Plano Geral de Testes
- É dono de: estratégia de testes, níveis, ferramentas, estratégia por RNF.
- Linka para: Documento de Visão (RNFs), Lista de US, Especificação de US, Plano de Teste da Iteração.

### Plano de Iteração
- É dono de: objetivos da iteração, tarefas, responsáveis, cronograma, riscos da iteração.
- Linka para: Plano de Release, Lista de US, Especificação de US, Plano de Teste da Iteração.

### Plano de Teste da Iteração
- É dono de: casos de teste (IDs CT), critérios de entrada/saída, cronograma de teste, riscos de teste.
- Linka para: Plano de Iteração, Lista de US, Especificação de US (§8), Plano Geral de Testes.

### Atas de Reunião
- É dono de: participantes, pauta, status das tarefas, decisões, ações, pendências entre reuniões, data da próxima reunião.
- Linka para: Plano de Iteração (tarefas e cronograma), Atas anteriores.

### Relatório de Testes
- É dono de: resultados, resumo executivo, bugs e providências, conclusão.
- Linka para: Plano de Teste da Iteração (IDs CT), Especificação de US, Plano Geral de Testes.

### Termo de Encerramento
- É dono de: resumo do projeto, resultado dos critérios de sucesso, entregas realizadas, lições aprendidas, pendências pós-projeto, autorização de encerramento.
- Linka para: Termo de Abertura (identificação, autorização), Documento de Visão (critérios §7), Relatório de Testes (resultados), Plano de Release (entregas).

### DESIGN.md
- É dono de: identidade visual, componentes, padrões de tela.
- Linka para: Projeto Arquitetural (tecnologias de frontend).

### Glossário
- É dono de: termos e definições do processo e dos documentos.
- Linka para: nada (é referência passiva).

### AGENTS.md
- É dono de: regras de comportamento do agente no repositório.
- Linka para: templates/, prompts/, processo/glossario.md, processo/mapa-posse.md.

## 5. Regras de ouro

1. Se a informação já existe em outro documento, NÃO copie — linke.
2. Repetição permitida apenas no "extremamente necessário" (frase de contexto), sempre com link para a fonte.
3. Ao criar um documento, consulte o Glossário e o Mapa de Posse antes.
4. Ao alterar uma informação, altere no documento dono e verifique se os links continuam válidos.
5. IDs (US, RF, RNF, CT, Reunião) são referências estáveis — use-os nos links entre documentos, nunca renumere sem atualizar todos os vínculos.
6. O AGENTS.md do repositório deve referenciar este mapa como leitura obrigatória antes de gerar ou revisar qualquer documento.