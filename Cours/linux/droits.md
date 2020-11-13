# Les droits sous Linux

Linux intègre un système de gestion des droits complet et prennant en charge les utilisateurs aussi bien que les groupes.

## Les droits

- **r** : Le droit de lecture (r = read = lire)
- **w** : le droit d'écriture (w = write = écrire)
- **x** : le droit d'exécution (x = eXecute = exécuter)

### Affichage des droits

Lorsque vous listez le contenu d'un répertoire grâce par exemple à la commande __ls -al__, vous obtenez un série de caractères au début de chaque ligne. Par exemple : 

```bash
-rw-r--r-- 1 debian debian 3742 Nov  2 09:38 .bashrc
```

Cette série de caractères permet d'informer sur les droits dudit fichier ainsi que sur son type. Elle peut être découpée en 4 parties : 

- 1ère partie : premier caractère. Ce caractère peut prendre 3 formes différentes selon si l'élément est : 
	- **-** : permet de renseigner que l'élément est un fichier
	- **d** : permet de renseigner que l'élément est un répertoire (d = directory = répertoire)
	- **l** : permet de renseigner que l'élément est un lien symbolique (l = link = lien)
- 2ème partie : un groupement de 3 caractères (du 2ème au 4ème). Ce premier trinôme concerne l'utilisateur propriétaire de l'élément.
- 3ème partie : un groupement de 3 caractères (du 5ème au 7ème). Ce deuxième trinôme concerne le groupe affecté à l'élément et tous les utilisateurs étant liés à ce groupe.
- 4ème partie : un groupement de 3 caractères (du 8ème au 10ème). Ce troisième trinôme concerne les autres utilisateurs du système.

Chacun des groupements de caractères ont une signification précise. Ils sont constitués d'une suite de 3 caractères qui permettra de définir des droits d'accès en lecture, en écriture ou en exécution respectivements représentés par leurs symboles. Les 3 caractères peuvent être représentés de la sorte : 

1. **-** ou **r** : si le caractère est un __r__, alors le droit de lecture est attribué. Si c'est un __-__, alors il ne l'est pas.
2. **-** ou **w** : si le caractère est un __w__, alors le droit d'écriture est attribué. Si c'est un __-__, alors il ne l'est pas.
3. **-** ou **x** : si le caractère est un __x__, alors le droit d'exécution' est attribué. Si c'est un __-__, alors il ne l'est pas.




