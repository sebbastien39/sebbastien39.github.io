---
layout: post
title:  "Install xampp ubuntu"
date:   2023-07-09
categories: server, install, ubuntu
---

FTP passwd for daemon : xampp	localhost

# Install 
Télécharger .deb sur site xampp	`xampp-linux-x64-8.2.4-0-installer.run`

Donner droit d'exécution `sudo chmod +x xampp-linux-x64-8.2.4-0-installer.run`  
Renommer `manager-linux-64.run` par `xmanager.run` (plus facile de s’en souvenir).



Créer un nouveau projet ds htdocs : 
`mkdir /opt/lampp/htdocs/nomDuProjet`



<mark>/!\ Important, Donner les droits à votre utilisateur :</mark> 
Changer propriétaire par moiUser (clic droit sur fichier) ou `chown moiUser nomDuProjet`



Créer un raccourcis vers répertoire du projet : 
`ln -s /opt/lampp/htdocs/nomDuProjet /home/moiUser/nomRaccourcisProjet`



Démarrer xampp : 
`sudo /opt/lampp/xmanager.run`
http://localhost
