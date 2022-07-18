# Primeiros Passos com Git e GitHub

## Comandos Básicos
- Criar um diretório - **mkdir**
- Criar um arquivo - **touch nome**
- Criar um repositório Git - **git init**

## Sobre verificação de repositórios e arquivos

- Verificar o status (criações, exclusões, modificações) atual de arquivos - **git status**
- Adicionar uma modificação ao rastreamento (e consequentemente à staging área) - **git add nome do arquivo / -A (todos)**
- Fazer um commit **git commit -m** (*-m seguido de aspas para adicionar uma descrição/ -am para adicionar e commitar ao mesmo tempo)
- Verificar histórico de commit **git log** (--oneline para limitar as informações do commit)

## Sobre exclusão de arquivos, diretórios e repositórios

- Para excluir um arquivo usa-se **git rm nome** (--cached se o arquivo em questão estiver localizado na staging área)
- Para arquivos que nunca passaram pela staging area (não rastreados), usa-se somente **rm nome** (sem o percursor 'git')
- Para exclusão de diretórios vazios, usa-se **rmdir** ou **rm -d**
- Para a exclusão de diretórios que contém arquivos e/ou sub diretórios, usa-se **rm -r**
- Para a exclusão de arquivos com extensões especificas, usa-se **rm dir (*)** (sem os parenteses)
*Ao deletar um diretório com a pasta .git, temos a exclusão de um repositório git local.*

## Verificando diferenças/mudanças no conteúdo de arquivos

- Usa-se o comando **git diff** para verificar modificações feitas no working directory.
- Usa-se o comando **git diff --cached** ou **git diff --staged** para verificar modificações na staging area em relação ao último commit.
- Usa-se **git diff hash hash** para visualizar mudanças de um commit para o outro.
- Usa-se **git diff --name-only** para verificar somente nomes de arquivos modificados.
- Usa-se **git diff nome-do-arquivo** para verificar alterações isoladas.

## Métodos para apontar para um commit anterior (ou posterior)

- Usa-se **git reset --soft** para apontar para um commit desejado mantendo a staging area e o working directory atual. 
- Usa-se **git reset --mixed** para apontar para um commit desejado mantendo somente o working directory atual.
- Usa-se **git reset --hard** para apontar para um commit desejado. O modo *hard* faz com que o arquivo do working directory fique na forma do commit desejado de forma irreversível.

*Bônus:* Usa-se **git checkout HEAD -- nome-do-arquivo** para reverter modificações no working directory.