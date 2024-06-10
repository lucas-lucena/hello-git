# hello-world

## Configurando token HTTPS

No seu perfil no github, va em:

\> settings > developer settings > personal access tokens > tokens (classic) > generate >

### comandos para configurar token na maquina local

```
git config --global credentials.helper store

git config --global --show-origin credential.helper
```

## Configurando chave SSH

No seu perfil no github, va em:

\> settings > SSH and GPG keys > New SSH key

### comandos para configurar chave ssh na maquina local

Verificar se ja existem chaves ssh:

```
ls -al ~/.ssh
```

Gerar nova chave ssh:

```
ssh-keygen -t ed25519 -C "youremail@example.com"

[Press enter]

[Type a passphrase]

[Type passphrase again]
```

Adicionar chave ssh local ao ssh-agent:

```
eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_ed25519
```

## Criando e Clonando repositorios

Criar repositorio local:

```
git init
```

Para clonar um repositorio:

```
git clone "url do repositorio"
```

Caso queria mudar o nome do workspace local:

```
git clone "url do repositorio" "novo nome local"
```

Verificar se o repositorio local esta vinculado a um repositorio remoto:

```
git remote -v
```

Conectar um repositorio remoto ao repositorio local:

```
git remote add origin "url do repositorio remoto"
```

Para ver mais configurações do repositorio local

```
cd .git

cat config
```

## Revertendo Alterações

Caso queira apagar alguma pasta:

```
rm -rf "nome da pasta"
```

Verificar se existem alterações no repositorio local:

```
git status
```

Verificar histórico de alterações

```
git log
```

Vizualizar histórico de commits

```
git reflog
```

Retornar algum arquivo ao ultimo estado dele:

```
git restore "nome do arquivo"
```

Alterar ultimo comit pelo editor de texto:

```
git commit --amend
```

Alterar apenas o comentário do ultimo commit:

```
git commit --amend -m "comentário"
```

Remover arquivos da area de preparação

```
git restore --staged Nome_do_arquivo
```

### Git resets

Temos 3 opções de git reset, sendo elas _"soft"_, _"mixed"_ ou _"hard"_

Restaurando o commit a um estado anterior já adincionando os arquivos a area de preparação

```
git reset --soft ID_do_commit
```

Função padrão do git reset, retorna a um estado anterior sem adicionar arquivos a area de preparação

```
git reset --mixed ID_do_commit

ou

git reset ID_do_commit
```

Retorna a um estado anterior apagando todas as modificações feitas posteriormente

```
git reset --hard ID_do_commit
```
