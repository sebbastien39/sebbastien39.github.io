---
layout: post
title:  "Javascript resumé"
date:   2023-08-02 14:57:23 +0200
categories: Javascript
---

## Déclarez une variable

Vous pouvez identifier une valeur en lui attribuant un nom grâce à une variable.

Pour déclarer une variable en JavaScript, vous devez utiliser les instructions : 
- let si la valeur de la variable évolue dans le code ;
- const si la valeur de la variable est constante.

Utilisez l’instruction console.log(nomDeMaVariable) pour vérifier le contenu d’une variable.

Le mot-clé var ne doit plus être utilisé. Vous pourrez néanmoins le retrouver dans des codes plus 
anciens.

Veillez à bien nommer vos variables : indiquez leur contenu de manière explicite pour rendre votre code lisible pour tout le monde.

## Modifiez une variable

Vous connaissez les types de données : string, number, boolean.

Vous pouvez modifier une variable en utilisant des opérateurs qui seront différents en fonction du type de données que vous manipulez.

Vous obtiendrez alors des résultats différents, comme une opération mathématique entre deux chiffres, ou une concaténation entre deux chaînes de caractères.

## Structurez des données grâce aux objets
Un objet en JavaScript peut posséder plusieurs propriétés qui auront pour chacune d’elles une valeur.

Pour déclarer un objet en JavaScript, vous devez utiliser les accolades  { }  .

Pour ajouter ou récupérer une propriété, vous devez utiliser le point  .  .

## Regroupez des données grâce aux tableaux

Un tableau est un conteneur qui permet de regrouper plusieurs valeurs ou variables.

Un tableau possède une propriété length qui permet de connaître le nombre de données contenues dans un tableau.

Une méthode s’utilise avec des parenthèses  ( )  , et permet d’interagir avec le contenu du tableau. Il existe de nombreuses méthodes différentes mises à disposition par le langage.

Lorsqu’on copie une variable simple, JavaScript réalise une copie par valeur (la valeur est dupliquée).

Lorsqu’on copie une variable complexe, JavaScript réalise une copie par référence (les deux variables pointent sur la même valeur).

## Appréhendez la logique de programmation

Un fichier JavaScript répond à une logique de programmation qui a pour but de résoudre un problème donné.

Pour construire cette logique de programmation, vous devrez :
- concevoir un algorithme qui définit les étapes permettant de résoudre un problème donné ;
- transposer cet algorithme en code organisé avec des structures conditionnelles et/ou des fonctions intégrant des blocs de code. 

Pour coder, vous devez utiliser un éditeur de code comme Visual Studio Code pour créer ou importer vos fichiers JavaScript et HTML.

Pour tester votre code, affichez la console de votre navigateur grâce aux Outils de développement.

## Contrôlez du code grâce aux conditions

Une condition est un type de structure conditionnelle qui contient un test dont le résultat sera vrai ou faux.

Les conditions if / else permettent d’exécuter du code selon une réponse unique à un test.

Les conditions switch permettent d’exécuter du code si notre test peut avoir plusieurs réponses.

Vous pouvez utiliser des booléens pour les tests de vos conditions, ou des opérateurs de comparaison, en fonction de ce que vous souhaitez tester.

## Répétez du code grâce aux boucles

Une boucle est une structure conditionnelle qui permet de répéter du code plusieurs fois.

La boucle for permet de répéter du code pour un nombre défini de fois.

La boucle while permet de répéter du code jusqu’à ce qu’une condition ne soit plus remplie.

## Organisez votre code grâce aux fonctions

Une fonction est un morceau de code qui accomplit une tâche spécifique. L’utilisation de fonctions permet d’organiser son code en blocs fonctionnels.

Pour créer une fonction en JavaScript, on utilise le mot-clé function et on lui attribue un nom.

On peut appeler une fonction en utilisant son nom, suivi de parenthèses  ()  . Si la fonction comporte des paramètres, ceux-ci sont ajoutés entre les parenthèses. 

Vous pouvez définir une valeur de retour que la fonction renvoie après son exécution. Cette valeur retournée par la fonction pourra alors être utilisée dans la suite du code. 

Séparer son code en plusieurs fonctions et en plusieurs fichiers vous permet de mieux découper votre code, et donc de le rendre plus simple à comprendre.  

Une variable déclarée dans un bloc de code n’est accessible que dans ce bloc de code.

## Récupérez un élément d’une page web

Une page web est constituée de balises HTML, et repose sur une structure que l’on appelle DOM. Cette structure permet de relier les balises entre elles.

Pour récupérer un élément du DOM :
- utilisez defer dans l’inclusion de vos fichiers JS pour retarder leur prise en compte, afin que la variable document ait le temps d’être créée ; 
- partez du point d’entrée du DOM : la variable document ;
- utilisez les méthodes adaptées : getElementById, querySelector ou querySelectorAll.

## Modifiez un élément d’une page web

Utilisez des attributs pour configurer les éléments HTML d’une page web.

Modifiez la valeur des attributs : 
- en utilisant la méthode setAttribute ;
- en utilisant la syntaxe : elementHtml.nomAttribut = “nouvelle valeur d’attribut”.

Créez un nouvel élément dans une page web

Créez un nouvel élément HTML : 
- en utilisant la méthode createElement puis en liant l’élément créé à la page grâce à appendChild ;
- en utilisant la propriété innerHTML pour insérer directement du HTML sous forme de texte à l’intérieur d’une balise.

L’interpolation permet de générer facilement des chaînes de caractères complexes en utilisant des backticks.

## Interagissez avec un élément d’une page web grâce aux événements

La programmation événementielle consiste à écrire du code qui réagit à des événements.

Un événement est un signal envoyé par l’élément HTML lorsque l’utilisateur effectue une action (clic, frappe au clavier…).

Pour savoir quand un événement est envoyé, vous devez attacher un écouteur à l’élément HTML.

Pour gérer un événement, vous devez l’écouter en utilisant la méthode AddEventListener.

Vous pouvez récupérer des informations sur un événement en utilisant la variable event.

## Récupérez la valeur d’un champ de formulaire

Utilisez les formulaires pour permettre à l'utilisateur de saisir des informations. 

Vous pouvez utiliser différent types de champs pour saisir ces informations :
- input de différents types (texte, numérique, radio, case à cocher…) ;
- textarea ;
- select.

Pour récupérer la valeur d’un champ, utilisez différentes options en fonction de votre contexte : 
- pour la plupart des champs : utilisez la propriété value ;
- pour les cases à cocher : utilisez la propriété checked ;
- pour récupérer la valeur des boutons radio, parcourez-les jusqu’à trouver celui qui est coché, puis utilisez la propriété value sur ce bouton.

## Soumettez votre formulaire

Un navigateur est un client HTTP. Il fait appel au serveur pour récupérer les informations sur la page qu’il veut afficher.

Lorsqu’un utilisateur valide un formulaire, l’événement submit est envoyé. 

Lorsqu'un événement submit est envoyé, par défaut, il provoque un appel au serveur. Cela génère un rechargement de la page qui empêche l'exécution du code.

Pour éviter ce comportement par défaut : 
- écoutez l’événement submit ;
- empêchez le comportement avec la méthode preventDefault.

## Mettez en place des règles de validation

Mettez en place des règles de validation pour vous assurer que l’utilisateur a correctement saisi ses données : 
- vérifiez la valeur d’un champ pour les cas simples ;
- définissez des expressions régulières pour les cas plus complexes.

Vous pouvez tester vos champs : 
- à l’envoi du formulaire grâce à l’événement submit ;
- à la saisie d’un champ du formulaire grâce aux événements input ou change.

Définissez vos expressions régulières étape par étape en vous aidant des sites ci-dessous : 
- regex101.com pour tester votre expression ;
- Regexper pour visualiser votre expression.

Affichez un message d’erreur
En tant que développeur, veillez à traiter toutes les erreurs qui pourraient survenir dans le code : 
- grâce à if / else pour les erreurs courantes ;
- en centralisation la gestion des erreurs grâce aux exceptions try, catch et throw pour les situations plus complexes.

Le bloc try catch fonctionne en deux parties :
- un bloc try qui essaie d’exécuter une portion de code ;
- un bloc catch qui est lancé si jamais un élément du bloc try a lancé une exception.

Vous pouvez utiliser throw new Error(message) pour lancer vous-même vos exceptions.

