
# Délestage Frixo

## 1 - Description
Plugin permettant de gérer le délestage électrique. Le plugin gère 3 types de délestage :

-   Délestage “intelligent” réservé pour le délestage de Thermostat Jeedom uniquement
-   Délestage hiérarchique.
-   Délestage cascado-cyclique.

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

**Remarque :** Il est obligatoire de saisir la puissance de chaque équipement (dans le plugin Délestage Frixo)


## Configuration

### Configuration générale

Voici les paramètres à configurer sur le plugin :

-   Type de délestage : intelligent, hiérarchique ou cascadocyclique
-   Type de compteur : Puissance instantanée ou Ampérage instantané
-   Compteur : sélectionner ici la commande qui renvoie soit la puissance soit l’ampérage (dans ce cas il sera nécessaire de configurer la tension du réseau)
-   Seuil en Watts : Seuil **en W** à partir duquel le délestage se déclenchera , cela peut être une valeur fixe (ex : 11000 pour 11000W) ou une info d'un équipement Jeedom

### Actions supplémentaires

Il est possible de définir des actions complémentaires en plus des actions de délestage.
Il est, par exemple, possible d’envoyer un sms pour prévenir du début et de la fin du délestage.


### Configuration avancée

Les paramètres suivants peuvent être réglés:

-   Tension du réseau en Volts (220V par défaut)
-   Délai avant réactivation en mins (5 mns par défaut) : délai avant lequel les équipements ne se réactiveront pas (afin d’éviter les on/off trop répétitifs)
-   Délai minimum entre les relevés en s (10s par défaut) : délai nécessaire entre 2 relevés
-   Puissance minimum (en W) pour considérer un équipement valide à délester (ex : si vous saisissez 100 (W), tout équipement dont la puissance constatée sera <100 sera considéré comme OFF , donc à ignorer lors du délestage) - Cette option peut être utile lorsque vous utilisez 'une information d'un équipement jeedom' pour la puissance d'un équipement à délester, et non une valeurs fixe. 