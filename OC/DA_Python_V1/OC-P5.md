1. Identifier les données qui te seront nécessaires et les EndPoints qui correspondent à tes besoins.
2. Réaliser un schéma de BDD (via workbench par exemple). Exporter le script de création de BDD depuis Workbench et vérifier qu'il est fonctionnel. A défaut, effectuer les corrections.
3. Créer un fichier de config et y intégrer une constante qui prendra pour valeur chacune des catégories à récupérer depuis OFF (compter 5 catégories dans cette constante). Intégrer également une constante ("X") pour savoir combien de produits on doit récupérer au maximum pour chaque catégorie.
  - créer un script qui va récupérer la liste des catégories à récupérer (dans le fichier de config)
  - enregistrer en base de données l'ensemble de ces catégories (pour générer des identifiants uniques)
  - Pour chaque catégorie, effectuer une requête à l'API pour récupérer les "X" produits de ladite catégorie.
4. Pour chacun des produits récupérés : vérifier l'intégrité des données (complètes, cohérentes, etc...), puis les enregistrer dans ta base de données en y intégrant l'identifiant de la catégorie correspondante (identifiant provenant de TA base de données)
5. Commencer le programme python "final" : 

Ton menu doit contenir les choix suivants : 

- (etape 3) choisir une catégorie
  - Une fois la catégorie affichée, afficher la liste des produits appartenants à la catégorie.
  - Permettre le choix d'un produit pour afficher de potentiels substituts en fonction du grade nutritionnel
  - Afficher une liste de "Z" potentiels substituts, Z étant un nombre modifiable dans les constantes.
  - Une fois que l'utilisateur à choisi un substitut, lui proposer le l'enregistrer
  - Une fois la décision d'enregistrement effectuée, renvoyer sur le menu principal
- (etape 4) afficher les produits substitués
- (etape 2) réinitialiser la BDD
  - supprimer l'ensemble de l'existant
  - re-créer ta BDD a partir de ton script SQL (qui va être exécuté par Python)
  - re-déclencher l'appel a l'API pour récupérer les informations
- (etape 1) quitter le programme.

## Exemple code python pour requete API
```
URL ='https://fr.openfoodfacts.org/cgi/search.pl'
payload = {
    'action': 'process',
    'tagtype_0': 'categories',
    'tag_contains_0': 'contains',
    'tag_0': category, # => catégorie de te boucle
    'tagtype_1': 'nutrition_grade',
    'tag_contains_1': 'contains',
    'page_size': nb, # => 50
    'json': 'true',
}
req = requests.get(URL, params=payload)
return req.json().get('products')
```
