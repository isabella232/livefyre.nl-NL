---
description: Revisies bieden een breed scala aan aanpassingen, zodat u een Revisie-app kunt maken die aan uw behoeften en branding voldoet.
seo-description: Revisies bieden een breed scala aan aanpassingen, zodat u een Revisie-app kunt maken die aan uw behoeften en branding voldoet.
seo-title: Een Revisietoepassing maken
solution: Experience Manager
title: Een Revisietoepassing maken
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Een Revisietoepassing maken{#creating-a-reviews-app}

Revisies bieden een breed scala aan aanpassingen, zodat u een Revisie-app kunt maken die aan uw behoeften en branding voldoet.

Gebruik de Reviews-app door deze als een JS-toepassing op uw site in te sluiten. U kunt geen Revisies-app maken in LiveCyre Studio. Zie [Revisies-integratie](/help/implementation/c-app-integrations/c-reviews-integration.md)voor informatie over het maken van een Revisies-app op uw site.


## Waarderingen {#section_hs5_c4h_21b}

Waarderingen zijn de numerieke waarde die uw gebruikers aan de revisie toewijzen. Elke Controle moet een Classificatie omvatten, die als 5 stersysteem door gebrek wordt getoond. (Terwijl classificaties in de app als 0,5-5 worden weergegeven, slaat Livefyre een verhouding van X/100 op de achtergrond, zodat 1 ster 20/100 is en 2 sterren 40/100. Deze verhouding wordt getoond wanneer het bekijken van de overzichten binnen Studio.)

De beoordelingsschaal van 0,5 tot en met 5 kan worden geconfigureerd tot een rating van 100, waarbij ook halve ratings beschikbaar zijn.

Zie het veld maxRating voor het object Reviews convConfig voor meer informatie.

## Stijl classificatiepictogram {#section_cqn_c4h_21b}

Beoordelingspictogrammen kunnen worden aangepast aan uw merk en stijl.

Zie **[!UICONTROL Configure Star Ratings]** onder Revisies-aanpassing voor meer informatie.

## Beoordelingsafmetingen {#section_cnx_snh_21b}

Beoordelingsdimensies zijn de categorieën waarover uw revisoren uw product of service beoordelen. Voorbeelden van beoordelingsdimensies zijn &#39;prestaties&#39;, &#39;ontwerp&#39;, &#39;kosten&#39;, &#39;totaal&#39; of een andere categorie die u kiest.

Standaard wordt één &quot;algemene&quot; ratingdimensie weergegeven, maar u kunt meerdere ratingafmetingen definiëren en implementeren, zoals in het onderstaande voorbeeld wordt getoond.

Zie het veld RatingDimensions onder Metagegevens verzameling revisie voor meer informatie.

## Tekstvelden controleren {#section_xcm_4nh_21b}

U kunt ook extra tekstvelden toevoegen aan het product of de ervaring die wordt gecontroleerd. (Tekstvelden kunnen bijvoorbeeld Pros en Cons bevatten, of Niet Mappen.) Het nummer, de titel en de standaardtekst voor het veld kunnen worden aangepast. Gebruikers moeten alle tekstvelden invullen, evenals de titel, de instantie en de classificatie van de revisie, om hun revisie te publiceren. Optionele tekstvelden kunnen niet worden opgenomen.

Zie het veld ratingDimensions voor de metagegevens van de revisieverzameling voor meer informatie.

## Overzicht van revisie {#section_ysz_lnh_21b}

Standaard wordt een overzichtssectie boven aan de Revisies-app weergegeven. Deze sectie omvat een visualisatie van de Gemiddelde Classificatie van de Gebruiker en de Onderverdeling van de Classificatie voor de Inzameling van Revisies, die volledige aantallen slechts toont. Deze sectie is alleen-lezen en kan desgewenst worden verborgen.

Zie het veld ratingSummaryEnabled voor het object Reviews convConfig voor meer informatie.

## Filter Spam en Winstgevendheid {#section_hcm_jnh_21b}

De tekst van de Titel en het Lichaam van een Overzicht wordt overgegaan door ons filter van de Filter van het Spam en van de Winst zodra het Overzicht wordt gepost.

## Tekst aanpassen {#section_tjf_hnh_21b}

Tekstreeksen, inclusief knopinfo en labels, kunnen worden aangepast aan de taal of uw merk.

## Reageren op een revisie {#section_yng_fnh_21b}

Gebruikers kunnen in elke Revisieverzameling reageren op hun eigen of andere revisie. Alleen gebruikers die zijn aangemeld, kunnen een reactie op een revisie plaatsen.

De optie voor gebruikers om op een Overzicht te antwoorden wordt toegelaten in Studio. Eigenaars kunnen deze instelling voor het netwerk-, site- of verzamelingsniveau in- en uitschakelen. Moderatoren kunnen deze instelling alleen inschakelen voor hun verzamelingen.

## SocialSync en Curate {#section_llh_2nh_21b}

Omdat Revisies zijn ontworpen om een numerieke waarde toe te voegen voor elk stukje verzonden inhoud, worden SocialSync en Curate niet ondersteund in de Revisies.

## API&#39;s voor revisies {#section_xrh_wmh_21b}

Revisies-API&#39;s zijn beschikbaar zodat u de gemiddelde informatie over de classificatie en de classificatie van gebruikers en de activiteiten van gebruikersbeoordelingen op andere secties van de site kunt weergeven.

[Beoordelingen en beoordelingen](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Met het eindpunt van de Bootstrap-API kan uw revisie worden gelezen door zoekmachines zoals Google, zodat de inhoud en trefwoorden de optimalisatie van uw zoekmachine kunnen verbeteren.

* **[!UICONTROL Average User Ratings]** Met de API Gemiddelde gebruikersbeoordelingen haalt u de gemiddelde gebruikersclassificatie voor een of meer Revisies-verzamelingen op. Zo kunt u een visualisatie van deze gegevens op een indexpagina maken of aan een zoekindexpagina toevoegen.

* **[!UICONTROL Ratings Breakdown]** De indelings-API voor classificaties haalt een uitsplitsing op van alle classificaties voor een specifieke verzameling beoordelingen en stelt u in staat een visualisatie te maken die het aantal revisies weergeeft dat aan elke sterwaardering is gekoppeld.

* **[!UICONTROL User Reviews]** Met de API voor revisies van gebruikers worden de meest recente revisies voor een specifieke gebruiker opgehaald. Deze activiteit kan worden gebruikt om de recensies van een gebruiker op hun openbare profielpagina te tonen.
