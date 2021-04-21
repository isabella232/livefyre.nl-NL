---
description: Met LiveCycle Identity met Microsoft Live Identity kunt u gebruikers in staat stellen hun Facebook-aanmeldingen te gebruiken voor het communiceren van toepassingen op uw site.
title: Een Microsoft Live Identity-app maken voor gebruik met LiveCyre-identiteit
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Een Microsoft Live Identity-app maken voor gebruik met LiveCyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Met LiveCycle Identity met Microsoft Live Identity kunt u gebruikers in staat stellen hun Facebook-aanmeldingen te gebruiken voor het communiceren van toepassingen op uw site.

Om gebruikers in staat te stellen zich aan te melden met hun Microsoft Live Identity-referenties, hebt u de volgende Microsoft Live-identiteitsgegevens nodig:

* Client-id (persoonlijke sleutel)
* Clientgeheim (wachtwoord)

Een Microsoft Live Identity-app maken voor gebruik met LiveCycle Identity:

1. Maken of aanmelden bij een Microsoft Live-account op [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Maak een nieuwe of selecteer een bestaande app voor gebruik met LiveCycle Identity.
1. Klik **[!UICONTROL Add Platform]**, dan selecteer Web als platformtype.
1. Controleer of de optie **[!UICONTROL Allow Implicit Flow]** is ingeschakeld en voer de URL omleiden in in plaats van {network-name} met uw netwerknaam: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Genereer een nieuw wachtwoord/sleutelpaar om de Persoonlijke Sleutel te krijgen.
1. Schakel in **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]** de schakeloptie **[!UICONTROL Enable Microsoft Live Login]** in op **[!UICONTROL On]**.
1. Voer de Microsoft Live Client-id en de Microsoft Live Client-geheim in.
1. Klik op **[!UICONTROL Save Settings]**.

Als deze bewerking is voltooid, wordt op de pagina met toepassingsdetails van Microsoft Live Identity de client-id (Consumer Key) en de Client Secret (Consumer Secret) van de app vermeld voor gebruik op de pagina Integratie-instellingen van Studio.
