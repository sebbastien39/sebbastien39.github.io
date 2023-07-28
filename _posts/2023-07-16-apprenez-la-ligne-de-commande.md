---
layout: post
title:  "Ligne de commande"
date:   2023-07-16 19:38:11 +0200
categories: terminal
---


Un terminal est une application permettant de dialoguer avec son ordinateur via l’écriture de lignes de commande.
Il sert à naviguer dans une arborescence de fichiers, créer, supprimer et déplacer des dossiers et des fichiers et lancer des programmes.

`pwd` Print Working Directory - répertoire courant (de travail).

    instruction : `pwd`	paramètre (argument) : `–help`

## Naviguez dans le système

`cd` Change Directory  
`ls` list
`d` directory - fichier  

`Ctrl + r` Recherche dans l’historique des commandes.  
Flèche haut ou bas pour naviguer dans l’historique.

`Ctrl + a` ou `e` Aller au tout début ou fin de la ligne que l’on tape.

`ls .`	répertoire courant  
`ls ..`	répertoire parent

`mkdir` (make directory)	`mkdir “fichier avec espace”`	`mkdir fichier\ espace`  
`touch` (créer fichier)	`touch avecRepertoire/fichier.txt`

`mv` (moove)	ex : mv bonjour.txt text	déplace boujours.txt ds le fichier test
ex : mv boujours.txt salut.txt	renomme boujours.txt en salut.txt

`cp` (copy) source destination
cp fichier1.txt fichier1copie.txt	cp -r (recursive) repertoire repertoire2

`rm` (remove) ex : rm boujours.txt	supprime boujours.txt		rm -r répertoire

Wildcards (jockers)  : caractère qui remplace une partie du nom d’un fichier.
- `*`	n’importe quelle chaîne de caractère.
 
`man` pour afficher le manuel; man pwd;	man man

cat/less/more (ancienne version de less) pour afficher un contenu;

La redirection `>` pour envoyer le résultat (sortie) d’une commande à l’intérieur d’un fichier; Ex : ls -l > list.txt

***redirection*** : prends la sortie d’une commande et la redirige vers autre chose.

***grep*** pour faire des recherches d’élément à l’intérieur de fichier sans les ouvrirs.
- grep ceQuOnCherche fichierOuRechercher
- grep chaîneCaractèreAchercher *	//ds tout les répertoires
