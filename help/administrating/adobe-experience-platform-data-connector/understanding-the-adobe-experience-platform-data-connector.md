---
title: Présentation du connecteur de données de la plate-forme Adobe Experience
description: Adobe Experience Platform Data Connector permet aux clients existants de rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Campaign) avec les données XDM (Experience Data Model) sur Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 20%

---


# Présentation du connecteur de [!UICONTROL données de la plate-forme Adobe Experience]

>[!NOTE]
>
>Cette fonctionnalité est actuellement en version bêta et fait l&#39;objet de mises à jour fréquentes et de modifications sans préavis.
>Si vous prévoyez de mettre en oeuvre cette fonctionnalité, contactez le service [!UICONTROL d’assistance clientèle] Adobe.

## Présentation

Adobe Experience Platform [!UICONTROL Data Connector] helps existing customers to make their data available on Adobe Experience Platform by mapping XTK data (data ingested in Adobe Campaign) to [!DNL Experience Data Model] (XDM) data on Adobe Experience Platform.

Notez que le connecteur est unidirectionnel et envoie les données d’Adobe Campaign Standard vers Adobe Experience Platform. Les données ne sont jamais envoyées depuis Adobe Experience Platform à Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] is intended for data engineers who understand Adobe Campaign Standard [!UICONTROL custom resources] and have an understanding of how customer&#39;s overall data schema should be inside Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Cette vidéo présente un aperçu du connecteur[!UICONTROL de]données de la plate-forme Adobe Experience (09:35 min)*

>[!NOTE]
>
>The out-of-the-box transfer of [!UICONTROL subscription events] is not supported. To transfer [!UICONTROL subscription events], you can create corresponding XDM and dataset on Adobe Experience Platform, then configure a custom data mapping for these data.
>Les événements  d’expérience existants ne peuvent pas être assimilés à Adobe Experience Platform, mais les événements [!UICONTROL d’] expérience générés en cours seront diffusés en continu sur Adobe Experience Platform.

## Etapes clés permettant d’effectuer un mappage de données

Les didacticiels suivants décrivent les étapes clés pour effectuer un mappage de données entre Campaign Standard et Adobe Experience Platform :

1. [Mappage de ressources personnalisées](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mappage des Événements d’expérience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappage des données de table des sources](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modification du mappage des données](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Vérification de l&#39;état d&#39;une tâche d&#39;assimilation de données](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Autres ressources

* [À propos d’Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Présentation d’Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Définition du mapping](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Activation du mapping](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Déclenchement de l’ingestion des données via les API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
