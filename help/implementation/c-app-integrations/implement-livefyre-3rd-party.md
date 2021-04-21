---
description: Maak vanaf het begin livefyre-apps om aangepaste ervaringen en gegevensvisualisaties te maken.
title: LiveCycle integreren in een CMS
exl-id: 05d85792-de97-47b1-90cc-ad7e841754b5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Livefyre implementeren met integratie van derden

Maak vanaf het begin livefyre-apps om aangepaste ervaringen en gegevensvisualisaties te maken.

U kunt een LiveCyre-app helemaal vanaf het begin maken door LiveCycle en sociale gegevens te gebruiken met de API voor Bootstrap en streamen.

Voor LiveCyre Apps die authentificatie vereisen, zie de Integratie van de Identiteit voor informatie over gesteunde derdeauthentificatieplatforms.

U kunt als volgt conversieapps implementeren (opmerkingen, chatten, liveblog, advertenties):

1. Toepassingsintegratie uitvoeren.
a. Creeer een Inzameling die de Token CollectionMeta gebruikt.
b. Integreer LiveCyre-apps met gebruik van de ingesloten codestructuur van Livefyre.js.

   * Zie [Een toepassing insluiten](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) voor meer informatie over het gebruik van de ingesloten codestructuur van Livefyre.js.

   * Zie [Opmerkingen](/help/using/c-about-apps/c-comments/c-comments.md) voor informatie over hoe u de toepassing Comments kunt integreren.

   * Voor informatie over hoe te om Chat te integreren App, zie [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Zie [Live blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md) voor informatie over het integreren van de app Live blog.

   * Voor informatie over hoe te om Sidenotes App te integreren, zie [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Voer authentificatieintegratie uit.
a. Creeer de tokens van de Auteur van de Gebruiker om gebruikersgegevens in Levensstijl over te gaan en op te slaan.
b. Gebruikers- en verificatieplatforms van derden integreren. Voor een lijst van gesteunde platforms, zie [Identiteitsintegratie](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. App-aanpassingen uitvoeren. Pas de opties van Aanpassingen van de app aan om uw branding en stijl aan te passen en douanefunctionaliteit toe te voegen.

U kunt als volgt een visualisatieapp maken (Kaart, Media Wall, Trending, Carousel, Filmstrip, Storify, Feature Card, Mosaic, Opiniepeilingen):

1. Toepassingsintegratie uitvoeren.
a. Creeer een Inzameling die de Token CollectionMeta gebruikt.
b. Integreer LiveCyre-apps met gebruik van de ingesloten codestructuur van Livefyre.js. Zie [Een toepassing insluiten](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) voor meer informatie over het gebruik van de ingesloten codestructuur van Livefyre.js.

   * Voor informatie over hoe te om de Kaart te integreren App, zie [Kaart](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Voor informatie over hoe te om de Muur App van Media te integreren, zie [Muur van Media](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Voor informatie over hoe te om Trending te integreren, zie [Trending](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Voer authentificatieintegratie uit.
a. Creeer de tokens van de Auteur van de Gebruiker om gebruikersgegevens over te gaan en op te slaan in Levfyre.
b. Gebruikers- en verificatieplatforms van derden integreren. Voor een lijst van gesteunde platforms, zie [Identiteitsintegratie](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre biedt geen ondersteuning voor apps voor carrousel, filmstrip, Storify, functiekaart, mozaïek en opiniepeilingen die Livefyre.js gebruiken.

Integreer deze Apps gebruikend [creeer een App](/help/using/c-about-apps/c-create-an-app.md) proces.
