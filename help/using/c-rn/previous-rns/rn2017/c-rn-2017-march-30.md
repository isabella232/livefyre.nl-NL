---
description: Opmerkingen bij de release van 30 maart 2017.
title: 30 maart 2017
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 30 maart 2017{#march}

Opmerkingen bij de release van 30 maart 2017.

## Productievrijgave

| Type probleem | Component | Opmerking vrijgeven |
|---|---|---|
| Bug | Sociale zoekfunctie | Het probleem waarbij publicatie van opgeslagen YouTube-elementen in sociale zoekopdracht werd voorkomen, is opgelost. |
| Verbetering | Sociale synchronisatie | Vervangen Twitter Social Sync. |
| Verbetering | Storiseren 2 | Er is een uitbreiding toegevoegd om het bericht &quot;Geen resultaten gevonden&quot; weer te geven bij het zoeken naar Facebook Topic wanneer er geen resultaten worden gevonden. |
| Verbetering | Streams | Samenvattingsregels voor VEILIGE regels toegevoegd onder aan een Twitter Stream-pagina. |
| Bug | Streams | Er is een uitbreiding toegevoegd om het selectievakje &quot;geverifieerde gebruiker&quot; op Twitter Stream Rules zichtbaar uit te schakelen wanneer uitgesloten auteurs worden aangeboden. |
| Bug | Streams | Oplossing voor een bug waarbij het gebruik van ANDing-trefwoorden en een locatiefilter in een Twitter-regel waren toegestaan. |
| Bug | Studio | Het probleem waarbij de functietag niet correct kon worden opgeslagen tijdens de toepassing, is opgelost. |

## UAT Release

| Type probleem | Component | Opmerking vrijgeven |
|---|---|---|
| Bug | App-inhoud | Veranderde het gedrag van &quot;Meer Info&quot;dusdanig dat als er veelvoudige Anoniem markeringsgebeurtenissen op een bepaald stuk van inhoud zijn, de vroegste gebeurtenis altijd wordt getoond. |
| Bug | Bibliotheek | Het probleem waarbij bibliotheekzoekopdrachten met hashtags soms mislukten, is opgelost. |
| Bug | Kaarten | Oplossing voor een probleem in Maps ter ondersteuning van een groot aantal inhoud in clusters op iOS-apparaten. |
| Verbetering | Mozaïek | Mozaïek-apps configureren zodat u overal op een inhoudskaart kunt klikken om het modaal te openen met animatietype `none` in de ontwerper en `cardAnimation: 'off'`indien geïnstantieerd via de SDK. |
| Bug | Mozaïek | Probleem verholpen waarbij gebruikers mozaïektoepassingen konden wijzigen in Designer. |
| Verbetering | Verzoek om rechten | Er is een nieuwe aanvraagstatus voor rechten met de naam &quot;Verzoek mislukt&quot; toegevoegd om te markeren wanneer de aanvraagberichten voor rechten niet worden verzonden. |
| Verbetering | Instellingen | Toegevoegd de capaciteit voor klanten om de Regels van de Moderatie van SPAM in Montages tot stand te brengen. |
| Verbetering | Sociale zoekfunctie | Het probleem dat ervoor zorgde dat VK.com-berichten niet konden worden weergegeven via sociale URL-zoekopdrachten, is opgelost. |
| Verbetering | Sociale zoekfunctie | Als u zoekt naar Instagram-inhoud van Studio en de zoekopdracht is veroorzaakt door een verlopen Instagram API-token, wordt het foutbericht nu als zodanig weergegeven. |
| Bug | Streams | Oplossing voor een probleem dat ertoe leidde dat een banner &quot;App accepteert geen nieuwe inhoud&quot; onjuist werd weergegeven boven op streamregelpagina&#39;s. |
| Verbetering | Streams | Gewijzigd het gebrek van pas gecreëerde stroomregels om VEILIGE Regels toe te passen wanneer toepasselijk. |
| Verbetering | Streams (voorheen Curate Rules) | De optie Alleen wijnstokken is verwijderd uit de Twitter Stream/Curate-regels, omdat wijnstokken nu worden weergegeven als Twitter-video&#39;s. |
| Bug | Studio Shell | Probleem verholpen zodat Livefyre Studio wordt geladen als https:// expliciet aan de URL is toegevoegd. |
