---
layout: post
title: "Media-queries - CSS - 23"
date: 2023-10-21 11:31:25 +0200
categories: css
---

Media-Querie : Règles CSS qui permettent de modifier l'apparence d'un site web en fonction de l'appareil (taille d'écran).

```css
@media screen and (max-width: 1200px) {
/* Insérez vos propriétés CSS ici, avec vos sélecteurs*/
}
```

Breackpoint : point de rupture

```css
/* Sur les écrans, quand la largeur de la fenêtre fait au maximum 1280px */
@media screen and (max-width: 1280px)
/* Sur tous types d'écran, quand la largeur de la fenêtre est comprise entre 1024px et 1280px */
@media all and (min-width: 1024px) and (max-width: 1280px)
/* Sur tous types d'écrans orientés verticalement */
@media all and (orientation: portrait)
```