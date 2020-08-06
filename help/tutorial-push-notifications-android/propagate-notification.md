---
title: Étape 5 - Propagation des notifications
description: Dans cette partie, nous allons propager le message reçu d'Adobe Campaign à l'aide d'Android Notification Manager.Firebase
feature: Push
topics: Mobile
kt: 4829
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: c3ff1a137fb8ee9506a11f82e1a27d010bbd97e6
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Ajouter le service à envoyer une notification

Dans cette partie, nous propagerons le message reçu de Adobe Campaign en utilisant [!DNL Android Notification Manager]. [!DNL Notification manager] sert à informer l’utilisateur des événements qui se produisent.
Voici comment vous dites à l&#39;utilisateur que quelque chose s&#39;est passé en arrière-plan :

* Lancement [!DNL Android Studio]
* Ouvrir le *[!DNL ACSPushTutorial]* projet
* Développer la structure du projet
* Cliquez avec le bouton droit sur le dossier du package ([!DNL com.example.acspushtutorial]) et [!DNL New ->Java Class]
* Nommer cette classe *[!DNL MyService]* et s&#39;assurer qu&#39;elle s&#39;étend [!DNL FirebaseMessagingService]
* Créez *[!DNL sendNotification]* une méthode dans cette classe. Dans cette méthode, vous devez définir le contenu et le canal de la notification à l’aide d’un [!DNL NotificationCompat.Builder] objet. Pour faire apparaître la notification, appelez [!DNL NotificationManagerCompat.notify()]et transmettez-lui un identifiant unique pour la notification et le résultat de [!DNL NotificationCompat.Builder.build()].

```java
package com.example.pushmessaging;
import android.app.NotificationChannel;
import android.app.NotificationManager;
import android.app.PendingIntent;
import android.content.Context;
import android.content.Intent;
import android.media.RingtoneManager;
import android.net.Uri;
import android.os.Build;
import android.util.Log;

import androidx.core.app.NotificationCompat;

import com.google.firebase.messaging.FirebaseMessagingService;
import com.google.firebase.messaging.RemoteMessage;

import java.util.Map;

public class MyService extends FirebaseMessagingService {
@Override
public void onMessageReceived(RemoteMessage remoteMessage)
{
Map<String,String> data  = remoteMessage.getData();
Log.d("data payload: ", data.toString());
sendNotification(remoteMessage);
}


private void sendNotification(RemoteMessage message) {
Intent intent = new Intent(this, MainActivity.class);
intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
PendingIntent pendingIntent = PendingIntent.getActivity(this, 0 /* Request code */, intent, PendingIntent.FLAG_ONE_SHOT);

String channelId = "0";
Uri defaultSoundUri = RingtoneManager.getDefaultUri(RingtoneManager.TYPE_NOTIFICATION);
NotificationCompat.Builder notificationBuilder =
        new NotificationCompat.Builder(this, channelId)
                .setSmallIcon(R.drawable.ic_launcher_background)
                .setContentTitle("Message from AEM")
                .setContentText(message.getData().get("body"))
                .setAutoCancel(true)
                .setSound(defaultSoundUri)
                .setContentIntent(pendingIntent);

NotificationManager notificationManager =
        (NotificationManager) getSystemService(Context.NOTIFICATION_SERVICE);

// Since android Oreo notification channel is needed.
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
    NotificationChannel channel = new NotificationChannel(channelId,
            "Channel human readable title",
            NotificationManager.IMPORTANCE_DEFAULT);
    notificationManager.createNotificationChannel(channel);
}

notificationManager.notify(0 /* ID of notification */, notificationBuilder.build());
}
}
```

## Modify [!DNL AndroidManifest.xml]

Ajoutez le service qui a été créé pour vous [!DNL AndroidManifest.xml]. La finale [!DNL AndroidManifest.xml] doit se présenter comme suit :

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.pushmessaging">

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
        <service
            android:name=".MyService"
            android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.MESSAGING_EVENT" />
            </intent-filter>
        </service>

        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## Exécution de l’application

Exécutez l’application en cliquant sur la flèche **** verte dans la barre d’outils ou dans le [!DNL Run] menu.
