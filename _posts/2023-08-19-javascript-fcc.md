---
layout: post
title: "Javascript - FCC"
date: 2023-08-19 15:08:23 +0200
categories: javascript
---

## types de variables

8 différents types de données : undefined, null, boolean, string, symbol, bigint, number, and object.

Les variables sont comme x et y en math, un nom pour représenter une donnée.

## Variable non définie

undefined variable : var a;
le résultat sera : NaN Not a Number
dans le cas string : undefined

## Problème avec var

Le problème avec var, on peut effacer des déclaration de variable : 

```js
var camper = "James";
var camper = "David"; // James sera ecrasé
```

solution : let

```js
let camper = "James";
let camper = "David"; //Il y aura une erreur ds la console
```

Avec let, une variable de même nom ne peut être déclarée qu'une seule fois.

## __const__ is read-only

Read-Only Variable : const valeur constante

## Uppercase / camelCase

const en Majuscule  
let en camelCase

## Incrémenter / Décrémenter

Incrémenter un nombre : 
i++;		équivalent à :		i = i + 1;

Décrémenter un nombre : 
i--;		équivalent à :		i = i - 1;

## Reste

Trouver un reste (remainder) avec l'opérateur % : 
Les nombres pairs ont un reste de 0, tandis que les nombres impairs ont un reste de 1.
Le reste est différent du modulo même si très similaire, il ne fonctionne pas carrectement avec nombre négatifs.

## +=

```js
myVar = myVar + 5;
```

Tout ce qui se trouve à droite du signe égal est évalué en premier.

Opérateurs qui effectuent à la fois une opération mathématique et une affectation en une seule étape.

```
Comme l'opérateur +=
myVar += 5;
pareil pour : 
Soustraction : myVar -= 5;
Multiplication : myVar *= 5;
Division : myVar /= 5;
```

## "" ou ''

Guillemet à l’intérieur d’une chaîne de caractère : \
const sampleStr = "Alan said, \"Peter is learning JavaScript\".";
Avantage guillemets simples : 
`const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';`

## Échappement dans les chaînes

[source](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/escape-sequences-in-strings)

## Concaténation

Construire une nouvelle chaîne à partir d'autres chaînes en les concaténant ensemble.

__+__

`const myStr = "This is the start. " + "This is the end.";`

__+=__

Très utile pour casser une longue chaîne sur plusieurs lignes.

```js
let ourStr = "I come first. ";
ourStr += "I come second.";
```

## Construire des chaînes avec des variables

```js
const myName = "John";
const myStr = "My name is " + myName + " and I am well!";
```

## Ajout de variables aux chaînes

```js
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;
```

## Longueur (length) d'une chaîne

```js
console.log("Alan Peter".length);
```

## Trouver le premier caractère d'une chaîne

```js
const firstName = "Charles";
const firstLetter = firstName[0];
// firstLetter = C
```

## Comprendre l'immuabilité des chaînes

Ne peuvent pas être modifiés une fois créés.

```js
let myStr = "Bob";
myStr[0] = "J";
// error car B ne peut être changer en J
```
Mais :

```js
let myStr = "Bob";
myStr = "Job";
// myStr prends la valeur Job
```

## Trouver le dernier caractère d'une chaîne

```js
const firstName = "Ada";
// Soustraire un de la longueur de la chaîne.
const lastLetter = firstName[firstName.length - 1];
// Résultat : a (3ème lettre)
```

## Word Blanks

```js
const myNoun = "dog";
const myAdjective = "big";
const myVerb = "ran";
const myAdverb = "quickly";

const wordBlanks = myAdjective + " " + myNoun + " " + myVerb + " " + myAdverb;

// Résultat : big dog ran quickly
```

## Stocker plusieurs valeurs dans une variable à l'aide de tableaux

```js
const myArray = ["soleil", 10];
```

## Imbriquer un tableau dans un autre tableau - Tableau multidimensionnel

```js
const myArray = [["Soleil", 10], ["Lune", 50]];

console.log(myArray[0][0])
// Résultat : Soleil
```

## Accéder aux données d'un tableau avec des index

```js
const array = [50, 60, 70];
console.log(array[0]); // Prints 50
const data = array[1]; // data = 60
```

## Modifier les données du tableau avec des index

```js
const ourArray = [50, 40, 30];
ourArray[0] = 15; // ourArray = [15, 40, 30]
```

## Accéder aux tableaux multidimensionnels avec des index

Premier crochet : premier niveau (tableau 1)
Crochet(s) suivant(s) : deuxième niveau (tab ou tableau 2)

```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3]; // [[10, 11, 12], 13, 14]
const nestedSubarray = arr[3][0]; // [10, 11, 12]
const element = arr[3][0][1]; // 11
```

## Manipuler des tableaux avec les méthodes

### push

Ajouter des données à la fin d'un tableau.

```js
const arr1 = [1, 2, 3];
arr1.push(4); // Résultat [1, 2, 3, 4]
```

```js
const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]); // Résultat ["Stimpson", "J", "cat", ["happy", "joy"]]
```

### pop

Supprime le dernier élément d'un tableau et renvoie cet élément.

```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();

console.log(oneDown); // 6
console.log(threeArr); // [1, 4]
```

### shift

Supprime le premier élément d'un tableau et renvoie cet élément.

```js
const ourArray = ["Stimpson", "J", ["cat"]];

const removedFromOurArray = ourArray.shift(); // Stimpson
// ourArray : ["J", ["cat"]]
```

### unshift

Ajouter des données au début d'un tableau.

```js
const myArray = [["John", 23], ["dog", 3]]

myArray.unshift(["Paul", 35]) // [ [ 'Paul', 35 ], [ 'John', 23 ], [ 'dog', 3 ] ]
```

## Écrire du JavaScript réutilisable avec des fonctions

En JavaScript, nous pouvons diviser notre code en parties réutilisables appelées fonctions.

```js
// Exemple d'une fonction
function functionName() {
  console.log("Hello World"); // Code éxecuter à chaque appel de la fonction
}

// Apeller ou invoquer la fonction
functionName();
```

### Passer des valeurs à des fonctions avec des arguments

Les paramètres sont des variables qui agissent comme des espaces réservés pour les valeurs qui doivent être saisies dans une fonction lorsqu'elle est appelée. Lorsqu'une fonction est définie, elle est généralement définie avec un ou plusieurs paramètres. Les valeurs réelles entrées (ou "transmises") dans une fonction lorsqu'elle est appelée sont appelées arguments.

Fonction avec 2 paramètres :

```js
function testFun(param1, param2) {
  console.log(param1, param2);
}
```

```js
testFun("Hello", "World"); // Résultat : Hello World
```

Nous avons appeler la fonction avec 2 arguments : `Hello` (paramètre1) et `World` (paramètre2).

Il est possible d'appeler de nouveau la fonction avec des paramètres différents.

Exemple : 

```js
function functionWithArgs(arg1, arg2){
  console.log(arg1 += arg2)
}
functionWithArgs(1, 2) // 3
functionWithArgs(7, 9) // 16
```

### Renvoyer une valeur d'une fonction avec __Return__

Nous pouvons passer des valeurs dans une fonction avec des arguments. Vous pouvez utiliser une instruction ***return*** pour renvoyer une valeur d'une fonction.

```js
function plusThree(num) {
  return num + 3;
}

const answer = plusThree(5);
// answer vaut 8
```

Exemple : 

```js
function timesFive(arg1){
  return arg1 *= 5
}

console.log(timesFive(10)) // 50
```

## Portée globale et fonctions

En JavaScript, la portée fait référence à la visibilité des variables. Les variables définies en dehors d'un bloc fonctionnel ont une portée globale. Cela signifie qu'ils peuvent être vus partout dans votre code JavaScript.

Les variables déclarées sans les mots-clés __let__ ou __const__ sont automatiquement créées dans la portée __globale__. Cela peut créer des conséquences inattendues ailleurs dans votre code ou lors de la réexécution d'une fonction. Vous devez ***toujours déclarer vos variables avec `let` ou `const`***.

## Portée locale et fonction

Les variables déclarées dans une fonction, ainsi que les paramètres de la fonction, ont une portée locale. Cela signifie qu'ils ne sont visibles que dans cette fonction.

```js
function myTest() {
  const loc = "foo"; // Variable locale "loc"
  console.log(loc);
}

myTest(); // foo
console.log(loc); // error car "loc" n'est pas défini en dehors de la fonction
```

## Portée globale VS locale dans les fonctions

Il est possible d'avoir des variables locales et globales avec le même nom. Lorsque vous faites cela, la ***variable locale a priorité sur la variable globale***.

```js
const someVar = "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}

//Return "Head"
```

## Comprendre la valeur non défini renvoyée par une fonction

Une fonction peut inclure l'instruction return mais ce n'est pas obligatoire. Dans le cas où la fonction n'a pas d'instruction de retour, lorsque vous l'appelez, la fonction traite le code interne mais la valeur renvoyée est indéfinie.

```js
let sum = 0;

function addSum(num) {
  sum = sum + num;
}

addSum(3);
```

addSum est une fonction sans instruction de retour. La fonction changera la variable globale "sum" mais la valeur renvoyée de la fonction est non défini.

## Affectation avec une valeur renvoyée

Nous pouvons prendre la valeur de retour d'une fonction et l'affecter à une variable.

```js
function sum (num1, num2){
  return (num1 + num2)
}

let ourSum = sum(5, 12) // ourSum vaut 17
```

## Stand in line - Faire la queue

En informatique, une file d'attente est une structure de données abstraite dans laquelle les éléments sont conservés dans l'ordre. De nouveaux éléments peuvent être ajoutés à l'arrière de la file d'attente et les anciens éléments sont retirés du début de la file d'attente.

## Les valeurs booléennes - __true__ __false__

Peut être soit vrai (activé) soit faux (désactivé). Ce sont des interrupteurs.

## La logique conditionnelle avec les instructions __If__

`if` est fait pour prendre des décisions dans le code. Execute le code entre accolades sous certaine conditions entre parenthèse - condition booléennes, soit vrai soit faux.

Si la condition est vrai, le programme exécute l'instruction à l'intérieur des accolades. Si faux, l'instruction ne s'exécute pas.

`if (condition is true) {
  statement is executed
}`

```js
function test (myCondition) {
  if (myCondition) {
    return "It was true";
  }
  return "It was false";
}

test(true);
test(false);

```

## Comparaison avec l'opérateur d'égalité __=__

Il existe de nombreux opérateurs de comparaison en JavaScript. Tous ces opérateurs ***renvoient une valeur booléenne vraie ou fausse***.

L'opérateur le plus basique est l'opérateur d'égalité ==. L'opérateur d'égalité compare deux valeurs et renvoie ***true si elles sont équivalentes*** ou ***false si elles ne le sont pas***. Notez que l'égalité est différente de l'affectation (=), qui affecte la valeur à droite de l'opérateur à une variable à gauche.

```js
function equalityTest(myVal) {
  if (myVal == 10) {
    return "Equal"; //return true
  }
  return "Not Equal";
}
```

Si myVal est égal à 10, l'opérateur d'égalité renvoie true, donc le code entre les accolades s'exécutera et la fonction renverra Equal. Sinon, la fonction renverra Non égal.
Pour que JavaScript puisse comparer deux types de données différents (par exemple, des nombres et des chaînes), ***il doit convertir un type en un autre***. C'est ce qu'on appelle la coercition de type.

Exemples :

>1   ==  1  // true  
1   ==  2  // false  
1   == '1' // true  
"3" ==  3  // true

## Comparaison avec l'opérateur d'égalité stricte __===__

L'opérateur d'égalité stricte n'effectue ***pas de conversion de type***.

Si les valeurs comparées ont des types différents, elles sont considérées comme inégales et l'opérateur d'égalité stricte renverra faux.

Exemples :

>3 ===  3  // true  
3 === '3' // false

## Comparaison avec l'opérateur d'inégalité __!=__

L'opérateur d'inégalité (!=) est l'opposé de l'opérateur d'égalité. Cela signifie non égal et renvoie faux là où l'égalité renverrait vrai et vice versa. Comme l'opérateur d'égalité, l'opérateur d'inégalité ***convertira les types de données*** des valeurs lors de la comparaison.

Exemples :

>1 !=  2    // true  
1 != "1"   // false  
1 != '1'   // false  
1 != true  // false  
0 != false // false

```js
function testNotEqual(val) {
  if (val != 99) {
    return "Not Equal";
  }
  return "Equal";
}

console.log(testNotEqual(10)); // Not Equal
```

## Comparaison avec l'opérateur d'inégalité stricte __!==__

L'opérateur d'inégalité stricte (!==) est l'opposé logique de l'opérateur d'égalité stricte. Cela signifie "Strictement différent" et renvoie faux là où une égalité stricte renverrait vrai et vice versa. L'opérateur d'inégalité stricte ***ne convertira pas les types de données***.

Exemples :

>3 !==  3  // false  
3 !== '3' // true  
4 !==  3  // true

```js
function testStrictNotEqual(val) {
  if (val !== 17) {
    return "Not Equal";
  }
  return "Equal";
}

console.log(testStrictNotEqual(10)); // Not Equal
```

## Comparaison avec l'opérateur Supérieur à __>__

L'opérateur supérieur à (>) compare les valeurs de deux nombres. Si le ***nombre à gauche est supérieur au nombre à droite, il renvoie vrai***. Sinon, il renvoie faux.

Comme l'opérateur d'égalité, l'opérateur supérieur à ***convertira les types de données*** des valeurs lors de la comparaison.

Exemples :

>5   >  3  // true  
7   > '3' // true  
2   >  3  // false  
'1' >  9  // false

## Comparaison avec l'opérateur supérieur ou égal à __>=__

L'opérateur supérieur ou égal à (>=) compare les valeurs de deux nombres. Si le ***nombre à gauche est supérieur ou égal au nombre à droite, il renvoie vrai***. Sinon, il renvoie faux.

Comme l'opérateur d'égalité, l'opérateur supérieur ou égal à ***convertira les types de données*** lors de la comparaison.

Exemples :

>6   >=  6  // true  
7   >= '3' // true  
2   >=  3  // false  
'7' >=  9  // false

## Comparaison avec l'opérateur Inférieur à __<__

L'opérateur inférieur à (<) compare les valeurs de deux nombres. Si le ***nombre à gauche est inférieur au nombre à droite, il renvoie vrai***. Sinon, il renvoie faux. Comme l'opérateur d'égalité, l'opérateur inférieur à ***convertit les types de données*** lors de la comparaison.

Exemples :

>2   < 5 // true  
'3' < 7 // true  
5   < 5 // false  
3   < 2 // false  
'8' < 4 // false

## Comparaison avec l'opérateur Inférieur ou égal à __<=__

L'opérateur inférieur ou égal à (<=) compare les valeurs de deux nombres. Si le ***nombre à gauche est inférieur ou égal au nombre à droite, il renvoie vrai***. Si le nombre de gauche est supérieur au nombre de droite, il renvoie faux. Comme l'opérateur d'égalité, l'opérateur inférieur ou égal à ***convertit les types de données***.

Exemples :

4   <= 5 // true  
'7' <= 7 // true  
5   <= 5 // true  
3   <= 2 // false  
'8' <= 4 // false

## Comparaisons avec l'opérateur logique et __&__

Parfois, vous devrez ***tester plus d'une chose à la fois***. L'opérateur logique et (&&) renvoie vrai si et seulement si les opérandes à gauche et à droite de celui-ci sont vrais.

Le même effet pourrait être obtenu en imbriquant une ***instruction if dans une autre if***.

```js
if (num > 5) {
  if (num < 10) {
    return "Yes";
  }
}
return "No";
```

Est équivalent à :

```js
if (num > 5 && num < 10) {
  return "Yes";
}
return "No";
```

## Comparaisons avec l'opérateur logique OU __||__

L'opérateur logique ou (||) ***renvoie vrai si l'un des opérandes est vrai***. Sinon, il renvoie faux.

Le modèle ci-dessous devrait vous sembler familier des waypoints précédents.

```js
if (num > 10) {
  return "No";
}
if (num < 5) {
  return "No";
}
return "Yes";

```

Est équivalent à : 

```js
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";

```

## instructions Else

Lorsqu'une condition pour une instruction if est vraie, le bloc de code qui la suit est exécuté. Qu'en est-il lorsque cette condition est fausse ? Normalement, rien ne se passerait. Avec une instruction else, un autre bloc de code peut être exécuté.

```js
if (num > 10) {
  return "Bigger than 10";
} else {
  return "10 or Less";
}
```

## instructions Else If

Si vous avez plusieurs conditions à traiter, vous pouvez enchaîner les instructions ***if*** avec les instructions ***else if***.

```js
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```

## Ordre logique dans les instructions __If Else__

L'ordre est important dans les instructions ***if***, ***else if***.

La fonction est ***exécutée de haut en bas***, vous devez donc faire attention à quelle instruction vient en premier.

Prenons ces deux fonctions comme exemple.

```js
function foo(x) {
  if (x < 1) {
    return "Less than one";
  } else if (x < 2) {
    return "Less than two";
  } else {
    return "Greater than or equal to two";
  }
}

foo(0) //Less than one
```

La seconde change simplement l’ordre des déclarations :

```js
function bar(x) {
  if (x < 2) {
    return "Less than two";
  } else if (x < 1) {
    return "Less than one";
  } else {
    return "Greater than or equal to two";
  }
}

bar(0) //Less than two
```
## Chaînage d'instructions If Else

Les instructions if/else peuvent être enchaînées pour une logique complexe. Voici le pseudocode de plusieurs instructions if/else if enchaînées :

```
if (condition1) {
  statement1
} else if (condition2) {
  statement2
} else if (condition3) {
  statement3
. . .
} else {
  statementN
}
```

Exemple :

|Strokes	|Return|
|1	|"Hole-in-one!"|
|<= par - 2	|"Eagle"|
|par - 1	|"Birdie"|
|par	|"Par"|
|par + 1	|"Bogey"|
|par + 2	|"Double Bogey"|
|>= par + 3	|"Go Home!"|

```js
const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
  if (strokes == 1) {
    return names[0];
  } else if (strokes <= par - 2) {
    return names[1];
  } else if (strokes === par - 1) {
    return names[2];
  } else if (strokes === par) {
    return names[3];
  } else if (strokes === par + 1) {
    return names[4];
  } else if (strokes === par + 2) {
    return names[5];
  } else {
    return names[6];
  }
}

console.log(golfScore(5, 4)); //Birdie
```

## Sélection parmi de nombreuses options avec les instructions __Switch__

Si vous devez faire correspondre une valeur à plusieurs options, vous pouvez utiliser une instruction switch. Une instruction switch compare la valeur aux instructions case qui définissent diverses valeurs possibles. Toutes les instructions JavaScript valides peuvent être exécutées à l'intérieur d'un bloc de cas et s'exécuteront à partir de la première valeur de cas correspondante jusqu'à ce qu'une rupture soit rencontrée.

```js
switch (fruit) {
  case "apple":
    console.log("The fruit is an apple");
    break;
  case "orange":
    console.log("The fruit is an orange");
    break;
}
```

les valeurs de `case` sont testées avec une égalité stricte (===). Le break indique à JavaScript d'arrêter l'exécution des instructions. Si le break est omis, l'instruction suivante sera exécutée.

Exemple :

```js
function caseInSwitch(val) {
  let answer = ""; // <== Important ça ! Déclarer vide !
switch (val) {
  case 1:
    answer = "alpha";
    break;
  case 2:
    answer = "beta";
    break;
  case 3:
    answer = "gamma";
    break;
  case 4:
    answer = "delta";
    break;}
  return answer;
}

console.log(caseInSwitch(4)); //delta
```

## Ajout d'une option par défaut dans les instructions Switch

Dans une instruction switch, vous ne pourrez peut-être pas spécifier toutes les valeurs possibles sous forme d'instructions case. Au lieu de cela, vous pouvez ajouter l'instruction par défaut qui sera exécutée si aucune instruction case correspondante n'est trouvée. Pensez-y comme à la dernière instruction else d'une chaîne if/else.

Une instruction par défaut devrait être le dernier cas.

```js
switch (num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  default:
    defaultStatement;
    break;
}
```

Exemple avec __default__ :

```js
function switchOfStuff(val) {
  let answer = ""
switch (val){
  case "a":
    answer = "apple"
    break
  case "b":
    answer = "bird"
    break
  case "c":
    answer = "cat"
    break
  default: // <== Default c'est comme un else
    answer = "stuff"
    break
}
  return answer
}

console.log(switchOfStuff("a")) //apple
```

## Plusieurs options identiques dans les instructions Switch

Si l'instruction break est omise dans le cas d'une instruction switch, la ou les instructions case suivantes sont exécutées jusqu'à ce qu'une rupture soit rencontrée. Si vous avez plusieurs entrées avec la même sortie, vous pouvez les représenter dans une instruction switch comme celle-ci :

```js
let result = "";
switch (val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
// Les cas 1, 2 et 3 produiront tous le même résultat.
```

Exemple :

```js
function sequentialSizes(val) {
  let answer = "";
switch (val){
  case 1:
  case 2:
  case 3:
    answer = "Low"
    break
  case 4:
  case 5:
  case 6:
   answer = "Mid"
   break
  case 7:
  case 8:
  case 9:
    answer = "High"
}
  return answer;
}

console.log(sequentialSizes(1)); //Low
```

## Remplacement des chaînes __If Else__ avec __Switch__

Si vous avez le choix entre de nombreuses options, une instruction switch peut être plus facile à écrire que de nombreuses instructions if/else if enchaînées. Ce qui suit:

```js
if (val === 1) {
  answer = "a";
} else if (val === 2) {
  answer = "b";
} else {
  answer = "c";
}
```

Peut être remplacer par :

```js
switch (val) {
  case 1:
    answer = "a";
    break;
  case 2:
    answer = "b";
    break;
  default:
    answer = "c";
}
```

Exemple :

```js
function chainToSwitch(val) {
  let answer = "";
  if (val === "bob") {
    answer = "Marley";
  } else if (val === 42) {
    answer = "The Answer";
  } else if (val === 1) {
    answer = "There is no #1";
  } else if (val === 99) {
    answer = "Missed me by this much!";
  } else if (val === 7) {
    answer = "Ate Nine";
  }
  return answer;
}

console.log(chainToSwitch(7)); //Ate Nine
```

Peut être remplacer par :

```js
function chainToSwitch(val) {
  let answer = "";
switch(val) {
  case "bob":
    answer = "Marley"
    break
  case 42:
    answer = "The Answer"
    break
  case 1:
    answer = "There is no #1"
    break
  case 99:
    answer ="Missed me by this much!"
    break
  case 7:
    answer = "Ate Nine"
    break
  default:
   answer = "empty string"
}
  return answer;
}

console.log(chainToSwitch(42)); //The Answer
```

## Renvoi de valeurs booléennes à partir de fonctions

Tous les opérateurs de comparaison renvoient une valeur booléenne vraie ou fausse.

Parfois, les gens utilisent une instruction if/else pour faire une comparaison, comme ceci :

```js
function isEqual(a, b) {
  if (a === b) {
    return true;
  } else {
    return false;
  }
}
```
Mais il existe une meilleure façon de procéder. Puisque === renvoie vrai ou faux, nous pouvons renvoyer le résultat de la comparaison :

```js
function isEqual(a, b) {
  return a === b;
}
```

Exemple :

```js
function isLess(a, b) {
  if (a < b) {
    return true;
  } else {
    return false;
  }
}

console.log(isLess(10, 15)); // true
```

Meilleur façon : 

```js
function isLess(a, b) {
  return a < b
}

console.log(isLess(10, 15)); //true
```

## Return Early Pattern for Functions

When a return statement is reached, the execution of the current function stops and control returns to the calling location.

```js
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
```

Ce qui précède affichera la chaîne Hello dans la console et renverra la chaîne World. La chaîne byebye ne s'affichera jamais dans la console, car la fonction se termine à l'instruction return.

Exemple :

```js
function abTest(a, b) {
  if (a < 0 || b < 0) { // <== Ce qu'il fallait écrire
    return undefined
  }
  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

console.log(abTest(-2,2)); //undefined
```

Exemple :

|Count |Change	Cards|
|+1	|2, 3, 4, 5, 6|
|0	|7, 8, 9|
|-1	|10, 'J', 'Q', 'K', 'A'|

```js
let count = 0;

function cc(card) {
switch (card) {
  case 2:
  case 3:
  case 4:
  case 5:
  case 6:
    count++
  break
  case 10:
  case "J":
  case "Q":
  case "K":
  case "A":
    count--
    break
}
  let holdbet = "Hold"
   if (count > 0){
     holdbet = "Bet"
  };
  return count + " " + holdbet
}

console.log(cc(2)); cc(3); cc(7); cc('K'); cc('A'); //1 Bet
```

## objets

Les objets sont similaires aux tableaux, sauf qu'au lieu d'utiliser des index pour accéder et modifier leurs données, vous accédez aux données des objets via ce que l'on appelle des propriétés.

Les objets sont utiles pour stocker des données de manière structurée et peuvent représenter des objets du monde réel, comme un chat.

```js
const cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```

```js
const anotherObject = {
  make: "Ford",
  5: "five",
  "model": "focus"
};
```

However, if your object has any non-string properties, JavaScript will automatically typecast them as strings.

Exemple :

```js
const myDog = {
  name: "hello",
  legs: 10,
  tails: 10,
  friends: ["yes", "no"]
};

console.log(myDog) //{ name: 'hello', legs: 10, tails: 10, friends: [ 'yes', 'no' ] }
```

## Accéder aux propriétés d'un objet avec la notation par points

l existe deux manières d'accéder aux propriétés d'un objet : la notation par points (.) et la notation par crochets ([]), similaire à un tableau.

La notation par points est ce que vous utilisez lorsque vous connaissez à l'avance le nom de la propriété à laquelle vous essayez d'accéder.

Voici un exemple d'utilisation de la notation par points (.) pour lire la propriété d'un objet :

```js
const myObj = {
  prop1: "val1",
  prop2: "val2"
};

const prop1val = myObj.prop1; //val1
const prop2val = myObj.prop2; //val2
```

Exemple :

```js
const testObj = {
  "hat": "ballcap",
  "shirt": "jersey",
  "shoes": "cleats"
};

const hatValue = testObj.hat;      // <= .hat
const shirtValue = testObj.shirt;    // <= .shirt

console.log(hatValue) //ballcap
console.log(shirtValue) //jersey
```

## Accès aux propriétés d'un objet avec la notation entre crochets

La deuxième façon d'accéder aux propriétés d'un objet est la notation entre crochets ([]). Si la propriété de l'objet auquel vous essayez d'accéder comporte un espace dans son nom, vous devrez utiliser la notation entre crochets.

Cependant, vous pouvez toujours utiliser la notation entre crochets sur les propriétés d'objet sans espaces.

Voici un exemple d'utilisation de la notation entre crochets pour lire la propriété d'un objet :

```js
const myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock",
  "NoSpace": "USS Enterprise"
};

myObj["Space Name"]; //Kirk
myObj['More Space']; //Spock
myObj["NoSpace"]; //USS Enterprise
```

Nom de propriété entre guillemets (simples ou doubles).

Exemple :

```js
const testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};

const entreeValue = testObj["an entree"];   // Change this line
const drinkValue = testObj["the drink"];    // Change this line

console.log(entreeValue) //hamburger
console.log(drinkValue) //water
```

## Accéder aux propriétés d'un objet avec des variables

Une autre utilisation de la notation entre crochets sur les objets consiste à accéder à une propriété qui est stockée comme valeur d'une variable. Cela peut être très utile pour parcourir les propriétés d'un objet ou pour accéder à une table de recherche.

Voici un exemple d'utilisation d'une variable pour accéder à une propriété :

```js
const dogs = {
  Fido: "Mutt",
  Hunter: "Doberman",
  Snoopie: "Beagle"
};

const myDog = "Hunter"; //Mets la propriété "Hunter" dans une variable
const myBreed = dogs[myDog];// Équivaut à const myBreed = dogs["Hunter"]
console.log(myBreed); // Résultat : Doberman
```

Notez que nous n'utilisons pas de guillemets autour du nom de la variable lorsque nous l'utilisons pour accéder à la propriété car nous utilisons la valeur de la variable, pas le nom.

Exemple :

```js
const testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};
//Mettre la valeur 16 dans variable, utiliser la variable pour assigner le nom du joueur à la variable player.
const playerNumber = 16;  // Change this line
const player = testObj[playerNumber];   // Change this line

console.log(playerNumber) //16
console.log(player) //Montana
```

## Mise à jour des propriétés d'un objet

Après avoir créé un objet JavaScript, vous pouvez mettre à jour ses propriétés à tout moment, comme vous le feriez pour n'importe quelle autre variable. Vous pouvez utiliser la notation par points ou par crochets pour mettre à jour.

Par exemple, regardons ourDog :

```js
const ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};
```

Mettre à jour la propriété name :

`ourDog.name = "Happy Camper"`

name prends désormais la valeur "Happy Camper"

## Ajouter de nouvelles propriétés à un objet

Vous pouvez ajouter de nouvelles propriétés aux objets JavaScript existants de la même manière que vous les modifieriez.

```js
//Ajouter la propriété "bark" à l'objet "ourDog"
ourDog.bark = "bow-wow";

//ou
ourDog["bark"] = "bow-wow";

//Résultat
console.log(ourDog.bark) //bow-wow
```

Exemple : 

```js
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

myDog.bark = "woof" // <== Ajout propriété + valeur

console.log(myDog)
/*
{ name: 'Happy Coder',
  legs: 4,
  tails: 1,
  friends: [ 'freeCodeCamp Campers' ],
  bark: 'woof' }
  */
```

## Supprimer les propriétés d'un objet

Supprimer les propriétés des objets comme ceci :

`delete ourDog.bark;`

Exemple :

```js
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"],
  "bark": "woof"
};

delete myDog.tails // <== Supprimer propriété

 console.log(myDog)
 /*
 { name: 'Happy Coder',
  legs: 4,
  friends: [ 'freeCodeCamp Campers' ],
  bark: 'woof' }
```

## Utiliser des objets pour les recherches

Les objets peuvent être considérés comme un stockage clé/valeur, comme un dictionnaire. Si vous disposez de données tabulaires, vous pouvez utiliser un objet pour rechercher des valeurs plutôt qu'une instruction switch ou une chaîne if/else. Ceci est particulièrement utile lorsque vous savez que vos données d'entrée sont limitées à une certaine plage.

Voici un exemple d’objet article :

```js
const article = {
  "title": "How to create objects in JavaScript",
  "link": "https://www.freecodecamp.org/news/a-complete-guide-to-creating-objects-in-javascript-b0e2450655e8/",
  "author": "Kaashan Hussain",
  "language": "JavaScript",
  "tags": "TECHNOLOGY",
  "createdAt": "NOVEMBER 28, 2018"
};

const articleAuthor = article["author"]; //Kaashan Hussain
const articleLink = article["link"]; //https://www.freecodecamp.org/news/a-complete-guide-to-creating-objects-in-javascript-b0e2450655e8/

const value = "title"; 
const valueLookup = article[value]; //How to create objects in JavaScript
```

Exemple :

```js
function phoneticLookup(val) {
  let result = "";

  // Only change code below this line
  switch(val) {
    case "alpha":
      result = "Adams";
      break;
    case "bravo":
      result = "Boston";
      break;
    case "charlie":
      result = "Chicago";
      break;
    case "delta":
      result = "Denver";
      break;
    case "echo":
      result = "Easy";
      break;
    case "foxtrot":
      result = "Frank";
  }

  // Only change code above this line
  return result;
}

phoneticLookup("charlie");
```

Devient :

```js
function phoneticLookup(val) {
  let result = ""; // Ne pas oublier ""

  const lookup = {
    alpha: "Adams",
    bravo: "Boston",
    charlie: "Chicago",
    delta: "Denver",
    echo: "Easy",
    foxtrot: "Frank"
  }
  result = (lookup[val]) // <== Et oui ! "val" :)
  
  return result;
}

console.log(phoneticLookup("charlie")); //Chicago
```

## Test des objets pour les propriétés

Pour vérifier si une propriété sur un objet donné existe ou non, vous pouvez utiliser la méthode `.hasOwnProperty(). someObject.hasOwnProperty(someProperty)` renvoie vrai ou faux selon que la propriété est trouvée ou non sur l'objet.

```js
function checkForProperty(object, property) {
  return object.hasOwnProperty(property);
}

checkForProperty({ top: 'hat', bottom: 'pants' }, 'top'); // true
checkForProperty({ top: 'hat', bottom: 'pants' }, 'middle'); // false
```

## Manipulation d'objets complexes

Parfois, vous souhaiterez peut-être stocker des données dans une structure de données flexible. Un objet JavaScript est un moyen de gérer des données flexibles. Ils permettent des combinaisons arbitraires de chaînes, de nombres, de booléens, de tableaux, de fonctions et d'objets.

Voici un exemple de structure de données complexe :

```js
const ourMusic = [
  {
    "artist": "Daft Punk",
    "title": "Homework",
    "release_year": 1997,
    "formats": [ 
      "CD", 
      "Cassette", 
      "LP"
    ],
    "gold": true
  }
];
```

Il s'agit d'un tableau qui contient un objet à l'intérieur. L'objet contient diverses métadonnées sur un album. Il dispose également d'un tableau "formats" imbriqués (nested). Si vous souhaitez ajouter d'autres enregistrements d'album, vous pouvez le faire en ajoutant des enregistrements au tableau de niveau supérieur. Les objets contiennent des données dans une propriété qui a un format clé-valeur. Dans l'exemple ci-dessus, « artiste » : « Daft Punk » est une propriété qui a une clé d'`artist` et une valeur de `Daft Punk`.

Remarque : Vous devrez placer une virgule après chaque objet du tableau, sauf s'il s'agit du dernier objet du tableau.

## Accéder aux objets imbriqués (nested)

Les sous-propriétés des objets sont accessibles en enchaînant la notation par points ou par crochets.

Voici un objet imbriqué :

```js
const ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": { 
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};

ourStorage.cabinet["top drawer"].folder2; //secrets
ourStorage.desk.drawer; //stapler
```

## Accéder aux tableaux imbriqués (nested)

Comme nous l'avons vu dans les exemples précédents, les objets peuvent contenir à la fois des objets imbriqués et des tableaux imbriqués. Semblable à l'accès aux objets imbriqués, la notation entre crochets de tableau peut être chaînée pour accéder aux tableaux imbriqués.

Voici un exemple de comment accéder à un tableau imbriqué :

```js
const ourPets = [
  {
    animalType: "cat",
    names: [
      "Meowzer",
      "Fluffy",
      "Kit-Cat"
    ]
  },
  {
    animalType: "dog",
    names: [
      "Spot",
      "Bowser",
      "Frankie"
    ]
  }
];

ourPets[0].names[1]; //Fluffy
ourPets[1].names[0]; //Spot
```

## Exercice Collection de disques

Vous créez une fonction qui facilite la maintenance d'une collection d'albums musicaux. La collection est organisée comme un objet contenant plusieurs albums qui sont également des objets. Chaque album est représenté dans la collection avec un identifiant unique comme nom de propriété. Dans chaque objet album, il existe diverses propriétés décrivant des informations sur l'album. Tous les albums ne contiennent pas des informations complètes.

La fonction updateRecords prend 4 arguments représentés par les paramètres de fonction suivants :

- records - un objet contenant plusieurs albums individuels
- id - un numéro représentant un album spécifique dans l'objet records
- prop - une chaîne représentant le nom de la propriété de l'album à mettre à jour
- value - une chaîne contenant les informations utilisées pour mettre à jour la propriété de l'album

Complétez la fonction en utilisant les règles ci-dessous pour modifier l'objet passé à la fonction.

- Votre fonction doit toujours renvoyer l’intégralité de l’objet records.
- Si value est une chaîne vide, supprimez la propriété prop donnée de l'album.
- Si prop n'est pas une piste et que value n'est pas une chaîne vide, attribuez la valeur à l'accessoire de cet album.
- Si prop est une piste et que la valeur n'est pas une chaîne vide, vous devez mettre à jour le tableau des pistes de l'album. Tout d’abord, si l’album n’a pas de propriété tracks, attribuez-lui un tableau vide. Ajoutez ensuite la valeur comme dernier élément du tableau des pistes de l'album.

Remarque : Une copie de l'objet recordCollection est utilisée pour les tests. Vous ne devez pas modifier directement l'objet recordCollection.

```js
// Setup
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  return records;
}

updateRecords(recordCollection, 5439, 'artist', 'ABBA');
```

Solution :

