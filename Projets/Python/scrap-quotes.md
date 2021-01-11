# Scrapper de citations

## Liens utiles

- http://quotes.toscrape.com/
- https://www.crummy.com/software/BeautifulSoup/bs4/doc/
- https://requests.readthedocs.io/en/master/

## Énoncé

En vous servant de la librairie Beautiful Soup 4 (BS4), vous devrez scrapper la totalité des citations présentes sur le site. Vous devrez respecter la structure de stockage d'informations suivante :

- 1 dossier "quotes"
	- 1 fichier "markdown" sous forme de tableau. Chaque ligne devra contenir les informations suivantes (par colonne) : 
		- citation
		- nom de l'auteur
		- liste des tags (sans doublon)
- 1 dossier "tags"
	- 1 fichier "txt" contenant tous les tags. 1 tag par ligne.
- 1 dossier "authors"
	- 1 fichier Excel par auteur, présentant le nom dans une colonne, puis la description dans une autre.

## Contraintes

- Respect de la PEP8 avec __Pylint__ ET __Flake8__
- commits réguliers avec des bons messages, clairs et explicites
- Création d'un dossier "resultats" à la racine du projet. Le contenu de ce dossier devra être ignoré dans github. L'ensemble des éléments scrappés devront y être insérés.