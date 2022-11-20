Apprendre Git en éditant le site Write the Docs
===============================================

Identifiez la page que vous souhaitez modifier
----------------------------------

1. Trouvez un "problème existant", ou une page que vous voulez améliorer.
2. Dans l'interface utilisateur du repo, trouvez le fichier qui correspond à la page. Pour
   exemple :
   https://www.writethedocs.org/documentarians/ est produit par
   ``/docs/documentarians.rst``. (Vous aurez besoin de ce nom de fichier plus tard pour
   faire des modifications sur votre copie locale).
3. Il s'agit d'un fichier ReStructuredText (.rst).
   `Documentation RST`_. D'autres formats de balisage courants sont Markdown (.md)
   et AsciiDoc (.adoc).

Conditions préalables
-------------

1. `Créer un compte GitHub`_.
2. `Téléchargez et installez Git`_.
3. Ouvrez une fenêtre de terminal et suivez les instructions pour `associer votre
   votre nom d'utilisateur GitHub à votre installation locale de Git`_.

   1. Sous macOS : Ouvrez l'application **Terminal**.
   2. Sous Windows : Dans le menu Démarrer, ouvrez **Git Bash**.

Commencez à utiliser Git et modifiez le fichier source d'une page
----------------------------------------------------

1.  Visitez le projet `Write the Docs www`_.

2.  Cliquez sur le bouton **Fork** dans le coin supérieur droit pour créer une
    copie du projet dans votre compte GitHub. La nouvelle page pour le
    projet bifurqué s'ouvre.

3.  Cliquez sur le bouton **Clone ou téléchargement** et copiez l'URL https de la page du projet.
    la page du projet.

4.  Ouvrez une fenêtre de terminal pour que vous puissiez exécuter les commandes ``git``.

    1. Sous macOS : Ouvrez l'application **Terminal**.
    2. Sous Windows : Dans le menu Démarrer, ouvrez **Git Bash**.

5.  Naviguez vers ou créez le répertoire dans lequel vous voulez cloner le référentiel. 

6.  Dans votre fenêtre de terminal, tapez ``git clone``, suivi d'un espace,
    et ensuite collez l'URL du projet :

    : :

       git clone https://github.com/myname/www.git

6.  Appuyez sur la touche Entrée. La commande copie les fichiers depuis GitHub vers un dossier nommé
    ``www`` sur votre machine locale.

7.  Dans la fenêtre du terminal, allez dans le répertoire ``www``.

    : :

       cd www

8.  Créez et passez à une branche. En utilisant les commandes ci-dessous,
    remplacez ``nom-de-branche`` par un nom qui décrit brièvement les
    les changements que vous allez faire, en utilisant de préférence des tirets entre les mots. Pour
    Par exemple, ``important-typo-fix``.

    a. Créez une branche avec :

       : :

          git branch branch-name

       Passez à la branche :

       : :

          git checkout nom-branche

    b. Vous pouvez aussi utiliser une seule commande pour effectuer les deux étapes en même temps :

       : :

          git checkout -b nom-branche

9. Ouvrez le dossier ``www`` sur votre ordinateur.

10. | Ouvrez le fichier que vous souhaitez modifier en utilisant un éditeur de texte comme `Sublime
      Text`_ ou `Visual Studio Code`_, puis enregistrez le fichier.

11. Dans votre fenêtre de terminal, tapez :

    : :

       git status

    Cela vous montrera tous les fichiers que vous avez mis à jour.

12. Si vos changements semblent exacts, tapez ce qui suit dans votre fenêtre de terminal :

   : :

      git add -A

   Ceci ajoutera tous les fichiers nouveaux et modifiés à votre projet local.

13. Pour sauvegarder vos changements, entrez ce qui suit dans votre fenêtre de terminal :

   : :

      git commit -m "Votre message"

   Ceci sauvegardera tous vos fichiers modifiés. Remplacez ``Votre message`` par une description de la mise à jour que vous avez faite.
   par une description de la mise à jour que vous avez effectuée. *Protip* : Apprenez comment
   à écrire un bon message de validation.

   Vous pouvez répéter le même processus pour ajouter plusieurs commits dans votre
   branche.

14. Envoyez votre/vos commit(s) à votre projet GitHub en utilisant ``git push``. Entrez ce qui suit dans votre fenêtre de terminal :

   : :

      git push -u origin branch-name

15. Créez une `GitHub pull request`_ dans le projet `Write the Docs www`_.


.. _problème existant : https://github.com/writethedocs/www/issues
.. _Documentation RST : https://docutils.readthedocs.io/en/sphinx-docs/user/rst/quickstart.html
.. _Créer un compte GitHub : https://github.com/join
.. _Télécharger et installer Git : https://git-scm.com/downloads
.. _associer votre nom d'utilisateur GitHub à votre installation locale de Git : https://help.github.com/en/articles/setting-your-username-in-git
.. . _Écrire le projet Docs www : https://github.com/writethedocs/www
.. _Sublimez le texte : https://www.sublimetext.com
.. _Code Visual Studio : https://code.visualstudio.com/
.. _Écrire un bon message de validation : https://chris.beams.io/posts/git-commit/
.. _demande de pull sur GitHub : https://help.github.com/en/articles/creating-a-pull-request
.. ... _Écrire le projet Docs www : https://github.com/writethedocs/www
