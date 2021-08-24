---
title: Présentation d'Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector permet aux clients existants de rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Campaign) avec les données XDM (Experience Data Model) sur Adobe Experience Platform.
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 25%

---

# Présentation de Adobe Experience Platform [!UICONTROL Connecteur de données]

>[!NOTE]
>
>Cette fonctionnalité est actuellement en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.
>
>Contactez le [!UICONTROL service clientèle d’Adobe] si vous prévoyez de mettre en oeuvre cette fonctionnalité.

## Vue d&#39;ensemble

Adobe Experience Platform [!UICONTROL Data Connector] aide les clients existants à rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Adobe Campaign) sur les données [!DNL Experience Data Model] (XDM) sur Adobe Experience Platform.

Notez que le connecteur est unidirectionnel et envoie les données d’Adobe Campaign Standard vers Adobe Experience Platform. Les données ne sont jamais envoyées de Adobe Experience Platform vers Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] est destiné aux ingénieurs de données qui comprennent les [!UICONTROL ressources personnalisées d’Adobe Campaign Standard] et connaissent la définition du schéma de données global du client dans Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Cette vidéo donne un aperçu du connecteur de  [!UICONTROL données Adobe Experience Platform]  (09:35 min)*

>[!NOTE]
>
>Le transfert d’usine des [!UICONTROL événements d’abonnement] n’est pas pris en charge. Pour transférer [!UICONTROL des événements d’abonnement], vous pouvez créer le XDM et le jeu de données correspondants sur Adobe Experience Platform, puis configurer un mappage de données personnalisé pour ces données.
>
>Les [!UICONTROL événements d’expérience] existants ne peuvent pas être ingérés dans Adobe Experience Platform, mais les [!UICONTROL événements d’expérience] générés en cours seront diffusés en continu vers Adobe Experience Platform.

## Principales étapes pour effectuer un mapping des données

Les tutoriels suivants décrivent les étapes clés pour effectuer un mapping de données entre Campaign Standard et Adobe Experience Platform :

1. [Mappage de ressources personnalisées](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapping des événements d&#39;expérience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappage des données de tableau de contrôle](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modification du mapping des données](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Vérification de l&#39;état des traitements d&#39;ingestion de données](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Autres ressources

* [À propos d’Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Présentation d’Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Définition du mapping](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Activation du mapping](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Déclenchement de l’ingestion des données via les API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
