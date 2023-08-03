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

## I. Déclarez une variable

vidéo : 

Pour commencer à programmer en J, il faut absolument déclarer une variable.
En programmation on manipule plein de données.

une donnée = une information (prénom, date de naissance, citation … quasiment n’importe quoi).

Pour travailler avec ces données, on a besoin de les ranger, on les range dans des variables.

Imaginons la mémoire de l’ordinateur comme une gigantesque armoire. Chaque variable est comme un tiroir de cette armoire.

—

Théorie :

Je veux que mon code retrouve “mon prénom”. “mon prénom” c’est une donnée que je vais ranger dans une variable.

Une variable c'est toujours un ensemble de 3 éléments : une valeur, un nom, un type.

***valeur*** = donnée	içi David  
***nom*** = ce qui permet de retrouver notre donnée (comme une étiquette sur notre tiroir 🙂)  
***type*** = catégorie de donnée (type basique), chaîne de caractères - string, chiffre - number, boolean - true/false.

—

Pratique :

### Déclarer une variable : En J, il faut choisir entre let et const.

***let***, permet de déclarer une variable dont la valeur peut changer au cours du code.  
***const*** (constante), permet de déclarer une variable dont la valeur reste la même tout au long du code.

déclarer une variable : `let/const nomVariable = valeur`

ex : `const monPrenom = David`		ou	`let monAge = 42`

—

En informatique, <mark>une variable est un conteneur qui stocke la donnée temporairement au sein de votre code. Cela vous permet d’enregistrer des données.</mark>

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

## II. Modifiez une variable

<mark>Une fois les variables déclarées, on peut les modifier.</mark>

Il y a 3 types de variables, de données basiques : 

- number (3, 42 ...)
- string ("hello, world!")  Récuperer un nom d'utilisateur
- Boolean (true / false)    Si un utilisateur est conecté

On va toucher n'y au type, n'y au nom, mais juste changer la valeur de la variable, en utilisant des opérations simples (un peu comme en math). Selon le type de donnée que l'on modifie, on ne peut pas réalisé les mêmes opérations.

### Number

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

### modifier une valeur de type "string"

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

### Boolean

Pour manipuler un boléen, il n'y a pas l'embarras du choix car il ne prennent que 2 valeurs (true / false), oui/non, vrai/faux, allumé/éteint.

```javascript
// On pourra écrire soit
let monBoolean = true
// soit
let monBoolean = false
```

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204726-modifiez-une-variable)

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

## III. Structurez des données grâce aux objets

![](/assets/images/2023-07-24 14-34-25.png)

Si un élément a plusieurs valeurs à la fois, on va utiliser les objets javascript.

***Objet*** : sorte de conteneur qui contient ***plusieurs valeurs*** attribuées ***à un même élément***. Ces données ne sont pas toutes du même type, certaine sont des string, number, booleen (information binaire).

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

Plus tard si je souhaite ***ajouter une propriété à l'objet***, c'est possible, en utilisant le `.` : 

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

<mark>Lorsque vous manipulez des objets JavaScript, vous avez également besoin d’accéder à leurs propriétés pour les stocker dans des variables, et les utiliser dans la suite de votre code ou dans un autre contexte.</mark>

Pour accéder à la propriété d’un objet, vous devez utiliser le point `.` suivi du nom de la propriété. Il ne vous reste plus qu’à stocker sa valeur dans une variable.

Dans le cadre de l’***objet monPersonnage***, vous écrirez :

```javascript
const nomDeMonPersonnage = monPersonnage.nom

// Vérification
console.log(nomDeMonPersonnage)
console.log(monPersonnage.nom)
```

### Déf

Un ***Object*** (objet, en français) JavaScript est un conteneur. Il est composé de propriétés qui ont chacune une valeur. Ainsi, le type de donnée Object offre la possibilité de stocker plusieurs valeurs en une seule fois, plutôt que de devoir stocker séparément nos valeurs dans plusieurs variables différentes.

### Résumé

Un ***objet*** en JavaScript peut posséder plusieurs propriétés qui auront pour chacune d’elles une valeur.

Pour déclarer un objet en JavaScript, vous devez utiliser les accolades  `{ }`

Pour ajouter ou récupérer une propriété, vous devez utiliser le point `.`

### Exercice

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

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204834-structurez-des-donnees-grace-aux-objets).

---

## Regroupez des données grâce aux tableaux

vidéo :

Nos variables commences à se multiplier. on va les regrouper en utilisant des tableaux.

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

méthode ***pop*** : permet de supprimer la dernière valeur de la liste. Pas besoin d'écrire une valeur entre parenthèses.

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

### Déf

Un ***tableau*** en JavaScript est donc un objet qui permet de lister plusieurs variables ou valeurs, et de les regrouper.

Les ***tableaux*** sont des conteneurs, comme les objets que nous avons vus dans le chapitre précédent. Pour effectuer des actions sur les données stockées dans votre tableau (ajouter, supprimer des données…), vous utiliserez des méthodes.

Les ***méthodes*** s’utilisent avec des parenthèses  ( )  . À l’intérieur de ces parenthèses vous pouvez passer des valeurs, c'est-à-dire des données, qui serviront à la méthode pour modifier les données de votre tableau. En réalité, vous avez déjà utilisé une méthode fournie par JavaScript : console.log() ! 

La ***copie par valeur***. Nous avons copié le contenu d’une variable à l’intérieur d’une autre variable. Nous avons donc deux variables indépendantes.

La ***copie par référence***. Les variables font référence au même espace mémoire.

### Résumé

- Un ***tableau*** est un conteneur qui permet de regrouper plusieurs valeurs ou variables.

- Un ***tableau*** possède une propriété ***length*** qui permet de connaître le nombre de données contenues dans un tableau.

- Une méthode s’utilise avec des parenthèses `( )` , et permet d’interagir avec le contenu du tableau. Il existe de nombreuses méthodes différentes mises à disposition par le langage.

- Lorsqu’on copie une ***variable simple***, JavaScript réalise une copie par valeur (la valeur est dupliquée).

- Lorsqu’on copie une ***variable complexe***, JavaScript réalise une copie par référence (les deux variables pointent sur la même valeur).

### +

Déclarer tableau `[]`  
Déclarer objet `{}`  
Pour utiliser des méthodes `()`

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8204994-regroupez-des-donnees-grace-aux-tableaux). [Doc Moz Tableau](https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Arrays).

---

***

## Appréhendez la logique de programmation

    Comprendre la logique de programmation de Javascript

Dans cette deuxième partie du cours,  vous allez rédiger un programme informatique qui répond à une logique de programmation : votre navigateur est capable de comprendre et d’interpréter ce programme.

### La notion d'algorithme

En tant que développeur, vous rédigez du code dans le but de développer un programme informatique. Vous allez donc écrire, en JavaScript, un ***ensemble d’instructions et d’opérations*** qui seront exécutées par un ordinateur dans un but précis.Dans notre cas, nous souhaitons coder un algorithme capable de :
- proposer des mots à un utilisateur ;
- vérifier que les mots entrés par l’utilisateur sont corrects. 

Un ***algorithme*** est une façon de concevoir les étapes d’un code dans le but de ***résoudre un problème donné***.

Dans notre cas, l’application AzerType va proposer des mots, et l’utilisateur devra taper ces mots correctement avec son clavier. Notre problème est donc le suivant : comment faire comprendre cela à l’ordinateur ?

L’idéal serait de lui fournir une liste d’étapes pour lui expliquer, pas à pas, chaque instruction qu’il doit exécuter. Eh bien un algorithme, c’est exactement ça !

Notre algorithme pourrait donc ressembler à cette suite d’étapes :

- Étape 1 : L’application propose un mot. 

- Étape 2 : L’utilisateur tape ce mot au clavier. 

- Étape 3 : Si le mot de l’utilisateur est exactement le même que le mot de l’application, alors on ajoute un point au score.

- Étape 4 : On passe au mot suivant.  

- Étape 5 : On recommence à l’étape 1, jusqu’à ce que le temps soit écoulé. 

Je vous rassure, nous n’irons pas plus loin sur la notion d’algorithmique dans ce cours. Tout ce que vous avez besoin de retenir, c’est qu’un algorithme vous aidera à bien penser vos étapes en amont de votre code. Toutefois, si vous souhaitez en savoir plus, n’hésitez pas à consulter le cours [Découvrez le fonctionnement des algorithmes.](https://openclassrooms.com/fr/courses/7527306-decouvrez-le-fonctionnement-des-algorithmes)

### Organisez votre code grâce aux blocs de code

Dans les chapitres précédents, nous avons écrit des lignes de code les unes à la suite des autres. Maintenant que nous suivons une logique de programmation, cette logique doit transparaître dans l’organisation de votre code. C’est là qu’interviennent les ***blocs de code***.

<mark>Les blocs de code sont des regroupements de lignes de code. Ils permettent d’organiser votre code et de clarifier à quoi sert un groupe de lignes de code. En JavaScript, ils sont délimités par des accolades  { }</mark>

Exemple de bloc de code :

```javascript
{
    const monChiffre = 4
    console.log(monChiffre)
}
```
Ici, j’ai utilisé un bloc de code pour déclarer la variable monChiffre.

Mais…. Il est un peu seul, ton bloc de code, non ?

Pour le moment, oui. 😃 Mais dans un programme informatique, les blocs de code sont associés à des ***structures conditionnelles*** et à des ***fonctions***. Je ne rentre pas plus dans les détails pour l’instant, car vous allez justement le découvrir dans cette partie en construisant votre premier fichier JavaScript.

### Installez votre environnement de travail

Utilisez un éditeur de code (IDE) tel que Visual Studio Code.

Une fois votre éditeur lancé, votre première étape consiste à créer un dossier qui contiendra tous les fichiers nécessaires à votre projet.

Dans VSCode : File > openFolder > FichierDuProjet

Pour exécuter du code Javascript, il faut au minimum 2 fichiers :
- un fichier .html : notre page web.
- un fichier .js : qui contiendra le code Javascript.

***index.html*** : 

```html
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

### Affichez la console de votre navigateur

- Ouvrir index.HTML dans navigateur (Ds VSCode : Clic D, Reveal in File Explorer).
- Afficher les Dev tool > Console

Dans la console, vous verrez notre “Hello World”, qui correspond à l’instruction écrite dans le fichier script.js.

Personne n’est à l'abri d’une erreur de code, même les développeurs les plus expérimentés. Prenez donc l’habitude de tester très régulièrement votre code. Il vous sera alors bien plus facile de trouver votre erreur qu’en ne testant qu’à la fin ! Cela vous évitera également de longues heures de débogage, au passage…

### Déf

Un ***algorithme*** est une façon de concevoir les étapes d’un code dans le but de résoudre un problème donné.

***IDE*** (Integrated Development Environment, ou environnement de développement intégré). Un IDE permet de regrouper tout ce dont nous aurons besoin pour écrire notre code. Tous les fichiers seront au même endroit, et le code sera coloré pour faciliter la lecture.

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

Pour un ordinateur, Il faut lui parler dans sa langue :

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

// vidéo

Je veux que mon téléphone affiche la liste de mes contacts. CaD, la photo de mon ami n°1, n°2, n°3, etc. Le problème, j'ai 500 contacts et je ne vais pas écrire l'instruction 500 fois. Pas de problème, je vais utiliser une boucle.

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

// Fin vidéo

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

- La ***boucle for*** permet de répéter du code lorsque l’on sait d’avance combien de fois il faudra le répéter.

Par exemple, si nous voulons demander exactement trois fois à l’utilisateur d’entrer un mot.

- La ***boucle while*** permet de répéter du code autant de fois qu’il le faut pour qu’une condition ne soit plus vraie.

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

### Exercice

- Factoriser le code suivant, c'est-à-dire de mettre en commun les parties répétées à l’aide d'une boucle :

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

Résultat de la factorisation :

```javascript
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
// length : propriété du tableau pour connaitre le nombre d'éléments.

// i = compteur; nombre de tours de boucle (nb d'élément ds le tableau; i++)

-  Pour rendre le jeu plus engageant, nous voulons que l’utilisateur puisse avoir le choix entre deux listes de mots différentes : une liste avec des mots et une liste avec des phrases.

```javascript
// SB93:)
const listMots = ["Cachalot","Pétunia","Serviette"]
const listPhrases = ["Pas de panique !", "La vie, l'univers et le reste", "Merci pour le poisson"]

let score = 0

let choix = prompt("Entrez listMots ou listPhrase : ")

if (choix === "listMots"){

for (let i = 0; i < listMots.length; i++){
  let motUtilisateur = prompt("Entrez un mot : " + listMots[i])
  if (motUtilisateur === listMots[i]){
    score++
  } 
}
} else {

for (let i = 0; i < listPhrases.length; i++){
  let motUtilisateur = prompt("Entrez un mot : " + listPhrases[i])
  if (motUtilisateur === listPhrases[i]){
    score++
  } 
}
}


console.log("Votre score est de : " + score + " sur " + listMots.length)
// SB93:) 30/07/23
```

Correction : 

```javascript
const listMots = ["Cachalot","Pétunia","Serviette"]
const listPhrases = ["Pas de panique !", "La vie, l'univers et le reste", "Merci pour le poisson"]

let score = 0

let choix = prompt("Veuillez choisir la liste : mots ou phrases")
while (choix !== "mots" && choix !== "phrases"){
    choix = prompt("Veuillez choisir la liste : mots ou phrases")
}

if(choix === "mots"){
    for (let i = 0; i > listMots.length; i++){
        let motUtilisateur = prompt("Entrez le mot : " + listMots[i])
        if (motUtilisateur === listMots[i]){
            score++
        }
    }
    console.log("Votre score est de " + score + " sur " + listMots.length)
} else {
    for (let i = 0; i > listPhrases.length; i++){
        let motUtilisateur = prompt("Entrez le mot : " + listPhrases[i])
        if (motUtilisateur === listPhrases[i]){
            score++
        }
    }
    console.log("Votre score est de " + score + " sur " + listPhrases.length)
}
```

[Le corrigé en vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205519-repetez-du-code-grace-aux-boucles#/id/r-8205506)

### Résumé

- Une boucle est une structure conditionnelle qui permet de répéter du code plusieurs fois.

- La boucle ***for*** permet de répéter du code pour un nombre défini de fois.

- La boucle ***while*** permet de répéter du code jusqu’à ce qu’une condition ne soit plus remplie.

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205519-repetez-du-code-grace-aux-boucles). 

---

## Organisez votre code grâce aux fonctions

// vidéo

Jusqu'içi, on a écrit notre code un peu en bazarre, comme ça vient.

On va mettre un peu d'ordre dans tout ça en apprenant à utiliser des fonctions. Ça veut dire, que l'on va regrouper des instructions, leurs données un nom, des paramètres (ce qui sera en Entrée) et un résultat ou valeur de retour (c'est la valeur que l'on récupère en Sortie).

En fait, une fonction c'est un peu comme "une machine à pain". Si vous avez une machine à pain, en Entrée vous mettez de la farine, de l'eau, de la levure, du sel et en Sortie, vous avez du pain.

Donc en Entrée, une fonction prends des paramètres. Les paramètres, c'est les ingrédients que vous mettez dans la machine à pain. Avec une machine et pas de farine, vous n'aurez pas de résultats. La machine traite ces paramètres et retourne le résultat, içi le pain.

Si vous modifier les paramètres, vous allez obtenir un résultat différent. Par exemple, si vous ajoutez des noix en Entrée, votre valeur de retour sera du pain aux noix. Mais peut importe les ingrédients, votre machine, elle, reste toujours la même machine à pain. C'est pareil pour le code, même si les paramètres sont différents, ***vous utilisez la même fonction***.

Si vous en avez marre du pain, on peut imaginer une fonction bien mathématique et bien concrète. Une fonction qui calcule la TVA par exemple.

Pour déclarer ma fonction, j'écris "function" puis le nom que je veux lui donner, en règle général, on utilise un verbe qui correspond à l'action de la fonction. Içi, je vais mettre "calculer TVA". Ensuite j'ouvre les parenthèses, c'est là que je vais insérer mes paramètres. Pour calculer une TVA ma fonction va avoir besoin de 2 valeurs d'Entrée : le prix hors taxe et le taux de la TVA. Ensuite, j'ouvre des crochets pour indiquer le fonctionnement de ma fonction, je veux qu'elle retourne le résultat d'un calcul, j'écris donc ***return***. Le calcul, c'est le prix hors taxe multiplier par le taux de la TVA, le tout diviser par 100, et je ferme l'accolade.

`function nomDeLaFonction (paramètres){fonctionnement de la fonction}`

![](/assets/images/2023-07-30 15-30-34.png)

Et voilà le travail ! Enfin pas tout à fait.

Avec ces 2 lignes de codes, on à créé un outils dans notre programme. Il existe, il est fonctionnel mais il n'est pas encore en marche. C'est un peu comme si j'avais ma voiture et que tous les voyants sont au vert mais qu'elle est encore à l'arrêt. Pour la faire avancer, il faudrat appeler la fonction.

Je vous montre comment faire dans la suite du chapitre.

Pour l'instant, retenez que l'on va pouvoir appeler cette fonction aussi souvent qu'on en aura besoin. Tout au long de notre code, on pourra appeler, "calculer TVA" avec plein de prix différents et on obtiendra toujours le bon résultat.

Ça va vraiment nous permettre d'organiser et de simplifier notre code.

Avec les fonctions, vous allez pouvoir commencer à créer des programmes un peu plus pointus mais aussi plus compréhensibles et plus faciles à maintenirs.

Une dernière chose, étends donner que l'on va commencer à compartimenter notre code; on va pouvoir définir la portée de nos variables. Une variable n'existe que dans un certain espace.

- D'un côté, on a les ***variables locales***. <mark>Variables déclarées au sein d'une fonction et qui ne sont pas utilisables en dehors de cette fonction.</mark>

- De l'autre, on peut aussi définir des ***variables globales***. Des variables déclarées en dehors d'une fonction, qui peuvent donc être utilisées au sein de n'importe qu'elles fonctions.

À notre niveau, on va utiliser surtout des variables locales. <mark>Moins on utilise de variables globales, meilleur est le code</mark>.

// Fin vidéo

Notre projet avance ! Nous pouvons maintenant proposer plusieurs mots ou phrases à l’utilisateur, compter son score et l’afficher. 🚀

Pour l’instant notre code est encore relativement petit, mais il va grandir au fur et à mesure du développement. Il est donc très important de l’organiser pour qu’il reste lisible et fonctionnel. C’est d’autant plus important que, en tant que développeur, vous devrez fréquemment dupliquer du code. Voyons ensemble comment éviter cette répétition et réaliser cela efficacement, grâce aux fonctions ! 😃

### Découvrez les fonctions

Une fonction est un bloc de code auquel on attribue un nom. Appeler cette fonction permet d’exécuter le code qu’elle contient. On parle donc de fonction, car il s’agit d’un bloc de code qui a un rôle spécifique au sein de votre fichier JavaScript. Une fonction peut ainsi : 

- contenir des informations, qu’on appelle paramètres ;
- retourner un résultat ;
- effectuer une action. 

En fait, vous utilisez déjà des fonctions depuis le début de ce cours, sans même le savoir ! Par exemple, quand vous écrivez :

```javascript
motUtilisateur = prompt('Entrez un mot')
```

Prompt est une fonction : 

- elle prend en paramètre le message à afficher (ici, “Entrez un mot”) ;
- elle retourne un résultat : le mot tapé par l’utilisateur. 

Dans l’exemple ci-dessus, le retour de la fonction prompt est copié dans motUtilisateur. 

### Rédigez une fonction en JavaScript

Dans le cadre de notre application, nous souhaitons écrire une fonction qui va générer une phrase pour donner le score final à l'utilisateur. Cette fonction prendra donc en paramètre deux informations : 

- le score ;

- le nombre de questions.

Elle retournera une phrase contenant ces informations.

Cela donne donc :

```javascript
function retournerMessageScore(score, nombreQuestions) {
    let message = 'Votre score est de ' + score + ' sur ' + nombreQuestions
    return message
}
```

Revenons en détail sur ce morceau de code :

- le mot-clé function (“fonction”, en anglais) est suivi du nom “retournerMessageScore”. Ce mot est ici obligatoire pour définir la fonction, mais il n’est ensuite plus nécessaire lorsqu’on l’utilise ;

- par conséquent, la fonction “retournerMessageScore” est créée ;

- entre parenthèses sont indiqués les paramètres envoyés à cette fonction : “score” et “nombreQuestions” ;

- entre accolades est indiqué le bloc de code qui sera exécuté quand la fonction sera appelée (let message… et return) ;

- dans ce bloc de code, nous déclarons une variable message dans laquelle nous créons notre message ;

- le code est finalisé avec le nouveau mot-clé return. Ce mot signifie que la fonction va retourner le contenu de message.

Si vous ajoutez ce code dans votre projet et que vous le testez, il ne provoquera aucun changement pour le moment. Ces instructions définissent notre fonction… Mais pour qu’elle produise son effet, nous devons ***l’appeler***.

Par exemple :

```javascript
let nouveauMessage = retournerMessageScore(5, 10)
console.log(nouveauMessage)
```

Gardez également en tête que l’***ordre des paramètres est très important*** ! La fonction a un premier paramètre nommé “score” et un second paramètre nommé “nombreQuestions” : 

- si on appelle la fonction avec 5 et 10, 5 étant le premier paramètre, il ira donc dans la variable “score” ;

- le 10 étant positionné en second, il ira dans la variable “nombreQuestions”, positionnée en second aussi. 

![schéma fonction](/assets/images/2023-07-30 17-41-47.png)

[Cette opération en vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205714-organisez-votre-code-grace-aux-fonctions#/id/r-8205582)

Exemple :

```javascript
// Déclarer une fonction

function retournerMessageScore(score, nombreMotMax) {
    let message = "Le score est de " + score + " sur " + nombreMotMax
    return message
}

// Apeller la fonction avec (score et nb de mots)

let retourFonction = retournerMessageScore(1, 3)
console.log(retourFonction)
```

### Codez proprement

Vous vous rendrez compte très rapidement que les fonctions sont un élément majeur de votre code. Il est donc très important de ***respecter quelques bonnes pratiques*** pour prévenir tout problème. Voici quelques conseils.

#### Définissez une tâche spécifique pour chaque fonction

Dans l’idéal, on attribue ***une seule tâche à une fonction*** : afficher, calculer, lancer une opération, initialiser… Si une fonction s’occupe de tout gérer à la fois, elle comportera beaucoup de lignes, difficiles à comprendre, à modifier et à tester.

#### Écrivez des fonctions courtes

Dans l'idéal, vos fonctions ne doivent pas dépasser 30 lignes. Si le but de la fonction est clair, un code court est généralement suffisant pour l’atteindre.

Si la fonction prend trop d’ampleur, c’est peut-être qu’elle est mal conçue, qu’elle fait trop de choses, ou qu’il faudrait la découper en plusieurs sous-fonctions.

- Nommez clairement vos fonctions

Comme pour les variables, le nom d’une fonction devrait être suffisamment clair pour permettre d’en deviner le contenu sans lire le code qu’elle contient.

Vous pouvez par exemple utiliser un verbe pour nommer vos fonctions. Si une fonction s’appelle resultat, que fait-elle ? Elle calcule le résultat ? Elle l’affiche ? Elle le réinitialise ? En utilisant des noms tels que afficherResultat, calculerResultat, reinitialiserResultat… là, plus aucune ambiguïté ! 😃

- Nommez clairement vos paramètres

Les paramètres doivent également être le plus explicites possible :

```javascript
lancerJeu(a) {
    // code
}
```

Que dois-je envoyer à ma fonction pour remplir le paramètre a ? Est-ce qu’il représente le nom du joueur ? La liste des mots qu’il doit taper ? Autre chose ? 

Ici, est donc préférable d’écrire :

```javascript
lancerJeu(listeMots) {
    // code
}
```

Rien qu’avec le nom, nous savons maintenant que le paramètre contient en réalité un tableau avec une liste de mots. N’oubliez pas non plus qu’en cas d'ambiguïté, vous pouvez toujours insérer un commentaire pour ajouter une précision !

### Organisez votre code en plusieurs fichiers

Découper votre code en plusieurs fonctions permet de mieux organiser vos idées et facilite les modifications, mais ce n’est pas suffisant…

Si votre projet continue de grandir, regrouper toutes vos fonctions au même endroit risque de rapidement causer des problèmes de lisibilité et de navigation. C’est encore plus vrai si vous êtes plusieurs à travailler sur le même projet !

Souvenez-vous, quand nous avons créé notre fichier index.HTML, nous avons écrit :

```javascript
<script src="script.js"></script>
```

… afin d’inclure notre fichier script.

Imaginez maintenant que nous voulions créer un fichier de configuration qui contiendrait nos deux tableaux listeMots et listePhrases. Cela nous permettrait de faire évoluer ces tableaux sans risquer de modifier par erreur la logique du code ! 😃

Pour y parvenir, nous pouvons inclure ce nouveau fichier en insérant une nouvelle ligne dans le fichier HTML pour préciser le chemin du nouveau fichier     

```javascript
<script src="config.js"></script>
<script src="script.js"></script>
```

Dans cet exemple, j’ai mis le fichier config.js avant script.js, car les variables que je vais définir dans le fichier config.js seront utilisées par script.js. Elles doivent donc être définies en premier.

Ensuite, nous devons définir le contenu du fichier. Pour cela, nous allons supprimer les deux const listeMots et listesPhrases de script.js, et les copier  dans config.js.

```javascript
// Liste des mots utilisés pour le jeu
const listeMots = ['Bonjour', 'Salut', 'Coucou']
const listePhrases = ['Bonjour, comment allez-vous ?', 'Salut, ça va ?', 'Coucou, ça va ?']
```

N'hésitez pas à ajouter des commentaires pour donner des précisions dans votre code. Mettre un commentaire inutile n’est pas très grave. En revanche, ne pas avoir un commentaire utile peut parfois faire perdre beaucoup de temps.

[Ces opérations en vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205714-organisez-votre-code-grace-aux-fonctions#/id/video_Player_3)


### Maîtrisez la portée des variables

Nous avons commencé à apprendre le JavaScript en déclarant des variables. Maintenant que vous manipulez des fonctions et des blocs de code, vous devez maîtriser une notion importante : la portée des variables. Pas de panique, je vous explique ! 😉

Les variables ont une portée, qui est définie par l’endroit où cette variable est déclarée. Ainsi, on distingue deux types de variables :  

- les variables globales : visibles et utilisables dans l’ensemble du code ;

- les variables locales : qui ne peuvent être utilisées qu’au sein du bloc de code dans lequel elles sont définies.

Ouh là là là…  Aurais-tu un exemple pour rendre les choses plus claires ? 😱

Bien sûr ! Prenons l’exemple ci-dessous :

```javascript
let monNombre = 1
// monNombre est une variable globale, car elle est déclarée en dehors d’un bloc de code

function afficheUnNombre() {
    let monNombreLocal = 2
   // monNombreLocal est une variable locale, car déclarée uniquement au sein d’une fonction
    console.log("Intérieur de la fonction : ")
    console.log(monNombre) // monNombre est accessible
    console.log(monNombreLocal) // monNombreLocal est accessible
}

afficheUnNombre()
console.log("Extérieur de la fonction : ")
console.log(monNombre) // monNombre est accessible
console.log(monNombreLocal) // monNombreLocal n’est pas accesssible
```

Si vous copiez-collez ce code dans votre éditeur de code, vous constaterez plusieurs choses :

- les chiffres 1 et 2 apparaissent en premier : ils sont affichés dans la fonction afficheUnNombre ;

- le dernier console.log renvoie une erreur, due au fait que la variable monNombreLocal est définie au sein du bloc de code de la fonction afficheUnNombre.

Comme il s’agit d’une variable locale, elle n’est pas accessible dans l’ensemble du code. Elle est donc inconnue lorsqu’on tente de l’afficher hors de la fonction qui la déclare.

À mesure que votre code s’agrandit, les variables s’accumulent. Certaines peuvent désigner le même élément, avoir le même nom… et provoquer des résultats inattendus 😱. ***En restreignant une variable à un bloc de code, vous l’empêchez d'interférer avec une autre variable globale. Cela vous évitera de nombreux bugs particulièrement difficiles à trouver !***


### Exercice

[Découpez votre code en fonctions](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205714-organisez-votre-code-grace-aux-fonctions#/id/r-8205679)


###  Résumé

Une fonction est un morceau de code qui accomplit une tâche spécifique. L’utilisation de fonctions permet d’organiser son code en blocs fonctionnels.

Pour créer une fonction en JavaScript, on utilise le mot-clé function et on lui attribue un nom.

On peut appeler une fonction en utilisant son nom, suivi de parenthèses  ()  . Si la fonction comporte des paramètres, ceux-ci sont ajoutés entre les parenthèses. 

Vous pouvez définir une valeur de retour que la fonction renvoie après son exécution. Cette valeur retournée par la fonction pourra alors être utilisée dans la suite du code. 

Séparer son code en plusieurs fonctions et en plusieurs fichiers vous permet de mieux découper votre code, et donc de le rendre plus simple à comprendre.  

Une variable déclarée dans un bloc de code n’est accessible que dans ce bloc de code.


### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205714-organisez-votre-code-grace-aux-fonctions)

---

## Récupérez un élément d’une page web

// vidéo

Jusqu'içi, on a appris des notions de programmation générales. Des briques de base qui resterons valables dans tous les languages de programmations. Mais maintenant, on va se concentrer sur une spécificité de Javascript et on va ***communiquer directement avec le HTML***. Il n'y a que le javascript qui est capable de faire ça.

Concrètement, ça veut dire que l'on va pouvoir ***récupérer, modifier,  créer et supprimer des éléments de notre page HTML***.

Étape 1 : Récupérer un élément. Pour ça, petit rappel HTML. Les balises, éléments de base du codage en HTML.

À partir de maintenant, il va falloir garder en tête que les balises HTML correspondent au code qui se cache derrière chaque éléments de l'interface d'une page web.

Donc la structure d'une page HTML, c'est une grande imbrication d'éléments représentée par des balises.

![Schéma des éléments HTML en branches](/assets/images/2023-08-01 11-59-23.png)

Au fur et à mesure qu'on ajoute des éléments, on rajoute des branches.

C'est l'***arbre DOM***, c'est la ***structure d'une page web*** représentée sous forme d'arbre, avec des branches pour chaques imbrications.

C'est avec ce DOM que l'on va intéragir à partir de maintenant.

getElementById :

Concrétemment, comment intéragir avec le DOM : On va faire appelle à une ***variable globale*** un peu magic qui s'appelle ***document***. En particulier "document" va nous ***permettre d'intéragir avec le DOM grâce à la méthode "getElemntById"***

Exemple :

Sur ma page web, j'ai intégré un petit jeu que j'ai placé dans une div, pour accéder à cette div, je vais écrire en javascript 'document.GetElementById'. Pour que ça marche, il faut que la div ait un "ID".

![](/assets/images/2023-08-01 12-14-29.png)

Voilà, on a récupérer notre élément.

Une fois cela fait, on va pouvoir agir deçu. Modifier son style, son contenu, voir le supprimer. Ce sera dans les chapitres qui suivent.

Mais d'abord, je veux vous montrez une deuxième façon d'***accéder à un élément*** dans le cas où on a pas d'ID. ***Grâce aux sélécteurs CSS***.

Par exemple si on veut accéder à la balise `<main>`, en CSS on écrit `main {propriétés}`.

En javascript on écrit :

```javascript
// Pour récupérer la balise "main"
let maBaliseMain = document.querySelector("main")

// Pour récupérer toutes les div de notre document
let mesBalisesDiv = document.querySelectorALL("div")
```

Donc :

`querySelector` pour récupérer un élément HTML en particulier.  
`querySelectorAll` pour récupérer tous les éléments correspondants à un même sélécteur.

![](/assets/images/2023-08-03 10-49-24.png)

Dans mon exemple, je l'utilise pour récupérer toutes les div mais je pouurrai aussi récupérer toutes les images de ma page pour les affichées en grand ou tous les textes pour en changer la couleur.

Le principe, c'est qu'une fois que j'ai récupérer mes éléments, je vais pouvoir les modifier à ma guise.

Génial !

// Fin vidéo


Dans la partie précédente, nous avons découvert la logique de programmation en JavaScript, et nous avons manipulé des structures conditionnelles, des boucles et des fonctions. Nous avons fait une belle partie du chemin, mais pour l’instant, nous nous sommes contentés d’écrire dans la console. Notre prochaine étape est donc de manipuler directement une page HTML pour la rendre interactive. Dans le cadre de notre application Azertype, cela permettra d’afficher en HTML les mots à recopier et le score.

Notre première étape, dans ce chapitre, est d’établir un lien entre le code HTML et le code JavaScript. Cela nous permettra, dans le chapitre suivant, de modifier le code HTML directement depuis notre code JavaScript. Alors, avant de rentrer dans le vif du sujet, regardons ensemble comment une page web est structurée ! 😉
Appréhendez la structure d’une page web

Généralement, une page web est constituée de deux parties :

- un head qui donne des informations générales sur la page ;

- un body qui contient ce qui est affiché dans la page. 

- Voici un exemple de body pour une page simple :

```html
<body>
    <header>
        <h1>AzerType</h1>
    </header>

    <main>
        <div>
            <h2>Le jeu</h2>
            <p>Un petit texte</p>
        </div>
        <div>
            <h2>Une autre div</h2>
            <p>Un autre texte</p>
        </div>
    </main>

    <footer>
        @Copyright : OpenClassrooms.
    </footer>
</body>
```

Ce code HTML est simple. Il est constitué d’un header avec un titre, d’un corps (main) et d’un footer.

Ce code est un peu structuré comme un arbre, c’est pourquoi on appelle cette structure l’arbre DOM (Document Object Model, ou modèle objet du document, en français). En fait, JavaScript ne lit pas une page HTML comme du simple texte. Il la représente comme une structure organisée en parents/enfants, et composée de nœuds qui représentent des balises.

Ouh là là là, ça devient un peu abstrait ton truc, là… 😅

C’est un peu imagé oui, mais revenons ensemble sur l’illustration de l’arbre DOM ci-dessous :

![](/assets/images/16836136690232_STATIC-P3C1.png)

|Illustration de la structure de l’arbre DOM|

Dans la structure ci-dessus :

- le body en haut représente la racine de l’arbre DOM ;

- de cette racine se déploient des branches (en bleu sur l’image) ;

- ces branches mènent à des nœuds : header, main, footer, h1, h2, div, p… ;

- les branches se terminent généralement par une feuille : texte. 

En développement informatique, on dit que header, main et footer sont les noeuds enfants de body, et que body est le parent de ces nœuds.

Chaque nœud de cet arbre DOM (header, main, div…) est un objet HTMLElement. Pour le dire autrement, JavaScript a regroupé dans un même objet deux choses : 

- les informations sur cet objet (son nom, son id, sa position, etc.) : ce sont les propriétés de l’objet ;

- ce que cet objet est capable de faire (réagir au clic, par exemple) : ce sont les méthodes. 

Dans ce cours, nous explorons plusieurs propriétés et méthodes, mais il en existe d’autres. Si vous voulez en savoir plus, la documentation est à votre disposition. 😃

### Récupérez un élément du DOM

Dans ce chapitre, notre but est de récupérer certains éléments de l’arbre DOM, qui a pour racine la balise body. Cependant, vous vous souvenez peut-être que nos fichiers JavaScript sont stockés dans la balise head, qui se situe avant le body.

Utilisez ***defer*** pour différer l’exécution du script

Pour manipuler le DOM, JavaScript doit ainsi construire une variable globale, document, qui est donc accessible depuis n’importe où dans notre code. Cependant, pour construire cette variable, la page HTML doit être chargée en entier. Hors, le script étant lancé dans la balise head, avant que le body ne s’affiche à l’écran, la page HTML n’existe pas encore. Nous devons donc attendre que la page ait fini de charger avant d’utiliser la variable document.

Pour résoudre ce problème, la méthode la plus efficace est d’ajouter le mot-clé defer dans la balise script. Concrètement, cela revient à demander au navigateur “Si tu rencontres la balise script, diffère sa prise en compte et attends que la page soit chargée.”

```js
<script src="scripts/config.js" defer></script>
<script src="scripts/script.js" defer></script>
<script src="scripts/main.js" defer></script>
```

### Utilisez différentes syntaxes pour récupérer un élément

JavaScript propose tout un éventail de méthodes pour récupérer les éléments du DOM. Dans ce chapitre, nous en aborderons trois :

- getElementById ;
- querySelector ;
- querySelectorAll.

Il existe bien sûr d’autres méthodes, et je vous invite d’ailleurs à les découvrir par vous-même. L’essentiel est de choisir la méthode la plus adaptée à la problématique suivante : cibler le ou les éléments qui nous intéressent au milieu d’une page HTML souvent très conséquente. 

Récupérez un élément avec ***getElementById***

La première méthode, et probablement la plus simple, est getElementById. Comme son nom l’indique, elle permet de récupérer un élément en fournissant son id en paramètre.

- Dans notre application par exemple, nous affichions jusqu’à maintenant le mot à recopier dans le texte du prompt. Désormais, notre objectif est de l’afficher dans une zone de la page dédiée.

Pour cela, nous pouvons commencer par créer une div dans le HTML. Pour la distinguer des autres, nous lui fournissons un id :

```html
<body>
    <div id="zoneProposition">Cachalot</div>
</body>
```

Pour accéder à cette balise, nous allons donc écrire :

```js
let baliseZoneProposition = document.getElementById("zoneProposition");
console.log(baliseZoneProposition);
```

Ici, nous avons demandé à JavaScript, depuis document, donc toute la page : “Trouve-moi un élément HTML qui a pour id zoneProposition”. Puis nous avons mis le résultat dans la variable baliseZoneProposition. 

Quand nous faisons un console.log de cette variable, nous constatons bien le contenu de notre variable baliseZoneProposition, et nous retrouvons bien notre div :

![](/assets/images/2023-08-02 13-08-57.png)

Cette variable est un objet de type HTMLElement. Si nous cliquons sur le petit triangle à côté de cette div pour déployer le contenu, les détails de cet objet HTMLElement vont s’afficher, comme dans la capture d’écran ci-dessous.

[capture écran](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205925-recuperez-un-element-d-une-page-web#/id/r-8208156)

Ah oui…. Ca fait beaucoup d'informations, tout ça !

Eh oui… JavaScript propose beaucoup de propriétés et de méthodes sur les objets HTLMElement. Pour vous, ce sont autant d’opportunités d’aller les piocher en fonction de vos besoins !

Enfin, comme pour n’importe quel objet en JavaScript, vous pouvez accéder aux propriétés de votre nœud grâce au point “.” .

Par exemple, pour afficher la hauteur de l’élément dans votre console, vous pouvez écrire :

```js
console.log(baliseZoneProposition.clientHeight);
```

Récupérez un élément ***QuerySelector***

Lorsqu’on a un id sur nos éléments, document.getElementById est une bonne option pour les récupérer. Malheureusement, il arrive régulièrement que ça ne soit pas le cas !

JavaScript a donné une réponse particulièrement intuitive à ce problème : utiliser les sélecteurs CSS. En gros, si vous savez désigner un élément en CSS, alors il vous suffit de reprendre exactement la même syntaxe ! 😃

Modifions légèrement le contenu de notre page HTML pour illustrer cela :

```html
<body>
    <div id="zoneProposition">
        Entrez le mot : <span>Cachalot</span>
    </div>
</body>
```

Pour mettre le mot Cachalot en gras en CSS, nous aurions écrit :

```js
#zoneProposition span {
    font-weight: bold;
}
```

Ce code signifie : “Il faut mettre la police d’écriture en gras pour tous les span contenus dans un élément qui a l’id zoneProposition.”

querySelector nous permet de trouver le premier élément qui correspond au sélecteur CSS proposé :

```js
let baliseZonePropositionSpan = document.querySelector("#zoneProposition span");
console.log(baliseZonePropositionSpan);
```

Et voilà le résultat dans la capture d’écran ci-dessous : nous voyons dans la console que nous avons bien trouvé notre span.

[Résultat](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205925-recuperez-un-element-d-une-page-web#/id/r-8208185)

Notez que  #  est présent devant l’id, comme on l’écrirait en CSS, alors que ce  #  n’était pas nécessaire avec getElementById.

Récupérez plusieurs éléments avec ***QuerySelectorAll***

Ici, le principe est le même que pour tous les éléments dans une liste de type NodeList (ou liste de nœuds, en français).

Modifions à nouveau notre body :

```html
<body>
    <div class="zoneChoix">
        <input type="radio" name="optionSource" id="mots" value="1" checked>
        <label for="mots">Mots</label>
        <input type="radio" name="optionSource" id="phrases" value="2">
        <label for="phrases">Phrases</label>
    </div>
    <div class="zoneProposition">
        Entrez le mot : <span>Cachalot</span>
    </div>

</body>
```

Dans ce code, j’ai ajouté une nouvelle div avec la classe zoneChoix. Cette div contient deux inputs de type radio.

Pour récupérer tous les inputs de type radio d’un seul coup, je peux donc écrire :

```js
let listeInputRadio = document.querySelectorAll(".zoneChoix input");
console.log(listeInputRadio);
```

Notez que j’ai écrit .zoneChoix et pas #, car ici, j’ai mis une classe à ma div et pas un id.

Et voici le résultat : nous obtenons une NodeList.

[Résultat](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205925-recuperez-un-element-d-une-page-web#/id/r-8208212)

Nous voyons bien ici notre NodeList. Pour reprendre l’image de l’arbre DOM, JavaScript a sélectionné dans cet arbre les nœuds qui correspondent à notre sélecteur CSS.

Nous allons devoir parcourir les différents éléments de cette liste un par un pour y accéder. Nous utiliserons donc une boucle :

```js
for (let i = 0; i < listeInputRadio.length; i++) {
    console.log(listeInputRadio[i]);
}
```

Et voilà le résultat, nous retrouvons bien le détail de tous nos éléments :

[Résultat](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205925-recuperez-un-element-d-une-page-web#/id/r-8208233)

[Récap vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205925-recuperez-un-element-d-une-page-web#/id/video_Player_2)


---



`defer` pour différer l'exécution du script.
`<script src="script.js" defer></script>`

document = la page HTML

getElementById : Récupérer élémént par son ID

```html
<div id="divJeu">

</div>
```

```javascript
let divJeu = document.getElementById("divJeu")
// Pour tester avec console.log
console.log(divJeu)
```

Methode querySelector

```html
<div id="divJeu">
    <h2>Le jeu</h2>
</div>
```

```javascript
let h2 = document.querySelector("#divJeu h2")
// Pour tester avec console.log
console.log(h2)
```

Methode querySelectorALL

```html
//  Récupérer l'intégralité des h2
<div id="divJeu">
    <h2>Le jeu</h2>
</div>
<div id="divAutre">
    <h2>Une autre Div</h2>
</div>
```

```javascript
let listeh2 = document.querySelectorAll("#divJeu h2")
// Pour tester avec console.log
console.log(listeh2)
```

### Résumé

Une page web est constituée de balises HTML, et repose sur une structure que l’on appelle DOM. Cette structure permet de relier les balises entre elles.

Pour récupérer un élément du DOM :

- utilisez `defer` dans l’inclusion de vos fichiers JS pour retarder leur prise en compte, afin que la variable document ait le temps d’être créée ; 

- partez du point d’entrée du DOM : la variable `document` ;

- utilisez les méthodes adaptées : `getElementById`, `querySelector` ou `querySelectorAll`.

### +

[source](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8205925-recuperez-un-element-d-une-page-web) [HTMLElement Moz](https://developer.mozilla.org/fr/docs/Web/API/HTMLElement)

---

## Modifiez un élément d’une page web

### Modifiez un élément du DOM

Pour modifier un élément du DOM, JavaScript propose là encore de nombreuses méthodes. Nous en aborderons deux dans ce chapitre :

- setAttribute : méthode la plus générique, qui permet de spécifier n’importe quel attribut ;
- classList : propriété spécifique qui permet de modifier des classes. 

```html
<img id="premiereImage" src="image.jpg" alt="Ceci est une image de test" class="photo flexCenter">
```

setAttribute pour modifier les attributs

```js
let baliseImage = document.getElementById("premiereImage");
baliseImage.setAttribute("alt", "Ceci est la nouvelle valeur de alt");
```

nous pouvons plus simplement écrire :

```js
baliseImage.alt = "Ceci est une image de test modifiée";
```

classList pour modifier les classes :

```html
<div class="listeMots centree actif photo"></div>
```

```js
    baliseImage.alt = "Ceci est une image de test modifiée";
    baliseImage.classList.add("nouvelleClasse")
    baliseImage.classList.remove("photo")
```

## Créez un nouvel élément dans une page web

Nous savons maintenant comment modifier un élément existant. Mais comment créer un nouvel élément dans une page web ? La façon de faire est toujours la même : d’abord créer l’élément, puis le lier à un élément déjà existant de la page.

Pour créer nos éléments, là encore JavaScript nous propose plusieurs manières de faire. Nous en aborderons deux dans ce chapitre :

- la méthode createElement ;

- la propriété innerHTML. 

### Créez une nouvelle balise grâce à createElement

CreateElement est une méthode fournie par JavaScript, accessible depuis document. Elle permet de créer n’importe quelle balise :

```js
let nouvelElement = document.createElement("div");
```

Ici, vous pouvez remplacer div par le nom de balise que vous désirez, section, p, h1, etc. Une fois cette balise créée, vous pouvez la configurer avec les méthodes que nous avons vues dans le chapitre précédent. 

Dans nouvelElement, nous aurons un objet HTMLElement qui représente la balise que nous avons créée. 
Insérez votre balise dans la page

Une fois l’élément créé, il n'apparaît pas encore dans la page. Pour que cette nouvelle balise apparaisse, nous devons l’insérer dans l’arbre DOM afin que JavaScript sache exactement à quel endroit il faudra mettre l’élément. Pour cela, nous devons : 

- déterminer quel sera l’élément parent ;
- utiliser appendChild (littéralement en anglais : “ajouter un enfant”).

```js
// Récupérer un élément parent existant
let parentElement = document.getElementById("conteneur");

// Ajouter le nouvel élément au parent
parentElement.appendChild(nouvelElement);
```

ci, j’ai ajouté une balise div à un élément que j’ai récupéré grâce à getElementById.

Il existe d’autres méthodes pour insérer des éléments dans l’arbre DOM, comme prepend, before ou insertAdjacentElement. N’hésitez pas à consulter la documentation pour en savoir plus.
Utilisez la propriété innerHTML pour insérer du HTML

Avec la méthode createElement, nous créons un élément que nous pouvons modifier et insérer dans le HTML. Mais que se passe-t-il quand nous devons créer et imbriquer de nombreux éléments ?

Regardons ensemble avec cet exemple plus complexe :

```js
// Définition des variables contenant le texte du titre et du paragraphe
let contenuTitre = "Azertype"
let contenuParagraphe = "L'application pour apprendre à taper plus vite !"

// Création d'un div avec createElement. Dans cette div, on va créer un titre h1 et un paragraphe p
let nouvelleDiv = document.createElement("div")
let nouveauTitre = document.createElement("h1")
let nouveauParagraphe = document.createElement("p")

// On ajoute du texte dans le titre et le paragraphe
nouveauTitre.textContent = contenuTitre
nouveauParagraphe.textContent = contenuParagraphe

// On ajoute le titre et le paragraphe dans la div
nouvelleDiv.appendChild(nouveauTitre)
nouvelleDiv.appendChild(nouveauParagraphe)

// On ajoute la div dans le body
let body = document.querySelector("body")
body.appendChild(nouvelleDiv)
```

Dans le code ci-dessus :

- je crée deux variables qui vont contenir le texte du titre et du paragraphe ;

- je crée trois éléments, une div, un titre et un paragraphe ;

- j’insère du texte créé avec les variables dans le titre et le paragraphe ;

- j’insère du titre et du paragraphe en tant qu’enfants de la div ;

- j’insère une div en tant qu’enfant de la balise body. 

Cela fonctionne parfaitement, et donne le résultat suivant :

![](/assets/images/2023-08-02 12-54-01.png)

Alors oui, ça marche, mais avouez que c’est un peu fastidieux avec la méthode createElement. Comment savoir avec précision quels éléments sont les enfants de qui, quand le code est complexe ? Tout cela rend la maintenance compliquée… Dans ce cas, la solution est d’écrire directement du HTML, sous forme de texte, et de l’insérer dans une propriété innerHTML. 
Utilisez l’interpolation pour générer du HTML

Pour générer le HTML, nous pouvons utiliser la concaténation, comme nous l’avons vu au début de ce cours avec + .  Dans ce chapitre, l’heure est venue de découvrir une nouvelle méthode plus efficace encore : l’interpolation.

L’interpolation ? 🤨 Ça marche comment ?

L’interpolation consiste à entourer la chaîne de caractères avec des backticks : `  . Ce caractère correspond à l’accent du “è”, mais sans le e en dessous 🙂. Ainsi, quand nous voulons insérer une variable, il suffit de l’entourer avec${} .

Voici un exemple :

```js
let contenuTitre = "Azertype"
let contenuParagraphe = "L'application pour apprendre à taper plus vite !"

let div = `
    <div>
        <h1>${contenuTitre}</h1>
        <p>${contenuParagraphe}</p>
    </div>
```

OK je vois…. Mais du coup pourquoi utiliser ça plutôt que l’opérateur + ?

Car l’interpolation est plus sécurisée que la concaténation simple avec  +  , et souvent plus facile à lire. N’hésitez donc pas à vous en servir à chaque fois que vous en avez besoin !
Insérez votre HTML grâce à innerHTML

Maintenant que le code HTML est généré, comme avec createElement, nous devons l’insérer dans un élément existant de la page. Pour cela, on choisit la balise qui va contenir notre code HTML, et on met simplement ce code HTML dans la propriété innerHTML :

```js
let body = document.querySelector("body")
body.innerHTML = div
```

Et voilà, le tour est joué ! 🥳

[recap  vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8206130-creez-un-nouvel-element-dans-une-page-web#/id/r-8206109)

### résumé

Créez un nouvel élément HTML : 

- en utilisant la méthode createElement puis en liant l’élément créé à la page grâce à appendChild ;

- en utilisant la propriété innerHTML pour insérer directement du HTML sous forme de texte à l’intérieur d’une balise.

L’interpolation permet de générer facilement des chaînes de caractères complexes en utilisant des backticks.

---
---
---
---

## Interagissez avec un élément d’une page web grâce aux événements

//vidéo

Depuis le début de ce cours, on a écrit du code qui s'exécute ligne par ligne jusqu'à la fin du programme. Un peu comme un livre qu'on lirait de la première ligne jusqu'à la dernière page. Mais maintenant ça va changer parqu'on va commencer à utiliser des événements.

En programmation, un événement c'est un signal qui est envoyer par le navigateur.

Par exemple, pour indiquer que l'utilisateur a réaliser une action. Le fait de cliquer sur un bouton est un événement, le fait de terminer le chargement d'une page aussi. Le fait d'envoyer un formulaire, pareil !

Toutes ces actions, ces événements peuvent envoyer un signal.

À partir de maintenant, on va utiliser ces signauxpour lancer l'exécution de certaines fonctions dans notre code. En gros, les signaux liers au événements vont agir un peu commme un coup de siflet et indiquer le top départ d'une action programmée. On appelle ça la "programmation événementielle".

Le principe, c'est d'au lieu d'écrire notre code dans l'ordre chronologique pour qu'il s'exécute ligne par ligne, on va écrire des blocs de codes qui ne vont pas êtres exécutées automatiquement.

Ces blocs de codes, on va faire en sorte que par défaut, ils ne soient pas pris en compte. Dans le cas ou un événement spécifique se réalise et seulement dans ce cas là, alors notre bloc de codes va s'exécuté.

Par exemple, on peu vouloir faire en sorte que "bonjour" s'affiche seulement quand l'utilisateur clique sur le bouton. Dans ce cas, on va utilisé la programmation événementielle.

En fait, au lieu de se lire comme un roman du début jusqu'à la fin, notre code va commencer à ce comporter un peu comme dans un jeu vidéo : si je vais parler au grand ssage de la fôret au début du jeux, il n'a rien à me dire. Quand j'y retourne après avoir sauver le dragon, alors saudainement, il a des tas de conseils à me donner. C'est un peu le même principe.

Concrêtement, comment notre code va savoir si un événement c'est produit ou non ? Il va tendre l'oreil...

On va utiliser un fonction "eventListener", fonction charger d'écouté un événement.

// Fin vidéo

Nous savons désormais comment récupérer un élément HTML, le modifier et en créer de nouveaux. Dans ce chapitre, nous apporterons une nouvelle dimension à notre page grâce à la ***programmation événementielle***. Concrètement, nous allons découvrir comment ***réagir à des événements*** comme le clic ou l’utilisation du clavier, pour rendre notre projet interactif ! C’est parti !  🚀

### Découvrez la programmation événementielle

Jusqu’à présent, notre code s’est toujours exécuté de manière ***séquentielle*** : d’abord la première instruction, puis la seconde, et ainsi de suite jusqu’à ce que toutes les instructions aient été exécutées. Dans ce chapitre, nous allons aborder une nouvelle manière d’envisager la programmation, avec la ***programmation événementielle***.

Un ***événement*** correspond à une action spécifique, comme par exemple le clic sur un bouton, ou la frappe d’un clavier. Ainsi, la programmation événementielle consiste à ***réagir à ces événements et exécuter du code au moment où ces événement se produisent***.

Pour implémenter cela, nous devons d’abord dire à JavaScript de les ***écouter grâce à un eventListener***, littéralement un “écouteur d’évènement”, en français. Puis, nous devons ***lier l’événement à un bloc de code***. C’est parti ! 🚀

### Écoutez un événement avec addEventListener

AddEventListener est une méthode fournie par JavaScript, qui peut être appelée directement depuis les éléments HTML. Cette méthode prend deux paramètres : 

- le nom de l’événement, comme click, par exemple ;
- une fonction. 

La fonction peut s’écrire de deux manières différentes que nous allons voir :

- les fonctions classiques avec le mot-clé function ;
- les fonctions fléchées. 

__Utilisez addEventListener avec le mot-clé function__

Prenons un exemple très simple pour illustrer ceci. Créons un bouton dans un fichier HTML :

```html
<button id="monBouton">Cliquez-moi !</button>
```

Dans le fichier JavaScript, nous allons récupérer ce bouton et ajouter un écouteur :

```js
    let monBouton = document.getElementById("monBouton");
    monBouton.addEventListener("click", function () {
        console.log("Vous avez cliqué sur le bouton")
    });
```

D’abord nous récupérons monBouton, jusqu’ici, pas de souci. Ensuite, nous définissons une fonction avec le mot-clé function.

Heuu…. Mais la fonction n’a pas de nom ? C’est normal… ?

Eh oui ! Cette fonction n’a pas de nom, c’est ce qu’on appelle une ***fonction anonyme***. Elle est créée au moment où nous faisons notre addEventListener.

Si nous exécutons ce code, le console.log ne s’affichera pas, car nous avons simplement ***ajouté un écouteur d’événement***. Nous avons dit à ce dernier : “Lorsque l’événement click se produit sur monBouton, alors tu vas exécuter la fonction que je te donne”. Par conséquent, tant qu’on ne clique pas sur le bouton, il ne se passe rien. En revanche, le console.log apparaîtra à l’instant où on cliquera dessus.

Ainsi, gardez bien en tête que, une fois que l’addEventListener est exécuté, la fonction passée en paramètre ne se lance pas immédiatement. Cette dernière sera lancée :

- au moment où l'événement qu’on écoute (ici, un click sur monBouton) se produit ;
- autant de fois que l’événement se produit (si on clique dix fois, nous verrons dix fois le message).

__Utilisez addEventListener avec une fonction fléchée__

Dans l’exemple précédent, pour créer une fonction nous avons utilisé le mot-clé ***function***. Cependant, pour corriger certains soucis notamment liés à la manipulation des objets et à la performance, JavaScript a introduit une autre notation : ***les fonctions fléchées***.

> Voyons un exemple d’addEventListener où le second argument, qui est la fonction qui sera exécutée lorsque l’événement se produit, est écrit avec une fonction fléchée :

```js
monBouton.addEventListener("click", () => {
    console.log("Vous avez cliqué sur le bouton")
});
```

Dans le code ci-dessus :

- le mot function est remplacé par des parenthèses vides ; 
- une flèche apparaît entre les parenthèses et les accolades (d’où le nom de fonction fléchée !)

En dépit de ces modifications, le fonctionnement reste le même. La fonction fléchée sera appelée à chaque fois que l’utilisateur va cliquer sur monBouton.

Les deux notations, fonction fléchée et function, sont très utilisées. Cependant, pour la suite du cours, je vais privilégier la notation avec les fonctions fléchées. 

[Récapitulons en vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8206297-interagissez-avec-un-element-d-une-page-web-grace-aux-evenements#/id/video_Player_2)

### Pour aller plus loin : récupérez les informations sur un événement avec la variable “event”

Il arrive régulièrement que l’on souhaite avoir des informations sur l’événement qui vient de se dérouler. Par exemple :

- Sur quel élément l’utilisateur a-t-il cliqué ?
- Quelles étaient les coordonnées de la souris ?
- Sur quelle touche du clavier l’utilisateur a-t-il appuyé ?

> Un exemple classique est la gestion du clavier. Lorsque l’on appuie sur une touche, l’événement appelé keypress se déclenche. Nous pourrions d’ailleurs l’utiliser dans notre application, par exemple, pour valider un mot lorsque l’on appuie sur la touche Entrée.

Nous pouvons écouter cet événement grâce à addEventListener, mais comment savoir quelle touche a été pressée ?

```js
document.addEventListener('keypress', (event) => {
    console.log(event.key);
});
```

Entre les parenthèses est apparue une nouvelle variable appelée event. Cette variable est fournie directement par JavaScript. C’est un objet qui contient toutes les informations liées à l’événement. Ici, ce code affiche dans la console toutes les touches sur lesquelles nous pressons.

N’hésitez pas à faire un console.log de event pour explorer un peu cette variable. JavaScript propose beaucoup d’informations pour parer à toutes les situations. Certaines d’entre elles sont particulièrement intéressantes : 

- event.target : renvoie l’élément HTML qui a déclenché l’événement ;
- event.key : la touche appuyée quand l’événement écouté est lié au clavier ;
- event.clientX et event.clientY : les coordonnées de la souris quand l’événement écouté est lié à la souris.

[revoir cette opération dans la vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8206297-interagissez-avec-un-element-d-une-page-web-grace-aux-evenements#/id/video_Player_3)

[À vous de jouer !](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8206297-interagissez-avec-un-element-d-une-page-web-grace-aux-evenements#/id/r-8206282)

### Résumé

La programmation événementielle consiste à écrire du code qui réagit à des événements.

Un événement est un signal envoyé par l’élément HTML lorsque l’utilisateur effectue une action (clic, frappe au clavier…).

Pour savoir quand un événement est envoyé, vous devez attacher un écouteur à l’élément HTML.

Pour gérer un événement, vous devez l’écouter en utilisant la méthode AddEventListener.

Vous pouvez récupérer des informations sur un événement en utilisant la variable event.

---

