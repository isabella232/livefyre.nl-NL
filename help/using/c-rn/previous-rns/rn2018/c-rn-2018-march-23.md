---
description: Opmerkingen bij de release van 23 maart 2018.
seo-description: Opmerkingen bij de release van 23 maart 2018.
seo-title: 23 maart 2018
solution: Experience Manager
title: 23 maart 2018
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 23 maart 2018{#march}

Opmerkingen bij de release van 23 maart 2018.

## Nieuwe functies {#section_syx_mdt_wcb}

De volgende functies zijn nieuw in de productieversie van deze release:

* **Nieuw in productie:** Facebook heeft een beveiligingsupdate gemaakt voor aanmelding bij Facebook waardoor de aanmelding bij Facebook van een klant niet correct werkt. U moet:

   1. Voeg de volgende URL toe aan **[!UICONTROL Valid OAuth redirect URIs]** veld in Client OAuth Settings. Vervangen `<networkname>` door de juiste netwerknaam:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Schakel **[!UICONTROL Use Strict Mode for Redirect URI]** over naar **[!UICONTROL Yes]**.

* **Nieuw in UAT:** U kunt nu de betrouwbaarheidsdrempel voor slimme tags in streams kiezen. Door de precisiescore (0-100) voor tags in te stellen, kunt u de nauwkeurigheid bepalen van de elementen die worden opgehaald.

## Problemen {#section_ehw_ndt_wcb}

De problemen in de volgende tabellen zijn opgelost in deze release.

## Productievrijgave

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Bug | Mediumwand | Probleem verholpen met Media Wall waarbij niet op tags kon worden geklikt wanneer een Instagram-post vanuit een streamregel werd toegevoegd. |
| Bug | ModQ | Probleem verholpen waarbij ModQ niet correct werd geladen. |
| Bug | ModQ | Het probleem waarbij het insluiten van audio ertoe leidde dat ModQ niet meer werkte, is opgelost. |

## UAT Release

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Verbetering | Filmstrip | Oplossing voor een aantal problemen om de filmstrip toegankelijker te maken. |
| Verbetering | Studio | U kunt zich nu aanmelden bij LiveCycle met een IMS-aanmelding. |

