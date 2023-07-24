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

Je veux que mon code retrouve “mon prénom”. “mon prénom” c’est une donnée que je vais ranger dans une variable.

Une variable est toujours un ensemble de 3 éléments : une valeur, un nom, un type.

***valeur*** = donnée	içi David  
***nom*** = ce qui permet de retrouver notre donnée (comme une étiquette sur notre tiroir 🙂)  
***type*** = catégorie de donnée (type basique), chaîne de caractères - string, chiffre - number, boolean - true/false.

—

Pratique :

### Déclarer une variable : En J, il faut choisir entre let et const.

***let***, permet de déclarer une variable dont la valeur peut changer au cours du code.  
***const*** (constante), permet de déclarer une variable dont la valeur reste la même tout au long du code.

déclarer une variable : let/const nomVariable = valeur

ex : `const monPrenom = David`		ou	`let monAge = 42`

—

En informatique, une variable est un conteneur qui stocke la donnée temporairement au sein de votre code. Cela vous permet d’enregistrer des données.

En tant que développeur, vous utilisez des variables pour stocker un nom d’utilisateur ou encore un chiffre représentant le nombre de produits restants dans votre stock. Cela vous permet de retrouver ces données plus facilement.

Les ***instructions*** sont des mots-clés uniques qui permettent au code d’être correctement interprété. Pour déclarer des variables, vous utiliserez les instructions let et const.

—

```javascript
let monAge = 42

// Je peux faire évoluer cette valeur en écrivant :
monAge = 43
```

Notez que je n’ai pas réécrit l’instruction let. En effet, une fois la variable déclarée une première fois grâce à let, je peux l’utiliser directement.

—

Dans ce cours, nous avons fait le choix de ne pas mettre le caractère `;` pour indiquer la fin d’une ligne de code. Vous serez cependant amené à le retrouver dans certains extraits de code. Les deux écritures sont acceptées.

L’instruction `var` peut également être utilisée pour déclarer une variable, mais elle est considérée comme ***obsolète***. Pour autant, ne soyez pas surpris d’en trouver parfois dans le code d’autres développeurs, ou dans de vieux projets.

—

L’instruction `console.log()`
Pour vérifier le contenu d’une variable, il est possible d’utiliser l’instruction console.log(), avec entre les parenthèses, le nom de la variable.

```javascript
let monAge = 42
console.log(monAge)
```

—

Je vous encourage vivement à vous servir de `console.log` tout au long de ce cours. Cela vous permettra de vérifier les valeurs de n’importe quelle variable, et de vous assurer que notre code produit bien les résultats attendus.

—

## Codez proprement

Il n’est jamais trop tôt pour coder proprement, et cela commence dès que vous déclarez une variable ! Ainsi, il est très important de nommer correctement nos variables.

Concrètement : donnez du sens aux noms de vos variables, et décrivez précisément leur contenu.

C’est également utile pour moi, lorsque je reviens sur du code écrit il y a longtemps, pour l’améliorer ou ajouter quelque chose. Avec des variables bien nommées, je suis sûr de retrouver le sens de ce qui a été codé. 😉

## En résumé

Vous pouvez identifier une valeur en lui attribuant un nom grâce à une variable.

Pour déclarer une variable en JavaScript, vous devez utiliser les instructions : 
- ***let*** si la valeur de la variable évolue dans le code ;
- ***const*** si la valeur de la variable est constante.

Utilisez l’instruction `console.log(nomDeMaVariable)` pour vérifier le contenu d’une variable.

Le mot-clé var ne doit plus être utilisé. Vous pourrez néanmoins le retrouver dans des codes plus anciens.

Veillez à bien nommer vos variables : indiquez leur contenu de manière explicite pour rendre votre code lisible pour tout le monde.

---

## Modifiez une variable

Une fois les variables déclarées, on peut les modifier.

Il y a 3 types de variables, de données basiques : 

- number (3, 42 ...)
- string ("hello, world!")  Récuperer un nom d'util
- Boolean (true / false)    Sit un utilisateur est conecté

On va toucher n'y au type, n'y au nom, mais juste changer la valeur de la variable, en utilisant des opérations simples (un peu comme en math). Selon le type de donnée que l'on modifie, on ne peut pas réalisé les mêmes opérations.

## Number

Pour les valeurs de type "number", on peut utiliser les opérations mathématiques simples :

 addition | soustraction | division | multiplication 
 ---------|--------------|----------|----------------
 + | - | / | *

Ex : variable compte le nombre d'utilisateurs de mon site.


```javascript
// Modifier une variable number
let nombreUtilisateurs = 200
nombreUtilisateurs = nombreUtilisateurs + 100
nombre Utilisateurs = 300
```

```javascript
// Modifier une variable number avec des opérateurs d'affectation
let nombreUtilisateurs = 200
nombreUtilisateurs += 100
nombreUtilisateurs = 300
```

```javascript
// idem pour les autres opérateurs
let nombreUtilisateurs = 200
nombreUtilisateurs -= 100
nombreUtilisateurs = 100
```

***Opérateur d'affectation*** : raccourcis qui permettent d'associer la variable à une opération sans avoir à écrire son nom 2 fois.

|+= |-= |/= | *= |

## modifier une valeur de type "string"

Pour modifier valeur string on lui ajoute des mots > concaténation.

***concaténation*** : joindre bout à bout 2 chaînes de caractères. On utilise cette opération quand la chaîne de caractères que l’on souhaite stocker dans une variable est dans deux variables différentes.

Pour réaliser une cancaténation, on utilise l'opérateur `+` ou `+=`

```javascript
// Modifier une variable string
let messageBienvenue = "Bienvenue,"
let nomUtilisateur = "David42"
let messageBienvenuePerso = messageBienvenue + nomUtilisateur
// messageBienvenuePerso vaut "Bienvenue, David42".
```

```javascript
// Modifier une variable string avec des opérateurs d'affectations
let messageBienvenuePerso = "Bienvenue,"
messageBienvenuePerso += "David42".
// messageBienvenuePerso vaut "Bienvenue, David42".
```

L'opérateur `+` n'a pas la même action dans le cas d'une valeur "number" ou "string".

- il additionne les number.
- il concatène les chaînes de caractères.

## Boolean

Pour manipuler boléen, il n'y a pas l'embarras du choix car il ne prennent que 2 valeurs (true / false), oui/non, vrai/faux, allumé/éteint.

```javascript
let monBoolean = true
let monBoolean = false
```

## +

### Convertire du texte en chiffre

```javascript
let maVariable = "25"   //interprété comme du texte à cause des ""
console.log(maVariable + 5)
// Résultat 255
```

Pour y remédier, utiliser l 'instruction `Number`, pour convertir la variable en chiffres.

```javascript
let maVariable = "25"
console.log(Number(maVariable) + 5)
```

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204726-modifiez-une-variable). [Opérateurs d'affectation](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Expressions_and_Operators#op%C3%A9rateurs_daffectation).


---

## Structurez des données grâce aux objets

![](/assets/images/2023-07-24 14-34-25.png)

Si un élément a plusieurs valeurs à la fois, on va utiliser les objets javascript.

***Objet*** : sorte de conteneur qui contient ***plusieurs valeurs*** attribuées ***à un même élément***.

Pour déclarer un objet, on utilise des accolades.

`Instruction + nomDeLaVariable = { propriétés : valeur }`

Grâce aux objets, il est possible de déclarer des propriétés à l'infini.

```javascript
let monPersonnage = {
    nom: "Wayne",
    prenom: "Bruce",
    age: 35,
    couleurPreferee: "noir",
    hobbies: "sortir la nuit"
}
```

Plus tard si l'on souhaite ajouter une propriété à l'objet, c'est possible : 

`nomDeMonObjet.nomDeLaPropriété = valeurDeLaProPriété`

```javascript
monPersonnage.vehiculePrefere = "Batmobile"
```

Pour accéder à la valeur d'une propriété qui est dans l'objet, pour l'afficher dans la console par exemple : 

`console.log(nomDeLobjet.nomDeLaPropriété)
// Affiche la valeur de la propriété`

```javascript
console.log(monPersonnage.couleurPreferee) // Affiche "noir"
```

## Def

Un ***Object*** (objet, en français) JavaScript est un conteneur. Il est composé de propriétés qui ont chacune une valeur. Ainsi, le type de donnée Object offre la possibilité de stocker plusieurs valeurs en une seule fois, plutôt que de devoir stocker séparément nos valeurs dans plusieurs variables différentes.

## +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204834-structurez-des-donnees-grace-aux-objets). 