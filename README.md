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
	alias vpnup='openvpn3 session-start --config /home/bracin/Genesis/Dourados/VPN_Dourados.ovpn && openvpn3 sessions-list'
####
	alias vpndown='for session in $(openvpn3 sessions-list | grep "Path" | awk "{print \$2}"); do openvpn3 session-manage --disconnect --path "$session"; done'

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
    sudo apt install php7.4-cli php7.4-common php7.4-fpm php7.4-mysql php7.4-pgsql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath php7.4-pgsql php7.4-bz2 php7.4-intl php7.4-json
##### Extensões PHP 8.2
	sudo apt install php8.2-cli php8.2-common php8.2-fpm php8.2-mysql php8.2-pgsql php8.2-zip php8.2-gd php8.2-mbstring php8.2-curl php8.2-xml php8.2-bcmath php8.2-pgsql php8.2-bz2 php8.2-intl php8.2-imap php8.2-ldap
##### Extensões PHP 8.3
	sudo apt install php8.3-cli php8.3-common php8.3-fpm php8.3-mysql php8.3-pgsql php8.3-zip php8.3-gd php8.3-mbstring php8.3-curl php8.3-xml php8.3-bcmath php8.3-pgsql php8.3-bz2 php8.3-intl php8.3-imap php8.3-ldap

#### Trocar a Versão do PHP
#### Para 7.4
	sudo update-alternatives --set php /usr/bin/php7.4
#### Para 8.2
	sudo update-alternatives --set php /usr/bin/php8.2

#### Docker
    sudo apt update
####
	sudo apt-get install ca-certificates curl
####
    sudo install -m 0755 -d /etc/apt/keyrings
####
    sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
####
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo ${UBUNTU_CODENAME:-$VERSION_CODENAME}) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
####
    sudo apt update
####
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
####
	sudo docker run hello-world
####
    sudo groupadd docker
####
    sudo usermod -aG docker $USER
####
	docker run hello-world

#### Docker Compose
##### [Verificar a ultima versão](https://github.com/docker/compose/releases) 
    sudo curl -SL https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
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
    sudo apt install postgresql postgresql-contrib

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
    /opt/android-studio/bin/studio

## Visual Studio Code | Extensões (Ctrl+P):

#### Atom Material Icons:
    ext install AtomMaterial.a-file-icon-vscode

#### Auto Close Tag:
    ext install formulahendry.auto-close-tag

#### Auto Rename Tag:
    ext install formulahendry.auto-rename-tag

#### Bookmarks
	ext install alefragnani.Bookmarks

#### Bootstrap IntelliSense:
	ext install hossaini.bootstrap-intellisense

#### Colorize:
    ext install kamikillerto.vscode-colorize

#### Commit Message Editor
	ext install adam-bender.commit-message-editor

#### Dev Containers:
    ext install ms-vscode-remote.remote-containers

#### Docker:
    ext install ms-azuretools.vscode-docker

#### DotENV
	ext install mikestead.dotenv

#### Dracula Official:
    ext install dracula-theme.theme-dracula

#### Error Lens
	ext install usernamehw.errorlens

#### Git Graph
    ext install mhutchie.git-graph

#### GitHub Copilot
	ext install GitHub.copilot

#### GitHub Copilot Chat
	ext install GitHub.copilot-chat

#### GitLens:
    ext install eamodio.gitlens

#### IntelliCode:
    ext install VisualStudioExptTeam.vscodeintellicode

#### Output Colorizer:
    ext install IBM.output-colorizer

#### PHP Debug
	ext install xdebug.php-debug

#### PHP Intelephense:
    ext install bmewburn.vscode-intelephense-client

#### PHP Namespace Resolver
	ext install MehediDracula.php-namespace-resolver

#### Portuguese (Brazil) Language Pack:
    ext install MS-CEINTL.vscode-language-pack-pt-BR

#### Prettier - Code formatter:
    ext install esbenp.prettier-vscode

#### VS Code PDF
	ext install tomoki1207.pdf

## Visual Studio Code | Configurações (Ctrl + Shift + P):

#### Idioma:
    Configure Display Language
    
## Visual Studio Code | Configurações (Usuário - settings.json):
	{
	    "workbench.iconTheme": "a-file-icon-vscode",
	    "workbench.colorTheme": "Dracula Theme",
	    "workbench.activityBar.location": "top",
	    "editor.bracketPairColorization.enabled": true,
	    "editor.guides.bracketPairs": "active",
	    "editor.linkedEditing": true,
	    "editor.minimap.enabled": false,
	    "editor.tabSize": 4,
	    "editor.wordWrapColumn": 120,
	    "editor.defaultFormatter": "esbenp.prettier-vscode",
	    "diffEditor.ignoreTrimWhitespace": true,
	    "explorer.confirmDelete": false,
	    "files.autoSave": "onFocusChange",
	    "files.encoding": "utf8",
	    "files.associations": {
	        "*.php": "php",
	        ".env*": "dotenv"
	    },
	    "[php]": {
	        "editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
	    },
	    "git.confirmSync": false,
	    "git.allowForcePush": true,
	    "git.autofetchPeriod": 1800,
	    "git.autofetch": "all",
	    "git.openRepositoryInParentFolders": "always",
	    "gitlens.gitCommands.skipConfirmations": ["fetch:command", "switch:command"],
	    "prettier.tabWidth": 4,
	    "prettier.printWidth": 120,
	    "window.commandCenter": false,
	    "auto-close-tag.enableAutoCloseTag": true,
	    "editor.tokenColorCustomizations": {
	        "[*Light*]": {
	            "textMateRules": [
	                {
	                    "scope": "ref.matchtext",
	                    "settings": {
	                        "foreground": "#000"
	                    }
	                }
	            ]
	        },
	        "[*Dark*]": {
	            "textMateRules": [
	                {
	                    "scope": "ref.matchtext",
	                    "settings": {
	                        "foreground": "#fff"
	                    }
	                }
	            ]
	        },
	        "textMateRules": [
	            {
	                "scope": "keyword.other.dotenv",
	                "settings": {
	                    "foreground": "#FF000000"
	                }
	            }
	        ]
	    }
	}

## Visual Studio Code | Configurações (Extensões):

#### PHP Intelephense:
- Procurar em Extensões por: @builtin php
+ Desabilitar: PHP Language Features (Recursos da Linguagem PHP)
