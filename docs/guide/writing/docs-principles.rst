Principes de documentation
========================

Le développement logiciel bénéficie de `philosophies`_ et de `principes`_ tels que
`DRY`_, `KISS`_, `code reuse`_, et bien d'autres. Grâce à ces normes communément comprises
et acceptées par tous, les développeurs peuvent se tenir et se tenir mutuellement
à produire un code de haute qualité.

.. _philosophies : https://en.wikipedia.org/wiki/Category:Software_development_philosophies
.. _principes : https://en.wikipedia.org/wiki/Category:Programming_principles
.. _SÉCHERESSE : https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
.. _Ne vous répétez pas : https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
.. _KISS : https://en.wikipedia.org/wiki/KISS_principle
.. _Réutilisation du code : https://en.wikipedia.org/wiki/Code_reuse

Cet ensemble de principes vise à définir des normes similaires pour les logiciels
*logiciels qui, lorsqu'ils sont mis en pratique, favorisent un contenu propre et intuitif.
propre et intuitif. L'objectif final est d'enchanter les lecteurs et de leur donner les moyens d'agir en
en rendant l'information plus facile à acquérir.

Aperçu, par composant
----------------------

Toute la documentation
~~~~~~~~~~~~~~~~~

En général, la documentation doit être...

* `Précursoire <#precursoire>`__
* `Participative <#participative>`__

Contenu
~~~~~~~

*Le "contenu" est l'information conceptuelle de la documentation.

**Contenu** doit être...

* `ARID <#arid>`__
* `Skimmable <#skimmable>`__
* `Exemplaire <#exemplaire>`__
* `Consistant <#consistant>`__
* `Current <#current>`__

Sources
~~~~~~~

*Une "source" fait référence à un système utilisé pour stocker et modifier du contenu.
Voici quelques exemples de sources : les fichiers texte écrits avec
reStructuredText ou Markdown, le contenu HTML d'une base de données CMS, l'aide
texte d'aide stocké dans des chaînes de caractères dans le code d'application
d'application, les commentaires de code à assembler ultérieurement dans une documentation formalisée, et d'autres encore*.

Toutes les **sources** doivent être...

* `Nearby <#nearby>`__
* `Unique <#unique>`__


Publications
~~~~~~~~~~~~

*Une "publication" désigne un outil unique et cohérent que les lecteurs utilisent pour consommer de la documentation.
documentation.
Elle peut être statique ou interactive - numérique ou papier. Plusieurs
publications peuvent être créées à partir d'une source unique (comme les versions Web et PDF du même manuel).
d'un même manuel). Bien que cela soit plus rare, plusieurs sources peuvent
être utilisées pour créer une seule publication. D'autres exemples de
publications comprennent : La référence API, la page de manuel, la ligne de commande
``--help``, conseils d'aide dans l'application, tutoriels en ligne,
manuels d'ingénierie internes, et d'autres encore.

Chaque **publication** doit être...

* `Discoverable <#discoverable>`__
* `Addressable <#addressable>`__
* `Cumulatif <#cumulatif>`__
* `Complet <#complete>`__
* `Beautiful <#beautiful>`__

Corps
~~~~

*Un "corps" désigne l'ensemble des publications d'un projet logiciel et de ses sous-projets.
projet et de ses sous-projets*.

Un **corps** de documentation doit être...

*Corps complet <#comprehensive>`__


===============================================================================


En général, la documentation doit être...
--------------------------------------

Précurseur
~~~~~~~~~~

*Commencez à documenter avant de commencer à développer.*

Avant de coder, rédigez les exigences et les spécifications qui servent également de
première version de la documentation. Ces textes auront sans doute besoin d'un peu de
Ces textes auront sans doute besoin d'un peu de nettoyage avant d'être publiés, mais en mettant la documentation en avant,
vous tracez un chemin clair vers l'avant. Une documentation précoce permet également de faciliter
les commentaires des pairs et les décisions de groupe pour guider votre travail. Ce modèle est le
sentiment qui sous-tend la " conception axée sur la documentation <../style-guides#documentation-driven-design>`_.

Participatif
~~~~~~~~~~~~~

*Dans le processus de documentation, incluez tout le monde, des développeurs aux utilisateurs finaux.
utilisateurs finaux.*

Intégrez la documentation dans le flux de travail standard des développeurs, et
développeurs, et cherchez à réduire les silos qui ne sollicitent la documentation que d'un sous-ensemble de
des contributeurs du logiciel. Les développeurs et les ingénieurs sont les personnes
Les développeurs et les ingénieurs sont les personnes qui ont le meilleur accès aux informations demandées.
et les amener à les documenter contribuera à favoriser une *culture* de la documentation.

De même, les "lecteurs" de la documentation (c'est-à-dire les utilisateurs) devraient avoir des moyens clairs de participer à la documentation.
pour s'impliquer dans la documentation. Une bonne première étape consiste à donner aux
lecteurs la possibilité de donner leur avis sous forme de commentaires ou de suggestions.
suggestions. Permettre aux lecteurs de modifier directement la documentation (par exemple, dans un
wiki) peut également être efficace, mais doit être mis en balance avec la nécessité et la capacité de surveillance
la nécessité et la capacité d'une supervision éditoriale.

Encouragez *tout le monde* à devenir un :doc:`documentariste </documentaristes>` !

Le contenu doit être...
--------------------

ARID
~~~~

*Accepter (un peu) de répétition dans la documentation.*

Si vous voulez écrire du bon code, "Ne vous répétez pas". Mais
si vous adhérez strictement à ce principe DRY lorsque vous écrivez de la documentation,
vous n'irez pas très loin. *Une certaine quantité de logique métier décrite par votre code devra être décrite.
votre code devra être décrite *encore une fois* dans votre documentation.

Dans un monde idéal, un système automatisé génèrerait de la documentation à partir du code source du logiciel.
le code source du logiciel, *et* le système serait assez intelligent pour
générer une *bonne* documentation sans aucune entrée supplémentaire.
Malheureusement, nous ne vivons pas (encore) dans ce monde et aujourd'hui, la meilleure documentation est écrite à la main.
documentation est écrite à la main, ce qui signifie que juste en écrivant *toute* documentation, vous vous répétez.
documentation, vous vous répétez. Bien sûr, les "générateurs de documentation" existent et sont utiles.
existent et sont utiles, mais il est important de reconnaître qu'ils nécessitent toujours
qu'ils ont toujours besoin de l'apport des humains pour fonctionner.

.. _générateurs de documentation : http://en.wikipedia.org/wiki/Comparison_of_documentation_generators

L'objectif de *minimiser* les répétitions reste valable ! ARID ne signifie pas
``HUILE`_, d'où le choix du mot. Cela signifie : essayez de garder les choses *aussi sèches que possible*.
mais aussi reconnaître que vous aurez inévitablement besoin d'une certaine quantité d'"humidité"
pour produire de la documentation.

.. _EAU : https://en.wikipedia.org/wiki/Don't\_repeat\_yourself#DRY\_vs\_WET\_solutions

La prise de conscience de cette vérité dérangeante constituera, nous l'espérons, une
de rappeler aux développeurs qu'il est souvent nécessaire de mettre à jour la documentation
de mettre à jour la documentation en même temps que le code.

Ecumable
~~~~~~~~~

*Structurer le contenu pour aider les lecteurs à identifier et à sauter les concepts qu'ils comprennent déjà ou qui ne sont pas pertinents pour eux.
qu'ils comprennent déjà ou qui ne sont pas pertinents pour leurs questions immédiates.
questions immédiates.

L'enfouissement des concepts dans la prose et le verbiage demande plus de temps aux lecteurs qui cherchent des réponses à des questions spécifiques.
Les concepts enfouis dans la prose et le verbiage demandent plus de temps aux lecteurs qui cherchent des réponses à des questions spécifiques. Faites gagner du temps à vos lecteurs en
en écrivant comme un journal et non comme un roman.

Plus précisément :

- Les titres - doivent être descriptifs et concis.
- Les hyperliens doivent être entourés de mots qui décrivent le lien lui-même (jamais de phrases comme "cliquez ici" ou "cette page").
   (jamais de phrases comme "cliquez ici" ou "cette page").
- Les paragraphes et les listes doivent commencer par des concepts identifiables.
   le plus tôt possible.

Exemplaire
~~~~~~~~~

*Incluez (quelques) exemples et tutoriels dans le contenu.

De nombreux lecteurs se tournent d'abord vers les exemples pour trouver des réponses rapides.
Les lecteurs se tournent d'abord vers les exemples pour trouver des réponses rapides, et les inclure leur permettra de gagner du temps. Essayez d'écrire des exemples pour les
cas d'utilisation les plus courants, mais pas pour tout. Trop d'exemples peuvent
rendre la documentation moins `skimmable <#skimmable>`__. En outre, envisagez de
séparer les exemples et les didacticiels des informations de référence plus denses
pour aider davantage les lecteurs à écrémer.

Cohérence
~~~~~~~~~~

*Utilisez un langage et un formatage cohérents dans le contenu.

Plus le nombre d'éditeurs de contenu est élevé, plus le guide de style est important pour faciliter la cohérence.
devient plus important pour faciliter la cohérence. La cohérence permet également de rendre la documentation
`skimmable <#skimmable>`__ et `beautiful <#beautiful>`__.

.. Guide de style : https://www.writethedocs.org/guide/writing/style-guides/

Actuel
~~~~~~~

*Considérez qu'une documentation incorrecte est pire qu'une documentation manquante.
que l'absence de documentation.

Lorsqu'un logiciel évolue plus vite que sa documentation, les utilisateurs en pâtissent.
Maintenez-la à jour.

Faites tout votre possible pour rédiger un contenu qui ne dépend pas de la version et qui a donc moins besoin de maintenance.
moins besoin de maintenance. Par exemple, généralisez les numéros de version des
logiciels lorsqu'ils apparaissent dans les didacticiels (par exemple, l'extraction d'une archive de code source avec le numéro de version dans le didacticiel).
tarball avec le numéro de version dans le nom du fichier).

Sachez également que certains utilisateurs continueront à utiliser des versions plus anciennes de votre logiciel et auront donc besoin de versions plus anciennes de votre logiciel.
versions de votre logiciel, et auront donc besoin d'anciennes versions de votre documentation. Les plateformes de documentation appropriées de
Les plates-formes de documentation appropriées s'adapteront à ces besoins.

Les sources doivent être...
--------------------

Près de
~~~~~~

*Stocker les sources aussi près que possible du code qu'elles documentent*.

Fournir aux développeurs des systèmes qui leur permettent d'effectuer facilement des
documentation en même temps que leurs modifications de code. Une façon de le faire est de stocker le contenu de la documentation dans des
documentation dans des blocs de commentaires au sein du code source de l'application. Une autre solution consiste à
Une autre solution consiste à le stocker dans des fichiers texte distincts, mais dans le même référentiel que le code source de l'application.
code source de l'application. Dans tous les cas, l'objectif est de fusionner (autant que possible) les flux de travail de développement et de documentation.
possible) les flux de travail pour le développement et la documentation.

Unique
~~~~~~

*Éliminer le chevauchement de contenu entre des sources distinctes.*

Le stockage du contenu dans différentes sources est acceptable, à condition que la portée de chaque source soit clairement définie et disjointe de celle des autres.
chaque source est clairement définie et disjointe des autres sources. L'objectif
ici est d'empêcher toute maintenance parallèle (ou pire - *absence* de maintenance) de la même information dans plusieurs sources.
maintenance) de la même information dans plusieurs sources.

Chaque publication doit être...
-----------------------------

Découvrable
~~~~~~~~~~~~

*Fournir intuitivement les utilisateurs vers les publications par tous les chemins probables.
probables.*

Essayez d'identifier tous les endroits où l'utilisateur pourrait chercher de la documentation,
et dans tous ces endroits, insérez des pointeurs utiles pour qu'il la trouve.
Il n'est pas nécessaire que la documentation *existe* à tous ces endroits, il suffit de l'indiquer.
seulement des pointeurs vers elle.

Si un manuel utilisateur est publié dans les bois, et que personne n'est là pour le lire, existe-t-il ?
il existe ? La "découvrabilité" dit "non".

.. _Discoverability : https://en.wikipedia.org/wiki/Discoverability

Adressable
~~~~~~~~~~~

*Fournir aux lecteurs des adresses qui renvoient directement au contenu à un niveau granulaire*.
niveau granulaire*.

La possibilité de faire référence à des sections *spécifiques* au sein d'un corpus de
documentation facilite une communication productive sur la
documentation, même avec soi-même. Ces adresses peuvent prendre la forme
d'URL, de numéros de page ou d'autres formes, selon le support de publication.
support de publication. Les lecteurs peuvent souhaiter marquer certaines sections d'un signet, les partager avec d'autres utilisateurs ou faire part de leurs commentaires aux auteurs.
d'autres utilisateurs, ou fournir un retour d'information aux auteurs. Plus cette capacité est granulaire
plus granulaire, et plus elle est facile d'accès, mieux c'est.

Cumulatif
~~~~~~~~~~

*Le contenu doit être ordonné de manière à couvrir d'abord les concepts préalables.

Un lecteur peut-il suivre l'ensemble de votre documentation, de manière linéaire, du début à la fin, sans être dérouté ?
du début à la fin sans se tromper ? Si oui, la documentation est
parfaitement "cumulative", ce qui est formidable, mais pas toujours possible. C'est
C'est un objectif à atteindre, en particulier dans les didacticiels et les exemples. Si vous
Si vous avez séparé vos tutoriels et exemples de la documentation de référence
documentation de référence, placez les didacticiels et les exemples en premier. Ensuite, le contenu
dans la section des informations de référence peut être classé par ordre alphabétique
ou par ordre topique sans tenir compte des besoins préalables.

L'objectif de l'ordre cumulatif n'est pas d'encourager les lecteurs à consommer votre documentation de manière linéaire.
votre documentation de manière linéaire, mais plutôt de les aider à affiner leur recherche d'informations lorsqu'ils doivent combler des lacunes.
recherche d'informations pour combler les lacunes de leurs connaissances. Si un
Si un lecteur arrive avec une *certaine* connaissance du logiciel et commence à lire
la documentation à 25 %, il est probable qu'il revienne en arrière lorsqu'il est
confus.

Complète
~~~~~~~~

*Dans chaque publication, couvrez les concepts dans leur intégralité, ou pas du tout.*

Imaginez la documentation d'un logiciel comme le plan d'un quartier. Si
Si la carte affiche des routes, les lecteurs s'attendront à ce qu'elle affiche *toutes* les routes (qui existent et sont du même *type* que celui affiché).
(qui existent et sont du même *type* que celui qui est affiché). Peut-être que la
carte n'affiche pas les *chemins de fer*, par exemple. Ainsi, un lecteur
s'approchant de la carte pour chercher des chemins de fer n'en trouvera aucun et cherchera alors une
une autre carte - mais la carte est toujours "complète", même avec cette
cette lacune. "Complète" ne signifie pas que la carte doit décrire *toutes* les caractéristiques du terrain.
caractéristiques du territoire. Cela signifie simplement que, pour les
caractéristiques qu'elle choisit de décrire, elle doit décrire *toutes* d'entre elles.
toutes* ces caractéristiques. Une carte qui affiche cinquante des cent bouches d'incendie d'un quartier est *mauvaise* que celle qui affiche cinquante des cent bouches d'incendie.
quartier est *mauvaise* qu'une carte qui n'en affiche aucune.

A titre d'exemple, ``iconv`` est un outil en ligne de commande pour travailler avec les
les encodages de caractères. Sa page d'accueil couvre *toutes* les options disponibles.
de ses options disponibles mais *aucun* des encodages de caractères possibles
acceptés comme valeurs de ces options. A la place, la page de manuel indique à l'utilisateur
l'utilisateur de lancer ``iconv -l`` pour produire une liste de codages de caractères. Dans
Dans cet exemple, la page de manuel et la liste sont des publications distinctes, toutes deux complètes, ce qui est une bonne chose.
qui sont toutes deux complètes, ce qui est bien !

.. _man page : http://man7.org/linux/man-pages/man1/iconv.1.html

La publication d'une documentation partiellement achevée doit être faite avec précaution. Pour
d'éviter d'induire les lecteurs en erreur, faites tout votre possible pour indiquer clairement, dès le départ
qu'un concept particulier n'est que partiellement couvert.

Magnifique
~~~~~~~~~

*Le style visuel doit être intentionnel et esthétiquement plaisant.

L'esthétique n'est pas importante pour tout le monde, mais (consciemment ou non) certains lecteurs auront du mal à se sentir à l'aise dans une documentation.
mais (consciemment ou non) certains lecteurs auront du mal à se sentir à l'aise dans une documentation qui n'accorde pas d'attention au style visuel.
l'attention portée au style visuel. Même dans la documentation en mode texte, comme
``--help``, le style visuel est toujours présent sous la forme de l'espacement
et de majuscules. Si le style visuel n'est pas important pour vous personnellement,
alors pensez à demander des améliorations stylistiques à d'autres personnes pour qui il l'est.
l'est.

Un corps de documentation doit être...
---------------------------------

Complet
~~~~~~~~~~~~~

*S'assurer qu'ensemble, toutes les publications du corps de la documentation répondent à toutes les questions que l'utilisateur est susceptible de se poser.
peuvent répondre à toutes les questions que l'utilisateur est susceptible de se poser.*

Nous ne pourrons jamais créer suffisamment de documentation pour satisfaire *toutes* les questions,
Nous ne pourrons jamais créer suffisamment de documentation pour répondre à *toutes* les questions, même les plus obscures, que peuvent se poser les utilisateurs.
mais satisfaire les questions *probables* est certainement réalisable et devrait donc être l'objectif
d'un corpus de documentation. Le terme "probable" est certes flou, mais il est aussi relatif.
mais il est également relatif, ce qui signifie qu'un corpus de documentation qui
répond à des questions très peu probables et ne répond pas à des questions probables.
est quelque peu déséquilibré.

La réponse à certaines questions peut nécessiter que l'utilisateur lise plusieurs publications, ce qui n'est pas grave.
