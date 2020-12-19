# Conceitos báscios 
* Git workflow
  * Working directory// Aqui mostra os arquivos da pasta. Com git add seus arquivos ou folders vão para STAGE AREA.
  * Stage area// local onde o arquivo está preparado para ser commitado. 
  * Local repository // local para onde os arquivos commitados vão.

# git
- git init // inicia o repositório git no local.
- para verificar o folder que você está use no git bash o comando: PWD. 
- cd Documents/Folder_exemplo //permite você trabalhar no folder indicado.  

- mkdir nomeDiretorio // cria um diretório
- touch file.txt // cria arquivo dentro do diretório.
- vim file.txt // edita arquivo // dentro do vim ESC + :wq (write and quit) sai do editor e salva o que foi realizado.

## git add 

- git add <file> // adiciona o arquivo indicado. 
- git add . // adiciona todos os arquivos para serem commitados.
- git add *.md // adiciona somente os arquivos do tipo md, serve para outros como .html/.css/.js.

## git commit 
- git commit -m "Exemplo commit" // realiza um commit enviando o arquivo, ou arquivos, para a working tree.
- git commit -am "teste commit" // serve para pular a fase de add <file> e commita direto, só serve para arquivos já rastreados.
- git commit --amend -m "Aqui altera o ultimo commit feito" 


##  GIT LOG  
- git log // mostra todos os commits realizados.
- git log --oneline // mostra o HASH(código que indica determinado commit), além da mensagem de commit.

- git log -n 5 // mostra os 5 últimos commits. 
- git log --since=2020-10-01 // mostra os commits desde a data indicada. 
- git log --until=2020-10-01 // com until é possível ver os commits anteriores a data indicada.

- git log --author==Lucas //filtra o log pelo autor.

- git log --grep="initial" // traz tudo que contem o commit com "initial"  //exemplo1.
- git log --grep="bugfix" // traz tudo que contem o commit com "bugfix"  //exemplo2.

## FILES 
 
-git restore // restaura a ultima modificação feita no arquivo.

-git reset HEAD <nome_arquivo> // semelhante ao --staged.

-git show <hash> // mostra o que foi alterado no commit indicado pelo hash.
-git show <hash> -- src/view/* //mostra tudo o que foi realizado na pasta indicada.

## GIT DIFF  
-git diff // mostra tudo que foi alterado no working directory. 
-git diff --staged ||(ou) git diff --cached // mostra somente o que está no stage area.
-git diff --color-words // mostra somente as palavras que foram alteradas.

## GIT RM 
-git rm <arquivo> // deleta o arquivo jogando para stage area, em seguida é só usar o git add para excluir.
-git rm -r --cached . // tira tudo que tinha no cache

## GIT VM
- git vm exemplo exemplo_V2 // renomeia o arquivo exemplo para exemplo_V2.

* Quando arquivo já tiver na stage area, é possível mudá-lo de pasta. 
  * git mv arquivo_exemplo src/arquivo_exemplo // move arquivo_exemplo para pasta src. 

# GIT CHECKOUT

- git checkout <HASH> -- <nome_arquivo>  // retorna o arquivo excluido como new file.

## GIT CLEAN

- git clean -n // mostra o que será removido dos arquivos untrackeds.
- git clean -f // remove os arquivos permanentemente.

# GIT REVERT 

- git revert HEAD~2 // ele reverte o commit feito, trazendo novamente o arquivo. O ~2 se da pela ordem que o commit está atras do HEAD, como no exemplo indica o antepenultimo commit realizado.

- git revert 5868c3a // reverte o commit através do hash.

## GIT IGNORE 

* serve para ignorar determinado arquivo que não será utilizado. 
  ** vim .gitignore // coloque aqui o folder ou file que deseja ignorar.para sair aperte ESC e digite: :wq











