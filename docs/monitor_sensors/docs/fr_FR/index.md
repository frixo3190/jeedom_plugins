# Monitor Sensor

#### 1 - Description
Le plugin se veut très simple d'utilisation ! 
Activez d'abord le plugin, comme tout plugin JEEDOM. Si vous désirez profiter des alertes, pensez à renseigner dans la configuration du plugin une commande pour l'envoie des message (mail, sms, télégram, ...)

Puis ajouter un équipement dans le plugin.

Pensez à activer l'équipement, et effectuez le paramétrage que vous désirez, enregistrez. 

#### 2 - Paramétrage
Le paramétrage se fait sur un 'équipement' du plugin 'monitor sensor', dans l'onglet paramétrage. Diverses options vous sont proposez, lisez les bien et activez ce que vous désirez.
Pensez à sauvegarder.

#### 3 - Monitoring
Dans l'onglet 'Monitoring' de l'équipement, vous trouverez le résultat du dernier monitoring, vous pouvez le forcer via le bouton refresh.

Un refresh forcé peut être long (env 2min), car notamment pour le ZWAVE , le plugin peut (si vous l'avez activé) pingguer les nodes hors délais et attendre un peu leur réponse. 

#### 4 - Spécificité
Seul un utilisateur de Jeedom avec le profil 'Administrateur' peut consulter et éditer un équipement de monitor sensor



# Changelog <a name="changelog"></a>

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 20/01/2022
- Ajout de la surveillance de la queue Zwave (et alertes si nécessaire)
- Ajout de la surveillance du status Zwave (et alertes si nécessaire)
- Ajout de la surveillance des status des Daemons de tous les plugins (et alertes si nécessaire)

# 06/01/2022
- Correction bug (et bonne année)

# 19/12/2021
- Ajout la possibilité d'exclure certains équipements de l'analyse
- ajout d'une nouvelle option activée par defaut : 'Ne pas renvoyer une alerte déjà envoyé lors de l'analyse précédente'

# 18/12/2021
- Correction bug

# 17/12/2021
- Ajout du rfxcom (beta)
- Ajout d'une nouvelle option pour le zwave (Considérer uniquement la date du dernier message recu pour le ZWAVE (ignorer lastmsgsended & lastCommunication))

# 16/12/2021
- Corrections bugs

# 01/12/2021
- Augmentation du délais d'attente entre les 2 tentatives (1m30)

# 21/10/2021
- Correction doublon notif

# 12/10/2021
- Création du plugin