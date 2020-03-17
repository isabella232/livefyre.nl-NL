---
description: Toon de actiefste Inzamelingen op uw Plaats of Netwerk.
seo-description: Toon de actiefste Inzamelingen op uw Plaats of Netwerk.
seo-title: Trend
solution: Experience Manager
title: Trend
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Trend{#trending}

Toon de actiefste Inzamelingen op uw Plaats of Netwerk.

Gebruik Trending om de verzamelingen weer te geven met de meest recente activiteit op uw site of in uw netwerk.

## Integratie {#section_wtz_whb_c1b}

De snelste manier om te integreren met Trending is de ingebouwde versie te gebruiken die op CDN van Livefyre wordt ontvangen.

Voeg eerst [Livefyre.js](https://github.com/Livefyre/Livefyre.js) aan de pagina toe.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Vervolgens plaatst u het element waarin de app wordt weergegeven.

```
<div id="trending"></div>
```

Tot slot gebruik `Livefyre.require` om de component te construeren.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

U hebt nu een Trending App! Zie dit alles in actie in [dit voorbeeld](https://codepen.io/gobengo/pen/GijEy).

## Configuratie {#section_k5k_qhb_c1b}

`network`

Het netwerk waarvan de Inzamelingen zullen worden getrokken. (Vereist.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Verstrek identiteitskaart van de Plaats om Inzamelingen slechts van één enkele Plaats binnen uw Netwerk te tonen. (Optioneel.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Geef één verzamelingstag op om alleen verzamelingen met dat label weer te geven. (Optioneel.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

