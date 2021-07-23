# github-course
Comandos Úteis:
- git init - inicializa um repositório.

- git log - Exibe o histórico de commits.

- git shortlog - Exibe o histórico de commits com informações reduzidas (contribuidores e comentários de cada commit).
  - Parâmetros:
    - --s - resume os dados em quantitativos;
    - aplicação de filtros - adicionar --[campo desejado] e valor desejado (e.g. --author "Pedro").

- git --graph - mostra histórico visual de commits.

- git show [hash do commit] - mostra os dados de um commit especifico.

git add
git rm

git diff - mostra as diff.
	--name-only - só nome dos arquivos modificados.

git checkout - descarta as diff do arquivo antes dele estar staged.

git restore - retorna de staged ao estado modified.

git reset
	HEAD [arquivo] - retorna ao arquivo original do repo, descartando o local.
	--soft [hash] - indica para o commit que quer se voltar, com os arquivos ja em estado staged
	--mixed -  indica para o commit que quer se voltar, com os arquivos ja em estado modified
	--hard -  indica para o commit que quer se voltar sem arquivos adicionias

gerar ssh key
ssh-keygen -t rsa -b 4096 -C "ree.lopes@hotmail.com"

git remote add origin git@github.com:reelopes/github-course.git
conecta no repo do github

git remote -v mostra onde esta conectado

git push -u origin master
envia arquivos do repo para o github da branch master para a master do github (origin)

git pull origin master
baixa o repo para a branch especificada.

git clone git@github.com:viavarejo-banqi/banqi-testes-funcionais-app.git [destino]

comando more le arquivo.

git checkout -b testing
cria branch

git checkout testing
seleciona branch

git branch -D testing
deleta branch

git merge [branch]
faz o merge

git rebase [branch]
integra a branch no master mas não faz um commit extra, ou seja, não é possível rastrear mais se veio de outra branch

git stash e git stash apply
faz salvar os arquivos locais  escondendo os do commit e o apply os faz aparecer novamente.

git stash list mostra arquivos que estão no stash

git tag [nomeTag] - cria tag
git push origin master --tags comita as tags
git tag :[nome Tag] - apaga do repo remoto

