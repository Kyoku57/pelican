Trucs et astuces pour Pelican
#############################

Personnaliser l'url d'un article pour Pelican
=============================================

Par défaut, quand vous créez un article ayant pour titre *Mon article pour Pelican*,
l'url par défaut devient *mon-article-pour-pelican.html*. Cependant, il est possible 
de modifier cela en utilisant la technique utilisée pour les traductions d'article,
c'est à dire le paramètre *:slug:* ::

	Mon article pour Pelican
	########################

	:date: 2011-01-31 11:05
	:slug: super-article-pour-pelican

	bla, bla, bla …

En prenant cet exemple ci dessus, votre url deviendra *super-article-pour-pelican.html*


Créer des liens directs entre vos documents
===========================================

Dans cette exemple, on va encore se servir du paramètre *:slug:* ::

Prenons le cas de l'arboresence suivante ::

    |-- Cat1                    # category
    |   `-- article1.rst        # article avec :slug:article-1
    |-- Cat2                    # category
    |   `-- article2.rst        # article avec :slug:article-2
    |-- Cat3                    # category
    |   |-- article3.rst        # article avec :slug:article-3
    |   `-- article4.rst        # article avec :slug:article-4
    |-- pages                   # dossier static
        `-- contact.rst         # page avec :slug:contact


Pour faire un lien d'un article ou d'une page vers un autre article, on utilise la syntax *:link:slug:title*


Exemple ::

    Vous pouvez consulter l':link:article-3:article 3: sur le sujet numéro 3
    

Pour faire un lien d'un article ou d'une page vers une autre page, on utilise la syntax *:link:pages/slug:title*


Exemple ::

    Vous pouvez consulter l':link:pages/contact:La page suivante: sur le sujet de la page

