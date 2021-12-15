
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