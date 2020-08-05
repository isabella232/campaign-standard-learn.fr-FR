---
title: ÉTAPE 4 - Définir l'identifiant de recherche
description: '**pushIdentifier** est une chaîne qui contient le jeton de périphérique pour les notifications Push. Il s’agit du même jeton envoyé par Firebase et transmis au SDK à l’aide de la méthode MobileCore.setPushIdentifier.'
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Étape 4 - Définition [!DNL pushidentifier]

Il **[!DNL pushidentifier]** s’agit d’une chaîne contenant le jeton de périphérique pour les [!DNL Push] notifications. Il s’agit du même jeton qui est envoyé par [!DNL Firebase] et transmis au SDK à l’aide de la [!DNL MobileCore.setPushIdentifier] méthode.

Ouvrez votre projet en [!DNL Android ]studio. Supprimez l&#39;intégralité du code dans, [!DNL MainActivity] à l&#39; **exception de la première ligne qui correspond à votre instruction** de package.

Collez le code suivant dans [!DNL MainActivity]:

```java{.line-numbers}
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## Tester votre application

C&#39;est le bon moment pour tester votre application, avant d&#39;aller plus loin.

* Exécutez votre application en cliquant sur la flèche verte ou sélectionnez **[!DNL Run->Run'app']**.
* L’ [!DNL Android] émulateur doit être début et votre application doit s’exécuter avec [!DNL "Hello World" ]du texte.
* Ouvrez la [!DNL logcat] fenêtre. Recherchez &quot;[!DNL Got]&quot;. Vous devriez voir le jeton qui a été reçu de [!DNL Firebase] écrit dans le journal comme illustré ci-dessous. La longue chaîne après &quot;[!DNL Got token]&quot; est celle [!DNL pushidentifier ]qui est envoyée à Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Vérifier les abonnés aux applications mobiles

Connectez-vous à votre instance Adobe Campaign Standard.
Accédez à **[!UICONTROL Administration->Canaux->Application mobile(SDK AEP)]**. Ouvrez l’application mobile appropriée. Accédez à l’onglet Abonnés [!UICONTROL aux applications] mobiles. Un jeton [!UICONTROL d’enregistrement doit s’afficher ]dans la liste.

![abonnés-applications-mobiles](assets/mobile-application-subscribers.PNG)

>[REMARQUE]
>
>Si vous ne voyez pas de jeton d’enregistrement dans l’onglet Abonnés [!UICONTROL d’applications] mobiles, ARRÊTEZ ici avant de poursuivre.
