---
description: Bouw het trekkrachteindpunt om aan verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.
title: Het eindpunt van de trek opbouwen
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Het volledige eindpunt opbouwen{#build-the-pull-endpoint}

Bouw het trekkrachteindpunt om aan verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.

1. Maak een HTTPS-eindpunt dat LiveCycle-verzoeken ontvangt en reageert met een JSON-object dat de meest recente gebruikersgegevens bevat.

   >[!NOTE]
   >
   >Dit eindpunt moet toegankelijk zijn. Ook wordt ten zeerste aanbevolen zowel verzoeken als antwoorden via het HTTPS-protocol te verzenden.

1. Registreer het Eindpunt met Studio.
