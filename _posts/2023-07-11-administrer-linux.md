---
layout: post
title:  "Administrez un système Linux"
date:   2023-07-09 18:13:13 +0200
categories: linux
---

## Découvrez les terminaux Linux

Dans les années 70, les ordinateurs sont tellement grands qu'ils occupent une salle entière. Les opérateurs de ces ordi sont dans le coin de cette salle ou même dans une autre salle. Pour intéragir avec ces machines on utilise un petit équipement physique qui resseble à une machine à écrire ou un minitel, équipé d'un clavier et d'un écran, il était appelé "Terminal" car il était à l'extrémité de ces systèmes.

Avec le temps, les ordinateurs ont évoluer et les "Terminaux" aussi. Aujourd'hui, il n'est plus n'écessaire que le terminal soit un équipement à part entière, un ***logiciel*** suffit. On parle alors d'***Émulateur de Terminal*** ou ***Terminal Virtuel***.


***Émulateur de Terminal*** ou ***Terminal Virtuel*** : Programme qui reproduit le comportement des anciens boitiers physiques.

2 gros avantages :
- La possibilité de ce connécter à distance.
- La possibilité de lancer plusieurs "Émulateur de Terminal" en simultanés.

Console = Terminal  //Uniquement en mode texte et  occupe tous l'espace écran disponnible.

Linux propose 7 Terminaux dit "physiques", ils sont accessibles uniquement quand on est en face du serveur et pas à distance. Il sont gérer par sa console via les combinaisons de touches `Ctrl+Alt+F1 à F7`.

Sur serveur Linux :

- Si on est physiquement face au serveur avec un clavier et un écran, on utilise les ***7 Terminaux Physiques gérés par la console***.

- Lorsque l'on est à distance via le réseau, on utilise un ***Émulateur de Terminal***, c'est à dire, un programme qu'on lance sur notre poste de travail.
 

Bon Émulateurs pour démarrer sur Linux : [XFCE Terminal](https://docs.xfce.org/apps/terminal/start) ou [Gnome Terminal](https://help.gnome.org/users/gnome-terminal/stable/).  
Putty sur windows.


### Déf

Émulateur de Terminal : gère la connexion au serveur distant avec un protocole réseau (telnet, rlogin ou SSH). 

- Le protocole VNC (Virtual Network Computing) permet notamment de prendre la main à distance sur un ordinateur. C’est un protocole de terminal virtuel graphique.

- Le protocole RDP (Remote Desktop Protocol) qui permet de se connecter sur des serveurs Windows Terminal Serveur en est un également.




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

