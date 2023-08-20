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
var camper = "James";
var camper = "David"; // James sera ecrasé
solution : let
let camper = "James";
let camper = "David"; //Il y aura une erreur ds la console

Avec let, une variable de même nom ne peut être déclarée qu'une seule fois.

## const is read-only

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

Comme l'opérateur +=
myVar += 5;
pareil pour : 
Soustraction : myVar -= 5;
Multiplication : myVar *= 5;
Division : myVar /= 5;

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

Si vous avez plusieurs conditions à traiter, vous pouvez enchaîner les instructions if avec les instructions else if.

```js
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```

