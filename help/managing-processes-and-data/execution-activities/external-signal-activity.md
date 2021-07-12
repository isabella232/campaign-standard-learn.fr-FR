---
title: Activité Signal externe - Appeler un workflow avec des paramètres
description: Découvrez comment démarrer un workflow à partir d’un autre pour prendre en charge des parcours client plus complexes, tout en étant en mesure de mieux surveiller les problèmes et de réagir.
feature: Activité d’exécution
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: User, Developer
level: Experienced
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 18%

---

# [!UICONTROL Activité Signal externe  ]- Appeler un workflow avec des paramètres

[!UICONTROL L’activité Signal externe] permet d’organiser et d’orchestrer différents processus qui font partie du même parcours client dans différents workflows. Elle permet de démarrer un workflow à partir d&#39;un autre, supportant ainsi des parcours client plus complexes tout en améliorant le contrôle et la réactivité en cas de problèmes.

Dans ACS 19.2, l&#39;activité [!UICONTROL Signal externe] peut non seulement appeler un workflow, mais aussi transmettre des paramètres au workflow (un nom d&#39;audience à cibler, un nom de fichier à importer, une partie du contenu du message, etc.) au workflow à partir d’un autre workflow ou d’un appel d’API REST à intégrer à vos systèmes externes.

Cela inclut également une nouvelle activité **Test** dans laquelle vous pouvez exécuter des tests sur cette fonctionnalité.

La vidéo suivante explique les étapes de configuration requises pour :

1. **Recevez des** paramètres externes d&#39;un système externe, comme un système de gestion de contenu (CRM) :

   * Déclarez les paramètres dans l’activité Signal externe
   * Configurez l’appel API pour définir les paramètres et déclencher l’activité Signal externe du workflow. Pour plus d’informations sur la configuration d’un appel API, voir [Déclenchement d’une activité de signal](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Personnaliser un workflow avec des paramètres**  externes (variables d&#39;événements) :

   Une fois le workflow déclenché, les paramètres sont ingérés dans les variables d’événements du workflow et peuvent être utilisés au sein du workflow. Voir la [documentation](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) pour toutes les activités qui peuvent être personnalisées avec des variables d’événement :

   * Configuration de l’activité de test (nouveauté de la version 19.2)
   * Configuration de l’activité Lecture d’audience et Diffusion Email

1. **Configurer une** activité de fin pour appeler un workflow avec des paramètres externes

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Ressources supplémentaires

* [Signal externe (documentation)](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
