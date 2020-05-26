---
title: Activité de signal externe - Appelez un processus avec des paramètres
description: L'Activité Signal Externe est utilisée pour organiser et orchestrer différents processus qui font partie du même parcours client dans différents workflows. Elle permet de démarrer un workflow à partir d'un autre, supportant ainsi des parcours client plus complexes tout en améliorant le contrôle et la réactivité en cas de problèmes.
feature: External Signal Activity
topics: Workflows
kt: 2750
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 19%

---


# [!UICONTROL activité de signal externe ]- Appelez un processus avec des paramètres

The [!UICONTROL External Signal activity] is used to organize and orchestrate different processes that are part of the same customer journey into different workflows. Elle permet de démarrer un workflow à partir d&#39;un autre, supportant ainsi des parcours client plus complexes tout en améliorant le contrôle et la réactivité en cas de problèmes.

Dans ACS 19.2, l&#39;activité [!UICONTROL Signal] externe peut non seulement appeler un flux de travail, mais également transmettre des paramètres au flux de travail (un nom d&#39;audience à la cible, un nom de fichier à importer, une partie du contenu du message, etc.). au processus à partir d’un autre processus ou d’un appel d’API REST pour l’intégrer à vos systèmes externes.

This also includes a new **Test** Activity where you can run tests on this functionality.

La vidéo suivante explique les étapes de configuration requises pour :

1. **Recevez des paramètres** externes d’un système externe, tel qu’un système de gestion de contenu (CRM) :
   * Déclarer les paramètres dans l&#39;Activité Signal externe
   * Configurez l’appel d’API pour définir les paramètres et déclencher l’Activité de signal externe du processus. Pour plus d’informations sur la configuration d’un appel d’API, voir [Déclenchement d’une Activité](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)de signal.

1. **Personnalisez un processus avec des paramètres** externes (variables de événement) :
Une fois le processus déclenché, les paramètres sont incorporés dans les variables de événement du processus et peuvent être utilisés dans le processus. Consultez la [documentation](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) de toutes les activités qui peuvent être personnalisées à l’aide de variables de événement :

   * Configuration de l&#39;Activité de test (nouveauté de la version 19.2)
   * Configurer l&#39;Activité d&#39;Audience de lecture et de Diffusion de courriel

1. **Configurer une Activité** de fin pour appeler un processus avec des paramètres externes

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Ressources supplémentaires

* [Signal externe (documentation)](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
