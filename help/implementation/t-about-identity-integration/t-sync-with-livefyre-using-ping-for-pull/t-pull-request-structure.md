---
description: Bouw de structuur van het trekkingsverzoek om verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.
title: Pull Request Structure
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Pull Request Structure{#pull-request-structure}

Bouw de structuur van het trekkingsverzoek om verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.

Livefyre geeft een verzoek van de Pull aan uw eindpunt URL uit.

Bijvoorbeeld, als uw Pull eindpunt URL is:

```
https://example.yoursite.com/some_path/?id={id}
```

De Livefyre Pull-aanvraag voor dit eindpunt is:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

waarbij `lftoken` een JSON Web Token is die met uw netwerksleutel wordt ondertekend, en **[!UICONTROL {userAuthToken}]** is het gebruikerstoken dat door Livefyre wordt geproduceerd.

1. Gebruik `lftoken` om te bevestigen dat de verzoeken aan uw Ping voor Pull URL door Livefyre en niet een kwaadwillige agent werden verzonden.
1. Voor alle binnenkomende aanvragen:

   * Zorg ervoor dat de `lftoken` vraagkoord op het verzoek aanwezig is.
   * Gebruik de methode `validateLivefyreToken` in de bibliotheken van de Livefy om ervoor te zorgen dat `lftoken` met uw Sleutel van het Netwerk werd ondertekend.

   * Als `lftoken` niet aanwezig is, of bevestiging ontbreekt, sta uw eindpunt niet toe om met profielinformatie te antwoorden. Reageer in plaats daarvan met een 403 (Verboden) statuscode en geen reactielichaam.

1. `userAuthToken` wordt gegenereerd door de Livefyre- `buildUserAuthToken` methode voor de gebruiker, met gebruikersidentificatie &quot;system&quot;. Deze gebruiker is de eerste gebruiker die voor elk nieuw netwerk wordt gecreeerd.
