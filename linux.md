# Linux

## Astuces (CLI)

- **tabulation** est une touche magique. Elle permet : 
  - soit d'utiliser l'autocomplétion dans la console / le terminal
  - soit d'afficher l'ensemble des éléments dans le dossier cible en appuyant 2 fois dessus
- **fleche du haut / bas** : Permet de naviguer parmis les anciennes commandes effectuées
- **\<command\> && \<command\>** : Permet d'enchaîner plusieurs commandes en une seule ligne.
- **le wildcard \( * \)** : Est un symbole qui permet de tout sélectionné :D

## Ligne de commande (CLI)

- **ls** : Lister l'ensemble des fichiers & dossiers présents dans le répertoire courant, sans les dossiers et fichiers cachés
- **ls -al** : Lister l'ensemble des fichiers & dossiers présents dans le répertoire courant, y compris les dossiers et fichiers cachés
- **cd \<dossier\>** : Permet de changer de dossier courant
  - **cd /** : permet d'aller a la racine du système
  - **cd** : permet d'aller a la racine du dossier personnel de l'utilisateur connecté
- **nano** : Permet d'éditer un fichier. Attention, les commandes une fois dans le programme sont renseignées en bas de l'écran, avec un chapeau (^) qui représente la touche "Ctrl".
- **source \<fichier\>** : permet de "recharger" le fichier dans le système pour la prise en compte des modifications effectuées
- **sudo \<action\>** : permet d'exécuter une action en changeant l'utilisateur courant, et principalement en utilisant l'utilisateur "root" qui dispose de tous les droits par défaut.
- **mkdir \<nom\>** : crée un dossier dans le répertoire courant avec le nom renseigné
- **rm** : permet de supprimer des éléments
  - **rm \<fichier\>** : permet de supprimer un fichier
  - **rm -r \<dossier\>** : permet de supprimer un dossier et tout son contenu (le "-r" permet de signifier la __reccursivité__)
  - **rm -rf \<dossier\>** : force la suppression du dossier grace au "-f" ( pour "forcer")
- **touch \<nom\>** : Permet de créer un fichier avec le nom "__nom__"
- **cat \<fichier\>** : Permet d'afficher dans la console le contenu du fichier sans l'ouvrir
- **mv** : Permet de déplacer des éléments
  - **mv \<source\> \<destination\>** : Permet de déplacer l'élément __source__ a l'emplacement de __destination__
  - **astuce** : __mv__ est également utilisé pour renommer des fichiers. Par exemple, si un fichier s'appelle "toto" et que l'on souhaite le renommer "tata", il suffira d'utiliser la commande __mv__ de la sorte : **mv toto tata**
- **cp** : Permet de copier des éléments
  - **cp \<fichier_source\> \<fichier_destination\>** : Copie le fichier source en fichier de destination
  - **cp -r \<dossier_source\> \<dossier_destination\>** : Copie le dosser source en dossier de destination (le "-r" permet de signifier la __reccursivité__)
- **grep \<regex || string\> \<fichier\>** : Permet d'effectuer une recherche dans un fichier, a partir d'une regex, ou d'une string
- **man \<command\>** : Permet de vous afficher la documentation de la commande renseignée
- **whereis \<string\>** : Permet de rechercher tous les fichiers nommés __\<string\>__ parmis les fichiers exécutables de l'OS.
- **apt-get \<command\>** : Gestionnaire de paquets de l'OS
  - **apt-get update** : met à jour la liste des paquets disponibles
  - **apt-get upgrade** : met à jour les paquets déjà installés sur votre machine
  - **apt-get install \<paquet1\> \<paquet2\> ...** : installer un ou plusieurs paquets
  - **apt-get remove \<paquet1\> \<paquet2\> ...** : supprimer les paquets __SANS__ les fichiers de configuration
  - **apt-get purge \<paquet1\> \<paquet2\> ...** : supprimer les paquets __ET__ les fichiers de configuration
  - **apt-get autoclean** : permet de supprimer les paquets "vieux" et "non utilisés". Conserve les versions à jour des paquets.
- **su \<username\>** : permet de se connecter en tant qu'un autre utilisateur
- **shutdown -h now** : permet d'arrêter la machine
- **shutdown -r now** : permet de redemarrer la machine
- **reboot** : permet de redemarrer la machine
- **reboot -f** : permet de forcer le redemarrage la machine

### Utilisateurs & Groupes

#### Infos utiles
- les utilisateurs sont stockés dans le fichier __/etc/passwd__
- les groupes sont stockés dans le fichier __/etc/group__

#### Commandes
- **useradd \<username\>** : commande permettant d'ajouter un utilisateur
- **useradd -G \<groups\> \<username\>**: crée un utilisateur __username__ en lui affectant automatiquement les groupes listés dans __groups__ (si plusieurs, groupes, les séparer par des virgules)
- **passwd \<username\>** : permet de définir le nouveau mot de passe à l'uilisateur __username__. Par défaut, si vous saisissez unqieuemnt __passwd__, alors vous pourrez modifier le MDP de l'utilisateur avec lequel vous êtes connecté.
- **userdel \<username\>** : permet de supprimer l'utilisateur __usernmae__
- **groupadd \<nom_du_groupe\>** : permet de créer un groupe __nom_du_groupe__
- **groupdel \<nom_du_groupe\>** : permet de supprimer le groupe __nom_du_groupe__
- **gpasswd -a \<utilisateur\> \<groupe\>** : permet d'ajouter l'utilisateur existant __utilisateur__ au groupe existant __groupe__
- **gpasswd -d \<utilisateur\> \<groupe\>** : permet de supprimer l'utilisateur existant __utilisateur__ du groupe existant __groupe__

## Quelques fichiers utiles
- **~/.bashrc** : fichier permettant de gérer les "alias" et donc les raccourcis"

## Architecture des fichiers

```bash
\
├── bin
|   ├── cd
|   ├── nano
|   ├── mv
|   └── ...      //contient les commandes de LINUX
|
├── boot   // système pour le lancement
|   ├── grub
|   └── ... -amd64
|
├── dev      //périphériques
|   ├── stdin
|   ├── stdout
|   ├── cdrom
|   └── ...
|
├── etc   //configuration système
|   ├── sudoers
|   ├── sudoers.d
|   └── ...
|
├── home
|   ├── lost+found     // ne peut pas être ouvert
|   └── osboxes        // nom de l'utilisateur
|       ├── Desktop
|       ├── Documents
|       └── ...        // contient fichiers perso du user
|
├── mnt
|
├── opt
|
├── proc
|   └── ... // tous les fichiers temp de processus
|
├── root  // répertoire admin système
|
├── run    // fichiers pour l'execution
|   ├── alsa
|   ├── cup
|   └── ...
|
├── srv
|
├── sys   // fonctionnalité système
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
├── tmp
|   └── ...  // Fichiers temporaires
|
├── usr
|   ├── bin
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
```

### reste à voir : 
- chown
- chmod
- which
- histoire de linux
- processus
- path
- tar
- cpio
- dd

- shell ?

# A faire pour demain (13/11/2020) 
- Architecture des dossiers / fichiers
  - exemple : https://www.cyberciti.biz/media/new/faq/2012/11/Tree-Display-Structure-Directory-Hierarchy.png
  - faire au format MarkDown un treeview des dossiers et fichiers importants, en expliquant à chaque fois son rôle / but
- Histoire de linux
  - au format markdown
  - uniquement une liste de dates / évènements importants sur l'histoire de linux
