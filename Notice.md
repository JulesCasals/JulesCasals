# Notice d'utilisation

---
## Sommaire
  
### Installation de la virtual box

#### Installer la virtual box

* créer la virtualbox
* télécharger l'iso debian et l'installer

#### configuration sans interface graphique

* définition de root
* configuration du premier utilisateur
* partitionner les disques
* configurer l'outil de genstions des paquets
* configuration du proxy
* sélection des logiciels
* installer le progrmme de démarrage GRUB sur un disque dur

#### Ajout interface graphique

* ajout d'une interface graphique
---
### Installation de la virtual box

<a name="virtualbox">

#### Installer la virtual box

##### Créer la virtual box

* une fois sur l'application virtual box cliquer sur nouvelle
Choisir son nom, son type (linux) et sa version (debian 64bit)y allouer un espace mémoire vive (aux choix)
* Cliquez sur "créer un disque dur virtuel maintenant" et y allouer une taille

##### Télécharger l'iso de debian et l'installer

* Aller sur le site de debian et télécharger la dernière version de celle ci
* Aller dans la "configuration" de sa virtual box puis aller dans "stockage"
* Changer le controleur ide en le fichier debian.iso que l'on vient de télécharger

#### Installation sans interface graphique 

##### définition du root

* Après avoir donné le nom de votre machine
* choisir le mot de passe du superutilisateur root

##### définition du premier utilisateur

* choisir le nom de l'utilisateur et son mot de passe

##### partitionner les disques

* choisir "utiliser un disque entier"
* faire entrée
* choisir "tout dans une seule partition"
* choisir "terminer le partionnement et appliquer les changements
* choisir "oui"

##### configurer l'outil de gestion des paquets

* choisir "non"
* choisir la langue de son choix
* choisir "deb.debian.org"

##### configurer le proxy

* écrire "http://"utilisateur"":motdepasse"@"hôte":port"

##### sélection des logiciels

* choisir uniquement "utilitaires usuels du système"

##### installer le progrmme de démarrage GRUB sur un disque dur

* choisir "oui"
* choisir "/dev/sda"

</a>

