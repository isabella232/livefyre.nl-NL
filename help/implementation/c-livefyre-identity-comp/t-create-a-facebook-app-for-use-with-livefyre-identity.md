---
description: U kunt Livefyre Identity gebruiken met Facebook om gebruikers in staat te stellen hun Facebook-aanmeldingen te gebruiken om te communiceren met Apps op uw site.
seo-description: U kunt Livefyre Identity gebruiken met Facebook om gebruikers in staat te stellen hun Facebook-aanmeldingen te gebruiken om te communiceren met Apps op uw site.
seo-title: Een Facebook-app maken voor gebruik met LiveCyre-id
solution: Experience Manager
title: Een Facebook-app maken voor gebruik met LiveCyre-id
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Een Facebook-app maken voor gebruik met LiveCyre-id{#create-a-facebook-app-for-use-with-livefyre-identity}

U kunt Livefyre Identity gebruiken met Facebook om gebruikers in staat te stellen hun Facebook-aanmeldingen te gebruiken om te communiceren met Apps op uw site.

Om uw gebruikers in staat te stellen zich aan te melden met hun Facebook-gegevens, vereist Livefyre de volgende Facebook-toepassingsgegevens:

* Toepassings-id
* App Secret

Een Facebook-app maken voor gebruik met LiveCycle Identity:

1. Ga naar [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Meld u aan bij uw Facebook-ontwikkelaarsaccount.
1. Klik op **[!UICONTROL Add New App]** of selecteer een bestaande app voor gebruik met LiveCycle Identity.
1. Klik **[!UICONTROL Settings]** dan **[!UICONTROL Basic]**. Voer een **[!UICONTROL Contact Email]** adres in, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** en **[!UICONTROL Terms of Service URL]**.
1. Klik op het plusteken ( **[!UICONTROL +]**) naast **[!UICONTROL Products]**.
1. Klik op **[!UICONTROL Set Up]** onder **[!UICONTROL Facebook Login]**.
1. Klik op de volgende opties **[!UICONTROL Settings]** en stel deze in:

   * Instellen **[!UICONTROL Client OAuth Login]** op **[!UICONTROL Yes]**.
   * Instellen **[!UICONTROL Web OAuth Login]** op **[!UICONTROL Yes]**.
   * Instellen **[!UICONTROL Use Strict Mode for Redirect URIs]** op **[!UICONTROL Yes]**.
   * Instellen **[!UICONTROL Enforce HTTPS for Web OAuth Login]** op **[!UICONTROL Yes]**.
   * Voeg onder **[!UICONTROL Valid OAuth redirect URLs]** de URL toe `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (waar `{networkName}` de door Livefy geleverde netwerknaam is).

1. Onder **[!UICONTROL App Review]**:

   * Maak de app openbaar.
   * Zorg ervoor dat de **[!UICONTROL Approved Items]** instructies for **[!UICONTROL Login Permissions]** include, `email`, and `public_profile``user_friends`.

Wanneer deze bewerking is voltooid, wordt op de pagina Dashboard van de Facebook-ontwikkelaar de toepassings-id en het toepassingsgeheim vermeld voor gebruik in de Integratie-instellingen van Studio.
