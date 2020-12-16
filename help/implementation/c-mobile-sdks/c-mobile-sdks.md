---
description: Voeg LiveCycle toe aan uw systeemeigen mobiele apps.
seo-description: Voeg LiveCycle toe aan uw systeemeigen mobiele apps.
seo-title: Mobiele SDK's
solution: Experience Manager
title: Mobiele SDK's
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# Mobiele SDK&#39;s{#mobile-sdks}

Voeg LiveCycle toe aan uw systeemeigen mobiele apps.

Er zijn verschillende opties beschikbaar voor mobiele implementaties, afhankelijk van de mate van aanpassing die u wilt uitvoeren:

* Mobiele webtoepassingen
* Livefyre Android- of iOS-SDK&#39;s
* HTTP-API&#39;s

## Mobiele webtoepassingen {#section_t2k_vpb_11b}

Klanten die een webpagina op een mobiel apparaat openen, krijgen automatisch een LiveCycle-inhoudsstroom die is geoptimaliseerd voor mobiele apparaten, zoals de opmaak die is aangepast aan de beperkte schermgrootte en wijzigingen om aanraakgebeurtenissen af te handelen.

>[!NOTE]
>
>Wanneer u een LiveCycle-toepassing gebruikt in een Android WebView, moet de Android-parameter [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) zijn ingesteld op true. Als localStorage niet is ingeschakeld, kan Livefyre een gebruiker niet aanmelden bij de Livefyre-app.

Voor optimalisatie voor mobiele apparaten beperkt LiveCyre de functie Opmerkingen, Live Blog en Chat App die is ingesteld op:

* Post
* Bewerken
* Markering
* leuk
* Reageren
* Aantal listeners
* Aantal opmerkingen
* Inline in afwachting van Moderatie
* Hovercards
* Opmerkingen bovenaan
* Hot Threads
* Opmerkingen in wachtrij

Als u in Mobile Web Apps op de naam van een auteur klikt, worden de gegevens op de hyperlink op een nieuwe pagina geopend.

## Livefyre Android SDK of iOS SDK {#section_zdz_spb_11b}

Livefyre biedt ook twee mobiele SDK&#39;s: een iOS SDK en een Android SDK. Deze SDK&#39;s zijn wikkelaars rondom onze HTTP-eindpunten en zijn ontworpen om een eenvoudigere methode te bieden voor het verzenden en ontvangen van gegevens. Er wordt geen interface geleverd met deze SDK&#39;s, waardoor u flexibeler kunt werken met de manier waarop de inhoud wordt weergegeven en gebruikt in uw mobiele app.

De SDK&#39;s van Android en iOS ondersteunen de volgende functies voor Opmerkingen, Live Blog en Chat:

| iOS-functies: | Android-functies: |
|--- |--- |
| <ul><li> Post </li><li>Bewerken </li><li>Markering </li><li>leuk </li><li>Reageren </li><li>Hot Threads</li></ul> | <ul><li>Post </li><li>Bewerken </li><li>leuk </li><li>Reageren </li><li>Hot Threads</li></ul> |

## HTTP-API&#39;s {#section_yqb_qpb_11b}

De HTTP APIs is de groep eindpunten die u toestaat om gesprekken en inhoud op het platform van de Levensstijl tot stand te brengen. Het geeft alle Livefyre ook de mogelijkheid om de box streams te verlaten. Hoewel deze oplossing meer ontwikkelingstijd van uw engineeringteam vergt, biedt deze meer flexibiliteit bij het gebruik van de Livefyre-productsuite en maakt native mobiele integratie mogelijk.

>[!IMPORTANT]
>
>**Creëer** geen verificatietokens voor gebruikers binnen de mobiele client, omdat u hiervoor de sleutel voor het geheim netwerk van LiveCycle in een onbeveiligde app beschikbaar moet maken. Voor een robuustere en veiligere oplossing, zie de Tokens van de Authentificatie van de Gebruiker sectie.

