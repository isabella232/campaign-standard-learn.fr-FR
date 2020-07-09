---
title: Panneau de contrôle
description: Le Panneau de configuration vous permet de surveiller et de gérer votre enregistrement SFTP par instance et par adresse IP de liste autorisée.
feature: Control Panel
topics: Control Panel
kt: 4696
doc-type: feature video
activity: use
team: PM
translation-type: tm+mt
source-git-commit: db20c4e6aeb10dc04a6c4556fefaa8cd18366c44
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 6%

---


# [!UICONTROL Panneau de contrôle] {#control-panel}

>[!NOTE]
>
>Les termes &quot;[!UICONTROL liste blanche]&quot; et &quot;listenoire&quot; ont été remplacés par les termes &quot;[!UICONTROL liste autorisée]&quot; et &quot;[!UICONTROL liste bloquée&quot; dans la documentation Adobe Campaign. ] Certaines occurrences de ces termes peuvent toujours exister dans l’interface utilisateur du produit, les noms d’option, le code interne, ainsi que dans les vidéos du didacticiel. Ils seront remplacés dans les prochaines versions du Panneau de configuration.

Le [!UICONTROL Panneau] de configuration permet aux administrateurs d’Adobes Campaign de surveiller les ressources clés et d’effectuer des tâches administratives, telles que la gestion de l’enregistrement SFTP par instance ou les adresses IP de [!UICONTROL liste autorisée] .

## Accessing [!UICONTROL Control Panel]

Pour accéder au Panneau de configuration, accédez à Accueil Experience Cloud : [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com):

* **[!UICONTROL Accueil]** Experience Cloud > Accès **[!UICONTROL rapide]**

   ou
* **[!UICONTROL Accueil]** de l&#39;Experience Cloud > Sélecteur [!UICONTROL de]solution : **Campaign** > Carte **[!UICONTROL du Panneau]de configuration **

   ou

* Directement à partir de l’URL : [https://experience.adobe.com/#/controlpanel](https://experience.adobe.com/#/controlpanel)

## Prérequis

Avant de commencer, remplissez les conditions préalables suivantes :

### Confirmer [!DNL IMS Org ID]

Tu as besoin de connaître ton [!DNL IMS org ID]. La vidéo suivante décrit où vous pouvez rechercher votre instance [!DNL IMS org ID].

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Vérification[!DNL IMS Org ID](00:26 min)*

### Droits d’administrateur

Les droits d’administrateur sont requis pour accéder au panneau [!UICONTROL de]configuration.
La vidéo suivante explique comment ajouter un administrateur à une instance Campaign.

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Comment ajouter un administrateur au profil produit &quot;[!UICONTROL Administrateurs]&quot; pour pouvoir utiliser le Panneau[!UICONTROL de]configuration (01:03 min)*

## Didacticiels du panneau de configuration

* **Gestion des serveurs SFTP**

   *Découvrez comment surveiller la capacité du serveur, les adresses IP de liste autorisée et ajouter des clés SSH :*

   * [Surveillance de la capacité du serveur, autorisation de la liste des adresses IP et ajout de clés SSH](/help/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.md)
   * [Génération d&#39;une clé SSH](/help/administrating/control-panel/generate-ssh-key.md)
   * [Connexion à un serveur SFTP](/help/administrating/control-panel/connect-to-sftp-server.md)
* **[Délégation de sous-domaines](/help/administrating/control-panel/subdomain-delegation.md)**

   *Découvrez comment déléguer complètement un sous-domaine à un Adobe Campaign*
* **[Ajouter des certificats SSL](/help/administrating/control-panel/adding-ssl-certificates.md)**

   *Découvrez comment ajouter des certificats SSL pour sécuriser vos sous-domaines.*
* **[Gestion des certificats SSL](/help/administrating/control-panel/managing-ssl-certificates.md)**

   *Découvrez comment vous pouvez vue l’état des certificats SSL de vos sous-domaines, ainsi que demander des renouvellements.*
* **[Gestion des enregistrements TXT Google](/help/administrating/control-panel/google-txt-record-management.md)**

   *Découvrez comment ajouter un enregistrement de vérification de site Google TXT à tous les sous-domaines utilisés pour envoyer des courriers électroniques aux adresses GMAIL via le Panneau de configuration Campaign.*

* **Gestion des clés GPG**

   *Découvrez comment générer et installer une paire de clés publique/privée sur une instance Campaign spécifique pour le chiffrement des données sortantes, ainsi que importer et installer une clé publique sur une instance Campaign pour le déchiffrement des données entrantes :*

   * [Génération et installation de clés GPG pour le chiffrement des données](./gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.md)
   * [Utilisation d’une clé GPG pour chiffrer des données](./gpg-key-management/using-a-gpg-key-to-encrypt-data.md)
   * [Décrypter des données](./gpg-key-management/decrypting-data.md)

* **[Fusillade problématique](/help/administrating/control-panel/trouble-shooting.md)**

   *Comprendre comment résoudre les problèmes du Panneau de configuration*

## Autres ressources

* [Centre d’aide du panneau de configuration](https://docs.adobe.com/content/help/fr-FR/control-panel/using/control-panel-home.html)

