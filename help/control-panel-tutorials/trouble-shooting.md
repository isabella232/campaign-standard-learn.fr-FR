---
title: Résolution des problèmes liés au panneau de contrôle
description: Le panneau de contrôle permet de surveiller et de gérer votre espace de stockage SFTP par instance et d’ajouter des adresses IP aux listes autorisées.
feature: Panneau de contrôle
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 100%

---

# Résolution des problèmes liés au [!UICONTROL panneau de contrôle]

Découvrez comment résoudre les problèmes liés à l’utilisation du panneau de contrôle.

## Connexion et page d’accueil

Problèmes liés à la connexion et à la page d’accueil.

### Symptôme : impossible de se connecter à Adobe Experience Cloud.

**Que faire :**
l’utilisateur doit rechercher son [!DNL IMS Org ID] (xxx). L’administrateur doit ajouter l’utilisateur au [!UICONTROL profil de produit] [!DNL “Campaign-xxx-Admins”] pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il peut quand même avoir besoin de s’ajouter en tant qu’*[!UICONTROL utilisateur]*.

### Symptôme : les liens dans la [!UICONTROL page d’accueil d’Adobe Experience Cloud] permettant d’accéder au [!UICONTROL panneau de contrôle] n’apparaissent pas pour un utilisateur.

**Cause :**
les utilisateurs ne verront pas les liens tant qu’ils ne seront pas ajoutés en tant qu’utilisateurs au [!UICONTROL profil de produit]. `Campaign-xxx-Administrators/Admin`

**Que faire :**
l’administrateur doit ajouter l’utilisateur au [!UICONTROL profil de produit] *[!DNL Campaign-xxx-Admins]* pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il peut quand même avoir besoin de s’ajouter en tant qu’*[!UICONTROL utilisateur]*.

### Symptôme : une instance n’est pas répertoriée dans le [!UICONTROL panneau de contrôle].

**Cause :**
l’utilisateur doit probablement être ajouté en tant qu’*[!UICONTROL utilisateur]* au profil de produit `Campaign-xxx-Administrators/Admin` pour l’instance manquante.

**Que faire :**
l’administrateur doit ajouter l’utilisateur au profil de produit `Campaign-xxx-Admins` pour chaque instance qu’il souhaite gérer. Si l’utilisateur est un administrateur de toutes les instances, il peut quand même avoir besoin de s’ajouter en tant qu’*[!UICONTROL utilisateur]*.

### Vidéos utiles

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Vérification [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Comment ajouter un administrateur au [!UICONTROL profil de produit] [!DNL administrators] pour pouvoir utiliser le [!UICONTROL panneau de contrôle] (01:03 min)*

### Documentation utile

* [Découvrir le [!UICONTROL panneau de contrôle]](https://helpx.adobe.com/fr/campaign/kb/control-panel-overview.html)
* [Gestion des autorisations pour le [!UICONTROL panneau de contrôle]](https://helpx.adobe.com/fr/campaign/kb/control-panel-access.html)

## Établissement de la connexion au serveur SFTP (client ou API)

La connexion aux serveurs SFTP requiert :

* La [!UICONTROL mise sur une liste autorisée] de l’adresse IP à partir de laquelle vous vous connectez au serveur SFTP.
* Une paire de clés privée/publique qui doit être enregistrée auprès d’Adobe Campaign.
* Si vous vous connectez directement au serveur SFTP, vous aurez également besoin d’un logiciel client SFTP.

### Documentation utile {#helpful-docs}

* [Connexion à votre serveur SFTP](https://docs.adobe.com/content/help/fr-FR/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)
