---
description: U kunt Livefyre Identiteit met LinkedIn gebruiken om gebruikers toe te staan om hun logins LinkedIn te gebruiken om Apps op uw plaats in wisselwerking te staan.
seo-description: U kunt Livefyre Identiteit met LinkedIn gebruiken om gebruikers toe te staan om hun logins LinkedIn te gebruiken om Apps op uw plaats in wisselwerking te staan.
seo-title: Een LinkedIn-toepassing maken voor gebruik met LiveCycle-identiteit
solution: Experience Manager
title: Een LinkedIn-toepassing maken voor gebruik met LiveCycle-identiteit
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Een LinkedIn-toepassing maken voor gebruik met LiveCycle-identiteit{#create-a-linkedin-app-for-use-with-livefyre-identity}

U kunt Livefyre Identiteit met LinkedIn gebruiken om gebruikers toe te staan om hun logins LinkedIn te gebruiken om Apps op uw plaats in wisselwerking te staan.

Voor het inschakelen van LinkedIn-aanmelding vereist LiveCycle de volgende LinkedIn-toepassingsgegevens:

* Consumentencode (API-sleutel)
* Consumentengeheim (API Secret)

Een LinkedIn-app maken voor gebruik met LiveCycle-identiteit:

1. Ga naar https://www.linkedin.com/secure/developer en meld u aan bij uw LinkedIn-account om een nieuwe of een bestaande app te maken voor gebruik met LiveID.
1. Klik op **[!UICONTROL Create Application]**.
1. Vul het formulier in om de toepassing te maken.
1. Schakel in de **[!UICONTROL Default Application Permissions]** app de machtigingen **[!UICONTROL r_basicprofile]** en de **[!UICONTROL r_emailaddress]** toepassingsmachtigingen in.
1. Voer de waarde in **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** als `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Sla de app op.
1. Schakel in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, de **[!UICONTROL Enable LinkedIn Login]** schakeloptie in op **[!UICONTROL On]**.
1. Ga LinkedIn identiteitskaart van de Cliënt en LinkedIn Geheim van de Cliënt in.
1. Klik op **[!UICONTROL Save Settings]**.

Wanneer deze bewerking is voltooid, wordt op de pagina met toepassingsdetails van LinkedIn de API-sleutel (Consumer Key) en het API-geheim (Consumer Secret) vermeld voor gebruik op de pagina Integratie-instellingen van Studio.
