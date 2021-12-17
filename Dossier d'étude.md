# Markdown

Installation d'un poste pour le développement
---------------------------------------------

## Dossier d'étude et de choix des solutions

Rédigez un dossier synthétique de trois pages maximum. 

Ce dossier reprend le tableau des besoins (voir plus haut) complété en indiquant par besoin les logiciels que vous proposez. 
Vous trierez la liste des logiciels proposés suivant vos préférences.

# Détail des livrables

L'ensemble des documents seront écrits en `markdown`, rendus en `markdown` **et** en PDF (voir `pandoc` par exemple). Les schémas seront en [vectoriel](https://fr.wikipedia.org/wiki/Image_vectorielle).




### Installation et Essai sur mon système de logiciels répondant à des besoins

| Besoin                                                                             | Nombre d'outils différents demandés | 	     Logiciels proposés 	|
| ---------------------------------------------------------------------------------- |-------------------------------------|------------------------------------|
| Avoir des Gestionnaires de bureau/fenêtre (dont un qui vous plaise)                | 4                                   | Xfce4, GNOME, i3, LXDE             |
| Avoir deux utilisateurs: vous et "stagiaire"                                       |                                     | jules, stagiaire                   |
| Compiler un programme C                                                            | 2                                   | GNU Compiler Collection(GCC), LLVM |
| Regarder les pages de man de la libC                                               | 2                                   |    	Info, man               |
| Lancer un `make`                                                                   |                                     |                   		        |
| Éditer du code source                                                              | 4                                   |VisualCode Studio,Geany, Bluefish,            |
| Déboguer du code                                                                   | 2                                   |            gdb, valgrind           	|
| Naviguer sur le Web                                                                | 2                                   |  Chromium, Firefox, Konqueror      |
| Naviguer sur le Web avec la version de firefox dans backports                      | 1                                   |                    		|
| Éditer une image matricielle (png...)                                              | 2                                   |           GIMP, Krita          	|
| Éditer une image vectorielle (svg)                                                 | 1                                   |             Inkscape    		|
| (Dé)Compresser les formats `targz` et `7z` et `rar`                                | 1                                   |                7zip    		|


## Commande utilisée pour chacun des outils

#### Gestionnaires de bureau/fenêtre:

Installation de l'environnement de bureau Xfce4 : sudo apt-get install xfce4
Puis lors du premier démarrage: startxfce4

Installation du méta-paquet de l'environnement de bureau GNOME: sudo apt-get install task-gnome-desktop$
GNOME est celui que je préfère, il est celui que j'utilise en permanence. Mais je trouve que son environnement est intuitif et séduisant par rapport aux autres environnement de bureau comme xfce ou Lxde

Installation de l'environnement de bureau LXDE: sudo apt-get install lxde
J'ai effectué cette commande pour avoir l'ensemble complet et non pas le minimum des composants. Pour cela il suffit de rajouter (après lxde)-core à la commande

Installation du gestionnaire de fenêtre i3: sudo apt install i3
Mon choix s'est porté sur i3 car au début de la SAE c'était le seul que je connaissais. De plus, il est facilement personnalisable et permet de pratiquer la saisie de commandes pour s'améliorer

#### Deux utilisateurs: vous et "stagiaire":

Ajouter un utilisateur "stagiaire":
>`sudo adduser stagiaire`

#### Compiler un programme C:

GNU Compiler Collection(GCC):
>`sudo apt install gcc`

LLVM: 
>`sudo apt install llvm`

#### Regarder les pages de man de la libC:

Man:
>

Info:
>

#### Lancer un 'make':
Pour pouvoir lancer le paquet make il faut l'installer avec la commande:
> `sudo apt install make`

#### Éditer du code source:

Geany: 
>`apt-get update && apt-get install geany`

#### Déboguer du code:

GDB:
> `sudo apt gdb`

Valgrind:
> `sudo apt-get install valgrind --classic`

#### Naviguer sur le Web avec la version de firefox dans backports
...
#### Éditer une image matricielle (png...)

Gimp: 
>`sudo apt install gimp`

Krita:
>`sudo apt install krita`
>
#### Éditer une image vectorielle (svg)
Inkscape:
>`sudo apt install inkscape`

#### (Dé)Compresser les formats `targz` et `7z` et `rar`
Pour l'installation de 7zip que j'ai choisi car c'est celui que j'utilise le plus et celui donc que je maîtrise le mieux, il faut rentrer la commande:
>`sudo apt install p7zip`


## Gestionnaire de paquets

* Pour Installer un logiciel:
> `apt install/apt-get install`

* Pour Désinstaller un logiciel:
> `apt remove`

* Pour Faire une recherche sur les paquets disponibles.
>`dpkg -l "nom du paquet"`

* Pour Faire une mise à jour:
> `apt-update`

* Pour Lister les fichiers installés par un paquet.
> `dpkg –list paquet`

* Pour Rechercher quel paquet contient un fichier donné. 
> `dpkg –S "nom du fichier"`

* Pour Idem si le paquet n'est pas installé.
>> ``


### Réseau

#### Pouvoir se connecter sur une autre machine avec `ssh`

> 

#### Permettre à une autre machine de se connecter sur la vôtre.

>

#### Installer un serveur web capable de lire vos pages perso (`userdir`)

>

### Sauvegardes

#### Faire une archive d'un répertoire (et de ses sous répertoires).

>

#### Copier l'archive sur une clé USB.

>

#### Copier l'archive via `scp` (vous pouvez vous entraîner sur `localhost`)

> `scp (source) @iplocal (destination)`



### Services (voir `systemd` ou autre selon OS)

#### Savoir démarrer/stopper un service.
> `systemctl start/stop`

#### Savoir en vérifier l'état.
> `systemctl  status`

#### Savoir afficher les messages d'erreur.
> sudo journalctl -u "nom du service" | grep "failed"`

### Divers

#### Comment faire pour que le *stagiaire* n'ait pas accès aux données de votre compte ?

>chmod 711 ~/
