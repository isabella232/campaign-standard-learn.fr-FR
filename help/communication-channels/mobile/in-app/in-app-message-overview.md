---
title: Présentation des messages In-App
description: Découvrez comment présenter à l’utilisateur des messages in-app contextuellement pertinents en réponse au comportement en temps réel d’un client dans l’application mobile.
feature: Dans l’application
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: Business Practitioner
level: Beginner
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 16%

---

# Présentation des messages [!UICONTROL in-app] {#introduction}

Le canal [!UICONTROL Messagerie in-app] vous permet d’afficher un message lorsque l’utilisateur est principal dans l’application mobile. Ce canal nécessite l’intégration des applications mobiles avec [!UICONTROL Adobe Experience Platform SDK].

Ce didacticiel explique les étapes requises pour configurer les propriétés mobiles, l&#39;[!UICONTROL extension de lancement] pour le canal [!UICONTROL Messagerie in-app], ainsi que la façon de préparer, de personnaliser et d&#39;envoyer des messages [!UICONTROL in-app] dans Adobe Campaign Standard. Les liens vous conduiront aux didacticiels vidéo sur chacune des rubriques mises en évidence.

## Prérequis {#prerequisites}

1. Assurez-vous de pouvoir accéder au canal **[!UICONTROL In-App]**. Si vous ne pouvez pas accéder à ces canaux, contactez l&#39;équipe de votre compte.
1. Vérifiez que votre **utilisateur** dispose des **autorisations** nécessaires en Adobe Campaign Standard et [!UICONTROL Lancement].

   1. En Adobe Campaign Standard, assurez-vous que l’utilisateur IMS fait partie des groupes [!UICONTROL Utilisateur standard] et [!UICONTROL Administrateur].\
      Cette étape permet à l’utilisateur de se connecter à Adobe Campaign Standard, d’accéder à la page de l’application mobile SDK Experience Platform et de vue des propriétés de l’application mobile que vous avez créée dans [!UICONTROL Launch].
   1. Dans [!UICONTROL Launch], assurez-vous que votre utilisateur IMS fait partie d&#39;un [!UICONTROL profil de produits ] Launch.\
      Cette étape permet à l’utilisateur de se connecter à [!UICONTROL Launch] pour créer et vue les propriétés. Pour plus d&#39;informations sur les profils de produits dans [!UICONTROL Lancement], voir [Création de votre profil de produits](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile). Dans le profil de produit, aucune autorisation ne doit être définie pour l’entreprise ou les propriétés, mais l’utilisateur doit être en mesure de se connecter.

1. En Adobe Experience Platform Launch :

   1. Créez l’application mobile en créant une propriété mobile et instrumentalisez votre application mobile avec le SDK Experience Platform.
   1. Installez l&#39;extension **Adobe Campaign Standard** pour votre application mobile.

Pour plus d&#39;informations sur les extensions, consultez la documentation [Configurer l&#39;extension Campaign Standard dans Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) dans [!UICONTROL Adobe Launch ]documentation.

## Etapes de configuration des messages [!UICONTROL in-App] {#steps-to-set-up}

1. [Configurer une application mobile à l’aide d’un SDK Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [Configuration de événements](/help/communication-channels/mobile/in-app/configure-events.md).

## Créer, gérer et publier des [!UICONTROL Diffusions ] intégrées {#create-manage-publish}

Vous pouvez créer des diffusions intégrées à l’application en cliquant sur la carte **[!UICONTROL Créer un message intégré]** à partir de la page d’accueil, à partir de [!UICONTROL Activités marketing], ou [Créer une diffusion intégrée dans un flux de travail](/help/communication-channels/mobile/in-app/in-app-activity.md).

Lors de la configuration de la diffusion, vous disposez de trois options pour cible de vos utilisateurs en choisissant parmi différents modèles de diffusion :

1. [**Diffusez un**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) message intégré pour cible tous les utilisateurs d’une application mobile.

   Ce type de message vous permet d&#39;envoyer des messages à tous les utilisateurs (actuels ou futurs) de votre application mobile, même s&#39;ils n&#39;ont pas de profil existant dans Adobe Campaign. La personnalisation n’est donc pas possible lorsque vous personnalisez les messages, car le profil utilisateur n’existe pas nécessairement dans Adobe Campaign.

1. Cible tous les utilisateurs en fonction de leur profil d’application mobile.

   Ce type de message vous permet de cible à tous les utilisateurs connus ou anonymes d’une application mobile disposant d’un profil mobile dans Adobe Campaign. Ce type de message peut être personnalisé à l&#39;aide d&#39;attributs qui ne sont pas personnels ni sensibles. Il n&#39;est pas nécessaire d&#39;établir une liaison sécurisée entre le SDK Mobile et le service de messagerie In-App d&#39;Adobe Campaign. Donc, la stratégie de personnalisation est basée sur ce que vous avez appris sur les utilisateurs à partir de leur interaction avec l&#39;appareil. Par exemple, cible de tous les utilisateurs qui ont lancé leur application plus de 5 fois au cours de la semaine écoulée.

1. [**Cibler les utilisateurs en fonction de leur profil Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Ce type de message vous permet d’cible des profils Adobe Campaign (profils CRM) qui se sont abonnés à votre application mobile. Le message peut être personnalisé avec tous les attributs de profil disponibles dans Adobe Campaign, mais nécessite une poignée de main sécurisée entre Mobile SDK et Campaign In-App Messaging Service pour s’assurer que les messages contenant des informations personnelles et sensibles sont utilisés uniquement par les utilisateurs autorisés.

Ce modèle est utile pour prendre en charge les cas d’utilisation d’orchestration sur plusieurs canaux, où vous avez déjà ciblé les utilisateurs sur d’autres canaux tels que Courrier électronique ou Push et où, en fonction de leur réponse, vous souhaitez les impliquer avec un message in-app.

## Rapport sur vos diffusions in-app {#report}

Une fois votre diffusion publiée, vous pouvez [créer un rapport sur votre diffusion intégrée](/help/communication-channels/mobile/in-app/in-app-reporting.md).

## Ressources supplémentaires

* [Rapport In-App](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Configuration d’une propriété mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configuration d’une application mobile à l’aide des SDK Adobe Experience Platform](https://helpx.adobe.com/fr/campaign/kb/configuring-app-sdk.html)
* [Préparation et envoi d’un message In-App](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personnalisation d’un message In-App](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Envoi d&#39;un message In-App dans un workflow](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Activer les mesures de cycle de vie](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
