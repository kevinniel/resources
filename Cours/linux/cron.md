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