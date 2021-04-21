---
description: Gebruik Bootstrap- en Stream-API met LiveCycle Apps.
title: Accountdetails weergeven
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Bootstrap- en stream-API gebruiken met LiveCycle Apps {#bootstrap-stream-api}

## Bootstrap-API {#bootstrap-api}

### Hoe kan ik inhoud ouder dan de nieuwste 50 stukken terugwinnen? {#howcontentolder}

Bootstrap is alle inhoud in een LiveCycle-app. Het zijn de gegevens in de cache, doorgaans 12-20 minuten oud. Het wordt geleverd in brokken van 50 stukken en wordt gepagineerd zodat kunt u inhoud ouder dan 50 stukken terugwinnen.

[API-naslag](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Voorbeeld van aanvraag](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

Met de voorbeeldaanvraag hierboven wordt de `init`-pagina geladen die de verzamelingsinstellingen en de enige oorspronkelijke set ~50 stuks nieuwste inhoud bevat. Als u oudere inhoud wilt opiniepeilen, moet u volgende opstartpagina&#39;s laden waarbij `N` het paginanummer is:

Verzoek: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Een voorbeeldtoepassing heeft bijvoorbeeld 120 stukken inhoud. Inhoud &quot;1&quot; is het oudste stuk inhoud en Inhoud &quot;70&quot; is het nieuwste stuk inhoud.

* `Init` Hiermee worden ~120-70 stukken inhoud in aflopende volgorde geladen:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` Hiermee laadt u ~ 1-50 stukken inhoud in oplopende volgorde:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` Hiermee laadt u ~ 51-100 stukken inhoud in oplopende volgorde:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` hiermee worden ~101-120 stukken inhoud in oplopende volgorde geladen:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Klik hier om het Bootstrap opiniepeilingdiagram te zien.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## Stream-API {#stream-api}

Wat is Stream API?
Stream is een lange opiniepeiling die door ontwerp is bedoeld om ongeveer 30 seconden open te blijven. Hieronder vindt u een beschrijving van de techniek voor lange opiniepeiling: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Dit lange opiniepeilend eindpunt stroomt nieuwe inhoud (bijvoorbeeld een gebruiker plaatst een commentaar), veranderingen van de inhoudsstatus (b.v. de gebruiker schrapt hun commentaar, houdt) en moderatieveranderingen in inhoud (b.v. de moderator keurt een stuk van inhoud goed) aan een Levensmiddelenapp.

De aanvraag voor stream-API moet ~30 seconden (lang polling) zijn met een verwachte time-out na 30 seconden wanneer er geen nieuwe inhoud wordt gestreamd.

API-referentie: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Voorbeeld van aanvraag:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Opmerking: De `maxEventId` in een stroom API reactie is hoogste identiteitskaart van de Gebeurtenis van de updates in deze reactie. Gebruik deze waarde als padparameter `lastEventId` bij het maken van de URL van uw volgende Stream API-aanvraag om updates te verkrijgen die optreden na alle updates in deze reactie.

Het onderstaande voorbeeld is gebaseerd op een Comments App:

Opmerking &quot;Eerste opmerking&quot; is eerst geplaatst. &quot;Tweede opmerking&quot; is geplaatst na.

Eerste API-reactie voor commentaarstroom:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

`maxEventId` in de reactie is &quot;1520289700953369&quot; die als `lastEventId` zal worden gebruikt om het eindpunt te onderzoeken om updates (d.w.z. tweede Commentaar) te krijgen die na alle updates in deze reactie voorkomen.

Tweede API-reactie voor commentaarstroom:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

`maxEventID` &quot;1520289700953369&quot; in de reactie zou beurtelings als `lastEventID` moeten worden gebruikt om de stroom API reactie voor de volgende update te bouwen.
