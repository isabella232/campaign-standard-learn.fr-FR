---
title: Etape 2 - Intégration du SDK mobile
description: Dans cette partie, nous allons intégrer l'application Android à Mobile SDK. Pour intégrer le SDK mobile à l’application Android
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# ÉTAPE 2 - Intégration du SDK  mobile avec l’application Android

Dans cette partie, nous allons intégrer l’ [!DNL Android] application à [!UICONTROL Mobile SDK]. Pour intégrer le SDK  mobile à l’ [!DNL Android] application, procédez comme suit :

* Ouvrez le projet *ACSPushTutorial* dans [!DNL Android Studio]
* Créez une nouvelle classe java appelée *MainApp* qui s’étend [!DNL android.app.Application]
* La structure de votre projet à ce stade doit ressembler à la suivante

![application principale](assets/android-main-app.PNG)

* Développez le [!DNL Gradle Scripts] dossier. Doublon cliquez sur le [!DNL build.gradle] du module. Collez les dépendances suivantes dans la section des dépendances du [!DNL build.gradle] fichier. Votre [!DNL build.gradle] fichier doit maintenant ressembler à celui-ci ci-dessous.

```java{.line-numbers}
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![niveau module](assets/module-build-gradle.PNG)

* Synchronisez votre [!DNL Android] projet en cliquant sur le bouton Synchroniser maintenant pour synchroniser votre projet.

## Modify [!DNL AndroidManifest.xml]{#modify-android-manifest}

Ouvrez *AndroidManifest.xml* et collez les 2 lignes suivantes après l’élément manifest et avant l’élément d’application. Cela permet à votre application de communiquer avec un monde extérieur

```xml{.line-numbers}
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copiez la ligne suivante dans l’élément[!DNL android:name=".MainApp"]de l’application Enregistrez votre [!DNL AndroidManifest.xml]image [!DNL AndroidManifest.xml] de base.

```xml{.line-numbers}
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
