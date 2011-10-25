##Balsa est un "framework" php minimaliste
Les _"_ sont là car Balsa est très léger et limité en lui même.

Il est défini en structure simple, ou chaque chose est à sa place pour votre projet.

Pour installer Balsa, il faut :
1. extraire le contenu de l'archive dans un répertoire accessible depuis le web 
2. se rendre sur l'url qui pointe sur le fichier `install.php` depuis le navigateur
3. remplissez le formulaire

Vous devriez être bon pour commencer ^^

> Info: Un Back office est accessible via la page `admin.php`

##A propos de la structure :

Il y a deux dossiers principaux : `www/` et `nw/`, comme leurs nom peuvent l'indiquer le dossier `www/` sera accessible depuis le web et le dossier `nw/` ne le sera pas (dans un monde parfait.)


###Le dossier `www`

Commençons par le plus simple, le dossier `www/` :
Il y a peu de fichiers dans ce dossier: 
* `index?php` 
* `goulot.php`
* `admin.php` et le dossier
* `media/`

La page `index.php` est l'entrée pour les fichiers contenus dans le dossier `nw/page/`, il inclura,s'il existe, le fichier nommé dans le paramètre _get_ 'page'
La page `goulot.php` est l'entrée pour les fichiers contenus dans le dossier `nw/ajax/`, il inclura, s'il existe, le fichier nommé dans le paramètre _get_ 'page'
`admin.php` a un rôle identique au deux fichier précèdent sauf qu'il gère les requêtes pour le back office.

Dans le dossier `media/` vous trouverez les sous dossier suivant :
+ `css/`  qui contient la version compressé par balsa des diffèrent fichiers _css_
+ `js/`   qui marche de la meme maniere que `css/`` mais avec les fichiers _javascript_
+ `img/`  qui contiendra les images
+ `font/` qui contiendra les différentes polices d'écritures

###Le dossier `nw`

Et maintenant le plat de résistance, le dossier `nw/` :
Vous trouverez ici le fichier `init.php` et les dossiers suivant :
* `admin`,
* `ajax`,
* `data`,
* `fonction`,
* `install`,
* `media`,
* `page`

Le fichier `init.php` est la première partie de logiciel, il initialise les différentes constantes utilisées
 
Le dossier `ajax/` contient tout les fichiers appelés par `goulot.php` avec le paramètre _get_ 'page'
Ajouter simplement un fichier ici et appeler le avec l'url:
`goulot.php?page=nom_du_fichier_sans_php`

Le dossier `data/` contiendra les sous dossiers relatif aux données du logiciel

Le dossier `fonction/` va contenir toutes vos bibliothèque (fonctions et classes) qui seront utiliser dans votre programme
Il contient aussi un sous dossier `lib/` ou vous placerez toutes les librairie tierce que vous utilisez
Le fichier `fonction.php` contient toutes les fonctionnalités de base, s'il vous plait ne le modifié pas :P

Le dossier `install/` contient les fichier relatif à l'installation

Le dossier `media/` contient deux sous dossier :
* `js/` qui contient les fichiers _js_ qui seront compressés
* `css/` qui contient tout les fichiers _css_ qui seront compressés

Le dossier page contient tout les fichier appeler via le paramètre get 'page' dans `index.php`

Le dossier `admin` contient tout les fichiers concernant le back office
Le fichier `auth.php` qui contient toutes les fonction pour l'authentification, c'est aussi lui qui ouvre l'accès  au reste de la partie d'administration
Le dossier `fonction/` sert à la même chose que le dossier `nw/fonction/`


C'est à peu près tout :D

###Contributions

En lui même le projet ne devrait pas évoluer trop fortement, la structure devrais rester fortement identique.
Seule la partie _admin_ est en évolution constante
