---
description: Voeg de markering userPrivacyOptOut toe aan de pagina zodat een sitebezoeker zich kan afmelden voor deze tracering.
seo-description: Voeg de markering userPrivacyOptOut toe aan de pagina zodat een sitebezoeker zich kan afmelden voor deze tracering.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

Voeg de `userPrivacyOptOut` vlag aan de pagina toe zodat een bezoeker van de site zich kan afmelden voor deze tracering.

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

1. Voeg de `userPrivacyOptOut` markering toe aan de pagina vóór het `Livefyre.js` JavaScript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Voeg ergens na `Livefyre.js` de pagina toe `userPrivacyOptOut`.

   Livefyre Apps instantiëren met de verhoogde privacymontages.

   >[!NOTE]
   >
   >Wijzig de waarde van `userPrivacyOptOut` zodra LiveCycle Apps is geladen niet.

Zorg ervoor dat in de toestemmingsworkflow de waarde true wordt ingesteld `userPrivacyOptOut` als een bezoeker van de site de optie Weigeren kiest.
