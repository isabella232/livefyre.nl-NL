---
description: Release-aantekeningen voor de release van 1 november 2018.
seo-description: Release-aantekeningen voor de release van 1 november 2018.
seo-title: 1 november 2018
solution: Experience Manager
title: 1 november 2018
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# 1 november 2018{#november}

Release-aantekeningen voor de release van 1 november 2018.

## Nieuwe functies {#section_syx_mdt_wcb}

De volgende nieuwe functies zijn vrijgegeven in de productieversie van deze release:

* Slimme video-tags

   Gebruik de geavanceerde computergezichtstechnologie, aangedreven door Adobe Sensei, om video-inhoud automatisch te labelen wanneer u deze opslaat in de bibliotheek. Met slimme tags kunt u UGC effectiever beheren, maar kunt u ook supernauwkeurige curatieregels (streams) maken die inhoud verzamelen op basis van wat in de video staat, niet alleen de tekst, waardoor u bespaart op een aanzienlijke mate van inspanning bij het matigen van ongewenste inhoud.

   Details onderdeel:

   * Slimme tags worden automatisch toegevoegd aan video&#39;s die zijn opgehaald uit sociale zoekopdrachten, streams en geüploade videobestanden in de bibliotheek. Tags weergeven in de elementdetails van een individuele video
   * Hiermee worden video&#39;s gecodeerd in de indelingen .MP4, .MOV en AVI
   * Hiermee kunt u video&#39;s van maximaal 60 seconden of 50 MB labelen
   * Er zijn twee categorieën slimme tags van toepassing op video&#39;s: kenmerken (dieren, objecten, plaatsen, enz.) en handelingen (lopen, lopen, zingen, enz.)

   Zie [Slimme tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags) voor meer informatie

* Snelheidsbeperking installatieschema

   Instagram heeft het aantal verzoeken veranderd dat om het even welk bedrijf dat de Instagram API, met inbegrip van Livefyre gebruikt, van 5.000 verzoeken per uur per teken aan 200 verzoeken een uur per teken kan maken. Dit wordt *snelheidsbegrenzing* genoemd. Voor meer informatie, zie [Beperking van het Snelheidscijfer ](/help/using/c-streams/c-instagram-rate-limiting.md).

* Audiobestanden in de bibliotheek

   U kunt nu de volgende functies uitvoeren op audiobestanden vanuit het deelvenster Bibliotheek:

   * Zoeken
   * Voorvertoning
   * Importeren
   * Filteren op audiobestanden
   * Bestanden naar de ontwerper slepen en neerzetten

## Problemen {#section_ehw_ndt_wcb}

Er zijn geen nieuwe problemen opgelost in de productieversie van deze release. Zie [sectie boven](#c_rn/section_syx_mdt_wcb).

## UAT-release {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

De kwesties in de volgende lijsten werden opgelost in de versie van UAT van deze versie.

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Verbetering | GDPR | Alle gegevens die aan voormalige klanten binnen Analytics worden toegeschreven, worden verwijderd. |
| Bug | Bibliotheek | Probleem verholpen waarbij een video die naar de bibliotheek is geüpload en vervolgens in detail wordt weergegeven, niet correct werd weergegeven. |
| Bug | Mozaïek | Probleem verholpen waarbij het laatste stuk inhoud van een Instagram-carrousel door een mozaïek als miniatuur werd weergegeven in plaats van als een kaart. |
| Bug | Sociale zoekfunctie | Probleem verholpen waarbij sociaal zoeken op Instagram niet werkte zoals u had verwacht. |

