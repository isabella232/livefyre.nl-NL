---
seo-title: Een app insluiten
solution: Experience Manager
title: Een app insluiten
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Een app insluiten{#embed-an-app}

Met de codestructuur van Livefyre.js kunt u Live-apps aan uw webpagina&#39;s toevoegen.

Deze documentatie is bedoeld voor een technisch publiek. Voor [niet-technische informatie over toepassingen](/help/using/c-about-apps/c-about-apps.md).

In deze sectie wordt de codestructuur beschreven die u in uw paginasjabloon moet opnemen om Live-apps op uw site in te sluiten.

1. Maak een HTML-bestand met een tijdelijke aanduiding voor LiveCycle.

   Maak een nieuw HTML-bestand in de teksteditor van uw keuze. Maak een `<div>` element voor plaatsaanduiding Livefyre waarin de app wordt ingesloten.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Neem de bibliotheek Livefyre.js op.

   Neem vervolgens de Livefyre JS-bibliotheek op. Plaats de volgende verwijzing in een `<script>` element in uw `<head>` element. Open vervolgens de pagina in een browser en gebruik de webcontrole van uw browser om te bevestigen dat LiveCycle is geladen.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construeer de Livefyre-app.

   Gebruik deze optie `Livefyre.require` om zowel Core- als SDK-apps samen te stellen door de LiveCycle-pakketten door te geven die u wilt gebruiken.

   1. Een Core-app ontwikkelen.

      Als u een Core-app (Opmerkingen, Live Blog of Chat) wilt maken, gebruikt u de volgende structuur:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Maak een SDK-app.

      Gebruik de volgende structuur om een SDK-app zoals Media Wall of Feed te maken:

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Zie [meer informatie over specifieke apps](/help/using/c-about-apps/c-about-apps.md). U wordt aangeraden de nieuwste hoofdversie van het pakket (die u kunt vinden via [Livefyre.require](https://cdn.livefyre.com/packages.html)) vast te zetten om onverwachte verbroken integraties te voorkomen.

Volgende: Voeg verificatie toe aan uw site zodat uw gebruikers opmerkingen kunnen posten.
