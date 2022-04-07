# Anotações GIT

## Comandos

git init -> inicia um repositório no projeto
git status -> mostra o status do git (qual branch está, se há commits a fazer)
git config user.name 'nome' -> configurar o nome do usuário que utilizará o repositório
git config user.email 'email' -> configurar o email do usuário que utilizará o repositório
git config --global user.email 'email' -> flag --global para adicionar em todos os projetos
git add nome_do_arquivo -> adiciona o arquivo no controle do git (para ser commitado)
git add . -> adiciona todos os arquivos do projeto para ser commitado
git commit -m 'nome do commit' -> commita as alterações feitas (salva no repositório)
git log -> ver todo o histórico de commits (esse comando tem vários parâmetros, pesquisar caso necessário)
git log -5 -> mostra os 5 últimos commits
git log --oneline -> mostra os commits em uma linha
git checkout id_do_commit -> volta no tempo para o id de commit selecionado
git checkout master -> volta para a master (commit mais atual)
git checkout nome_do_arquivo -> caso tenha feito alguma alteração no arquivo e queira voltar pro estado anterior, utilizo esse comando
git mv nome_do_arquivo/diretório novo_nome -> renomeia o arquivo/diretório do projeto (forma melhor que renomear pela interface gráfica)
git rm nome_do_arquivo/diretório -> deleta o arquivo/diretório do projeto (forma melhor que deletar pela interface gráfica)
git diff -- stagged -> compara o que está commitado com a alteração a ser feita
git diff codigo_do_commit -> compara o projeto atual com o commit selecionado
git diff codigo_do_commit..codigo_do_commit -> compara um commit com o outro
git commit --amend -m "texto do commit" -> amend faz alteração no último commit, caso tenha esquecido de adicionar algo ou errado alguma descrição
git restore --staged nome_do_arquivo -> tira o arquivo da preparação para o commit
git reset HEAD --hard -> volta todos os arquivos para o status que estavam no último commit
git reset HEAD^ --hard -> volta o projeto para o último commit (caso eu tenha feito um commit com alguma alteração incorreta e queira voltar pro anterior)

# .gitignore

arquivo.sql -> adicionar um arquivo no gitignore faz com que o arquivo não entre no versionamento
*.py -> ignora todos os arquivos com extensão .py
**diretorio -> ignora todo o diretório



