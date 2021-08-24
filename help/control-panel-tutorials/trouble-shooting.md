---
title: Résolution des problèmes liés au panneau de contrôle
description: Le Panneau de Contrôle vous permet de surveiller et de gérer votre stockage SFTP par instance et par liste autorisée d’adresses IP.
feature: Panneau de contrôle
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 47%

---

# Résolution des problèmes liés au [!UICONTROL panneau de contrôle]

Découvrez comment résoudre les problèmes liés à l’utilisation du panneau de contrôle.

## Connexion et page d’accueil

Problèmes liés à la connexion et à la page d’accueil.

### Symptôme : Impossible de se connecter à Adobe Experience Cloud

**Que faire :**
l’utilisateur doit localiser son  [!DNL IMS Org ID] (xxx). L’administrateur doit ajouter l’utilisateur au [!UICONTROL profil de produit] [!DNL “Campaign-xxx-Admins”] pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il doit s’ajouter en tant que *[!UICONTROL user]*.

### Symptôme : les liens dans la [!UICONTROL page d’accueil d’Adobe Experience Cloud] permettant d’accéder au [!UICONTROL panneau de contrôle] n’apparaissent pas pour un utilisateur.

**Cause :**
les utilisateurs ne verront pas les liens tant qu’ils ne seront pas ajoutés en tant qu’utilisateurs au [!UICONTROL profil de produit]. `Campaign-xxx-Administrators/Admin`

**Que faire :**
l’administrateur doit ajouter l’utilisateur au  [!UICONTROL profil de ] *[!DNL Campaign-xxx-Admins]* produit pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il doit s’ajouter en tant que *[!UICONTROL user]*.

### Symptôme : une instance n’est pas répertoriée dans le [!UICONTROL panneau de contrôle]

**Cause :**
l’utilisateur le plus probable doit être ajouté en tant que profil  ** userProduct  `Campaign-xxx-Administrators/Admin` pour l’instance manquante.

**Que faire :**
l’administrateur doit ajouter l’utilisateur au profil de produit  `Campaign-xxx-Admins` pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il doit s’ajouter en tant que *[!UICONTROL user]*.

### Vidéos utiles

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Vérification [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Comment ajouter un administrateur au [!UICONTROL profil de produit] [!DNL administrators] pour pouvoir utiliser le [!UICONTROL panneau de contrôle] (01:03 min)*

### Documentation utile

* [Découvrir le [!UICONTROL panneau de contrôle]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=fr)
* [Gestion des autorisations pour le [!UICONTROL panneau de contrôle]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## Établissement de la connexion au serveur SFTP (client ou API)

La connexion aux serveurs SFTP requiert :

* La [!UICONTROL mise sur une liste autorisée] de l’adresse IP à partir de laquelle vous vous connectez au serveur SFTP.
* Paire de clés privée/publique qui doit être enregistrée auprès d’Adobe Campaign
* Si vous vous connectez directement au serveur SFTP, vous avez besoin du logiciel client SFTP.

### Documentation utile {#helpful-docs}

* [Connexion à votre serveur SFTP](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
