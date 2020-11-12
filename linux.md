# Linux

## Astuces (CLI)

- **tabulation** est une touche magique. Elle permet : 
  - soit d'utiliser l'autocomplétion dans la console / le terminal
  - soit d'afficher l'ensemble des éléments dans le dossier cible en appuyant 2 fois dessus
- **fleche du haut / bas** : Permet de naviguer parmis les anciennes commandes effectuées
- **\<command\> && \<command\>** : Permet d'enchaîner plusieurs commandes en une seule ligne.

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


## Quelques fichiers

- **~/.bashrc** : fichier permettant de gérer les "alias" et donc les raccourcis"

### La prochaine fois : 
- users
- groups
- chown
- chmod
- architecture
- which
- histoire de linux
- arrêt et redémarrage
- processus
- gestion de packages (apt)
- path
- wildcard * 
- tar
- cpio
- dd

- shell ?
