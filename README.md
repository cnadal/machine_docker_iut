

## 1 - Ce repo sous github contient les fichiers de bases permettant de monter des services sous docker :

**web** : accès via @ip:8082
**mysql** : accès via le port 3306
**phpmyadmin** : accès via @ip:8083

## 2 - Prérequis : avoir installé docker et docker desktop sur votre machine.

### Installation de Docker sous windows
Suivre https://docs.docker.com/desktop/install/windows-install/

### Installation de Docker sous mac intel
Suivre https://docs.docker.com/desktop/install/mac-install/ (partie intel)
Télécharger et installer https://desktop.docker.com/mac/main/amd64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-amd64

### Installation de Docker sous mac m1
Suivre https://docs.docker.com/desktop/install/mac-install/

Exécuter dans un terminal :
softwareupdate --install-rosetta
Télécharger et installer https://desktop.docker.com/mac/main/arm64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-arm64

### Installation de Docker sous linux

Suivre : https://docs.docker.com/desktop/install/linux-install/
Cloner normalement de dépôt git.

## 3 - Config :

> Il faut ensuite *configurer* le fichier <b>.env</b> avec votre nom de
> login car par défaut ce sont des services reliés à cyr qui vont être créés, remplacez <b>cyr</b> par votre Nom, ex pour vivian :

	DB_NAME=testcyr				==> 	DB_NAME=testvivian
	
	PROJECT_NAME=testcyr			==> 	PROJECT_NAME=testvivian
	
	PROJECT_PATH=/var/www/html
	
	MYSQL_USER_NAME=cyr			==> 	MYSQL_USER_NAME=vivian
	
	MYSQL_USER_PASSWORD=toto
	
	MYSQL_ROOT_PASS=root

## 4 - Test :

> Vous pourrez ensuite, exécuter vos conteneurs docker avec la.les
> instruction.s


  	docker compose build	 	la première fois
	docker compose up -d		exécute les conteneurs
						web,			PHP7.4, port 8082
						phpmyadmin,	 	port 8083
						mysql, 			port 3306

	docker compose stop		pour stopper les conteneurs
	
	docker ps			pour lister les conteneurs (on peut alors voir id, port et nom des conteneurs)

	docker exec -it testcyr bash	pour exécuter bash dans le conteneur testcyr (changer de nom ou d'id de conteneur cf commande docker ps)
					
	
	
	
