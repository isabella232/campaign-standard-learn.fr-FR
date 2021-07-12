---
title: Configurer des événements
description: '"Comprenez comment les événements définissent l’action initiée par l’utilisateur qui déclenche l’affichage d’un message in-app. "'
feature: Dans l'application
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 8%

---

# Configurer [!UICONTROL Événements] {#configuring-events}

Lors de la configuration d’un message [!UICONTROL In-App], vous devez définir l’action lancée par l’utilisateur qui déclenche l’affichage du message. Ces actions sont appelées [!UICONTROL events]. Trois catégories [!UICONTROL events] sont disponibles : [!UICONTROL Événements d’application mobile], [!UICONTROL Événements de cycle de vie] et [!UICONTROL Événements Analytics].

## [!UICONTROL Evénements d&#39;application mobile] {#mobile-application-events}

[!UICONTROL Les ] événements d’application mobile sont des  [!UICONTROL événements ] personnalisés qui sont implémentés dans votre application mobile.

Par exemple :

* Un client a consulté un article
* Un client ajoute un article au panier
* Abandon de panier
* Un client a acheté quelque chose

Vous devez configurer ces [!UICONTROL événements] dans Adobe Campaign. La vidéo suivante explique comment procéder.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Événements du cycle de vie] {#life-cycle-events}

[!UICONTROL Les ] événements de cycle de vie sont des  [!UICONTROL événements] d’usine. Les [!UICONTROL événements] suivants sont disponibles :

* [!UICONTROL launch]
* [!UICONTROL mis à niveau]
* [!UICONTROL crashed]

Un exemple d’utilisation peut être un message présentant de nouvelles fonctionnalités après une mise à niveau ou une promotion d’événement.

>[!NOTE]
>
>Le [!UICONTROL module Lifecycle] doit être configuré dans l’application mobile. Pour plus d’informations sur [Comment ajouter Lifecycle à votre application](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle), voir ici

## [!UICONTROL Evénements d&#39;analyse] {#analytics-events}

Les trois catégories suivantes sont prises en charge en fonction de ce qui est instrumenté dans votre application mobile :

* Adobe Analytics
* [!UICONTROL Données contextuelles]
* [!UICONTROL État d’affichage]

>[!NOTE]
>
>[!UICONTROL Les ] événements Analytics nécessitent une licence Adobe Analytics. Une fois que l’extension [[!DNL Analytics] est configurée](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) et que vous avez ajouté [Analytics à votre application](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), ces événements sont disponibles dans la configuration [!UICONTROL In-App] d’ACS.

## Ressources supplémentaires

* [Activation des mesures de cycle de vie (documentation)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
