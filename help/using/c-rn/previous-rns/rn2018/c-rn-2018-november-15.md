---
description: Release-aantekeningen voor de release van 15 november 2018.
seo-description: Release-aantekeningen voor de release van 15 november 2018.
seo-title: Opmerkingen bij de release
solution: Experience Manager
title: Opmerkingen bij de release
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: 573e815799fbae2c2c4f1d98a01ea0ae04108a34

---


# Opmerkingen bij de release{#release-notes}

Release-aantekeningen voor de release van 15 november 2018.

## Nieuwe functies {#section_syx_mdt_wcb}

De volgende nieuwe functies zijn vrijgegeven in de productieversie van deze release:

* **Updates voor zoeken en streamen in Instagram.** U kunt een *zakelijke account* voor Installagram gebruiken:

   * Een sociale zoekopdracht uitvoeren op gebruiker (de gebruiker moet ook een zakelijke account in Instagram zijn).

   * Instagramstreams maken van een specifieke Instagram-gebruikersaccount (de account moet ook een zakelijke account zijn), inclusief uw eigen account.

   * Rechten voor elementen aanvragen vanaf Instagram met behulp van een gedeeltelijk geautomatiseerde workflow.

   * Zie [Informatie over Instagram-accounts](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)voor informatie over welk type Instagram-accounts u moet instellen en rechten van Instagram wilt aanvragen.

* **Automatische controle van gebruiksrechten vraagt reacties voor zakelijke zoekopdrachten op basis van account.** Alleen voor zoekopdrachten op basis van zakelijke accounts: de mogelijkheid om reacties op verzoeken om rechten automatisch te controleren en de activiteitengeschiedenis in LiveCycle bij te werken, is beschikbaar.

Voor meer informatie over hoe te om rechten voor de rekeningen van het Installagram te verzoeken, zie de Verzoek van de Rechten van het Installagram manueel [verzenden en een Gedeeltelijk-Geautomatiseerde Verzoek](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) van de Rechten van het Installagram [](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)verzenden.

* **Adobe Target-integratie.** Toegevoegde integratie met Adobe Target waarmee u LiveCyre-apps rechtstreeks kunt delen met uw Adobe Target-bibliotheek. Raadpleeg de documentatie bij [Target voor meer informatie over het gebruik van LiveCycle met Adobe Target](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html).

## Problemen {#section_ehw_ndt_wcb}

De problemen in de volgende tabellen zijn opgelost in deze release.

### Productievrijgave

| Type probleem | Component | Opmerking vrijgeven |
|--- |--- |--- |
| Probleem | AppService: Livefyre-id | Probleem verholpen waarbij klikken op [! UICONTROL het Terugstellen aan Standaard] stelde het embleem onder Login Modal in Studio > de Montages van de Integratie > Identiteit van de Levensstijl aan het standaardbeeld niet terug. |
| Probleem | Bibliotheek | Probleem verholpen waarbij een video die naar de bibliotheek is geüpload en vervolgens in detail wordt weergegeven, niet correct werd weergegeven. |
| Probleem | Streams | Probleem verholpen waardoor producten niet konden worden weergegeven in een stroomregel. |
| Probleem | Streams | Probleem verholpen waarbij productcodes niet beschikbaar waren voor een stroomregel. |
| Verbetering | Studio | Probleem verholpen waarbij product-id niet werd weergegeven in LiveCyre Studio. |
| Probleem | Studio: ModQ | Probleem verholpen waarbij verwijderde inhoud nog steeds in ModQ werd weergegeven nadat deze was verwijderd. |

### UAT Release

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Probleem | Sociale component: Carousel | Correctie van een probleem waarbij de koppeling Delen niet reageerde en kopieerde de URL naar behoren in IE11 en Mozilla Firefox. |