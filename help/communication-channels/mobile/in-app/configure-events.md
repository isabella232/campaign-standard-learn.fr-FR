---
title: Configurer des événements
description: 'Lors de la configuration d’un message in-app dans les événements Adobe Campaign Standard (ACS), définissez l’action initiée par l’utilisateur qui déclenchera l’affichage du message. '
feature: In-App
topics: Mobile
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 7%

---


# Configure [!UICONTROL Events] {#configuring-events}

Lors de la configuration d’un message [!UICONTROL in-app] , vous devez définir l’action déclenchée par l’utilisateur qui déclenche l’affichage du message. Ces actions sont appelées [!UICONTROL événements]. Trois catégories de [!UICONTROL événements] sont disponibles : [!UICONTROL Événements]d’applications mobiles, événements de cycle de vie et événements Analytics.

## [!UICONTROL Evénements d&#39;application mobile] {#mobile-application-events}

[!UICONTROL Les événements] d’applications mobiles sont des événements  personnalisés qui sont implémentés dans votre application mobile.

Exemples :

* Un client a consulté un article
* Un client ajoute un article au panier
* Abandon de panier
* Un client a acheté quelque chose

Vous devez configurer ces [!UICONTROL événements] dans Adobe Campaign. La vidéo suivante décrit comment procéder.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Événements du cycle de vie]  {#life-cycle-events}

[!UICONTROL Les événements] de cycle de vie sont des [!UICONTROL événements]prêts à l&#39;emploi. Les [!UICONTROL événements] suivants sont disponibles :

* [!UICONTROL lancé]
* [!UICONTROL mis à niveau]
* [!UICONTROL écrasé]

Un exemple d’utilisation peut être un message présentant de nouvelles fonctionnalités après une mise à niveau ou une promotion de événement.

>[!NOTE]
>
>Le module  Lifecycle doit être configuré dans l&#39;application mobile. Pour plus d&#39;informations sur l&#39; [ajout de Lifecycle à votre application, reportez-vous à la section](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Evénements d&#39;analyse] {#analytics-events}

Les trois catégories suivantes sont prises en charge en fonction de ce qui est instrumenté dans votre application mobile :

* Adobe Analytics      
* [!UICONTROL Données contextuelles]
* [!UICONTROL Etat de la vue]

>[!NOTE]
>
>[!UICONTROL Les événements] Analytics nécessitent une licence Adobe Analytics. Une fois que vous avez configuré [[!DNL Analytics] l’](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) extension et ajouté [Analytics à votre application](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), ces événements deviennent disponibles dans la configuration [!UICONTROL In-App] dans ACS.

## Autres ressources

* [Activer les mesures de cycle de vie (documentation)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
