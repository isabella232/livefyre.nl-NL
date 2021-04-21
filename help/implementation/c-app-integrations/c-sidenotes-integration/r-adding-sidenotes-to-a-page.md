---
title: Symbolen toevoegen aan een pagina
description: Symbolen toevoegen aan een pagina
exl-id: 3ec089d0-3d51-4918-b510-d30ef645c9c2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Sidennotaties toevoegen aan een pagina {#adding-sidenotes-to-a-page}

Livefyre biedt verschillende configuratieopties voor het plaatsen van Sidenotes op de pagina:

* De optie Kiezers definieert de elementen waarop Sidenotes moeten worden weergegeven.
* Ankers vertegenwoordigen elementen die kunnen worden gedraaid.
* De container van de douanedraad staat u toe om te bepalen waar de draad van Sidenotes met betrekking tot de gedoteerde inhoud zal worden gevestigd.
* Met de optie voor het aantal identiotes kunt u het aantal toegevoegde Sidenotes op de opgegeven locatie weergeven.
* Gebruik meerdere `ConvConfig`-objecten om knooppunten toe te voegen aan meerdere artikelen op één pagina.

## Kiezers {#section_wyj_4sv_sy}

Met de optie Selectors kunnen id&#39;s inhoud op de pagina zoeken. Met de waarde voor deze optie kunt u dynamisch bepalen welke elementen worden gebruikt. Het kan een selecteurstekenreeks (zoals &quot;#content p, #content img&quot;), een jQuery-object (zoals `$(‘#content’)`), een array van DOM-elementen of een object met twee eigenschappen zijn: opnemen en uitsluiten. De Sidenotes App gebruikt vervolgens de opgegeven elementen of de overeenkomende elementen op de pagina. Als eigenschappen include en exclude worden gebruikt, zullen Sidenotes eerst de pagina ontleden om alle elementen op te vinden omvat bezit, dan om het even welke die elementen te verwijderen op het exclusief bezit worden gevonden.

## Ankers {#section_ehq_psv_sy}

Ankers vertegenwoordigen een element waarvan de inhoud kan worden voorgedraaid. Een ankerelement kan tekst of een afbeelding bevatten. De selecteursoptie die tijdens de bouw van de App wordt overgegaan zal de ankerelementen bepalen.

## Anker-id&#39;s {#section_rsb_rsv_sy}

Ankers op de pagina worden geïdentificeerd met een `data-lf-anchor-id`.

Als u de id voor een anker zelf wilt instellen, voegt u het kenmerk `data-lf-custom-anchor-id` toe aan het element dat u wilt toewijzen aan een anker. Dit is handig in gevallen waarin automatische detectie van ankers zou mislukken.

Als u bijvoorbeeld een andere URL wilt gebruiken voor de desktopversie en de mobiele versie van een afbeelding, kunnen twee verschillende URL&#39;s worden toegewezen aan verschillende ankers. Als uw HTML in plaats daarvan een `data-lf-custom-anchor-id` levert die op zowel mobiel als bureaublad hetzelfde is, wordt het afbeeldingselement behandeld als één anker.

Ankers hebben een type dat dynamisch wordt bepaald, maar kunnen ook uitdrukkelijk worden geplaatst gebruikend het `data-lf-custom-anchor-type` attribuut.

>[!NOTE]
>
>De opsommingsgetalwaarde moet worden gebruikt.

Beschikbare typen zijn:

* **Tekst:** 1
* **Afbeelding:** 2
* **Media:** 3
* **RTF:** 4

Zie [updateAnchors methode](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) voor meer over hoe te om de `updateAnchors` methode te gebruiken om inhoud Sidenote dynamisch aan de pagina toe te voegen.

## Aangepaste-thread-container {#section_jdh_btv_sy}

Gebruik de optie `threadContainerEl` om een locatie voor een Sidenotes-thread op te geven, anders dan de standaardpositie. Wanneer een anker wordt geactiveerd, worden de waarden standaard naast of onder de relevante inhoud weergegeven. Om dit gebrek te veranderen, gebruik `threadContainerEl` om het element te specificeren waar de draad zou moeten verschijnen.

Deze waarde voor deze optie werkt hetzelfde als de optie Kiezers, behalve dat alleen het eerste geldige element wordt gebruikt.

## Aantal identiotes {#section_pld_ntv_sy}

Met de optie `numSidenotesEl` kunt u een optionele widget voor het tellen van identiteiten op de pagina insluiten. Met deze optie wordt dezelfde invoer geaccepteerd als met de optie Selectors, maar wordt alleen het eerste geldige element in de invoerarray gebruikt.

De widget zal het verstrekte of aangepaste element versieren en zal het invoerpictogram Sidenotes, het aantal Sidenotes ingegaan op deze positie, en een hulppictogram omvatten.

Als u op de widget klikt, wordt een pop-up weergegeven met een korte uitleg van Sidenotes en hoe u deze gebruikt.

Zowel de uitleg als de voorbeeldtekst kunnen worden geconfigureerd met aangepaste tekenreeksen ( `questionExplanation` en `questionMockText`, respectievelijk). De weergave van de telwidget en de popover kan ook worden geconfigureerd met aangepaste stijlen ( `numSidenotes` respectievelijk `numSidenotesPopover`).

## Meerdere identiteitsverzamelingen toevoegen aan één pagina {#section_pjl_ptv_sy}

Met LiveCycle kunt u meerdere Sidenotes-verzamelingen toevoegen aan één pagina. Als de pagina bijvoorbeeld drie nieuwsartikelen bevat, kunt u drie verschillende versies van de Sidenotes App opnemen. Hiervoor moet u een afzonderlijk `ConvConfig`-object definiëren voor elke instantie van Sidenotes die u wilt maken. Bijvoorbeeld:

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
