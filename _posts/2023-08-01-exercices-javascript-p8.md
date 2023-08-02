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