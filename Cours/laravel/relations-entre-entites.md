# Relations entre entitées

1. Ajouter une foreign key dans votre base de données pour lier une table "A" à une table "B". Ajouter donc un champs "b_id" dans la table "A". Ensuite, déclarer votre foreign dans la migration grâce à : 

    ```
    # b_id est le nom de la colonne créée dans la table représentant le lien vers l'autre table
    # unsigned() permet d'éviter de nombreuses erreurs laravel
    # nullable() vous permet de ne pas rendre obligatoire le remplissage de ce champs.
    $table->bigInteger('b_id')->unsigned()->nullable();

    # le foreign('b_id') indique que c'est le champs 'b_id', créé juste au dessus, qui servira
    # de lien avec l'autre table.
    # references('id)->on('b') signifie que le champs 'b_id' va avoir comme référence (le champs qui va le lié à l'autre table) la colonne 'id', de la table 'b'
    $table->foreign('b_id') 
        ->references('id')
        ->on('b');
    ```

2. Déclarer cette relation dans vos models.
    - Ajouter le champs "b_id" dans l'attribut fillable du model "A"
    - déclarer dans le model "A", la relation avec le model "B", grâce au code suivant : 
    ```
        # le nom de la méthode est arbitraire. Vous pouvez mettre ce que vous souhaitez, cependant c'est ce nom de méthode que vous devrez utiliser avec l'utilisation du "with" plus bas.
        public function b()
        {
            # BelongsTo doit prendre en premier paramètre le nom du model A, puis en second paramètre, le nom du champs dans le modèle courant lié avec le model A grâce à sa foreign key
            return $this->belongsTo(B::class, "b_id");
        }
    ```
    - Vous pouvez déclarer la fonction inverse dans l'autre model pour pouvoir accéder au "with" depuis l'autre model : 
    ```
        # le nom de la méthode est arbitraire. Vous pouvez mettre ce que vous souhaitez, cependant c'est ce nom de méthode que vous devrez utiliser avec l'utilisation du "with" plus bas.
        public function as()
        {
            # la relation inverse se déclare grace a la méthode "hasMany", qui ne prend cette fois en paramètre, que le nom du model "A"
            return $this->hasMany(A::class);
        }
    ```

3. Vous pouvez maintenant vous servir des méthodes "as" et "b" respectivement des modèles "B" et "A" grâce à la méthode "with" d'Eloquent (désormais votre ORM préféré).
Pour cela, vous pouvez par exemple faire l'une des requêtes suivantes : 

```
    # Renverra a la fois le model A, en y incluant dans les relations, l'objet "B" correspondant en base de données
    $obj = A::where('id', $id)->with('b')->first();

    # Renverra a la fois le model B, en y incluant dans les relations, le ou les objets "A" correspondant(s) en base de données
    $obj = B::where('id', $id)->with('as')->first();
```