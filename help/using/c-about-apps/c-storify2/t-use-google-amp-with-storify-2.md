---
description: Gebruik Live-API's om Google AMP-functionaliteit toe te voegen aan uw Storify 2-pagina om de inhoud interactief en SEO-vriendelijk te houden.
title: Google AMP gebruiken met Storify 2
exl-id: 2fee8655-ac9f-484e-a042-9b7ac7151fcc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Google AMP gebruiken met Storify 2{#use-google-amp-with-storify}

Gebruik Live-API&#39;s om Google AMP-functionaliteit toe te voegen aan uw Storify 2-pagina om de inhoud interactief en SEO-vriendelijk te houden.

Als u Google AMP met Storify 2 wilt gebruiken, moet u een pagina voor uw Storify 2-app maken met Google AMP-opmaakcodes.

De AMP-versie van de app vraagt om updates vanaf de oorspronkelijke pagina (gebruik de parameter **pollInterval** in de API **amp-live-list** om het interval voor updateverzoeken in te stellen). Om ervoor te zorgen dat bezoekers op uw AMP-pagina snel de meest actuele inhoud krijgen, houdt u een TTL met lage cache op uw Storify 2 AMP-pagina&#39;s.

Niet-afbeeldingselementen (bijvoorbeeld video&#39;s) die zijn opgenomen als posts in een app voor Storify 2, moeten HTTPS gebruiken zoals opgegeven in de AMP-specificatie. AMP-URL&#39;s die gebruikmaken van het Google Cloud Content Delivery Network (CDN) gebruiken HTTPS.

Google AMP gebruiken met Storify 2:

1. Maak een door AMP gevalideerde sjabloon op uw site.
1. Gebruik een of meer van de volgende Google AMP-API&#39;s om uw Google AMP-pagina aan te passen:
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframe om de Storify 2-weergave aan te passen
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) List om het tijdinterval voor updates aan te passen
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) shareto toevoegen om een knop voor sociaal delen toe te voegen
1. Neem de inhoud van de volgende AMP-pagina Storify 2 op in de CSS voor uw Storify 2-pagina in de tag `<style amp-custom>`: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Neem de inhoud van de volgende API voor AMP-markering voor Storify 2 op in de Google AMP-sjabloon: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` waarbij {APP_ID} de toepassings-id is voor de app Storify 2 in LiveCycle Studio.
   1. De enige queryparameter is **pollInterval**. Dit is het interval waarin de toepassing controleert op updates (ingesteld in milliseconden).
   1. De URL bevat inhoud van de meest recente posts (zoals tweets, video&#39;s, enz.)
   1. De uitgeverspagina moet inhoud van deze URL krijgen net zo vaak als u wilt dat de Google AMP-pagina wordt bijgewerkt.
