---
title: Étape 3 - Enregistrement des extensions avec votre application mobile
description: Dans cette partie, nous allons ajouter le code pour enregistrer les extensions UserProfile, Identity, Lifecycle et Signal.
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# Étape 3 - Enregistrement des extensions avec votre application mobile

Dans cette partie, nous allons ajouter le code pour enregistrer les extensions Profil utilisateur, Identité, Lifecycle et Signal. Ces extensions font partie de [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Nous devrons également enregistrer l&#39;extension Adobe Campaign Standard comme le montre le code ci-dessous.

Ouvrez votre projet en [!DNL Android] studio. Supprimez l&#39;intégralité du code dans MainApp, **à l&#39;exception de la première ligne qui correspond à l&#39;instruction** du pack.

Collez le code suivant dans MainApp.

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Ligne 32 vous devez fournir l&#39;ID de fichier d&#39;environnement de votre[!UICONTROL  propriété Launch] . Vous pouvez y accéder à partir de l’onglet  environnement de votre propriété [!UICONTROL Launch] .

![launch-id](assets/launch-id-property.PNG)
