---
description: 'null'
seo-description: 'null'
seo-title: SSL-handhaving
solution: Experience Manager
title: SSL-handhaving
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---


# SSL-handhaving{#ssl-enforcement}

Om ervoor te zorgen dat uw gegevens veilig blijven, wordt HTTP vervangen door HTTPS. Adobe Livefyre zal alle HTTP en onveilige SSL/TLS ciphers volledig onbruikbaar maken tegen eind Augustus 2018. Dit is een Adobe Standard die is ontworpen om de privacy van u en uw gebruikers te beschermen.

## Wie heeft er last van? {#section_jf2_4yz_kcb}

Dit kan gevolgen hebben voor Livefyre-klanten die:

* Server-aan-server vraag van hun CRM, CMS, WordPress, of andere Cliënt.
* Mobiele integratie (Android- en iOS-toepassingen)
* Aangepaste toepassingen of aangepaste code

## Wat moet ik doen? {#section_unv_dc5_kcb}

1. Alle klanten van het Levensonderhoud moeten met alle APIs via HTTPS voor al verkeer communiceren, met inbegrip van:

   * Integraties van server naar server (CRM, CMS, WordPress, enz.)
   * Mobiele integratie (Android- en iOS-toepassingen)
   * Aangepaste toepassingen (Streamhub SDK of direct gecodeerd).

1. Server naar server en mobiele HTTP-clients moeten TLS 1.2 ondersteunen
1. Wijzig de hostnamen van `{*}.<network>.fyre.co` in `<network>.{*}.fyre.co`. De hostnaam `example.network.fyre.co` verandert bijvoorbeeld in `network.`example.fyre.co&quot;. Bijvoorbeeld:

   * `bootstrap.<network_name>.fyre.co` tot  `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` tot  `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` tot  `<network_name>.admin.fyre.co`

## Hoe weet ik of ik de wijzigingen heb aangebracht? {#section_sqk_5d5_kcb}

U kunt al HTTPS gebruiken, maar LiveCycle raadt u aan om de controle te verdubbelen, vooral als u hebt:

* Server-aan-server vraag van uw CMS of CRM.
* Aangepaste code of gebruik SDK&#39;s voor aangepaste apps in JavaScript of Mobile.
* Als uw integratie meer dan een jaar oud is.
* Als de technologie in uw stapel ouder is dan één jaar.

Zelfs als u al HTTPS gebruikt, moet u controleren of uw API-clients TLS 1.2 ondersteunen.

## Hoe kan ik verifiëren dat mijn API-clients TLS 1.2 ondersteunen? {#section_nd1_j25_kcb}

Een persoon die werkt aan de ontwikkeling van uw site kan:

* Identificeer de clientsoftware.
* Identificeer de versie.
* Lees de documentatie om ervoor te zorgen dat de API-client ondersteuning biedt voor TLS 1.2.
* Schakel indien nodig de foutopsporingsmodus in.

## Java-ondersteuning voor TLS 1.2 {#section_lwn_rwk_ycb}

Oracle en OpenJDK JVMs voor Java 8 en later worden gevormd om TLS 1.2, door gebrek, voor alle SSL verbindingen te gebruiken. U hoeft geen aanvullende actie te ondernemen als u Java 8 of hoger gebruikt.

Gebruikers van Java 7 of eerder dienen openbare documentatie te raadplegen over de manier waarop TLS 1.2 kan worden ingeschakeld.

## Waarom moet ik mijn gastheernamen veranderen? {#section_d5q_p25_kcb}

Livefyre heeft geen SSL-certificaten op `{*}.<network>.fyre.co`-domeinen. Als u alleen de URL wijzigt in HTTPS, wordt de toepassing verbroken.

## Moet ik een upgrade uitvoeren naar de nieuwste versie van de Livefyre SDK&#39;s? {#section_dw5_s25_kcb}

Nee. U kunt de code in plaats daarvan repareren. Als u de code wilt repareren, wijzigt u enkele statische tekenreeksen en maakt u de code opnieuw. Als uw HTTP-client verouderd is, moet u dat ook bijwerken of een andere client gebruiken.

## Hoe lang duurt dit? {#section_lgd_v25_kcb}

De duur van dit neemt van uw opstelling af. Als u een eenvoudige implementatie hebt, zou het weinig tijd moeten vergen om te bevestigen. Als u vele aanpassingen hebt, zult u bijgewerkte code aan uw servers of nieuwe Apps aan App Stores moeten testen en opstellen. Voor de beste resultaten raden we u aan een eerste controle van het werk uit te voeren, zodat u uw werk op langere termijn kunt plannen.

## Wat is de tijdlijn voor het voltooien van dit werk? {#section_kgk_w25_kcb}

Livefyre zal haven 80 (HTTP) aan onze diensten tegen eind augustus 2018 onbruikbaar maken en slechts verbindingen aan 443 (HTTPS) steunen. Browsers en andere clients, die HTTP proberen te gebruiken, zullen mislukken.

## Wanneer moet ik dit werk voltooien? {#section_rvb_x25_kcb}

Alle klanten moeten uiterlijk eind juli 2018 HTTPS gebruiken. Neem contact op met ons team op prioritysupport@livefyre.com als u deze deadline niet kunt halen.
