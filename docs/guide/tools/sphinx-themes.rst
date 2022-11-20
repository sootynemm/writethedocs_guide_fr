======================
Introduction à Sphinx
======================

Philosophie
----------

`Sphinx`_ est ce que l'on appelle un générateur de documentation.
Cela signifie qu'il prend un tas de fichiers sources en texte brut,
et génère un tas d'autres choses géniales, principalement du HTML.
Pour notre cas d'utilisation, vous pouvez le considérer comme un programme qui prend du texte brut
au format `reStructuredText`_, et produit du HTML.

.. _reStructuredText : http://sphinx-doc.org/rest.html

: :

    reST -> Sphinx -> HTML

Donc, en tant qu'utilisateur de Sphinx, votre travail principal sera d'écrire ces fichiers texte.
Cela signifie que vous devriez être un minimum familier avec `reStructuredText`_ en tant que langage.
en tant que langage.
Il est similaire à Markdown à bien des égards.
Il est beaucoup plus puissant que Markdown,
mais avec cette puissance vient une augmentation
complexité.
Sachez juste que certaines syntaxes maladroites vous permettent de faire des choses plus intéressantes
plus intéressantes plus tard.
En particulier, il est extensible : il a une façon formelle d'ajouter des balises
`directives`_ qui permettent une analyse plus sophistiquée. 
Par exemple, Sphinx inclut des directives pour relier la documentation de 
modules, classes et méthodes au code correspondant.

Installation de Sphinx
-----------------

La première étape pour se lancer est d'installer `Sphinx`_.
Sphinx est un projet Python, il peut donc être installé comme toute autre bibliothèque Python.
Plusieurs systèmes d'exploitation (Mac OS X, les principales versions de Linux/BSD) ont Python pré-installé,
donc vous n'aurez qu'à exécuter : :

    sudo pip install Sphinx

Les instructions pour installer Python et Sphinx sous Windows peuvent être trouvées sur la page `Sphinx install`_.

... note : : Les utilisateurs avancés peuvent installer ceci dans un virtualenv s'ils le souhaitent.


Mise en route
---------------

Vous voudrez lire le guide `Sphinx Getting Started`_,
car il fournit une introduction à beaucoup d'idées de base. Si vous utilisez
l'outil ``sphinx-quickstart`` décrit ici, il créera un projet
un exemple de projet avec la structure standard suivante : :

    projet/
        docs/
            conf.py
            index.rst
            Makefile

Nous avons un répertoire "docs" de premier niveau dans le répertoire principal du projet.
A l'intérieur de celui-ci se trouve :

``index.rst`` :
    C'est le fichier d'index pour la documentation, ou ce qui vit dans le répertoire ``/``.
    Il peut être considéré comme une page d'accueil qui contient des sujets enfants
    vers lesquels les utilisateurs peuvent naviguer. Il contient normalement une `table des
    table des matières`_ qui lie les autres sujets de la documentation.

``conf.py`` : qui permet de personnaliser la sortie.
    Dans la plupart des cas, il ne devrait pas avoir besoin d'être modifié.

``Makefile`` : Il est livré avec sphinx,
    et est l'interface principale pour le développement local,
    mais ne devrait pas être modifié.

D'autres fichiers ``*.rst`` pour des sous-sections spécifiques de la documentation.

Structure de la table des matières
------------------------------------------

La méthode pour spécifier une structure de table des matières (TOC) dans
Sphinx est quelque peu inhabituelle. Au lieu d'un fichier maître qui contient la
structure hiérarchique de la table des matières pour l'ensemble du projet, vous devrez
d'inclure des directives `toctree`_ dans chaque sujet parent qui a des sujets enfants.
enfants. Sphinx déduira alors la structure globale de la Table des Matières à partir des directives ``toctree``.
dans les fichiers individuels.

Par exemple, le fichier ``index.rst`` dans le dossier de votre projet peut contenir
la directive toctree suivante : :

   .. toctree: :

      TopLevel1
      Niveau supérieur 2

Cela indique qu'il existe deux sujets de premier niveau. Si vous voulez que le sujet
TopLevel1`` contienne des sujets enfants, alors vous insérez la directive
directive ``toctree`` suivante dans TopLevel1: :

  .. toctree: :

     Enfant1
     Enfant 2
     Enfant3
 
Différents thèmes Sphinx auront différentes façons d'afficher la table des matières
dans la barre latérale. Vous pouvez également configurer l'affichage ou non de la directive
toctree en tant que mini-toc dans le sujet lui-même, en ajoutant une option
option ``:hidden:`` à la directive ``toctree`'.
     
Rédaction de la documentation
------------

L'endroit où vous écrirez votre documentation variera en fonction de la façon dont le projet est
projet.
Généralement, les sujets principaux seront placés dans un fichier bien nommé dans le
répertoire docs de premier niveau.
Si un sujet devient plus important, il peut être réparti en plusieurs fichiers dans un répertoire.
répertoire.
Lorsque vous écrivez un document, vérifiez qu'il n'y a pas déjà une place pour lui dans le projet.
le projet, sinon n'hésitez pas à commencer un nouveau fichier.

... avertissement : : Si vous faites un nouveau fichier, assurez-vous qu'il est inclus dans un
	     ``toctree`` dans un fichier qui est dans la Table des Matières. Lorsque
	     vous construisez la documentation, Sphinx affichera un
	     avertissement pour chaque document qui n'est pas dans la table des matières.


reStructuredText
~~~~~~~~~~~~~~~~

Pour écrire une documentation agréable à lire, vous devez avoir une compréhension de base du langage RST.
compréhension de base du langage RST.
Le `reStructuredText Primer`_ est un bon endroit pour commencer à lire, et il couvre la plupart de la syntaxe dont vous aurez besoin.
couvre la plupart de la syntaxe dont vous aurez besoin.
Les parties principales dont vous aurez besoin au début sont :

* **Marquage en ligne**
* **Code source**
**Hyperliens**
**Sections**
* **Directives**

... note : : Vous pouvez visionner en direct RST sur le web : http://rst.ninjs.org/
          . Notez qu'il ne comprendra pas les balises spécifiques à Sphinx.

N'hésitez pas à jouer un peu avec RST pour être sûr de comprendre son fonctionnement.
son fonctionnement.

. avertissement : : RST est sensible aux espaces blancs par endroits.
    S'il se comporte bizarrement, assurez-vous que vous indentez les lignes qui font partie du
    même contenu de manière similaire.

.. _Sphinx : http://sphinx-doc.org/
.. _En-têtes : http://sphinx.pocoo.org/rest.html#sections
.. _Guide de démarrage de Sphinx : http://www.sphinx-doc.org/en/master/usage/quickstart.html
.. _Primaire du texte structuré : http://sphinx.pocoo.org/rest.html#rst-primer
.. _Page d'installation de Sphinx : http://sphinx-doc.org/install.html
.. _table des matières : http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#table-of-contents
.. _directives toctree : http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#table-of-contents
.. _directives : http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#


Construction de la documentation
-------------

Une fois que vous avez écrit votre documentation et que vous voulez la transformer en HTML,
c'est assez simple. Exécutez simplement : :

    # dans le répertoire docs/ de premier niveau.
    make html

Cela devrait exécuter Sphinx dans votre shell, et produire du HTML.
A la fin, il devrait dire quelque chose à propos des documents qui sont prêts dans le répertoire
``_build/html``.
Vous pouvez maintenant les ouvrir dans votre navigateur en tapant : :

    open_build/html/index.html
