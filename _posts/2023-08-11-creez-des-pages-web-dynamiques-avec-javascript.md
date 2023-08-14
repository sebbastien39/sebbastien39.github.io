---
layout: post
title: "Créez des pages web dynamiques avec Javascript"
date: 2023-08-11 16:49:24 +0200
categories: javascript
---

À la fin de ce cours, vous serez capable de :

- Créer une interface web à partir de données existantes ;
- Rendre votre page web interactive ;
- Interagir avec un service web à l’aide d’une API HTTP ;
- Enrichir vos pages web grâce aux librairies.

## Préparez votre projet

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7910981-preparez-votre-projet)

Pour développer un site web depuis zéro, vous utiliserez le format SQL et vous stockerez les données sur un serveur de base de données.

Pour manipuler des données exportées d’un logiciel ou des fichiers de sauvegarde d’un projet, vous utiliserez plutôt les formats CSV, XML ou JSON, et vous stockerez les données dans des fichiers.

Enfin, pour interagir avec des API en ligne, vous devrez utiliser le format JSON pour les API récentes. Certaines API utilisent aussi le format XML, mais leur nombre reste assez limité. Le JSON a l’avantage d’être plus concis que les autres formats textuels, et d’être facilement compréhensible par les navigateurs.

[API](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7910981-preparez-votre-projet#/id/r-7908437) - Application Public Interface

### npm

NodeJS est un Framework de serveur open source basé sur JavaScript qui est principalement utilisé pour créer des applications de serveur backend avec JavaScript. Il est basé sur le moteur JavaScript V8 de Chrome. Npm est le gestionnaire de packages par défaut pour NodeJS.

[source](https://ubunlog.com/fr/nodejs-npm-instalacion-ubuntu-20-04-18-04/)

```bash
npm run dev
```

`localhost:8080`

## Exploitez des données au format JSON

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911021-exploitez-des-donnees-au-format-json)

La syntaxe JSON : (JavaScript Object Notation) est issu du langage JavaScript, il est utilisé par des programmes écrits dans d’autres langages, comme Python, le C ou le PHP. Il a donc vocation à s’adapter à cette diversité d’environnements.

Il dispose de :

- 4 types primitifs : les nombres, les textes, les booléens, la valeur null ;
- 2 types structurants : les objets et les tableaux.

[définition nombre](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911021-exploitez-des-donnees-au-format-json#/id/r-7908524)

> JavaScript permet de délimiter les chaînes de caractères de deux autres manières : avec le guillemet simple ***'*** et le back tick ***`*** . JSON n’a conservé que le double guillemet. Attention à n’utiliser que ce dernier lorsque vous écrivez en JSON.

### Indentation

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911021-exploitez-des-donnees-au-format-json#/id/r-7911537)

## Générez le contenu de votre page grâce au DOM

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911057-generez-le-contenu-de-votre-page-grace-au-dom)

![](/assets/images/2023-08-11 18-39-42.png)

### Importez les données de notre fichier JSON

Fonction `fetch` pour manipuler les données du document JSON.

```js
// Récupération des pièces depuis le fichier JSON
const reponse = await fetch("pieces-autos.json");
const pieces = await reponse.json();
```

### Créez de nouveaux éléments du DOM

avec la fonction ***document.createElement***

```js
const article = pieces[0];

const imageElement = document.createElement("img");
imageElement.src = article.image;

const nomElement = document.createElement("h2");
nomElement.innerText = article.nom;

const prixElement = document.createElement("p");
prixElement.innerText = `Prix: ${article.prix} €`; //template strings

const categorieElement = document.createElement("p");
categorieElement.innerText = article.categorie;
```

### rattaché l'élément au reste du document

Pour faire ce rattachement, nous avons besoin d’un parent et de la fonction ***appendChild***

```js
const sectionFiches = document.querySelector(".fiches"); //Le parent
sectionFiches.appendChild(imageElement);
sectionFiches.appendChild(nomElement);
sectionFiches.appendChild(prixElement);
sectionFiches.appendChild(categorieElement);
```

### Choisir entre deux possibilités grâce à l’opérateur ternaire

L’***opérateur ternaire*** s’utilise lorsque l’on doit choisir entre deux possibilités.

> La syntaxe générale de l’opérateur ternaire est formulée ainsi :  
expression à tester ? valeur si vrai : valeur si faux.

```js
//Donc
article.prix < 35 ? "€" : "€€€"
```

```js
// …
const prixElement = document.createElement("p");
prixElement.innerText = `Prix: ${article.prix} € (${article.prix < 35 ? "€" : "€€€"})`;
// ...
document.body.appendChild(prixElement);
```

### Fournir une valeur par défaut grâce à l’opérateur `nullish`

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911057-generez-le-contenu-de-votre-page-grace-au-dom#/id/r-7911087)

L’opérateur nullish s’utilise lorsque vous pensez avoir une information dans une variable mais que finalement, il n’y en a pas.

> L’opérateur s’écrit avec deux ?? sous la forme suivante :  
expression à tester ?? valeur de substitution

```js
categorieElement.innerText = article.categorie ?? "(aucune catégorie)";
```

---

## Manipulez les listes en JavaScript

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911102-manipulez-les-listes-en-javascript)

### Affichez plusieurs éléments en parcourant les listes

__Affichez plusieurs fiches produits grâce à la boucle for__

Les boucles permettent de répéter du code.

Il existe trois boucles différentes :

- la boucle `while` permet de répéter des instructions tant qu’une condition de test est vraie ;

- la boucle `do while` permet d'exécuter au moins une fois une instruction avant de vérifier s’il faut la répéter;

- la boucle `for` est utilisée lorsqu’on sait à l’avance combien de fois on doit exécuter la boucle.

__Réordonnez et filtrez les fiches produits grâce aux fonctions `sort` et `filter`__

[source](https://openclassrooms.com/fr/courses/7697016-creez-des-pages-web-dynamiques-avec-javascript/7911102-manipulez-les-listes-en-javascript#/id/r-7911112)



fonction filter (argumentqui est une fonction anonyme)

