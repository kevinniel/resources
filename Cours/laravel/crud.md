# Etapes d'un CRUD

1. Création d'une table en base de données :
    - Création d'un ou plusieurs fichier(s) de migration avec la commande "php artisan make:migration [NOM_DU_FICHIER_DE_MIGRATION]"
    - Migration des fichiers grâce à la commande "php artisan migrate"
2. Création du modèle en lien avec la table créée en base de données :
    - Création du fichier avec la commande "php artisan make:model [NOM_DU_MODEL]"
    - Renseignement du nom de la table en lien avec le nouveau modèle grâce à l'attribut : "protected $table="[NOM_DE_LA_TABLE]";"
    - Renseignement des champs de la table qui peuvent être modifiés grâce au modèle via le tableau unidimensionnel contenu dans l'attribut "protected $fillable=[TABLEAU_DES_CHAMPS]"
3. Création d'une ou plusieurs route(s)
    - Ajout de la / des route(s) dans le fichier "/routes/web.php". Renseignement de l'URL attendue, du contrôleur ainsi que de sa méthode qui doit être appelée au matching de l'URL, puis définition d'un nom sur la route pour facilité son utilisation a posteriori.
4. Création du contrôleur
    - Création du fichier avec la commande "php artisan make:controller [NOM_DU_CONTROLLER]"
    - Définition de la / des méthode(s) en lien avec les routes précédemment créées
    - Penser à retourner les vues à l'issue de chaque méthode du controleur
5. Création des vues
    - Pour chaque vue nécessaire, créer un fichier avec l'extension ".blade.php" dans le dossier "/ressources/views/". Nommer ce fichier de telle sorte à pouvoir l'appeler simplement dans les méthodes des contrôleurs.