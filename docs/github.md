# Git e GitHub

Fluxo de trabalho usando git com repositório local e remoto.

![Fluxo de Trabalho do Git](git-workflow.png)

## Instalação do Git

No linux faça:

```commandLine
sudo apt install git
```

Ou baixe de https://git-scm.com/downloads.

## Resumo de Comandos

### Configuração do Git

```commandLine
git config --global user.name "John Smith"

git config --global user.email "example@email.com"
```

### Comandos Git

`git init`: Inicializa um repositório local.

`git add`: adiciona um arquivo ou modificação no staging.

`git commit`: envia a modificação para o repositório local.

`git status`: apreseta a situação do repositório.

`git log`: apresenta a lista de commits.

`git diff`: compara os arquivos na pasta de trabalho (workspace) com o staging e com o repositório.

### Comandos do Terminal

`ls` : lista os diretórios (-al: lista ocultos)
`mkdir`: criar um diretório
`clear`: limpar tela
`cd`: entra em diretórios


---

## Boas Práticas de Git para Tarefas Acadêmicas (GitFlow Simplificado)

Em disciplinas que utilizam o GitHub para submissão de tarefas individuais e em equipe, o fluxo de desenvolvimento adota um modelo baseado em **Forks**, **Branches dedicadas**, **Commits Semânticos** e **Pull Requests**.

### 1. Fluxo de Trabalho (Workflow) Padronizado

O ciclo de vida padrão de entrega de uma tarefa compreende:
1. **Fork do repositório original:** O discente cria uma cópia do repositório da disciplina na sua própria conta do GitHub.
2. **Clone local:** Clona o fork para o seu ambiente local (`git clone https://github.com/<username>/<repo>.git`).
3. **Configuração do upstream:** Configura o repositório original como remote de referência para atualizações contínuas:
   ```bash
   git remote add upstream https://github.com/<org-ou-professor>/<repo>.git
   ```
4. **Criação de Issue:** Abre a issue referente à tarefa no repositório original para obter o identificador (`#<id_issue>`).
5. **Criação da Branch:** Cria uma branch limpa e específica para a tarefa a partir da branch `main` atualizada.
6. **Commits pequenos e atômicos:** Desenvolve a solução realizando commits pequenos que identificam a issue na mensagem (`#<id_issue>`).
7. **Push e Pull Request:** Envia a branch para o seu fork remoto e abre o Pull Request da sua feature branch para a branch `main` do repositório original.

---

### 2. Regra de Ouro: Criação e Isolamento de Branches

Ao iniciar uma nova tarefa (por exemplo, Tarefa 02) enquanto uma tarefa anterior (Tarefa 01) ainda aguarda revisão e merge no repositório principal:

> **Atenção Mandatória:** **Toda nova branch deve ser criada a partir da branch `main` atualizada do seu fork**, e **NUNCA** a partir da branch de uma tarefa anterior.

#### Passo a passo para criar a branch da nova tarefa:
```bash
# 1. Retorne para a branch principal
git checkout main

# 2. Sincronize sua main com o repositório original (upstream)
git pull upstream main

# 3. Atualize a branch main do seu fork no GitHub
git push origin main

# 4. Crie e mude para a branch dedicada da nova tarefa
git checkout -b tarefa02/<username>
```

#### Por que NÃO ramificar em cascata?
Se você criar a branch da `tarefa02` estando na branch `tarefa01` (que ainda não foi mergeada na `main` do repositório original):
- O Pull Request da Tarefa 02 herdará **todos os commits e arquivos da Tarefa 01**;
- O histórico de commits ficará misturado e desorganizado;
- Criar-se-á uma dependência artificial entre Pull Requests que deveriam ser independentes;
- A conferência automatizada de commits identificará commits que não pertencem à tarefa em avaliação.

Como as tarefas são desenvolvidas em arquivos separados (ex.: `tarefa01.md`, `tarefa02.md`), cada tarefa é uma unidade independente de trabalho e deve ter seu ciclo de vida totalmente isolado.
