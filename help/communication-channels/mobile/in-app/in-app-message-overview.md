---
title: Présentation des messages In-App
description: Découvrez comment présenter à l’utilisateur des messages in-app pertinents du point de vue contextuel en réponse au comportement en temps réel d’un client dans l’application mobile.
feature: In App
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 30e8e10575aad4dcf2b0473cdd9fd6d5fc2815f4
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 16%

---

# Introduction à [!UICONTROL In-App] messages {#introduction}

Le [!UICONTROL Messagerie in-app] channel vous permet d’afficher un message lorsque l’utilisateur est principal dans l’application mobile. Ce canal nécessite l’intégration des applications mobiles avec [!UICONTROL SDK Adobe Experience Platform].

Ce tutoriel explique les étapes requises pour configurer les propriétés mobiles, le [!UICONTROL Launch] pour l’extension [!UICONTROL Messagerie in-app] canal et comment préparer, personnaliser et envoyer [!UICONTROL In-App] messages dans Adobe Campaign Standard. Les liens mènent aux tutoriels vidéo sur chacune des rubriques mises en évidence.

## Conditions préalables {#prerequisites}

1. Assurez-vous que vous pouvez accéder au **[!UICONTROL In-App]** canal. Si vous ne pouvez pas accéder à ces canaux, contactez l&#39;équipe de votre compte.
1. Vérifiez que la variable **user** dispose des **permissions** dans Adobe Campaign Standard et [!UICONTROL Launch].

   1. Dans Adobe Campaign Standard, assurez-vous que l’utilisateur IMS fait partie de la variable [!UICONTROL Utilisateur standard] et [!UICONTROL Administrateur] groupes.

      Cette étape permet à l’utilisateur de se connecter à Adobe Campaign Standard, d’accéder à la page de l’application mobile du SDK Experience Platform et d’afficher les propriétés de l’application mobile que vous avez créées dans [!UICONTROL Launch].

   1. Dans [!UICONTROL Launch], assurez-vous que votre utilisateur IMS fait partie d’un [!UICONTROL Launch] profil de produit. Cette étape permet à l’utilisateur de se connecter à [!UICONTROL Launch] pour créer et afficher les propriétés. Dans le profil de produit, aucune autorisation ne doit être définie pour l’entreprise ou les propriétés, mais l’utilisateur doit être en mesure de se connecter.

1. Dans Adobe Experience Platform Launch :

   1. Créez l’application mobile en créant une propriété mobile et instrumentez votre application mobile avec le SDK Experience Platform.
   1. Installez le **Adobe Campaign Standard** pour votre application mobile.

Pour plus d’informations sur les extensions, reportez-vous à la section [Configuration de l’extension Campaign Standard dans Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) dans la documentation.

## Étapes de configuration [!UICONTROL In-App] messages {#steps-to-set-up}

1. [Configurer une application mobile à l’aide d’un SDK Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [Configuration des événements](/help/communication-channels/mobile/in-app/configure-events.md).

## Créer, gérer et publier [!UICONTROL In-App] Diffusions {#create-manage-publish}

Vous pouvez créer des diffusions In-App ponctuelles en cliquant sur le **[!UICONTROL Création d’un message in-app]** à partir de la page d’accueil, à partir de la [!UICONTROL Activités marketing], ou vous pouvez [Créer une diffusion In-App dans un workflow](/help/communication-channels/mobile/in-app/in-app-activity.md).

Lors de la configuration de la diffusion, vous disposez de trois options pour cibler vos utilisateurs en choisissant parmi différents modèles de diffusion :

1. [**Diffuser un message In-App**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) pour cibler tous les utilisateurs d’une application mobile.

   Ce type de message permet d&#39;envoyer des messages à tous les utilisateurs (actuels ou futurs) de votre application mobile, même s&#39;ils n&#39;ont pas de profil existant dans Adobe Campaign. La personnalisation n’est donc pas possible lors de la personnalisation des messages, car le profil utilisateur n’existe pas nécessairement dans Adobe Campaign.

1. Ciblez tous les utilisateurs en fonction de leur profil d’application mobile.

   Ce type de message permet de cibler tous les utilisateurs connus ou anonymes d’une application mobile ayant un profil mobile dans Adobe Campaign. Ce type de message peut être personnalisé à l&#39;aide d&#39;attributs qui ne sont pas personnels ni sensibles. Il n&#39;est pas nécessaire d&#39;établir une liaison sécurisée entre le SDK Mobile et le service de messagerie In-App d&#39;Adobe Campaign. Ainsi, la stratégie de personnalisation est basée sur ce que vous avez appris sur les utilisateurs de leur interaction avec l’appareil. Par exemple, ciblez tous les utilisateurs qui ont lancé leur application plus de cinq fois au cours de la semaine écoulée.

1. [**Cibler les utilisateurs en fonction de leur profil Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Ce type de message permet de cibler les profils Adobe Campaign (profils CRM) abonnés à votre application mobile. Le message peut être personnalisé avec tous les attributs de profil disponibles dans Adobe Campaign. Il nécessite une liaison sécurisée entre le SDK Mobile et le service de messagerie In-App de Campaign pour s’assurer que les messages contenant des informations personnelles et sensibles sont utilisés uniquement par les utilisateurs autorisés.

Ce modèle est utile pour prendre en charge les cas d’utilisation d’orchestration cross-canal, où vous avez déjà ciblé les utilisateurs sur d’autres canaux tels que Email ou Push. En fonction de leur réponse, vous souhaitez ensuite leur envoyer un message In-App.

## Créer des rapports sur vos diffusions In-App {#report}

Une fois votre diffusion publiée, vous pouvez : [rapport sur votre diffusion In-App](/help/communication-channels/mobile/in-app/in-app-reporting.md).

## Ressources supplémentaires

* [Rapport In-App](https://experienceleague.adobe.com/docs/campaign-standard/using/reporting/list-of-reports/in-app-report.html?lang=en)
* [Configuration d’une propriété mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configuration d’une application mobile à l’aide des SDK Adobe Experience Platform](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-channels/configuring-a-mobile-application.html?lang=en)
* [Préparation et envoi d’un message In-App](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html?lang=en)
* [Personnalisation d’un message In-App](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html?lang=en)
* [Envoi d&#39;un message In-App dans un workflow](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html?lang=en)
* [Activation des mesures de cycle de vie](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
