# Ethermine

#### 1 - Description
Si vous êtes un adepte du minage d'ethereum , et que vous minez en pool sur [Ethermine] , alors ce plugin va être en mesure de se connecter à votre dashboard et vous donner un certain nombre d'informations telles que : 
 - Unpaid Balance Eth
 - Unpaid Balance Euro (taux de change actualisé)
 - Workers Active (à 15min prêt)
 - Gain journalier (estimation)
 - Gain mensuel (estimation)
 - Gain annuel (estimation)
 - Date dernier paiement 


#### 2 - Configuration du plugin
Rien de spécifique à prévoir, l'installer via le market , et l'activer.

#### 3 - Se connecter à Ethermine
Ajouter un équipement sur la page du plugin, et bien préciser son adresse de portefeuille qui sert d'identifiant Ethermine. 

#### 4 - Estimation des gains
Toutes les 5 min le plugin rafraichit automatiquement l'ensemble des équipements , et va **affiner** l'estimation des gains.
*Attention, le coût de l'électricité consommé par vos équipements n'est pas déduit , c'est une estimation brute du gain.*

#### 5 - Date dernier paiement
En se basant sur le montant gagné non payé, le plugin va détecter lorsqu'un paiement du pool est effectué sur vote portefeuille. Via Jeedom il est donc simple de créer un scénario avec comme déclencheur **la date du dernier paiement** pour vous avertir

#### 6 - Active workers
Attention : Les API fournies par Ethermine ne sont pas en temps réel, mais à 15min prêt environ. 



[Ethermine]: <https://ethermine.org/>