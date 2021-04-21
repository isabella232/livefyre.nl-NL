---
description: Met Live Blog kunt u realtime updates en afbeeldingen van de eigen editors van uw site weergeven wanneer u een live gebeurtenis bedekt.
title: Live blog
exl-id: e8a16b56-53c9-488e-9807-1cf80b62462e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Live blog{#live-blog}

Met Live Blog kunt u realtime updates en afbeeldingen van de eigen editors van uw site weergeven wanneer u een live gebeurtenis bedekt.

## Live blog {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

Met Live Blog kunt u realtime updates en afbeeldingen van de eigen editors van uw site weergeven wanneer u een live gebeurtenis bedekt.

## Integratie {#c_live_blog_integration}

Met Live Blog kunt u realtime updates en afbeeldingen van de eigen editors van uw site weergeven wanneer u een live gebeurtenis bedekt.

Als u een Live Blog-app wilt insluiten, volgt u de procedure voor het insluiten van een app. Zie [Een toepassing insluiten](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Hieronder ziet u hoe een ingesloten live-blogtoepassing eruit ziet.

### Voorbeeld

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
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
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

CollectionMeta is een gecodeerd JSON-object. In het bovenstaande voorbeeld heeft het JSON-object de volgende indeling voordat JWT-codering wordt uitgevoerd:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## Object NetworkConfig {#c-networkconfig-object}

Het object `NetworkConfig` is een JSON-object dat het verificatiesysteem voor netwerkgebruikers aanpast.

Het object `NetworkConfig` is een JSON-object dat de volgende parameters bevat:

| Parameter | Type | Beschrijving |
|---|---|---|
| **authDelegate** | ** requiredobject | Wordt gebruikt om het verificatiesysteem voor aangepaste netwerkgebruikers aan te passen. |
| **netwerk** | ** vereiste tekenreeks A door LiveCycle geleverde netwerknaam. Bijvoorbeeld: *uwnaam.fyre.co* |
| **gehechtheidDelegate** | ** optioneel object | Wordt gebruikt om de typen mediabijlagen op te geven die zichtbaar zijn in de App-stream. Zie [Media beperken](../c-app-customizations/c-restrict-media.md#c_restrict_media) voor meer informatie. |
| **tekenreeksen** | ** optioneel object | Wordt gebruikt om tekstreeksen van de HTML-elementen in een van de LiveCycle Core-toepassingen aan te passen. Voor meer informatie, zie [Koordaanpassingen](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## ConvConfig-object {#c-convconfig-object}

Het object `convConfig` is een JSON-object dat wordt gebruikt om de inhoud op te geven die de LiveCycle App op de pagina rendert.

>[!NOTE]
>
>De `convConfig` objectparameters die hier worden vermeld, zijn niet van toepassing op de app Revisies. Zie Revisies-integratie voor integratieinformatie over de app Revisies met het object `convConfig`.

Het object `ConvConfig` bevat de volgende vereiste parameters:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| **artikelId** | ** vereiste tekenreeks | Identificeert uniek een Inzameling binnen uw Plaats. Gewoonlijk komt dit overeen met een primaire databasetoets of post-id in uw CMS. Bijvoorbeeld: &quot;post-42&quot;. Maximaal 255 tekens.  Opmerking:  Als u het artikel-URL gebruikt als uw articleId, moet u controleren of de tekenreeks is gecodeerd met MD5 of SHA-1. |
| **collectionMeta** | ** vereiste tekenreeks | JWT-gecodeerde metagegevens over de verzameling. Zie Object CollectionMeta voor meer informatie. |
| **el** | ** vereiste tekenreeks | De id van een DOM-element waarnaar de inhoudsstroom wordt gerenderd. |
| **siteId** | ** vereiste tekenreeks | De door Livefy verschafte id voor de website of toepassing waartoe de verzameling behoort. Bijvoorbeeld: &quot;303617&quot;. |

>[!NOTE]
>
>De `app` parameter wordt niet vereist voor een implementatie van Commentaar App.

Het object `ConvConfig` kan ook de volgende optionele parameters bevatten:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| **actionButtons** | ** optionele array | Een array met aangepaste actieknoppen die aan een stuk inhoud naast de knoppen Delen en Vlag worden toegevoegd. Zie Aangepaste knoppen toevoegen voor meer informatie. |
| **animaties** | ** optionalboolean | Hiermee bepaalt u of animaties worden uitgevoerd binnen de Livefyre-app. Ingesteld op false om animaties uit te schakelen. Heeft als standaardwaarde true. |
| **anoniemFlaggingEnabled** | boolean | Bepaalt of de gastgebruikers de optie hebben om inhoud te markeren. De standaardwaarde is true. |
| browserType | ** optionalString | Definieert het apparaat waarvoor weergave-inhoud moet worden gegenereerd. Hierdoor worden de CSS en enige functionaliteit aangepast aan het invoerapparaattype. De opties zijn desktop, mobiel of tablet. (Als deze optie niet wordt ingevuld, wordt de Google Agent standaard ingesteld op de indeling van de weergave.) |
| **controlesom** | ** optionele tekenreeks (aanbevolen) | Hiermee wordt de huidige status van de CollectionMeta aangegeven. Als deze waarde wordt gewijzigd, worden de gegevens op de server door LiveCycle bijgewerkt met de nieuwe waarden in CollectionMeta. |
| **datetimeFormat** | **  optionele tekenreeksobjectfunctie | Hiermee geeft u de datetime-indeling van gestreamde inhoud op. Zie Datum- en tijdstempels aanpassen voor meer informatie. |
| disableAvatars | ** optionalboolean | Voorkomt dat avatars worden gerenderd in de App-stream en verlaagt zo het aantal items dat in de browser wordt geladen. De standaardwaarde is false. |
| disableIE8Shim | ** optionalboolean | Hiermee schakelt u het standaardschild dat door LiveCycle wordt gebruikt, uit op polyfill Internet Explorer 8, zodat HTML5-elementen worden ondersteund. Livefyre gebruikt het volgende project:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . De standaardwaarde is false.  Opmerking:  Als deze waarde false is, moet een bepaalde sorteervolgorde worden gebruikt voordat LiveCycle wordt aangeroepen voor ondersteuning door Internet Explorer 8. |
| **disableThirdPartyAnalytics** | ** optionalboolean | Schakelt analysesystemen van derden (Quantserve en Google Analytics) uit die Livefyre kan gebruiken voor interne metingen. De standaardwaarde is false. |
| **editorCss** | ** optioneel object | Wordt gebruikt om de opmaak van de commentaareditor aan te passen. U kunt de achtergrondkleur van het bewerkingsveld opmaken, evenals de lettertypekleur, -grootte en -familie van de tekst die in de editor wordt weergegeven.  Bijvoorbeeld: {background: ‘#ccc’, color: &quot;red&quot;, font: ’30px &quot;Helvetica Neue&quot;, Helvetica, Arial, Genève, sans-serif&quot;} |
| **initialNumVisible** | ** optionalinteger | Hiermee kunt u het standaardaantal opmerkingen instellen dat tijdens het laden in uw app zichtbaar is. Dit kan een geheel getal van 1 tot en met 50 zijn. |
| **initialNumVisibleLegacy** | ** optionalinteger | Staat u toe om het standaardaantal erfenisinhoudspunten te plaatsen zichtbaar in uw App bij lading. Dit kan een geheel getal van 1 tot en met 50 zijn. Als deze parameter niet wordt gespecificeerd, blijft aan initialNumVisible in gebreke.  Bijvoorbeeld: Als uw inzameling 100 actieve en 100 erfeniscommentaren omvat, plaats initalNumVisible:10, en initialNumVisibleLegacy:5, om 10 actieve commentaren (met een Show Meer knoop) + 5 archiefcommentaren (met een Show Meer knoop) te tonen. |
| **maxVisible** | ** optionalinteger | Hiermee stelt u het maximum aantal zichtbare stukken inhoud op hoofdniveau in de chatapp in. Als er nieuwe stukken inhoudsstroom in staan, wordt de inhoud onder aan de stream van de pagina verwijderd. Als op de knop Meer weergeven... wordt geklikt, wordt de parameter genegeerd en kan de gebruiker de gewenste hoeveelheid inhoud weergeven. (Gebruik deze parameter om het aantal items te bepalen dat op de pagina in snelle streams wordt weergegeven.) |
| **postToButtons** | ** optionele array | Hiermee configureert u welke providers worden weergegeven bij het insluiten van de app Live blog. Beschikbare opties zijn twee (Twitter), fb (Facebook) en li (LinkedIn). De standaardwaarde is [ tw , fb ]. |
| **readOnly** | ** optionalboolean | Hiermee schakelt u alle interactiviteit voor de verzameling uit. Indien waar (true), kunnen gebruikers zich niet aanmelden bij de stream en kunnen ze de inhoud niet posten, bewerken, beantwoorden of eruit zien. Indien waar (true), kunnen gebruikers inhoud markeren en delen. De standaardwaarde is false. |
| **stream** | ** optioneel object | Bevat opties om het stromen van App te vormen. |
| stream.catchup | ** optionalinteger | Geeft het aantal seconden vóór het huidige moment op dat de stream moet worden geladen. Standaard laadt LiveCycle 50 stuks inhoud en laadt vervolgens alle verzonden inhoud tussen deze en de huidige tijd. In zeer snelle gevallen kan de inhoud te snel worden gepost, zodat de app het heden kan ‘inhalen’. Gebruik deze instelling om het aantal seconden vóór het moment te definiëren waarvoor inhoud wordt gepost (na het eerste laden van de inhoud). |
| **stream.delay** | ** optionalinteger | Hiermee geeft u het aantal seconden op tussen streamingaanvragen. Gebruik deze parameter om de stroom van inhoud te controleren en te vertragen hoe vaak DOM wordt bijgewerkt.  Opmerking:  Als deze te groot is, kan de stream achterblijven. |


>[!NOTE]
>
>U kunt een of meer `convConfig`-objecten tijdens de initialisatie van de app doorgeven om meerdere apps op dezelfde pagina weer te geven. Houd er rekening mee dat extra apps browserbronnen gebruiken en dat de prestaties kunnen afnemen naarmate het aantal toeneemt.

## Object CollectionMeta {#c-collectionmeta-object}

Het object `CollectionMeta` is een JSON-object dat de metagegevens opgeeft die in de verzameling moeten worden opgeslagen.

`CollectionMeta` wordt altijd gecodeerd voordat deze ter beveiliging wordt doorgegeven aan LiveCycle. De gecodeerde waarde wordt doorgegeven aan het object `ConvConfig` dat hierboven wordt weergegeven.

>[!NOTE]
>
>U moet code aan de serverzijde toevoegen om het JSON-object `CollectionMeta` te coderen. Zie Tokens aan de serverzijde samenstellen voor meer informatie.

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| **artikelId** | ** vereiste tekenreeks | Een unieke id voor de verzameling. |
| **titel** | ** vereiste tekenreeks | De titel die u op de verzameling wilt toepassen. Dit komt vaak overeen met de titel van de pagina waarop de app wordt weergegeven.  Bijvoorbeeld: &quot;Integratie is zo leuk!&quot;  Opmerking:  De maximale tekenlengte voor de titel is 255 tekens. Het titelveld ondersteunt geen HTML-entiteiten. Codeer speciale tekens met UTF-8. |
| **url** | ** vereiste tekenreeks | De canonieke absolute URL die u aan deze verzameling wilt koppelen. Deze URL wordt gebruikt om koppelingen te genereren naar de app vanuit inhoud die wordt gedeeld op Facebook en Twitter, e-mailmeldingen en LiveCyre Studio.  Opmerking:  Livefyre vereist het gebruik van een volledig gekwalificeerde domeinnaam; het havenaantal of een callback om de lokale opstelling op te lossen wordt niet vereist. Als u lokaal test, moet u zeker weten dat u een geldig basis-URL-domein gebruikt. (Bijvoorbeeld: `https://customer.com` is geldig, terwijl `https://localhost:5995` niet. is) Zodra u opstelling uw lokale webserver hebt om volledig - gekwalificeerde domeinnaam goed te keuren, zijn geen callbacks of resoluties nodig, en de lokale ontwikkeling kan te werk gaan zoals verwacht. |
| **type** | ** requiredString | Het type verzameling. Moet livechat zijn. |

Het object `CollectionMeta` kan ook de volgende optionele parameter bevatten:

| Parameter | Type | Beschrijving |
|---|---|---|
| **tags** | ** optionele tekenreeks | Een door komma&#39;s gescheiden lijst met enkele trefwoorden of woordgroepen. Verzamelingen zoeken op tags in Studio of met de zoek-API. **Opmerking:** tags die via Studio zijn toegevoegd, kunnen spaties bevatten, maar tags die via de API zijn ingevoerd, kunnen dit niet. Gebruik onderstrepingstekens om tags te definiëren waarmee spaties in de gebruikersinterface worden weergegeven. (Bijvoorbeeld: gebruik maandag_Quarterback om Maandag Quarterback in Studio te tonen.) |

## Een gebeurtenishandler {#concept_D835C710A7214F6D921571E0770B6BC5} toevoegen

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
