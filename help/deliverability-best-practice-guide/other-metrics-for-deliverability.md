---
title: Autres mesures importantes pour la délivrabilité
description: Les mesures constituent l’un des meilleurs moyens d’identifier un problème de réputation d’envoi. Examinons quelques mesures clés de délivrabilité à surveiller et comment les utiliser pour identifier un problème de réputation.
feature: null
topics: Deliverability
kt: 5256
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: 6e4824185b84715d514bf21aace9e57c602e970d
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 1%

---


# Autres mesures importantes pour la délivrabilité

Les mesures constituent l’un des meilleurs moyens d’identifier un problème de réputation d’envoi. Examinons quelques mesures clés de délivrabilité à surveiller et comment les utiliser pour identifier un problème de réputation.

## Bounces

Les rebonds sont le résultat d’une tentative de diffusion et d’un échec lorsque le fournisseur de services Internet fournit des avis d’échec. Le traitement de la manipulation des rebonds est un élément essentiel de l&#39;hygiène des listes. Une fois qu’un message électronique donné a rebondi plusieurs fois de suite, ce processus le signale pour suppression. Le nombre et le type de rebonds requis pour déclencher la suppression varient d’un système à l’autre. Ce processus empêche les systèmes de continuer à envoyer des adresses électroniques non valides. Les rebonds sont l&#39;un des éléments clés de données que les FAI utilisent pour déterminer la réputation de leur IP. Il est très important de garder un oeil sur cette mesure. La méthode la plus courante pour mesurer la diffusion des messages marketing consiste à comparer &quot;distribués&quot; et &quot;rebondissés&quot; : plus le pourcentage de prestations est élevé, mieux c&#39;est. Nous allons creuser deux types différents de rebonds.

## Hard bounces

Les rebonds en dur sont des échecs permanents générés après qu’un FAI ait déterminé qu’une tentative d’envoi à une adresse d’abonné n’était pas livrable. En Adobe Campaign, les rebonds durs classés comme non livrables sont ajoutés à la quarantaine, ce qui signifie qu’ils ne seront pas tentés de nouveau. Dans certains cas, un rebond brutal serait ignoré si la cause de l&#39;échec est inconnue. Voici quelques exemples courants de rebonds durs :

* L&#39;adresse n&#39;existe pas
* Compte désactivé
* Syntaxe incorrecte
* Domaine incorrect

## Soft bounces

Les rebonds à la baisse sont des échecs temporaires que les FAI génèrent lorsqu&#39;ils ont des difficultés à livrer du courrier. Les échecs d’Soft vont se reproduire à plusieurs reprises (avec des écarts selon l’utilisation des paramètres personnalisés ou prêts à l’emploi de la diffusion Adobe Campaign) afin de tenter une diffusion réussie. Les adresses qui rebondissent continuellement doucement ne seront pas ajoutées à la quarantaine tant que le nombre maximal de Reprises n’aura pas été tenté (ce qui varie à nouveau selon les paramètres). Voici quelques-unes des causes courantes des rebonds en douceur :

* Boîte pleine
* Réception du serveur de messagerie vers le bas
* Problèmes de réputation de l&#39;expéditeur

![types de rebond](assets/bounce-types.png)

>[!NOTE]
>
>Les rebonds sont un indicateur clé d’un problème de réputation car ils peuvent mettre en évidence une source de données incorrecte (rebond) ou un problème de réputation avec un fournisseur de services Internet (rebond en douceur).
>
>Les retours à l’écran se produisent souvent dans le cadre de l’envoi d’un courrier électronique et doivent être autorisés à résoudre ce problème pendant le traitement de la nouvelle tentative avant de le caractériser comme un véritable problème de délivrabilité. Si votre taux de rebonds en douceur est supérieur à 30 % pour un seul FAI et que vous ne résolvez pas le problème dans les 24 heures, il est recommandé de s’inquiéter auprès de votre consultant en livrabilité Adobe Campaign.

## Plaintes

Les plaintes sont enregistrées lorsqu’un utilisateur indique qu’un courriel est indésirable ou inattendu. Cette action d’abonnement est généralement consignée par le client de messagerie de l’abonné lorsqu’il clique sur le bouton spam ou par un système de rapports de messages indésirables tiers.

### plainte de fournisseur

La plupart des FAI de niveau 1 et certains FAI de niveau 2 fournissent une méthode de rapports antispam à leurs utilisateurs, car les processus d&#39;exclusion et de désabonnement ont été utilisés de manière malveillante dans le passé pour valider une adresse électronique. Adobe Campaign reçoit ces plaintes via les FBL des FAI. Ceci est établi pendant le processus de configuration pour tous les FAI qui fournissent des FBL et permet à Adobe Campaign d&#39;ajouter automatiquement des adresses électroniques qui se sont plaintes à la table de quarantaines pour suppression. Les pics de plaintes des fournisseurs de services Internet peuvent être un indicateur de la mauvaise qualité des listes, des méthodes de collecte de listes moins qu&#39;optimales ou des politiques d&#39;engagement déficientes. Ils sont également souvent notés lorsque le contenu n’est pas pertinent.

### Réclamations de tiers

Il existe plusieurs groupes antispam qui permettent un rapports plus large du spam. Les mesures de plainte utilisées par ces tiers sont utilisées pour baliser le contenu des messages électroniques afin d’identifier les messages indésirables. Ce processus est également appelé empreinte digitale. Les utilisateurs de ces méthodes de traitement des plaintes par des tiers sont généralement plus avertis en ce qui concerne les courriels, de sorte qu&#39;ils peuvent avoir un impact plus important que les autres plaintes si elles n&#39;ont pas reçu de réponse.

>[!NOTE]
>
>Les FSI collectent les plaintes et les utilisent pour déterminer la réputation globale d&#39;un expéditeur. Toutes les plaintes devraient être supprimées et ne plus être contactées aussi rapidement que possible et conformément aux lois et règlements locaux.

## Pièges indésirables

Un piège à spam est une adresse utilisée pour identifier un courriel non autorisé ou non sollicité. Il existe des pièges à messages indésirables pour aider à identifier les messages envoyés par des expéditeurs frauduleux ou ceux qui ne suivent pas les meilleures pratiques en matière de messagerie. En règle générale, l&#39;adresse de courriel de piège à spam n&#39;est pas publiée publiquement et est presque impossible à identifier. La diffusion de courriels à des pièges à pourriels peut avoir un impact sur votre réputation avec des degrés de gravité différents selon le type de piège et le fournisseur de services Internet. Pour en savoir plus sur les différents types de pièges à spam, consultez les sections suivantes.

### Recyclé

Les pièges à pourriels recyclés sont des adresses qui étaient autrefois valides mais qui ne sont plus utilisées. L&#39;un des moyens clés pour garder les listes aussi propres que possible est d&#39;envoyer régulièrement des courriels à votre liste entière et de supprimer de manière appropriée les courriels rebondis. Cela permet de mettre en quarantaine les adresses électroniques abandonnées et de les empêcher d&#39;être utilisées.

Dans certains cas, une adresse peut être recyclée dans les 30 jours. L&#39;envoi régulier est un aspect essentiel d&#39;une bonne hygiène des listes, tout en supprimant régulièrement les utilisateurs inactifs. Les campagnes de réengagement font généralement partie de programmes de marketing par courriel élaborés. Ce style de campagne permet à l’expéditeur de tenter de récupérer des utilisateurs qui autrement ne seraient plus envoyés par la poste.

### Typo

Une erreur typographique de spam est une adresse qui contient une faute d&#39;orthographe ou une déformation. Cela se produit souvent avec des fautes d’orthographe connues de domaines principaux tels que [!DNL Gmail] (par exemple : [!DNL gmail] est une faute de frappe courante). Les FAI et les autres opérateurs de liste de blocage enregistreront les noms de domaines inappropriés connus pour être utilisés comme piège à spam afin d&#39;identifier les spammeurs et de mesurer la santé de l&#39;expéditeur. Le meilleur moyen d’éviter les pièges à messages indésirables consiste à utiliser un processus d’inclusion doublon pour la collecte de listes.

### Pristine

Un piège antispam intacte est une adresse qui n&#39;a pas d&#39;utilisateur final et n&#39;a jamais eu d&#39;utilisateur final. Il s’agit d’une adresse créée uniquement pour identifier les messages indésirables. Il s’agit du type de piège à pourriels le plus efficace, car il est pratiquement impossible de l’identifier et cela exigerait un effort considérable pour nettoyer votre liste. La plupart des listes bloquées utilisent des pièges antispam intacts pour liste des expéditeurs non fiables. La seule façon d’éviter que les pièges à spam ne infectent votre liste de messagerie marketing plus large consiste à utiliser un processus d’inclusion de doublon pour la collecte de listes.

## Bulking

Le stockage en masse est la diffusion du courrier dans le dossier de spam ou de courrier indésirable d&#39;un fournisseur de services Internet. Il est identifiable lorsqu’un taux d’ouverture inférieur à la normale (et parfois un taux de clics) est associé à un taux de remise élevé. Les raisons pour lesquelles les courriels sont groupés varient selon le fournisseur de services Internet. En général, cependant, si des messages sont placés dans le dossier de vrac, un indicateur qui influence la réputation d&#39;envoi (l&#39;hygiène de liste, par exemple) doit être réévalué. Il s’agit d’un signal indiquant que la réputation diminue, ce qui est un problème qui doit être corrigé immédiatement avant d’affecter d’autres campagnes. Travaillez avec votre consultant en livrabilité Adobe Campaign pour résoudre tous les problèmes de blocage en fonction de votre situation.

## Blocage

Un blocage survient lorsque les indicateurs de spam atteignent les seuils de fournisseurs de services Internet propriétaires et que le fournisseur de services Internet commence à bloquer le courrier (visible par des tentatives de publipostage reportées) d&#39;un expéditeur. Il existe différents types de blocs. En règle générale, des blocs se produisent spécifiques à une adresse IP, mais ils peuvent également se produire au niveau du domaine ou de l’entité d’envoi. La résolution d&#39;un bloc nécessite une expertise spécifique. Contactez votre consultant en livrabilité Adobe Campaign pour obtenir de l&#39;aide.

## Liste bloquée

Une liste bloquée se produit lorsqu’un gestionnaire de listes bloquées tiers enregistre un comportement de type spammer associé à un expéditeur. La cause d&#39;une liste bloquée est parfois publiée par la liste bloquée. Une liste est généralement basée sur l’adresse IP, mais dans les cas les plus graves, elle peut être établie par plage d’adresses IP ou même par domaine d’envoi. La résolution d&#39;une liste bloquée doit faire appel à l&#39;aide de votre consultant en livrabilité Adobe Campaign afin de résoudre et d&#39;empêcher toute nouvelle inscription. Certaines annonces sont extrêmement sévères et peuvent causer des problèmes de réputation à long terme difficiles à résoudre. Le résultat d’une liste bloquée varie selon la liste bloquée, mais peut avoir un impact sur la diffusion de tous les courriels.

## Autres ressources

* [Types de diffusion en échec et raisons](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/monitoring-messages/understanding-delivery-failures.html#delivery-failure-types-and-reasons)
