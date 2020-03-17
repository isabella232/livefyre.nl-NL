---
description: Met LiveCycle Identity met Microsoft Live Identity kunt u gebruikers in staat stellen hun Facebook-aanmeldingen te gebruiken om toepassingen op uw site te interageren.
seo-description: Met LiveCycle Identity met Microsoft Live Identity kunt u gebruikers in staat stellen hun Facebook-aanmeldingen te gebruiken om toepassingen op uw site te interageren.
seo-title: Een Microsoft Live Identity-app maken voor gebruik met LiveCyre-identiteit
solution: Experience Manager
title: Een Microsoft Live Identity-app maken voor gebruik met LiveCyre-identiteit
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Een Microsoft Live Identity-app maken voor gebruik met LiveCyre-identiteit{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Met LiveCycle Identity met Microsoft Live Identity kunt u gebruikers in staat stellen hun Facebook-aanmeldingen te gebruiken om toepassingen op uw site te interageren.

Om gebruikers in staat te stellen zich aan te melden met hun Microsoft Live Identity-referenties, hebt u de volgende Microsoft Live-identiteitsgegevens nodig:

* Client-id (persoonlijke sleutel)
* Clientgeheim (wachtwoord)

Een Microsoft Live Identity-app maken voor gebruik met LiveCycle Identity:

1. Maken of aanmelden bij een Microsoft Live-account op [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Maak een nieuwe of selecteer een bestaande app voor gebruik met LiveCycle Identity.
1. Klik **[!UICONTROL Add Platform]** en selecteer vervolgens Web als het platformtype.
1. Controleer of de **[!UICONTROL Allow Implicit Flow]** optie is ingeschakeld en voer de URL voor omleiding in in plaats van {network-name} met uw netwerknaam: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Genereer een nieuw wachtwoord/sleutelpaar om de Persoonlijke Sleutel te krijgen.
1. Schakel in **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, de **[!UICONTROL Enable Microsoft Live Login]** schakeloptie in op **[!UICONTROL On]**.
1. Voer de Microsoft Live Client-id en de Microsoft Live Client-geheim in.
1. Klik op **[!UICONTROL Save Settings]**.

Als deze bewerking is voltooid, wordt op de pagina met toepassingsdetails van Microsoft Live Identity de client-id (Consumer Key) en de Client Secret (Consumer Secret) van de app vermeld voor gebruik op de pagina Integratie-instellingen van Studio.
