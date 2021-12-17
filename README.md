#markdown

title: Installation d'un poste pour le développement

## Aperçu des livrables

- Dossier d'étude et de choix des solutions, 13 points. Cette partie sera aussi évaluée à l'oral.
- Notice d'installation et d'utilisation, 3 points. Cette partie sera aussi évaluée à l'oral.
- Présentation orale en anglais, 2 points. Il s'agit d'anglais technique. 
- Schéma de l'architecture logicielle, 2 points.

# Sujet détaillé

## Installation du système de base

L'OS que j'ai choisi est Debian car c'était un des seuls que je connaissais et que j'appréciais bien car cet un logiciel libre. Un système d'exploitation stable, sûr puisqu'il fournit une configuration par défaut correcte pour chaque paquet ainsi que des mises à jour de sécurité régulières pour toute la durée de vie des paquets.

Installation et Essai sur mon système de logiciels répondant à des besoins

| Besoin                                                                             | Nombre d'outils différents demandés | 	     Logiciels proposés 	|
| ---------------------------------------------------------------------------------- |-------------------------------------|------------------------------------|
| Avoir des Gestionnaires de bureau/fenêtre (dont un qui vous plaise)                | 4                                   | Xfce4, GNOME, i3, LXDE             |
| Avoir deux utilisateurs: vous et "stagiaire"                                       |                                     | jules, stagiaire                   |
| Compiler un programme C                                                            | 2                                   | GNU Compiler Collection(GCC), LLVM |
| Regarder les pages de man de la libC                                               | 2                                   |    man,                 		|
| Lancer un `make`                                                                   |                                     |                   		        |
| Éditer du code source                                                              | 4                                   |VisualCode Studio,Geany                 |
| Déboguer du code                                                                   | 2                                   |            ( gdb, dbb  )             |
| Naviguer sur le Web                                                                | 2                                   |  Chromium, Firefox, Konqueror      |
| Naviguer sur le Web avec la version de firefox dans backports                      | 1                                   |                    		|
| Éditer une image matricielle (png...)                                              | 2                                   |           ( GIMP, Krita )           	|
| Éditer une image vectorielle (svg)                                                 | 1                                   |            (  Inkscape  )   		|
| (Dé)Compresser les formats `targz` et `7z` et `rar`                                | 1                                   |                    		|


# Commande utilisée pour chacun des outils

## Gestionnaires de bureau/fenêtre:

Installation de l'environnement de bureau Xfce4 : sudo apt-get install xfce4
Puis lors du premier démarrage: startxfce4

Installation du méta-paquet de l'environnement de bureau GNOME: sudo apt-get install task-gnome-desktop$
GNOME est celui que je préfère, il est celui que j'utilise en permanence. Mais je trouve que son environnement est intuitif et séduisant par rapport aux autres environnement de bureau comme xfce ou Lxde

Installation de l'environnement de bureau LXDE: sudo apt-get install lxde
J'ai effectué cette commande pour avoir l'ensemble complet et non pas le minimum des composants. Pour cela il suffit de rajouter (après lxde)-core à la commande

Installation du gestionnaire de fenêtre i3: sudo apt install i3
Mon choix s'est porté sur i3 car au début de la SAE c'était le seul que je connaissais. De plus, il est facilement personnalisable et permet de pratiquer la saisie de commandes pour s'améliorer

## Deux utilisateurs: vous et "stagiaire":

Ajouter un utilisateur "stagiaire": sudo adduser stagiaire

## Compiler un programme C:

.GNU Compiler Collection(GCC): sudo apt install gcc
.LLVM: sudo apt install llvm


## Regarder les pages de man de la libC:


## Lancer un 'make':

Voici mon Makefile

CC = gcc
CFLAGS = -Wall -fPIC

all : testExo

testExo : testExo.o exo.o
	$(CC) -o testExo testExo.o exo.o
	
testExo.o : testExo.c exo.h
	$(CC) -c $(CFLAGS) testExo.c
	
exo.o : exo.c exo.h
	$(CC) -c $(CFLAGS) exo.c
	
clean :
	rm -f testExo *.o

## Éditer du code source:

Geany: apt-get update && apt-get install geany


## Déboguer du code:


*Naviguer sur le Web avec la version de firefox dans backports
*Éditer une image matricielle (png...)
*Éditer une image vectorielle (svg) 
*(Dé)Compresser les formats `targz` et `7z` et `rar`





### Gestionnaire de paquets

* Pour Installer un logiciel


* Pour Désinstaller un logiciel.


* Pour Faire une recherche sur les paquets disponibles.


* Pour Lister les fichiers installés par un paquet.


* Pour Rechercher quel paquet contient un fichier donné.


* Pour Idem si le paquet n'est pas installé.


### Réseau

* Pouvoir se connecter sur une autre machine avec `ssh`.


* Permettre à une autre machine de se connecter sur la vôtre.


* Installer un serveur web capable de lire vos pages perso (`userdir`).

### Sauvegardes

* Faire une archive d'un répertoire (et de ses sous répertoires).


* Copier l'archive sur une clé USB.


* Copier l'archive via `scp` (vous pouvez vous entraîner sur `localhost`).



### Services (voir `systemd` ou autre selon OS)

* Savoir démarrer/stopper un service.


* Savoir en vérifier l'état.


* Savoir afficher les messages d'erreur.


### Divers

* Comment faire pour que le *stagiaire* n'ait pas accès aux données de votre compte ?


### Bonus

* Écrire un service utilisateur qui se lance dès la connexion de l'utilisateur.
* Écrire un service qui se lance périodiquement.
* Installer un logiciel propriétaire en restreignant ses droits d'accès à votre environnement.


# Détail des livrables

L'ensemble des documents seront écrits en `markdown`, rendus en `markdown` **et** en PDF (voir `pandoc` par exemple). Les schémas seront en [vectoriel](https://fr.wikipedia.org/wiki/Image_vectorielle).

## Dossier d'étude et de choix des solutions

Rédigez un dossier synthétique de trois pages maximum. 

Ce dossier reprend le tableau des besoins (voir plus haut) complété en indiquant par besoin les logiciels que vous proposez. 
Vous trierez la liste des logiciels proposés suivant vos préférences.


## Notice d'utilisation

La notice d'utilisation est ici à destination d'un utilisateur souhaitant reproduire à l'identique le système que vous avez créé.

Nous attendons à trouver dans votre notice d'utilisation l'application des compétences acquises en cours/TP de PPP sur la constitution et la réalisation d'un manuel utilisateur, ici "un guide d'installation".

Elle reprend les choix principaux que vous avez faits pendant l'installation. 

## Présentation orale

Lors de cette présentation orale de sept minutes (éventuellement échelonnée au cours des TP) vous présenterez à votre enseignant vos productions de la SAÉ (dossier d'étude et de choix des solutions, notice d'utilisation, schéma de l'architecture logicielle).

Votre enseignant évaluera le fond, la forme et votre capacité à répondre aux questions qu'il vous posera.

Cette présentation orale sera également l'occasion d'évaluer votre capacité à traduire à la volée en français, un texte technique en anglais (extrait d'une page de manuel, messages d'erreurs, ...), en rapport à vos cours/TP d'anglais sur la constitution d'un lexique. 

## Schéma d'architecture logicielle

Faites un schéma (donc en [vectoriel](https://fr.wikipedia.org/wiki/Image_vectorielle)) donnant les informations suivantes :
  
* Comment s'appelle l'élément logiciel qui gère votre carte réseau (comme un driver) ?
* Comment s'appelle l'élément logiciel qui gère votre carte graphique (comme un driver) ?
* Quel est le chemin du périphérique (*device*) qui représente votre carte graphique ?
* Quel est le nom du *serveur graphique* que vous utilisez ?
* Avec quel élément de votre schéma le gestionnaire de bureaux/fenêtres que vous utilisez communiquent ?







sublimetext: wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg
