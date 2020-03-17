---
description: Bouw de structuur van het trekkingsverzoek om verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.
seo-description: Bouw de structuur van het trekkingsverzoek om verzoeken om toegang tot uw systeem van de gebruikersidentiteit te ontvangen en te antwoorden.
seo-title: Pull Request Structure
solution: Experience Manager
title: Pull Request Structure
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

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

waar `lftoken` is een Symbolisch van het Web JSON dat met uw netwerksleutel wordt ondertekend, en **[!UICONTROL {userAuthToken}]** is het symbolische teken van de gebruikersauteur dat door Livefyre wordt geproduceerd.

1. Gebruik `lftoken` om te bevestigen dat de verzoeken aan uw Ping voor Pull URL door Livefyre en niet een kwaadwillige agent werden verzonden.
1. Voor alle binnenkomende aanvragen:

   * Zorg ervoor dat de `lftoken` queryreeks aanwezig is op het verzoek.
   * Gebruik de `validateLivefyreToken` methode in de bibliotheken van de Livefy om ervoor te zorgen dat met uw Sleutel van het Netwerk `lftoken` werd ondertekend.

   * Als `lftoken` niet aanwezig is, of geen bevestiging ontbreekt, sta uw eindpunt niet toe om met profielinformatie te antwoorden. Reageer in plaats daarvan met een 403 (Verboden) statuscode en geen reactielichaam.

1. `userAuthToken` wordt gegenereerd door de Livefyre- `buildUserAuthToken` methode voor de gebruiker, met user-id &quot;system&quot;. Deze gebruiker is de eerste gebruiker die voor elk nieuw netwerk wordt gecreeerd.
