---
description: De kernbibliotheek van Livefyre die wordt gebruikt om Livefyre op uw plaats aan te drijven.
title: Livefyre.js
exl-id: 82083dc0-3b4a-467c-bad7-dbf242ab5bbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Livefyre.js {#livefyre-js}

De kernbibliotheek van Livefyre die wordt gebruikt om Livefyre op uw plaats aan te drijven.

`Livefyre.js` Dit is de kernbibliotheek die u op elke LiveCycle-webpagina kunt installeren. Het definieert het globale `window.Livefyre`-object en één openbare methode, `Livefyre.require`, die kan worden gebruikt om andere LiveCycle JavaScript-bibliotheken te laden die helpen met [Livefyre Apps insluiten](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [Uw verificatieprovider integreren met LiveCycle](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) en meer.

## Toevoegen aan uw site {#section_cst_twg_xz}

Voeg de volgende tag `<script>` toe aan uw webpagina of websitesjabloon. Voeg het bestand indien mogelijk toe aan de sectie `<head>` van uw HTML-document, zodat het snel wordt geladen.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Met dit script wordt een zeer klein bestand (~1 kB), genaamd Livefyre.js-scout, ingesloten dat vervolgens de nieuwste versie van Livefyre.js laadt via het protocol waarmee uw webpagina is geopend (HTTP of HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` is een aangepaste JavaScript-modulelader, zoals  [curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/). Het kan worden gebruikt om de meeste pakketten te laden die door Livefyre worden gepubliceerd en biedt een handig en intuïtief integratiepad.

Pakketten die toegankelijk zijn via `Livefyre.require` worden versioned met [Semantische versie](https://semver.org/). Pakketten kunnen in een specifieke versie of in een reeks versies worden vereist, zodat uw webpagina automatisch kan profiteren van de nieuwe functies voor foutopsporing. Dit biedt u flexibiliteit bij het integreren van Livefyre op uw site. Er zijn drie niveaus van versie die u met `Livefyre.require` kunt gebruiken.

* **package-name#1:** Vastzetten op hoofdversie v1. U ontvangt alle nieuwe updates die een achterwaarts compatibele API onderhouden. Vastzetten aan een belangrijke versie om insectenmoeilijke situaties en minder belangrijke eigenschapverhogingen voor die versie te ontvangen.
* **package-name#1.1:** Pin to minor version v1.1. Alle problemen worden in deze kleine versie opgelost. Met LiveCycle Engineering wordt altijd een kleine versie van een pakket geplaatst als het standaardgedrag of het functionele bereik zodanig verandert dat er nieuw, onverwacht gedrag op de webpagina kan optreden. Als u geautomatiseerde foutoplossingen wilt ontvangen, maar geen aanvullende functionaliteit of wijzigingen in standaardgedrag wilt toepassen, moet u deze vastzetten in een lagere versie.
* **package-name#1.1.1:** Vastmaken aan patchversie v1.1.1. Het gedrag van deze insluiten verandert nooit, zelfs niet als er fouten zijn. Zet aan een flardversie als u uitgebreide CSS aanpassingen voor uw plaats hebt die van de de prijsverhogingsstructuur van een pakket afhangen die kan veranderen, of als u andere redenen hebt om te verkiezen dat de versie van de Levensstijl u loopt op geen enkele manier zal veranderen.

Een voorbeeldintegratie met `Livefyre.require` zou als volgt kunnen kijken:

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Beschikbare pakketten {#section_ygd_dwg_xz}

Welke LiveCycle JavaScript-pakketten zijn beschikbaar via `Livefyre.require`? Hier vindt u altijd een bijgewerkte lijst met ondersteunde pakketten en de meest recente versies: [packages.html](https://cdn.livefyre.com/packages.html).

## Prereleaseversies van pakketten testen {#section_pgm_dpg_xz}

Soms wilt u een volgende versie van een LiveCycle-pakket testen om ervoor te zorgen dat het op uw website werkt of om een functie die op uw verzoek wordt ontwikkeld, te accepteren. Naast het opnemen van een Semantische waaier van de Versie, kan het preUAT milieu worden gespecificeerd.

Hieronder vindt u bijvoorbeeld de UAT-release van `fyre.conv`, de toepassingen Opmerkingen, Live blog en Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
