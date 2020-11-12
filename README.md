# Informações úteis:
* Por que usar Command Line? Porque é uma ferramenta que utiliza todo o "poder" do git, algumas funções não podem ser utilizadas com programas gráficos do git. Também por questões de ajuda online, ao pesquisar em fóruns ou buscar informações online, e mais comum encontrar as informações por comandos.
* Por que usar Source Control? Porque e uma forma de backup, controle de versões, facilita de verificar quem fez certos ajustes, voltar modificações anteriores e experimentos isolados.
* Repositorios: Sao 3 repositórios locais e um remoto. Working directory - Repositorio local onde esta trabalhando. Staging Area - Repositório temporário que enfileira as versões para serem consolidados (commit). Commit - Repositorio do Git (historico). Remote repository - Repositorio com os tres anteriores internamente.








## Repositorio

* Criar um repositório é muito simples, segue o link com instruções para a criar um repositorio: https://guides.github.com/activities/hello-world/.

# Comandos


* pwd - print working directory - Verificar o pasta atual.
* mkdir - make directory - Criar pasta.
* cd - change directory - mudar pasta, ir para.
* ls - list - Listar arquivos dentro da pasta.
* ls -al - list all listing directory - Listar todos os arquivos dentro da pasta incluindo .files e .folders.
* rm - remove directory - remover pasta ou arquivo.
* rm -rf nome_do_arquivo - remover arquivo forçado. (r- apagar recursivamente, f- apagar forcado)


* git help log - Mostrar funcoes do Git (Q para sair).
* git config --global user.name "insira seu nome" - Utiliza para configurar seu usuario do git.
* git config --global user.email "insira seu email" - utiliza-se para configurar seu e-mail.
* git status - Verificar estados dos arquivos e diretórios. Verifica se há alguma alteração entre os repositórios, working directory, staging area, repository e remote.
* git clone insira_a_URL - Criar um arquivo a partir de um projeto no Github.
* git reset HEAD <nome_do_arquivo> - Retornar um arquivo do Staging para o working directory
* git ls-files - Listar todos os arquivos commitados.
* git fetch <repositorio_local> <repositorio_remoto> - Comando não destrutivo que atualiza as referencias entre Repositorio Remoto e Repositorio local.


* git add -A - "-A" é utilizado para adicionar todos os arquivos recursivamente e também para atualizar todos arquivos renomeados, movidos ou excluídos.
* git add -u - "-u" é utilizado para informar alterações no nome do arquivo e nao esta sendo criado um novo.




* .gitignore - Arquivo criado para ignorar arquivos indesejados.


## ==== Git Log (historico) =====

* git log - Verificar historico de Commits
* git log --oneline - Verificar historico de cada commit abreviado e em uma linha (recomendado)
* git log --abbrev-commit  - Verificar historico abreviado.
* git log --oneline --graph --decorate  -
* git log "codigo_abreviado"..."codigo_abreviado" - Verificar historico de X a Y.
* git log --since="dias_atras" - Verificar históricos de X dias atras.
* git log -- "nome_do_arquivo" -Verificar historico de um arquivo.
* git log --follow -- "arquivo_deletado" - 
* git show "codigo completo" - 


## ==== Git Diff ====

* git diff - Comparar alterações realizadas entre Working Area (local) com Staging Area (git add).
* git diff HEAD - Comparar alterações entre Working Area (local) com Repository (git commit).
* git diff --staged HEAD - Comparar alterações entre Staging Area (git add) com Repository (git commit).
* git diff -- <nome_do_arquivo> - Comparar alterações de apenas um arquivo.
* git diff <commit_ID_1> <commit_ID_2> - Comparar alteracoes entre Commits.
* git diff master origin/<nome_da_branch> - Comparar alteracoes local com a branch remota.


## ==== Git Branchs ====

* git branch -a - Listar todas as ramificacoes.
* git branch <nome_da_branch> - Criar uma nova ramificacao.
* git checkout <nome_da_branch> - Alterar para a ramificacao.
* git branch -m <nome_da_branch_atual> <novo_nome> - Alterar nome da ramificacao.
* git branch -d <nome_da_branch> - "-d" de deletar, remove ramificacao.

## ==== Git Merge ====

// Fast-forward merge - Apenas quando a branch não possui nenhuma alteracao apos ter sido ramificada.

* git merge <nome_da_branch> - Realizar a mescla da branch escolhida com a branch atual.
* git merge --no-ff - Realizar a mescla sem transpor o que foi feito na Master (git log --oneline --decorate --graph).


## ==== Git Rebase ====

// Funciona como se fosse rebobinar a branch. 

* git rebase <branch_a_rebobinar> - Rebobinar as alteracoes para antes das alteracoes na branch atual.
* git pull --rebase origin <branch_remota> - Rebobinar as informacoes adicionadas no GitHub (remote) com as informacoes locais.

## ==== Git Stash ====

// Utiliza para armazenar uma alteracao para trabalhar em outra mais importante.

* git stash - Por padrao, armazena as informacoes atuais realizadas para prosseguir com o diretorio "limpo" para trabalhar em outros dados.
* git stash apply - Retomar as alteracoes realizadas antes do git stash.
* git stash list - Listar todas as stash criadas.
* git stash drop - Deletar uma stash.
* git stash -u - "-u" permite inserir os arquivos não marcados pelo Git (novos arquivos, ainda nao realizados git add).
* git stash pop - Dois comandos em um, apply e drop. retoma as alteracoes que estao no Stash e apaga a Stash.
* git stash drop stash@{<numero_na_lista>} - Apagar uma stash especifica.
* git stash clear - Apagar todas as stashs disponiveis.
* git stash branch <nome_da_branch_> - Criar e alterar para branch e retomar os itens da Stash na branch. Tambem apaga a stash.

## ==== Ao iniciar o trabalho ====

* git pull // atualiza o código com base na branch do github.

* git checkout -b nome_da_branch // criar a branch nome_da_branch e trocar pra ela.

* git branch nome_da_branch // cria branch nova.
* git checkout nome_da_branch // troca pra branch.


## ==== Depois de fazer as alterações =====

* git add . // adicionar todas as modificações feitas à fila (staging area).

* git commit -m "Explica o que fez nesse commit" - preparar as alterações para serem enviadas ao github (commit).

* git commit -am // git add e git commit em um unico comando.

* git push origin nome_da_branch // enviar o código atual pro github.


* git commit -m "ch230 [Sammuel R] "ch230/feature/selecionar-interesses""

* git commit -m "ch208 [Sammuel R] Create initial folder structure" -m "Create initial folders to strucute the project"
> chCARD (clubhouse + card do story atual)
> [Nome Inicial]
> Tarefa no infinitivo começando com letra maiúscula
> Nome dos arquivos com letras maiúsculas quando precisar

* git pull // atualiza o código com base na branch do github

* git checkout -b nome_da_branch // criar a branch nome_da_branch e trocar pra ela

* git branch nome_da_branch // cria branch nova
* git checkout nome_da_branch // troca pra branch

* git push -u origin nome_da_branch // enviar o branch pro github


## ==== Depois de fazer as alterações =====

* git add . // adicionar todas as modificações feitas

* git commit -m "Explica o que fez nesse commit"

* git push // enviar o código atual pro github


## ==== Extras ====

* git rebase nome_da_branch // atualizar a origem da branch atual

* git status // mostra o status atual (algum arquivo modificado, adicionado ou excluído)

* git checkout . // remove todas as modificações feitas (SE PRECISAR)