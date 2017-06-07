<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Tuto créateur de thèmes](#tuto-crateur-de-thmes)
	- [Se rendre sur l'instance](#se-rendre-sur-linstance)
	- [Se connecter avec son compte OpenStreetMap](#se-connecter-avec-son-compte-openstreetmap)
	- [Créer un nouveau thème](#crer-un-nouveau-thme)
	- [Configurer le thème](#configurer-le-thme)
		- [Se géolocaliser](#se-golocaliser)
		- [Configuration générale](#configuration-gnrale)
			- [Nom du thème, description et couleurs](#nom-du-thme-description-et-couleurs)
			- [Positionnement et géolocalisation](#positionnement-et-golocalisation)
			- [Géocodeur, Affichage des informations et Statistiques](#gocodeur-affichage-des-informations-et-statistiques)
		- [Fonds de carte](#fonds-de-carte)
	- [Créer une couche de données](#crer-une-couche-de-donnes)
		- [Cas de la requête overpass](#cas-de-la-requte-overpass)
		- [Tester sa requête](#tester-sa-requte)
			- [Le cache !](#le-cache-)
			- [Quelques bonnes pratiques](#quelques-bonnes-pratiques)
		- [Cas du fichier CSV](#cas-du-fichier-csv)
		- [Cas du fichier GeoJSON](#cas-du-fichier-geojson)
		- [Cas du fichier GPX](#cas-du-fichier-gpx)
	- [Configurer ses tags](#configurer-ses-tags)
	- [Définir les types de noeuds, "modèles"](#dfinir-les-types-de-noeuds-modles)
	- [Traduire son thème](#traduire-son-thme)

<!-- /TOC -->

# Tuto créateur de thèmes
À L'instar d'[OpenBeerMap](http://openbeermap.github.io), d'[OsmHydrant](http://osmhydrant.org/) et de [wheelmap](https://wheelmap.org), MapContrib vise à faciliter la contribution à OpenStreetMap, par la création de thèmes en fonction des TOC (Troubles Obsessionnelles Cartographiques) propres à chacun.
Ces thèmes se basent sur :
- une requête overpass (technique pour aller interroger une copie synchronisée de la base de donnée OpenStreetMap),
- la définition de "types de noeuds",

Ce tutoriel vise à accompagner la création d'un thème.
Les pré-requis pour pouvoir le faire sont :
- l'envie et/ou le besoin,
- un compte OpenStreetMap,
- connaître les tags (clé / valeur) dans l'ontologie OpenStreetMap,
- connaître une requête OverPass,

Pour ce tutoriel, l'instance utilisée est https://mapcontrib.xyz.

## Se rendre sur l'instance

Pour ce tutoriel, l'instance utilisée est https://mapcontrib.xyz.
![Page d'accueil](images/MapContrib_057.png)

## Se connecter avec son compte OpenStreetMap
- Se rendre dans la colonne de paramètres

![Page d'accueil](images/MapContrib_008.png)

- Se connecter

![Colonne](images/MapContrib_009.png)

- en utilisant son compte OpenStreetMap

![Pop-up OpenStreetMap](images/MapContrib_010.png)

- Renseigner ses identifiants OpenStreetMap

![Page de connexion OpenStreetMap](images/MapContrib_013.png)

- Accepter que MapContrib accède à votre compte OpenStreetMap

![Autoriser accès MapContrib](images/MapContrib_014.png)

## Créer un nouveau thème

- Se rendre dans la colonne de paramètres

![Page d'accueil connectée](images/MapContrib_015.png)

![Colonne connectée](images/MapContrib_016.png)

À noter :

- la possibilité de retrouver tous les thèmes que l'on a créé
- la possibilité de retrouver ses favoris (des thèmes que l'on a créé ou pas, dont on souhaite garder la trace)

![Favoris 1](images/MapContrib_059.png)

![Favoris 1](images/MapContrib_060.png)

![Favoris 1](images/MapContrib_058.png)

## Configurer le thème

Un thème porte un titre, peut s'ouvrir sur un territoire particulier et possède quelques options générales décrites ci-dessous. Toutes ses options sont modifiables par la suite.

### Se géolocaliser
![Nouveau thème](images/MapContrib_023.png)

- le raccourci clavier Ctrl+f fonctionne

![Recherche Gap](images/MapContrib_024.png)

### Configuration générale

#### Nom du thème, description et couleurs

![Configuration](images/MapContrib_017.png)

![Configuration générale](images/MapContrib_018.png)

![Colonne configuration générale - partie 1](images/MapContrib_019.png)
- Nom du thème / apparaît à la fois dans l'url et en haut du thème
  - si vous changez le titre, même une ancienne url fonctionne car le titre n'est pas pris en compte, seul le code (unique) sert à trouver le thème,
  - pas d'inquiétudes donc vous pouvez changer le nom de votre thème quand vous voulez :)
- Description / permet de décrire le sujet de votre thème. Lorsque ce champ est rempli, un i apparaît à coté du nom du thème et permet d'accéder à la description.

![Colonne configuration générale - partie 1-1](images/MapContrib_061.png)

![Colonne configuration générale - partie 1-2](images/MapContrib_062.png)

![Colonne configuration générale - partie 1-3](images/MapContrib_063.png)

#### Positionnement et géolocalisation

![Colonne configuration générale - partie 2](images/MapContrib_020.png)

- Positionnement / Enregistrer les paramètres actuels / permet de garder la géolocalisation sur Gap ainsi que le niveau de zoom. Ainsi, lorsqu'une personne arrive sur le thème elle est centrée selon des paramètres définis par le créateur du thème,
- Géolocalisation / permet de passer outre les paramètres ci-dessus et de géolocaliser automatiquement toute personne arrivant sur le thème.

#### Géocodeur, Affichage des informations et Statistiques

![Colonne configuration générale - partie 3](images/MapContrib_021.png)

- Géocodeur / permet de définir le géocodeur utilisé lors des recherche (Ctrl+F). Par défaut, Photon est utilisé pour des raisons de fluidité.
- Affichage des informations / les informations des POI peuvent être affichés dans plusieurs types de fenêtres. Par défaut en colonne à droite, il est aussi possible de changer le comportement du thème en affichant :
  - des Infobulles ![infobulle](images/MapContrib_064.png),
  - des Fenêtres modales![infobulle](images/MapContrib_065.png),

### Fonds de carte

![Fonds de carte - partie 1](images/MapContrib_055.png)

![Fonds de carte - partie 2](images/MapContrib_056.png)

- Définition des fonds de cartes pour les contributeurs. Ces derniers auront la possibilité d'en choisir d'autres mais ceux définit par le créateur du thème sont mis en avant.

## Créer une couche de données

![Création couches - Partie 1](images/MapContrib_025.png)

![Création couches - Partie 2](images/MapContrib_026.png)

![Création couches - Partie 3](images/MapContrib_027.png)

 - 4 types de données peuvent être ajoutés
 	- des données provenant directement d'OpenStreetMap à travers une requête overpass,
	- des données dans un fichier csv comportant des titres de colonnes longitude et latitude,
	- par un fichier GeoJSON,
	- par un fichier GPX,

### Nom, Description et Visibilité

![Création couches - Partie 4](images/MapContrib_028.png)

- Nom / définit le nom de cette couche, telle que cela apparaît pour les contributeurs,
- Description / permet de mieux renseigner le contenu de la couche, supporte également le markdown !
	- ![Création couches - Partie 4](images/MapContrib_067.png)
- Visibilité / va permettre au créateur de thème de préparer de nouvelles couches mais de ne pas les montrer aux contributeurs sur le thème,

### Représentation, Marqueur et Contenu des bulles

![Création couches - Partie 4](images/MapContrib_029.png)

#### Représentation

Sous forme de points groupables (par défaut) ou de carte thermique.
- ![Carte thermique](images/MapContrib_068.png)

- Options ![Carte thermique, options](images/MapContrib_069.png)

#### Marqueur
Les marqueurs de chaque couche sont personnalisables :
- au niveau de la couleur et de la forme
	- ![Couleurs et formes marqueurs](images/MapContrib_070.png)

- avec une bibliothèque d'icônes :
	- ![Bibliothèques d'icônes](images/MapContrib_071.png)

- ou un lien vers une image extérieure (assurez vous d'avoir les droits d'utilisation de l'image) :
	- ![Lien icône externe](images/MapContrib_072.png)

#### Contenu des bulles
Les données de la couche, quelque soit la source, peuvent être affichés de manière dynamique dans la "bulle" associée à chaque point.

Pour cela, il est important de définir le contenu des bulles.

Pour appeler une valeur dynamique, on utilisera la clé entre accolade : {clé} renvoie la valeur de manière dynamique.

- ![Contenu de la bulle](images/MapContrib_073.png)
- ![Résultat dynamique](images/MapContrib_074.png)

### Cas de la requête overpass
#### Zoom minimum, Requête OverPass et Cache
![Couche overpass - Partie 1](images/MapContrib_075.png)

- Zoom minimum / définit la valeur à laquelle la requête overpass se déclenche,
- Requête OverPass / Zone pour l'exécution de la requête
	- le temps de requête maximum (timeout) est limité à 120 secondes,
	- la taille maximale de données rapatriés est limitée à 1 Mo !
- Le cache !
	- activer le cache présente des avantages et des inconvénients
		- les données se chargent plus rapidement (la requête overpass n'est pas exécuté, les données sont téléchargées depuis leur stockage en cache sur nos serveurs) mais se mettent à jour moins régulièrement (la requête est relancée une fois par jour pour mise à jour),
		- sur un thème dont le cache est activé, une étoile jaune signale l'ajout d'une donnée depuis ce thème (et seulement depuis ce thème),


### Tester sa requête
Selon le zoom minimum défini, la requête peut ne pas se déclencher à l'ouverture du thème. Il faudra alors zoomer pour permettre le déclenchement.

![Tester sa requête overpass - Partie 1](images/MapContrib_051.png)

![Tester sa requête overpass - Partie 1](images/MapContrib_052.png)

![Tester sa requête overpass - Partie 1](images/MapContrib_053.png)




#### Quelques bonnes pratiques

- pas trop de requètes
- TIPS : durée max et taille de fichier max !


### Cas des autres formats de fichiers pour les couches
Nom, Description, Visibilité, Représentation (groupable ou thermique), Marqueur et Contenu des bulles fonctionnent de la même manière. Seule la manière de voir des données diffèrent, par l'import d'un fichier depuis son ordinateur. Ces données ne seront ni modifiables, ni déplaçables et n'ont pas d'interactions avec la base de données OpenStreetMap.
Ces sources de données peuvent servir de comparaison, vérification de complétude par rapport à une autre source, ...

#### CSV
![Fichier CSV - Partie 1](images/MapContrib_005.png)

#### GeoJSON
![Fichier GeoJSON - Partie 1](images/MapContrib_006.png)

#### GPX
![Fichier GPX - Partie 1](images/MapContrib_007.png)

## Configurer ses tags

La configuration des tags va permettre ensuite de les utiliser traduit dans les "modèles" de points mais également dans les pop-ups de manière dynamique. Cela permet ainsi d'avoir une interface sans aucun mot étranger (souvent un frein pour les contributeurs ni geek ni cartographe ni contributeur).

![Définir les tags - Partie 1](images/MapContrib_032.png)

![Définir les tags - Partie 2](images/MapContrib_033.png)
![Définir les tags - Partie 3](images/MapContrib_034.png)

![Définir les tags - Partie 4](images/MapContrib_035.png)
![Définir les tags - Partie 5](images/MapContrib_036.png)
![Définir les tags - Partie 6](images/MapContrib_037.png)

## Définir les types de noeuds, "modèles"
![Définir les types de noeuds - Partie 1](images/MapContrib_038.png)
![Définir les types de noeuds - Partie 2](images/MapContrib_039.png)
![Définir les types de noeuds - Partie 3](images/MapContrib_040.png)
![Définir les types de noeuds - Partie 4](images/MapContrib_041.png)
![Définir les types de noeuds - Partie 5](images/MapContrib_042.png)

## Traduire son thème

Après avoir rempli l'ensemble des informations (chaînes de caractères par défaut, dans la langue de son choix), il est également possible de traduire les thèmes pour qu'il soit adapté en fonction de la langue du navigateur.
L'absence de traduction d'une langue entraîne l'utilisation des chaînes de caractères par défaut.

![Traduction - Partie 1](images/MapContrib_043.png)
![Traduction - Partie 2](images/MapContrib_044.png)
![Traduction - Partie 3](images/MapContrib_045.png)
![Traduction - Partie 4](images/MapContrib_046.png)
![Traduction - Partie 5](images/MapContrib_047.png)
![Traduction - Partie 5](images/MapContrib_049.png)