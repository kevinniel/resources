# CRON

## Qu'est-ce que c'est

C'est un outil qui permet de déclencer des actions / des scripts de manière planifiée. Il peut être modifié grâce à l'utilitaire __crontab__.

## Commandes utiles
- **crontab -l** : Permet d'afficher le contenu du ficher crontab
- **crontab -e** : Permet d'éditer le contenu du ficher crontab

## Rappel utile

```
# Example of job definition:
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  *  user command to be executed
```

## Les valeurs possibles
Pour chaque ligne de tâche dans le CRON, vous devez renseigner 5 valeurs. Chacune doit être séparée par un espace des autres précisément.

Pour chaque unité, plusieurs notations peuvent être utilisées : 
- **1** : prendra en compte l'unité "1"
- **1-5** : prendra en compte toutes les unités de 1 à 5
- **\*/6** : prendra en compte toutes les unités en comptant par intervalle de "6" (ex : 0, 6, 12, 18, 24, etc...)
- **2,4,8** : prendra en compte les unités "2", "4", "8" précisément