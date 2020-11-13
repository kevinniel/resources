# Architecture des fichiers

```bash
\
├── boot // système pour le lancement. ce sont les fichiers qui sont exécutés lors du lancement de l'OS
|   ├── grub
|   └── ... -amd64
|
├── dev // fichiers pilotes des périphériques
|   ├── stdin
|   ├── stdout
|   ├── cdrom
|   └── ...
|
├── etc //configuration système
|   ├── cron.d
|   ├── cron.daily
|   ├── cron.hourly
|   ├── cron.monthly
|   ├── crontab // plannification de tâche réccurentes, chronologiques, et automatique
|   └── dhcp // configuration automatique de l'adressage IP en réseau
|   └── dpkg // "debian package" gestionnaire de package de debian
|   └── group // fichier qui contient les groupes d'utilisateurs sur la machine
|   └── hosts // DNS
|   └── init.d // Dossier contenant les services
|       └── apache2
|       └── cron
|       └── mysql
|       └── nginx
|       └── ssh
|       └── sudo
|   └── ldap // Gestion d'annuaire
|   └── mime.types // liste de tous les types de fichiers pris en charges / autorisés
|   └── passwd // fichier qui contient les utilisateurs sur la machine
|   └── ssh // permet de gérer des connexion grâce au protocol SSH
|   └── sudoers // permet de gérer le fonctionnement de la commande "sudo"
|   └── ...
|
├── home
|   └── __user__ // dossier utilisateur qui contient ses fichiers
|       └── ... // dossiers "personnels" de l'utilisateur
|
├── mnt // (mount) point de montage pour les montages temporaires
|
├── opt // répertoire des logiciels "autres" que système
|
├── proc // tous les fichiers temporaires de processus. Contient des informations système
|   └── ... 
|
├── root // répertoire admin système (de l'utilisateur "root")
|
├── run // fichiers contenant des données d'execution
|   ├── alsa
|   ├── cup
|   └── ...
|
├── srv // fichiers contenant des données d'execution fournis par le système
|
├── sys // fonctionnalité système
|   ├── block
|   ├── bus
|   ├── class
|   ├── dev
|   ├── device
|   ├── firmware
|   ├── fs
|   ├── hypervisor
|   ├── kernel
|   ├── module
|   └── power
|
├── tmp // Fichiers temporaires
|   └── ...
|
├── usr // Hiérarchie secondaire = besoin non vital
|   ├── bin //contient les commandes de LINUX
|       ├── cd
|       ├── nano
|       ├── mv
|       └── ...
|   ├── games
|   ├── include
|   ├── lib
|   ├── lib32
|   ├── lib64
|   ├── libexec
|   ├── libx32
|   ├── local
|   ├── sbin
|   ├── share
|   └── src
|
└── var // données variables
|   └── www // en général racine des serveurs web
|   └── ...
```