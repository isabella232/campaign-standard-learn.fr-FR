---
title: Configurer des événements
description: "Comprenez comment les événements définissent l’action initiée par l’utilisateur qui déclenche l’affichage d’un message in-app. "
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 56b973566e9dee412aeee1412fe6271537fc1295
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 8%

---

# Configurer [!UICONTROL Événements] {#configuring-events}

Lors de la configuration d’une [!UICONTROL In-App] , vous devez définir l’action initiée par l’utilisateur qui déclenche l’affichage du message. Ces actions sont appelées [!UICONTROL events]. Trois catégories [!UICONTROL events] sont disponibles : [!UICONTROL Événements d’application mobile], [!UICONTROL Événements de cycle de vie], et [!UICONTROL Événements Analytics].

## [!UICONTROL Evénements d&#39;application mobile] {#mobile-application-events}

[!UICONTROL Événements d’application mobile] are [!UICONTROL événements personnalisés] qui sont implémentés dans votre application mobile.

Par exemple :

* Un client a consulté un article
* Un client ajoute un article au panier
* Abandon de panier
* Un client a acheté quelque chose

Vous devez configurer ces [!UICONTROL events] dans Adobe Campaign. La vidéo suivante explique comment procéder.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Événements de cycle de vie] {#life-cycle-events}

[!UICONTROL Événements de cycle de vie] sont prêts à l’emploi [!UICONTROL events]. Les éléments suivants [!UICONTROL events] sont disponibles :

* [!UICONTROL launch]
* [!UICONTROL mis à niveau]
* [!UICONTROL crashed]

Un exemple d’utilisation peut être un message présentant de nouvelles fonctionnalités après une mise à niveau ou une promotion d’événement.

>[!NOTE]
>
>Le [!UICONTROL Module Lifecycle] doit être configuré dans l’application mobile. Voir ici pour plus d’informations sur [Comment ajouter Lifecycle à votre application](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Evénements d&#39;analyse] {#analytics-events}

Les trois catégories suivantes sont prises en charge en fonction de ce qui est instrumenté dans votre application mobile :

* Adobe Analytics
* [!UICONTROL Données contextuelles]
* [!UICONTROL État d’affichage]

>[!NOTE]
>
>[!UICONTROL Événements Analytics] nécessitent une licence Adobe Analytics. Une fois que vous avez [!DNL Analytics] l’extension configurée et ayant ajouté Analytics à votre application ; ces événements deviennent disponibles dans la variable [!UICONTROL In-App] dans ACS.
