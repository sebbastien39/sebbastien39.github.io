---
layout: post
title:  "Install xampp ubuntu"
date:   2023-07-09 18:14:13 +0200
categories: terminal
---

## Install

### Télécharger .deb sur site xampp

`xampp-linux-x64-8.2.4-0-installer.run`

### Donner droit d'exécution

```console
moi@monPC:~$ sudo chmod +x xampp-linux-x64-8.2.4-0-installer.run
```

### Renommer `manager-linux-64.run`
par `xmanager.run` (plus facile de s’en souvenir).

### Créer un nouveau projet ds htdocs

```console
moi@monPC:~$ mkdir /opt/lampp/htdocs/nomDuProjet
```

### <mark>Important, Donner les droits à votre utilisateur</mark>

Changer propriétaire par moiUser (clic droit sur fichier) ou `chown moiUser nomDuProjet`

### Créer un raccourcis vers répertoire du projet

```console
moi@monPC:~$ ln -s /opt/lampp/htdocs/nomDuProjet /home/moiUser/nomRaccourcisProjet
```

## Démarrer xampp

```console
moi@monPC:~$ sudo /opt/lampp/xmanager.run
```

---

## php-cli

PHP fournit un serveur web interne qui utilise PHP en ligne de commande pr provoquer l’exécution du script et le rendu de la page.

Ex : Création de index.php avec code suivant : 
```
<?php
echo "Hello world";
```

Exécute index.php en ligne de commande (à partir du dossier le contenant).

localhost = nom de domaine locale  
8080 = port http quelconque.

`php -S localhost:8080`

[Retour de l’exécution du script sur http://localhost:8080/index.php](http://localhost:8080/index.php)

## +

FTP passwd for daemon : xampp  
[localhost](http://localhost)
