=================================================
Introduction à reStructuredText
=================================================

Qu'est-ce que reStructuredText ?
----------------------------

`reStructuredText <http://docutils.sourceforge.net/rst.html>`_ est un langage de balisage léger qui est utilisé dans les générateurs de sites statiques comme :doc:`Sphinx <../tools/sphinx>`. Il contient des outils robustes pour le balisage sémantique, la réutilisation du contenu et les filtres de contenu pour différents types de sorties. Il est également facilement extensible à l'aide de `directives personnalisées <http://docutils.sourceforge.net/docs/ref/rst/directives.html>`_ que vous pouvez créer vous-même, ce qui vous permet de satisfaire une grande variété de besoins de documentation.

reStructuredText est largement utilisé pour la documentation Python---à la fois pour le `langue Python lui-même <https://docs.python.org/3/tutorial/index.html>`_ et pour les bibliothèques Python.

Pourquoi utiliser reStructuredText ?
----------------------------

reStructuredText est un langage de balisage léger, il est donc plus facile à lire en format texte brut par rapport à des langages de balisage plus lourds comme DITA et d'autres formats basés sur XML. Vous pouvez facilement trouver des éditeurs de texte qui rendent reStructuredText avec une coloration syntaxique et des aperçus en direct, sans avoir à investir dans des outils complexes.

Par rapport à certains autres langages de balisage légers comme :doc:`MarkDown <markdown>`, reStructuredText contient des outils de balisage sémantique plus puissants. `Certains rédacteurs <http://ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/>`_ préfèrent également reStructuredText parce que les normes de balisage sont plus bien définies par rapport à MarkDown.

Comment utiliser reStructuredText
-----------------------------------

Mise en forme du texte principal
~~~~~~~~~~~~~~~~~~~~~~~~~~

Dans reStructuredText, les paragraphes sont des blocs de texte séparés par au moins une ligne blanche. Toutes les lignes du paragraphe doivent être indentées de la même manière.

Le balisage en ligne des styles de police est similaire à celui de MarkDown :

* Utilisez un astérisque (``*text*``) pour l'italique.
* Utilisez deux astérisques (``**text**``) pour les caractères gras.
* Utilisez deux backticks (````text````) pour les échantillons de code.
* Les liens vers des sites externes contiennent le texte du lien et une URL entre crochets, suivis d'un trait de soulignement : "Lien vers Write the Docs <https://www.writethedocs.org/>".

En-têtes
~~~~~~~~~~~~~~~~~~~

Les en-têtes sont délimités par des caractères non alphanumériques comme les tirets, les signes égaux ou les tildes. Utilisez le même caractère pour les en-têtes de même niveau. L'exemple suivant crée un en-tête : :

  ===============
  Chapitre 1
  ===============

S'il est inséré dans le même document, il crée un en-tête de niveau différent:: :

  Section 1.1
  ------------------

Il est acceptable d'avoir un texte souligné uniquement, mais aussi d'avoir un texte souligné et surligné. Si vous utilisez le même caractère non alphanumérique pour des en-têtes soulignés seulement et soulignés et surlignés, ils seront considérés comme étant à des niveaux *différents*.

La rangée de caractères non alphanumériques doit être au moins aussi longue que le texte de l'en-tête.


Listes
~~~~~~~~~~~~~~

Pour les listes énumérées, utilisez un chiffre ou une lettre suivi d'un point, ou suivi d'un crochet droit, ou entouré de crochets: :

  1. Utilisez ce format pour les chiffres de votre liste comme 1., 2., etc.

  A. Utilisez ce format pour les éléments de votre liste comme A., B., etc. Les lettres majuscules et minuscules sont acceptées.

  I. Les chiffres romains sont également acceptés, en majuscules ou en minuscules.

  (1) Les chiffres entre parenthèses sont acceptables.

  1) Il en va de même pour les chiffres suivis d'une parenthèse.

Pour les listes à puces, utilisez l'indentation pour indiquer le niveau d'imbrication d'une puce. Vous pouvez utiliser les caractères " - ", " + " ou " * " comme caractères de puce : :

  * Point de suspension
    
    - puce imbriquée
      
      + encore plus de puces imbriquées

Exemples de code
~~~~~~~~~~~~~~~~~~~

Pour afficher des échantillons de code, ou tout autre texte qui ne doit pas être formaté, terminez le paragraphe précédant l'échantillon de code par deux points de suspension (``::``) et indentez l'échantillon de code: :

  Voici le paragraphe qui précède l'échantillon de code: :

    #un exemple de code


 
Ressources
-------------------

* `A ReStructuredText Primer <http://docutils.sourceforge.net/docs/user/rst/quickstart.html>`_
* `Primaire de ReStructuredText <http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_
* `Cheatsheet <https://github.com/ralsina/rst-cheatsheet>`_
