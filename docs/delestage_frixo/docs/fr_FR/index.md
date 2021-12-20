
  

# Délestage Frixo

  

Ceci est la version maintenue à jour du plugin Délestage recodé et debuggé par Frixo (et passé en V4) suite à un an de tentative de correction du plugin Délestage officiel

Ce n'est pas un simple FORK du plugin officiel, et ce n'est pas une tentative de bypasser JEEDOM.

Le développeur s'engage a retirer cette application si l'appli officielle Délestage est de nouveau maintenue comme il se doit

**NOUVEAU** : Ajout de la white list
  

## 1 - Description

Plugin permettant de gérer le délestage électrique. Le plugin gère 3 types de délestage :

  

- Délestage “intelligent” réservé pour le délestage de Thermostat Jeedom uniquement

- Délestage hiérarchique.

- Délestage cascado-cyclique.

  

## 2 - Fonctionnement

### Délestage intelligent.

  

Le délestage intelligent **nécessite le plugin Thermostat** pour fonctionner.

  

Le plugin classe les thermostats en fonction de leurs températures réelles en fonction des températures de consigne.

  

Ainsi le délestage interviendra en priorité sur les pièces dont l’écart est le plus faible. La gène pour les occupants sera ainsi moins importante.

  

**Remarque :** Il est obligatoire de saisir la puissance de chaque thermostat (la puissance demandé dans le plugin Délestage Frixo, pas celle dans le plugin Thermostat)

  

### Délestage hiérarchique

  

Le délestage s’effectue en mode hiérarchisé sur les x actionneurs. L’actionneur 1 sera délesté en priorité puis le 2, 3…

  

Les actionneurs seront réenclenchés dans l’ordre inverse du délestage

**Remarque :** Il est obligatoire de saisir la puissance de chaque équipement (dans le plugin Délestage Frixo)

  
  

### Délestage cascadocyclique

  

Le délestage s’effectue en mode rotatif sur les actionneurs définis pour le mode cyclique puis si la puissance est toujours supérieure au seuil, en mode hiérarchisé sur les autres.

  

**Remarque :** Il est n'est PAS obligatoire de saisir la puissance de chaque équipement (dans le plugin Délestage Frixo), mais si la puissance est saisie, alors le délestage sera plur rapide (et donc plus précis), cas sans puissance renseignée, le délesteur ne délestera que 1 équipement , puis attendra un nouveau rapport de puissance instantanée , et si la puissance est encore supérieure au seuil paramétrée, il délestera a nouveau un équipement etc etc. Si la puissance est renseigné, plusieurs équipements seront délestés en même temps afin de repasser sous le seuil immédiatement.

  
  

## Configuration

  

### Configuration générale

  

Voici les paramètres à configurer sur le plugin :

  

- Type de délestage : intelligent, hiérarchique ou cascadocyclique

- Type de compteur : Puissance instantanée ou Ampérage instantané

- Compteur : sélectionner ici la commande qui renvoie soit la puissance soit l’ampérage (dans ce cas il sera nécessaire de configurer la tension du réseau)

- Seuil en Watts : Seuil **en W** à partir duquel le délestage se déclenchera , cela peut être une valeur fixe (ex : 11000 pour 11000W) ou une info d'un équipement Jeedom

  

### Actions supplémentaires

  

Il est possible de définir des actions complémentaires en plus des actions de délestage.

Il est, par exemple, possible d’envoyer un sms pour prévenir du début et de la fin du délestage.

  
  

### Configuration avancée

  

Les paramètres suivants peuvent être réglés:

  

- Tension du réseau en Volts (220V par défaut)

- Délai avant réactivation en mins (5 mns par défaut) : délai avant lequel les équipements ne se réactiveront pas (afin d’éviter les on/off trop répétitifs)

- Délai minimum entre les relevés en s (10s par défaut) : délai nécessaire entre 2 relevés

- Puissance minimum (en W) pour considérer un équipement valide à délester (ex : si vous saisissez 100 (W), tout équipement dont la puissance constatée sera <100 sera considéré comme OFF , donc à ignorer lors du délestage) - Cette option peut être utile lorsque vous utilisez 'une information d'un équipement jeedom' pour la puissance d'un équipement à délester, et non une valeurs fixe.


### WhiteList
Il est possible de 'retirer' temporairement un équipement du délesteur , en l'ajoutant à la white liste.
S'il est en cours de délestage, il sera réactivé.
Si un cycle est en cours (mode cascadocyclique) , et que l'équipement ajouté à la whiteliste est délesté, il sera réactivé et le cycle sera relancé sans respecter exceptionnellement le délais paramétré. 
Pour ajouter un équipement à la white list, il faut appeler la commande 'Retirer un équipement temporairement du délestage'  et passer en 'Title' l'identifiant JEEDOM de la commande ON (ou l'identifiant du thermostat pour le mode SMART) de l'équipement (pour ce faire, vous pouvez utiliser un scénario ou un Virtuel)

Il est possible d'effacer totalement la white list, ou de réinclure un seul ID (via les commandes associées)


### Liaison entre délesteur
Il est désormais possible de lier des délesteur entre eux. On aura donc un délesteur père, un fils (on peut avoir un petit fils, etc...).

Le délesteur fils ne s'enclenchera que si : 
- le délesteur père est déja enclenché et qu'il a délester le maximum de ce qu'il pouvait faire !

Le délesteur père ne réenclenchera des équipements délesté que si :
- le délesteur fils est totalement réactivé (aucun équipement délesté)

il faut donc bien paramétré sur chaqu'un des délesteur (père et fils) , qui est le père de l'un , et qui est le fils de l'autre.


