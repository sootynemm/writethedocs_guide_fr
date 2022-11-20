Guide de rédaction de la documentation pour les débutants
===========================================

. note: : Ceci est un compte-rendu d'une `Présentation <https://speakerdeck.com/ericholscher/writing-docs-a-beginners-guide-to-writing-documentation>`_ .
          Veuillez faire part de vos commentaires à `@ericholscher`_.
          Vous pouvez voir la source sur `GitHub`_.

.. _@ericholscher : http://twitter.com/ericholscher
.. _GitHub : https://github.com/writethedocs/www/blob/master/docs/guide/writing/beginners-guide-to-docs.rst

..

	| La caméra fait un panoramique de la scène à gauche.
	| Elle montre un éditeur de texte, ouvert sur une page blanche.
	| Une personne courbée devant, la tête contre le bureau.

La scène ci-dessus est bien connue de tous ceux qui écrivent pour vivre ;
les émotions mélangées d'une page blanche.
Pleine d'excitation, la fraîcheur d'un nouveau départ.
Mais aussi de désespoir : par où commencer ?

Je suis ici pour empêcher cette scène de se produire.

Voici un guide pour documenter votre premier projet.
La première fois est toujours la plus difficile,
et j'espère que ce guide vous aidera à vous engager sur le bon chemin.
A la fin,
vous devriez avoir un projet qui est prêt à être publié.

N'hésitez pas à lire ce document en entier,
ou simplement l'utiliser comme référence.

.. _pourquoi :

Pourquoi écrire des documents
--------------

Vous utiliserez votre code dans 6 mois
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Le code que vous avez écrit il y a 6 mois est souvent impossible à distinguer du code que quelqu'un d'autre a écrit.
Vous regarderez un fichier avec un sentiment de souvenir ému.
Puis un sentiment sournois de pressentiment,
sachant que quelqu'un de moins expérimenté, de moins sage, l'a écrit.

En accomplissant cet acte désintéressé de démêler des choses qui étaient évidentes ou intelligentes il y a des mois,
vous commencerez à avoir de l'empathie pour vos utilisateurs.
Si seulement j'avais écrit pourquoi j'avais fait ça.
La vie serait tellement plus simple.
La documentation vous permet de transférer le "pourquoi" derrière le code.
De la même manière que les commentaires de code expliquent le *pourquoi*,
et non le *comment*,
la documentation sert le même objectif.

... sidebar: :  Sidebar sur l'open source

	Il y a un sentiment magique qui se produit lorsque vous publiez votre code.
	Il se manifeste de différentes manières, mais il vous frappe toujours de la même façon.
	*Quelqu'un utilise mon code?!*
	Un mélange de terreur et d'excitation.

		| J'ai fait quelque chose de valeur !
		| Et si ça casse ?
		| Je suis un vrai développeur open source !
		| Oh mon Dieu, quelqu'un d'autre utilise mon code...

	La rédaction d'une bonne documentation contribuera à atténuer certaines de ces craintes.
	Une grande partie de cette peur vient du fait de mettre quelque chose au monde.
	Ma citation préférée à ce sujet est quelque chose de ce genre :

		| La peur est ce qui arrive quand vous faites quelque chose d'important.
		| Si vous faites un travail qui n'est pas effrayant,
		| il n'améliore ni toi ni le monde.

	Félicitations pour avoir peur !
	Cela signifie que tu fais quelque chose d'important.

Tu veux que les gens utilisent ton code
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Vous avez écrit un morceau de code,
et vous l'avez diffusé dans le monde.
Vous l'avez fait parce que vous pensez que d'autres personnes pourraient le trouver utile.
Cependant,
les gens ont besoin de comprendre pourquoi votre code pourrait leur être utile,
avant de décider de l'utiliser.
La documentation indique aux gens que ce projet est pour eux.

	| Si les gens ne savent pas pourquoi votre projet existe,
	| ils ne l'utiliseront pas.
	| Si les gens ne savent pas comment installer votre code,
	| ils ne l'utiliseront pas.
	| Si les gens ne savent pas comment utiliser votre code,
	| ils ne l'utiliseront pas.

Il y a un petit nombre de personnes qui sont prêtes à utiliser n'importe quel code existant.
C'est un nombre infiniment petit de personnes,
comparé aux personnes qui utiliseront votre code s'il est correctement documenté.
Si vous aimez vraiment votre projet,
documentez-le,
et laissez d'autres personnes l'utiliser.


Vous voulez que les gens vous aident
~~~~~~~~~~~~~~~~~~~~~~~~~~~

L'open source est une chose magique, non ?
Vous publiez un code,
et les gnomes du code viennent et l'améliorent pour vous.

Pas tout à fait.

Il y a beaucoup de façons dont l'open source est incroyable,
mais il n'existe pas en dehors des lois de la physique.
Vous devez y mettre du travail,
pour obtenir du travail.

	| Vous n'obtenez des contributions qu'après avoir fourni beaucoup de travail.
	| On ne reçoit des contributions qu'après avoir eu des utilisateurs.
	| Vous n'obtiendrez des contributions que si vous disposez d'une documentation.

La documentation fournit également une plate-forme pour vos premières contributions.
Beaucoup de gens n'ont jamais contribué auparavant,
et les changements de documentation sont beaucoup moins effrayants que les changements de code.
Si vous n'avez pas de documentation,
vous passerez à côté de toute une catégorie de contributeurs.

Vous voulez que votre code soit meilleur
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il est très facile d'avoir une idée dans la tête qui semble parfaite,
mais l'acte de mettre des mots sur le papier exige une distillation de la pensée qui n'est peut-être pas si facile.

La rédaction de la documentation améliore la conception de votre code.
Le fait de coucher sur papier vos décisions en matière d'API et de conception vous permet d'y réfléchir de manière plus formelle.
Un effet secondaire intéressant est que cela permet aux gens de contribuer à un code qui respecte également vos intentions initiales.

Vous voulez devenir un meilleur rédacteur
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

La rédaction de documentation est une forme d'écriture différente de celle que la plupart des gens connaissent.
La rédaction technique est un art qui ne vient pas naturellement.
La rédaction de documentation vous permettra de devenir un meilleur rédacteur technique,
ce qui est une compétence utile pour un programmeur.

L'écriture devient également plus facile avec le temps.
Si vous n'écrivez pas pendant plusieurs mois,
il est beaucoup plus difficile de recommencer à écrire.
Le fait de documenter vos projets vous permettra de continuer à écrire à une cadence raisonnable.

Commencer simplement est le meilleur moyen d'obtenir des résultats concrets.
Je vais vous présenter un chemin bien pavé à parcourir,
et une fois que vous aurez l'idée de base,
vous pourrez élargir votre champ d'action.
Les outils doivent être puissants et faciles à utiliser.
Cela permet d'éliminer les obstacles qui empêchent de mettre réellement des mots sur la page.

.. _markup_languages :

.. sidebar: : Encadré sur les langages de balisage.

   Les exemples de ce document sont à la fois valides `Markdown`_ et `reStructuredText`_.
   reStructuredText est un peu plus difficile à utiliser,
   mais il est plus puissant.
   Je vous recommande d'essayer les deux,
   et de décider lequel vous voulez utiliser à l'avenir.

.. _reStructuredText : https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _Markdown : http://daringfireball.net/projects/markdown/

Texte brut contrôlé par version
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

En tant que programmeurs, nous vivons dans un monde de texte brut.
Nos outils de documentation ne devraient pas faire exception.
Nous voulons des outils qui transforment le texte brut en un joli HTML.
Nous disposons également de certains des meilleurs outils disponibles pour le suivi des modifications apportées aux fichiers.
Pourquoi renoncerions-nous à utiliser ces outils lors de la rédaction de la documentation ?
Ce flux de travail est puissant et familier aux développeurs.


Exemple de base
~~~~~~~~~~~~~

: :

	Ressources
	---------

	* Documentation en ligne : http://docs.writethedocs.org/
	* Conférence : http://conf.writethedocs.org/

Ceci rendra dans un en-tête
avec une liste en dessous.
Les URLs seront hyperliées automatiquement.
C'est facile à écrire,
ça a toujours du sens en tant que texte brut,
et s'affiche joliment en HTML.

README
~~~~~~

Vos premiers pas dans la documentation doivent être faits dans votre README.
Les services d'hébergement de code rendront votre README en HTML automatiquement si vous fournissez l'extension appropriée.
C'est également la première interaction que la plupart des utilisateurs auront avec votre projet.
Un bon fichier README sera donc très utile à votre projet.

Certaines personnes vont même jusqu'à "commencer votre projet avec un README".

.. _démarrez votre projet avec un README : http://tom.preston-werner.com/2010/08/23/readme-driven-development.html

.. _écrire :

Que faut-il écrire ?
-------------

Maintenant, nous entrons dans le vif du sujet.
Assurez-vous que vous donnez à vos utilisateurs toutes les informations dont ils ont besoin,
mais pas trop.

Tout d'abord, vous devez vous demander pour qui vous écrivez.
Au début,
vous devez généralement vous adresser à deux publics :

* les utilisateurs
* les développeurs.

Les utilisateurs sont des gens qui veulent simplement utiliser votre code,
et ne se soucient pas de savoir comment il fonctionne.
Les développeurs sont des personnes qui veulent contribuer à votre code.

Quel problème votre projet résout-il ?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

De nombreuses personnes consulteront votre documentation en essayant de comprendre ce qu'est exactement votre projet. Quelqu'un le mentionnera, ou ils chercheront une phrase sur Google au hasard. Vous devez expliquer ce que fait votre projet et pourquoi il existe. Fabric_ fait un excellent travail à cet égard.

.. _Fabric : http://docs.fabfile.org/

Un petit exemple de code
~~~~~~~~~~~~~~~~~~~~

Montrez un exemple parlant de ce à quoi votre projet servirait normalement. Requests_ en fait un excellent exemple.

.. _Requests : https://requests.kennethreitz.org/en/master/

Un lien vers votre code et votre gestionnaire de problèmes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Les gens aiment parfois parcourir le code. Ils peuvent être intéressés par le dépôt de bogues dans le code pour des problèmes qu'ils ont trouvés. Facilitez la tâche des personnes qui souhaitent contribuer au projet de quelque manière que ce soit. Je pense que le `Guide Python`_ fait un bon travail avec le lien vers la partie code.

.. Guide Python : http://docs.python-guide.org/en/latest/index.html

Foire aux questions (FAQ)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Beaucoup de gens ont les mêmes problèmes. Si les choses se produisent tout le temps, vous devriez probablement corriger votre documentation ou le code, afin que les problèmes disparaissent. Cependant, il y a toujours des questions qui sont posées sur votre projet, des choses qui ne peuvent pas être changées, etc. Documentez-les, et **tenez-les à jour**. Les FAQ sont généralement obsolètes, mais lorsqu'elles sont bien faites, elles constituent une ressource en or. Tastypie_ a fait un excellent travail à ce sujet, avec son concept de "livre de recettes".

.. _Tastypie : http://django-tastypie.readthedocs.org/en/latest/cookbook.html

Comment obtenir de l'aide
~~~~~~~~~~~~~~~~~~

Liste de diffusion ? Canal IRC ? Documentez comment obtenir de l'aide et interagir avec la communauté autour d'un projet. Django_ fait un excellent travail à ce sujet.

.. _Django : https://docs.djangoproject.com/en/1.8/faq/help



Informations pour les personnes qui veulent contribuer en retour
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Les gens ont généralement des normes sur la façon dont ils s'attendent à ce que les choses soient faites dans leurs projets. Vous devriez les documenter de sorte que si les gens écrivent du code, ils puissent faire les choses dans la norme du projet. `Open Comparison`_ fait un excellent travail à ce sujet.

.. _Open Comparison : https://packaginator.readthedocs.io/en/latest/contributing.html


Instructions d'installation
~~~~~~~~~~~~~~~~~~~~~~~~~

Une fois que les gens ont décidé d'utiliser votre code ou non, ils doivent savoir comment l'obtenir et le faire fonctionner. Avec un peu de chance, vos instructions d'installation devraient tenir en quelques lignes pour le cas de base. Une page qui donne plus d'informations et des avertissements devrait être liée à partir d'ici si nécessaire. Je pense que chez "Read the Docs", nous faisons un bon travail à ce sujet.

.. _Lisez les docs : http://read-the-docs.readthedocs.org/en/latest/install.html


La licence de votre projet
~~~~~~~~~~~~~~~~~~~~~~~

BSD ? MIT ? GPL ? Ce genre de choses n'a peut-être pas d'importance pour vous, mais les personnes qui veulent utiliser votre code s'y intéressent beaucoup. Pensez à ce que vous voulez accomplir avec votre licence, et s'il vous plaît ne choisissez qu'une des licences standards que vous voyez sur le web.

.. _template :


Prochaines étapes
----------

Après avoir suivi le guide ci-dessus,
nous savons que votre projet sera une réussite !
Pour plus de lecture,
consultez ce post sur `comment maintenir un projet open source`_.

.. _comment maintenir un projet open source : https://medium.com/p/aaa2a5437d3a

Modèle
--------

Un modèle simple pour vous permettre de commencer,
pour votre ``README``.
Nommez le fichier ``README.md`` si vous voulez utiliser markdown,
ou ``README.rst`` si vous voulez utiliser reStructuredText.
Vous trouverez plus d'informations à ce sujet dans la :ref:`barre latérale sur le balisage <markup_languages>`.

: :

	$projet
	========

	$project résoudra votre problème de savoir par où commencer avec la documentation,
	en fournissant une explication basique de comment le faire facilement.

	Regardez comme il est facile à utiliser :

	    import project
	    # Faites votre travail
	    project.do_stuff()

	Caractéristiques
	--------

	- Être génial
	- Accélérer les choses

	Installation
	------------

	Installez $projet en exécutant :

	    install project

	Contribuer
	----------

	- Issue Tracker : github.com/$project/$project/issues
	- Code source : github.com/$project/$projet

	Support
	-------

	Si vous rencontrez des problèmes, veuillez nous en faire part.
	Nous avons une liste de diffusion à l'adresse : project@google-groups.com

	Licence
	-------

	Le projet est sous licence BSD.
