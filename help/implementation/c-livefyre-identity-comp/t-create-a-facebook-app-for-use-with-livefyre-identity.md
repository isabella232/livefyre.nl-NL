---
description: Met LiveCycle Identity met Facebook kunt u gebruikers toestaan hun Facebook-aanmeldingen te gebruiken om te communiceren met Apps op uw site.
title: Een Facebook-app maken voor gebruik met LiveCyre-id
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Een Facebook-toepassing maken voor gebruik met LiveCyre-identiteit{#create-a-facebook-app-for-use-with-livefyre-identity}

Met LiveCycle Identity met Facebook kunt u gebruikers toestaan hun Facebook-aanmeldingen te gebruiken om te communiceren met Apps op uw site.

Om uw gebruikers in staat te stellen zich aan te melden met hun Facebook-gebruikersgegevens, vereist LiveCyre de volgende Facebook-toepassingsgegevens:

* Toepassings-id
* App Secret

Een Facebook-app maken voor gebruik met LiveCycle Identity:

1. Ga naar [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Meld u aan bij uw Facebook-ontwikkelaarsaccount.
1. Klik **[!UICONTROL Add New App]** of selecteer een bestaande App voor gebruik met de Identiteit van het Leven.
1. Klik **[!UICONTROL Settings]**, dan **[!UICONTROL Basic]**. Voer een **[!UICONTROL Contact Email]**-adres, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** en **[!UICONTROL Terms of Service URL]** in.
1. Klik op het plusteken ( **[!UICONTROL +]**) naast **[!UICONTROL Products]**.
1. Klik op **[!UICONTROL Set Up]** onder **[!UICONTROL Facebook Login]**.
1. Klik op **[!UICONTROL Settings]** en stel het volgende in:

   * Stel **[!UICONTROL Client OAuth Login]** in op **[!UICONTROL Yes]**.
   * Stel **[!UICONTROL Web OAuth Login]** in op **[!UICONTROL Yes]**.
   * Stel **[!UICONTROL Use Strict Mode for Redirect URIs]** in op **[!UICONTROL Yes]**.
   * Stel **[!UICONTROL Enforce HTTPS for Web OAuth Login]** in op **[!UICONTROL Yes]**.
   * Voeg onder **[!UICONTROL Valid OAuth redirect URLs]** de URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` toe (waarbij `{networkName}` uw door Livefy verschafte netwerknaam is).

1. Onder **[!UICONTROL App Review]**:

   * Maak de app openbaar.
   * Zorg ervoor dat **[!UICONTROL Approved Items]** voor **[!UICONTROL Login Permissions]** `email`, `public_profile`, en `user_friends` omvat.

Als de bewerking is voltooid, worden de toepassings-id en het toepassingsgeheim vermeld op de pagina van het dashboard van de Facebook-ontwikkelaar voor gebruik in de integratie-instellingen van Studio.
