# Architecture de Laravel

|- /app  
|----- /Console  
|--------- /Commands : Dossier qui contient toutes les commandes personnalisées créées.  
|----- /Exceptions  
|----- /Http  
|--------- /Controller : Dossier qui contiendra l'ensembe des controleurs  
|------------- controller.php : Controleur de base du framework  
|--------- /Middleware : Dossier qui contiendra l'ensemble des middleware  
|----- /Providers  
|----- User.php : Modèle utilisateur généré automatiquement par Laravel  
|- /bootstrap  
|- /config : Contient les fichiers de configuration de l'application  
|- /database  
|----- /migrations : Contient les fichiers de migrations qui permettent de créer, modifier ou   supprimer une ou plusieurs table(s)  
|- /public : dossier d'entrée de l'application  
|----- index.php : point d'entrée de l'application  
|- /ressources  
|----- /lang : dossier qui contient les fichiers de traductions de l'application  
|----- /views : dossier qui contient l'ensemble des vues du projet  
|- /routes  
|----- api.php : fichier pour déclarer les routes relatives à une API  
|----- web.php : fichier pour déclarer les routes relatives à une application web.  
|- /storage  
|- /tests : dossier contenant les tests unitaires & fonctionnels  
|- /vendor : Contient l'ensemble des dépendances du projet (géré par Composer)  
|- composer.json => le fichier qui permet de lister les dépendances  
|- .env => fichier de configuration de l'application  