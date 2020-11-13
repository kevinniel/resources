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

### Les correspondances de valeurs pour les droits

| Position binaire | Valeurs octale | Textuel | Droits |
|------------------|----------------|---------|--------|
|       000        |       0        |  \-\-\- | ø |
|       001        |       1        |  \-\-x  | Exécuter |
|       010        |       2        |  \-w\-  | Ecrire |
|       011        |       3        |  \-wx   | Ecrire, Exécuter |
|       100        |       4        |  r\-\-  | Lire |
|       101        |       5        |  r\-x   | Lire, Exécuter |
|       110        |       6        |  rw\-   | Lire, Ecrire |
|       111        |       7        |  rwx    | Lire, Ecrire, Exécuter |

Il existe plusieurs moyens de représenter des droits. Nous avons vu ci-dessus la forme "textuelle". Il existe également une forme dite "Octale" (nombres de 0 à 7) ainsi qu'une forme binaire (de 000 à 111). Voici un tableau de correspondance : 

## Les commandes

### CHOWN
CHOWN (Change Owner) permet de changer l'appartenance d'un élément. Vous allez pouvoir changer le propriétaire d'un élément, aussi bien que le groupe auquel il est affecté. Pour l'utiliser : 

```
chown \[utilisateur\]\[groupe\] targets
```

quelques exemples : 
```
chown toto a // va définir le propriétaire du fichier "a" comme étant "toto"
chown -R toto a // va définir le propriétaire du dossier "a" comme étant "toto"
chown -R toto:tata a // va définir le propriétaire du dossier "a" comme étant toto, et le groupe associé au dossier comme étant "tata"
chown toto a b c d // va définir toto comme étant le propriétaire des fichiers "a", "b", "c" et "d".
```

### CHMOD
Le CHMOD permet de modifier les droits à un élément. Pour pouvoir utiliser cette commande sur un élément, il faut soit être en utilisateur "root", soit être son propriétaire.

Il existe plusieurs syntaxes pour utiliser cette commande. Parmis lesquelles :

#### la syntaxe textuelle

La commande s'effectuera de la sorte : __chmod u+rwx,g+rwx,o+rwd fichiers__ .
On distingue bien nos trois groupements de droits, séparés par des virgules. Ici dans l'exemple, tous les droits sont attribués à tout le monde : 

- **u+rwx** : __u__ pour "user" (donc tous les utilisateurs). __+__ pour affecter les droits. Le triptyque représentatif des droits à attribuer.
- **g+rwx** : __g__ pour "group" (donc le groupe lié). __+__ pour affecter les droits. Le triptyque représentatif des droits à attribuer.
- **o+rwx** : __o__ pour "owner" (donc le propriétaire). __+__ pour affecter les droits. Le triptyque représentatif des droits à attribuer.
- **fichiers** : le ou les fichiers concernés. S'il s'agit d'un dossier, penser à inclure la récursivité avec l'option __-R__ comme pour CHOWN.

Lorsque vous ne souhaitez pas attribuer l'un des droits ci-dessus au groupe, au propriétaire ou aux utilisateurs, alors vous devez remplacer le caractère représentant votre droit par un __-__.






