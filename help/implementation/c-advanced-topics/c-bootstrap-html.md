---
description: Maak inhoud van de gemeenschap beschikbaar voor zoekprogrammacrawlers.
seo-description: Maak inhoud van de gemeenschap beschikbaar voor zoekprogrammacrawlers.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Bootstrap HTML

Maak inhoud van de gemeenschap beschikbaar voor zoekprogrammacrawlers.

Zie de sectie Live [API Reference](https://api.livefyre.com/docs) voor een volledige lijst met beschikbare eindpunten.

Live Apps vereist dat u JavaScript op uw pagina uitvoert om inhoud voor uw Verzamelingen te tonen. Omdat de meeste zoekmachinecrawlers geen JavaScript kunnen uitvoeren, kunnen ze de inhoud die door uw community wordt geplaatst niet zien. Gebruik de Bootstrap HTML API om doorzoekbare fragmenten van deze inhoud toe te voegen aan de eerste HTTP-reactie van uw pagina, zodat uw inhoud en trefwoorden de optimalisatie van uw zoekmachine kunnen verbeteren.

>[!NOTE]
>
>Deze API is alleen beschikbaar voor typen opmerkingen en actieve blogverzamelingen.

## Integratie

De Bootstrap HTML-API van Livefyre retourneert een HTML-fragment van uw gebruikersinhoud dat kan worden opgenomen in de HTTP-reactie van de pagina. Deze reactie kan worden gelezen door crawlers van zoekprogramma&#39;s zonder JavaScript uit te voeren. Wanneer de pagina live is in de browser van een gebruiker, wordt het HTML-fragment vervangen door de volledige, interactieve widget en kan de gebruiker inhoud posten.

De Bootstrap HTML API implementeren:

1. Maak een server aan server API verzoek aan het Bootstrap eindpunt van HTML dat hieronder wordt gedocumenteerd.

   >[!NOTE]
   >
   >Als u de HTML-code voor Bootstrap probeert te gebruiken voor een gesprek dat nog niet bestaat (dat wil zeggen als u de app nog moet insluiten of de verzameling hebt gemaakt), ontvangt u een 200-pagina, maar met inhoud die er ongeveer als volgt uitziet: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Als uw terugkeer geen inhoud met &quot;404&quot;in het omvat, bewaar het in een koord. U kunt deze reactie voor later gebruik in de cache plaatsen om te voorkomen dat de Bootstrap HTML API op elke pageload wordt aangevraagd.
1. Plaats de HTML-tekenreeks Bootstrap in uw webpagina waar u de inhoud wilt weergeven.
1. Geef uw webpagina door aan de browser (of zoekprogrammacrawler).

## Resource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parameters

* **** networkNameYour Livefyre verstrekte netwerknaam. Bijvoorbeeld: *labs* in `labs.fyre.co`.
* **** siteIdDe site-id van de verzameling.
* **b64** articleIdThe Article ID of the Collection using the base64url encoding.

## Voorbeeld

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Antwoord

```
https://gist.github.com/ec5c2457322faf9cf515 
```
