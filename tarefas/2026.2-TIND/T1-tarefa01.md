**Tarefa 01 - Git e GitHub com Markdown**

**Turma:** DCT2302 — 2026.2-TIND (Ensino Individualizado)
**Discente:** Artur Morais Candeia

Para responder às questões abaixo você deve utilizar um **fork** do repositório **eng-software-2** no github: [https://github.com/tacianosilva/eng-software-2](https://github.com/tacianosilva/eng-software-2).

Lembre-se que você trabalhará no seu fork e depois fará um pull request. Coloque seus arquivos de resposta no diretório com seu nome dentro de *tarefas/2026.2-TIND/\<username\>/*. Acesse o Guia Básico de Markdown: [https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown](https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown)

1. Cadastre uma tarefa (issue) para você com o título **“Tarefa 01 - Adicionado página Markdown de \<nomedodiscente\>”** no repositório da disciplina [**eng-software-2**](https://github.com/tacianosilva/eng-software-2).  
2. Faça o **fork** do repositório [**eng-software-2**](https://github.com/tacianosilva/eng-software-2).  
3. Faça **um clone do seu fork**:   
   *git clone https://github.com/\<username\>/eng-software-2.git*  
4. Atualize o seu fork:

   git remote add upstream https://github.com/tacianosilva/eng-software-2.git  
   git fetch upstream  
   git checkout main  
   git merge upstream/main  
   git push origin main  
      
5. Crie uma branch para sua tarefa antes de desenvolver. Algo como: git checkout -b tarefa01  
6. Crie um diretório com seu ***nome de usuário do github*** dentro do diretório *tarefas/2026.2-TIND*  
7. Crie um arquivo chamado **tarefa01.md** no seu diretório.  
8. Coloque na página **tarefa01.md** o título da página **“Tarefa 01 - Git e GitHub com Markdown”**, e abaixo do título coloque seu **nome, usuário github e e-mail.**  
9. Crie uma seção com as seguintes informações:  
   1. Título e descrição do seu projeto na disciplina. Tipo de sistema, objetivo e link para o repositório do projeto. Nesta modalidade individualizada, você é o único responsável pelo projeto (ex: [SIGAEX](https://github.com/labens-ufrn/sigaex-backend)).  
   2. Fale sobre a linguagem de programação que será utilizada no projeto. Qual o seu domínio e experiência com a linguagem. Consulte o repositório do projeto para confirmar a stack atual (ex: Python/Django no backend).  
   3. Fale um pouco sobre os frameworks que serão utilizados no projeto (ex: Django REST Framework, Vue 3 + Vite). Se não tiver definido, pesquise um framework e fale sobre ele.  
   4. Fale um pouco da IDE que você utiliza. Fale sobre as **ferramentas de debug** e de **controle de versão** que ela tem integrada.  
   5. Busque pelo menos um link de Tutorial para fazer um CRUD na tecnologia escolhida. Apresente o link e descreva em poucas palavras o conteúdo do tutorial.  
   6. Pesquise e fale um pouco sobre **branches** e **pull request** (também conhecido como *merge request*) usando git e github com o GitFlow.  
   7. Pesquise sobre **Versionamento Semântico** ([https://semver.org/lang/pt-BR/](https://semver.org/lang/pt-BR/)) e faça um pequeno resumo.  
   8. Pesquise sobre **Conventional Commits** (Convenções para Mensagens de Commits - link [https://www.conventionalcommits.org/pt-br/v1.0.0/](https://www.conventionalcommits.org/pt-br/v1.0.0/)). Faça um pequeno resumo.  
   9. Pesquise e fale sobre **Tags** no Git. Diferencie **tag anotada** de **tag leve** e mostre como criar (`git tag -a v1.0.0 -m "..."`), listar (`git tag -l`) e remover (`git tag -d <tag>`) tags. Explique a relação entre tags e **Versionamento Semântico**. **Prática:** crie uma tag anotada `v1.0.0` no commit final da sua entrega no seu fork.  
   10. Pesquise e fale sobre os principais comandos de **inspeção e colaboração** do Git, além de `commit`/`push`: `git log` (com `--oneline`, `--graph`, `--author`), `git show`, `git diff`, `git stash`, `git rebase`, `git cherry-pick` e `git blame`. Explique o propósito de cada um.  
   11. Pesquise **como automatizar o Versionamento Semântico** em projetos com a tecnologia do projeto. Investigue ferramentas como `python-semantic-release` (para o backend Django/Python) e `semantic-release`/`standard-version` (para o frontend Vue/Vite) e descreva como elas geram versões, tags e releases automaticamente a partir de **Conventional Commits** (ex: integração com GitHub Actions).  
10. Para cada item que você resolver da questão 9, faça um commit. Na mensagem de commit sempre acrescente o ID da issue criada na questão 1\. Ao final da atividade faça um pull para seu repositório. Depois crie um *pull request* do seu fork para o repositório da disciplina.

    Exemplo:  
    git commit -m "feat: adiciona descrição do projeto \#\<id\_issue\>"

Lembre-se das boas práticas do Git: 

1. **atualizar seu fork** a partir do original com **pull request** antes de começar a desenvolver  
2. faça **um clone do seu fork**: **git clone** https://github.com/*\<username\>*/eng-software-2.git  
3. fazer git pull para atualizar sua pasta de trabalho: **git pull**  
4. fazer commits pequenos e sempre colocar uma mensagem relevante e ao final da mensagem identifique a issue com **\#\<id\_issue\>**  
5. enviar suas modificações para seu repositório remoto: **git push**  
6. enviar um **pull request** com suas contribuições.