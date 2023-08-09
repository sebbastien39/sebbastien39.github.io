---
layout: post
title:  "Simplifiez-vous le CSS avec Sass"
date:   2023-08-09 17:06:22 +0200
categories: sass css
---

![](/assets/images/2023-08-09 17-40-35.png)
![](/assets/images/2023-08-09 17-41-14.png)

[source](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8069768-tirez-un-maximum-de-ce-cours)

## Simplifiez votre code

Trouver les répétitions / Les réunirent dans une class / Réutiliser ces class pour éviter de nouvelles répétitions

Méthode ***DRY*** (don’t  repeat yourself)
***Refactoring*** : (refactorisation) amélioration du code

Exemple pour un bouton générique (.btn) qui reprend toutes les propriétés communes des autres boutons.

Puis appliquer les propriétés additionnelles ( .btn-orange), en complément de notre sélecteur générique. Nous allons donc appliquer plusieurs règles CSS pour obtenir notre bouton.

__Les priorités__ :

1. ***inline*** (balise HTML) - CSS dans HTML - /!\ Déconseillé !
2. ***ID*** - évitez d’utiliser des id dans vos sélecteurs. ne peut être utilisé qu'une fois dans le code, utilisé dans le cas de valeurs uniques, utile en JavaScript, pour reconnaître certaines balises.
3. ***class*** - permet d’appliquer style à plusieurs éléments
4. ***les éléments*** - nom de la balise HTML div, h1, p …

***pseudoclass*** : mot clé ajouté à un sélécteur		ex : :hover

> inline > id > pseudoclasses > pseudoéléments

## convention BEM

(Bloc Element Modificator) toujours implémentés sous forme de classes.

bloc : `.navbar { color:red }``

élément : `.navbar__logo { background-color: blue }` ou `.navbar__link { background-color: yellow }`

modificator : `.navbar__link–red { color: red }`


## Sass

Le Sass doit être compiler en CSS pour être compréhensible par navigateur web.

2 manière d’écrire du Sass et donc 2 extension de fichier - `.sass` et `.scss`

__.scss s’appuie sur la syntax standard CSS__

```scss
//scss
.nav {
    text-align: right;
    .nav__link {
        font-size: 15px;
        padding-left: 30px;
        .nav__link--purple {
            color: #a5b4fc;
    }
  }
}
```
__.sass__

```scss
//Sass
.nav
  text-align: right

 .nav__link
    font-size: 15px
    padding-left: 30px

  .nav__link--purple
      color: #a5b4fc;
```

### nesting

placer un sélecteur dans un autre sélecteur.

```scss
.nav {
    text-align: right;
    .nav__link {
        font-size: 15px;
        padding-left: 30px;
        .nav__link--purple {
            color: #a5b4fc;
    }
  }
}
```

Ce qui donne - après génération en CSS :

```css
.nav {
  text-align: right;
}

.nav .nav__link {
  font-size: 15px;
  padding-left: 30px;
}

.nav .nav__link .nav__link--purple {
  color: #a5b4fc;
}
```

[sassmeister](https://www.sassmeister.com/) permet de coder en Sass ou SCSS, et d’observer en temps réel le code CSS compilé.

### Variables

permettent de stocker des valeurs répétées fréquemment.	Trés utiles pour changer toutes les couleurs d'un site en cas de remise au goût du jour par exemple.

```scss
//Déclaration de la variable
$main-color: red;

.header {
  background-color: $main-color; //Récupèration de la valeur
}

.footer {
  background-color: $main-color; //Récupèration de la valeur
}
```

### Mixins

stockent plusieurs valeurs.

```scss
//Déclaration mixin
@mixin nomMixin {
    text-shadow: 10px 10px red;
}

.nav {
    color: white;
    @include nomMixin; //Appel de la mixin
}
```

## Combinateurs

__combinateur descendant (enfant)__ `>`

__Combinateur adjacent__ `+`

__Concaténer sélécteur parent enfant avec__ `&`

[source](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8142701-optimisez-la-lecture-du-code)


## Combinez les variables et les mixins

***modifier*** votre mixin pour qu’elle se comporte différemment selon des paramètres.

Si vous placez des parenthèses entre le nom de votre mixin et les accolades, et qu’entre ces parenthèses vous mettez un argument (ou plusieurs), votre mixin devient customisable.

```scss
@mixin nomMixin($color){
    text-shadow: .55rem .55rem #0f0f1c;
}
```
`$color`  ressemble fort à une variable, non ? C’est l’argument. Les arguments, c’est comme des variables vides qui ne vivent que dans la mixin. Vous choisissez leur valeur à chaque fois que vous placez la mixin dans votre code, et cette valeur est utilisée dans le bloc de la mixin quand il est compilé en CSS :

```scss
@mixin title-shadow($color){
    text-shadow: .55rem .55rem $color;
}
```

Sass remplacera la variable `$color` avec la valeur de couleur que vous choisirez pour créer l’ombre.

```scss
.intro__title {
    @include text-shadow(#fff);
}
```

[source](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8142726-utilisez-les-variables-et-mixins#/id/r-8187267)

## Améliorez vos mixins grâce aux fonctions

[documentation](https://sass-lang.com/documentation/modules/color/)

Les ***fonctions*** sont des bouts de code préfabriqués qui effectuent des tâches, comme par exemple prendre un argument, le modifier et renvoyer la nouvelle valeur sans que vous n’ayez à le faire vous-même.

### Utilisez une fonction avec votre mixin

```scss
@mixin title-shadow {
 text-shadow: .50rem .50rem $dark-purple;
}
```

Nous allons remplacer `$dark-purple` par la fonction darken. Nous voulons que notre ombre s’adapte à la couleur du titre, et donc `$title-color`.

```scss
@mixin title-shadow {
  text-shadow: .50rem .50rem darken($title-color,  35%);
}
```

Nous avons :

1. Remplacé $darken-purple  par la fonction  darken  .

2. Passé $title-color  en premier argument.

3. Passé le pourcentage à appliquer pour assombrir notre couleur $title-color  en deuxième argument : ici 35 %.

## Adaptez votre code sur tous supports

[source](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8142736-adaptez-votre-code-sur-tous-supports)

## Déployez votre code Sass en ligne

[source](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8142741-deployez-votre-code-sass-en-ligne#/id/r-8154934)

## Installer Sass en locale

[source](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8142741-deployez-votre-code-sass-en-ligne#/id/r-8154995)

## +

[liens](https://openclassrooms.com/fr/courses/8069761-simplifiez-vous-le-css-avec-sass/8142686-passez-au-niveau-superieur-avec-sass#/id/r-8153826) [sassmeister](https://www.sassmeister.com/)