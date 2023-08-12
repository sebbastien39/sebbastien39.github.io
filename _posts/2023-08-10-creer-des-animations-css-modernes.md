---
layout: post
title:  "Créer des animations CSS modernes"
date:   2023-08-10 11:44:12 +0200
categories: css animation
---

Objectif :

- réaliser vos premières animations CSS;
- maîtriser les translations, les rotations et l’opacité;
- réaliser des animations dynamiques.

Les techniques d'animation sont nombreuses : JavaScript, SVG, Canvas, WebGL mais surtout CSS. Le couplage CSS3/HTML5 fait partie des techniques les plus utilisées pour créer des animations web.

Nous allons écrire des bouts de CSS pour faire évoluer l’apparence d’éléments HTML sur une certaine durée. Par exemple l’animation de la couleur d’un bouton.

## Créez des animations simples avec les transitions

2 moyens de créer des animations en CSS : les ***transitions***, et les ***keyframes***.

### Transitions

permettent à un élément de passer d'un état A à un état B.

Pour créer une transition, vous aurez besoin de plusieurs informations :

- une propriété CSS à modifier ;
- une valeur initiale pour votre propriété CSS ;
- une valeur finale pour cette même propriété ;
- une durée ;
- un événement (une pseudoclass) pour déclencher l'animation (transition).

Exemple d'un bouton : 

```html
<body>
    <div class="container">
        <div class="btn">
            Vois comme je grandis !
        </div>
    </div>
</body>
```

```scss
$cd-btn: #011c37;
$cd-txt: #15DEA5;
.btn {
    background: $cd-btn;
    color: $cd-txt;
    font-size: 3rem;
    cursor: pointer;
    padding: 1.85rem 3rem;
    border-radius: 10rem;
}
```

__Passez d’un état A à un état B__

`transition-property` : déclarer une transition.

`transition-duration` : durée que prendra la transition.

pseudoclasse `:hover` pour déclencher notre transition.Les pseudoclasses sont en quelque sorte le if/else du CSS.

### Maîtrisez les propriétés raccourcies

***propriété raccourcie*** `transition`

```css
transition-property: transform;
transition-duration: 400ms;
```

est équivalent à :

```css
transition: transform 400ms;
```

```scss
$cd-btn: #011c37;
$cd-txt: #15DEA5;
.btn {
    background: $cd-btn;
    color: $cd-txt;
    font-size: 3rem;
    cursor: pointer;
    padding: 1.85rem 3rem;
    border-radius: 10rem;
    //Début code animation Bouton
    transition: transform 400ms; //Déclarer transition sur sélécteur .btn + Durée de la transition
    &:hover { //Pseudoclass qui déclenche le changement d'état
        transform: scale(1.15); //Fonction scale
    }
}
```
## Déclenchez vos transitions avec les pseudoclasses

`:hover`, qui est déclenché au survol de la souris;

`:active`, activé au clic de l'utilisateur (le plus souvent pour les liens et boutons);

`:focus`, qui se déclenche lorsque son élément reçoit le focus (soit il est sélectionné à l'aide du clavier, soit il est activé avec la souris);

`:valid`, dont la validation du contenu s'effectue correctement par rapport au type de donnée attendu;

`:invalid`, qui inversement, correspond à un élément dont la validation du contenu ne s'effectue pas correctement par rapport au type de donnée attendu;

`:not()`, qui correspond à la négation. Elle prend un sélecteur en argument et permet de cibler les éléments qui ne sont pas représentés par cet argument;

`:checked`, qui correspond aux input de type checkbox, option ou radio qui sont cochés ;

`:enabled`, un élément avec lequel on peut interagir ;

`:disabled`, qui correspond à un élément dont l'interaction a été bloquée.

[liste pseudoclass](https://developer.mozilla.org/fr/docs/Web/CSS/Pseudo-classes)

Les pseudoclasses sont essentielles pour déclencher une transition en CSS. Une transition peut également être déclenchée par un changement de classe en JavaScript, même si nous ne verrons pas cette technique ici.

### Validez un formulaire

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340914-declenchez-vos-transitions-avec-les-pseudoclasses#/id/r-6333192)

## Appliquez les 12 principes de l’animation au web

Les 12 principes de l'animation sont :

- Squash and Stretch ;
- Anticipation ; 
- Staging (mise en scène) ;
- Straight Ahead and Pose to Pose ; 
- Follow Through and Overlapping Action ; 
- Slow in and slow out ;
- Arc ;
- Secondary Action ;
- Timing ;
- Exaggeration (exagération) ; 
- Solid Drawing (notion de volume) ;
- Appeal (charisme).

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340915-appliquez-les-12-principes-de-l-animation-au-web)

## Créez des transitions CSS à propriétés multiples

Faire une superposition d’effets de mouvement, afin d’obtenir une animation qui paraît bien plus authentique aux yeux de l’utilisateur.

### Créez des animations naturelles en combinant les transitions

Créer une action secondaire au survol de la souris

```scss
.btn {
    background-color: $cd-btn-start;
    border: 4px solid $cd-btn;
    border-radius: 10rem;
    cursor: pointer;
    font-size: 3rem;
    padding: 1.85rem 3rem;
    &:hover {
        transform: scale(1.13);
        background-color: $cd-btn-end; //Action secondaire au survol souris
    }
}
```

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340916-creez-des-transitions-css-a-proprietes-multiples)

### Séparez les propriétés

```scss
    &:hover {
        transition: transform 450ms, background-color 300ms;
        transition-delay: 0, 150ms;
    }
```
ou

```scss
    &:hover {
        transition: transform 450ms, background-color 300ms 150ms;
    }
```

## Créez des animations plus naturelles avec les fonctions de timing

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340917-creez-des-animations-plus-naturelles-avec-les-fonctions-de-timing)

---

## Optimisez les performances de votre navigateur pour vos animations CSS

🇺🇸 FPS - Frames Per second / 🇫🇷 IPS - Images Par seconde

En animation web, on vise 60 FPS ( = à 60 hz des écrans).

Le nombre d’images par seconde de nos animations est variable. Pour y remédier, il suffit de suivre certaines bonnes pratiques dans la manière d'écrire vos animations CSS.

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340918-optimisez-les-performances-de-votre-navigateur-pour-vos-animations-css)

En d’autres termes, il ne faut animer que des propriétés qui font partie de l’étape composition. Les plus adaptées sont donc `transform` et `opacity`.

## Créez des animations fluides avec la propriété CSS transform

La meilleur manière de créer des animations fluides est d'utiliser les propriétés `transform` et `opacity`.

### transform

`transform` dispose de plus d'une vingtaine de fonctions pour : ***grossir, pivoter, déplacer, tordre*** un élément.

__Modifiez la taille d'un élément avec `scale`__ [source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340919-creez-des-animations-fluides-avec-la-propriete-css-transform#/id/r-6426988)

__Modifiez la position d'un élément `translate`__ [source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340919-creez-des-animations-fluides-avec-la-propriete-css-transform#/id/r-6427040)

__Faites pivoter vos éléments avec `rotate()`__ [source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340919-creez-des-animations-fluides-avec-la-propriete-css-transform#/id/r-6427121)

> Pour animer les propriétés d’un objet en CSS, elles doivent se trouver à côté de l’élément suivant dans la hiérarchie. 

__Combinez les fonctions `scale`, `position` et `rotate`__ [source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340919-creez-des-animations-fluides-avec-la-propriete-css-transform#/id/r-6427415)

__Incliner des objets horizontalement ou verticalement `skew()`__ [source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340919-creez-des-animations-fluides-avec-la-propriete-css-transform#/id/r-6427486)

__les transformations en 3D `perspective()`__ [source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340919-creez-des-animations-fluides-avec-la-propriete-css-transform#/id/r-6498983)

## Modifiez le point d’ancrage d’un élément grâce à transform-origin

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340920-modifiez-le-point-d-ancrage-d-un-element-grace-a-transform-origin)

La propriété `transform-origin` permet de déplacer un point d’ancrage où on veut, pour faire partir nos animations de ce point.

### Déplacez le centre








## Analysez la performance de vos animations avec Chrome DevTools

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340921-analysez-la-performance-de-vos-animations-avec-chrome-devtools)

DevTool > ***Performance*** , permet d’enregistrer et d’analyser comment une page se charge, réagit, et s’anime.

## Animez les couleurs de manière performante avec opacity

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340922-animez-les-couleurs-de-maniere-performante-avec-opacity)

 La propriété `opacity` permet de faire des transitions de couleur sans que le navigateur fasse des calculs de type “paint”. La performance reste donc optimale.

 /!\ Ne pas utilisé ~~background-color~~

Pseudoélément `::after`

pseudoclasse `:`  
pseudoélément `::`

La propriété `content` est indispensable au fonctionnement des pseudoéléments. Elle permet de remplir un pseudoélément de texte ou d’images et d’assigner une valeur (chaine de caractère vide) au pseudoélément dans le cas d'un bouton `content: "";`.

[content, dans le cas d'un bouton](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340922-animez-les-couleurs-de-maniere-performante-avec-opacity#/id/r-6428893)

### Découvrez les dégradés

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340922-animez-les-couleurs-de-maniere-performante-avec-opacity#/id/r-6429394)

// Fin mouvement des élément d'un point A à un point B, les ***transitions***, avec une valeur de départ et une valeur de fin. Il est possible d changer le timing de la transition.

## Créez des animations plus complexes avec la règle CSS @keyframes

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340923-creez-des-animations-plus-complexes-avec-la-regle-css-keyframes)

***Keyframes*** étapes qui compose une animation CSS.

### Définissez vos keyframes

Les ***transitions***, qui sont à usage unique, n'existent qu'à l'intérieur du sélecteur où elles ont été déclarées.

Les ***@keyframes*** sont disponibles globalement, ne sont pas déclarés dans un sélecteur mais au niveau de base du fichier CSS, n'importe quel sélecteur dans notre fichier CSS peut les utiliser.

__Déclarer une Keyframe__ :

```scss
@keyframes progress-bar {
    
}
```

```js
@keyframes progress-bar{
    0% {    //keyframe défini en utilisant son pourcentage
        transform: scaleX(0); //propriétés entre {}
    }
    100% {
        transform: scaleX(1);
    }
}
```

__keyframes de début et de fin sans rien au milieu__

```scss
// Pas besoin de %
@keyframes progress-bar{
    from {
        transform: scaleX(0);   
    }
    to {
        transform: scaleX(1);
    }
}
```

### Passez à l'action

`animation-name`
`animation-duration`

## Utilisez les propriétés de l'animation CSS

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6341109-utilisez-les-proprietes-de-lanimation-css)

### Comprenez la différence entre ***@keyframes*** et ***transition***

2 techniques ayant des logiques différentes, car elle ne répondent pas au même objectif.

### Déclenchez vos animations dès le chargement de la page

Avec les @keyframes, nous pouvons déclencher une animation dès le chargement d'un élément.

Nous pouvons créer des animations sur notre site web pour introduire des éléments au fur et à mesure de leur chargement.

### Ajoutez un délai à votre animation @keyframes

`transition-delay` permet de retarder (seulement) les transitions.

`animation-delay` retarde les animations conçues avec des @keyframes.

```scss
.progress {
    &__bar {
        animation: progress-bar 1000ms 150ms;
    }
}
```

### Étendez les propriétés de vos keyframes avec animation-fill-mode

## Manipulez et réutilisez les animations CSS

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340941-manipulez-et-reutilisez-les-animations-css)

### Repensez votre validation d'email

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340941-manipulez-et-reutilisez-les-animations-css#/id/r-6434075)

### Créez des émotions avec vos animations

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340941-manipulez-et-reutilisez-les-animations-css#/id/r-6490707)

### Faites boucler vos animations à l'infini

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340941-manipulez-et-reutilisez-les-animations-css#/id/r-6490715)

`infinite`

### Faites une pause

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340941-manipulez-et-reutilisez-les-animations-css#/id/r-6490721)

`animation-play-state`

`random()`

## Affinez vos animations CSS avec DevTools

[source](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340942-affinez-vos-animations-css-avec-devtools)

## +

[liens](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes/6340949-resume-du-cours#/id/r-6464730)
