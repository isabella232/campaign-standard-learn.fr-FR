---
title: Etape 1 - Création d’une application Android et configuration pour l’utilisation de la messagerie Firebase Cloud
description: Dans cette partie, nous allons créer  [!DNL Android] App to receive [!UICONTROL Push notifications] envoyé depuis Adobe Campaign Standard. Pour recevoir les notifications Push, l'application doit être enregistrée auprès de Google [!DNL Firebase Cloud Service].
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: cdd78e97f2769503d3d4f26933ccc7f35e9b20b9
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---


# Étape 1 - Création d&#39;une application [!DNL Android] et configuration pour utiliser [!DNL Firebase Cloud Messaging]

Dans cette partie, vous allez créer une application [!DNL Android] pour recevoir les [!UICONTROL notifications Push] envoyées d&#39;Adobe Campaign Standard. Pour recevoir les notifications Push, l&#39;application doit être enregistrée auprès de [!DNL Firebase Cloud Service] Google.

1. Connectez-vous à votre compte [!DNL Firebase].

   [!DNL Firebase] est la plate-forme mobile de Google qui vous aide à développer rapidement des applications de haute qualité. Si vous n&#39;avez pas de compte [!DNL Firebase], créez-en un [à partir d&#39;ici](https://firebase.google.com).

2. Lancer [!DNL Android Studio]
3. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Nouveau]** > **[!UICONTROL Nouveau projet].**
4. Sélectionnez **[!UICONTROL Activité vide]** et cliquez sur **[!UICONTROL Suivant].**

   ![android-project](assets/android-project.PNG)

5. Attribuez un nom significatif au projet.

   Aux fins de cette démonstration, nous avons nommé notre projet *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acceptez les noms de package par défaut et cliquez sur **[!DNL Finish]** pour créer votre projet.
7. La structure de votre projet doit ressembler à la capture d’écran ci-dessous.

   ![android-project-structure](assets/android-project-structure.PNG)

8. Cliquez sur **[!UICONTROL Outils]** > **[!UICONTROL Firebase].** (ceci ajoute le projet à  [!DNL Firebase])
9. Cliquez sur **[!UICONTROL Configurer Firebase Cloud Messaging].**

   ![configuration de base de feu](assets/android-project-firebase-messaging.PNG)

10. Cliquez sur **[!UICONTROL Se connecter à Firebase].**
11. Une fois votre application connectée à Firebase, cliquez sur **[!UICONTROL Ajouter FCM à votre application].**
12. Cliquez sur **[!UICONTROL Accepter les modifications].**

   Lorsque vous ajoutez FCM à votre application, l’assistant a besoin de votre autorisation pour apporter des modifications à votre projet.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Une fois l’intégration de votre application avec Firebase réussie, vous devez recevoir un message tel que celui illustré ci-dessous :

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Assurez-vous que votre projet est répertorié  [!DNL Firebase ]dans Console.](https://console.firebase.google.com/)

## Configurer les paramètres [!UICONTROL Canal push]

1. Connexion à la console [!DNL Firebase]
2. Ouvrez le projet **[!UICONTROL ACSPushTutorial]**.
3. Cliquez sur l&#39;icône **engrenage** et ouvrez les paramètres du projet.

   ![project-settings](assets/firebase-project-settings.PNG)

4. Appuyez sur l’onglet **[!UICONTROL Cloud Messaging]**.
5. Copier la clé de serveur

   ![clé de serveur](assets/firebase-server-key.PNG)

6. Connexion à votre instance Adobe Campaign Standard
7. Cliquez sur **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Application mobile].**
8. Sélectionnez **[!UICONTROL Mobile Application Property] approprié.**
9. Cliquez sur l&#39;icône **[!DNL Android]** dans la section **[!UICONTROL Paramètres de Canal Push]**.
10. Collez la clé de serveur dans le champ de clé de serveur.

Si tout se passe bien, vous devriez voir un message SUCCESS.

![push-canal-settings](assets/push-channel-settings.PNG)

En résumé, nous avons créé un [!DNL Android App] et connecté [!DNL Android App] à [!DNL Firebase]. Nous avons ensuite connecté l’application mobile en Adobe Campaign avec l’[!DNL Android App] en collant la clé de serveur de l’application [!DNL Android] dans l’application mobile de Adobe Campaign Standard.
