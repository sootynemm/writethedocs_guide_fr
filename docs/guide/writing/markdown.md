## Introduction à Markdown

## Qu'est-ce que Markdown ?

Markdown est un langage de balisage libre doté d'une syntaxe de formatage simple. Utilisez-le pour créer des pages Web, des documents ou tout texte devant être transformé dans d'autres formats comme le HTML.

## Pourquoi utiliser le format Markdown ?

Il permet aux rédacteurs non techniques de produire plus facilement une documentation à la fois collaborative et flexible.

## Comment utiliser le format Markdown

### Formatage du texte en Markdown

- Pour mettre en forme le texte, suivez les règles suivantes :
  - Pour l'italique, entourez l'élément d'une étoile de chaque côté : `*une étoile de chaque côté*`.
  - Pour le texte en gras, placez deux étoiles de chaque côté de l'élément : `**deux étoiles de chaque côté**`.
  - Pour barrer le texte dans le format GitHub Markdown, placez deux tildes autour de l'élément : `~~strikethrough~~`.
  - Pour les liens, mettez le texte du lien entre crochets [ ], puis mettez l'URL entre parenthèses ( ) : `[Ce texte est lié à WritetheDocs](https://www.writethedocs.org)`.

Le texte formaté ressemblera à ceci :

- Pour l'italique, entourez l'élément d'une étoile de chaque côté, comme ceci : *une étoile de chaque côté*.
- Pour les lettres en gras, entourez l'élément de deux étoiles de chaque côté : **deux étoiles de chaque côté**.
- Pour barrer le texte dans le format GitHub Markdown, placez deux tildes autour de l'élément : ~~strikethrough~~.
- Pour les liens, mettez le texte du lien entre crochets [ ], puis mettez l'URL entre parenthèses ( ) : [Ce texte est lié à WritetheDocs] (https://www.writethedocs.org/).

### Ajout d'images

L'ajout d'images est similaire à l'ajout de liens. Il suffit d'ajouter un point d'exclamation au début de la ligne :

`![alt text](https://pbs.twimg.com/profile_images/556169790587281409/AwkaVrhP_400x400.png).`

L'image ressemblera à ceci :

![alt text](https://pbs.twimg.com/profile_images/556169790587281409/AwkaVrhP_400x400.png).

### Comment produire des listes ?

Pour ajouter une liste d'éléments à puces ou non ordonnée :

```
- Il suffit d'ajouter un tiret d'abord, puis d'écrire un texte.
- Si vous ajoutez un autre tiret dans la ligne suivante, vous aurez un autre élément dans la liste.
  - Si vous ajoutez quatre espaces ou utilisez une touche de tabulation, vous créerez une liste en retrait.
    - Si vous devez insérer une liste en retrait à l'intérieur d'une liste prévue, il vous suffit d'appuyer à nouveau sur la touche de tabulation.
```

Le texte formaté ressemblera à ceci :

- Il suffit d'ajouter un tiret d'abord, puis d'écrire un texte.
- Si vous ajoutez un autre tiret dans la ligne suivante, vous aurez un autre élément dans la liste.
  - Si vous ajoutez quatre espaces ou utilisez une touche de tabulation, vous créerez une liste en retrait.
    - Si vous devez insérer une liste en retrait à l'intérieur d'une liste prévue, il vous suffit d'appuyer à nouveau sur la touche de tabulation.

Pour ajouter une liste d'éléments numérotés ou ordonnés :

```
1. Tapez simplement un numéro suivi d'un point.
2. Si vous voulez ajouter un deuxième élément, tapez simplement un autre nombre suivi d'un point.
1. Si vous faites une erreur en tapant des chiffres, n'ayez crainte, Markdown la corrigera pour vous.
    1. Si vous appuyez sur une touche de tabulation ou tapez quatre espaces, vous obtiendrez une liste indentée et la numérotation recommencera à zéro.
    recommencera à zéro.
        1. Si vous voulez insérer une liste numérotée en retrait dans une liste numérotée en retrait existante,
        il suffit d'appuyer à nouveau sur la touche de tabulation.
            - Si nécessaire, vous pouvez également ajouter une liste non ordonnée en retrait à l'intérieur d'une liste numérotée en retrait, et vice versa,
            en appuyant sur la touche de tabulation et en tapant un tiret.
```

Le texte formaté ressemblera à ceci :

1. Tapez simplement un nombre suivi d'un point.
2. Si vous voulez ajouter un deuxième élément, il suffit de taper un autre nombre suivi d'un point.
1. Si vous faites une erreur en tapant des chiffres, n'ayez crainte, Markdown la corrigera pour vous.
    1. Si vous appuyez sur une touche de tabulation ou tapez quatre espaces, vous obtiendrez une liste indentée et la numérotation recommencera à zéro.
        1. Si vous voulez insérer une liste numérotée en retrait dans une liste numérotée en retrait existante,
        il suffit d'appuyer à nouveau sur la touche de tabulation.
            - Si nécessaire, vous pouvez également ajouter une liste non ordonnée en retrait à l'intérieur d'une liste numérotée en retrait, et vice versa,
            en appuyant sur la touche de tabulation et en tapant un tiret.

### En-têtes

Si vos documents sont longs, il est préférable de leur donner une certaine structure, ce que vous pouvez faire avec des en-têtes. Faites-le avec des hachages (#) :

`# Ceci est un en-tête de premier niveau`

`## Ceci est un en-tête de second niveau`

`### Ceci est un en-tête de troisième niveau`

Et ainsi de suite, jusqu'à un en-tête de sixième niveau.

Le texte formaté ressemblera à ceci :

![](/_static/img/guide/markdown-headers.png)

### Règle horizontale

Créez une règle horizontale avec trois traits d'union, astérisques ou traits de soulignement ou plus sur une ligne :

`---`

`* * *`

`___`

Le texte formaté ressemblera à ceci :

---

### Citations et code

Ajoutez une citation avec le caractère > au début de chaque ligne :

```
> "Je fais passer Jessica Simpson pour une scientifique du rock."

> -Tara Reid, actrice
```

La citation ressemblera à ceci :

> "Je fais ressembler Jessica Simpson à une scientifique du rock."

> -Tara Reid, actrice

Enfin, insérez du code dans votre texte en plaçant une apostrophe de chaque côté lorsque vous ajoutez du code sur une ligne, ou en plaçant trois apostrophes pour ouvrir et fermer votre bloc de code, comme ceci :

Cette ligne contient du ``code``.

Voici une section de code :

<pre>
```
Ceci est du code
```
</pre>

Qui ressemblera à ceci :

Cette ligne contient du `code`.

Ceci est une section de code :

```
Ceci est du code
```

Vous pouvez également "tricher", en ajoutant du texte au format HTML lorsque le format démarque semble trop limité, mais consultez d'abord ces ressources pour trouver des solutions :

#### Ressources

- [The fundamental guide for using Markdown](https://daringfireball.net/projects/markdown/)
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [Atom - a flexible editor that you can use for formatting Markdown texts](https://atom.io/)
- [Stackedit - an online Markdown editor](https://stackedit.io/editor)
- [Codecademy course on Markdown](https://www.codecademy.com/courses/web-intermediate-en-Bw3bg/0/1)
