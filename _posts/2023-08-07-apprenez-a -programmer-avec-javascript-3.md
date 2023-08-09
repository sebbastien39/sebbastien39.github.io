---
layout: post
title:  "Apprenez à Programmer avec Javascript III"
date:   2023-08-07 23:59:35 +0200
categories: Javascript
---

## Récupérez la valeur d’un champ de formulaire

//vidéo

Un formulaire est le moyen le plus simple de demander quelque chose à l'utilisateur et d'obtenir une réponse. Mais il y a plein de champs différents. Des champs de texte, des cases à cocher, des boutons radios etc. En fonction de ces champs, les valeurs ne sont pas récupérées de la même manière.

Avec un champ de texte libre, on récupère la valeur telle qu'elle est tapée. C'est le cas pour 80% des éléments de formulaire.

Deuxième type de champ, les cases à cochées "checkbox", là on a 2 valeurs, vrai ou faux. Dans ce cas on utilise la propriété "checked" qui vaut soit true soit false.
Le type de champ le plus compliqué est le bonton radio. Là pour la même donnée, on va devoir vérifier laquelle des cases est sélectionée. On a plusieurs réponse possible, donc plein d'éléments qui se réfaire à la même valeur. On va donc bonclé deçu avec une boucle for ou while jusqu'à ce qu'on trouve le bouton qui est coché. Là seulement, on pourra récupérer la valeur de ce bouton.

C'est un peu plus complexe, mais avec ces 3 méthodes, on peut tout récupérer.

Écrire le formulaire en lui même, ne pose pas de problème particulier. Javascript créé un événement submit lors de l'envoie du formulaire au serveur et recharge l'intégralité de la page. C'était quelque chose de nécessaire à l'époque de sa création. Il est aujourd'hui nécessaire de neutraliser cet événement par défaut. Pour ça, il faut récupérer l'événement submit et lui  attribuer l'action ***event.preventDefault***, comme ça on évite le rechargement de la page.

// Fin vidéo

### Découvrez les différents types de champs de formulaire

À ce stade du projet, notre objectif est de répondre aux questions suivantes :

- Comment permettre aux utilisateurs de saisir des informations sur notre page web ?

- Comment leur permettre d’interagir avec le contenu ?

La réponse se trouve dans la gestion des formulaires, qui sont un élément clé des pages web interactives. Un formulaire est un regroupement de champs que l'utilisateur peut utiliser pour saisir des données.

Mais… notre page web contient déjà un champ de formulaire, non ?

Exactement ! Mais il existe une grande variété de champs en programmation, en fonction du type de données utilisé (nombres, texte, e-mail, dates…). Concrètement, dans votre code, cela ressemble à l’exemple ci-dessous :

```js
<form>
    <label for="name">Nom</label>
    <input type="text" id="name" name="name" placeholder="Votre nom" required>
    <label for="email">Email</label>
    <input type="email" id="email" name="email" placeholder="Votre email" required>
    <label for="message">Message</label>
    <textarea id="message" name="message" placeholder="Votre message" required></textarea>
    <input type="submit" value="Envoyer">
</form>
```

Un formulaire est composé d’une balise form qui englobe une série d’autres balises qui composent le formulaire : labels, input, texterea et select.

Mais je ne comprends plus… On parle de champs ou de balises ? 🤨

> En fait, on parle de champ ou de champ de saisie pour évoquer les éléments qui permettent à l’utilisateur de saisir une donnée dans un formulaire. Mais, en HTML, ces champs sont rédigés grâce à des balises dédiées : input, textarea, select…

Revenons en détail sur chacune d’entre elles… 😉

__Les balises labels__

Les balises labels servent à indiquer un texte, lié au champ que l’utilisateur va devoir remplir. 

__Les balises input__

Les balises input (“entrée”, en français) forment le cœur des formulaires. Elles permettent à l’utilisateur de saisir des données. D’ailleurs, nous en avons déjà utilisé une dans notre projet. Eh oui, rappelez-vous, c’est grâce à cela que le joueur peut maintenant saisir le mot qu’il doit recopier.

```js
<input type="text" id="inputEcriture" name="inputEcriture">
```

> Dans cet exemple, l’attribut ***type=***”text” permet de définir le type de données que l’utilisateur peut saisir :

    text : pour saisir un texte ;

    password : pour saisir un texte tout en cachant ce qui est saisi ;

    email : pour saisir un texte et vérifier que son format correspond bien à celui d’un e-mail ; 

    number : pour saisir un nombre ; 

    checkbox : pour afficher une case à cocher ;

    radio : pour afficher un bouton radio, c’est-à-dire un bouton qui permet à l'utilisateur de sélectionner un seul élément dans une liste ;

    date : pour saisir une date à l’aide d’un calendrier qui s’affiche au clic sur le champ.

N’hésitez pas à explorer la [documentation](https://developer.mozilla.org/fr/docs/Web/HTML/Element/input) pour découvrir d’autres types de données.

__Les balises textarea__

La balise input de type texte ne comporte qu’une seule ligne. Elle n’est donc pas indiquée pour saisir une grande portion de texte, comme un commentaire. Dans ce cas, la meilleure solution est d’utiliser une balise ***textarea***, dans laquelle il sera plus pratique d’écrire des paragraphes :

```js
<textarea name="textarea" id="textarea"></textarea>
```

__Les balises select__

La ***balise select*** permet de créer une liste déroulante où l'utilisateur peut sélectionner une option à partir d'une liste prédéfinie d'options. La liste d'options est définie à l'aide de ***balises option*** imbriquées à l'intérieur de la balise select.

    Voici un exemple de champ select :

```js
<select id="films" name="films">
    <option value="batman">Batman</option>
    <option value="seigneur-des-anneaux">Le seigneur des anneaux</option>
    <option value="titanic">Titanic</option>
</select>
```

Vous voulez en savoir plus sur les formulaires ? N’hésitez pas à suivre [ce chapitre](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3/8061492-creez-des-formulaires) du cours Créez votre site web avec HTML5 et CSS3.

### Récupérez la valeur d’un champ

Maintenant que nous savons à quoi ressemble un formulaire, il est temps de récupérer, dans notre code JavaScript, le contenu de chacun de ces champs. Pour y parvenir, nous utiliserons différentes méthodes, en fonction du type de champ.
Récupérez les valeurs avec la propriété “value”

La plupart du temps, il est assez simple de récupérer la valeur d’un champ. Il suffit d’utiliser la propriété value.

    Voici un exemple avec un champ appelé name :

```js
<input type="text" id="nom" name="nom">
```

Pour récupérer sa valeur en JavaScript, nous écrirons :

```js
let baliseNom = document.getElementById("nom")
let nom = baliseNom.value
console.log(nom); // affiche ce qui est contenu dans la balise name
```

Cette méthode fonctionne pour la plupart des balises :

    input de type texte, numérique, e-mail, mot de passe ; 

    textarea ;

    select. 

__Récupérez les valeurs des cases à cocher__

Une case à cocher est un cas particulier, car l’utilisateur ne rentre pas une valeur. Il décide de cocher, ou non, la case. La valeur de ce champ est donc nécessairement true si la case est cochée, ou false si elle ne l’est pas.

Pour vérifier cela, vous devez utiliser la propriété checked.

    Voici un exemple :

```html
<input type="checkbox" id="accepter" name="accepter">
```

```js
let baliseAccepter = document.getElementById("accepter")
let accepter = baliseAccepter.checked
console.log(accepter); // affiche true ou false
```

__Récupérez les valeurs des boutons radio__

Les boutons radio partagent le même“name”. De cette manière, lorsqu’un utilisateur clique sur un des boutons pour le sélectionner, les autres sont automatiquement désélectionnés. Ici aussi, il s’agit d’un cas particulier.

    Regardons comment sont déclarés les boutons radio grâce à l’exemple ci-dessous :

```js
<label>Préférence de couleur :</label>
<input type="radio" id="red" name="couleur" value="red" checked>
<label for="red">Rouge</label>
<input type="radio" id="blue" name="couleur" value="blue">
<label for="blue">Bleu</label>
<input type="radio" id="green" name="couleur" value="green">
<label for="green">Vert</label>
```

Dans ce code, il y a plusieurs champs input de type radio. Ces derniers ont des values différentes. Avant de récupérer la bonne value, nous devons donc savoir quel est le champ qui est coché.

Pour cela, nous devons faire une boucle sur l’ensemble des boutons radio jusqu’à trouver celui qui a la propriété checked à true. Nous pourrons alors récupérer la value de ce bouton en particulier.

```js
let baliseCouleur = document.querySelectorAll('input[name="couleur"]')
let couleur = ""
for (let i = 0; i < baliseCouleur.length; i++) {
    if (baliseCouleur[i].checked) {
        couleur = baliseCouleur[i].value
        break
    }
}
console.log(couleur) // affiche la valeur du radio coché
```

Dans le code ci-dessus :

    j’ai d'abord récupéré tous les inputs avec le name qui vaut “couleur”, en utilisant querySelectorAll ;

    j’ai ensuite parcouru l’ensemble des balises jusqu’à trouver une balise qui est cochée ;

    j’ai enfin stocké la couleur dans la variable couleur et j’ai écrit break, pour stopper la boucle et arriver directement au console.log après celle-ci. 

[Récap vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8206488-recuperez-la-valeur-d-un-champ-de-formulaire#/id/r-8206433


)