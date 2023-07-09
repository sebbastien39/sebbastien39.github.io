---
layout: post
title:  "Structure theme WordPress"
date:   2023-07-09
categories: WordPress
---

index.php
style.css
functions.php
header.php
footer.php
sidebar.php
front-page.php
home.php
singular.php
single.php
single-{post-type}.php
archive.php
archive-{post-type}.php
page.php
page-{slug}.php
category.php
author.php
date.php
search.php
attachment.php
image.php
404.php
comments.php
Si vous avez envie de connaître l’utilité de chaque fichier, je vous invite à aller voir la page de documentation dédiée.

Les fichiers obligatoires pour chaque thème sont :
index.php  : le template principal d’un thème. Si aucun autre template n’existe, c’est lui qui sera pris en compte ;
style.css  : la feuille de style principale d’un thème. Ce fichier contient les informations d’en-tête de votre thème, c'est-à-dire les informations principales qui définissent votre thème (nom, auteur, version, etc.) ;
functions.php  : le cœur des fonctionnalités de votre thème. Il permettra d’ajouter, modifier ou supprimer des possibilités offertes par WordPress. On travaillera principalement dans ce fichier.
Après, vous trouverez les fichiers suivants qui nous permettront de personnaliser notre thème :
header.php  :  permet de coder la partie haute d’un template, à partir de l’ouverture de la balise html  jusqu’à l’ouverture de la balise body  , et parfois un peu plus. Ce fichier est en général importé dans les différents fichiers de template ;
footer.php  : permet de coder la partie basse d’un template à partir de la balise footer jusqu’à la fermeture de la balise html  . Ce fichier est en général importé dans les différents fichiers de template.
Si vous souhaitez faire des templates avancés pour les pages d’archive, il y a certains fichiers plus spécialisés. Nous n’entrerons pas en détail sur ces fichiers dans ce cours, mais vous saurez qu’ils existent. Les fichiers les plus utiles sont :
single.php  : affiche la page d’un article ;
single-{post-type}.php  : affiche un article d’un type précis. Cette notion de post-type  est avancée ;
archive.php  : affiche la liste des articles, que ce soit selon la catégorie, l’auteur, la date, etc. Ce fichier peut être surclassé par d’autres fichiers de template plus précis. Si aucun surclassement n’existe, ce fichier est appelé en dernier lieu ;
archive-{post-type}.php  : utilisé quand on veut afficher la liste des articles d’un type précis. Cette notion de post-type  est avancée ;
category.php  : affiche la liste des articles d’une catégorie ;
taxonomy.php  : affiche la liste des articles d’une taxonomie ;
search.php: affiche les résultats d’une recherche.

Il est commun, par exemple, de regrouper les fichiers statiques (c’est-à-dire les fichiers chargés par le navigateur, comme images  ,  css  , js  ) dans un dossier assets  et dans des sous-dossiers css  , js  et img  .

Selon le développeur qui a créé le thème, sa structure peut être différente et plus ou moins complexe, car WordPress permet d’ajouter, modifier et supprimer des fonctionnalités avancées grâce au fichier functions.php  . À partir de ce fichier, on peut être amené à coder de plein de manières différentes. C’est la flexibilité du PHP qui permet cela.

Lien : child theme. Home / Theme Handbook / Theme Basics / Template Files


