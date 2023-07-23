---
layout: post
title:  "Arborescence des fichiers Linux"
date:   2023-07-18 21:54:23 +0200
categories: linux fichier
---

Ds Linux tout est fichier, tout est gérer sous forme de fichiers.

Quel fichier contient quoi :

`/boot` noyau Linux  
`/bin` commandes  
`/etc` fichiers de configuration  
`/root` compte super utilisateur, réserver au tâches d'administration sur le système - pr des raisons de sécurité, il ne doit pas être ni identifié, ni attaché à un compte "humain".  
Il est recommander de ne pas stocker de fichier ou gérer une boite de messagerie pour root.

Le system Linux a besoin d'un compte rootbmais pas d'un repertoire root. Ne pas stocker de fichier sensible ds le repertoire root.

`/home` permet de stocker les fichiers des comptes personnels des utilisateurs. Sur un serveur web, pas besoin de /home, sur un serveur de fichier oui.

`/proc` `/sys` Vitrine virtuel, n'existe pas sur le disque dur. C'est Linux qui les maintiens en mémoire et permettent à l'administrateur de modifier le contenu des fichiers et d'intervenir à chaud sur le comportement du systeme.

