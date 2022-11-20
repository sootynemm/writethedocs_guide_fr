DocOps
======

auteur : Jodie Putrino & la communauté Write the Docs

Qu'est-ce que DocOps ?
-----------------------

Avec l'avènement de :doc:`/guide/docs-as-code`, la communauté des rédacteurs techniques a vu se développer une nouvelle spécialisation appelée "DocOps" (ou "doc-ops"). 
a vu naître une nouvelle spécialisation appelée "DocOps" (ou "doc-ops").

Mais qu'est-ce que DocOps signifie réellement, et qui "fait" DocOps ?

Ce sujet a fait l'objet d'une discussion lors d'une session Unconference à la conférence Write 
the Docs (WTD) North America en 2021 à Portland. 
Cette page représente certaines des idées présentées lors de cette session.

D'une manière générale, "DocOps" est comme "DevOps". Mais au lieu de s'appliquer largement au 
développement de logiciels, DocOps s'applique spécifiquement à la création, 
gestion et la diffusion de la documentation.  

Si l'on s'en tient à la définition de DevOps fournie par Atlassian et mentionnée dans le 
paragraphe précédent, nous pourrions donc définir DocOps comme suit :

   "un ensemble de pratiques visant à automatiser et à intégrer le processus de développement de la documentation au sein de l'ingénierie, du produit, de l'entreprise et de l'organisation. 
   de développement de la documentation au sein des équipes d'ingénierie, de produit, de support et, bien sûr, de rédaction technique. 
   et, bien sûr, les équipes de rédaction technique". 

Tout comme DevOps, DocOps met l'accent sur la collaboration et l'amélioration continue. 
l'amélioration continue. Ci-dessous, nous avons adapté le diagramme du cycle de vie traditionnel de DevOps pour
pour représenter DocOps :

... image: : /_static/img/guide/docops-lifecycle.png

.. _DevOps : https://www.atlassian.com/devops

Qui pratique DocOps ?
---------------------

Pour répondre à cette question, il est préférable d'examiner les responsabilités 
qu'un praticien ou une équipe DocOps pourrait avoir. 

* Sélectionner et fournir un support pour les outils utilisés pour produire la documentation -- langage de balisage, générateur de site statique (SSG), etc. 
  langage de balisage, générateur de site statique (SSG), fournisseur d'hébergement, etc.
* Définir les processus et les méthodes de travail établies, y compris la place de la documentation dans les méthodologies agiles ou autres.
  dans les méthodologies de développement agiles ou autres.
* Définir les priorités et les livrables de la documentation
* Formation des auteurs pour leur permettre de contribuer à la documentation.
* Gestion du contenu     
* Construire et maintenir un thème pour une SSG.
* Modélisation et mise en œuvre des stratégies de versionnement du produit en ce qui concerne la documentation. 
  la documentation
* Créer et maintenir des scripts de construction 
* Maintenir la barrière d'entrée pour la création de la documentation à un niveau bas afin de rendre la contribution facile et (osons le dire ?) amusante. 
  (osons le dire ?) amusante

Il ne s'agit en aucun cas d'une liste exhaustive. Si vous avez des responsabilités qui 
chevauchent ou intègrent certaines de ces responsabilités, vous êtes peut-être un praticien DocOps.

Il est également important de noter que, même si DocOps est souvent associé à la notion de 
docs-as-code, ce n'est pas une obligation. Vous pouvez utiliser DITA, un CMS, un wiki, etc ; 
Si vous êtes impliqué dans les domaines énumérés ci-dessus, quel que soit l'ensemble d'outils, il y a de fortes chances que vous soyez DocOps. 
il y a de fortes chances que vous soyez DocOps !

Ressources DocOps
----------------

Si vous êtes intéressé par DocOps, rejoignez la conversation sur le Slack de Write the Docs 
`#docops`_ channel !

* `CA Technologies`_ a été parmi les premiers à utiliser publiquement le terme "DocOps" pour 
  décrire leur approche du contenu technique
* Chris Noonan a fait une présentation sur la "Rocky Road to DocOps" à la JMT Europe en 2020.
* `Doc Tool Hub`_ fournit une liste d'articles et de billets de blog liés à DocOps.

.. _#docops : https://writethedocs.slack.com/archives/C62BVHJ7K
.. _CA Technologies : https://www.k15t.com/blog/2014/12/webinar-how-ca-technologies-broke-the-rules-the-docops-approach-to-agile-technical-content
.. _Chris Noonan : https://www.youtube.com/watch?v=2HjeYNs2z7o
.. _Doc Tool Hub : https://doctoolhub.com/collection/docops/ 
