# Utilisateurs & Groupes

## Infos utiles
- les utilisateurs sont stockés dans le fichier __/etc/passwd__
- les groupes sont stockés dans le fichier __/etc/group__

## Commandes
- **useradd \<username\>** : commande permettant d'ajouter un utilisateur
- **useradd -G \<groups\> \<username\>**: crée un utilisateur __username__ en lui affectant automatiquement les groupes listés dans __groups__ (si plusieurs, groupes, les séparer par des virgules)
- **passwd \<username\>** : permet de définir le nouveau mot de passe à l'uilisateur __username__. Par défaut, si vous saisissez unqieuemnt __passwd__, alors vous pourrez modifier le MDP de l'utilisateur avec lequel vous êtes connecté.
- **userdel \<username\>** : permet de supprimer l'utilisateur __usernmae__
- **groupadd \<nom_du_groupe\>** : permet de créer un groupe __nom_du_groupe__
- **groupdel \<nom_du_groupe\>** : permet de supprimer le groupe __nom_du_groupe__
- **gpasswd -a \<utilisateur\> \<groupe\>** : permet d'ajouter l'utilisateur existant __utilisateur__ au groupe existant __groupe__
- **gpasswd -d \<utilisateur\> \<groupe\>** : permet de supprimer l'utilisateur existant __utilisateur__ du groupe existant __groupe__
