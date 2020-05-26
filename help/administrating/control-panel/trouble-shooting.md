---
title: Problème lors de l'exécution du Panneau de configuration
description: Le Panneau de configuration vous permet de surveiller et de gérer votre enregistrement SFTP par instance et adresses IP de liste blanche.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 3%

---


# Problème lors de la prise en charge du [!UICONTROL Control Panel}

Découvrez comment résoudre les problèmes lors de l’utilisation du Panneau de configuration.

## Connexion et page d&#39;accueil

Problèmes survenant avec la connexion et la page d’accueil.

### Symptôme : Impossible de se connecter à Adobe Experience Cloud

**Que faire :**
L’utilisateur doit localiser son [!DNL IMS Org ID] (xxx). L’administrateur doit ajouter l’utilisateur au profil [!UICONTROL de] produits [!DNL “Campaign-xxx-Admins”] pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il peut encore être nécessaire de s’ajouter en tant qu’ *[!UICONTROL utilisateur]*.

### Symptôme : Les liens dans la page d’accueil [!UICONTROL d’] Adobe Experience Cloud permettant d’accéder au panneau [!UICONTROL de] configuration n’apparaissent pas pour un utilisateur.

**Cause :**
Les utilisateurs ne verront pas les liens tant qu’ils ne seront pas ajoutés en tant qu’utilisateurs au profil de [!UICONTROL produits.] `Campaign-xxx-Administrators/Admin`

**Que faire :**
L’administrateur doit ajouter l’utilisateur au profil [!UICONTROL de] produits *[!DNL Campaign-xxx-Admins]* pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il peut encore être nécessaire de s’ajouter en tant qu’ *[!UICONTROL utilisateur]*.

### Symptôme : Une instance n’est pas répertoriée dans le panneau de [!UICONTROL configuration.]

**Cause :**
L&#39;utilisateur doit probablement être ajouté en tant qu&#39;Profil *[!UICONTROL utilisateur]* du produit `!DNL Campaign-xxx-Administrators/Admin` pour l&#39;instance manquante.

**Que faire :**
L’administrateur doit ajouter l’utilisateur au Profil de produits `Campaign-xxx-Admins` pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il peut encore être nécessaire de s’ajouter en tant qu’ *[!UICONTROL utilisateur]*.

### Vidéos utiles

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Vérification[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Comment ajouter un administrateur au profilde produits *[!DNL administrators]*pour pouvoir utiliser le Panneaude configuration (01:03 min)*

### Documentation utile

* [Découvrez le panneau de [!UICONTROL configuration]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [[!UICONTROL Gestion des autorisations pour le panneau de contrôle]](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## Établissement de la connexion au serveur SFTP (client ou API)

La connexion aux serveurs SFTP requiert :

* [!UICONTROL Liste blanche] de l’adresse IP à partir de laquelle vous vous connectez au serveur SFTP.
* Paire de clés privée/publique qui doit être enregistrée avec Adobe Campaign
* Si vous vous connectez directement au serveur SFTP, vous aurez également besoin du logiciel client SFTP.

### Documentation utile

* [Connexion à votre serveur SFTP](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)

