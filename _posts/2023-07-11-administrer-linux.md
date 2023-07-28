---
layout: post
title:  "Administrer Linux"
date:   2023-07-09 18:13:13 +0200
categories: linux
---

## Découvrir le terminal et le shell

shell standard de Linux `Bash`

Le shell exécuté après l’étape d’authentification est configuré dans le fichier `/etc/passwd`

Pour garantir que l'utilisateur ne pourra jamais lancer de shell à la suite du processus d'authentification lors de la connexion. Et donc, pas faire grand chose. Il faut modifier le fichier `/etc/passwd` et indiquer un interpréteur de commandes comme `/usr/bin/nologin` ou `/dev/zero` ou encore `/dev/null`.


### Lancer des commandes sous Bash

#### Utiliser le prompt et consulter ses variables

```sh
# Exemple de prompt :
moi@monPC:~$
```

Utilisateur `moi` `\u`  
Séparateur `@`  
Hostname de l'équipement `monPC` `\h`  
On se trouve dans le répertoire personnel de l'utilisateur `~` `\w`  
Utilisateur non privilégié `$` `\$`  
root `#`

Toute cette configuration est stockée dans la variable `$PS1`gérée par le shell Bash. `echo $PS1` [Commande line reference](https://ss64.com/bash/syntax-prompt.html)

Ds Terminal `export PS1="\u-\h:\s"`

Ds `.bashrc` `export PS1="\u-\h:\s";`

La variable `$SHELL` dit sur quel shell on est connecté. `echo $SHELL`


#### Lister le contenu d'un répertoire

option (modifie la Sortie) :  
`ls` long list `-l`; trier par date `t`; résultats inversés `r`; recursive, ds les répertoires `R`; human readable `h`.

argument (donnée d'Entrée pr exécuter commande):  
`ls -ltrh repertoire1`

[Utility Convention](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html)

### Les différents types de commandes Linux


Les commandes internes : Livrées avec l'interpréteur de commandes directement, comme une primitive du shell. Elles sont disponibles à tout moment par l'administrateur du système. Cependant, il est probable que toutes ne soient pas forcément intégrées à l’interpréteur de commandes que vous allez utiliser. Il est également possible que leurs options ne soient pas toutes identiques non plus.

 Les commandes externes : Externes à l'interpréteur de commandes, c'est-à-dire qu'elles ne sont pas fournies par le shell. Elles sont généralement présentes sur le système sous la forme d'un fichier compilé binaire ou d'un fichier disposant des droits d'exécution (comme un script Perl par exemple).

- `type` permet de récupérer infos sur une commande. `type echo` = `echo is a shell builtin` echo est une commande intégrée au shell.

- `file` info sur un fichier

- Pour chaîner des commandes `&&`. `cd /home && file *`

- `id` info sur compte utilisateur connecté. `type id` `file /usr/bin/id`

### Configurer l'accès aux commandes

Le shell Bash accède aux commandes externes grace à la variable `$PATH` (liste de répertoires)

`./siCommandeDsrépertoireCourant`


`/usr/local/bin`

`/usr/bin`

`/bin`

Pouvoir appeler commande de n'importe où : Ds `.bashrc` `export PATH=$PATH:/home/user/FichierDexécution`

### Consultez la documentation des commandes sous Linux 

- **Commandes internes** `help` affiche liste des commandes internes intégrées au shell.

ex : info sur une commande : `help echo`

- **Commande externe** 

ex : `id --help` ou + détaillé `man id`

### Profitez des fonctionnalités avancées de Bash 

```sh
history
```

```sh
# rappeler une commande par son numéro
!1212
```

Rechercher dans `history` : Ctrl + R "mot à rechercher" > pour remonter ds l'occurence refaire Ctrl + R > Tab

**Alias de commande** : Déclare une variable qui contient une commande "sur mesure".

Editer `.bashrc`  
`alias ll='ls -lrtha';`  
Vérifier avec `type ll`  
`alias` liste tous les alias préconfigurés




## Manipuler les fichiers

## Gérer le réseau

## Surveiller l'activité d'un système

