Introduction à AsciiDoc
========================

Qu'est-ce qu'AsciiDoc ?
-----------------

`AsciiDoc <http://asciidoc.org>`_ est un format de document texte qui a été explicitement conçu en tenant compte des besoins de l'édition, à la fois imprimée et web. Il prend en charge tous les éléments structurels nécessaires à la rédaction de notes, de documentation, d'articles, de livres, d'ebooks, de diaporamas, de pages web, de manuels techniques et de blogs. AsciiDoc est utilisé dans les générateurs de sites statiques comme `Antora <https://antora.org>`_.

AsciiDoc est hautement configurable : à la fois la syntaxe du fichier source AsciiDoc et les balises de sortie backend (qui peuvent être presque n'importe quel type de balisage SGML/XML) peuvent être personnalisés et étendus par l'utilisateur.

Les fichiers AsciiDoc peuvent être traduits dans de nombreux formats, notamment HTML, PDF, EPUB, DocBook, page de manuel. Certains sites web, comme GitHub, rendent les fichiers AsciiDoc directement en HTML.

En 2013, le projet Asciidoctor a été lancé. Il s'agissait d'un effort pour apporter une chaîne d'outils de publication complète et accessible, centrée sur la syntaxe AsciiDoc, à un éventail croissant d'écosystèmes, notamment Ruby, JavaScript et la JVM.

Pourquoi utiliser AsciiDoc ?
-----------------

AsciiDoc est un langage de balisage léger qui vous aide à vous concentrer sur la rédaction de contenu plutôt que d'être distrait par des traitements de texte complexes, d'enterrer le contenu dans des schémas XML comme DocBook, ou de vous battre avec des éditeurs WYSIWYG pointilleux. Avec AsciiDoc, vous pouvez oublier la mise en page, la composition, le style (et même certains aspects sémantiques) et vous contenter d'écrire.

    Vous écrivez un document AsciiDoc de la même manière que vous écririez un document texte normal. Il n'y a pas de balises ou de notations de format bizarres. Les fichiers AsciiDoc sont conçus pour être visualisés, édités et imprimés directement ou traduits dans d'autres formats de présentation.

Ce qui fait vraiment d'AsciiDoc le bon investissement, c'est que sa syntaxe a été conçue pour être étendue en tant que fonctionnalité de base. Cette extensibilité signifie non seulement qu'AsciiDoc a beaucoup plus à offrir, avec une marge de progression, mais aussi qu'il remplit l'objectif de garantir que votre contenu est réutilisable au maximum.

Comment utiliser AsciiDoc ?
--------------------

Paragraphes
~~~~~~~~~~

Les paragraphes ne nécessitent pas de balisage particulier dans AsciiDoc. Un paragraphe est simplement une ou plusieurs lignes de texte consécutives.

Pour commencer un nouveau paragraphe, il faut le séparer par au moins une ligne blanche. Les retours à la ligne à l'intérieur d'un paragraphe ne sont pas affichés.

Formatage du texte
~~~~~~~~~~~~~~~

: :

    bold *constrained* & **un**constrained
    
    italique _constrained_ & __un__constrained
    
    gras italique *_constrained_* & **__un__**constrained
    
    monospace `constrained` & `un``constrained
    
    monospace bold `*constrained*` & `**un**``constrained
    
    monospace italic `_constrained_` & `__un__``constrained
    
    monospace bold italic `*_constrained_*` & ``**__un__**``constrained

Titres des sections (en-têtes)
~~~~~~~~~~~~~~~~~~~~~~~~~

Les titres sont créés à l'aide de signes égaux suivis d'un espace. Le nombre de signes égaux correspond au niveau de l'en-tête dans la sortie HTML. Par exemple, le niveau de section 1 devient un titre <h2>:: :

    = Titre du document (niveau 0)

    == Titre de section de niveau 1

    === Titre de section de niveau 2

    ==== Titre de section de niveau 3

    ===== Titre de section de niveau 4

    ====== Titre de section de niveau 5

    == Un autre titre de section de niveau 1

En-têtes
~~~~~~~

Les en-têtes dans AsciiDoc sont facultatifs.
L'en-tête ne peut pas contenir de lignes vides et doit être décalé du contenu d'au moins une ligne vide: :

    = Titre de mon document

    Mon document fournit...

: :

    = Titre de mon document
    Rédacteur du document <doc.writer@asciidoctor.org>

    Mon document fournit...

Listes
~~~~~

Listes non ordonnées: :

    * Edgar Allen Poe
    * Sheri S. Tepper
    * Bill Bryson

    - Edgar Allen Poe
    - Sheri S. Tepper
    - Bill Bryson

    * Niveau 1
    ** niveau 2
    *** niveau 3
    **** niveau 4
    ***** niveau 5
    * niveau 1

Listes ordonnées : :

    . étape 1
    . Étape 2
    . Étape 3 .

    . Étape 1
    . Étape 2 .
    .. Étape 2a
    .. Étape 2b
    . Étape 3

    . niveau 1
    ... niveau 2
    ... niveau 3
    .... niveau 4
    ..... niveau 5
    . niveau 1

Liste mixte : :

    Systèmes d'exploitation : :
    Linux:: :
        . Fedora
        * Bureau
        . Ubuntu
        * Desktop
        * Serveur
    BSD:: :
        . FreeBSD
        . NetBSD

    Fournisseurs de cloud :: :
    PaaS : : :
        . OpenShift
        . CloudBees
    IaaS :: :
        . Amazon EC2
        . Rackspace

Liste de contrôle: :

    * [*] vérifié
    * [x] également vérifié
    * [ ] non vérifié
    * élément normal de la liste

Liens
~~~~~

Externe : :

    https://asciidoctor.org - automatique !

    https://asciidoctor.org [Asciidoctor]

    https://github.com/asciidoctor [Asciidoctor @ *GitHub*]

Relatif: :

    link:index.html [Docs]

Ancres en ligne : :

    [[bookmark-a]]Les ancres en ligne permettent de référencer un contenu arbitraire.

    [#bookmark-b]#Les ancres en ligne peuvent être appliquées à une phrase comme celle-ci.#

    anchor:bookmark-c[]Utilisez une référence croisée pour créer un lien vers cet emplacement.

    [[bookmark-d,dernier paragraphe]]L'attribut xreflabel sera utilisé comme texte de lien dans le lien de référence croisée.

Références croisées internes: :

    Voir <<paragraphes>> pour apprendre à rédiger des paragraphes.

    Apprenez à organiser le document en <<titres de section,sections>>.

Images
~~~~~~

Bloc: :

    image::sunset.jpg[]

    image::sunset.jpg [Coucher de soleil]

    Un coucher de soleil en montagne
    [#img-sunset]
    [caption="Figure 1 : ",link=https://www.flickr.com/photos/javh/5448336655]
    image::sunset.jpg [Coucher de soleil,300,200]

En ligne: :

    Cliquez sur image:icons/play.png [Play, title="Play"] pour que la fête commence.

    Cliquez sur image:icons/pause.png [title="Pause"] lorsque vous avez besoin d'une pause.

    image:sunset.jpg [Sunset,150,150,role="right"] Quel beau coucher de soleil !

Code source
~~~~~~~~~~~

Bloc de code avec titre et coloration syntaxique : :

    .app.rb
    [source,ruby]
    ----
    Requiert 'sinatra'.

    get '/hi' do
    "Hello World !"
    fin
    ----

Bloc de code avec callouts: :

    [source,ruby]
    ----
    nécessite 'sinatra' // <1>

    get '/hi' do // <2>
    "Hello World !" // <3>
    fin
    ----
    <1> Importation de la bibliothèque
    <2> Mappage d'URL
    <3> Corps de la réponse HTTP


Tables
~~~~~~

Tableau avec un titre, trois colonnes, un en-tête et deux rangées de contenu: :

    .Titre de la table
    |===
    |Nom de la colonne 1 |Nom de la colonne 2 |Nom de la colonne 3 

    |Cellule de la colonne 1, ligne 1
    |Cellule de la colonne 2, rangée 1
    |Cellule de la colonne 3, rangée 1

    |Cellule de la colonne 1, rangée 2
    |Cellule de la colonne 2, rangée 2
    |Cellule de la colonne 3, rangée 2
    |===

Admonitions
~~~~~~~~~~~

AsciiDoc fournit cinq étiquettes de style admonition prêtes à l'emploi : :

    NOTE : Veuillez noter que...

    TIP : Un conseil de pro...

    IMPORTANT : N'oubliez pas...

    AVERTISSEMENT : Faites attention à...

    ATTENTION : Assurez-vous que...

Les admonitions peuvent également encapsuler tout contenu de bloc: :

    [IMPORTANT] 
    Nourrir les loups-garous
    ==== 
    Bien que les loups-garous soient des membres robustes de la communauté, gardez à l'esprit les préoccupations diététiques suivantes :

    . Ils sont allergiques à la cannelle.
    . Plus de deux verres de jus d'orange en 24 heures les font hurler en harmonie avec les alarmes et les sirènes.
    . Le céleri les rend tristes.
    ====

Table des matières
~~~~~~~~~~~~~~~~~

Document avec ToC: :

    = Guide du rédacteur d'AsciiDoc
    Doc Writer <doc.writer@asciidoctor.org>
    v1.0, 2019-08-01
    :toc :

Document avec TdC positionné à droite : :

    = AsciiDoc Writer's Guide
    Doc Writer <doc.writer@asciidoctor.org>
    v1.0, 2014-08-01
    :toc : droite

Inclure les fichiers
~~~~~~~~~~~~~

: :

    = Documentation de référence
    Développeur principal

    Ceci est la documentation du projet X.

    include::basics.adoc[]

    include::installation.adoc[]

    include::example.adoc[]

    include::https://raw.githubusercontent.com/asciidoctor/asciidoctor/master/README.adoc[]


Ressources
---------
* `AsciiDoc <http://asciidoc.org>`_ 
* `AsciiDoc Cheatsheet <https://powerman.name/doc/asciidoc>`_
* `Asciidoctor <https://asciidoctor.org>`_
* `AsciiDoctor Référence rapide à la syntaxe <https://asciidoctor.org/docs/asciidoc-syntax-quick-reference/>`_
