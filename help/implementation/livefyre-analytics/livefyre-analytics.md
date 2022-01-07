---
description: Analyseer de gebruikers-, inhoud- en moderatoractiviteiten voor uw site.
title: Analyse
exl-id: dc0545ec-2294-44ab-87c4-67eb30c3f787
source-git-commit: 9cd6617c4204b2c09787ea294227f640018928ce
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Analyse{#analytics}

Analyseer de gebruikers-, inhoud- en moderatoractiviteiten voor uw site.

## Analyse {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analyseer de gebruikers-, inhoud- en moderatoractiviteiten voor uw site.

Live Analytics biedt toegang tot uw netwerkgegevens in eenvoudig te lezen dashboards voor conversies, moderatie en gebruikersgegevens. Gebruik deze dashboards om de activiteit te controleren en snelle analyses op uw plaats(en) uit te voeren.

De dashboards kunnen door plaats, datum, en activiteit worden gefiltreerd. Gebruik de keuzelijst Netwerk linksboven in het venster om de site te selecteren die u wilt weergeven. Klik op een kolomkop om de grafiek te sorteren, of klik met de muis boven de grafiek voor meer specifieke informatie over een willekeurig gegevenspunt.

Deze pagina beschrijft:

* Een datumbereik voor het dashboard selecteren
* Beschikbare activiteiten weergeven/verbergen
* Dashboardgegevens exporteren
* Het dashboard Verzamelingen
* Het dashboard voor modernisering
* Het gebruikersdashboard

>[!NOTE]
>
>Analyses ondersteunen momenteel activiteiten die afkomstig zijn van Livefyre Core Apps en Moderation. De meeste activiteiten in deze dashboards zijn ook beschikbaar via LiveCycle JavaScript Events, die kunnen worden gebruikt om uw eigen aangepaste of externe analyseprogramma aan te sturen.

## Datumbereik {#concept_798C438120E643B6BE262C9997DC87C4}

Klik op de datumkeuzelijst om een bereik te selecteren dat u wilt weergeven. Gebruik de snelle datums of selecteer een begin- en einddatum in de opgegeven kalenders.

![](assets/analytics-date-range.png)

Snelle datums:

* **Vandaag:** Hiermee geeft u gegevens weer van middernacht op de ochtend van de huidige dag tot het laatste volledige uur voor dit moment.
* **Gisteren:** Geeft de gegevens van de vorige 24 uur weer.
* **7 dagen:** Geeft de gegevens van de vorige 7 dagen weer, exclusief vandaag.
* **30 dagen:** Geeft de gegevens van de vorige 30 dagen weer, exclusief vandaag.
* **Deze week:** Geeft gegevens weer van middernacht op de ochtend van afgelopen zondag tot het laatste volledige uur voor dit moment.
* **Deze maand:** Geeft gegevens weer van middernacht op de ochtend van de eerste dag van de huidige maand tot het laatste volledige uur voor dit moment.
* **Vorige week:** Hier worden de gegevens van vorige week weergegeven.
* **Vorige maand:** Gegevens van vorige maand worden weergegeven.

## Weergeven/verbergen {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Activiteiten zijn acties die gebruikers op uw site uitvoeren, zoals opmerkingen plaatsen, markeren, delen en modereren. Gebruik de **Activiteiten tonen/verbergen** keuzelijst voor het selecteren van activiteiten die u wilt opnemen in het dashboard.

>[!NOTE]
>
>Als u nieuwe gebeurtenissen voor het filter selecteert, wordt de pagina opnieuw weergegeven zonder de URL te wijzigen.

![](assets/analytics-show-hide-activities.png)

De beschikbare activiteiten variëren per dashboardtype en export en kunnen het volgende omvatten:

* **Post:** Hiermee geeft u gegevens weer van middernacht op de ochtend van de huidige dag tot het laatste volledige uur voor dit moment.
* **Reacties:** Geeft de gegevens van de vorige 24 uur weer.
* **Koppelingen:** Geeft de gegevens van de vorige 7 dagen weer, exclusief vandaag.
* **Niet leuk:** Geeft de gegevens van de vorige 30 dagen weer, exclusief vandaag.
* **Bevat media:** Geeft gegevens weer van middernacht op de ochtend van afgelopen zondag tot het laatste volledige uur voor dit moment.
* **Post heeft foto-upload:** Geeft gegevens weer van middernacht op de ochtend van de eerste dag van de huidige maand tot het laatste volledige uur voor dit moment.
* **Post heeft koppeling:** Hier worden de gegevens van vorige week weergegeven.
* **Post heeft @mnotices:** Gegevens van vorige maand worden weergegeven.
* **Goedgekeurd:** Gegevens van vorige maand worden weergegeven.
* **Bozo&#39;d:** Gegevens van vorige maand worden weergegeven.
* **Verlopen:** Gegevens van vorige maand worden weergegeven.
* **Totaal moderatie:** Gegevens van vorige maand worden weergegeven.

## Dashboardgegevens exporteren {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Gebruik de **Exporteren** keuzemenu om uw dashboardgegevens te exporteren als een CSV-bestand.

* Dagelijkse samenvatting (alleen verzamelingen): exporteert de dagelijkse tabellen van de laatste volledige week voor elke verzameling.
* Tabelgegevens: Hiermee exporteert u alle opgeschoven verzamelingsgegevens (alle kolommen en alle rijen in het huidige rapport).
* Onbewerkte gegevens: Hiermee exporteert u alle afzonderlijke gebeurtenissen die zijn gebruikt om het huidige oprolrapport te maken.

>[!NOTE]
>
>Deze rapporten kunnen een paar minuten duren om te worden geëxporteerd. Alle tijdstempels zijn Unix-tijd.

## Verzamelingen {#concept_228D8E5553784DB8BABF3819A5FF0345}

Het dashboard van Inzamelingen maakt een lijst van gebruikersactiviteit door Inzameling, die u toestaat om uw het meest (en minst) het in dienst nemen inhoud te bepalen. Elke vermelde verzameling bevat een koppeling naar de pagina waarop deze kan worden gevonden.

![](assets/analytics-collections.png)

## Moderatie {#concept_98689B1E804B43CEA21E3F456107CCD9}

Het dashboard van de Moderatie maakt een lijst van gebeurtenissen door moderator, die u toestaat om hun activiteit te evalueren. Gebruik dit rapport om uw actiefste Moderatoren, en hun gemeenschappelijkste matigingsacties te vinden.

>[!NOTE]
>
>De geautomatiseerde Livefyre moderatie activiteiten zullen voor de moderatornaam Livefyre Systeem worden vermeld.

![](assets/analytics-moderation.png)

## Gebruikers {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Het dashboard Gebruikers geeft de siteactiviteit per gebruiker weer, zodat u kunt analyseren hoe individuele gebruikers met uw site werken. Gebruik dit dashboard om uw meest actieve gebruikers over uw plaats te vinden, en de populairste plaatsactiviteiten te evalueren.

![](assets/analytics-users.png)
