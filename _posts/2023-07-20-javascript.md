---
layout: post
title:  "Apprenez à programmer avec JavaScript"
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

    Découverte du language Javascripte et de sa syntaxe.

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

## +

Contrairement aux variables déclarées avec let qui peuvent changer de valeur au cours du code, les variables déclarées avec const ne changent pas de valeur. Rappelez-vous que const est un raccourci pour le mot constante.

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204629-declarez-une-variable).  

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

Plus tard si l'on souhaite ***ajouter une propriété à l'objet***, c'est possible : 

`nomDeMonObjet.nomDeLaPropriété = valeurDeLaProPriété`

```javascript
monPersonnage.vehiculePrefere = "Batmobile"
```

Pour ***accéder à la valeur d'une propriété qui est dans l'objet***, pour l'afficher dans la console par exemple : 

`console.log(nomDeLobjet.nomDeLaPropriété) // Affiche la valeur de la propriété`

```javascript
console.log(monPersonnage.couleurPreferee) // Affiche "noir"
```

-

Lorsque vous manipulez des objets JavaScript, vous avez également besoin d’accéder à leurs propriétés pour les stocker dans des variables, et les utiliser dans la suite de votre code ou dans un autre contexte.

Pour accéder à la propriété d’un objet, vous devez utiliser le point `.` suivi du nom de la propriété. Il ne vous reste plus qu’à stocker sa valeur dans une variable.

Dans le cadre de l’***objet monPersonnage***, vous écrirez :

```javascript
const nomDeMonPersonnage = monPersonnage.nom

// Vérification
console.log(nomDeMonPersonnage)
console.log(monPersonnage.nom)
```

## Def

Un ***Object*** (objet, en français) JavaScript est un conteneur. Il est composé de propriétés qui ont chacune une valeur. Ainsi, le type de donnée Object offre la possibilité de stocker plusieurs valeurs en une seule fois, plutôt que de devoir stocker séparément nos valeurs dans plusieurs variables différentes.

## Résumé

Un ***objet*** en JavaScript peut posséder plusieurs propriétés qui auront pour chacune d’elles une valeur.

Pour déclarer un objet en JavaScript, vous devez utiliser les accolades  `{ }`

Pour ajouter ou récupérer une propriété, vous devez utiliser le point `.`

## Exercice

```javascript
const ticket = {
  nomFilm: "Batman",
  prix: 20,
  numeroSalle: 2    //pas de virgule à la dernière propriété
}

let nom = "Seb"     // j'ai mis let puis const et en fait c'est let

// Méthode 1
let texteAffichage = "Bonjour "
texteAffichage += nom
texteAffichage += ", Votre film "
texteAffichage += ticket.nomFilm
texteAffichage += ", est en salle "
texteAffichage += ticket.numeroSalle

// Méthode 2
let texteAffichage = "Bonjour " + nom + ", Votre film " + ticket.nomFilm + ", est en salle " + ticket.numeroSalle

console.log(ticket) //Pour tester valeur
console.log(nom)    //Pour tester valeur
console.log(texteAffichage) //Afficher la concaténation

```

## +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204834-structurez-des-donnees-grace-aux-objets).

---

## Regroupez des données grâce aux tableaux

Regrouper des variables en utilisant des tableaux.

***Tableau*** : conteneur qui permet de regrouper plusieurs variables ou plusieurs valeurs. Sorte de super variable qui en regroupe plusieurs.

On déclare un tableau avec des crochets `[]` Chaque valeur est séparée par une `,`

`instruction nomTableau = ["valeur1","valeur2","valeur3"]`

`const mesFilms = ["Titanic","Jurassic Park","Le seigneur des Anneaux"]`

Il est possible de stocker des variables dans un tableau : 

```javascript
const monFilmPrefere = "Titanic"
const monPremierFilm = "Le Seigneur des Anneaux"

const maCollectionDeFilms = [monFilmPrefere, monPremierFilm]

// maCollectionDeFilms vaut ["Titanic", "Le Seigneur des Anneaux"]
```

### Accéder à un élément d'un tableau

Mettre entre crochet le numéro de la case à regarder. Le tableau commence à zéro `0`

```javascript
let premierFilmDuTableau = maCollectionDeFilms[0]
```

### Compter le nombre d'éléments d'un tableau

Connaitre le nombre de données contenu dans un tableau avec la ***propriété `length`***, en utilisant le point `.` , comme pour les objets. Cette propriété est préétablie par JavaScript. Elle est donc automatiquement disponible pour tous les tableaux.

`console.log(mesFilms.length) // Il y a 3 éléments dans le tableau`

Les ***méthodes*** : permettent de modifier facilemment les données contenu dans un tableau, on les utilise avec des parenthèse, en mettant les valeurs à ajouter ou a supprimer du tableau entre 2 parenthèses `()`.

### Ajouter un élément

méthode ***push*** : permet d'ajouter un élément, toujours à la dernière place de la liste des valeurs dans le tableau : 

```javascript
mesFilms.push("Retour vers le futur")
// Retour vers le futur sera ajouter au tableau
```

### Supprimer un élément

méthode ***pop*** : permet de supprimer la dernière valeur de la liste. Pas besoin d'écrir une valeur entre parenthèses.

```javascript
let mesFilms = ["Titanic","Jurassic Park","Retour vers le futur"]
mesFilms.pop()
// mesFilms vaut ["Titanic","Jurassic Park"]
```

### Distinguez les copies par “valeur” et par “référence”

Lorsqu’on programme, il arrive parfois que l’on veuille dupliquer une variable. C’est le cas lorsque l’on doit sauvegarder une valeur avant de la modifier, par exemple. Pour cela, le plus simple est de copier le contenu d’une variable à l’intérieur d’une autre variable.

***Copie par valeur***

```javascript
// Copie par valeur
let variableSimple1 = 25
let variableSimple2 = variableSimple1
```
Si variable2 est un type simple (boolean, number ou string), alors le contenu sera dupliqué.

Au final, nous aurons deux tiroirs indépendants avec chacun une valeur à l’intérieur.

***Copie par référence***

Imaginez maintenant que vous vouliez copier une variable qui contient un contenu de type “complexe” :  un objet ou un tableau, par exemple. Dans ce cas, JavaScript fait une copie par référence.

```javascript
let variableComplexe1 = ['pomme', 'cerise']
let variableComplexe2 = variableComplexe1
```

Ici, nous n’avons pas deux tiroirs, c’est l’étiquette qui a été copiée. En d’autre termes, variable1 et variable2 sont deux étiquettes différentes pour le même tiroir. Nous avons donc deux variables qui pointent sur le même contenu.

***Différence copie par valeur, copie par référence*** : 

Dans le cas d’une copie par ***valeur***, si vous modifiez la valeur d’une des deux variables, la valeur de l’autre ne change pas.

Dans le cas d’une copie par ***référence***, si vous changez la valeur de la première variable, la valeur de la seconde est affectée aussi.

### Dupliquer (cloner) un tableau

1. Déclarer un nouveau tableau.
2. Copier les données dans le nouveau tableau avec le "spread operator" `...`

```javascript
let variableComplexe3 = [...variableComplexe1];
// Copie tous les éléments de variableComplexe1 dans variableComplexe3
// Les 2 tableaux sont indépendants
```

 Les tableaux sont souvent déclarés avec ***const*** en JavaScript, même s'ils évoluent tout au long du code. Ce qui est constant, ce n’est pas le contenu, mais l’endroit en mémoire où est stocké le tableau. 

### Supprimer donnée précise

`splice` pour supprimer une donnée précise.

### Trier les données

`sort` pour trier les données.

## Déf

Un ***tableau*** en JavaScript est donc un objet qui permet de lister plusieurs variables ou valeurs, et de les regrouper.

Les ***tableaux*** sont des conteneurs, comme les objets que nous avons vus dans le chapitre précédent. Pour effectuer des actions sur les données stockées dans votre tableau (ajouter, supprimer des données…), vous utiliserez des méthodes.

Les ***méthodes*** s’utilisent avec des parenthèses  ( )  . À l’intérieur de ces parenthèses vous pouvez passer des valeurs, c'est-à-dire des données, qui serviront à la méthode pour modifier les données de votre tableau. En réalité, vous avez déjà utilisé une méthode fournie par JavaScript : console.log() ! 

La ***copie par valeur***. Nous avons copié le contenu d’une variable à l’intérieur d’une autre variable. Nous avons donc deux variables indépendantes.

La ***copie par référence***. Les variables font référence au même espace mémoire.

## Résumé

Un ***tableau*** est un conteneur qui permet de regrouper plusieurs valeurs ou variables.

Un ***tableau*** possède une (seule) propriété ***length*** qui permet de connaître le nombre de données contenues dans un tableau.

Une méthode s’utilise avec des parenthèses `( )` , et permet d’interagir avec le contenu du tableau. Il existe de nombreuses méthodes différentes mises à disposition par le langage.

Lorsqu’on copie une ***variable simple***, JavaScript réalise une copie par valeur (la valeur est dupliquée).

Lorsqu’on copie une ***variable complexe***, JavaScript réalise une copie par référence (les deux variables pointent sur la même valeur).

## +

Déclarer tableau `[]`  
Déclarer objet `{}`  
Pour utiliser des méthodes `()`

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204994-regroupez-des-donnees-grace-aux-tableaux). [Doc Moz Tableau](https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Arrays).

---

***

## Appréhendez la logique de programmation

    Comprendre la logique de programmation de Javascript

Rédiger un programme informatique, qui répond à une logique de programmation. Le navigateur web, est capable de comprendre et d’interpréter ce programme.

### La notion d'algorithme

En tant que développeur, vous rédigez du code dans le but de développer un programme informatique. Vous allez donc écrire, en JavaScript, un ***ensemble d’instructions et d’opérations*** qui seront exécutées par un ordinateur dans un but précis.

### Organisez votre code grâce aux blocs de code

Les blocs de code sont des regroupements de lignes de code. Ils permettent d’organiser votre code et de clarifier à quoi sert un groupe de lignes de code. En JavaScript, ils sont délimités par des accolades  `{ }`

Exemple de bloc de code :

```javascrip
{
    const monChiffre = 4
    console.log(monChiffre)
}
```
Ici, j’ai utilisé un bloc de code pour déclarer la variable monChiffre.

### Installez votre environnement de travail

Utilisez un éditeur de code (IDE) tel que Visual Studio Code.

Avoir un dossier de travail pour le projet. DS VSCode : File > openFolder > FichierDuProjet

Pour exécuter du code Javascript, il faut au minimum 2 fichiers :
- un fichier .html : notre page web.
- un fichier .js : qui contiendra le code Javascript.

***index.html*** : 

```javascript
<!DOCTYPE HTML>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="script.js"></script>
</head>
<body>

</body>
</html>
```

La ligne `<script src="script.js"></script>` va lier fichier HTML au fichier JS, le fichier HTML va charger le ***script JS***. C'est grâce à cette ligne que le navigateur saura qu’il doit exécuter les instructions contenues dans script.js.

***script.js***

```javascript
// Pour tester que tout fonctionne avec “Hello World”
console.log("Hello World");
```

#### Affichez la console de votre navigateur

- Ouvrir index.HTML dans navigateur (Ds VSCode : Clic D, Reveal in File Explorer).
- Afficher les Dev tool > Console

Dans la console, vous verrez notre “Hello World”, qui correspond à l’instruction écrite dans le fichier script.js.

### Déf

Un ***algorithme*** est une façon de concevoir les étapes d’un code dans le but de résoudre un problème donné.

****IDE*** (Integrated Development Environment, ou environnement de développement intégré). Un IDE permet de regrouper tout ce dont nous aurons besoin pour écrire notre code. Tous les fichiers seront au même endroit, et le code sera coloré pour faciliter la lecture.

### Résumé

Un fichier JavaScript répond à une logique de programmation qui a pour but de résoudre un problème donné.

Pour construire cette logique de programmation, vous devrez :

- concevoir un algorithme qui définit les étapes permettant de résoudre un problème donné ;

- transposer cet algorithme en code organisé avec des structures conditionnelles et/ou des fonctions intégrant des blocs de code. 

Pour coder, vous devez utiliser un éditeur de code comme Visual Studio Code pour créer ou importer vos fichiers JavaScript et HTML.

Pour tester votre code, affichez la console de votre navigateur grâce aux Outils de développement.

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205116-apprehendez-la-logique-de-programmation)

---

## Contrôlez du code grâce aux conditions

Pour écrire un code fonctionnel et permettre à notre ordinateur de réalisé certaine opérations à notre place, il va falloir utiliser des conditions.

Exemple de condition "humaine" : À la boulangerie, si il y a du pain au noix, j'en prends un, sinon je prends une baguette.

Pour un ordinateur (Il faut lui parler dans sa langue).

En programmation, une condition, c'est un test, dont le résultat peut être soit vrai soit faut et en fonction du résultat de ce test, notre programme va effectuer une opération ou bien une autre. Il va agir de manière conditionnelle.

![](/assets/images/2023-07-26 18-22-18.png)

Cette fois, c'est un robot programmé qui va à la boulangerie : 

![](/assets/images/2023-07-26 18-25-27.png)

![](/assets/images/2023-07-26 18-28-56.png)

Donc une condition c'est :

![](/assets/images/2023-07-26 18-32-18.png)

Si vous avez compris ça, vous avez le pouvoir !

Exercice AzerType :

L’utilisateur va devoir recopier un mot qui lui est proposé. Si le mot est correct, son score augmentera, sinon… Eh bien, il ne se passera rien.

Algorithme de l'application : 

    si “mot tapé par l’utilisateur” == “mot proposé”  
    alors “on augmente le score”

/!\ Notez l’absence de “sinon”. On ne le précise que si l’on veut réaliser un
traitement dans le cas où la condition n’est pas valide, ce qui n’est pas le cas ici.

### Rédigez une condition en JavaScript

Pour  rédiger une condition, vous devez :

- utiliser des structures conditionnelles ;
- rédiger un test ;
- rédiger un bloc de code.

Il existe deux principaux types de conditions en JavaScript :

- les ***conditions if / else*** permettent d’exécuter du code selon une réponse unique à un test ;
- les ***conditions switch*** permettent d’exécuter du code si notre test peut avoir plusieurs réponses.

### Utilisez des conditions if / else pour gérer une seule réponse

syntaxe d’une condition en JavaScript :

```javascript
if (condition) {
    // Code exécuté si la condition est vraie
} else {
    // Code exécuté si la condition est fausse
}
```

Ce morceau de code signifie : Si (if, en angais) la condition est vraie, alors j’exécute le premier bloc de code, sinon (else, en anglais) j’exécute le second.

La condition utilisée peut être un booléen (valant true ou false), ou une comparaison (exemple : variable === 42).

#### Rédigez un test avec des booléens

Ex : Dans notre cas, nous cherchons à comparer le mot tapé par l’utilisateur à celui choisi par l’application.

Je crée ainsi une variable motTapeOk qui contiendra true ou false, et j’écris mon test en fonction :

```javascript
let motTapeOk = true // Essayez de mettre false à la place de true

if (motTapeOk) {
    console.log("Bravo, vous avez correctement tapé le mot")
} else {
    console.log("Échec, le mot n'est pas correct")
}
```

Ici, motTapeOk est une variable de type booléen. Comme la variable vaut true (vrai), alors JavaScript a exécuté le premier bloc de code, car la condition est validée. Le mot tapé est correct, j’affiche donc le message correspondant.

En fait, le else est optionnel. Vous pouvez donc simplement écrire :

```javascript
let motTapeOk = true // Essayez de mettre false à la place de true

if (motTapeOk) {
    console.log("Bravo, vous avez correctement tapé le mot")
}
```

Si l’utilisateur a correctement tapé le mot, le premier bloc sera exécuté, sinon… eh bien pas de sinon. Le code s’arrête là.

#### Rédigez un test avec des opérateurs de comparaison

```javascript
let motUtilisateur = prompt("Entrez un mot :")
console.log(motUtilisateur)
```

Dans ce morceau de code :

- nous déclarons une variable motUtilisateur ;

- à l’intérieur nous mettons le résultat de l’instruction prompt(“Entrez un mot :”). Cette instruction fera apparaître une petite popup sur la page ;

- l’utilisateur n’a plus qu’à répondre à la question, et ce mot se retrouve à l’intérieur de la variable motUtilisateur. 


#### Les opérateurs de comparaison :

|<  | inférieur à|
|<= | inférieur ou égal à|
|=== | égal à	|
| >= | supérieur ou égal à|
| > | supérieur à|
| !== | différent de|

Il existe également les opérateurs  ==  et  !=  pour comparer des valeurs entre elles. Cependant, il n’est pas recommandé de les utiliser, car ils ne permettent pas de tester en une seule opération la valeur et le type de données de la valeur. Vous pourrez néanmoins être amené à en trouver dans le code d’autres développeurs.

Ex : `===` va nous permettre de comparer si deux éléments ont exactement la même valeur.

```javascript
const motApplication = "Bonjour" // Essayez de mettre un autre mot ici !
let motUtilisateur = prompt("Entrez le mot : " + motApplication)

if (motUtilisateur === motApplication) {
    console.log("Bravo !")
} else {
    console.log("Vous avez fait une erreur de frappe.")
}
```

#### Utilisez la condition switch/case pour gérer plusieurs réponses

- définir le test avec switch(laValeurATester) ;
- lister les valeurs possibles avec case.

```javascript
switch (motUtilisateur) {
    case motApplication:
        console.log("Bravo !")
        break
    case "Gredin":
        console.log("Restez correct !")
        break
    case "Mécréant":
        console.log("Restez correct !")
        break
    case "Vilain":
        console.log("Soyez gentil !")
        break
    default:
        console.log("Vous avez fait une erreur de frappe.")
}
```
Ici, je teste motUtilisateur : 

- si l’utilisateur a tapé “Gredin”, alors c’est le premier console.log qui va s’exécuter ;
- s’il a tapé “Mécréant”, c’est le second console.log qui s’exécute. ;
- s’il a tapé “Vilain”, c’est le troisième ;
- s’il a rentré autre chose (default), alors c’est le dernier console.log qui s’exécute.

Le ***break*** sert à arrêter le code.

### Exercice

Faire évoluer le score, quand le mot est exacte.

```javascript
const listMots = ["Cachalot","Pétunia","Serviette"]
let score = 0

let motUtilisateur = prompt("Entrez un mot : " + listMots[0])
if (motUtilisateur === listMots[0]) {
 score++
}

motUtilisateur = prompt("Entrez un mot : " + listMots[1])
if (motUtilisateur === listMots[1]) {
 score++
}

motUtilisateur = prompt("Entrez un mot : " + listMots[2])
if (motUtilisateur === listMots[2]) {
 score++
}

console.log(score)
```

### Déf

Une ***condition*** est une ***structure conditionnelle*** qui contient un ***test*** dont le résultat sera vrai ou faux. Elle permet d'exécuter des instructions en fonction du résultat de ce test. On parle donc de structure conditionnelle, car un code ne s’exécutera qu’***à condition*** que le test soit vrai ou faux.

### Résumé

Une condition est un type de structure conditionnelle qui contient un test dont le résultat sera vrai ou faux.

Les conditions if / else permettent d’exécuter du code selon une réponse unique à un test.

Les conditions switch permettent d’exécuter du code si notre test peut avoir plusieurs réponses.

Vous pouvez utiliser des booléens pour les tests de vos conditions, ou des opérateurs de comparaison, en fonction de ce que vous souhaitez tester.

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205369-controlez-du-code-grace-aux-conditions).

---

## Répétez du code grâce aux boucles

Je veux qu mon téléphone affiche la liste de mes contacts. CaD, la photo de mon ami n°1, n°2, n°3, etc. Le problème, j'ai 500 contacts et je ne vais pas écrire l'instruction 500 fois. Pas de problème, je vais utiliser une boucle.

Le principe des boucles, c'est de pouvoir répéter une instruction plein de fois, sans avoir à la réécrire à chaque fois.

2 types de boucles :

- La boucle ***For***, correspond à une instruction que l'on va demander de répéter un certain nombre de fois (500 par exemple). Dans ce cas là, notre variable va prendre la valeur de 0 à 499 et on va s'en servir pour exécuter l'instruction "affiche la photo de mon ami n° X". X va de 0 à 499. En gros, la boucle va compter jusqu'à 500 et s'arrêtera de tourner seulement lorsqu'elle aura exécuter l'instruction 500 fois.

> For (ce qui défini le ***fonctionnement de la boucle***) {Bloc de code à exécuter à chaque tour}

On va créer un compteur pour notre boucle et gérer son fonctionnement, avec 3 éléments.

> For (initialisation du compteur ; condition d'arrêt ; exécuter à chaque tour de boucle et mets à jour le compteur)

![](/assets/images/2023-07-28 07-53-58.png)

> Attention ! <mark>compteur vaut 0, puis 1, puis 2, puis 3, etc</mark>

![](/assets/images/2023-07-28 07-55-12.png)

Il faut connaitre combien de tour de boucle on a besoin de faire.

- La boucle ***While*** 

J'ai besoin de chercher dans mes contacts le n° d'une amie qui s'appelle Alice. Je ne sais pas si dans mon répertoire c'est au n°3 ou au n°250. Je vais utliser un deuxième type de boucle, la boucle ***While***.

> let compteur =  
> let i=  
i pour index (convention de nommage)

```javascript
let i=0
// Je vais continuer à boucler tant que le contact que je regarde n'est pas Alice.
while (condition d'arrêt)

{
    // Mise à jour du compteur i
    i=i+1   // équivalent à i++
    }
```

La boucle va tourner jusqu'à ce qu'elle trouve le contact "Alice".

![](/assets/images/2023-07-28 09-04-39.png)

Au moment où l'on sort de la boucle, on sait que "Alice" est le contact n°i, on va pouvoir afficher son numéro de téléphone avec `console.log(listContact[i].telephone)`


---

### Découvrez les boucles

En tant que développeur, vous aurez parfois besoin de faire plusieurs fois la même action sur une variable ou sur une partie de votre code. Dans cette situation, vous devrez utiliser des boucles.

Une ***boucle*** est une structure conditionnelle qui permet de répéter un certain nombre de fois du code, jusqu’à ce qu’un test ne soit plus vrai.

Rappelez-vous, dans l’exercice du chapitre précédent, nous avons déclaré un tableau qui contient trois mots : Cachalot, Pétunia et Serviette.

Pour afficher chacun de ces mots, on peut donc écrire :

```javascript
const listeMots = ['Cachalot', 'Pétunia', 'Serviette']
console.log(listeMots[0])
console.log(listeMots[1])
console.log(listeMots[2])
```

Mais imaginez maintenant que le tableau contienne tout un dictionnaire… Ça va faire beaucoup de console.log ! 😱 D’autant qu’à chaque ligne, une seule chose change : l’indice du tableau (0, 1, 2…). Je vous propose donc de rédiger une boucle qui va nous permettre de répéter du code, et de résoudre ce problème.

### Rédigez une boucle

Il  existe deux principaux types de boucles :

- La boucle for permet de répéter du code lorsque l’on sait d’avance combien de fois il faudra le répéter.

Par exemple, si nous voulons demander exactement trois fois à l’utilisateur d’entrer un mot.

- La boucle while permet de répéter du code autant de fois qu’il le faut pour qu’une condition ne soit plus vraie.

Par exemple, si nous voulons redemander un mot à l’utilisateur jusqu’à ce que ce mot soit correct.

Comme toujours, je vous propose de découper notre problème en petites étapes. 😉

Commençons par écrire une boucle qui affiche 0, puis 1, puis 2. Dans ce cas, ****nous savons à l’avance combien de tours de boucle*** nous voulons faire, un for est donc tout à fait indiqué ici.

Pour rédiger notre boucle ***for***, nous allons utiliser l’instruction ***for*** (“pour”, en anglais). Cette instruction sera suivie d’une condition entre parenthèses dans laquelle on indiquera : 

- le départ de la boucle ;
- au bout de combien de tours la boucle devra s’arrêter.

Voici comment la rédiger :

```javascript
for (let compteur = 0; compteur < 3; compteur = compteur + 1) {
    console.log(compteur)
}
```

Ouh là là… Je ne suis pas sûr d’avoir tout suivi…

Aucun souci, voyons en détail ce qui est écrit.

- Nous avons d’abord notre for, suivi de trois instructions séparées par un point virgule `;`
- Ensuite, un bloc de code entre accolades : le `console.log` 

Ce bloc de code sera exécuté à chaque tour de boucle. 

Première instruction :

```javascript
let compteur = 0
```

Ici nous définissons une nouvelle variable appelée “compteur”, et qui contient 0.

Deuxième instruction :

```javascript
compteur < 3
```

Ceci est la condition d’arrêt. La boucle continuera tant que compteur est plus petit que 3.

Troisième instruction :

```javascript
compteur = compteur + 1`
```

À chaque tour de boucle, on fait évoluer la valeur de compteur. Ici, on dit que compteur vaut la valeur précédente de compteur, plus 1.

Au premier tour de boucle, compteur vaut 0, puis 1, puis 2, jusqu’à ce que compteur arrive à 3 (la condition d'arrêt) et là, on sort de la boucle. 

Le bloc de code entre accolades aura donc été exécuté 3 fois avec compteur ayant la valeur 0, puis 1, puis 2.

> Il est très courant en programmation d’utiliser une boucle for. Pour la taper plus vite, il existe donc une écriture un peu raccourcie. Par convention, on nomme souvent la variable compteur “i” (comme “indice”). Et au lieu d’écrire i = i+1, on utilise l’opérateur d’incrémentation  ++  , qui augmente la valeur d’une variable de 1.

Cela donne :

```javascript
for (let i = 0; i < 3; i++) {
    console.log(i)
}
```

Le résultat est exactement le même.

Grâce à la boucle ***for***, nous avons donc répété du code, de manière à ne pas écrire plusieurs fois la ligne de `codeconsole.log()` .

[Je vous invite à revoir ces opérations dans la vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205519-repetez-du-code-grace-aux-boucles#/id/video_Player_2)

### Utilisez l’instruction while pour répéter du code

La boucle ***for*** est utilisée lorsque l'on connaît en amont le nombre de tours à effectuer. Mais cela n’est pas toujours possible ! Dans ce cas, nous utiliserons la boucle <mark>while, qui peut s’adapter à tous les cas.</mark>

Reprenons notre exemple de compteur avec un algorithme différent :

Tant que le compteur n’est pas égal à 3, on augmente le compteur de 1.

> Pour rédiger cette boucle while, nous allons utiliser la structure conditionnelle while (“tant que”, en français) qui sera suivie d’une condition entre parenthèses. Cette condition indique le moment où notre boucle doit s’arrêter.

Nous allons donc écrire :

```javascript
let i = 0
while (i < 3) {
    console.log(i)
    i++
}
```

Dans le code ci-dessus :

- on déclare la variable i, que l’on initialise à zéro, avant la boucle ;
- le while ne contient que la condition d’arrêt : tant que i est plus petit que 3 ;
- on incrémente i (i va gagner +1 à chaque tour de boucle). 

> Attention ! Si vous oubliez d’augmenter la valeur de i, alors la condition i < 3 sera toujours vraie, et vous aurez une boucle infinie ! Cela peut même faire planter votre navigateur !

[Je vous invite à revoir ces opérations dans la vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205519-repetez-du-code-grace-aux-boucles#/id/r-8205468)



### Résumé

Une boucle est une structure conditionnelle qui permet de répéter du code plusieurs fois.

- La boucle ***for*** permet de répéter du code pour un nombre défini de fois.

- La boucle ***while*** permet de répéter du code jusqu’à ce qu’une condition ne soit plus remplie.

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205519-repetez-du-code-grace-aux-boucles). 