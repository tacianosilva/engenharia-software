# Tarefa 01 - Git e GitHub com Markdown

**Nome:** Artur Morais Candeia  
**Usuário GitHub:** ArturCandeia  
**E-mail:** artur.candeia.086@ufrn.edu.br

---

## 1. Projeto na Disciplina

**Título:** git-estudos  

**Descrição:** Sistema de administração de rotinas, tarefas e simulados 
para alunos interessados em se prepararem para o ENEM. A plataforma 
permite que os estudantes organizem seus estudos, acompanhem seu 
progresso e realizem simulados preparatórios.

**Equipe:** Artur Morais Candeia

**Repositório:** [ArturCandeia](https://github.com/ArturCandeia/git-estudos)

---

## 2. Linguagem de Programação e IDE

A linguagem usada sera Python e o framework sera Django

O motivo é que ja se tem mais experiencia em Python e Django foi escolhido
pela facilidade de uso e aprendizado e por ser uma ferramenta muito boa e
bem documentada

IDE:Sera usado do VScode e a versão do git 2.40

---

## 3. Tutorial de CRUD

https://www.youtube.com/watch?v=Q2tEqNfgIXM  
O tutorial ensina  como desenvolver uma API em Python, utilizando o Django framework mostrando passo a passo mostrando quais packs baixar e como organizar o ambiente.

---

## 4. Branches, Pull Request e GitFlow

### Branches

Branch (ramificação) é uma cópia independente do código principal que 
permite desenvolver funcionalidades, corrigir bugs ou fazer testes sem 
afetar o código principal. Cada branch tem seu próprio histórico de 
commits e pode ser mesclada ao código principal quando estiver pronta.

### Pull Request / Merge Request

Pull Request (PR) é uma solicitação para mesclar as alterações de uma 
branch para outra. É muito usado no trabalho em equipe, pois permite 
que outros membros revisem o código antes de ser integrado ao código 
principal. No GitHub é chamado de Pull Request e no GitLab de 
Merge Request.


### GitFlow

GitFlow é um modelo de organização de branches que define um fluxo 
de trabalho padronizado para equipes. Ele utiliza branches específicas 
para cada finalidade:`main`,`develop`,`feature/`,`release/`,`hotfix/`

---

## 5. Versionamento Semântico

Versionamento Semântico (SemVer) é um conjunto de regras que define como 
os números de versão de um software devem ser atribuídos e incrementados 
ao longo do tempo. Ele foi criado para resolver um problema muito comum no 
desenvolvimento de software chamado "inferno das dependências", que ocorre 
quando um sistema cresce e passa a depender de muitos pacotes externos, 
tornando difícil atualizar ou manter a compatibilidade entre eles.

O SemVer utiliza o formato **X.Y.Z**, onde cada número tem um significado 
específico:

- **MAJOR (Maior):** incrementado quando são feitas mudanças incompatíveis 
com versões anteriores. Ou seja, algo que funcionava antes pode deixar de 
funcionar após essa atualização.

- **MINOR (Menor):** incrementado quando novas funcionalidades são 
adicionadas mantendo a compatibilidade com versões anteriores. O sistema 
continua funcionando normalmente, apenas ganhou algo novo.

- **PATCH (Correção):** incrementado quando são feitas correções de bugs 
que não afetam a compatibilidade. É apenas uma correção de algo que estava 
errado.

---

## 6. Conventional Commits

Conventional Commits é uma convenção para padronizar as mensagens de 
commit, tornando o histórico do projeto mais legível e organizado, tanto 
para humanos quanto para ferramentas automatizadas. Ela se integra 
diretamente com o Versionamento Semântico, pois cada tipo de commit 
corresponde a um nível de versão.

## Tipos e o que significam

| `feat` | Adição de uma nova funcionalidade (relacionado ao MINOR do SemVer) |
| `fix` | Correção de um bug (relacionado ao PATCH do SemVer) |
| `docs` | Alterações apenas na documentação |
| `style` | Formatação, ponto e vírgula, espaços, sem mudança de lógica |
| `refactor` | Refatoração de código sem adicionar feature ou corrigir bug |
| `test` | Adição ou correção de testes |
| `build` | Mudanças no sistema de build ou dependências externas |
| `chore` | Tarefas gerais que não alteram o código fonte |
| `BREAKING CHANGE` | Mudança que quebra compatibilidade (relacionado ao MAJOR do SemVer) |

---

## 9.i Feedback

Feedback Feito

## 9.j Projeto

Projeto Cadastrado
