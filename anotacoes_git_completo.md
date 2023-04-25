# Anotações GIT

## .gitignore

arquivo.sql -> adicionar um arquivo no gitignore faz com que o arquivo não entre no versionamento
*.py -> ignora todos os arquivos com extensão .py
**diretorio -> ignora todo o diretório

## Branchs

Um branch é uma ramificação do projeto. A branch master é o ramo principal do projeto.
Cada branch é um galho da branch principal (master) e cópia da branch principal a partir de determinado commit.
Normalmente são criados novos branchs quando queremos testar uma funcionalidade, mas não queremos mexer no branch principal.

## Pull Requests - Workflow fork

- Vá até o repositório escolhido e crie um fork dele na sua conta github;
- Faça um clone desse fork, faça suas modificações, commite e push para o repositório remoto;
- Vá até o repositório com fork e crie um Pull Request.

## Pull Requests - Workflow dono do repositório

- Teste o código do pull request em uma branch separada para checar se há bugs ou erros;
- Utilize o comando git fetch origin pull/codigo_do_pull_request/head:nome_da_branch_a_ser_criada para criar uma branch para testes;
- Após todos os testes realizados, é possível aceitar o pull request e assim é feito um merge.

## Principais comandos

`git init` - inicia um repositório no projeto

`git status` - mostra o status do git (qual branch está, se há commits a fazer)

`git config user.name 'nome'` - configurar o nome do usuário que utilizará o repositório

`git config user.email 'email'` - configurar o email do usuário que utilizará o repositório

`git config --global user.email 'email'` - flag --global para adicionar em todos os projetos

`git add nome_do_arquivo` - adiciona o arquivo no controle do git (para ser commitado)

`git add .` - adiciona todos os arquivos do projeto para ser commitado

`git commit -m 'nome do commit'` - commita as alterações feitas (salva no repositório)

`git log` - ver todo o histórico de commits (esse comando tem vários parâmetros, pesquisar caso necessário)

`git log -5` - mostra os 5 últimos commits

`git log --oneline` - mostra os commits em uma linha

`git checkout id_do_commit` - volta no tempo para o id de commit selecionado

`git checkout master` - volta para a master (commit mais atual)

`git checkout nome_do_arquivo` - caso tenha feito alguma alteração no arquivo e queira voltar pro estado anterior, utilizo esse comando

`git mv nome_do_arquivo/diretório novo_nome` - renomeia o arquivo/diretório do projeto (forma melhor que renomear pela interface gráfica)

`git rm nome_do_arquivo/diretório` - deleta o arquivo/diretório do projeto (forma melhor que deletar pela interface gráfica)

`git diff -- stagged` - compara o que está commitado com a alteração a ser feita

`git diff codigo_do_commit` - compara o projeto atual com o commit selecionado

`git diff codigo_do_commit..codigo_do_commit` - compara um commit com o outro

`git commit --amend -m "texto do commit"` - amend faz alteração no último commit, caso tenha esquecido de adicionar algo ou errado alguma descrição

`git restore --staged nome_do_arquivo` - tira o arquivo da preparação para o commit

`git reset HEAD --hard` - volta todos os arquivos para o status que estavam no último commit

`git reset HEAD^ --hard` - volta o projeto para o último commit (caso eu tenha feito um commit com alguma alteração incorreta e queira voltar pro anterior)

`git reset HEAD~1` - apaga a partir do commit selecionado (1 é o ultimo, 2 é o penúltimo, etc - se eu colocar 10, vai apagar do 10 até o último commit feito)

`git branch` - consulta as branchs do projeto

`git branch nome_da_branch` - cria uma branch

`git branch -b nome_da_branch` - cria uma branch e já entra na branch

`git checkout nome_da_branch` - muda para a branch especificada

`git branch -d nome_da_branch` - deleta a branch especificada

`git merge nome_da_branch` - junta a branch especificada com a master

`git rebase nome_da_branch` - junta a branch especificada com a master a partir do ponto de criação da branch

`git clone caminho_do_repositorio` - clona um repositório para o projeto remoto

`git push` - envia os commits para o repositório remoto (exporta commits para branches remotos)

`git fetch` - baixa as atualizações do repositório remoto mas não aplica elas no repositório local (necessário fazer merge caso queira os arquivos no repositório)

`git pull` - baixa as atualizações do repositório remoto e organiza os arquivos aplicando os commits (baixa e faz o merge)

`git tag nome_da_tag` - cria uma tag no repositório (posso criar uma tag v1.0 por exemplo, e enviar os arquivos dela com git push v1.0 para a branch principal)

`git tag` - mostra as tags do projeto

`git init --bare` - inicia o repositório bare (define um repositório como repositório central - como se fosse hospedado no Github, por exemplo)

`git remote -v` - mostra quais repositórios Github (remoto) estão registrados no projeto

`git checkout -- .` - caso eu tenha alterado vários arquivos e queira voltar para o status antes das modificações, utilizo esse comando

`git checkout -- nome_do_arquivo` - volta somente o arquivo selecionado para o status anterior

`git checkout HEAD -- .` - voltar arquivos que foram adicionados para o status antes das modificações

`git checkout HEAD -- nome_do_arquivo` - volta somente o arquivo selecionado que foi adicionado para o status anterior

`git revert id_do_commit` - faz um commit desfazendo o que foi feito no commit selecionado
