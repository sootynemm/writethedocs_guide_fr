======
Apiary
======

Docs sur l'hébergement
------------

Apiary fournit un service de création et d'hébergement de la documentation des API décrites au format API Blueprint ou Swagger. Une fois la description de l'API terminée, Apiary génère une documentation interactive dans une disposition en trois colonnes. Des exemples de demandes et de réponses sont présentés pour chaque point de terminaison dans plusieurs langages de programmation. Il permet également à l'utilisateur de faire des demandes à votre API en direct. 

.. _apiary-building-docs :

Building Docs
-------------

Pour construire localement des documents de style Apiary, vous devez installer les outils Apiary CLI. Les instructions complètes sont disponibles `ici. <https://help.apiary.io/tools/apiary-cli/>`_

Une fois qu'il est installé, naviguez dans le répertoire contenant votre fichier ``.apib`` et exécutez : :

  apiary preview --path="monfichier.apib" --output="monfichier.html"

Ceci validera votre fichier ``.apib`` et créera le fichier HTML. Vous pouvez alors visualiser le document dans votre navigateur.
