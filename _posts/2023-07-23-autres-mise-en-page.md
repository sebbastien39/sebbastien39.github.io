---
layout: post
title:  "Autres mise en page CSS"
date:   2023-07-23 14:42:25 +0200
categories: autre mise en page css
---

La propriété `display` permet de ***changer le comportement de base d'un élément*** : 

- transformer un élément  inline  en  block  ;

- inversement, un élément  block  en  inline  ;

- mais aussi de faire un mélange des deux avec  inline-block.

`position` : permet de positionner avec précision un élément sur une page.

Le positionnement ***relatif*** permet de décaler un bloc par rapport à sa position normale.

Le positionnement ***absolu*** permet de placer un élément où l'on souhaite sur la page, au pixel près.

Un élément A positionné en absolu à l'intérieur d'un autre élément B (lui-même positionné en absolu, fixe ou relatif) se positionne par rapport à l'élément B, et non par rapport au coin en haut à gauche de la page.

Lorsque plusieurs éléments s'empilent, il est possible de les ordonner avec `z-index`.

## +

Masquer élément avec `display: none;`

Pour qu'un élément reste à l'écran `position: fixed / sticky;`, - menu de Nav par ex.

[source](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3/8061421-abordez-dautres-techniques-de-mise-en-page)