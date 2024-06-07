# hello-world

## Configurando token HTTPS

No seu perfil no github, va em:

\> settings > developer settings > personal access tokens > tokens (classic) > generate >

### comandos para configurar token na maquina local

```git config --global credentials.helper store

git config --global --show-origin credential.helper
```

## Configurando chave SSH

No seu perfil no github, va em:

\> settings > SSH and GPG keys > New SSH key

### comandos para configurar chave ssh na maquina local

Verificar se ja existem chaves ssh:

```ls -al ~/.ssh
```

Gerar nova chave ssh:

```ssh-keygen -t ed25519 -C "youremail@example.com"

[Press enter]

[Type a passphrase]

[Type passphrase again]
```

Adicionar chave ssh local ao ssh-agent:

```eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_ed25519
```

## Criando e Clonando repositorios

Criar repositorio local:

```git init
```

Para clonar um repositorio:

```git clone "url do repositorio"
```

Caso queria mudar o nome do workspace local:

```git clone "url do repositorio" "novo nome local"
```

Verificar se o repositorio local esta vinculado a um repositorio remoto:

```git remote -v
```

Conectar um repositorio remoto ao repositorio local:

```git remote add origin "url do repositorio remoto"
```

Para ver mais configurações do repositorio local

```cd .git

cat config
```
