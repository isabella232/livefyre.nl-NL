---
description: U kunt Livefyre Identity gebruiken met Yahoo! om gebruikers toe te staan hun Yahoo te gebruiken! meldt zich aan om te communiceren met Apps op uw site.
seo-description: U kunt Livefyre Identity gebruiken met Yahoo! om gebruikers toe te staan hun Yahoo te gebruiken! meldt zich aan om te communiceren met Apps op uw site.
seo-title: Maak een Yahoo! Toepassen voor gebruik met livefyre-id
solution: Experience Manager
title: Maak een Yahoo! Toepassen voor gebruik met livefyre-id
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Maak een Yahoo! Toepassen voor gebruik met livefyre-id{#create-a-yahoo-app-for-use-with-livefyre-identity}

U kunt Livefyre Identity gebruiken met Yahoo! om gebruikers toe te staan hun Yahoo te gebruiken! meldt zich aan om te communiceren met Apps op uw site.

Uw gebruikers kunnen zich alleen aanmelden met hun Yahoo-referenties als Livefyre de volgende Yahoo App-gegevens heeft:

* Client ID (Consumentencode)
* Clientgeheim (Consumentengeheim)

Een Yahoo maken! app voor gebruik met LiveCycle Identity:

1. Ga naar [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)en meld u aan bij uw Yahoo! een nieuwe account maken of een bestaande app selecteren voor gebruik met LiveCycle Identity.
1. Selecteer **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Selecteer **[!UICONTROL API Permissions: Profiles (Social Directory)]** en **[!UICONTROL Read Public]**.

   Wanneer deze bewerking is voltooid, wordt op de pagina met toepassingsdetails van Yahoo de client-id (Consumer Key) en de clientgeheim (Consumer Secret) vermeld voor gebruik op de pagina Integratie-instellingen van Studio.

   >[!NOTE]
   >
   >Als u Yahoo inschakelt! aanmelden zonder Yahoo te maken! en als u de velden Client ID en Client Secret in Studio leeg laat, gebruikt LiveCyre OpenID om deze gebruikers aan te melden bij uw LiveCyre-apps. OAuth en aangepaste branding zijn in dit geval niet beschikbaar.