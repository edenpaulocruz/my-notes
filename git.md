# Git

## Instalação

```
# add-apt-repository ppa:git-core/ppa 
# apt update; apt install git
```

## Comandos

- criando um novo repositório local

  `git init`

- adicionando um repositório remoto

  `git remote add origin <servidor>`

- visualizando os repositórios remotos

  `git remote -v`

- clonando um repositório

  - local

    `git clone /caminho/para/o/repositório`

  - remoto

    `git clone usuário@servidor:/caminho/para/o/repositório`

- adicionando arquivo(s) para commitar

  - arquivo(s) específicos

    `git add <arqivo>`

  - todos os arquivos alterados

    `git add *`

    `git add .`

- fazendo um commit

  - com mensagem direta no comando

    `git commit -m 'comentários das alterações'`

  - adicionando arquivos e fazendo o commit

    `git commit -am 'comentários das alterações'`

  - abrindo editor para escrever a mensagem

    `git commit`

- enviando alterações

  `git push origin <branch>;`

- criando um novo branch

  `git branch <nova_branch>`

  - e entrando na nova branch

    `git checkout -b <nova_branch>`

- trocando de branch

  `git checkout <branch>`

  `git switch <branch>`

- visualizando todos os branchs

  `git branch`

- removendo um branch

  `git branch -d <branch>`

- atualizando o branch ativo

  `git pull`

- mesclando um branch com o branch ativo

  `git merge <branch>`

- verificando diferenças entre branchs

  `git diff <branch origem> <branch destino>`

- rotulando um branch

  `git tag 1.0.0 1b2e1d63ff`

  *1.0.0* é o rótulo e *1b2e1d63ff* representa os 10 primeiros caracteres do id do commit.

- visualizando o histórico

  `git log`

- sobrescrevendo alerações locais

  `git checkout -- <arquivo>`

  Isto substitui as alterações na sua árvore de trabalho com o conteúdo mais recente no HEAD. Alterações já adicionadas ao index, bem como novos arquivos serão mantidos.

  `git checkout <id do commit> -- <arquivo>`

  Isto substitui as alterações na sua árvore de trabalho com o conteúdo do commit especificado. 

  `git fetch origin`

  `git reset --hard origin/<branch principal>`

  Remove todas as alterações e commits locais, recupera o histórico mais recente do servidor e aponta para o branch principal local.

- usando saídas do git coloridas

  `git config color.ui true`

- exibindo log em apenas uma linha por commit

  `git config format.pretty oneline`

- fazendo inclusões interativas

  `git add -i`

- visualizando as alterações de um commit

  - último commit

    `git show`

  - commit específico

    `git show <id do commit>`

- armazenando as credenciais de acesso

  `git config credential.helper store`

  Isso irá reduzir o número de vezes em que irá digitar o username ou senha.

- alterando a mensagem do último commit

  `git commit -m 'Nova mensagem' --ammend