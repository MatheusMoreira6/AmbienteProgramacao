# Ambiente de Programação

## Chave SSH
#### Atual
    ssh-keygen -t ed25519 -C "your_email@example.com"
#### Legado
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    
## Atalhos no Terminal
#### Alias
    nano $HOME/.bashrc
#### Comandos
    alias atualizar='sudo apt update && sudo apt upgrade -y && sudo apt autoremove -y && sudo apt autoclean && sudo apt clean'
####
    alias dockerup='cd ~/Genesis/dev-environment/ && docker compose up -d'
#### 
    alias dockerdown='cd ~/Genesis/dev-environment/ && docker compose down'
####
    alias ecidade='cd ~/Genesis/equipe_dev/atualizacao-de-projetos/ && node atualizar.js'
####
    alias sshlocal='ssh genesis@192.168.100.18'
####
    alias producao='ssh gen@44.212.150.104'
####
	alias vpnup='hotspotshield connect BR && hotspotshield status'
####
	alias vpndown='hotspotshield disconnect && hotspotshield status'

## Aplicações e Dependências

#### Repositório PHP
	sudo add-apt-repository ppa:ondrej/php
####
	sudo add-apt-repository ppa:ondrej/apache2

#### PHP 7.4
	sudo apt update
####
	sudo apt install php7.4

#### PHP 8.2
	sudo apt update
####
	sudo apt install php8.2

#### PHP 8.3
	sudo apt update
####
	sudo apt install php8.3
	
##### Extensões PHP 7.4
    sudo apt install php7.4-cli php7.4-common php7.4-fpm php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath php7.4-pgsql php7.4-json php7.4-bz2 php7.4-intl
##### Extensões PHP 8.2
	sudo apt install php8.2-cli php8.2-common php8.2-fpm php8.2-mysql php8.2-zip php8.2-gd php8.2-mbstring php8.2-curl php8.2-xml php8.2-bcmath
##### Extensões PHP 8.3
	sudo apt install php8.3-cli php8.3-common php8.3-fpm php8.3-gd php8.3-bcmath php8.3-mysql php8.3-imap php8.3-ldap php8.3-xml php8.3-curl php8.3-mbstring php8.3-zip

#### Trocar a Versão do PHP
#### Para 7.4
	sudo update-alternatives --set php /usr/bin/php7.4
#### Para 8.2
	sudo update-alternatives --set php /usr/bin/php8.2

#### Docker
    sudo apt update
####
    sudo apt upgrade
####
    sudo apt install curl apt-transport-https ca-certificates software-properties-common
####
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
####
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
####
    sudo apt update
####
    apt-cache policy docker-ce
####
    sudo apt install docker-ce docker-ce-cli containerd.io
####
    sudo groupadd docker
####
    sudo usermod -aG docker $USER
####
    sudo systemctl status docker

#### Docker Compose
##### [Verificar a ultima versão](https://github.com/docker/compose/releases) 
    sudo curl -L "https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
####
    sudo chmod +x /usr/local/bin/docker-compose
####
    docker-compose --version

#### Compose
    sudo apt update
####
    sudo apt install php-cli unzip
####
    cd ~
####
    curl -sS https://getcomposer.org/installer -o composer-setup.php
####
    HASH=`curl -sS https://composer.github.io/installer.sig`
####
    php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
####
    sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
####
    composer self-update 2.4.4
####
    composer

#### NodeJS
    sudo snap install node --classic
    
#### SSH2
    npm install ssh2

#### PostgreSQL
    sudo apt install postgresql

#### PgAdmin
    curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /usr/share/keyrings/packages-pgadmin-org.gpg
####
    sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
####
    sudo apt install pgadmin4
####
    sudo apt install pgadmin4-desktop

#### Flutter
    sudo snap install flutter --classic

#### DBeaver
    sudo snap install dbeaver-ce

#### Postman
    sudo snap install postman

#### Git
    sudo apt install git

#### GitKraken
    sudo snap install gitkraken --classic

#### VsCode
    sudo snap install code --classic
    
#### Discord
    sudo snap install discord

#### AutoKey
	sudo apt install autokey-qt
    
## Android Studio

#### LIBs 64x
    sudo apt install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
    
#### Java
    sudo apt install openjdk-17-jdk openjdk-17-jre
    
#### Android Studio
    sudo add-apt-repository ppa:maarten-fonville/android-studio
####
    sudo apt-get update
####
    sudo apt-get install android-studio

#### Comando para Executar
    /opt/android-studio/bin/studio.sh

## Visual Studio Code | Extensões (Ctrl+P):

#### Portuguese (Brazil) Language Pack:
    ext install MS-CEINTL.vscode-language-pack-pt-BR

#### Atom Material Icons:
    ext install AtomMaterial.a-file-icon-vscode

#### Dracula Official:
    ext install dracula-theme.theme-dracula

#### Docker:
    ext install ms-azuretools.vscode-docker
    
#### Dev Containers:
    ext install ms-vscode-remote.remote-containers

#### GitLens:
    ext install eamodio.gitlens
 
#### Git Graph
    ext install mhutchie.git-graph

#### Auto Close Tag:
    ext install formulahendry.auto-close-tag

#### Auto Rename Tag:
    ext install formulahendry.auto-rename-tag

#### PHP Intelephense:
    ext install bmewburn.vscode-intelephense-client
    
#### Prettier - Code formatter:
    ext install esbenp.prettier-vscode

#### IntelliCode:
    ext install VisualStudioExptTeam.vscodeintellicode

#### Bootstrap IntelliSense:
	ext install hossaini.bootstrap-intellisense

#### Bootstrap 5 Quick Snippets
	ext install AnbuselvanRocky.bootstrap5-vscode

#### Colorize:
    ext install kamikillerto.vscode-colorize

#### Bookmarks
	ext install alefragnani.Bookmarks

#### Output Colorizer:
    ext install IBM.output-colorizer
	
#### VS Code PDF
	ext install tomoki1207.pdf

#### GitHub Copilot
	ext install GitHub.copilot

#### GitHub Copilot Chat
	ext install GitHub.copilot-chat

#### Commit Message Editor
	ext install adam-bender.commit-message-editor

## Visual Studio Code | Configurações (Ctrl + Shift + P):

#### Idioma:
    Configure Display Language
    
## Visual Studio Code | Configurações (Usuário - settings.json):
	{
		"workbench.iconTheme": "vscode-icons",
		"workbench.colorTheme": "Dracula",
		"editor.bracketPairColorization.enabled": true,
		"editor.minimap.enabled": false,
		"editor.guides.bracketPairs": "active",
		"editor.defaultFormatter": "esbenp.prettier-vscode",
		"diffEditor.ignoreTrimWhitespace": false,
		"explorer.confirmDelete": false,
		"files.autoSave": "onFocusChange",
		"files.encoding": "iso88591",
		"git.confirmSync": false,
		"prettier.tabWidth": 4,
		"vsicons.dontShowNewVersionMessage": true,
		"auto-close-tag.enableAutoCloseTag": true,
		"auto-close-tag.enableAutoCloseSelfClosingTag": true,
		"auto-close-tag.insertSpaceBeforeSelfClosingTag": false,
		"files.associations": {
			"*.php": "php"
		},
		"[php]": {
			"editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
		},
		"auto-rename-tag.activationOnLanguage": [
			"html",
			"xml",
			"php",
			"javascript"
		],
		"auto-close-tag.activationOnLanguage": [
			"xml",
			"php",
			"blade",
			"ejs",
			"jinja",
			"javascript",
			"javascriptreact",
			"typescript",
			"typescriptreact",
			"plaintext",
			"markdown",
			"vue",
			"liquid",
			"erb",
			"lang-cfml",
			"cfml",
			"HTML (Eex)"
		],
		"gitlens.gitCommands.skipConfirmations": [
			"fetch:command",
			"switch:command"
		],
		"git.openRepositoryInParentFolders": "always"
	}

## Visual Studio Code | Configurações (Extensões):

#### PHP Intelephense:
- Procurar em Extensões por: @builtin php
+ Desabilitar: PHP Language Features (Recursos da Linguagem PHP)
