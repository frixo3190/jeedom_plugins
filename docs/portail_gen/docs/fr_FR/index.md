
# Portail

  

#### 1 - Ajout d'un portail

Le plugin se veut très simple d'utilisation !

Activez d'abord le plugin, comme tout plugin JEEDOM.
Puis ajouter un équipement dans le plugin via le bouton '+'.

#### 2 - Configuration du portail
Le plugin se veut le plus générique et flexible possible ! Cela dit , certains paramètres reste obligatoire pour un bon fonctionnement : 
- Actions pour ouvrir (onglet Actions)
- Actions pour fermer (onglet Actions)
- Une information détectant que le portail est fermé (onglet Etats)

Il est ensuite préférable de remplir : 
- le temps constaté d'ouverture du portail
- Si vous avez un capteur indiquant lorsque le portail est ouvert, cela peut être intéressant aussi pour améliorer la précision du plugin

#### 3 - Alertes
Dans l'onglet 'Communication' vous pouvez ajouter des actions (vous envoyer un mail, ...) à effectuer lorsque :
- le portail est ouvert
- le portail est fermé
- le portail n'arrive pas à se fermer
- le portail se ferme automatiquement 

#### 4 - Sécurité
le plug-in peut gérer pour vous la fermeture automatique du portail après un certain temps ouvert.
Le plug in va aussi s'assurer que lorsqu'un ordre de fermeture a été envoyé,le portail se ferme réellement sinon il va effectuer un certain nombre de tentatives.

#### 5 - Portillon
Si vous avez un petit portillon ou que vous avez la possibilité de pouvoir ouvrir qu'un seul battant du portail, le plug-in peut le prendre en charge aussi.


#### 6 - Defaillance
Si lors d'un ordre d'ouverture du portail, le capteur de fermeture du portial ne détecte pas que ce dernier n'est plus fermé dans les 5 seconde suivant l'ordre, une alerte défaillance sera émise

# Changelog <a name="changelog"></a>
# Changelog plugin Portail

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 30/01/2022
- Grosses mise a jour, beaucoup de nouveauté, je vous invite a bien revérifier votre équipement !

# 24/12/2021
- Correctifs
- Ajout de la possibilité d'effectuer des actions d'une NOUVELLE tentative de fermeture

# 18/12/2021
- Correctif sur le widget (prise en compte de l'action masquer une commande)

# 12/12/2021
- Création du plugin
