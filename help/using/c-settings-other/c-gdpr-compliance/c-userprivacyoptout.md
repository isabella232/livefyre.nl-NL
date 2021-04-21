---
description: Voeg de markering userPrivacyOptOut toe aan de pagina zodat een sitebezoeker zich kan afmelden voor deze tracering.
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

Voeg de markering `userPrivacyOptOut` toe aan de pagina zodat een sitebezoeker deze tracering kan uitschakelen.

LiveCycle biedt JavaScript-gebeurtenissen om de gebruikersactiviteit in uw LiveCycle-apps te volgen.

Als u LiveCycle Apps insluit en een bezoeker niet akkoord gaat met bijhouden, kunt u LiveCycle dynamisch configureren om functionaliteit uit te schakelen om de privacy van de bezoeker te garanderen.

Indien geconfigureerd, zal Livefyre:

* Schakel verificatieondersteuning in Apps uit.
* Livecount en het genereren van gebeurtenissen uitschakelen
* Bestaande cookies verwijderen die zijn gemaakt door apps die op de pagina staan
* Proxymedia met afbeeldingen van domeinen van derden om te voorkomen dat derden cookies maken
* Doorklikken van videomasker inschakelen voor video&#39;s van derden waarvoor een extra klik nodig is

## Een pagina configureren voor Uitschakelen

Integraties die LiveCycle Apps insluiten kunnen LiveCycle configureren wanneer een bezoeker van de site geen toestemming heeft verleend met behulp van één JavaScript-variabele.

Instructies:

1. Voeg de markering `userPrivacyOptOut` toe aan de pagina vóór het JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Voeg `Livefyre.js` aan de pagina toe overal na `userPrivacyOptOut`.

   Livefyre Apps instantiëren met de verhoogde privacymontages.

   >[!NOTE]
   >
   >Wijzig de waarde van `userPrivacyOptOut` niet als LiveCycle Apps zijn geladen.

Zorg ervoor dat in uw toestemmingsworkflow de `userPrivacyOptOut` op true wordt ingesteld als een sitebezoeker ervoor kiest om te weigeren.
