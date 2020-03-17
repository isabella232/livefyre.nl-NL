---
description: Bouw het trekkrachteindpunt om aan verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.
seo-description: Bouw het trekkrachteindpunt om aan verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.
seo-title: Het eindpunt van de trek opbouwen
solution: Experience Manager
title: Het eindpunt van de trek opbouwen
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Het eindpunt van de trek opbouwen{#build-the-pull-endpoint}

Bouw het trekkrachteindpunt om aan verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.

1. Maak een HTTPS-eindpunt dat LiveCycle-verzoeken ontvangt en reageert met een JSON-object dat de meest recente gebruikersgegevens bevat.

   >[!NOTE]
   >
   >Dit eindpunt moet toegankelijk zijn. Ook wordt ten zeerste aanbevolen zowel verzoeken als antwoorden via het HTTPS-protocol te verzenden.

1. Registreer het Eindpunt met Studio.
