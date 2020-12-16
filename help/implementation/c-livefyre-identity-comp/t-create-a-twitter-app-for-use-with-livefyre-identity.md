---
description: U kunt Livefyre Identity gebruiken met Twitter om gebruikers in staat te stellen hun Twitter-aanmeldingen te gebruiken voor het communiceren van apps op uw site.
seo-description: U kunt Livefyre Identity gebruiken met Twitter om gebruikers in staat te stellen hun Twitter-aanmeldingen te gebruiken voor het communiceren van apps op uw site.
seo-title: Een Twitter-app maken voor gebruik met LiveCyre-identiteit
solution: Experience Manager
title: Een Twitter-app maken voor gebruik met LiveCyre-identiteit
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Een Twitter-app maken voor gebruik met LiveCyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}

U kunt Livefyre Identity gebruiken met Twitter om gebruikers in staat te stellen hun Twitter-aanmeldingen te gebruiken voor het communiceren van apps op uw site.

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
