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
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 13%

---

# Introduction à [!UICONTROL In-App] messages {#introduction}

The [!UICONTROL In-App Messaging] channel allows you to display a message when the user is active within the mobile application. This channel requires mobile applications to be integrated with [!UICONTROL Adobe Experience Platform SDK].

Ce tutoriel explique les étapes requises pour configurer les propriétés mobiles, le [!UICONTROL Launch] pour l’extension [!UICONTROL Messagerie in-app] canal et comment préparer, personnaliser et envoyer [!UICONTROL In-App] messages dans Adobe Campaign Standard. The links lead to the video tutorials on each of the highlighted topics.

## Conditions préalables requises {#prerequisites}

1. Assurez-vous que vous pouvez accéder au **[!UICONTROL In-App]** canal. Si vous ne pouvez pas accéder à ces canaux, contactez l&#39;équipe de votre compte.
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and [!UICONTROL Launch].

   1. In Adobe Campaign Standard, ensure that the IMS user is part of the [!UICONTROL Standard User] and [!UICONTROL Administrator] groups.

      Cette étape permet à l’utilisateur de se connecter à Adobe Campaign Standard, d’accéder à la page de l’application mobile du SDK Experience Platform et d’afficher les propriétés de l’application mobile que vous avez créées dans [!UICONTROL Launch].

   1. Dans [!UICONTROL Launch], assurez-vous que votre utilisateur IMS fait partie d’un [!UICONTROL Launch] profil de produit. Cette étape permet à l’utilisateur de se connecter à [!UICONTROL Launch] pour créer et afficher les propriétés. Dans le profil de produit, aucune autorisation ne doit être définie pour l’entreprise ou les propriétés, mais l’utilisateur doit être en mesure de se connecter.

1. Dans Adobe Experience Platform Launch :

   1. Créez l’application mobile en créant une propriété mobile et instrumentez votre application mobile avec le SDK Experience Platform.
   1. Installez le **Adobe Campaign Standard** pour votre application mobile.

Pour plus d’informations sur les extensions, reportez-vous à la section [Configuration de l’extension Campaign Standard dans Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) dans la documentation.

## Étapes de configuration [!UICONTROL In-App] messages {#steps-to-set-up}

1. [Configurer une application mobile à l’aide d’un SDK Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [Configuration des événements](/help/communication-channels/mobile/in-app/configure-events.md).

## Create, manage, and publish [!UICONTROL In-App] Deliveries {#create-manage-publish}

You can either create one time In-App deliveries by clicking the **[!UICONTROL Create an In-App Message]** card from the homepage, from the [!UICONTROL Marketing Activities], or you can [Create an In-App delivery within a workflow](/help/communication-channels/mobile/in-app/in-app-activity.md).

When setting up the delivery, you have three options to target your users by choosing from different delivery templates:

1. [**Diffuser un message In-App**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) pour cibler tous les utilisateurs d’une application mobile.

   Ce type de message permet d&#39;envoyer des messages à tous les utilisateurs (actuels ou futurs) de votre application mobile, même s&#39;ils n&#39;ont pas de profil existant dans Adobe Campaign. Personalization is therefore not possible when customizing the messages as the user profile does not necessarily exist in Adobe Campaign.

1. Ciblez tous les utilisateurs en fonction de leur profil d’application mobile.

   This message type enables you to target all known or anonymous users of a mobile app that have a mobile profile in Adobe Campaign. Ce type de message peut être personnalisé à l&#39;aide d&#39;attributs qui ne sont pas personnels ni sensibles. Il n&#39;est pas nécessaire d&#39;établir une liaison sécurisée entre le SDK Mobile et le service de messagerie In-App d&#39;Adobe Campaign. Ainsi, la stratégie de personnalisation est basée sur ce que vous avez appris sur les utilisateurs de leur interaction avec l’appareil. Par exemple, ciblez tous les utilisateurs qui ont lancé leur application plus de cinq fois au cours de la semaine écoulée.

1. [**Cibler les utilisateurs en fonction de leur profil Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Ce type de message permet de cibler les profils Adobe Campaign (profils CRM) abonnés à votre application mobile. Le message peut être personnalisé avec tous les attributs de profil disponibles dans Adobe Campaign. Il nécessite une liaison sécurisée entre le SDK Mobile et le service de messagerie In-App de Campaign pour s’assurer que les messages contenant des informations personnelles et sensibles sont utilisés uniquement par les utilisateurs autorisés.

Ce modèle est utile pour prendre en charge les cas d’utilisation d’orchestration cross-canal, où vous avez déjà ciblé les utilisateurs sur d’autres canaux tels que Email ou Push. En fonction de leur réponse, vous souhaitez ensuite leur envoyer un message In-App.

## Créer des rapports sur vos diffusions In-App {#report}

Once your delivery has been published, you can [report on your In-App delivery](/help/communication-channels/mobile/in-app/in-app-reporting.md).
