---
title: Etape 1 - Création d’une application Android et configuration pour l’utilisation de la messagerie Firebase Cloud
description: Dans cette partie, nous allons [!DNL Android] App to receive [!UICONTROL Push notifications] créer à partir de l'Adobe Campaign Standard. Pour recevoir les notifications Push, l'application doit être enregistrée auprès de Google [!DNL Firebase Cloud Service].
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---


# Etape 1 - Création d’ [!DNL Android] application et configuration pour l’utilisation [!DNL Firebase Cloud Messaging]

Dans cette partie, vous allez créer [!DNL Android] une application pour recevoir les notifications [!UICONTROL Push] envoyées depuis l&#39;Adobe Campaign Standard. Pour recevoir les notifications Push, l&#39;application doit être enregistrée auprès de Google [!DNL Firebase Cloud Service].

1. Connectez-vous à votre [!DNL Firebase] compte.

   [!DNL Firebase] est la plate-forme mobile de Google qui vous aide à développer rapidement des applications de haute qualité. Si vous n&#39;avez pas de [!DNL Firebase] compte, veuillez en créer un [à partir d&#39;ici](https://firebase.google.com).

2. Lancement [!DNL Android Studio]
3. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Nouveau]** > **[!UICONTROL Nouveau projet].**
4. Sélectionnez Activité **** vide et cliquez sur **[!UICONTROL Suivant].**

   ![android-project](assets/android-project.PNG)

5. Attribuez un nom significatif au projet.

   Pour les besoins de cette démonstration, nous avons nommé notre projet *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acceptez les noms de package par défaut et cliquez sur **[!DNL Finish]** pour créer votre projet.
7. La structure de votre projet doit ressembler à la capture d’écran ci-dessous.

   ![android-project-structure](assets/android-project-structure.PNG)

8. Cliquez sur **[!UICONTROL Outils]** > **[!UICONTROL Firebase].**(ceci ajoute le projet à[!DNL Firebase])
9. Cliquez sur **[!UICONTROL Configurer la messagerie]cloud Firebase.**

   ![configuration de base de feu](assets/android-project-firebase-messaging.PNG)

10. Cliquez sur **[!UICONTROL Se connecter à Firebase].**
11. Une fois votre application connectée à Firebase, cliquez sur **[!UICONTROL Ajouter FCM à votre application].**
12. Cliquez sur **[!UICONTROL Accepter les modifications].**

   Lorsque vous ajoutez FCM à votre application, l’assistant a besoin de votre autorisation pour apporter des modifications à votre projet.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Une fois l’intégration de votre application avec Firebase réussie, vous devez recevoir un message tel que celui illustré ci-dessous :

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Assurez-vous que votre projet est répertorié [!DNL Firebase ]dans Console.](https://console.firebase.google.com/)

## Configuration des paramètres de Canal  Push

1. Connexion à [!DNL Firebase] la console
2. Ouvrez le projet **[!UICONTROL ACSPushTutorial]** .
3. Cliquez sur l’icône **d’** engrenage et ouvrez les paramètres du projet.

   ![project-settings](assets/firebase-project-settings.PNG)

4. Accédez à l’onglet **[!UICONTROL Cloud Messaging]** .
5. Copier la clé de serveur

   ![clé de serveur](assets/firebase-server-key.PNG)

6. Connexion à votre instance d&#39;Adobe Campaign Standard
7. Cliquez sur **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Mobile App.]**
8. Sélectionnez la propriété **[!UICONTROL d’application]mobile appropriée.**
9. Cliquez sur l’ **[!DNL Android]icône **de la section Paramètres**[!UICONTROL du Canal ]**Push.
10. Collez la clé de serveur dans le champ de clé de serveur.

Si tout se passe bien, vous devriez voir un message SUCCESS.

![push-canal-settings](assets/push-channel-settings.PNG)

En résumé, nous avons créé un [!DNL Android App] et connecté le [!DNL Android App] avec [!DNL Firebase]. Nous avons ensuite connecté l’application mobile en Adobe Campaign avec l’application [!DNL Android App] en collant la clé de serveur de l’ [!DNL Android] application dans l’application mobile en Adobe Campaign Standard.
