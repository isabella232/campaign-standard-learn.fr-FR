---
title: ÉTAPE 4 - Définition de l’identifiant push
description: '**pushIdentifier** est une chaîne contenant le jeton de l’appareil pour les notifications push. Il s’agit du même jeton envoyé par Firebase et transmis au SDK à l’aide de la méthode MobileCore.setPushIdentifier .'
feature: Push
user: Admin
level: Experienced
jira: KT-4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 757afce50981b96b7820c987308d639a73746c0c
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Étape 4 - Définir [!DNL pushidentifier]

La variable **[!DNL pushidentifier]** est une chaîne contenant le jeton d’appareil pour [!DNL Push] notifications. Il s’agit du même jeton envoyé par [!DNL Firebase] et est transmis au SDK à l’aide de la variable [!DNL MobileCore.setPushIdentifier] .

Ouvrez votre projet dans [!DNL Android™]studio. Supprimer l’intégralité du code dans [!DNL MainActivity] **à l’exception de la première ligne qui correspond à votre instruction de package.**.

Collez le code suivant dans [!DNL MainActivity]:

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

## Test de votre application

C’est le bon moment pour tester votre application, avant d’aller plus loin.

* Exécutez votre application en cliquant sur la flèche verte ou sélectionnez **[!DNL Run->Run'app']**.
* La variable [!DNL Android™] L’émulateur doit commencer et votre application doit s’exécuter avec [!DNL "Hello World"]texte.
* Ouvrez le [!DNL logcat] fenêtre. Recherchez &quot;[!DNL Got]&quot;. Vous devriez voir le jeton reçu de [!DNL Firebase] écrit dans le journal comme illustré ci-dessous. La longue chaîne après &quot;[!DNL Got token]&quot; correspond à la variable [!DNL pushidentifier]envoyé à Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Vérifier les abonnés aux applications mobiles

Connectez-vous à votre instance Adobe Campaign Standard.
Naviguer **[!UICONTROL Administration -> Canaux -> Application mobile (SDK Experience Platform)]**. Ouvrez l’application mobile appropriée. Pour [!UICONTROL Abonnés aux applications mobiles] . Vous devriez voir une [!UICONTROL jeton d&#39;enregistrement]répertorié.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Si vous ne voyez pas de jeton d’enregistrement dans la variable [!UICONTROL Abonnés aux applications mobiles] Cliquez sur STOP ici avant de poursuivre.
