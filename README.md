# hello-world

## Configurando token HTTPS

no seu perfil no github, va em:
> settings

	> developer settings 
		
		> personal access tokens 
		
			> tokens (classic) 
		
				> generate new token (classic)

### comandos para configurar token na maquina local

_git config --global credentials.helper store_

_git config --global --show-origin credential.helper_


## Configurando chave SSH

no seu perfil no github, va em:
> settings 

	> SSH and GPG keys

		> New SSH key

### comandos para configurar chave ssh na maquina local
verificar se ja existem chaves ssh: 

_ls -al ~/.ssh_

gerar nova chave ssh:

_ssh-keygen -t ed25519 -C "youremail@example.com"_

_[Press enter]_

_[Type a passphrase]_

_[Type passphrase again]_

adicionar chave ssh local ao ssh-agent:

_eval "$(ssh-agent -s)"_

_ssh-add ~/.ssh/id_ed25519_
