# Artisan

Artisan est une interface utilisable en ligne de commande (CLI - Command Line Interface).

## Utilisation de base
Artisan est basé sur PHP, et nécessite donc l'utilisation de la commande "PHP" pour s'en servir.
Toute commande artisan débute donc par "php artisan".
La commande "php artisan" seule, affichera l'ensemble des commandes disponibles proposées par Artisan.

## Commandes usuelles
- Création de fichiers : Artisan nous permet de générer des fichiers a l'aide de la commande "make". On doit ensuite interposer le symbole ":", puis spécifier le type de fichier que l'on veut créer.
- gestion de la base de données : Artisan nous permet de créer, modifier ou supprimer des tables au sein d'une base de données. Il utilise les fichiers de migration, mais n'exécute chaque migration, que sur les fichiers qui n'ont pas déjà été migrés. Pour cela, il faut utiliser la commande "migrate".
- gestion du cache : Artisan nous permet de nettoyer le cache de manière rapide et simple avec la commande "cache:clear".
- Affichage des routes : Artisan nous permet d'afficher les routes existantes au sein de l'application avec la commande "route:list".
- publication des vendors : Artisan nous permet de publier les dépendances et librairies utilisées au sein d'un projet Laravel. Ceci nous permettant de modifier ces librairies et dépendances sans crainte de voir le travail perdue pour cause de mise à jour. la commande étant "vendor:publish"
