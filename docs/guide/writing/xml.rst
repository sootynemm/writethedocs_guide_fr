===================
Introduction à XML
===================

Qu'est-ce que le XML ?
============

Le XML est un méta-langage de balisage développé pour l'Internet. Il est dérivé du SGML (Standard Generalized Markup Language), la mère de tous les langages de balisage. Le XML a été conçu pour stocker et transporter des données. Contrairement au HTML qui définit l'apparence des données, le XML définit ce que sont les données. Les utilisateurs peuvent utiliser le XML "tel quel" ou l'adapter à leurs besoins en définissant de nouvelles balises ou de nouveaux blocs de construction.

Le XML définit un ensemble de règles permettant d'encoder les données dans un format lisible par l'homme et par la machine. C'est pourquoi la syntaxe XML est utilisée dans Microsoft Office, Apple iWork, LibreOffice, RSS, SVG et de nombreux autres outils.

Pourquoi utiliser XML ?
============

Comme vous définissez vos propres balises et attributs, vous pouvez utiliser le XML pour créer essentiellement votre propre langage de balisage. La définition de ces balises et attributs uniques donne également une structure à votre document.

En outre, le XML stocke les données en texte clair. Cela le rend indépendant du logiciel et du matériel sur lesquels les données enveloppées dans le XML sont envoyées, reçues et stockées. Cette conception facilite également la mise à jour vers de nouveaux navigateurs, de nouveaux systèmes d'exploitation et de nouveaux logiciels sans perte de données. 

Comment utiliser le XML
==============

Disons que nous voulons créer un tableau présentant les arbres d'une certaine région. Nous pourrions définir une balise <tree> qui contiendrait les noms des arbres, une balise <height>, une balise <type>, etc. Ces balises donnent une structure à notre document et celui-ci reste lisible par l'homme.: :

    <arbre>
        <nom>Erable à sucre</nom>
        <hauteur unités="m"> 30 </hauteur>
        <type> Feuilles caduques </type>
    </arbre>

    <arbre>
        <nom>Noyer noir</nom>
        <b>Unités de hauteur="m"> 16 </height>
        </type> Feuilles caduques </type>.
    </tree>
    
Le XML est souvent utilisé de concert avec HTML, CSS et JavaScript.

Comment afficher le XML
------------------

Le XML a besoin d'une feuille de style pour être lisible et utilisable. Les feuilles de style pour XML fonctionnent à peu près de la même manière que celles pour HTML. La différence est que nous attribuons des styles à nos balises XML uniques, et non aux balises standard utilisées en HTML.: :

    <?xml-stylesheet type="text/css" href="nutrition.css"?>
 
    nom {
        font-family : " Cooper Black ", serif ;
        taille de la police : 3em ;
        font-style : bold ;
    }
    
    height, type {
        font-family : "Bodoni", serif ;
        taille de la police : 1em ;
        font-style : none ;
    }        
 
Ressources
=========

`Tutoriel W3Schools sur le XML <https://www.w3schools.com/xml/default.asp>`_

`Utiliser XML par A List Apart <https://alistapart.com/article/usingxml/#comments>`_
