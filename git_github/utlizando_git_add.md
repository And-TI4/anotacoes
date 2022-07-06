## Utilizando o comando Git add

Usar o comando git add é muito simples e prático. O exemplo a seguir pode ser executado diretamente no [*Git Bash*](https://git-scm.com/downloads) ou em uma [IDE](https://blog.betrybe.com/tecnologia/ide/) de sua preferência:

- No projeto local, crie uma *branch*:

​	``git branch “Aqui vai o nome da branch”``

- Realize o checkout da nova branch:

​	``git checkout “Aqui vai o nome da branch”``

- Adicione um ou mais arquivos;

- Salve todas as alterações;

- Prepara as mudanças realizadas no diretório local:

​	``git add . “Aqui vai o nome da branch”``

1. Enviar as alterações locais para o servidor remoto:

​	``git commit “Aqui vai o nome da branch”``

Com esse exemplo, foi possível utilizar os principais comandos do Git. Nos próximos tópicos, vamos aprender outras opções utilizadas para esse comando.

## Desfazendo o Git add

Se você adicionou alguma mudança usando o comando git add e precisa desfazê-lo, utilize o comando git reset. Você pode usar esse comando nas seguintes opções:

​    Desfazer a inclusão de apenas um arquivo:

​	``git reset <nome_arquivo>``

​    Desfazer todas as mudanças que se encontram na *staging area*:

​	``git reset --mixed``

​    Reverter a mudança em bloco de arquivos novos e modificados:

​	``git reset -p <nome bloco mudança>``

​    Apagar todas as mudanças que se encontram na *staging area*:

​	``git reset --hard``

Desfazer o último [*pull*](https://git-scm.com/docs/git-pull/pt_BR) ou [*merge*](https://git-scm.com/docs/git-merge/pt_BR) realizado na branch atual:

​	``git reset --merge``

## Opções para usar junto

As opções para usar o comando git add são as seguintes:

​    Prepara todas as mudanças realizadas no diretório local:

​	``git add -A “Aqui vai uma mensagem”``

​    Prepara as mudanças realizadas nos arquivos novos e modificados:

​	``git add . “Aqui vai uma mensagem”``

​    Prepara as mudanças realizadas nos arquivos deletados e modificados:

​	``git add -u “Aqui vai uma mensagem”``

​    Prepara a mudança em bloco para os arquivos novos e modificados:

​	``git add -p “Aqui vai uma mensagem”``

## Git add interativo

Em cenários onde ocorrem muitas mudanças em arquivos do projeto, o comando permitirá escolher qual das opções de mudanças você deseja realizar de forma prática e rápida. Entenda como utilizar esse comando:

- Digite o comando: git add –i

- Serão exibidas oito opções para você escolher qual dessas você deseja realizar. Basta digitar um dos seguintes números:  

| 1. status | 2. update | 3. revert | 4. add untracked |
| --------- | --------- | --------- | ---------------- |
| 5. patch  | 6. diff   | 7. quit   | 8. help          |

Para entendermos melhor, vamos explicar cada uma dessas oito opções:

**Opção 1**: status

​    Lista os arquivos que foram modificados.

**Opção 2:** update

​    Adiciona somente as mudanças realizadas nos arquivos existentes no projeto.

**Opção 3**: revert

​    Reverte todas as mudanças que se encontram na *staging area.*

**Opção 4:** add untracked

​    Adiciona novos arquivos no projeto.

**Opção 5**: patch

​    Tem a mesma função que o comando git add -p. Prepara a mudança em bloco para os arquivos novos e modificados.

**Opção 6**: diff

​    Exibe detalhadamente as mudanças realizadas em cada um dos arquivos. É muito utilizado quando realizamos [*merge*](https://git-scm.com/docs/git-merge/pt_BR) entre [*branchs*](https://en.wikipedia.org/wiki/Branching_(version_control)).

**Opção 7**: quit

​    Esta opção finaliza toda a interação ocorrida no git add -i. 

Deve sempre ser acionado após você escolher uma das opções do ***Git add\* interativo**.

**Opção 8:** help

​      Exibe a lista de opções do comando.



Referencia:

https://blog.betrybe.com/git/git-add/#1