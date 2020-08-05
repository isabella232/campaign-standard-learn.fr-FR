---
title: Présentation des messages intégrés
description: Le canal de messagerie in-app Adobe Campaign Standard (ACS) vous permet de présenter à l’utilisateur des messages in-app contextuellement pertinents en réponse au comportement en temps réel d’un client dans l’application mobile.
feature: In-App
topics: Mobile
kt: 1911
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 14%

---


# Présentation des messages [!UICONTROL in-app] {#introduction}

The [!UICONTROL In-App Messaging] channel allows you to display a message when the user is active within the mobile application. This channel requires mobile applications to be integrated with [!UICONTROL Adobe Experience Platform SDK].

Ce didacticiel explique les étapes requises pour configurer les propriétés des dispositifs portables, l&#39;extension [!UICONTROL Launch] pour le canal de messagerie  in-app, ainsi que la préparation, la personnalisation et l&#39;envoi de messages [!UICONTROL in-app] dans Adobe Campaign Standard. Les liens vous conduiront aux didacticiels vidéo sur chacune des rubriques mises en évidence.

## Prérequis {#prerequisites}

1. Assurez-vous de pouvoir accéder au canal **[!UICONTROL intégré]** . Si vous ne pouvez pas accéder à ces canaux, contactez l&#39;équipe de votre compte.
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and [!UICONTROL Launch].

   1. In Adobe Campaign Standard, ensure that the IMS user is part of the [!UICONTROL Standard User] and [!UICONTROL Administrator] groups.\
      This step allows the user to log in to Adobe Campaign Standard, navigate to the Experience Platform SDK mobile app page, and view the mobile app properties that you created in [!UICONTROL Launch].
   1. In [!UICONTROL Launch], ensure that your IMS user is part of a [!UICONTROL Launch] product profile.\
      This step allows the user to log in to [!UICONTROL Launch] to create and view the properties. For more information about product profiles in [!UICONTROL Launch], see [Create your product profile](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile). Dans le profil de produit, aucune autorisation ne doit être définie pour l’entreprise ou les propriétés, mais l’utilisateur doit être en mesure de se connecter.

1. En Adobe Experience Platform Launch :

   1. Créez l’application mobile en créant une propriété mobile et instrumentalisez votre application mobile avec le SDK Experience Platform.
   1. Install the **Adobe Campaign Standard** extension for your mobile application.

For more on extensions, refer to the [Configure Campaign Standard extension in Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) in [!UICONTROL Adobe Launch ]documentation.

## Procédure de configuration des messages [!UICONTROL in-app] {#steps-to-set-up}

1. [Configurez une application mobile à l’aide du SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md)Adobe Experience Platform.

1. [Configuration de événements](/help/communication-channels/mobile/in-app/configure-events.md).

## Création, gestion et publication de Diffusions [!UICONTROL in-app] {#create-manage-publish}

Vous pouvez créer des diffusions intégrées à l’application une fois en cliquant sur la **[!UICONTROL carte Créer une diffusion de message]** intégrée à partir de la page d’accueil, à partir des Activités marketing, ou [Créer une  intégrée au sein d’un processus](/help/communication-channels/mobile/in-app/in-app-activity.md).

Lors de la configuration de la diffusion, vous disposez de trois options pour cible de vos utilisateurs en choisissant parmi différents modèles de diffusion :

1. [**Diffusez un message **](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)intégré à l’application pour cible tous les utilisateurs d’une application mobile.

   Ce type de message vous permet d&#39;envoyer des messages à tous les utilisateurs (actuels ou futurs) de votre application mobile, même s&#39;ils n&#39;ont pas de profil existant dans Adobe Campaign. La personnalisation n’est donc pas possible lorsque vous personnalisez les messages, car le profil utilisateur n’existe pas nécessairement dans Adobe Campaign.

1. Cible tous les utilisateurs en fonction de leur profil d’application mobile.

   Ce type de message vous permet de cible à tous les utilisateurs connus ou anonymes d’une application mobile disposant d’un profil mobile dans Adobe Campaign. Ce type de message peut être personnalisé à l&#39;aide d&#39;attributs qui ne sont pas personnels ni sensibles. Il n&#39;est pas nécessaire d&#39;établir une liaison sécurisée entre le SDK Mobile et le service de messagerie In-App d&#39;Adobe Campaign. Donc, la stratégie de personnalisation est basée sur ce que vous avez appris sur les utilisateurs à partir de leur interaction avec l&#39;appareil. Par exemple, cible de tous les utilisateurs qui ont lancé leur application plus de 5 fois au cours de la semaine écoulée.

1. [**Cibler les utilisateurs en fonction de leur profil Campaign **](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Ce type de message vous permet d’cible des profils Adobe Campaign (profils CRM) qui se sont abonnés à votre application mobile. Le message peut être personnalisé avec tous les attributs de profil disponibles dans Adobe Campaign, mais nécessite une poignée de main sécurisée entre Mobile SDK et Campaign In-App Messaging Service pour s’assurer que les messages contenant des informations personnelles et sensibles sont utilisés uniquement par les utilisateurs autorisés.

Ce modèle est utile pour prendre en charge les cas d’utilisation d’orchestration sur plusieurs canaux, où vous avez déjà ciblé les utilisateurs sur d’autres canaux tels que Courrier électronique ou Push et où, en fonction de leur réponse, vous souhaitez les impliquer avec un message in-app.

## Création de rapports sur vos diffusions in-app {#report}

Une fois votre diffusion publiée, vous pouvez [créer des rapports sur votre diffusion](/help/communication-channels/mobile/in-app/in-app-reporting.md)in-app.

## Autres ressources

* [Rapport In-App](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Configuration d’une propriété mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configuration d’une application mobile à l’aide des SDK Adobe Experience Platform](https://helpx.adobe.com/fr/campaign/kb/configuring-app-sdk.html)
* [Préparation et envoi d’un message In-App](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personnalisation d’un message in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Envoi d&#39;un message In-App dans un workflow](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Activer les mesures de cycle de vie](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
