Tester votre documentation
==========================

Tester votre documentation vous permet de vous assurer qu'elle est dans un état cohérent.
Cela permet à vos utilisateurs de vivre une meilleure expérience,
et réduit le stress lié aux problèmes courants en tant que rédacteur.

Cet `article <https://opensource.com/business/15/7/continuous-integration-and-continuous-delivery-documentation>`_ d'Anne Gentle est un bon point de départ pour comprendre ce concept.

Intégration continue
----------------------

Les tests les plus utiles sont exécutés sur chaque commit de votre projet.
C'est ce qu'on appelle **l'intégration continue**,
et c'est une pratique courante dans le monde du développement logiciel.

Nous recommandons de vérifier les outils suivants pour commencer :

* `Travis CI <https://travis-ci.org>`_ (GitHub uniquement, gratuit pour l'open source).
* `AppVeyor <https://www.appveyor.com/>`_ (support Windows, gratuit pour l'open source)

Erreurs de construction
------------

La vérification automatisée la plus simple à faire est de s'assurer que votre documentation se construit
correctement. Cela nécessite simplement d'exécuter votre outil de documentation et de vérifier
qu'il a correctement construit votre documentation.

La plupart des outils renverront un *code d'erreur* de 0 si le processus est réussi. Ceci
Cela signifie que vous devriez pouvoir faire une construction normale de votre outil, et votre
outil de test saura si le processus est réussi ou non.

Si votre outil de construction possède un mode *picky* qui signale les avertissements qui *pourraient* être
problématiques ainsi que les erreurs, il pourrait être judicieux de l'activer, mais vous
mais vous voudrez vous assurer que votre documentation est en bon état avant de le faire.

* Sphinx a un mode `nitpicky <https://www.sphinx-doc.org/en/stable/config.html#confval-nitpicky>`_.
* Jekyll a un mode strict <https://jekyllrb.com/docs/configuration/#liquid-options>`_.

Test des liens
------------

S'assurer que tous les liens hypertextes de vos docs fonctionnent est un très bon point de départ.
Cela permet de s'assurer que vos utilisateurs ne se retrouvent pas dans des impasses,
et c'est assez simple en termes d'automatisation.

Vous pouvez soit :

* Utiliser un outil fourni avec vos outils de documentation
* traiter votre documentation rendue comme un site web normal et utiliser un vérificateur de liens de sites web.

Voici les outils que nous connaissons et qui permettent de vérifier correctement les liens :

Sphinx
~~~~~~

Sphinx est livré avec un ``linkcheck`` `builder <https://www.sphinx-doc.org/en/stable/builders.html>`_ par défaut.
Vous pouvez le lancer avec un simple : :

    make linkcheck

Sa sortie ressemble à quelque chose comme ceci :

.. image: : /_static/img/guide/sphinx-linkcheck.png

Jekyll
~~~~~~

Jekyll possède quelques plugins qui prennent en charge la vérification des liens :

* https://github.com/endymion/link-checker

HTMLProofer
~~~~~~~~~~~

`HTMLProofer <https://github.com/gjtorikian/html-proofer>`_ vérifie les liens en
HTML, ainsi que les images, les titres et la validité des balises.

Vérification et linting des guides de style
----------------------------------

Les linters sont des outils qui vérifient automatiquement des règles spécifiques par rapport à votre code ou à votre documentation.
documentation. Ces outils sont utiles pour appliquer un guide de style ou pour détecter les problèmes de marque les plus courants.
les erreurs courantes en matière de marque.

Voici quelques liens qui pourraient être intéressants :

* https://blog.mapbox.com/regulating-english-with-retext-mapbox-standard-d79a8158f251
* https://krausefx.com/blog/writing-automated-tests-for-your-documentation


Vale
----

Vale est un linter syntaxique pour la prose, conçu pour la vitesse et l'extensibilité.

https://github.com/errata-ai/vale

Vous pouvez utiliser les styles suivants avec Vale, bien que depuis la v2.0.0, Vale n'inclut plus ces styles par défaut :

* `Proselint <https://github.com/amperser/proselint>`_
* `Write-good <https://github.com/btford/write-good>`_
* `Joblint <https://github.com/rowanmanning/joblint>`_

Vous pouvez également utiliser une implémentation du guide de style d'écriture de Microsoft et du guide de style de la documentation des développeurs de Google avec Vale. Vous pouvez trouver ces styles dans le dépôt suivant : https://github.com/errata-ai/styles.

Pour configurer Vale, suivez les instructions du fichier README. Si nécessaire, installez
binaire *vale* en tant qu'exécutable dans votre $PATH, afin de pouvoir exécuter *vale* directement
de la ligne de commande. Par exemple, sur les systèmes UNIX/Linux, vous pouvez copier vale
dans le répertoire /usr/local/bin.

Après avoir installé vale, exécutez les commandes suivantes pour vérifier la bonne installation :

$ `vale`

$ `vale dc`

Si vous voyez du JSON vide dans la sortie de la deuxième commande, vous avez réussi à
installé Vale avec succès.

Maintenant pour configurer Vale, vous aurez besoin d'un fichier de configuration .vale ou .vale.ini. Pour quelques
exemples, voir

* https://github.com/writethedocs/www/blob/master/.vale.ini
* https://github.com/cockroachdb/docs/blob/master/.vale.ini
* https://github.com/linode/docs/blob/develop/.vale.ini

Bien qu'il soit possible d'installer le fichier de configuration Vale à différents endroits,
il peut être plus pratique de l'installer dans le répertoire racine de votre référentiel
cible, comme indiqué dans les exemples ci-dessus.

Une fois configuré pour votre dépôt, vous devriez être capable de naviguer vers le chemin de votre dépôt
puis exécuter `vale dc` pour confirmer votre configuration.

Vous pouvez alors appliquer Vale comme un linter de grammaire directement à vos fichiers sources, avec
une commande comme :

$ `vale /path/to/someText.md`

Astuce : Vale fonctionne même avec des fichiers XML, comme ceux de DocBook et DITA, à condition que
que vous ayez inclus `*.xml` dans le fichier de configuration de Vale.
