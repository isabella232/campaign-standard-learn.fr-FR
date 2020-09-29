---
title: Processus de transition - Changement de plate-forme de messagerie
description: 'Lorsque vous déplacez des prestataires de messagerie (ESP), il n’est pas possible de transition également vos adresses IP existantes et établies. Il est important que vous suiviez les meilleures pratiques pour développer une réputation positive lors de votre redémarrage. Comme les nouvelles adresses IP que vous allez utiliser n''ont pas encore de réputation, les FAI ne peuvent pas faire entièrement confiance au courrier qui leur vient et doivent être prudents dans ce qu''ils autorisent à être livrés à leurs clients. '
feature: null
topics: Deliverability
kt: null
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f4dbccc1fea3db4dbddec0d4329b359993b62d20
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---


# Processus de transition - Changement de plate-forme de messagerie

Lorsque vous déplacez des prestataires de messagerie (ESP), il n’est pas possible de transition également vos adresses IP existantes et établies. Il est important que vous suiviez les meilleures pratiques pour développer une réputation positive lors de votre redémarrage. Comme les nouvelles adresses IP que vous allez utiliser n&#39;ont pas encore de réputation, les FAI ne peuvent pas faire entièrement confiance au courrier qui leur vient et doivent être prudents dans ce qu&#39;ils autorisent à être livrés à leurs clients.

Pensez à ce que vous faites quand vous rencontrez quelqu&#39;un de nouveau. En règle générale, vous devez établir la confiance au lieu de leur faire confiance immédiatement. Ne pensez pas que votre marque va automatiquement aider à cette confiance, parce que les spammeurs utiliseront votre nom pour faire de mauvaises choses. Les FAI doivent réévaluer vos pratiques d&#39;envoi, car l&#39;action est particulièrement révélatrice dans la délivrabilité des courriels.

Établir une réputation positive est un processus. Mais une fois qu&#39;il sera établi, de petits indicateurs négatifs auront moins d&#39;impact sur vous et votre diffusion de courrier.

![Le processus de transition](assets/transition-process.png)

Le temps nécessaire pour réchauffer vos adresses et domaines IP peut varier, mais jusqu&#39;à huit semaines de référence est fréquent pour les expéditeurs types d&#39;établir une réputation auprès de la plupart des fournisseurs de services Internet de niveau 1 ([!DNL Gmail], [!DNL Microsoft], [!DNL Verizon]/[!DNL Yahoo]/[!DNL AOL], etc.).
Dans les sections suivantes, nous étudierons certains domaines clés pour nous concentrer sur la navigation.

## Infrastructure

Le succès de la livraison dépend d&#39;une base solide. L&#39;infrastructure de courriel est un élément essentiel. Une infrastructure de messagerie correctement construite comprend plusieurs composants, à savoir les domaines et les adresses IP. Ces composants sont comme la machine derrière les courriels que vous envoyez, et ils sont souvent le point d&#39;ancrage de l&#39;envoi de réputation. Les consultants en livrabilité s’assurent que ces éléments sont correctement configurés lors de l’implémentation, mais en raison de l’élément réputation, il est important pour vous d’avoir cette compréhension de base.

### Configuration et stratégie des domaines

Les temps ont changé, et certains FAI (comme [!DNL Gmail] et [!DNL Yahoo]) intègrent désormais la réputation de domaine en tant que point supplémentaire lorsqu&#39;il s&#39;agit d&#39;associer la réputation de courriel à un expéditeur. La réputation de votre domaine repose sur votre domaine d’envoi plutôt que sur votre adresse IP. Cela signifie que votre marque a la priorité en ce qui concerne les décisions de filtrage des fournisseurs de services Internet.

Une partie du processus d’intégration des nouveaux expéditeurs à Adobe Campaign inclut la configuration de vos domaines d’envoi et la garantie que votre infrastructure est correctement établie. Vous devez travailler avec un expert sur les domaines que vous prévoyez d’utiliser à long terme. Voici quelques conseils qui façonnent une bonne stratégie de domaine :

* Soyez aussi clair et réfléchi à la marque que possible avec le domaine que vous choisissez afin que les utilisateurs n’identifient pas incorrectement le courrier comme indésirable. Voici quelques exemples [!DNL newsletter.foo.com], [!DNL receipts.foo.com]etc.
* Vous ne devriez pas utiliser votre domaine parent ou d’entreprise, car cela pourrait avoir un impact sur la diffusion du courrier de votre entreprise aux FAI.
* Envisagez d’utiliser un sous-domaine de votre domaine parent pour légitimer votre domaine d’envoi.
* Séparez vos sous-domaines pour les catégories de messages transactionnels et marketing. Cela permettra à votre trafic de courrier électronique d’être plus fiable, car les FAI recherchent cette méthode d’envoi, qui est une pratique recommandée et qui est bien connue.

### Stratégie IP

Il est important de mettre en place une stratégie de PI bien structurée pour aider à établir une réputation positive. Le nombre d’adresses IP et de configurations varie en fonction de votre modèle d’entreprise et de vos objectifs marketing. Travailler avec un expert à l&#39;élaboration d&#39;une stratégie claire pour le début à droite. Considérez les points importants à noter :

* Trop d&#39;adresses IP peuvent déclencher des problèmes de réputation car il s&#39;agit d&#39;une tactique courante consistant à spammer pour raquettes, une tactique utilisée par les spammeurs où le trafic est réparti sur de nombreuses adresses IP pour maximiser la diffusion du spam. Même si vous n’êtes pas un spammeur, vous pouvez ressembler à un si vous utilisez trop d’IP, en particulier si ces IP n’ont pas eu de trafic antérieur.
* Trop peu d’adresses IP peuvent provoquer des problèmes de débit et potentiellement provoquer des problèmes de réputation. Le débit varie en fonction du fournisseur de services Internet. Le montant et la rapidité d&#39;acceptation d&#39;un FAI dépendent généralement de son infrastructure et de l&#39;envoi de seuils de réputation.
* Il est essentiel de séparer le trafic des types de messagerie. Il est important, au minimum, de séparer le marketing et le courrier transactionnel dans des pools IP distincts.
* En fonction de votre stratégie de courrier, il peut également être conseillé de séparer différents produits ou flux marketing sur différents pools d’adresses IP si votre réputation est radicalement différente. Certains spécialistes du marketing segmentent également par région. La séparation de l’IP pour le trafic dont la réputation est inférieure ne corrige pas le problème de réputation, mais évite les problèmes liés à vos &quot;bonnes&quot; diffusions de messagerie de réputation. Après tout, vous ne voulez pas sacrifier votre bonne audience pour une  plus risquée.

### Boucles de commentaires

En coulisses, Adobe Campaign traite les données concernant les rebonds, les plaintes, les désabonnements, etc. La mise en place de ces boucles de rétroaction est un aspect important de la délivrabilité. Les plaintes peuvent nuire à la réputation ; vous devez donc supprimer les adresses électroniques qui enregistrent les plaintes de votre audience de cible. Il est important de noter que [!DNL Gmail] ces données ne sont pas fournies. Les en-têtes de désabonnement de liste et le filtrage d’engagement sont particulièrement importants pour [!DNL Gmail] les abonnés, qui constituent désormais la majorité des bases de données d’abonnés.

### Authentification

L&#39;authentification est le processus que les FAI utilisent pour valider l&#39;identité d&#39;un expéditeur. Les deux protocoles d’authentification les plus courants sont [!DNL Sender Policy Framework (SPF)] et [!DNL DomainKeys Identified Mail] (DKIM). Ils ne sont pas visibles pour l’utilisateur final mais aident les fournisseurs de services Internet à filtrer les courriers électroniques des expéditeurs vérifiés. [!DNL Domain-based Message Authentication Reporting and Conformance] (DMARC) gagne en popularité, bien que ses politiques ne soient pas encore intégrées par tous les FAI dans leurs systèmes de réputation.

#### **SPF**

[!DNL Sender Policy Framework (SPF)] est une méthode d&#39;authentification qui permet au propriétaire d&#39;un domaine de spécifier les serveurs de messagerie qu&#39;il utilise pour envoyer du courrier à partir de ce domaine.

#### **DKIM**

[!DNL Domain Keys Identified Mail (DKIM)] est une méthode d&#39;authentification utilisée pour détecter les adresses d&#39;expéditeur falsifiées (communément appelées [!DNL spoofing]). Si DKIM est activé, il permet au destinataire de confirmer si l&#39;expéditeur est autorisé à envoyer du courrier à partir de ce domaine.

#### **DMARC**

[!DNL Domain-based Message Authentication, Reporting and Conformance (DMARC)] est une méthode d’authentification qui permet aux propriétaires de domaines de protéger leur domaine contre une utilisation non autorisée. DMARC utilise SPF ou DKIM ou les deux pour permettre au propriétaire d’un domaine de contrôler ce qui se passe dans les messages dont l’authentification échoue : remis, mis en quarantaine ou rejeté.

## Critères de ciblage

Lors de l’envoi de nouveaux trafics, ne faites que cible à vos utilisateurs les plus actifs au cours des premières phases du réchauffement d’IP. Cela permet d&#39;établir une réputation positive dès le départ pour établir efficacement la confiance avant de se lancer dans vos audiences moins fières. Voici une formule de base pour l’engagement :

![Formule d&#39;engagement](assets/formula-for-enagement.png)

En règle générale, un taux d’engagement est basé sur une période spécifique. Cette mesure peut varier considérablement selon que la formule est appliquée à un niveau global ou à des types de publipostage ou campagnes spécifiques. Les critères de ciblage spécifiques doivent être fournis en collaboration avec votre consultant en livrabilité Adobe Campaign, puisque chaque expéditeur et fournisseur de services Internet varie et nécessitent généralement un plan personnalisé.

## Considérations spécifiques aux fournisseurs d’accès lors du réchauffement des IP

Les FAI ont des règles et des façons différentes de voir leur trafic. Par exemple, [!DNL Gmail] est l&#39;un des fournisseurs de services Internet les plus sophistiqués parce qu&#39;ils examinent l&#39;engagement de façon très stricte (les ouvertures et les clics) en plus de toutes les autres mesures de réputation. Cela nécessite un plan personnalisé qui ne cible que les utilisateurs les plus actifs au début. D&#39;autres FAI peuvent également exiger la même chose. Travaillez avec votre consultant en livrabilité Adobe Campaign pour un plan spécifique.

## Volume

Le volume de courrier que vous envoyez est essentiel pour établir une réputation positive. Mettez-vous à la place d&#39;un FAI — si vous début voir une tonne de trafic de la part de quelqu&#39;un que vous ne connaissez pas, ce serait alarmant. L&#39;envoi immédiat d&#39;un grand volume de courrier est risqué et est sûr de causer des problèmes de réputation qui sont souvent difficiles à résoudre. Il peut s&#39;avérer frustrant, chronophage et coûteux de se sortir de la mauvaise réputation et de problèmes de blocage et de harcèlement résultant de l&#39;envoi trop tôt.

Les seuils de volume varient selon le fournisseur de services Internet et peuvent également varier en fonction des mesures d’engagement moyennes. Certains expéditeurs nécessitent une rampe de volume très faible et lente, tandis que d&#39;autres peuvent permettre une rampe de volume plus raide. Nous recommandons de travailler avec un expert, comme un consultant en livrabilité Adobe Campaign, pour élaborer un plan de volume personnalisé.

Voici une liste d&#39;astuces et de conseils pour transition en douceur :

* **L&#39;autorisation** est la base de tout programme de courriel réussi.
* **Début** faible et lent avec de faibles volumes d&#39;envoi et puis augmenter au fur et à mesure que vous établissez votre réputation d&#39;expéditeur.
* Une stratégie **** de diffusion en tandem vous permet d&#39;augmenter le volume sur Campaign tout en réduisant votre fournisseur de services de messagerie électronique, sans perturber votre calendrier de messagerie.
* **L&#39;engagement est important** - début avec les abonnés qui ouvrent et cliquent régulièrement sur vos courriels.
* **Suivez le plan** — nos recommandations ont aidé des centaines de clients Campaign à augmenter leurs programmes de messagerie.
* **Surveillez votre compte** de messagerie électronique de réponse. Votre client n’a pas le droit d’utiliser [!DNL nore-ply@xyz.com] ou de ne pas répondre.
* Les adresses inactives peuvent avoir un impact négatif sur la délivrabilité. **Réactivez et réautorisez** votre plateforme actuelle, et non vos nouvelles adresses IP.
* **Domaines** : utilisez un domaine d&#39;envoi qui est un sous-domaine du domaine réel de votre société. Par exemple, si votre domaine de société est [!DNL xyz.com], [!DNL email.xyz.com] offre plus de crédibilité aux FAI que [!DNL xyzemail.com]
* **Transparence** : les détails d’enregistrement de votre domaine de courriel doivent être disponibles publiquement et ne pas être privés.

Dans de nombreuses circonstances, le courrier transactionnel ne suit pas l’approche traditionnelle du réchauffement de la promotion. Il est de toute évidence difficile de contrôler le volume des messages transactionnels en raison de leur nature, puisqu&#39;il nécessite généralement une interaction de l&#39;utilisateur pour déclencher la touche de messagerie. Dans certains cas, le courrier transactionnel peut simplement être acheminé sans plan officiel. Dans d&#39;autres cas, il peut être préférable de transition de chaque type de message au fil du temps pour augmenter lentement le volume. Par exemple, vous pouvez souhaiter transition comme suit :

1. Confirmation d&#39;achat - engagement important en général
2. Abandon du panier - engagement à moyen terme et élevé en général
3. Courriers électroniques de bienvenue - engagement élevé, mais pouvant contenir des adresses incorrectes en fonction des méthodes de collecte de vos listes
4. Courriers électroniques de retour en arrière - engagement généralement plus faible

## Autres ressources

* [Démarrer une nouvelle plate-forme](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/managing-deliverability/starting-new-platform.html)
