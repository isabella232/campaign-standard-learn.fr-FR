---
title: Demandes de confidentialité avec l'Adobe Campaign Standard (ACS) - Présentation
description: Ce didacticiel explique comment créer des requêtes de confidentialité via l’interface Adobe Campaign Standard (ACS).
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 32%

---


# Demandes de confidentialité avec l’interface utilisateur Adobe Campaign Standard

Adobe Campaign offre les contrôleurs de données trois méthodes pour effectuer l’accès à la vie privée et supprimer les demandes de données d’identification personnelle en conformité avec les lois sur la protection de la vie privée, telles que le RGPD (Règlement général sur la protection des données) et l’ACCP (Loi californienne sur la protection de la vie privée des consommateurs) :

* **Via l’intégration de Privacy Core Service : les demandes de** confidentialité transmises par  [!UICONTROL Privacy ] Service à toutes les solutions Experience Cloud sont automatiquement traitées par Campaign via un processus dédié. Reportez-vous à l&#39;[Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) pour savoir comment créer des requêtes de confidentialité à partir du service principal de confidentialité.

* **Par le biais de l’API :** Adobe Campaign fournit une API qui permet le traitement automatique des demandes de confidentialité à l’aide de REST

* **Via l’interface Adobe Campaign :** pour chaque demande de confidentialité, le contrôleur de données crée une nouvelle demande de confidentialité dans Adobe Campaign.

>[!NOTE]
>
> **MODIFICATIONS APPORTÉES À ACS 19.4 :**
> 
> L&#39;[intégration de Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) est la méthode à utiliser pour toutes les requêtes d&#39;accès et de suppression. Depuis la version 19.4, l’utilisation de l’API et de l’interface de Campaign pour les demandes d’accès et de suppression est obsolète. Pour plus d’informations sur les fonctionnalités de Campaign Standard obsolètes et supprimées, consultez [cette page](https://helpx.adobe.com/fr/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Droit d’opposition (opt-out) à la vente des informations personnelles (CCPA)**
>
>À compter de la version 19.4, le champ Option d’Opt-out du CCPA est fourni dans l’API et l’interface de Campaign. Pour la version 19.3, pour exploiter ces informations, vous devez créer ce champ en Adobe Campaign Standard. Pour plus d’informations, consultez la [documentation détaillée](https://helpx.adobe.com/fr/campaign/kb/acs-privacy.html#ccpa).
>
> Vous pouvez vérifier votre version en cliquant sur l’icône en forme de point d’interrogation (?) en haut à droite de l’interface et en sélectionnant À propos.

## Tutoriels vidéos

### Conditions préalables pour les demandes de confidentialité

1. [Création d’un Espace de nommage](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modification des ressources personnalisées](/help/privacy/custom-resources-for-privacy-requests.md)

### Créer, suivre et exécuter des requêtes de confidentialité via l’interface utilisateur Adobe Campaign

* [Création et suivi des requêtes de confidentialité via l’interface utilisateur Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Exécuter des requêtes de confidentialité](/help/privacy/execute-privacy-requests.md)

## Autres ressources

* [Règles générales relatives aux informations personnelles pour Campaign](https://helpx.adobe.com/fr/campaign/kb/campaign-privacy-overview.html)
* [CCPA pour ACS](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Documentation de l’API REST Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
