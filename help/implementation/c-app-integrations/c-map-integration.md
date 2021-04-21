---
description: Inhoud van gebruiker op een interactieve kaart plaatsen.
title: Kaart
exl-id: 836b475e-0ec6-49f8-b89f-3af3209cf1f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Kaart{#map}

Inhoud van gebruiker op een interactieve kaart plaatsen.

Met de kaart kunt u geotagged inhoud streamen op een wereldkaart, zodat u de sociale buzz kunt vinden rond het doorbreken van nieuws of een live gebeurtenis. Alle toepasselijke inhoud wordt weergegeven, inclusief tekst, opmerkingen, foto&#39;s en tweets.

>[!NOTE]
>
>Kaarten worden aangedreven door [©OpenStreetMap](https://www.openstreetmap.org/copyright), die de gegevens verstrekt die Livefyre gebruikt om zijn Kaarten terug te geven.

## Integratie {#section_w2m_db2_d1b}

De snelste manier om Kaart te gebruiken is de gebouwde versie te gebruiken die op CDN van Livefyre wordt ontvangen.

Voeg eerst [Livefyre.js](https://github.com/Livefyre/Livefyre.js) toe aan uw pagina.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Vervolgens plaatst u het element waarin de Kaart-app wordt weergegeven.

```
<div id="map" style="height: 500px;"></div>
```

Tot slot gebruik Livefyre.require om de Kaart te construeren, en een Inzameling te krijgen binnen van stroomhub-sdk. Houd er rekening mee dat op Kaart alleen inhoud met geotagged metagegevens kan worden weergegeven. Twitter en Instagram Curate ondersteunen deze functie. Voor de beste prestaties neemt u een geolocatiefilter op in al uw Curate Rules for the Collection.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Bekijk dit [live voorbeeld](https://codepen.io/cheung31/pen/wkmbF).

## Configuratie {#section_jc5_gxb_c1b}

`initial`

Het aanvankelijke aantal items dat vanaf de verzameling moet worden geladen en op de kaart moet worden weergegeven. Nadat dit aantal wordt geladen, kunnen de gebruikers een knoop klikken om meer te tonen. (Optioneel. Heeft als standaardwaarde 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opties voor het doorgeven aan de onderliggende [bijsluiter](https://leafletjs.com/)-kaart, die gebruikt wordt voor rendering. Gebruik deze optie om [Opties voor brochmap ](https://leafletjs.com/reference.html#map-options) in te stellen, inclusief het beginpunt van de kaart en de initiële en maximale zoomniveaus. (Optioneel.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```
