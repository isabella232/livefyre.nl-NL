---
description: Met LiveCycle Identity met Twitter kunnen gebruikers hun Twitter-aanmeldgegevens gebruiken voor de interactie tussen apps op uw site.
title: Een Twitter-app maken voor gebruik met LiveCyre-id
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Een Twitter-toepassing maken voor gebruik met LiveCyre-identiteit{#create-a-twitter-app-for-use-with-livefyre-identity}

Met LiveCycle Identity met Twitter kunnen gebruikers hun Twitter-aanmeldgegevens gebruiken voor de interactie tussen apps op uw site.

Voor het inschakelen van Twitter-aanmelding vereist Livefyre de volgende Twitter-toepassingsgegevens:

* Consumentencode (API-sleutel)
* Consumentengeheim (API Secret)

Een Twitter-app maken voor gebruik met LiveCycle Identity:

1. Ga naar [https://apps.twitter.com/](https://apps.twitter.com/) en meld u aan bij uw Twitter-account om een nieuwe of een bestaande app te maken voor gebruik met LiveCycle Identity.
1. Via de pagina Instellingen voor de app:

   * Ga **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (waar **{networkName}** uw Livefyre verstrekte netwerknaam is. Bijvoorbeeld:** [!UICONTROL labs]* in **[!UICONTROL `labs.fyre.co`]**.)
   * Schakel **[!UICONTROL Enable Callback Locking]** uit.
   * Selecteer **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Selecteer **[!UICONTROL Access: Read only]** op het tabblad **[!UICONTROL Permissions]**.

Wanneer deze bewerking is voltooid, worden op de pagina Toepassingsbeheer > Toetsen en Toegangstokens van Twitter de Consumentencode (API-sleutel) en Consumentengeheim (API-geheim) van de app vermeld voor gebruik op de pagina Integratie-instellingen van Studio.
