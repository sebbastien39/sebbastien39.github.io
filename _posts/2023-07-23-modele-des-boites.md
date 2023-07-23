---
layout: post
title:  "Modèle des boîtes"
date:   2023-07-23 12:27:15 +0200
categories: modèle boîte css
---

Types de balises HTML :

***block*** : ce type de balise crée automatiquement un retour à la ligne avant et après; 

***inline*** : ce type se trouve obligatoirement à l'intérieur d'une balise block. 

Il existe d'autres types : `table-cell`, `list-item`...

![](/assets/images/2023-07-23 13-33-36.png)

Il existe deux balises génériques (universelles) - on peut leur appliquer une  class  (ou un  id  ) pour le CSS quand aucune autre balise ne convient : 

La balise`<span>`(qui est de type inline).  
La balise`<div>`(qui est de type block).

Par défaut, un bloc prend 100 % de la largeur disponible.

Contrairement à un inline, un block peut avoir une largeur et une hauteur précises grâce à ces deux propriétés CSS, ***width*** et ***height***.

## margin / padding

***margin*** - taille de la marge extérieure.  
***padding*** - taille de la marge intérieure.

![](/assets/images/2023-07-23 13-43-22.png)

On distingue deux principaux types de balises en HTML :

les balises de type  block  comme `<p>` ou `<h1>` créent un retour à la ligne et occupent par défaut toute la largeur disponible. Elles se suivent de haut en bas ;

les balises de type  inline  comme `<a>` ou `<strong>` délimitent du texte au milieu d'une ligne. Elles se suivent de gauche à droite.

On peut modifier la taille d'une balise de type block  avec les propriétés CSS  width (largeur) et  height (hauteur).

Les éléments de la page disposent chacun de padding (marges intérieures) et de margin (marges extérieures).

On peut centrer le contenu d'un bloc dont la largeur est définie par `width` avec `margin: auto;`

## +

[source](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3/8061365-decouvrez-le-modele-des-boites)