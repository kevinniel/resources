# CRON

## Qu'est-ce que c'est

C'est un outil qui permet de déclencer des actions / des scripts de manière planifiée. Il peut être modifié grâce à l'utilitaire __crontab__.

## Commandes utiles
- **crontab -l** : Permet d'afficher le contenu du ficher crontab
- **crontab -e** : Permet d'éditer le contenu du ficher crontab
- **crontab -r** : Permet supprimer le contenu du ficher crontab

## Concept

```
# Example of job definition:
# .---------------- minute (0 - 59) (s'exprime de la forme "mm" donc sur 2 chiffres)
# |  .------------- hour (0 - 23) (s'exprime de la forme "hh" donc sur 2 chiffres)
# |  |  .---------- day of month (1 - 31) (s'exprime de la forme "dd" donc sur 2 chiffres)
# |  |  |  .------- month (1 - 12) (s'exprime de la forme "MM" donc sur 2 chiffres)
# |  |  |  |  .---- day of week (0 - 6) (Sunday = 0) (s'exprime de la forme "D" donc sur 1 chiffre)
# |  |  |  |  |
# *  *  *  *  *  [user] command_to_be_executed > log
```

Il y a 2 "paramètres" __optionnels__ lorsque vous insérez une ligne dans le crontab :
- **\[user\]** : qui permet de définir avec quel utilisateur déclencher la ligne de commande.
- **\> log** : qui permet d'écrire dans un fichier de log les éléments de la commande où __log__ est le nom (avec son chemin), du dossier contenant les logs.

## Les valeurs possibles
Pour chaque ligne de tâche dans le CRON, vous devez renseigner 5 valeurs. Chacune doit être séparée par un espace des autres précisément.

Pour chaque unité, plusieurs notations peuvent être utilisées : 
- **1** : prendra en compte l'unité "1"
- **1-5** : prendra en compte toutes les unités de 1 à 5
- **\*/6** : prendra en compte toutes les unités en comptant par intervalle de "6" (ex : 0, 6, 12, 18, 24, etc...)
- **2,4,8** : prendra en compte les unités "2", "4", "8" précisément
- **\*** : prendra en compte toutes les unités possibles

## Quelques exemples

———————————————————————————————————————————————————————————————

__Execution d'une tâche tous les jours, à 22h00__

```
00 22 * * * commande
```

———————————————————————————————————————————————————————————————

__Execution d'une tâche le vendredi, à 8h00, 10h00, 12h00 et 16h00, chaque 26 du mois__

```
00 08,10,12,16 26 * 5 commande
```

———————————————————————————————————————————————————————————————

__Execution d'une tâche par l'utilisateur "John" tous les jours entre 1h et 2h, toutes les 2 minutes, en insérant dans le fichier de log "login_file.txt" les retours de la commande__

```
*/2 01 * * * John commande > login_file.txt
```




