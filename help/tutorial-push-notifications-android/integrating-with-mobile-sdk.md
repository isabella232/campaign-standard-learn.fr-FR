---
title: Étape 2 - Intégration du SDK Mobile
description: Dans cette partie, nous allons intégrer l’application Android au SDK Mobile. Pour intégrer le SDK mobile à l’application Android
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# ÉTAPE 2 - Intégration [!UICONTROL SDK Mobile] avec l’application Android

Dans cette partie, nous intégrerons la [!DNL Android] application avec [!UICONTROL SDK Mobile]. Pour intégrer [!UICONTROL SDK mobile] avec le [!DNL Android] , procédez comme suit :

* Ouvrez le *ACSPushTutorial* project in [!DNL Android Studio]
* Créez une nouvelle classe java appelée *MainApp* qui étend [!DNL android.app.Application]
* À ce stade, la structure de votre projet doit ressembler à la suivante :

![main-app](assets/android-main-app.PNG)

* Développez l’objet [!DNL Gradle Scripts] dossier. Double-cliquez sur le bouton [!DNL build.gradle] du module . Collez les dépendances suivantes dans la section des dépendances de la fonction [!DNL build.gradle] fichier . Votre [!DNL build.gradle] doit maintenant ressembler à ce qui suit :

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* Synchronisez vos [!DNL Android] en cliquant sur le bouton Synchroniser maintenant pour synchroniser votre projet

## Modifier [!DNL AndroidManifest.xml]{#modify-android-manifest}

Ouvrir *AndroidManifest.xml* et collez les 2 lignes suivantes après l’élément manifest et avant l’élément application . Cela permet à votre application de communiquer avec le monde extérieur.

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copiez la ligne suivante dans l’élément application
[!DNL android:name=".MainApp"]
Enregistrez vos [!DNL AndroidManifest.xml]
Votre [!DNL AndroidManifest.xml] doit ressembler à ceci :

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
