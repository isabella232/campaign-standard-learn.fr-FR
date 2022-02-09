---
title: Étape 1 - Création d’une application Android et configuration pour utiliser Firebase Cloud Messaging
description: Dans cette partie, nous allons créer [!DNL Android] Application à recevoir [!UICONTROL Notifications push] envoyé depuis Adobe Campaign Standard. Pour recevoir les notifications push, l’application doit être enregistrée auprès de Google. [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# Etape 1 - Créer [!DNL Android] Application et configuration à utiliser [!DNL Firebase Cloud Messaging]

Dans cette partie, vous allez créer [!DNL Android] Application à recevoir [!UICONTROL Notifications push] envoyé depuis Adobe Campaign Standard. Pour recevoir les notifications push, l’application doit être enregistrée auprès de Google. [!DNL Firebase Cloud Service].

1. Connectez-vous à votre [!DNL Firebase] compte .

   [!DNL Firebase] est une plateforme mobile Google qui vous aide à développer rapidement des applications de haute qualité. Si vous n’avez pas de [!DNL Firebase] compte, créez-en un. [ici](https://firebase.google.com).

2. Lancer [!DNL Android Studio]
3. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Nouveau]** > **[!UICONTROL Nouveau projet].**
4. Sélectionner **[!UICONTROL Activité vide]** et cliquez sur **[!UICONTROL Suivant].**

   ![android-project](assets/android-project.PNG)

5. Attribuez un nom significatif au projet.

   Pour les besoins de cette démonstration, nous avons nommé notre projet *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acceptez les noms de packages par défaut et cliquez sur **[!DNL Finish]** pour créer votre projet.
7. La structure de votre projet doit ressembler à la capture d’écran ci-dessous.

   ![android-project-structure](assets/android-project-structure.PNG)

8. Cliquez sur **[!UICONTROL Outils]** > **[!UICONTROL Firebase].** (cela ajoute le projet à [!DNL Firebase])
9. Cliquez sur **[!UICONTROL Configuration de Firebase Cloud Messaging].**

   ![configuration de firebase](assets/android-project-firebase-messaging.PNG)

10. Cliquez sur **[!UICONTROL Connexion à Firebase].**
11. Une fois votre application connectée à Firebase, cliquez sur **[!UICONTROL Ajout de FCM à votre application].**
12. Cliquez sur **[!UICONTROL Accepter les modifications].**

   Lorsque vous ajoutez FCM à votre application, l’assistant a besoin de votre autorisation pour apporter des modifications à votre projet.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Une fois l’intégration de votre application avec Firebase réussie, vous devriez recevoir un message comme celui illustré ci-dessous :

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Assurez-vous que votre projet est répertorié dans [!DNL Firebase ]console](https://console.firebase.google.com/)

## Configurer [!UICONTROL Canal push] Paramètres

1. Connectez-vous à [!DNL Firebase] console
2. Ouvrez le **[!UICONTROL ACSPushTutorial]** projet.
3. Cliquez sur le bouton **icône d’engrenage** et ouvrez les paramètres du projet.

   ![project-settings](assets/firebase-project-settings.PNG)

4. Pour **[!UICONTROL Cloud Messaging]** .
5. Copiez la clé du serveur

   ![server-key](assets/firebase-server-key.PNG)

6. Connexion à votre instance Adobe Campaign Standard
7. Cliquez sur **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Application mobile].**
8. Sélectionnez les **[!UICONTROL Propriété de l’application mobile].**
9. Cliquez sur le bouton **[!DNL Android]icon** dans le **[!UICONTROL Paramètres du canal push]** .
10. Collez la clé du serveur dans le champ Clé du serveur .

Si tout se passe bien, un message SUCCESS s’affiche.

![push-channel-settings](assets/push-channel-settings.PNG)

Pour résumer, nous avons créé une [!DNL Android App] et connecté au [!DNL Android App] avec [!DNL Firebase]. Nous avons ensuite connecté l’application mobile dans Adobe Campaign à l’aide de la variable [!DNL Android App] en collant le [!DNL Android] Clé du serveur de l’application dans l’application mobile dans Adobe Campaign Standard.
