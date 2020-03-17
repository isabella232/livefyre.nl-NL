---
description: Live chat toevoegen aan uw pagina.
seo-description: Live chat toevoegen aan uw pagina.
seo-title: Chat
solution: Experience Manager
title: Chat
uuid: d6761a69-efa5-4ad3-abaf-1ba8e6c17f94
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Chat{#chat}

Live chat toevoegen aan uw pagina.

Chat staat uw publiek toe om in real time gesprek rond levende gebeurtenissen in dienst te nemen. Inhoud wordt weergegeven als een continue stroom, waardoor een snelle deelname aan de ontvouwende dialoog wordt aangemoedigd.

Huidige versie: Chatgebruik `fyre.conv v3.0.0.`

## Integratie {#concept_0A99792A7E89403F95D082D52D600F17}

Het insluiten van de Chat-app volgt het proces voor het insluiten van een Core-app die wordt beschreven in Getting Started > [Embedding an App](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

Voorbeeld:

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Zoals vermeld in de [sectie CollectionMeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) , is CollectionMeta een gecodeerd JSON-object. In het bovenstaande voorbeeld gebruikt het JSON-object de volgende indeling voordat de JWT-code is gecodeerd:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Object NetworkConfig {#c-networkconfig-object}

Het `NetworkConfig` object is een JSON-object dat het verificatiesysteem voor netwerkgebruikers aanpast.

Het `NetworkConfig` object is een JSON-object dat de volgende parameters bevat:

| Parameter | Type | Beschrijving |
|---|---|---|
| authDelegate | *vereist* object | Wordt gebruikt om het verificatiesysteem voor aangepaste netwerkgebruikers aan te passen. |
| netwerk | *vereiste* tekenreeks | Een door Livefy verschafte netwerknaam. Bijvoorbeeld: *uwnaam.fyre.co.* |
| gehechtheidDelegate | Object | Wordt gebruikt om de typen mediabijlagen op te geven die zichtbaar zijn in de App-stream. Zie Media [](../c-app-customizations/c-restrict-media.md#c_restrict_media)beperken voor meer informatie. |
| tekenreeksen | *optioneel* object | Wordt gebruikt om tekstreeksen van de HTML-elementen in een van de LiveCycle Core-toepassingen aan te passen. Zie [Tekenreeksaanpassingen](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)voor meer informatie. |

## ConvConfig-object {#c-convconfig-object}

Het `convConfig` object is een JSON-object dat wordt gebruikt om de inhoud op te geven die de LiveCycle App op de pagina rendert.

>[!NOTE]
>
>De hier vermelde `convConfig` objectparameters zijn niet van toepassing op de app Revisies. Zie Integratie van revisies voor informatie over de integratie van de revisies-app die het `convConfig` object gebruikt.

Het `ConvConfig` object bevat de volgende vereiste parameters:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| artikelId | *vereiste* tekenreeks | Identificeert uniek een Inzameling binnen uw Plaats. Gewoonlijk komt dit overeen met een primaire databasetoets of post-id in uw CMS. Bijvoorbeeld: &quot;post-42&quot;. Maximaal 255 tekens.  Opmerking:  Als u het artikel-URL gebruikt als uw articleId, moet u controleren of de tekenreeks is gecodeerd met MD5 of SHA-1. |
| collectionMeta | *vereiste* tekenreeks | JWT-gecodeerde metagegevens over de verzameling. Zie Object [CollectionMeta](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) voor meer informatie. |
| el | *vereiste* tekenreeks | De id van een DOM-element waarnaar de inhoudsstroom wordt gerenderd. |
| siteId | *vereiste* tekenreeks | De door Livefy verschafte id voor de website of toepassing waartoe de verzameling behoort. Bijvoorbeeld: &quot;303617&quot;. |

>[!NOTE]
>
>De `app` parameter is niet vereist voor een Comments App-implementatie.

Het `ConvConfig` object kan ook de volgende optionele parameters bevatten:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| actionButtons | *optionele* array | Een array met aangepaste actieknoppen die aan een stuk inhoud naast de knoppen Delen en Vlag worden toegevoegd. Zie Aangepaste knoppen toevoegen voor meer informatie. |
| animaties | *optioneel* boolean | Hiermee bepaalt u of animaties worden uitgevoerd binnen de Livefyre-app. Ingesteld op false om animaties uit te schakelen. Heeft als standaardwaarde true. |
| anoniemFlaggingEnabled | *optioneel* boolean | Bepaalt of de gastgebruikers de optie hebben om inhoud te markeren. De standaardwaarde is true. |
| browserType | *optionele* tekenreeks | Definieert het apparaat waarvoor weergave-inhoud moet worden gegenereerd. Hierdoor worden de CSS en enige functionaliteit aangepast aan het invoerapparaattype. De opties zijn desktop, mobiel of tablet. (Als deze optie niet wordt ingevuld, wordt de Google Agent standaard ingesteld op de indeling van de weergave.) |
| controlesom | *aanbevolen* tekenreeks (aanbevolen) | Hiermee wordt de huidige status van de CollectionMeta aangegeven. Als u deze waarde wijzigt, worden de gegevens op de server door LiveCycle bijgewerkt met de nieuwe waarden in CollectionMeta. |
| datetimeFormat | *optionele* tekenreeksobjectfunctie | Hiermee geeft u de datetime-indeling van gestreamde inhoud op. Zie Datum- en tijdstempels aanpassen voor meer informatie. |
| disableAvatars | *optioneel* boolean | Voorkomt dat avatars worden gerenderd in de App-stream en verlaagt zo het aantal items dat in de browser wordt geladen. De standaardwaarde is false. |
| disableIE8Shim | *optioneel* boolean | Hiermee schakelt u het standaardschild dat door LiveCycle wordt gebruikt, uit op polyfill Internet Explorer 8, zodat HTML5-elementen worden ondersteund. Livefyre gebruikt het volgende project:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). De standaardwaarde is false.  Opmerking:  Als deze waarde false is, moet een bepaalde sorteervolgorde worden gebruikt voordat LiveCycle wordt aangeroepen voor ondersteuning door Internet Explorer 8. |
| disableThirdPartyAnalytics | *optioneel* bBoolean | Schakelt analysesystemen van derden (Quantserve en Google Analytics) uit die Livefyre kan gebruiken voor interne metingen. De standaardwaarde is false. |
| editorCss | *optioneel* object | Wordt gebruikt om de opmaak van de commentaareditor aan te passen. U kunt de achtergrondkleur van het bewerkingsveld opmaken, evenals de lettertypekleur, -grootte en -familie van de tekst die in de editor wordt weergegeven.  Bijvoorbeeld: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| initialNumVisible | *optioneel* geheel getal | Hiermee kunt u het standaardaantal opmerkingen instellen dat tijdens het laden in uw app zichtbaar is. Dit kan een geheel getal van 1 tot en met 50 zijn. |
| initialNumVisibleLegacy | *optioneel* geheel getal | Staat u toe om het standaardaantal erfenisinhoudspunten te plaatsen zichtbaar in uw App bij lading. Dit kan een geheel getal van 1 tot en met 50 zijn. Als deze parameter niet wordt gespecificeerd, blijft aan initialNumVisible in gebreke.  Bijvoorbeeld: Als uw inzameling 100 actieve en 100 erfeniscommentaren omvat, plaats initalNumVisible:10, en initialNumVisibleLegacy:5, om 10 actieve commentaren (met een Show Meer knoop) + 5 archiefcommentaren (met een Show Meer knoop) te tonen. |
| maxVisible | *optioneel* geheel getal | Hiermee stelt u het maximum aantal zichtbare stukken inhoud op hoofdniveau in de chatapp in. Als er nieuwe stukken inhoudsstroom in staan, wordt de inhoud onder aan de stream van de pagina verwijderd. Als op de knop Meer weergeven... wordt geklikt, wordt de parameter genegeerd en kan de gebruiker de gewenste hoeveelheid inhoud weergeven. (Gebruik deze parameter om het aantal items te bepalen dat op de pagina in snelle streams wordt weergegeven.) |
| postToButtons | *optionele* array | Hiermee configureert u welke providers worden weergegeven bij het insluiten van de app Live blog. Beschikbare opties zijn twee (Twitter), fb (Facebook) en li (LinkedIn). Heeft als standaardwaarde [ tw, fb ]. |
| readOnly | *optioneel* boolean | Hiermee schakelt u alle interactiviteit voor de verzameling uit. Indien waar (true), kunnen gebruikers zich niet aanmelden bij de stream en kunnen ze de inhoud niet posten, bewerken, beantwoorden of eruit zien. Indien waar (true), kunnen gebruikers inhoud markeren en delen. De standaardwaarde is false. |
| stream | *optioneel* object | Bevat opties om het stromen van App te vormen. |
| stream.catchup | *optioneel* geheel getal | Geeft het aantal seconden vóór het huidige moment op dat de stream moet worden geladen. Standaard laadt LiveCycle 50 stuks inhoud en laadt vervolgens alle verzonden inhoud tussen deze en de huidige tijd. In zeer snelle gevallen kan de inhoud te snel worden gepost, zodat de app het heden kan ‘inhalen’. Gebruik deze instelling om het aantal seconden vóór het moment te definiëren waarvoor inhoud wordt gepost (na het eerste laden van de inhoud). |
| stream.delay | *optioneel* geheel getal | Hiermee geeft u het aantal seconden op tussen streaming aanvragen. Gebruik deze parameter om de stroom van inhoud te controleren en te vertragen hoe vaak DOM wordt bijgewerkt.  Opmerking:  Als deze te groot is, kan de stream achterblijven. |


>[!NOTE]
>
>U kunt een of meer `convConfig` objecten tijdens de initialisatie van de app doorgeven om meerdere apps op dezelfde pagina weer te geven. Houd er rekening mee dat extra apps browserbronnen gebruiken en dat de prestaties kunnen afnemen naarmate het aantal toeneemt.

## Object CollectionMeta {#c-collectionmeta-object}

Het `CollectionMeta` object is een JSON-object dat de metagegevens opgeeft die in de verzameling moeten worden opgeslagen.

`CollectionMeta` wordt altijd gecodeerd voordat deze ter beveiliging wordt doorgegeven aan LiveCycle. De gecodeerde waarde wordt doorgegeven aan het bovenstaande `ConvConfig` object.

>[!NOTE]
>
>U moet code aan de serverzijde toevoegen om het `CollectionMeta` JSON-object te coderen. Zie Tokens aan de serverzijde samenstellen voor meer informatie.

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| artikelId | *vereiste* tekenreeks | Een unieke id voor de verzameling. |
| titel | *vereiste* tekenreeks | De titel die u op de verzameling wilt toepassen. Dit komt vaak overeen met de titel van de pagina waarop de app wordt weergegeven.  Bijvoorbeeld: &quot;Integratie is zo leuk!&quot;  Opmerking:  De maximale tekenlengte voor de titel is 255 tekens. Het titelveld ondersteunt geen HTML-entiteiten. Codeer speciale tekens met UTF-8. |
| url | *vereiste* tekenreeks | De canonieke absolute URL die u aan deze verzameling wilt koppelen. Deze URL wordt gebruikt om koppelingen naar de app te genereren op basis van inhoud die wordt gedeeld op Facebook en Twitter, e-mailmeldingen en LiveCyre Studio.  Opmerking:  Livefyre vereist het gebruik van een volledig gekwalificeerde domeinnaam; het havenaantal of een callback om de lokale opstelling op te lossen wordt niet vereist. Als u lokaal test, moet u zeker weten dat u een geldig basis-URL-domein gebruikt. (Bijvoorbeeld: is `https://customer.com` geldig, maar `https://localhost:5995` niet.) Zodra u opstelling uw lokale webserver hebt om volledig - gekwalificeerde domeinnaam goed te keuren, zijn geen callbacks of resoluties nodig, en de lokale ontwikkeling kan te werk gaan zoals verwacht. |
| type | *vereiste* tekenreeks | Het type verzameling. Moet livechat zijn. |

Het `CollectionMeta` object kan ook de volgende optionele parameter bevatten:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| tags | *optionele* tekenreeks | Een door komma&#39;s gescheiden lijst met enkele trefwoorden of woordgroepen. Verzamelingen zoeken op tags in Studio of met de zoek-API.  Opmerking: Tags die door Studio zijn toegevoegd, kunnen spaties bevatten, maar tags die door de API zijn ingevoerd, kunnen dit niet. Gebruik onderstrepingstekens om tags te definiëren waarmee spaties in de gebruikersinterface worden weergegeven. (Bijvoorbeeld: gebruik maandag_Quarterback om Maandag Quarterback in Studio te tonen.) |

## Een gebeurtenishandler toevoegen {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Om gebeurtenismanagers te registreren, gebruik widget.on vraag binnen de callback functie van de App.

Bijvoorbeeld:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

Zie [JavaScript-gebeurtenissen](../c-app-customizations/c-javascript-events.md#c_javascript_events)voor meer informatie en voor een lijst met beschikbare gebeurtenissen.
