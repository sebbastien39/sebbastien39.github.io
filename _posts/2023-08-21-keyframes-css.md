---
layout: post
title: "@keyframes / CSS"
date: 2023-08-21 23:31:21 +0200
categories: css keyframes
---

Les animation css sont définient par les @keyframes.


```css
@keyframes wipe-enter {
        0% {
                transform: scale(0, .025);
        }
        50% {
                transform: scale(1, .025);
        }
}
```

Ensuite, utiliser l’animation sur un élément avec `animation-name`.

`animation-duration` durée de l'animation.

`animation-iteration-count` x fois animation jouée.

```css
@media (prefers-reduced-motion: no-preference) {
  .square {
    animation-name: wipe-enter;
    animation-duration: 1s;
    animation-iteration-count: infinite;
  }
}

// Equivalent

@media (prefers-reduced-motion: no-preference) {
  .square {
    animation: wipe-enter 1s infinite;
  }
}
```
---

On ajoute une class CSS (square-animation) pour contrôler le moment où l'animation est lue.

```html
<div class="square square-animation"></div>
```

```css
.square {
  width: 200px;
  height: 200px;
  background: orange;
  // etc...
}

@media (prefers-reduced-motion: no-preference) {
  .square-animation {
    animation: wipe-enter 1s 1;
  }
}
```

Il faut ajouter la class CSS (square-animation) à l'élément pour que que l'animation se lance.

Ceci est possible en cliquant sur un bouton.

Mais aussi possible en scrollant et visible à l'écran.

Il existe trois façons de déterminer quand l'élément défile dans la vue :

- Use the Intersection Observer API
- Measure the element's offset when the user scrolls
- Use a third-party JavaScript library that implements #1 or #2

Le mieux pour une animation de base déclenchée par défilement, API Intersection Observer car elle nécessite moins de code et est meilleure pour les performances.

## créer un observateur 

```js
// Create the observer
const observer = new IntersectionObserver(entries => {
  // Loop over the entries
  entries.forEach(entry => {
    // If the element is visible
    if (entry.isIntersecting) {
      // Add the animation class
      entry.target.classList.add('square-animation');
    }
  });
});

// Tell the observer which elements to track
observer.observe(document.querySelector('.square'));
```

`isIntersecting` soit vrai (visible), soit faut (non visible).

## Pour relire l'animation - supprimer la class de l'animation

Il est préférable d'envelopper (square-wrapper) l'élément que vous souhaitez animer dans un élément qui ne changera pas de taille ou de position.

Nous observons avec le container (square-rapper), et appliquons l'animation sur l'élément (square).

```js
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    const square = entry.target.querySelector('.square');

    if (entry.isIntersecting) {
      square.classList.add('square-animation');
	  return; // if we added the class, exit the function
    }

    // We're not intersecting, so remove the class!
    square.classList.remove('square-animation');
  });
});

observer.observe(document.querySelector('.square-wrapper'));
```

## Code final

### HTML

Container qui ne change pas : square-wrapper



```html
<div class="square-wrapper">
  <div class="square"></div>
</div>
```

### CSS

```css
.square {
  width: 200px;
  height: 200px;
  background: orange;
  // etc...
}

@media (prefers-reduced-motion: no-preference) {
  .square-animation {
    animation: wipe-enter 1s 1;
  }
}

@keyframes wipe-enter {
	0% {
		transform: scale(0, .025);
	}
	50% {
		transform: scale(1, .025);
	}
}
```

### JS

```js
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    const square = entry.target.querySelector('.square');

    if (entry.isIntersecting) {
      square.classList.add('square-animation');
	  return; // if we added the class, exit the function
    }

    // We're not intersecting, so remove the class!
    square.classList.remove('square-animation');
  });
});

observer.observe(document.querySelector('.square-wrapper'));
```