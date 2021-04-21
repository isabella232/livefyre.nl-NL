---
description: Met LiveCycle Identity met LinkedIn kunnen gebruikers hun LinkedIn-aanmeldgegevens gebruiken voor de interactie tussen apps op uw site.
title: Een LinkedIn-app maken voor gebruik met LiveCyre-id
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Een LinkedIn-toepassing maken voor gebruik met LiveCyre-identiteit{#create-a-linkedin-app-for-use-with-livefyre-identity}

Met LiveCycle Identity met LinkedIn kunnen gebruikers hun LinkedIn-aanmeldgegevens gebruiken voor de interactie tussen apps op uw site.

Voor het inschakelen van LinkedIn-aanmelding vereist Livefyre de volgende LinkedIn-toepassingsgegevens:

* Consumentencode (API-sleutel)
* Consumentengeheim (API Secret)

Een LinkedIn-app maken voor gebruik met LiveCycle Identity:

1. Ga naar https://www.linkedin.com/secure/developer en meld u aan bij uw LinkedIn-account om een nieuwe of selecteer een bestaande app voor gebruik met LiveCycle Identity.
1. Klik op **[!UICONTROL Create Application]**.
1. Vul het formulier in om de toepassing te maken.
1. Schakel in **[!UICONTROL Default Application Permissions]** de toepassingsmachtigingen **[!UICONTROL r_basicprofile]** en **[!UICONTROL r_emailaddress]** in.
1. Voer **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** in als `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Sla de app op.
1. Schakel in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** de schakeloptie **[!UICONTROL Enable LinkedIn Login]** in op **[!UICONTROL On]**.
1. Voer de LinkedIn Client ID en LinkedIn Client Secret in.
1. Klik op **[!UICONTROL Save Settings]**.

Wanneer deze bewerking is voltooid, worden op de pagina met toepassingsdetails van LinkedIn de API-sleutel (Consumer Key) en het API-geheim (Consumer Secret) van de app vermeld voor gebruik op de pagina Integratie-instellingen van Studio.
