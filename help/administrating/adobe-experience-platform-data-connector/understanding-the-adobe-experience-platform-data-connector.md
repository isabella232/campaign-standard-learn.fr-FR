---
title: Présentation d’Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector permet aux clients existants de rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Campaign) avec les données XDM (Experience Data Model) sur Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 26%

---

# Présentation du connecteur de données Adobe Experience Platform 

>[!NOTE]
>
>Cette fonctionnalité est actuellement en version bêta et fait l&#39;objet de mises à jour fréquentes et de modifications sans préavis.
>
>Contactez le [!UICONTROL service clientèle de l&#39;Adobe] si vous prévoyez de mettre en oeuvre cette fonctionnalité.

## Vue d’ensemble

Adobe Experience Platform [!UICONTROL Data Connector] aide les clients existants à rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Adobe Campaign) aux données [!DNL Experience Data Model] (XDM) sur Adobe Experience Platform.

Notez que le connecteur est unidirectionnel et envoie les données d’Adobe Campaign Standard vers Adobe Experience Platform. Les données ne sont jamais envoyées du Adobe Experience Platform à Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] est destiné aux ingénieurs de données qui comprennent les ressources personnalisées [!UICONTROL Adobe Campaign Standard] et qui savent comment le schéma de données global du client doit être intégré à Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Cette vidéo présente un aperçu du connecteur [!UICONTROL  de ] données Adobe Experience Platform (09:35 min)*

>[!NOTE]
>
>Le transfert prêt à l’emploi de [!UICONTROL événements d’abonnement] n’est pas pris en charge. Pour transférer des [!UICONTROL événements d&#39;abonnement], vous pouvez créer le XDM et le jeu de données correspondants sur Adobe Experience Platform, puis configurer un mappage de données personnalisé pour ces données.
>
>Les [!UICONTROL événements d’expérience ] existants ne peuvent pas être assimilés à Adobe Experience Platform, mais les [!UICONTROL événements d’expérience ] générés en cours seront transmis en continu à Adobe Experience Platform.

## Etapes clés permettant d’effectuer un mappage de données

Les didacticiels suivants décrivent les étapes clés pour effectuer un mappage de données entre Campaign Standard et Adobe Experience Platform :

1. [Mappage de ressources personnalisées](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapping des événements d’expérience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappage des données de table des sources](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modification du mappage des données](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Vérification de l’état des traitements d’ingestion de données](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Autres ressources

* [À propos d’Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Présentation d’Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Définition du mapping](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Activation du mapping](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Déclenchement de l’ingestion des données via les API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
