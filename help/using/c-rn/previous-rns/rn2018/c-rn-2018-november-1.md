---
description: Release-aantekeningen voor de release van 1 november 2018.
title: 1 november 2018
exl-id: b12b6a56-f14f-4447-9fde-25cb3acf6665
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '353'
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

* Limiet voor instagram-snelheden

   Instagram heeft het aantal aanvragen gewijzigd dat bedrijven die de Instagram API gebruiken, waaronder Livefyre, kunnen indienen van 5.000 aanvragen per uur per token tot 200 aanvragen per uur. Dit wordt *snelheidsbegrenzing* genoemd. Zie [Instagram Rate Limiting](/help/using/c-streams/c-instagram-rate-limiting.md) voor meer informatie.

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
| Bug | Mozaïek | Probleem verholpen waarbij het laatste stuk inhoud van een Instagram-carrousel als miniatuur in plaats van als kaart werd weergegeven in een mozaïek. |
| Bug | Sociale zoekfunctie | Probleem opgelost waarbij sociaal zoeken in Instagram niet naar behoren functioneerde. |
