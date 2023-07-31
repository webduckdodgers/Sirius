<!-- omit in toc -->
# Comprendre l'HTML

<!-- omit in toc -->
## Table des matières

- [Qu'est ce que le HTML ?](#quest-ce-que-le-html-)
- [Le squelette d'une page HTML](#le-squelette-dune-page-html)
- [Les balises](#les-balises)
  - [Principe d'une balise](#principe-dune-balise)
- [La balise `<html>`](#la-balise-html)
- [La balise `<head>`](#la-balise-head)
  - [La balise `<title>`](#la-balise-title)
- [Les balises `<meta>`](#les-balises-meta)
- [La balise `<body>`](#la-balise-body)
- [Les commentaires en HTML](#les-commentaires-en-html)
- [Classe et ID](#classe-et-id)
- [La balise `<div>`](#la-balise-div)
- [La balise `<p>`](#la-balise-p)
- [Les balises `<h1>` à `<h6>`](#les-balises-h1-à-h6)
- [La balise `<img>`](#la-balise-img)
- [La balise `<a>`](#la-balise-a)
  - [Les ancres](#les-ancres)
- [Les liens interne et externe](#les-liens-interne-et-externe)
- [Les tableaux](#les-tableaux)
  - [La balise `<table>`](#la-balise-table)
  - [Les balises `<tr>`, `<td>`, `<th>`](#les-balises-tr-td-th)
- [Les listes](#les-listes)
  - [Les listes non ordonnées `<ul>`](#les-listes-non-ordonnées-ul)
  - [Les listes ordonnées `<ol>`](#les-listes-ordonnées-ol)
  - [La balise `<li>`](#la-balise-li)
- [Encore quelques balises](#encore-quelques-balises)
- [Pour allez plus loin](#pour-allez-plus-loin)
- [Questionnaire HTML](#questionnaire-html)

## Qu'est ce que le HTML ?

HTML est l'acronyme de HyperText Markup Language.
Le HTML n'est pas un langage de programmation à proprement parlé comme on peut le dire du Javascript ou du PHP.
Il s'agit d'un "langage de balisage", il est directement interprété par le navigateur, c'est à dire qu'il n'a besoin d'aucune traduction pour que le navigateur puisse rendre le contenu visible sur votre ordinateur / tablette / GSM.

Par langage de balisage on entend qu'il utilise des balises pour indiquez au navigateur le type de contenu auquel il a à faire (ex: `<p>` `<h1>` `<h2>`  ). Elles indiquent l'endroit de la page où votre contenu doit être inséré, comme un coup de marqueur sur une carte.

C'est le squelette de votre page web, comme vos os soutiennent votre corps et ses différents tissus, le HTML soutient le contenu de votre page, permet de le styliser, de l'animer, de le rendre dynamique.

[:arrow_up: Revenir au top](#table-des-matières)

## Le squelette d'une page HTML

```html
<!doctype html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title> Coucou je suis une page html</title>
</head>
<body>
  <p> Salut je suis le contenu de la page</p>
</body>
</html>
```

> Voici un exemple de page HTML toute simple. Analysons un peu tout ça.

[:arrow_up: Revenir au top](#table-des-matières)

## Les balises

Ce sont tous ces mots étranges entre `< >`. Sans les balises HTML, une page ne serait qu'un simple bloc texte. Ce sont elles qui structurent le contenu de la page. Ces balises seront interprétées par le navigateur pour lui permettre d'afficher correctement votre page à l'utilisateur.

Elles peuvent être imbriquées l'une dans l'autre.

[:arrow_up: Revenir au top](#table-des-matières)

### Principe d'une balise

On commence toujours par la balise entrante, puis le contenu, ensuite on referme la balise.

```html
<p>Salut</p>
```

> Le nom de la balise se met entre `< >`, ce nom est définit dans les spécifications HTML, on ne met pas ce que l'on veut.

[:arrow_up: Revenir au top](#table-des-matières)

## La balise `<html>`

C'est elle qui ouvre et ferme tout votre code. Il est obligatoire d'ajouter les balises `<head>` et `<body>` entre votre balise `<html>`.

```html
<html lang="fr">
```

Cette balise prend généralement l'attribut `lang` qui permet de définir la langue de votre page. Cela permet une meilleur indexation pour les moteurs de recherches, aide à la synthèse vocale et permet la vérification orthographique des formulaires.

[:arrow_up: Revenir au top](#table-des-matières)

## La balise `<head>`

Elle détermine l'entête du document et contient les méta-informations (infos concernant la page). Ce sont des infos qui ne sont pas visibles des visiteurs de votre page mais qui servent aux moteurs de recherches notamment. On peut aussi y insérer des règles de styles pour votre page (mais ce n'est pas recommandé).

[:arrow_up: Revenir au top](#table-des-matières)

### La balise `<title>`

```html
<title>Le titre de ma super page HTML</title>
```

Elle est contenue dans la balise `<head>` et permet de donner un titre à votre page.

[:arrow_up: Revenir au top](#table-des-matières)

## Les balises `<meta>`

```html
<meta charset="UTF-8">
```

Il existe plusieurs type de balise meta. Elles servent notamment à définir quel set de caractères la page utilise, le nom de l'auteur de la page, des mots-clés, une description,... Tout cela aide la navigateur et les moteurs de recherches.

Quelques exemples de balises `<meta>`:

```html
<meta name="description" content="Ma première page web">
<meta name="author" content="Jeremy Scala">
<meta name="keywords" content="html, css, tutorials">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

> Leurs noms sont plutôt explicite.

[:arrow_up: Revenir au top](#table-des-matières)

## La balise `<body>`

C'est elle qui contient le contenu de la page. On y met toutes les balises de textes, d'images, de liens,...

[:arrow_up: Revenir au top](#table-des-matières)

## Les commentaires en HTML

Les commentaires dans le code sont une bonne pratique à avoir. Ils permettent de donner des informations complémentaires à ceux qui retravaillerons dans votre code. Généralement pour l'HTML, vu que c'est la base, il y a peu d'intérêt de commenter. Mais cela peut-être une bonne manière de vous organiser, surtout au début.

```html
<p> Je suis un texte visible <!-- je suis un commentaire invisible --></p>
```

Faisons une toute petite pause théorique. 

*Petit exercice:* Ouvrez VSCode et essayer de recréer un squelette HTML simple sans regarder l'exemple tout au dessus.

:bulb: Tu ne dois pas retenir ce squelette par coeur. Tu peux utiliser Emmet pour mettre en page rapidement ta structure de base HTML. Pour ce faire, enregistre ton document en `.html`. Ensuite dedans, tu peux tout simplement écrire `!` et valider avec la touche `Enter`. VSCode comprendra que tu utilises une abréviation d'Emmet et te mettra en place ta structure. Nous verrons Emmet un peu plus loin...

[:arrow_up: Revenir au top](#table-des-matières)

## Classe et ID

Pour identifier nos différentes balises et les différentier, on peut leurs attribuer des `classes` et des `id`. 

- **classe**: peut être multiplié sur la page.
- **id**: doit être unique sur la page.

## La balise `<div>`

La **div**ision est un conteneur. Cette balise permet de structurer sa page en "bloc". Dans ces balises/bloc on insérera le contenu adéquat (image, texte, liens,....).

```html
<div class="container">
  <p>contenu</p>
</div>
```

[:arrow_up: Revenir au top](#table-des-matières)

## La balise `<p>`

P pour paragraphe, c'est la balise la plus courante pour rédiger du texte. C'est un bloc qui est suivis d'un saut à la ligne. On peut mettre la balise `<p>` dans une `<div>` mais jamais de `<p>` dans une autre balise `<p>`.

```html
<p>Je suis un paragraphe</p>
```

[:arrow_up: Revenir au top](#table-des-matières)

## Les balises `<h1>` à `<h6>`

Ce sont les balises de titre. Il y en a 6 au total et pas plus. Chaque titre inclut un saut à la ligne. Le style de chaque titre est pré-défini par le navigateur mais peut être changé dans le style css.

```htmlé  
<h1>Je suis un titre de niveau 1, le plus important</h1>
<h2>Je suis un titre de niveau 2</h2>
<h3>Je suis un titre de niveau 3</h3>
<h4>Je suis un titre de niveau 4</h4>
<h5>Je suis un titre de niveau 5</h5>
<h6>Je suis un titre de niveau 6, le moins important</h6>
```

[:arrow_up: Revenir au top](#table-des-matières)

## La balise `<img>`

Cette balise sert à insérer une image dans votre page. Elle peut se placer un peu où vous voulez dans votre **\<body>**. Généralement dans un **\<div>** ou dans un **\<p>**

```html
<img src="lien vers mon image" alt="description de l'image"/>
```

- `src`: tout simplement un lien externe ou interne vers votre fichier image.
- `alt`: une description que les utilisateurs verront si votre image met du temps à se charger, si elle n'est plus en ligne ou pour aider la synthèse vocale.

Évidement une balise `<img>` peut prendre d'autres attributs, notamment des valeurs de taille, mais les deux vu ci dessus sont les plus courant.

> :book: [quelques infos complémentaire sur cette balise](https://www.w3schools.com/tags/tag_img.asp)

[:arrow_up: Revenir au top](#table-des-matières)

## La balise `<a>`

Il est maintenant temps d'insérer un lien dans votre code. Pour ce faire on utilise la balise `<a>`. Elle se place un peu où vous voulez et doit surtout englober un contenu comme du texte, une image ou même une `<div>`.

```html
<a href="mon lien" title="titre du lien" target="_blank">Mon texte cliquable</a>
```

- `href:` c'est l'attribut qui prend comme valeur le lien vers lequel l'utilisateur sera redirigé en cliquant. Il peut être externe ou interne.
- `title:` sert à préciser à l'utilisateur une information par rapport au lien lorsqu'il survole le lien avec sa souris.
- `target:` permet de préciser si le lien doit s'ouvrir à un endroit spécifique. Par exemple avec `_blank`, le lien s'ouvrira dans un nouvel onglet.

### Les ancres

Il est possible d'amener le visiteur de votre site vers un point précis de votre page grâce aux ancres. Pour ce faire il suffit de donner un `ID` à une balise et de placer cet `ID` dans le `href` de votre lien.

```html
<a href="#contact">Contact</a>
...
<div id="contact">
```

[:arrow_up: Revenir au top](#table-des-matières)

## Les liens interne et externe

Lorsque vous avez besoin de faire référence à un fichier il est possible d'utiliser deux méthode. Soit votre fichier se trouve déjà sur internet mais est extérieur à votre projet (lien vers un autre site, vers une ressource ou image,...), dans ce cas vous devez introduire l'url de ce fichier directement dans votre attribut `src` ou `href`.

Si votre ressource fait partie de votre projet, alors vous pouvez y faire référence directement. Voyons un rapide exemple:

![File tree](img/04/filetree.png)

Ici je possède deux images, une dans un dossier *Images* et l'autre à la racine de mon projet. Regardez le bout de code suivant

```html
<!-- index.html-->
<body>
  <div id="header">
    <img src="logo.jpg" alt="mon logo"/>
  </div>
  <div id="content">
    <img src="/images/monImage.jpg"/>``
  </div>
</body>
```

La source est différente en fonction d'où ce situe mon image. Pour le moment on ne va pas trop rentrer dans le détail, mais essayez de rester cohérent avec vous même et de placer vos fichiers correctement.

:exclamation: Si votre fichier est en local, il faudra l'envoyer avec votre page pour que la personne qui exécute votre page puis voir votre image. Ben oui, si vous n'envoyez que la page sans son image, la personne qui reçoit votre page n'a pas l'image stocké sur sa machine comme vous.

[:arrow_up: Revenir au top](#table-des-matières)

## Les tableaux

Une façon d'organiser ses informations sur une page peut être l'utilisation de tableaux. Ceux-ci sont composer de lignes et de cellules.

> :bangbang: On ne met pas en page le design de son site avec des tableaux!! Pour ce faire on utilisera le CSS qu'on verra dans la prochaine partie.

Voyons la marche à suivre pour créer ton premier tableau.

> :bulb: De nouveau, ouvre VSCode et essaye les différents bout de code qui seront présentés ici pour voir leur fonctionnement.

[:arrow_up: Revenir au top](#table-des-matières)

### La balise `<table>`

Alors non, ce n'est pas pour insérer un meuble pour poser votre assiette et votre verre, mais bien une balise qui va indiquer le début et la fin de votre tableau.

```html
<table>
  <!-- tout le contenu de mon tableau -->
</table>
```

[:arrow_up: Revenir au top](#table-des-matières)

### Les balises `<tr>`, `<td>`, `<th>`

Remplissons notre tableau avec quelques lignes et cellules.

```html
<table>
  <tr>
    <th>En-tête colone 1</th>
    <th>En-tête colone 2</th>
    <th>En-tête colone 3</th>
  </tr>
  <tr>
    <td>ligne 1 colonne 1</td>
    <td>ligne 1 colonne 2</td>
    <td>ligne 1 colonne 3</td>
  </tr> 
  <tr>
    <td>ligne 2 colonne 2</td>
    <td>ligne 2 colonne 1</td>
    <td>ligne 2 colonne 3</td>
  </tr>
</table>
```

- `th:` Table Header = En-tête du tableau.
- `tr:` Table Row = Ligne du tableau
- `td:` Table Data = Cellule contenant toute sorte d'infos (texte, image,...)

> Il y a encore quelques balises intéressantes à connaître pour personnaliser vos tableaux, voici un lien pour en savoir plus.
>
> :book: [W3Schools - Tableaux](https://www.w3schools.com/html/html_tables.asp)
>
> Nous verrons un peu plus loin comment mettre un peu de couleur à ce pauvre tableau tout triste.

N'hésite pas à t'amuser un peu avec les tableaux et à bien comprendre comment ils sont construits.

[:arrow_up: Revenir au top](#table-des-matières)

## Les listes

Il existe 2 types de listes, celle qui sont triées et celle qui ne le sont pas. Leurs utilisation dépend du contexte. Si vous devez énumérer une liste d'étapes, il vous faudra la balise `<ol>` et si c'est juste une liste de points à aborder, une balise `<ul>` suffira.

### Les listes non ordonnées `<ul>`

`ul:` Unordered List

```html
<ul>
  <!-- contenu de votre liste -->
</ul>
```

[:arrow_up: Revenir au top](#table-des-matières)

### Les listes ordonnées `<ol>`

`ol:` Ordered List

```html
<ol>
  <!-- contenu de votre liste -->
</ol>
```

[:arrow_up: Revenir au top](#table-des-matières)

### La balise `<li>`

C'est bien joli d'ouvrir une balise de liste, mais sans rien dedans ça fonctionne moins bien. Il faut maintenant rajouter une balise `<li>` pour List Item. En fonction du type de liste, un point ou un chiffre va apparaître devant votre contenu. Essaye!

```html
<ol>
  <li>Moi j'aurai le chiffre 1 devant moi</li>
  <li>Et moi le chiffre 2.</li>
</ol>
<ul>
  <li>Moi, comme je suis dans une liste non ordonnée, j'aurai juste un point.</li>
</ul>
```

[:arrow_up: Revenir au top](#table-des-matières)

## Encore quelques balises

Il existe encore pleins de balises, mais le but de ce premier cours n'est pas de toutes les voir, ni de toutes les retenir. Un des principes du coding, c'est de connaître suffisamment de concepts que pour pouvoir accomplir son travail, savoir que certaines choses existes et d'allez lire la documentation si besoin ou de faire des recherches sur le net.

Balises sémantiques :

  - `<article>`
  - `<aside>`
  - `<details>`
  - `<figcaption>`
  - `<figure>`
  - `<footer>`
  - `<header>`
  - `<main>`
  - `<mark>`
  - `<nav>`
  - `<section>`
  - `<blockquote>`

![semantic](https://www.w3schools.com/html/img_sem_elements.gif)

> :book: [plus d'infos](https://www.w3schools.com/html/html5_semantic_elements.asp)

Balises de style :

  - `<strong>`
  - `<em>`
  - `<span>`


> :book: [Tags HTML sur W3School](https://www.w3schools.com/tags/)
>
> :book: [Tags HTML sur MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element)

[:arrow_up: Revenir au top](#table-des-matières)

## Pour allez plus loin

> :bulb: Si tout ce que tu viens de voir te semble clair, voici quelques pistes pour allez un peu plus loin dans la matière et qui te servira pour ton exercice de cette semaine.

- Lire la doc de chacune des balises vue dans cette théorie.
- Manipuler les balises vue, essaye différentes choses.
- Essaye de trouver comment mettre une vidéo ou du son dans ta page. Ce n'est absolument pas nécessaire pour l'exercice, mais ça te ferra chercher un peu la documentation.

[:arrow_up: Revenir au top](#table-des-matières)

Phew! Ca en fait des nouvelles choses à assimiler. Tout va bien??

## Questionnaire HTML

Alors si tout va bien, un petit [questionnaire !](https://forms.gle/MFhdcrrkveThnQiRA)

[:rewind: Retour au sommaire du cours](../README.md#au-programme)

> Cours original : Julie Vanderbyse
>
> Modification : Jeremy Scala & Lucas Ielli
