---
title: Demandes d’accès à des informations personnelles avec Adobe Campaign Standard (ACS) - Vue d’ensemble
description: Le tutoriel explique comment créer des demandes d’accès à des informations personnelles via l’interface d’Adobe Campaign Standard.
feature: Outils d'accès à des informations personnelles
kt: 1480
doc-type: feature video
activity: use
team: TM
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 62%

---

# Demandes d’accès à des informations personnelles avec l’interface utilisateur d’Adobe Campaign Standard

Adobe Campaign offre aux contrôleurs de données trois méthodes permettant de gérer les demandes d’accès à des informations personnelles et de suppression des données PII en conformité avec les lois sur la protection des données personnelles, telles que le RGPD (Règlement général sur la protection des données) et la CCPA (Loi californienne sur la protection des données) :

* **Via l’intégration à Privacy Core Service :** les demandes d’accès à des informations personnelles transmises de [!UICONTROL Privacy Service] à toutes les solutions Experience Cloud sont automatiquement gérées par Campaign via un workflow dédié. Pour savoir comment créer des demandes d’accès à des informations personnelles depuis Privacy Core Service, reportez-vous à la section [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)

* **Via l’API :** Adobe Campaign fournit une API REST qui permet le traitement automatique des demandes d’accès à des informations personnelles.

* **Via l’interface Adobe Campaign :**  pour chaque demande d’accès à des informations personnelles, le contrôleur des données crée une demande d’accès à des informations personnelles dans Adobe Campaign.

>[!NOTE]
>
> **MODIFICATIONS APPORTÉES À ACS 19.4 :**
> 
> L’[intégration à Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html) est la méthode appropriée pour toutes les demandes d’accès et de suppression. Depuis la version 19.4, l’utilisation de l’API et de l’interface de Campaign pour les demandes d’accès et de suppression est obsolète. Pour plus d’informations sur les fonctionnalités de Campaign Standard obsolètes et supprimées, consultez [cette page](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=en).
>
>**Droit d’opposition (opt-out) à la vente des informations personnelles (CCPA)**
>
> Un champ Option d’Opt-out du CCPA est fourni dans l’API et l’interface de Campaign.
>
> Vous pouvez vérifier votre version, cliquer sur le lien **?** en haut à droite de l’interface et en sélectionnant À propos.

## Tutoriels vidéos

### Conditions préalables pour les demandes d’accès à des informations personnelles

1. [Création d’un espace de noms](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modification des ressources personnalisées](/help/privacy/custom-resources-for-privacy-requests.md)

### Création, suivi et exécution des demandes d’accès à des informations personnelles via l’interface utilisateur d’Adobe Campaign

* [Création et suivi des demandes d’accès à des informations personnelles via l’interface utilisateur d’Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Exécution des demandes d’accès à des informations personnelles](/help/privacy/execute-privacy-requests.md)

## Autres ressources

* [Règles générales relatives aux informations à caractère personnel concernant Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=en#getting-started)
* [CCPA pour ACS](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=en#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [Documentation de l’API REST d’Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
