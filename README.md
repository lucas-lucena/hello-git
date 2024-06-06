# hello-world

## Configurando token HTTPS

no seu perfil no github, va em:
> settings > developer settings > personal access tokens > tokens (classic) > generate new token (classic)

### comandos para configurar token na maquina local

	git config --global credentials.helper store

	git config --global --show-origin credential.helper


## Configurando chave SSH

no seu perfil no github, va em:
> settings > SSH and GPG keys > New SSH key

### comandos para configurar chave ssh na maquina local
verificar se ja existem chaves ssh: 

	ls -al ~/.ssh

gerar nova chave ssh:

	ssh-keygen -t ed25519 -C "youremail@example.com"

	[Press enter]

	[Type a passphrase]

	[Type passphrase again]

adicionar chave ssh local ao ssh-agent:

	eval "$(ssh-agent -s)"

	ssh-add ~/.ssh/id_ed25519

## Criando e Clonando repositorios

criar repositorio local:
	
	git init

para clonar um repositorio:
	
	git clone "url do repositorio"

caso queria mudar o nome do workspace local:
	
	git clone "url do repositorio" "novo nome local"

verificar se o repositorio local esta vinculado a um repositorio remoto:
	
	git remote -v

conectar um repositorio remoto ao repositorio local:
	
	git remote add origin "url do repositorio remoto"

para ver mais configurações do repositorio local
	cd .git
	cat config
