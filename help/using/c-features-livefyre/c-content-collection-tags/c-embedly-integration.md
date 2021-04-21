---
description: Gebruik embed.ly om meerdere mediaformaten direct in de app te tonen.
title: Embedly-integratie
exl-id: 859fe306-367e-4207-b9f7-c730ba0cd24d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 5%

---

# Embedly-integratie {#embedly-integration}

Gebruik `embed.ly` om veelvoudige media formaten, direct in App te tonen.

Voor een betere toegang tot ingesloten media-inhoud uit verschillende bronnen, zoals Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify en Tumblr, gebruiken LiveCyre Apps Embedly als een externe provider voor URL-uitbreiding. Als een gebruiker of moderator een gesteunde verbinding in een post omvat, zullen de media inbegrepen in de verbinding wanneer gepost aan de Inzameling uitbreiden.

Dit biedt Live Apps toegang tot de meer dan 250 verschillende ingesloten media-opties die insluiten ondersteunen.

>[!NOTE]
>
>Livefyre breidt slechts een ondergroep van Embedly&#39;s volledige leverancierslijst uit. Ingesloten afbeeldingen worden alleen op HTTPS-pagina&#39;s groter als de provider Twitter, YouTube, Imgur, Wine, Wikipedia of SoundCloud is. Neem contact op met uw technische accountmanager voor verdere vragen over het uitbreiden van koppelingen of bronnen.

Deze pagina bevat voorbeelden van populaire ingesloten mediatypen en hun acceptabele URL-patronen. `Embed.ly` voegt voortdurend nieuwe bronnen toe. Ga naar `https://embed.ly/embed/features/providers` voor een volledige lijst met providers.

>[!NOTE]
>
>Voor de indeling Insluiten is een volledige permalink vereist. Verkorte koppelingen werken niet.

Alleen openbaar zichtbare inhoud kan worden ingesloten. Als u probeert inhoud in te sluiten die niet openbaar is, wordt de koppeling naar de inhoud weergegeven in het blogbericht en wordt het pictogram voor een plaatsaanduiding weergegeven. Als op de koppeling wordt geklikt, verschijnt er een foutbericht van de service waar de inhoud wordt gehost, zoals een Facebook-bericht voor een foto die alleen voor vrienden bestemd is. Neem contact op met uw accountmanager als u merkt dat media niet naar behoren is uitgevouwen.

## Voorbeeld van Ingebedde URL&#39;s

| Type | Provider | URL&#39;s |
|--- |--- |--- |
| Kaarten | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Opmerking**: URL moet beginnen met  `http` en niet  `https.` |
| Sociale netwerken | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Foto&#39;s | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (service voor het uploaden van inhoud van Hoosuite) | `https://ow.ly/i/*` |
| Opiniepeilingen | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotiseren | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Toepassingen die deze functie gebruiken:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Opmerkingen](/help/using/c-about-apps/c-comments/c-comments.md)
* [Functiekaart](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Kaart](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mediumwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mozaïek](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Opiniepeilingen](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Revisies](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storiseren 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Trend](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Knop Uploaden](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
