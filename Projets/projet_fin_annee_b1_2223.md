## Contexte

Réalisation d'un projet regroupant l'ensemble des notions abordées dans l'année

## Objectifs

- comprendre la réalisation d'un projet de A à Z
- découvrir les aspects fonctionnels et techniques

## Travaux

Réalisation d'une application web sur le sujet de votre choix. Les différents travaux sont à mener : 

- réalisation d'un cahier des charges
- réalisation des documentations techniques et fonctionnelles
- réalisation d'une charte graphique
- développement de l'application

## Rendus

- 1 repo GIT par projet (dev)
- 1 Drive partagé à l'adresse mail : k.niel.pro@gmail.com

### Architecture du drive

```
|--D Cahier des charges
|--|----F Cahier des charges
|--|----D Brainstorming
|--D Documentation
|--|----D Technique
|--|----|----F Documentation technique
|--|----|----D Brainstorming
|--|----D Fonctionnelle
|--|----|----F Documentation fonctionnelle
|--|----|----D Brainstorming
|--D Graphisme
|--|----F Charte graphique
|--|----D Brainstorming
```

## Etapes

1. Listing de fonctionnalités (cahier des charges)
2. Dictionnaire des données (documentation fonctionnelle & technique)
  ==> Tableau Excel. L'idée est de décrire les tables de vos bases de données. Pour ça, 4 colonnes : 
    - nom de la table
    - Nom du champs
    - Type du champs
    - Spécification (AutoIncrement, NotNull)
    - Commentaires
3. Laravel
   - initialiser le projet
   - mettre en place les migrations
   - mettre en place les seeders
   - mettre en place les factories
4. Graphisme
  - trouver un template qui corresponde à vos besoins (adminLTE répond à beaucoup de besoins) OU trouver une maquette figma, et l'intégrer en HTML/CSS
5. Intégration static
  - Refaire toutes les pages du site web, en static (HTML + CSS + JS uniquement)
  __Remarque__ : Vous pouvez mettre les fichiers en ```.php``` pour gérer des include (menus, etc...)
6. Vérification des données
  - Vérifier que vos données en base de données soient suffisantes (qu'il ne vous en manque pas)
7. Mettre en place le templating avec Blade, définir le layout de base
8. pour chaque fonctionnalité, réaliser dans l'ordre : 
  - La création de la route, en lui donnant un nom
  - La mise en place du contrôleur et de sa méthode comme définie dans la route
  - La mise en place des modèles - dans un premier temps sans les relations
  - La mise en place de la vue associée

