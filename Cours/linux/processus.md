# Processus

## Définition

Les processus sont l'ensemble des programmes disponibles sur votre machine.

## Commandes

- **top** : permet de lister l'ensemble des processus sous forme de tableau en temps réel selon leur activité (pour quitter le tableau, tapez "q"): 
	- **PID** : (Processus IDentifier) identifiant "unique" d'un processus.
	- **USER** : utilisateur qui lance le processus
	- **PR** : (PRiority) Ordre de priorité
	- **S** : (State) Etat du processus
		- **D** : Le processus est en sommeil, non interruptible
		- **S** : Le processus est en sommeil, mais interruptible
		- **I** : Le processus est inactif
		- **R** : Le processus est en cours d'exécution
	- **%CPU** : pourcentage de CPU utilisé (processeur)
	- **%MEM** : pourcentage de mémoire utilisé
	- **TIME** : Temps total de processeur utilisé par le processus depuis son lancement
	- **COMMAND** : nom de la commande / ligne de commande
- **ps** : permet de montrer l'ensemble des processus lancés par l'utilisateur courant au moment de la commande
- **ps aux** : permet de montrer l'ensemble des processus de la machine au moment de la commande
- **ps -u \<username\>** : Permet d'afficher l'ensemble des processus lancés par l'utilisateur __username__
- **killall \<nomcommande\>** : Permet de forcer l'arrêt des processus issus de la commande __nomcommande__
- **kill -9 \<PID\>** : Permet de forcer l'arrêt du processus en fonction de son identifiant __PID__
- **pkill -u \<username\>** : Permet de forcer l'arrêt des processus d'un utilisateur