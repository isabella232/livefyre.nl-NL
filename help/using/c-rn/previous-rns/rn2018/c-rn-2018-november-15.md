---
description: Release-aantekeningen voor de release van 15 november 2018.
title: Opmerkingen bij de release
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Opmerkingen bij de release{#release-notes}

Release-aantekeningen voor de release van 15 november 2018.

## Nieuwe functies {#section_syx_mdt_wcb}

De volgende nieuwe functies zijn vrijgegeven in de productieversie van deze release:

* **Updates voor zoeken en streamen in Instagram.** U kunt een  *Instagram-* bedrijfsaccount gebruiken voor:

   * Een sociale zoekopdracht op Instagram uitvoeren door gebruiker (gebruiker moet ook een Instagram-zakelijke account zijn).

   * Maak Instagram-streams van een specifieke Instagram-gebruikersaccount (de account moet ook een zakelijke account zijn), inclusief uw eigen account.

   * Rechten aanvragen voor middelen van Instagram via een gedeeltelijk geautomatiseerde workflow.

   * Zie [Informatie over Instagram Accounts](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md) voor informatie over welk type Instagram-accounts u moet instellen en rechten van Instagram aanvragen.

* **Automatische controle van gebruiksrechten vraagt reacties voor zakelijke zoekopdrachten op basis van account.** Alleen voor zoekopdrachten op basis van zakelijke accounts: de mogelijkheid om reacties op verzoeken om rechten automatisch te controleren en de activiteitengeschiedenis in LiveCycle bij te werken, is beschikbaar.

Zie [Instagram Rights Request Manually](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) en [Send a Partially Automated Instagram Rights Request](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md) voor meer informatie over het aanvragen van rechten voor Instagram-accounts.

* **Adobe Target-integratie.** Toegevoegde integratie met Adobe Target zodat u LiveCycle Apps rechtstreeks kunt delen met uw Adobe Target Offers Library. Zie [Doeldocumentatie](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html) voor meer informatie over het gebruik van LiveCycle met Adobe Target.

## Problemen {#section_ehw_ndt_wcb}

De problemen in de volgende tabellen zijn opgelost in deze release.

### Productievrijgave

| Type probleem | Component | Opmerking vrijgeven |
|--- |--- |--- |
| Probleem | AppService: Livefyre-id | Probleem verholpen waarbij bij klikken op [!UICONTROL Reset to Default] het logo niet opnieuw werd ingesteld onder Aanmeldingsmodule in Studio > Integratie-instellingen > Livefyre Identity in de standaardafbeelding. |
| Probleem | Bibliotheek | Probleem verholpen waarbij een video die naar de bibliotheek is geüpload en vervolgens in detail wordt weergegeven, niet correct werd weergegeven. |
| Probleem | Streams | Probleem verholpen waardoor producten niet konden worden weergegeven in een stroomregel. |
| Probleem | Streams | Probleem verholpen waarbij productcodes niet beschikbaar waren voor een stroomregel. |
| Verbetering | Studio | Probleem verholpen waarbij product-id niet werd weergegeven in LiveCyre Studio. |
| Probleem | Studio: ModQ | Probleem verholpen waarbij verwijderde inhoud nog steeds in ModQ werd weergegeven nadat deze was verwijderd. |

### UAT Release

| **Type probleem** | **Component** | **Opmerking vrijgeven** |
|---|---|---|
| Probleem | Sociale component: Carousel | Correctie van een probleem waarbij de koppeling Delen niet reageerde en kopieerde de URL naar behoren in IE11 en Mozilla Firefox. |
