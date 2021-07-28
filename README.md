# github-course
COMANDO ÚTEIS
Inicialização e Configuração:
- git init - inicializa um repositório.
- git config - configurações do repositório. 
	- --global - define configurações para todos os usuários logados na máquina.
		- user.name [Nome Desejado] - define o nome do usuário.
		- user.email [Email Desejado] - define o e-mail do usuário.
	- --get - recupera uma determinada configuração.
	- --list - lista todas as configurações possíveis.

Logs:
- git log - Exibe o histórico de commits.
- git shortlog - Exibe o histórico de commits com informações reduzidas (contribuidores e comentários de cada commit).
	- --s - resume os dados em quantitativos;
	- --[campo desejado] e valor desejado (e.g. --author "Pedro") - filtro de dados.
- git --graph - mostra histórico visual de commits.
- git show [hash do commit] - mostra os dados de um commit especifico.

Controle de Arquivos:
- git status - exibe status dos arquivos contidos no repositório.
![git status](https://user-images.githubusercontent.com/11855011/127254608-f9bb30b6-d0db-4d9c-904f-f6e6a1e4ded3.png)

- git add [file ou . (para todos os arquivos)] - faz com que os arquivos apontados passem a ser gerenciados pelo git (status Untracked -> Unmodified).
- git diff - mostra as diferenças entre arquivos da branch e locais.
	--name-only - só nome dos arquivos modificados.
- git commit - grava as modificações na branch.
	- --m "[comentário]" - adiciona comentário ao commit.
	- --a - comita diretamente os arquivos modificados tbm, sem precisar dar um git add novamente nesses arquivos.
- git checkout - descarta as diff do arquivo antes dele estar staged.
- git restore - retorna de staged ao estado modified.
- git rm - retorna de staged ao estado unstaged.
- git reset
	- --HEAD [arquivo] - retorna ao arquivo original do repo, descartando o arquivo local.
	- --soft [hash] - indica para o commit que quer se voltar, com os arquivos ja em estado staged
	- --mixed -  indica para o commit que quer se voltar, com os arquivos ja em estado modified
	- --hard -  indica para o commit que quer se voltar sem arquivos adicionias

Gerar SSH KEY
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

