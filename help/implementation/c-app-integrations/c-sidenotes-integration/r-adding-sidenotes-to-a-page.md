---
description: 'null'
seo-description: 'null'
seo-title: Symbolen toevoegen aan een pagina
solution: Experience Manager
title: Symbolen toevoegen aan een pagina
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Symbolen toevoegen aan een pagina {#adding-sidenotes-to-a-page}

Livefyre biedt verschillende configuratieopties voor het plaatsen van Sidenotes op de pagina:

* De optie Kiezers definieert de elementen waarop Sidenotes moeten worden weergegeven.
* Ankers vertegenwoordigen elementen die kunnen worden gedraaid.
* De container van de douanedraad staat u toe om te bepalen waar de draad van Sidenotes met betrekking tot de gedoteerde inhoud zal worden gevestigd.
* Met de optie voor het aantal identiotes kunt u het aantal toegevoegde Sidenotes op de opgegeven locatie weergeven.
* Gebruik meerdere `ConvConfig` objecten om id&#39;s toe te voegen aan meerdere artikelen op één pagina.

## Kiezers {#section_wyj_4sv_sy}

Met de optie Selectors kunnen id&#39;s inhoud op de pagina zoeken. Met de waarde voor deze optie kunt u dynamisch bepalen welke elementen worden gebruikt. Dit kan een selecteurstekenreeks zijn (zoals &#39;#content p, #content img&#39;), een jQuery-object (zoals `$(‘#content’)`), een array van DOM-elementen of een object met twee eigenschappen: opnemen en uitsluiten. De Sidenotes App gebruikt vervolgens de opgegeven elementen of de overeenkomende elementen op de pagina. Als eigenschappen include en exclude worden gebruikt, zullen Sidenotes eerst de pagina ontleden om alle elementen op te vinden omvat bezit, dan om het even welke die elementen te verwijderen op het exclusief bezit worden gevonden.

## Ankers {#section_ehq_psv_sy}

Ankers vertegenwoordigen een element waarvan de inhoud kan worden voorgedraaid. Een ankerelement kan tekst of een afbeelding bevatten. De selecteursoptie die tijdens de bouw van de App wordt overgegaan zal de ankerelementen bepalen.

## Anker-id&#39;s {#section_rsb_rsv_sy}

Ankers op de pagina worden geïdentificeerd met behulp van een `data-lf-anchor-id`.

Als u de id voor een anker zelf wilt instellen, voegt u het kenmerk toe `data-lf-custom-anchor-id` aan het element dat u wilt toewijzen aan een anker. Dit is handig in gevallen waarin automatische detectie van ankers zou mislukken.

Als u bijvoorbeeld een andere URL wilt gebruiken voor de desktopversie en de mobiele versie van een afbeelding, kunnen twee verschillende URL&#39;s worden toegewezen aan verschillende ankers. Als in plaats daarvan uw HTML een afbeelding levert `data-lf-custom-anchor-id` die op zowel mobiel als bureaublad hetzelfde is, wordt het afbeeldingselement behandeld als één anker.

Ankers hebben een type dat dynamisch wordt bepaald, maar kunnen ook expliciet worden ingesteld met het `data-lf-custom-anchor-type` kenmerk.

>[!NOTE]
>
>De opsommingsgetalwaarde moet worden gebruikt.

Beschikbare typen zijn:

* **Tekst:** 1
* **Afbeelding:** 2
* **Media:** 3
* **Verzadigd:** 4

Zie [updateAnchors methode](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) voor meer informatie over hoe te om de `updateAnchors` methode te gebruiken om inhoud Sidenote dynamisch aan de pagina toe te voegen.

## Container met aangepaste verbindingen {#section_jdh_btv_sy}

Gebruik de `threadContainerEl` optie om een plaats voor een draad van Sidenotes, buiten de standaardpositie te specificeren. Wanneer een anker wordt geactiveerd, worden de waarden standaard naast of onder de relevante inhoud weergegeven. Om dit gebrek te veranderen, gebruik `threadContainerEl` om het element te specificeren waar de draad zou moeten verschijnen.

Deze waarde voor deze optie werkt hetzelfde als de optie Kiezers, behalve dat alleen het eerste geldige element wordt gebruikt.

## Aantal identiotes {#section_pld_ntv_sy}

Gebruik de `numSidenotesEl` optie om een optionele widget voor het tellen van identiteiten in te sluiten op de pagina. Met deze optie wordt dezelfde invoer geaccepteerd als met de optie Selectors, maar wordt alleen het eerste geldige element in de invoerarray gebruikt.

De widget zal het verstrekte of aangepaste element versieren en zal het invoerpictogram Sidenotes, het aantal Sidenotes ingegaan op deze positie, en een hulppictogram omvatten.

Als u op de widget klikt, wordt een pop-up weergegeven met een korte uitleg van Sidenotes en hoe u deze gebruikt.

Zowel de uitleg als de voorbeeldtekst kunnen worden geconfigureerd met aangepaste tekenreeksen ( `questionExplanation` respectievelijk en `questionMockText`). De weergave van de telwidget en de pop-up kunnen ook worden geconfigureerd met aangepaste stijlen ( `numSidenotes` respectievelijk `numSidenotesPopover`).

## Verzamelingen met meerdere knooppunten toevoegen aan één pagina {#section_pjl_ptv_sy}

Met LiveCycle kunt u meerdere Sidenotes-verzamelingen toevoegen aan één pagina. Als de pagina bijvoorbeeld drie nieuwsartikelen bevat, kunt u drie verschillende versies van de Sidenotes App opnemen. Hiervoor moet u een afzonderlijk `ConvConfig` object definiëren voor elke instantie van Sidenotes die u wilt maken. Bijvoorbeeld:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```