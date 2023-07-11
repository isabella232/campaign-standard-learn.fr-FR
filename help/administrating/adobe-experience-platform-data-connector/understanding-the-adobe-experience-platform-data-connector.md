---
title: Présentation du connecteur de données Adobe Experience Platform
description: Adobe Experience Platform Data Connector permet aux clients existants de rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Campaign) avec les données XDM (Experience Data Model) sur Adobe Experience Platform.
feature: People Core Service Integration
jira: KT-2826
thumbnail: 27304.jpg
role: User
level: Advanced
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 89f520da0455da693b27c397f95cdabab4552770
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 16%

---

# Présentation de Adobe Experience Platform [!UICONTROL Connecteur de données]

>[!NOTE]
>
>Cette fonctionnalité est en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.
>
>Veuillez contacter [!UICONTROL Service clientèle d’Adobe] si vous envisagez d’implémenter cette fonctionnalité.

## Vue d’ensemble

Adobe Experience Platform [!UICONTROL Connecteur de données] aide les clients existants à rendre leurs données disponibles sur Adobe Experience Platform en mappant les données XTK (données ingérées dans Adobe Campaign) sur [!DNL Experience Data Model] Données (XDM) sur Adobe Experience Platform.

Le connecteur est unidirectionnel et envoie les données d’Adobe Campaign Standard vers Adobe Experience Platform. Les données ne sont jamais envoyées de Adobe Experience Platform vers Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Connecteur de données] est destiné aux ingénieurs de données qui comprennent Adobe Campaign Standard [!UICONTROL ressources personnalisées] et ont une compréhension de la manière dont le schéma de données global du client doit se trouver dans Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&learn=on)

*Cette vidéo donne un aperçu de Adobe Experience Platform [!UICONTROL Connecteur de données] (09:35 min)*

>[!NOTE]
>
>Le transfert d’usine de [!UICONTROL événements d’abonnement] n’est pas prise en charge. À transférer [!UICONTROL événements d’abonnement], vous pouvez créer le XDM et le jeu de données correspondants sur Adobe Experience Platform, puis configurer un mappage de données personnalisé pour ces données.
>
>Existant [!UICONTROL événements d’expérience] ne peuvent pas être ingérés dans Adobe Experience Platform, mais générés en cours [!UICONTROL événements d’expérience] sont diffusées en continu vers Adobe Experience Platform.

## Principales étapes pour effectuer un mapping des données

Les tutoriels suivants décrivent les étapes clés pour effectuer un mapping de données entre Campaign Standard et Adobe Experience Platform :

1. [Mappage de ressources personnalisées](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapping des événements d&#39;expérience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappage des données de tableau de contrôle](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modification du mapping des données](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Vérification de l&#39;état d’un traitement d&#39;ingestion de données](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

