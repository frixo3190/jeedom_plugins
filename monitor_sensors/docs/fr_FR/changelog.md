# Changelog plugin Monitor Sensor

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 18/02/2024 
- Grosse mise à jour pour le support intégral de ZwaveJS
- Pour fonctionner nécessite ABSOLUMENT le plugin officiel MQTT2 de Jeedom
- Attention, désormais il y a une dépendance à installer dans le plugin

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
