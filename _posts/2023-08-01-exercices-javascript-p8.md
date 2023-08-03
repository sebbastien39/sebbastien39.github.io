---
layout: post
title:  "Exercices Javascript P8"
date:   2023-08-01 19:00:04 +0200
categories: exercice javascript
---

## Ex 1

```javascript
let totalLivres = 500
totalLivres += 50
totalLivres -= 10
totalLivres += 5

console.log(totalLivres)

let affichageTotalLivres = "Notre bibliothèque possède " + totalLivres + " livres"
console.log(affichageTotalLivres)
```

## Ex 2

Déclarer un objet "ticket"

```javascript
let nom = "seb"
let ticket = {
    nomFilm: "Titanic",
    Prix: 10,
    numeroSalle: 2
}

texteAffichage = "Bonjour " + nom + " , votre film " + ticket.nomFilm + " est en salle " + ticket.numeroSalle
  
console.log(texteAffichage)
```

[corrigé](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204834-structurez-des-donnees-grace-aux-objets#/id/r-8204823)

## Ex 3

```javascript
const playlist = ["m1", "m2", "m3"]

// Ajouter donnée dans tableau
playlist.push("m4", "m5")

// Supprimer la dernière donnée du tableau
playlist.pop()

// Nombre total de musiques
let totalMorceaux = playlist.length

console.log(playlist)
console.log(totalMorceaux)
```

[corrigé](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204994-regroupez-des-donnees-grace-aux-tableaux#/id/video_Player_4)

## Ex 4

Condition

```js
const listeMots = ["Cachalot", "Pétunia", "Serviette"]
let score = 0

let motUlitisateur = prompt ("Écrivez le mot : " + listeMots[0])
if (motUlitisateur === listeMots[0]) {
  score++
}

// Plus besoin de let ensuite
motUlitisateur = prompt ("Écrivez le mot : " + listeMots[1])
if (motUlitisateur === listeMots[1]) {
  score++
}

motUlitisateur = prompt ("Écrivez le mot : " + listeMots[2])
if (motUlitisateur === listeMots[2]) {
  score++
}

console.log("Votre score est de " + score + " sur 3")

```

[corrigé](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205369-controlez-du-code-grace-aux-conditions#/id/r-8205354)

## Ex 5

Boucles

Factoriser le code précédent en mettant en commun les parties répétées à l'aide d'une boucle.

```js
const listMots = ["Cachalot","Pétunia","Serviette"]
let score = 0

for (let i = 0; i < listMots.length; i++) {
    let motUtilisateur = prompt("Entrez un mot : " + listMots[i])
    if (motUtilisateur === listMots[i]) {
        score++
    }
}

console.log("Votre score est de : " + score + " sur " + listMots.length)
```

Évolution code précédent, Proposez 2 types de listes de mots.

```js
const listMots = ["Cachalot","Pétunia","Serviette"]
const listePhrases = ["Pas de panique !", "La vie, l’univers et le reste", "Merci pour le poisson"]
let score = 0
let choix = prompt("Tapez mots ou phrases")


if (choix === "mots"){
for (let i = 0; i < listMots.length; i++) {
    let motUtilisateur = prompt("Entrez un mot : " + listMots[i])
    if (motUtilisateur === listMots[i]) {
        score++
    }
}
} else {
for (let i = 0; i < listePhrases.length; i++) {
    let motUtilisateur = prompt("Entrez un mot : " + listePhrases[i])
    if (motUtilisateur === listePhrases[i]) {
        score++
    }
}
}
console.log("Votre score est de : " + score + " sur " + listMots.length)
```

[corrigé](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205519-repetez-du-code-grace-aux-boucles#/id/video_Player_4)

## Ex 6

Découpez votre code en fonctions.

```js

```

## Modifier élément

```html
<img id="yz" src="https://www.dupmx.com/13136-tm_thickbox_default/yamaha-yz-125-2022.jpg" alt="moto yz bleue">
```
```js
// Récupère l'élément
let moto = document.getElementById("yz")

// 2 arguments : l'élément que l'on veut changer. Attribut 2 = nouvelle valeur
moto.setAttribute("src", "https://www.velos17loisirs.com/wp-content/uploads/2021/01/Velo-tout-terrain_%C2%A9VELOS17LOISIRS_2022_7.jpg")

// on peut l'écrire aussi comme ça
moto.src = "https://www.littlemichelenoelle.com/52937-large_default/trotinette-deluxe-pliable-bleu-ocean.jpg"


// Attribut class possède une liste d'éléments
moto.classList.remove("nomClassASupprimee")

// Ajouter une class
moto.classList.add("NouvelleClass")
moto.classList.add("NouvelleClass2")
```

## Créer un élément HTML à partir de rien

2 façons de faire : 

Ajouter du code HTML dans une page - içi un titre h1 dans body.

```html
<body>

</body>
```

__Méthode n° 1 avec : document.creatElement__

```js
let titrePage = "Le titre de ma page"
// 1. Création de la balise h1
let h1 = document.createElement("h1")

// Ajouter contenu dans la balise avec : innerText
h1.innerText = titrePage    // On reprends valeur de la variable créée au début

// Insérer balise h1 dans le HTML, en récupérant la balise (içi body)
let body = document.querySelector("body")

// Ajouter balise h1 en tant que enfant de body
body.appendChild(h1)
``` 

__Méthode n°2 insérer code dans balise existante__

```js
let titrePage = "Le titre de ma page"
let body = document.querySelector("body")

// Générer le code
//Interpolation, insérer contenu d'une variable avec ${}
// Ne pas oublier ``
let html = `
    <header>
        <h1>${titrePage}</h1>
    </header>
`
//Insérer le code HTML dans la balise body
body.innerHTML = html
```