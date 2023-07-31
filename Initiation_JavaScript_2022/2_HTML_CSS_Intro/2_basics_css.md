<!-- omit in toc -->
# Design et style avec CSS

<!-- omit in toc -->
## Tables des matières
- [Qu'est ce que le CSS ?](#quest-ce-que-le-css-)
- [Le sélecteur d'HTML](#le-sélecteur-dhtml)
- [Sélecteur de hiérarchie](#sélecteur-de-hiérarchie)
- [Sélecteur d'enfant](#sélecteur-denfant)
- [Sélecteur de groupe](#sélecteur-de-groupe)
- [Qu'est-ce qu'une classe](#quest-ce-quune-classe)
- [L'identifiant (ID)](#lidentifiant-id)
- [On mélange tout!](#on-mélange-tout)
- [Espace](#espace)
- [Le sélecteur de tout!](#le-sélecteur-de-tout)
- [Convention de nommage](#convention-de-nommage)
- [Pour finir](#pour-finir)
- [Typographie](#typographie)
  - [font-family](#font-family)
  - [font-size](#font-size)
  - [color](#color)
  - [text-align](#text-align)
- [Arrière-plan](#arrière-plan)
  - [border-radius](#border-radius)
  - [background](#background)
- [Dimensions, margin et padding](#dimensions-margin-et-padding)
  - [width & height (max & min)](#width--height-max--min)
  - [margin & padding](#margin--padding)
- [Display](#display)
  - [display: block](#display-block)
  - [display: inline](#display-inline)
  - [display: inline-block](#display-inline-block)
  - [display: none](#display-none)
- [L'auto-complete de VSCode](#lauto-complete-de-vscode)
- [Exercices !](#exercices-)

## Qu'est ce que le CSS ?

Le CSS ou Cascading Style Sheets (feuilles de style en cascade), permet la mise en forme de votre squelette, c'est la partie émergée de l'iceberg, celle que vous pouvez voir quand vous consulter vos pages web.

Couleurs, polices, formes, tailles, mise en page, animations, tout ce qui rend "joli" (ou non) le squelette de votre page web ainsi que son contenu.
Attaché à votre HTML il vous permettra de reproduire une maquette de site.

Voici un exemple de syntaxe CSS que vous pourriez retrouver dans votre code:

```css
.main-title {
    font-size: 24px;
    color: white
}
```

[:arrow_up: Revenir au top](#table-des-matières)

## Le sélecteur d'HTML

Vous pouvez sélectionner n'importe quel élément HTML et lui appliquer un style, tous les éléments de la page seront impacté.

```css
p{
  color: green; /* Tous vos paragraphes seront écrit en vert */
}
```

## Sélecteur de hiérarchie

Pour sélectionner `<a>` descendant de `<p>` nous allons indiquer le chemin en séparant les élements par un espace:

```css
p a { ... }
```

## Sélecteur d'enfant 

Pour sélectionner `<a>` descendant **directement** de `<p>` nous allons indiquer le chemin en séparant les élements par un > :

```css
p > a { ... }
```

## Sélecteur de groupe

Pour sélectionner plusieurs éléments qui possèdent les mêmes valeurs, on les sépares par une virgule:

```css
h1, p { ... }
```

## Qu'est-ce qu'une classe

C'est un attribut que l'on donne à une balise HTML pour pouvoir la cibler plus facilement avec notre CSS.

On insère dans notre balise HTML un attribut **class** dont la **valeur** peut-être ce que vous voulez, soyez cohérent avec l'effet recherché.

```html
<p>Moi je serai jaune</p>
<p class="important">Mais moi je suis plus important du coup je serai en rouge</p>
```

```css
p{color: yellow;}
.important{color: red;}
```

Il est également possible d'utiliser plusieurs classes, on les sépare par des espaces tout simplement.

```html
<p class="important info">
```

> Ici la balise p prend 2 classes, `important` et `info`, qui sont définie dans la feuille de style.

Une classe peut être utilisé sur plusieurs balises dans la même document.

Il est également possible de cibler une balise HTML avec une classe. Pour ce faire on utilise la manière suivante:

```css
p.maClasse{ ... }
````

Cela ciblera tous les éléments `<p class="maclasse">`

Un autre exemple que vous verrez plus tard:

```html
<button type="button" class="btn btn-default"> ... </button>
```

```css
button.btn.btn-default{ ... } 
```

## L'identifiant (ID)

C'est la même chose qu'une classe sauf qu'il doit être unique sur la page, il sera moins utilisé. On ne peut utiliser qu'un id par balise. On le cible avec #

```html
<p id="monId">
```

```css
#monId { ... }
```

## On mélange tout!

Il est tout à fait possible de mélanger tous ces sélecteurs ensembles. Mais attention à ne pas créer du code CSS trop spécifique. 

```css
p#monId.maClasse { ... }
```

> :bulb: Ici on sélectionne tous les paragraphes qui ont la classe `maClasse` et l'id `monId`

## Espace

Si on ne met pas d'espace entre nos sélecteurs, cela signifie que toutes les conditions doivent être vraies. 

```css
p.important { ... }
```

> Dans l'exemple au dessus on ciblera tous les **paragraphes** qui ont une classe **important**

Si on met un espace, on cible la hiérarchie. 

```css
p .important { ... }
```

> Dans l'exemple au dessus on ciblera toutes les classes **important** qui ont sont descendants d'un paragraphe

Voyez comme un simple espace peut faire ou défaire votre page. Soyez attentif  et utilisez l'inspecteur de votre navigateur pour cibler plus facilement le problème.

## Le sélecteur de tout!

Pour sélectionner l'entièreté de notre page on peut utiliser `*`

```css
* {...}
```

:bulb: On peut combiner ce sélecteur avec d'autres pour sélectionner tous les éléments à l'intérieur d'un autre, par exemple: 

```css
p * {...}
```

> Sélectionnera tous les éléments à l'intérieur d'un `<p>`

## Convention de nommage

- un nom de classe ou d'ID ne doit pas avoir d'accent ou caractères spéciaux.
- On a tendance à éviter le "tout majuscule".
- Un nom d'ID ne prend jamais d'espace, sinon c'est une nouvelle ID.
- Un nom de classe ne prend jamais d'espace, sinon c'est une nouvelle classe.

[:arrow_up: Revenir au top](#table-des-matières)

## Pour finir 

Pas si compliqué, n'est-ce pas?

> :video_game: Petit jeu sympa pour s'entraîner aux sélecteurs: [http://flukeout.github.io/](http://flukeout.github.io/)

[:arrow_up: Revenir au top](#table-des-matières)

## Typographie

### font-family

```css
body{
  font-family: Arial, Helvetica, sans-serif;
}
```

Cette propriété définit la famille de police d'écriture à utiliser. Dans cet exemple, tout texte dans le `body` de votre page utilisera Arial en priorité, ensuite Helvetica si la police n'est pas disponible et pour finir n'importe quelle police sans-serif si les deux première ne sont pas sur l'ordinateur de l'utilisateur.

Voici une liste des polices dites "safe" à utiliser sur vos pages web: [https://www.cssfontstack.com/]

> :bulb: Mettez les liens dont on vous parle en favoris sur votre navigateur pour pouvoir les consulter plus tard en cas de besoin

Il est également possible d'utiliser les [polices Google](https://fonts.google.com/), qui sont très nombreuses. Les intégrer n'est pas très compliqué, on verra cela plus tard, mais si vous voulez essayer, n'hésitez pas!

[:arrow_up: Revenir au top](#table-des-matières)

### font-size

```css
body{
  font-size: 18px;
}
```

Définit la taille (hauteur) d'une police. On peut utiliser plusieurs unités (px, em,...)

[:arrow_up: Revenir au top](#table-des-matières)

### color

```css
body{
  color: red;
}
p{
  color: #222222;
}
a{
  color: rgba(255,0,0,0);
}
```

Définit la couleur de l'élément. Prends un **valeur hexadécimale**, **RGBA** ou **un mot-clé** (red, gray,...)

[:arrow_up: Revenir au top](#table-des-matières)

### text-align

```css
p{
  text-align: right;
}
```

Permet d'aligner le texte. Les valeurs sont: **left**, **right**, **center**, **justify** (comme sur Word).

> :bulb: Pour aligner une image, on peut la mettre dans un \<div> ou \<p> qui est aligné avec **text-align**, on verra comment "mieux" aligner une image plus tard.

[:arrow_up: Revenir au top](#table-des-matières)

## Arrière-plan

### border-radius

```css
h2{
  border: 5px;
  border-radius: 10px;
}
```

Définit un arrondis pour la bordure. Ne sert à rien si la propriété **border** n'est pas présente.

> :bulb: Comme pour la bordure, il est possible de définir un arrondis que pour certains coins avec la syntaxe suivante: `border-top/bottom-left/right-radius`
>
> On peut aussi écrire cela de façon plus simple: `border-radius: 2px 20px 5px 14px;` La première valeur commence en haut à gauche, puis suit les coins dans le sens horloger.

[:arrow_up: Revenir au top](#table-des-matières)

### background

```css
div{
  background: #6f1be4 url("img/image.png") no-repeat center;
}
```

[Une ressource contenant toutes les propiétés possibles pour le background](https://developer.mozilla.org/fr/docs/Web/CSS/background)

[:arrow_up: Revenir au top](#table-des-matières)

## Dimensions, margin et padding

### width & height (max & min)

> width = largeur
>
> height = hauteur

Prends comme valeurs: **auto**, **px**, **%** ou **em**

Il est également possible de préciser une valeur minimum ou maximum pour ces tailles.

```css
img{
  max-width: 100px;
}
```

> Dans cet exemple, l'image ne ferra jamais plus de 100 px de large.

[:arrow_up: Revenir au top](#table-des-matières)

### margin & padding

![marges](img/09/marges.png)

```css
// On aura des marges équivalente de chaque côté
.same{
  margin: 10px;
  padding: 5px;
}
  // On peut sélectionner chaque marge séparément
.different{
  margin-top: 10px;
  margin-bottom: 10px;
  margin-left: 5px;
  margin-right: 2px;
}
  // On peut sélectionner chaque marge séparément mais en une seule ligne en commençant par celle du haut puis en suivant le sens horloger
.different-but-one-line{
  margin: 10px 2px 10px 5px;
}
  // On peut sélectionner les marges du top et bottom et du left et right.
.different-one-line-two-values{
  margin: 10px 5px;
}
```

Ce qu'il faut retenir:

- `Padding`: marge intérieur
- `Margin`: marge extérieur
- Par défaut la valeur s'applique sur chaque côté (top, right, bottom, left) mais il est possible de préciser une valeur différente pour chaque côté.
- Peut s'écrire en une seule ligne (top, right, bottom, left)

[:arrow_up: Revenir au top](#table-des-matières)

## Display

Cette propriété va permettre une mise en forme avancée. Voici quelques valeurs possibles: **block**, **inline**, **inline-block**, **none**,... Certaines de ces valeurs sont appliquées par défaut en fonction des éléments (par exemple un `<p>` ou un `<div>` prend par défaut un **display:block**)

[:arrow_up: Revenir au top](#table-des-matières)

### display: block

```css
a{
  display: block;
}
```

Permet de changer les éléments **inline** en block. Par défaut il prend toute la largeur de son parent et est suivi d'un retour à la ligne.

Peux être modifié en **width** et **height**.

[:arrow_up: Revenir au top](#table-des-matières)

### display: inline

```css
p{
  display: inline;
}
```

Permet de transformer l'élément en type inline ce qui aura pour effet de le laisser sur une seule ligne.

Ne peux pas être modifié en **width** et **height**.

[:arrow_up: Revenir au top](#table-des-matières)

### display: inline-block

```css
p{
  display: inline-block;
}
```

Peux être modifié en **height** mais pas en **width**.

[:arrow_up: Revenir au top](#table-des-matières)

### display: none

```css
img{
  display: none;
}
```

Permet de retirer un élement de la page. Il ne sera plus visible et ne prendra plus de place. 

[:arrow_up: Revenir au top](#table-des-matières)

## L'auto-complete de VSCode

Si vous ne savez pas exactement quelle propriété existe ou comment elle s'écrit, VSCode est là pour vous aider. En effet quand vous travaillez dans un document CSS ou HTML enregistré, VSCode détecte votre syntaxe et vous aide à compléter votre frappe.

## Exercices !

J'espère que vous êtes prêt?! Je suis quand même gentil je vous laisse le choix entre deux niveaux de difficulté :
- 1er niveau : [Maquette Discord](https://github.com/sirius-school/initiation-html-css-2022/blob/main/1-html-css-debutant/11-exercice-css-maquette-discord.md)

- 2e niveau : [Maquette Feel the Music](https://github.com/sirius-school/initiation-html-css-2022/blob/main/1-html-css-debutant/20-exercice-css-maquette-feelthemusic.md)

[:arrow_up: Revenir au top](#table-des-matières)

[:rewind: Retour au sommaire du cours](../README.md#au-programme)

> Cours original: Julie Vanderbyse
>
> Modification: Jeremy Scala & Lucas Ielli