=============
Plan directeur de l'API
=============

API Blueprint est un langage de haut niveau pour la description des API Web. La syntaxe est une combinaison de la syntaxe Markdown et de la syntaxe Markdown pour la notation des objets (MSON), et les fichiers sont enregistrés avec une extension `.apib`. Markdown est une syntaxe légère de formatage de texte. `MSON <https://github.com/apiaryio/mson>`_ est une extension de Markdown pour la description des objets de données.

L'objectif du format API Blueprint est de soutenir la philosophie de conception première des API REST ; cependant, le format fonctionne tout aussi bien pour la documentation des API existantes.

Pour commencer
---------------

La façon la plus rapide de commencer est d'utiliser `Apiary <https://apiary.io/>`_ pour éditer et visualiser votre documentation. Apiary est un service qui vous permet d'éditer et d'héberger de la documentation en ligne. Commencez par vous inscrire à un compte `sur Apiary. <https://login.apiary.io/register>`_
Ensuite, continuez avec le `tutoriel sur le plan directeur de l'API. <https://apiblueprint.org/documentation/tutorial.html>`_ Il fournit un bon aperçu de la façon de décrire une API de base.

Rédaction de documents
------------

La structure d'un fichier ``.apib`` est : :

  Métadonnées
  Nom de l'API
  Groupe de ressources
    Ressource
      Action
      Action
    Ressource
  Groupe de ressources
  Structures de données

Métadonnées :
  décrit la version de l'API Blueprint

``Nom de l'API`` :
  est le nom de votre API

Groupes de ressources" :
  décrit une collection de points de terminaison d'API connexes

``Resources`` :
  décrit un point de terminaison d'API spécifique

``Actions`` :
  décrit les actions spécifiques du verbe http sur un point de terminaison.

Structures de données" :
  décrit les données utilisées dans vos demandes/réponses d'API. En les définissant dans une section distincte, elles peuvent être facilement réutilisées.

Création de documents
-------------

Les deux outils les plus populaires pour générer des documents à partir de Blueprints d'API sont Apiary et `Aglio <https://github.com/danielgtaylor/aglio>`_.

* :ref:`apiary-building-docs` avec Apiary.
