---
description: Als u aanmelden via een sociaal netwerk wilt inschakelen, gebruikt u Studio om de referenties van uw sociale apps toe te voegen aan uw LiveCycle-integratie en past u de aanmeldingsmodus aan.
seo-description: Als u aanmelden via een sociaal netwerk wilt inschakelen, gebruikt u Studio om de referenties van uw sociale apps toe te voegen aan uw LiveCycle-integratie en past u de aanmeldingsmodus aan.
seo-title: Studio gebruiken om uw sociale toepassingen te verbinden met uw LiveCycle-implementatie
title: Studio gebruiken om uw sociale toepassingen te verbinden met uw LiveCycle-implementatie
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Studio gebruiken om uw sociale toepassingen te verbinden met uw LiveCycle-implementatie{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Als u aanmelden via een sociaal netwerk wilt inschakelen, gebruikt u Studio om de referenties van uw sociale apps toe te voegen aan uw LiveCycle-integratie en past u de aanmeldingsmodus aan.

## Het aanpassen van Login Modal {#section_v4c_hv2_3z}

Met de aanmeldingsmodus kunt u de gegevens aanpassen die uw gebruikers zien wanneer ze zich aanmelden bij uw apps. U kunt het modale venster aanpassen.

* **Logo:** Upload een logo voor gebruik in uw aanmeldingsmodellen.
* **Lettertypefamilie:** Selecteer een lettertype dat overeenkomt met uw merk.
* **Kleur merk:** Voer een hexadecimale kleur in die moet worden gebruikt voor specifieke tekst in het modaal.
* **URL van voorwaarden en bepalingen:** Voer de URL in voor de pagina Voorwaarden en bepalingen van uw bedrijf. Dit veld is vereist voor gebruik met LiveCycle Identity.

## Livefyre-identiteit omzetten {#section_xxt_z52_3z}

U kunt vertaalsets voor tekstreeksen maken en wijzigen in LiveCycle Identity.

Zie Vertaalsets voor meer informatie over het gebruik van vertaalsets met LiveCycle Identity.

Zie Livefyre Identity voor meer informatie over de specifieke tekenreeksen die u kunt aanpassen voor LiveY Identity.

## Aanmelding via e-mail inschakelen {#section_dlv_wzt_bbb}

Gebruikers toestaan hun e-mailadressen te gebruiken om zich aan te melden bij en te communiceren met Apps op uw site.

Aanmelden met een native Livefyre-account inschakelen:

1. Navigeer naar **[!UICONTROL Integration Settings]** in LiveCyre Studio.
1. Schakel de **[!UICONTROL Enable Login with Email]** schakeloptie naar **[!UICONTROL On]**.

## Aanmelden met een Facebook-account inschakelen {#section_ph3_515_bbb}

Sluit uw Facebook-account aan op Livefyre zodat gebruikers hun Facebook-aanmeldingen kunnen gebruiken om te communiceren met Apps op uw site.

Aanmelden met een Facebook-account inschakelen:

1. Schakel de **[!UICONTROL Enable Login with Facebook]** schakeloptie naar **[!UICONTROL ON]**.

1. Voeg uw Facebook-app **[!UICONTROL App ID]** en **[!UICONTROL App Secret]**.

   Deze waarden worden vermeld in het dashboard voor Facebook-ontwikkelaars voor de app, beschikbaar op [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Aanmelden met Google inschakelen {#section_fq3_kb5_bbb}

Sluit uw Google+-account aan op Livefyre zodat gebruikers hun Google+-aanmeldgegevens kunnen gebruiken om te communiceren met Apps op uw site.

Aanmelden met een Google+-account inschakelen:

1. Schakel de **[!UICONTROL Enable Login with Google]** schakeloptie naar **[!UICONTROL ON]**.

1. Voeg de toepassingen **[!UICONTROL Client ID]** en **[!UICONTROL Client secret]** van Google toe.

   Deze waarden staan vermeld in uw projectinterface van het Google Cloud-platform, beschikbaar op [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Ga naar **[!UICONTROL API Manager > Credentials]** en klik op de projectnaam om deze informatie op te halen.

## Aanmelden met een Twitter-account inschakelen {#section_iyz_wb5_bbb}

Sluit uw Twitter-account aan op Livefyre zodat gebruikers hun Twitter-aanmeldingen kunnen gebruiken om te communiceren met Apps op uw site.

Aanmelden met een Twitter-account inschakelen:

1. Schakel de **[!UICONTROL Enable Login with Twitter]** schakeloptie naar **[!UICONTROL ON]**.

1. Voeg de Twitter-app **[!UICONTROL Consumer Key (API Key)]** en **[!UICONTROL Consumer Secret (API Secret)]**.

   Deze waarden staan op de **[!UICONTROL Keys and Access Tokens]** pagina van de Twitter-app, die u kunt vinden op [https://apps.twitter.com/](https://apps.twitter.com/).

## Aanmelding inschakelen met een Yahoo! Account {#section_s1q_3c5_bbb}

Verbind uw Yahoo! account aan Livefyre om gebruikers toe te staan hun Yahoo te gebruiken! meldt zich aan om te communiceren met Apps op uw site.

Aanmelden met een Yahoo inschakelen! account:

1. Schakel de **[!UICONTROL Enable Login with Yahoo!]** schakeloptie naar **[!UICONTROL ON]**.

1. Voeg je Yahoo toe! van de toepassing **[!UICONTROL Client ID]** en **[!UICONTROL Client Secret]**.

   Deze waarden staan in Yahoo! pagina met toepassingsdetails, beschikbaar op [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Aanmelden met een Microsoft Live-account inschakelen {#section_z42_4c5_bbb}

Sluit uw Microsoft Live-id-account aan op LiveCycle zodat gebruikers hun Microsoft Live-id-aanmeldingen kunnen gebruiken voor interactie met Apps op uw site.

Aanmelden met een Microsoft Live ID-account inschakelen:

1. Schakel in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, de **[!UICONTROL Enable Microsoft Live Login]** schakeloptie in op **[!UICONTROL On]**.

1. Voer de **[!UICONTROL Microsoft Live Client ID (Private Key)]** en **[!UICONTROL Microsoft Live Client Secret (Password)]** in.

1. Klik op **[!UICONTROL Save Settings]**.

   De **[!UICONTROL Microsoft Live Client ID (Private Key)]** en **[!UICONTROL Microsoft Live Client Secret (Password)]** waarden worden weergegeven op de pagina met details voor de Microsoft Live-id-toepassing.

## Sluit uw sociale apps aan op uw levensidentiteit {#section_on2_vc5_bbb}

Laat uw gebruikers toe om uw implementatie van de Identiteit van het Leven voor apps op uw plaats te gebruiken.

1. Maak een app.
1. Ga naar **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**.

1. Voer de vereiste App-referenties in voor de app die u hebt gemaakt.