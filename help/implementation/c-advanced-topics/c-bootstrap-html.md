---
description: Maak inhoud van de gemeenschap beschikbaar voor zoekprogrammacrawlers.
seo-description: Maak inhoud van de gemeenschap beschikbaar voor zoekprogrammacrawlers.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

Maak inhoud van de gemeenschap beschikbaar voor zoekprogrammacrawlers.

Voor een volledige lijst met beschikbare eindpunten raadpleegt u de sectie LiveCyre [API-naslaggids](https://api.livefyre.com/docs) .

Live Apps vereist dat u JavaScript op uw pagina uitvoert om inhoud voor uw Verzamelingen te tonen. Omdat de meeste zoekmachinecrawlers geen JavaScript kunnen uitvoeren, kunnen ze de inhoud die door uw community wordt geplaatst niet zien. Gebruik de HTML API van Bootstrap om doorzoekbare fragmenten van deze inhoud aan de aanvankelijke reactie van HTTP van uw pagina toe te voegen, toestaand uw inhoud en sleutelwoorden om uw onderzoeksmotor optimalisering te verbeteren.

>[!NOTE]
>
>Deze API is alleen beschikbaar voor typen opmerkingen en actieve blogverzamelingen.

## Integratie

De Bootstrap HTML-API van Livefyre retourneert een HTML-fragment van uw gebruikersinhoud dat mogelijk wordt opgenomen in de HTTP-reactie van de pagina. Deze reactie kan worden gelezen door crawlers van zoekprogramma&#39;s zonder JavaScript uit te voeren. Wanneer de pagina live is in de browser van een gebruiker, wordt het HTML-fragment vervangen door de volledige, interactieve widget en kan de gebruiker inhoud posten.

U implementeert als volgt de HTML-API van Bootstrap:

1. Maak een server aan server API verzoek aan het eindpunt van HTML Van Bootstrap hieronder gedocumenteerd.

   >[!NOTE]
   >
   >Als u de HTML van Bootstrap voor een gesprek probeert te pakken dat nog niet bestaat (namelijk als u nog niet App hebt ingebed of de Inzameling creeert), zult u 200 ontvangen, maar met inhoud die als kijkt: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Als uw terugkeer geen inhoud met &quot;404&quot;in het omvat, bewaar het in een koord. U kunt deze reactie voor later gebruik in de cache plaatsen om te voorkomen dat de Bootstrap HTML API wordt aangevraagd op elke pageload.
1. Plaats de HTML-tekenreeks Bootstrap in uw webpagina waar u de inhoud wilt weergeven.
1. Geef uw webpagina door aan de browser (of zoekprogrammacrawler).

## Resource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parameters

* **networkName** Uw Leven verstrekte netwerknaam. Bijvoorbeeld: *labs* in `labs.fyre.co`.
* **siteId** De site-id van de verzameling.
* **b64articleId** De artikel-id van de verzameling met de base64url-codering.

## Voorbeeld

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Antwoord

```
https://gist.github.com/ec5c2457322faf9cf515 
```
