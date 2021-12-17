# Notice d'utilisation

---
## Sommaire
  
### Installation de la virtual box

#### Installer la virtual box

* créer la virtualbox
* télécherger l'iso debian et l'installer

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

### Installation de zsh et configuration via oh my zsh

* Instalation de zsh
* Définition de zsh en tant que shell principal
* Installation de oh my zsh
* Configuration du thème oh my zsh
* Configuration des plugins oh my zsh
* Alias pratique

### configuration de vim afin d'en faire un espace pour coder

* création du .vimrc
* option de base
* installation d'un manager de plugin
* installer un plugin
* mes plugins
* option des plugins
* paremétrage de touche supplémentaire

<a name="instal_deb">

---
### Installation de la virtual box

<a name="virtualbox">

#### Installer la virtual box

##### Créer la virtual box

* une fois sur l'application virtual box cliquer sur nouvelle
* choisir son nom, son type (linux) et sa version (debian 64bit)
* y allouer un espace mémoire vive (aux choix)
* cliquez sur "créer un disque dur virtuel maintenant" et y allouer une taille

##### Télécharger l'iso de debian et l'installer

* Aller sur le site de debian et télécharger la dernière version de celle ci
* Aller dans la "configuration" de sa virtual box puis aller dans "stockage"
* changer le controleur ide en le fichier debian.iso que l'on vient de télécharger

</a>

<a name="sans_interface">

#### Installation sans interface graphique 

##### définition du root

* après avoit donner le nom de votre machine
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

<a name="avec_interface">

#### installation avec interface graphique

##### ajouter une interface graphique

* installer une interface graphique : `àpt install "nom de l'interface`
* relancer la machine pour avoir l'interface choisi 

</a>


<a name="instalzsh_deb">

---
### Installation de zsh et configuration via oh my zsh

#### Intallation de zsh

* installer le paquet zsh : `sudo apt install zsh`

#### Définition de zsh en tant que shell principal

* `sudo chsh -s $(which zsh)`
* `which zsh` donne le chemin vers le fichier zsh (souvent /usr/bin/zsh)

#### Installation de oh my zsh

* `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)`

#### Configuration du thème oh my zsh

* lister les différents thèmes préinstaller : `ls ~/.oh-my-zsh/themes`
* aller sur son fichier zshrc : `vim ~/.zshrc`
* chercher la ligne correspondant au thème : ZSH_THEME="xiong-chiamiov-plus"
* changer le thème de base par celui qu l'on préfère
* reset zsh en faisant : `source ~/.zshrc`
* Mon thème : "xiong-chiamiov-plus"

#### Configuration des plugins oh my zsh

* chercher les plugins sur internet avec leurs lien github
* ajouter les plugins a votre liste de plugins en faisant la commande `git clone "lien du github" ~/.oh-my-zsh/plugins
* aller sur son fichier zshrc : `vim ~/.zshrc`
* chercher la ligne des plugins : plugins=(git)
* ajouter ses plugins en les écrivants les uns à la suite des autres : plugins=(git zsh-syntax-highlighting web-search)
* reset zsh en faisant : `source ~/.zshrc`
* Mes plugins : zsh-syntax-highlighting (affiche les commandes bien écrites en vertes et mal écrite en rouge), web-search (permet de faire des recherches sur le moteur de recherche que l'on désire depuis le terminal, par exemple : ecosia wikipedia)

#### alias ptatique :

* c=`vim ~/.zshrc` (ouvre le fichier zshrc)\
* cv=`vim ~/.vimrc` (ouvre le fichier vimrc)\
* reset=`source ~/.zshrc` (relance le fichier zshrc pour appliquer les changements)
* make=`clear && make all` (clear le terminal avant d'afficher les erreurs à la compilation pour faciliter la lecture)
                      
</a>

<a name="instalvim_deb">

---
### Changement de la config vim

#### création du .vimrc

* dans son home faire `touch .vimrc`

#### option de base

écrire dans le fichier vimrc
* set nu (affiche le numéros de la ligne à la gauche de celle ci pour faciliter les déplacements dans les fichiers)
* syntax on (affiche des couleurs spéciale en fonction de ce que l'on fait par exemple des couleurs spéciales lorsque l'on code en C)
* set cindet (fait des autotabs lorsque l'on code en C)

#### installation d'un manager de plugin

on utilise un manager de plugin afin de pouvoir les installer plus facilement
* `$ curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim`

#### plugin principaux pour coder

* une fois le manager de plugin installer écrire dans son vimrc : call plug#begin()
* chercher les plugins que l'on veut installer et chercher leurs lien github
* ajouter le plugin en écrivant : Plug 'lien github du plugin'
* après avoir ajouter ses plugins écrire après : call plug#end()
* sauvegarder le fichier en faisant `:w` (dans vim)
* relancer le fichier vimrc en tapant la commande : `source %` (dans vim)
* intaller les plugins en faisant : `PlugInstall` (dans vim)
* relancer vim et les plugins seront intaller et utilisables

#### Mes plugins 

* nerdtree : permet d'afficher son arborescence de fichier dans vim et de les traversé afin d'ouvrir les fichiers que l'on veut directement dans vim
* auto-pairs : fait de l'autocomplétion pour les () {} "" et autre (quand on écrit l'ouvrant, il écrit le fermant)
* vim-raimbow : colore les () et {} afin de rendre la lecture plus claire
* vim-lightline : permet de voir plus facilement dans quel mode on est (insertion, normal, remplacement)
* supertab : permet de faire de l'autocomplétion en utilisant tab
* gruvbox : permet de changer le thème de couleur

#### option des plugins

* option pour lightline : `set laststatus=2` ( pour ouvrir automatiquement lightline), `set noshowmode` (pour enlever le mode de base qui affiche dans quel mode on est)
* option pour gruvbox : `let g:colors-name='gruvbox` laisse les couleurs de gruvbox

#### paramétrage de touche suplémentaire
* `nnoremap  \<C-h\> :NERDTreeToggle<CR>` : lorsque l'on fait controle h, ouvre nerdtree
* `nnoremap m :tabnew<CR>` : lorsque l'on appuit sur m, ouvre un nouvel anglais de vim
* `nnoremap <C-p> :tabn<CR>` : lorsque l'on appuit sur controle p, permet d'aller a l'onglet suivant
* `nnoremap <C-o> :tabp<CR>` : lorque l'on clique sur controle o, permet d'aller a l'onglet précédant

</a>
