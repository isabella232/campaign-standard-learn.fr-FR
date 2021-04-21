---
title: ÉTAPE 4 - Définir l'identifiant de recherche
description: '**pushIdentifier** est une chaîne qui contient le jeton de périphérique pour les notifications Push. Il s’agit du même jeton envoyé par Firebase et transmis au SDK à l’aide de la méthode MobileCore.setPushIdentifier.'
feature: Push
topic: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
translation-type: tm+mt
source-git-commit: ddbb0843ea45a83d9ab5bfa0877287f6ba7d6210
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Étape 4 - Définir [!DNL pushidentifier]

**[!DNL pushidentifier]** est une chaîne qui contient le jeton de périphérique pour les notifications [!DNL Push]. Il s’agit du même jeton envoyé par [!DNL Firebase] et transmis au SDK à l’aide de la méthode [!DNL MobileCore.setPushIdentifier].

Ouvrez votre projet dans [!DNL Android ]studio. Supprimez le code entier dans [!DNL MainActivity] **sauf la première ligne qui correspond à votre instruction de package**.

Collez le code suivant dans [!DNL MainActivity] :

<!--
Removed `{.line-numbers}` below
-->

```java
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
* L&#39;émulateur [!DNL Android] doit être début et votre application doit s&#39;exécuter avec [!DNL "Hello World" ]texte.
* Ouvrez la fenêtre [!DNL logcat]. Recherchez &quot;[!DNL Got]&quot;. Vous devriez voir le jeton reçu de [!DNL Firebase] écrit dans le journal comme illustré ci-dessous. La chaîne longue après &quot;[!DNL Got token]&quot; est la [!DNL pushidentifier ]qui est envoyée à Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Vérifier les abonnés aux applications mobiles

Connectez-vous à votre instance Adobe Campaign Standard.
Accédez à **[!UICONTROL Administration->Canaux->Mobile App(AEP SDK)]**. Ouvrez l’application mobile appropriée. Accédez à l&#39;onglet [!UICONTROL Abonnés aux applications mobiles]. Un jeton d&#39;enregistrement doit s&#39;afficher.

![abonnés-applications-mobiles](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Si vous ne voyez pas de jeton d&#39;enregistrement dans l&#39;onglet [!UICONTROL Abonnés d&#39;applications mobiles] ARRÊTEZ ici avant de poursuivre.
