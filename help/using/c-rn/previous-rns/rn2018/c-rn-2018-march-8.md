---
description: Opmerkingen bij de release van 8 maart 2018.
title: 8 maart 2018
exl-id: 46d4a425-17e0-48a2-a596-5cc7163f9edd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# 8 maart 2018{#march}

Opmerkingen bij de release van 8 maart 2018.

## Nieuwe functies {#section_syx_mdt_wcb}

De volgende functies zijn nieuw in de productieversie van deze release:

* **Apps worden verwijderd. **De mogelijkheid om Apps in Studio te verwijderen is toegevoegd, zodat gebruikers de App-lijst beter kunnen beheren. Als u een app verwijdert, wordt deze uit de tabel verwijderd, maar wordt de app niet van uw site verwijderd. De app blijft inhoud van een stream ontvangen als dit is geconfigureerd.

## Problemen {#section_ehw_ndt_wcb}

De problemen in de volgende tabellen zijn opgelost in deze release.

## Productievrijgave

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Bug | Opiniepeilingen | Gewijzigde opiniepeilingen om uitsluitend HTTPS te gebruiken. Eerder mochten opiniepeilingen nog steeds worden gebruikt met HTTP. |
| Bug | Studio | Probleem verholpen die het modale venster veroorzaakte dat aankondigingen weergaf wanneer u zich aanmeldt bij Studio om te groot weer te geven op schermen met een lage resolutie. |

## UAT Release

| Type probleem | Component | Opmerking vrijgeven |
|--- |--- |--- |
| Verbetering | Filmstrip | De volgende toegankelijkheidsfuncties voor filmstrip zijn bijgewerkt: <br><ul><li>Pijlen links/rechts, gecorrigeerd van &lt;div> naar &lt;button> </li><li>De voorvertoning van het afbeeldingselement is gewijzigd van een minder beschrijvend ARIA-label met de naam &quot;Gekoppelde foto openen&quot; in een label dat de naam van het platform en de tekst na de presentatie leest.</li></ul> |
| Bug | Mediumwand | Probleem verholpen met Media Wall waarbij niet op tags kon worden geklikt wanneer een Instagram-post werd toegevoegd van een streaming regel. |
| Verbetering | Mediumwand | Verbeterde toegankelijkheid van de mediamuur op de volgende manieren: <br><ul><li>Als u modaliteiten opent en sluit via toetsenbordopdrachten, wordt de focus niet meer naar de bovenkant van de pagina verplaatst. In plaats daarvan blijft de focus op het element dat het laatst is gefocust vóór de modale pop-up.</li><li>U kunt met de Enter-toets op het toetsenbord de knop Meer laden als tabbladen gebruiken en activeren.</li></ul> |
| Bug | Rights Management | Probleem verholpen waarbij de aanvraag voor rechten niet modaal kon worden weergegeven nadat rechten voor een Instagram-element waren verleend. |
