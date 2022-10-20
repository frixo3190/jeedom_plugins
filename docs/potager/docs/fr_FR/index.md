

# Documentation du Plugin Potager
*Date de la dernière mise à jour : 31/05/2021*

#### Sommaire  
  1. [Installation et activation du plugin](#installation) 
  2. [Configuration du plugin](#configuration) 
  3. [Les éléments du potager](#element)
  4. [Créer une semence ou un potager](#creer)
  5. [Déclarer un semis](#creer_semis)
  6. [Organiser un potager](#potager)
  7. [Planning de vos semis](#planning)
  8. [Gérez vos arrosages (NOUVEAU)](#arrosage)


NOUVEAU : POTAGER est compatible Tablette et Smartphone !

## 1 - Installation et activation du plugin <a name="installation"></a>
### 1.1 - Installation
L'installation du plugin passe par le Market Jeedom : [lien du plugin](https://market.jeedom.com/index.php?v=d&p=market_display&id=4130)

### 1.2 Activation du plugin
Comme n’importe quel plugin JEEDOM, il est nécessaire d’activer le plugin pour qu’il fonctionne

![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/activation.jpg)
  
  

## 2 - Configuration du plugin<a name="configuration"></a>
Le plugin Potager offre la possibilité de vous prévenir en début de mois lorsque vos semences entrent en période de : 
- semis
- plantation
- éclaircissage
- récolte
- à date de péremption 

Si vous désirez profitez de ces fonctionnalités de **notification**, pensez à renseigner dans le champ prévu a cet effet dans les paramètres un moyen de notification : 
- Télégram
- Mail
- SMS

Et pensez à **sauvegarder** !
  ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/parametres.jpg)

Vous pouvez aussi activer si vous le désirez un accès rapide à vos potager (via le menu Accueil de Jeedom) , en **activant le panneau desktop**
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/pannel.jpg)

![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/acces.jpg)

## 3 - Les éléments du potager<a name="element"></a>
Le plugin potager est organisé de la façon suivante : 
- Des potagers
- Des semences
- Des semis

**Un potager**
Un terrain sur lequel vous allez positionner/organiser vos semences ainsi que des éléments graphique de décoration (muret/cloture/serre) et aussi des équipements Jeedom (Sonde/Electro-vanne/...)

**Une semence**
Un ensemble de graines d'une même espèce variété que vous allez déclarer avec toutes ses propriétés (Tomate coeur de boeuf, Choux rouge d'Italie, que sais-je)

**Un semis**
Le fait de semer (faire germer) des semences entraine la création d'un semis. Chaque semis est donc associé à une semence (une semence peut donc avoir plusieurs semis !), et contient un certains nombre d'information propre tel que date de semis/plantation/récolte/etc

*Sur toutes les pages du plugin POTAGER, pour plus de cohérence , vous trouverez en haut la même barre de navigation*
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/barre.jpg)

## 4 - Créer une semence ou un potager<a name="creer"></a>

Cliquez sur le '+' pour ajouter de nouvelles semences et/ou potager![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/plus.jpg) 

Il est impératif ‘**d’activer**’ les ‘semences’/’potager’ pour qu’ils soient fonctionnels !
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/activer.jpg)

Libre à vous de remplir ou non les informations demandées.

Un champ a toutefois son importance : **le type** 
- semence
- potager

Cela se précise via le champ type.
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/type.jpg)
  

***visuel de vos semences***
Si votre semence est détectée par l'IA , vous aurez un visuel de votre semence réaliste , et ceux sans rien faire !
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/liste_semences.jpg)


**sinon :** 
Par défaut , vos semences sont des 'graines'
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/semence.jpg)
Mais si vous les déclarez comme semées, elles vont devenir des graines en godet
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/graine_g.jpg)
Et au bout de 10j , magie , elles vont germer
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/graine_gs.jpg)

**Astuce pour le nom de semences en double/triple/etc**
Jeedom interdit d'avoir plusieurs équipements du même nom dans le meme objet parent !
Afin de pouvoir créer plusieurs tomates (d'espèce différentes) , une astuce a été mise en place
écrivez simplement : **lenomdevotreespece@index**

*exemple :* 
- tomate @1
- tomate @2
- poreau     @456

Le plugin ignorera tout ce qui trouve à partir du '@' !




## 5- Déclarer un semis<a name="creer_semis"></a>
Comme expliqué précédemment, pour une même semence, on peut déclarer plusieurs semis.
Prenons le cas de la semence 'Radis de 18 jours', le jardinier va certainement semis en plusieurs fois. On peut donc créer un premier semis (disons premier semis le 1 mai) , puis un second 1 mois plus tard , etc ,etc

pour ce faire, il faut se rendre sur la fiche de la semence 
-> Onglet Gestion -> rechercher sa semence et la sélectionner
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/gestion.jpg)
-> Puis une fois sur la fiche de notre semence, cliquer sur l'onglet '**semis**'
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/ong_semis.jpg)
Vous avez un bouton pour déclarer de nouveau semis
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/n_semis.jpg)
Renseignez les informations du semis  en temps voulu
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/i_semis.jpg)
Et pensez à **SAUVEGARDER** 

*Il existe d'autre façon de créer des semis ou de déclarer un semis comme 'semé/récolté' , c'est via la vue 'planning' , n'hésitez pas à vous référer à cette section de la documentation*

## 6 - Organiser un potager <a name="potager"></a>

Rendez vous sur la vue 'Potager' via la barre commune du plugin
 ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/o_potager.jpg)

Juste sous la barre commune du plugin se trouve un menu déroulant (discret) qui vous permet de basculer sur l'ensemble de vos potagers créés (et activés) dans la vue gestion
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/l_potager.jpg)

Commencez par choisir la bonne dimension de vos potager, pour ce faire , en bas à droite de chaque potager , cliquez et maintenez le clic sur le petit carré pour le redimensionner.


Puis ajoutez et positionnez vos semences, vous pouvez ajouter des carrer potager, des arbres, des clotures, des ruisseaux....

**Le fond 'image' du potager**
2 options proposés : fond terre ou fond herbe, pour changer, clic droit sur le potager et 'Choisir un fond Terre/Herbe'
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/menu_potager.jpg)

**Verrouillage/Déverrouillage du potager**
Afin de ne pas déplacer par mégarde vos clotures/serres et autres éléments de décoration, une fonction de verrouillage est proposée
 ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/lock_potager.jpg)

**Déplacer un élément**
Rien de plus facile, cliquez dessus et déplacez le !
*NB : si le potager est 'verrouillé', seul les semences sont modifiables/déplaçables, pour être en mesure d'éditer des éléments de décorations, il faut s'assurer que le potager est bien 'déverrouillé'*

**ASTUCE : Déplacer TOUS les éléments (en même temps)**
Cliquez en MAINTENANT la touche ALT sur un élément quelconque déplacez le !
L'ensemble des éléments du potager se déplacera en même temps !
Cette fonction peut s'avérer utile lorsque vous redimensionnez le potager et que vous avez besoin de repositionner vos éléments tous ensemble !

**Redimensionner un élément**
Pour redimensionner vos éléments , utilisez le petit carré bleu en bas a droite 
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/coin_redim.jpg)

**Effectuer une rotation à un élément**
Amenez le curseur légèrement en dessous du carré violet sur le carré vert, le curseur va se transformer en 'croix' , et un pop up vous invitera a cliquer ( et maintenir le clic) pour effectuer une rotation de l'élément !
 ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/coin_redim2.jpg)
  
  **supprimer un élément**
  Effectuez un clic-droit pour faire apparaitre un menu qui vous proposera de supprimer l'élément désiré (semence/arbre/etc...)
  ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/menu_semence.jpg)

**sélection multiple - Alignement - Espacement**
Il peut être pratique de pouvoir sélectionner plusieurs éléments afin de les déplacer conjointement , ou de les aligners (horizontalement, verticalement, espacer régulièrement horizontalement...). 
Pour ce faire, plusieurs possibilité : 
-  Cliquez sur un premier élément, puis tout en maintenant la touche MAJ , sélectionnez d'autres éléments
- Cliquez sur le plan (pas sur une semence), maintenez le clic, et déplacez la souris, un rectangle de sélection vous permettra de sélectionner des semences.*Astuce : Si vous appuyez sur la touche MAJ lors de la sélection via Clic-&-Drag, vous ne désélectionnerez pas vos précédentes sélection !




**Permaculture - Associer les espèces entres-elles !**
Lorsque vous allez déplacer une semence dans votre potager afin de la positionner, si cette dernière est détectée automatiquement par l'IA et qu'une association est possible, un halo rouge ou vert vous invitera a la rapprocher d'une autre semence ou à l'éloigner ...
![sdfsdf](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/association.jpg?raw=true)
*Dans l'exemple ci-dessus, on a sélectionné la Tomate, l'IA nous invite a rapprocher la tomate du Basilic , et a l'éloigner du Concombre !*

**Détail d'une semence & détection automatique**
Lorsque vous passer le curseur sur une espèce et que vous le laisser dessus , au bout d'une seconde un 'pop up' apparait pour vous donner quelques info rapide.
Si l'espèce en question est détecté par le programme, cela sera précisé et les associations/non associations s'afficheront de même !
![sdfsdf](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/pop_up.jpg?raw=true)

*Une petite subtilité, le programme différencie les associations en deux catégorie (de même pour les non-associations / incompatibilités)* :
- *La semence sélectionnée est invitée a être associé avec les especes xxxx , car les espèces xxx vont lui être bénéfiques (halo vert plutot foncé)*
- *La semence sélectionnée est invitée a être associé avec les especes yyyyy, car elle va être bénéfique pour les espèces yyyy (halo vert plutot clair)*


**Afficher un quadrillage sur votre potager**
Effectuez un clic-droit sur le potager (pas sur un élément) pour faire afficher le menu du potager
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/menu_potager.jpg?raw=true)
Sélectionnez '**Afficher le quadrillage'** 
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/quadrillage.jpg?raw=true)



**Générer un schéma du potager imprimable**
Le bouton **imprimer** vous génèrera un schéma de votre potager !

![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/potager2.jpg)
 
## 7 - Planning de vos semis <a name="planning"></a>
 ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/b_planning.jpg)
La vue **planning** permet de visualiser rapidement vos semences et vos semis.
Lorsqu’il faut les semer, les mettre en terre etc. Un certain nombre d’icone sont affichées à côté de vos semences pour facilement identifier : son type (légume/plante/etc) , la quantité semé / si vous avez épuisé vos semences / …
Un moteur de recherche vous est proposé de même ainsi que certains filtres
Et aussi l'année à consulter (par défaut l'année en cours)
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/date_planning.jpg)

Un trait vertical ROUGE vous marque la date du jour et vos semences sont listées
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/planning.jpg)
  Il vous est possible de cliquer sur une semence pour consulter le détail de ses semis
  ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/semis_planning.jpg)
  Il est possible d'afficher tous les semis de toutes les semences via ce bouton ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/all_semis.jpg)

***Actions rapides sur le planning (clic - droit)***
Il est possible d’effectuer un clic droit sur une semence pour  :
- Ouvrir dans un nouvel onglet la fiche d'édition de la semence
- Créer un nouveau semis
- 
Il est possible d’effectuer un clic droit sur un semis pour  :
- déclarer comme 'semée' / 'récoltée' / ....

*NB : en maintenant **la touche CTRL** lorsque vous sélectionné une option du menu clic-droit (ex :marqué comme semé) , vous serez en mesure de **définir manuellement la date** , et non d’avoir la date du jour imposée.*
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/menu_rapide.jpg)
  
  *NB : Si vous désirez annuler une mise en terre/un semis/... il suffit de repasser par ce menu, il vous proposera d'annuler*
  

Un bouton **imprimer** permet de générer une page à imprimer optimisée pour économiser de l’encre et avoir une vue synthétique de vos semences.


Il est désormais possible sur le planning de sélectionner plusieurs semis via le bouton de sélection multiple ici
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/planning_multi.jpg)
pour ensuite appliquer une même déclaration (marquer comme semé/récolté/...)

## 8 - Gérez vos arrosages <a name="arrosage"></a>
 ![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/gestion.jpg)
Nouveauté ! Le plugin Potager permet désormais d'automatiser vos arrosages !
Pour ce faire, rendez-vous dans l'onglet GESTION.
Sélectionnez un équipement (peu importe, un potager, ou une semence), puis sélectionnez l'onglet 'Arrosage'
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/arrosage.jpg)
Vous pouvez ensuite créer autant de système d'arrosage automatique que désirez en cliquant sur le bouton 'Nouvel arrosage'

Un formulaire de gestion d'arrosage sera ainsi rajouté . Vous pouvez le nommer, et le paramétrer.
![enter image description here](https://raw.githubusercontent.com/frixo3190/jeedom_plugins/main/potager/docs/img/n_arrosage.jpg)
Il est très souple. Vous pouvez sélectionner plusieurs mode de déclenchement (CRON et/ou déclencheur)
Vous pouvez aussi préciser des conditions d'annulation de démarrage de l'arrosage (ex : lancer l'arrosage à 8H00 du matin sauf s'il pleut !)
Il faudra préciser ensuite la condition de fin d'arrosage , un timer ou une condition (ex : 20min ou capteur d'humidité saturé)
Et évidement il faudra préciser les actions à opérer pour lancer et arrêter l'arrosage !

**BIEN PENSEZ A ENREGISTRER**

Des commandes JEEDOM associées à votre arrosage seront créées associées à l'équipement sur lequel l'arrosage a été créé. . 



# Changelog <a name="changelog"></a>

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte ou l'ajout de semences dans la BDD de l'ia

*Aidez moi à faire connaître POTAGER - parlez de l'application autour de vous !*

# 20/10/2022
- Maj pour compatibilité Jeedom 4.3


# 19/09/2022
- Correction bug arrosage (détection de la condition d'annuliation)

# 29/05/2022

- Diverses corrections de bugs 
- Ajout de l'élément 'Herbe'
- Ajout de divers champs
- Possibilité d'utiliser une variable ou une commande info dans le champ Timer dans l'arrosage

# 10/05/2022

- Diverses corrections de bugs 

# 11/04/2022

- Diverses corrections de bugs 

# 01/04/2022

- Diverses corrections de bugs 
- Ajout des Evol de Mr Riquette :P
- Ajout d'une évol pour Jelo52

# 17/03/2022

- Diverses corrections de bugs (dont j'ai la flemme de détailler)
- Ajout de nouveaux champs
- Ajout d'une option dans le menu clic droit sur une semence dans le planning
- Ajout nouveau filtre planning

# 08/03/2022

- Diverses corrections

# 23/02/2022

- Diverses corrections
- Ajout de la gestion des achats
- Ajout d'une barre rouge sur les icones de semence en rupture
- Ajout du trie par nom dans le planning
- Correction impression du planning (couleur ligne + couleur icone en mode Dark)
- Correction bug critique affichage planing en boucle

# 09/02/2022

- Diverses corrections
- ajout champs divers & filtre dans le planning


# 15/11/2021

- Corrections bug lune
- Correction img épinard

# 02/07/2021

- Corrections diverses
- Ajout des taches semences

# 06/06/2021

- Support format smartphone !
- optimisation des notifs push

# 02/06/2021

- Ajout équipement lune
- correction bugs divers

# 31/05/2021

- correction bugs divers
- Support intégral du TACILTE !
- Ajout divers objets
- Ajout verouillage Semences

# 25/05/2021

- correction bug suppression des commandes

# 22/05/2021

- ajout d'image dans la bdd de l'ia
- amélioration de l'ia
- Ajout de la fonctionnalité de gestion de l'arrosage
- ajout de très nombreux critères
- ajout de la selection multiple de semis dans le planning
- correction du bug de sélection d'un element tourné sur le potager
- ajout des phases de la lune
- corrections diverses

# 17/05/2021

- Correction de bugs divers
- ajout d'image dans la bdd de l'ia
- ajout de nouvelles fonctionalités (dupplication multiple/désactivation de l'ia pour une semence/...)
- ajout de nouveaux champs

# 13/05/2021

- Correction du bug : perte (rare) des pref du potagers (couleur herbe/terre)

# 11/05/2021

- Ajout des images auto
- Corrections de divers bugs

# 08/05/2021

- Ajout des semis
- Refonte de la DOC !


# 01/05/2021

- Refonte visuelle
- Possibilité de vérouiller les éléments du background !
- Corrections diverses

# 27/04/2021

- On peut désormais ajouter des équipements ou commande/info JEEDOM dans le potager visuel !
- Corrections diverses
- Ajout de divers champs


# 24/04/2021

- Ajout de divers Champs
- Correction Bugs de l'ajustement automatique (la baguette magique)
- Ajout d'une marre en élément
- Possibilité de suppresion multiple (de la sélection)
- Ajout sélection via Clic & Drag (clic et maintient du clic et déplacesement vers le bas et la droite (l'autre coté est pas géré pour le moment))
- Meilleur suport de Firefox (Attention, les versions inférieurs à Firefox 88 sont pas supportées)

# 20/04/2021

- Bascule en mode 'sélection muliple' lorsqu'on sélectionne un élément tout en maintenant la touche CTR lors du clic
- Ajout selection multiple via clic sourris (maintient et sélection)

# 13/04/2021

- Amélioration de la fonction duppliquer
- dupplication multiple

# 08/04/2021

- Prise en compte de la configuration réseau de Jeedom
- ajout champ 'date de péremption'
- correction de bug divers
- ajout alerte péremption

# 02/04/2021

- Ajout sélection multiple dans le menu
- Ajout alignement et espacement de la selection
- Ajout option paillage semence
- Correction bugs divers

# 15/02/2021

- Création du plugin
