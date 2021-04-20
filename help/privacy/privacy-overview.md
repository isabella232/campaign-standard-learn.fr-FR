---
title: Demandes d’accès à des informations personnelles avec Adobe Campaign Standard (ACS) - Vue d’ensemble
description: Ce tutoriel explique comment créer des demandes d’accès à des informations personnelles via l’interface d’Adobe Campaign Standard (ACS).
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: ht
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: ht
source-wordcount: '373'
ht-degree: 100%

---


# Demandes d’accès à des informations personnelles avec l’interface utilisateur d’Adobe Campaign Standard

Adobe Campaign offre aux contrôleurs de données trois méthodes permettant de gérer les demandes d’accès à des informations personnelles et de suppression des données PII en conformité avec les lois sur la protection des données personnelles, telles que le RGPD (Règlement général sur la protection des données) et la CCPA (Loi californienne sur la protection des données) :

* **Via l’intégration à Privacy Core Service :** les demandes d’accès à des informations personnelles transmises de [!UICONTROL Privacy Service] à toutes les solutions Experience Cloud sont automatiquement gérées par Campaign via un workflow dédié. Reportez-vous à la documentation d’[Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) pour savoir comment créer des demandes d’accès à des informations personnelles à partir de Privacy Core Service.

* **Via l’API :** Adobe Campaign fournit une API REST qui permet le traitement automatique des demandes d’accès à des informations personnelles.

* **Via l’interface d’Adobe Campaign :** pour chaque demande d’accès à des informations personnelles, le contrôleur de données crée une demande d’accès à des informations personnelles dans Adobe Campaign.

>[!NOTE]
>
> **MODIFICATIONS APPORTÉES À ACS 19.4 :**
> 
> L’[intégration à Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) est la méthode appropriée pour toutes les demandes d’accès et de suppression. Depuis la version 19.4, l’utilisation de l’API et de l’interface de Campaign pour les demandes d’accès et de suppression est obsolète. Pour plus d’informations sur les fonctionnalités de Campaign Standard obsolètes et supprimées, consultez [cette page](https://helpx.adobe.com/fr/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Droit d’opposition (opt-out) à la vente des informations personnelles (CCPA)**
>
>À compter de la version 19.4, le champ Option d’Opt-out du CCPA est fourni dans l’API et l’interface de Campaign. Avec la version 19.3, pour exploiter ces informations, vous devez créer ce champ dans Adobe Campaign Standard. Pour plus d’informations, voir la [documentation détaillée](https://helpx.adobe.com/fr/campaign/kb/acs-privacy.html#ccpa).
>
> Vous pouvez vérifier votre version en cliquant sur l’icône en forme de point d’interrogation (?) en haut à droite de l’interface et en sélectionnant À propos.

## Tutoriels vidéos

### Conditions préalables pour les demandes d’accès à des informations personnelles

1. [Création d’un espace de noms](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modification des ressources personnalisées](/help/privacy/custom-resources-for-privacy-requests.md)

### Création, suivi et exécution des demandes d’accès à des informations personnelles via l’interface utilisateur d’Adobe Campaign

* [Création et suivi des demandes d’accès à des informations personnelles via l’interface utilisateur d’Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Exécution des demandes d’accès à des informations personnelles](/help/privacy/execute-privacy-requests.md)

## Autres ressources

* [Règles générales relatives aux informations à caractère personnel concernant Campaign](https://helpx.adobe.com/fr/campaign/kb/campaign-privacy-overview.html)
* [CCPA pour ACS](https://helpx.adobe.com/fr/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Documentation de l’API REST d’Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
