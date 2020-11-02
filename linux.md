# Linux

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

## Quelques fichiers

- **~/.bashrc** : fichier permettant de gérer les "alias" et donc les raccourcis"
