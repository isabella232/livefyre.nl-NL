---
description: Gebruik Bootstrap- en Stream-API met LiveCycle Apps.
title: Toepassingsimplementatie
uuid: null
exl-id: f1edef86-491d-4f8e-8ce5-f6e019d057ec
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Toepassingsimplementatie {#appimplementation}

Hoofdlettergebruik: Als klant, wil ik Livefyre in mijn derde partij CMS integreren gebruikend de methode Livefyre.js.

Er zijn drie manieren om Livefy in aan een douane AEM component of andere CMS&#39;s zoals WordPress, Sitecore, of DemandWare uit te voeren: Implementatie, API, implementatie en integratie van externe verificatie in Designer.

## Designer-app-implementatie {#designerapp}

Wat: Eenvoudige en snelste manier om een LiveCycle-app te integreren. U kunt een aangepaste Javascript-insluitcode ontwerpen, configureren en genereren om een Live App in minuten op een pagina te integreren.

Hoe: [Een LiveCyre-app maken, voorvertonen, publiceren en insluiten](/help/using/c-about-apps/c-create-an-app.md)

Voorbeeld: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementatie LiveCyre.js {#livefyrejsimp}

Wat: [Livefyre.js](/help/implementation/c-livefyre.js.md) is de kernbibliotheek die Apps en Auth op een plaats macht. Het definieert het globale `window.Livefyre`-object en één openbare methode, Livefyre.require, die kan worden gebruikt om andere LiveCycle JavaScript-bibliotheken te laden die helpen bij het insluiten van LiveCycle Apps en het integreren met externe gebruikersauteplatforms.

Hoe:

* [Creeer een Inzameling gebruikend de Token CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Apps integreren in CMS van derden met behulp van App Integrations

Voorbeelden:

* App met opmerkingen: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Revisies-app: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mediawand: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Voor geavanceerde aanpassingen die SDK gebruiken, zie StreamHub SDKs.

## API-implementatie {#apiimplementation}

Voor het maken van aangepaste ervaringen en gegevensvisualisaties kunnen LiveCyre-apps helemaal vanaf het begin worden gemaakt door LiveCycle- en sociale gegevens te gebruiken met de API voor Bootstrap en streamen.

## Integratie van verificatie van derden {#thirdpartyauth}

Zie [Identiteitsintegratie](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) voor externe verificatieplatforms voor Livefyre-toepassingen die verificatie vereisen.

## Voorbeelden van klanten {#customerexamples}

De volgende klanten implementeerden Livefy met de Integraties van CMS van derden:

* [PGA-kleurendrukschijf](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
