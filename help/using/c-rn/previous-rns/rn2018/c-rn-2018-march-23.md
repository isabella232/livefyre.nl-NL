---
description: Opmerkingen bij de release van 23 maart 2018.
title: 23 maart 2018
exl-id: 85fd6f79-7fa8-425e-b4c7-2e1635d6ef17
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 23 maart 2018{#march}

Opmerkingen bij de release van 23 maart 2018.

## Nieuwe functies {#section_syx_mdt_wcb}

De volgende functies zijn nieuw in de productieversie van deze release:

* **Nieuw in Productie:** Facebook heeft een beveiligingsupdate voor Facebook-aanmelding gemaakt die ervoor zorgt dat de Facebook-aanmelding van een klant niet correct werkt. U moet:

   1. Voeg de volgende URL toe aan **[!UICONTROL Valid OAuth redirect URIs]** gebied in de Montages van de Cliënt OAuth. Vervang `<networkname>` door uw correcte netwerknaam:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Schakel **[!UICONTROL Use Strict Mode for Redirect URI]** naar **[!UICONTROL Yes]**.

* **Nieuw in UAT:** U kunt nu de betrouwbaarheidsdrempel voor slimme tags in streams kiezen. Door de precisiescore (0-100) voor tags in te stellen, kunt u de nauwkeurigheid bepalen van de elementen die worden opgehaald.

## Problemen {#section_ehw_ndt_wcb}

De problemen in de volgende tabellen zijn opgelost in deze release.

## Productievrijgave

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Bug | Mediumwand | Probleem verholpen met Media Wall waarbij niet op tags kon worden geklikt wanneer een Instagram-post werd toegevoegd van een streaming regel. |
| Bug | ModQ | Probleem verholpen waarbij ModQ niet correct werd geladen. |
| Bug | ModQ | Het probleem waarbij het insluiten van audio ertoe leidde dat ModQ niet meer werkte, is opgelost. |

## UAT Release

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Verbetering | Filmstrip | Oplossing voor een aantal problemen om de filmstrip toegankelijker te maken. |
| Verbetering | Studio | U kunt zich nu aanmelden bij LiveCycle met een IMS-aanmelding. |
