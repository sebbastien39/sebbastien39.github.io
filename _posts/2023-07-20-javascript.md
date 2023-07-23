---
layout: post
title:  "Javascript"
date:   2023-07-09 18:14:13 +0200
categories: javascript débutant
---

![](/assets/images/Fiche+récap+-+Apprenez+à+programmer+en+Javascript.png)

À la fin de ce cours, vous serez capable de :

- manipuler des données avec JavaScript ;
- écrire un fichier JavaScript ;
- faire interagir JavaScript avec votre page web ;
- créer un formulaire de saisie de données.

codepen = bac à sable pour tester du code et voir le résultat en direct.

## Déclarez une variable

Pour commencer à programmer en J, il faut absolument déclarer une variable.
En programmation on manipule plein de données.

une donnée = une information (prénom, date de naissance, citation … quasiment n’importe quoi).

Pour travailler avec ces données, on a besoin de les ranger, on les range dans des variables.

Imaginons la mémoire de l’ordinateur comme une gigantesque armoire. Chaque variable est comme un tiroir de cette armoire.

—

Théorie : 
Ex : Je veux que mon code retrouve “mon prénom”. “mon prénom” c’est une donnée que je vais ranger dans une variable.

Une variable est toujours un ensemble de 3 éléments : une valeur, un nom, un type.

valeur = donnée	içi Seb
nom = ce qui permet de retrouver notre donnée (comme une étiquette sur notre tiroir 🙂)
type = catégorie de donnée (type basique), chaîne de caractères - string, chiffre - number, boolean - true/false.

—

Pratique : 
Déclarer une variable : En J, il faut choisir entre let et const.

let, permet de déclarer une variable dont la valeur peut changer au cours du code.
const (constante), permet de déclarer une variable dont la valeur reste la même tout au long du code.

déclarer une variable : let/const nomVariable = valeur

ex : const monPrenom = Seb		ou	let monAge = 42

—

En informatique, une variable est un conteneur qui stocke la donnée temporairement au sein de votre code. Cela vous permet d’enregistrer des données.

En tant que développeur, vous utilisez des variables pour stocker un nom d’utilisateur ou encore un chiffre représentant le nombre de produits restants dans votre stock. Cela vous permet de retrouver ces données plus facilement.

Les instructions sont des mots-clés uniques qui permettent au code d’être correctement interprété. Pour déclarer des variables, vous utiliserez les instructions let et const.
—
let monAge = 42

Je peux faire évoluer cette valeur en écrivant :
monAge = 43

Notez que je n’ai pas réécrit l’instruction let. En effet, une fois la variable déclarée une première fois grâce à let, je peux l’utiliser directement.

—

Dans ce cours, nous avons fait le choix de ne pas mettre le caractère;pour indiquer la fin d’une ligne de code. Vous serez cependant amené à le retrouver dans certains extraits de code. Les deux écritures sont acceptées.

L’instruction var peut également être utilisée pour déclarer une variable, mais elle est considérée comme obsolète. Pour autant, ne soyez pas surpris d’en trouver parfois dans le code d’autres développeurs, ou dans de vieux projets.

—

L’instruction console.log()
Pour vérifier le contenu d’une variable, il est possible d’utiliser l’instruction console.log(), avec entre les parenthèses, le nom de la variable.

let monAge = 42
console.log(monAge)

—

Je vous encourage vivement à vous servir de console.log tout au long de ce cours. Cela vous permettra de vérifier les valeurs de n’importe quelle variable, et de vous assurer que notre code produit bien les résultats attendus.

—

## Codez proprement

Il n’est jamais trop tôt pour coder proprement, et cela commence dès que vous déclarez une variable ! Ainsi, il est très important de nommer correctement nos variables.

Concrètement : donnez du sens aux noms de vos variables, et décrivez précisément leur contenu.

C’est également utile pour moi, lorsque je reviens sur du code écrit il y a longtemps, pour l’améliorer ou ajouter quelque chose. Avec des variables bien nommées, je suis sûr de retrouver le sens de ce qui a été codé. 😉

## En résumé

Vous pouvez identifier une valeur en lui attribuant un nom grâce à une variable.

Pour déclarer une variable en JavaScript, vous devez utiliser les instructions : 
- let si la valeur de la variable évolue dans le code ;
- const si la valeur de la variable est constante.

Utilisez l’instruction console.log(nomDeMaVariable) pour vérifier le contenu d’une variable.

Le mot-clé var ne doit plus être utilisé. Vous pourrez néanmoins le retrouver dans des codes plus anciens.

Veillez à bien nommer vos variables : indiquez leur contenu de manière explicite pour rendre votre code lisible pour tout le monde.

---

## Modifiez une varaible

