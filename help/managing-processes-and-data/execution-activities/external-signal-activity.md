---
title: Activité de signal externe - Appelez un processus avec des paramètres
description: L’Activité Signal Externe est utilisée pour organiser et orchestrer différents processus qui font partie du même parcours client dans différents workflows. Elle permet de démarrer un workflow à partir d'un autre, supportant ainsi des parcours client plus complexes tout en améliorant le contrôle et la réactivité en cas de problèmes.
feature: Activité Signal externe
topics: Workflows
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 2237e6a7d6a8c202ea87aeeb4b1e6fa83e1c677c
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 25%

---


# [!UICONTROL Activité de signal externe  ]- Appelez un processus avec des paramètres

L&#39;[!UICONTROL activité de signal externe] est utilisée pour organiser et orchestrer différents processus qui font partie du même parcours client dans différents workflows. Elle permet de démarrer un workflow à partir d&#39;un autre, supportant ainsi des parcours client plus complexes tout en améliorant le contrôle et la réactivité en cas de problèmes.

Dans ACS 19.2, l&#39;[!UICONTROL activité de signal externe] peut non seulement appeler un flux de travail, mais aussi transmettre des paramètres au flux de travail (un nom d&#39;audience à la cible, un nom de fichier à importer, une partie du contenu du message, etc.) au processus à partir d’un autre processus ou d’un appel d’API REST pour l’intégrer à vos systèmes externes.

Cela inclut également une nouvelle Activité **Test** dans laquelle vous pouvez exécuter des tests sur cette fonctionnalité.

La vidéo suivante explique les étapes de configuration requises pour :

1. **Recevoir des** paramètres externes à partir d’un système externe, tel qu’un système de gestion de contenu (CRM) :

   * Déclarer les paramètres dans l&#39;Activité Signal externe
   * Configurez l’appel d’API pour définir les paramètres et déclencher l’Activité de signal externe du processus. Pour plus d&#39;informations sur la configuration d&#39;un appel d&#39;API, voir [Déclenchement d&#39;une Activité de signal](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Personnaliser un processus avec des paramètres**  externes (variables de événement) :

   Une fois le workflow déclenché, les paramètres sont ingérés dans les variables d’événements du workflow et peuvent être utilisés au sein du workflow. Consultez la [documentation](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) pour toutes les activités qui peuvent être personnalisées avec des variables de événement :

   * Configuration de l&#39;Activité de test (nouveauté de la version 19.2)
   * Configurer l&#39;Activité d&#39;Audience de lecture et de Diffusion de courriel

1. **Configuration d’une** activité de fin pour appeler un processus avec des paramètres externes

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Autres ressources

* [Signal externe (documentation)](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
