---
description: Gebruik JavaScript-gebeurtenissen om te luisteren naar gebeurtenissen die in een mediamuur optreden en deze naar het hulpprogramma Analytics van uw keuze te verzenden.
seo-description: Gebruik JavaScript-gebeurtenissen om te luisteren naar gebeurtenissen die in een mediamuur optreden en deze naar het hulpprogramma Analytics van uw keuze te verzenden.
seo-title: Javascript-gebeurtenissen voor mediamuur
solution: Experience Manager
title: Javascript-gebeurtenissen voor mediamuur
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# Javascript-gebeurtenissen voor mediamuur{#javascript-events-for-media-wall}

Gebruik JavaScript-gebeurtenissen om te luisteren naar gebeurtenissen die in een mediamuur optreden en deze naar het hulpprogramma Analytics van uw keuze te verzenden.

LiveCycle biedt JavaScript-gebeurtenissen om de gebruikersactiviteit in uw LiveCycle-apps te volgen. U kunt bijvoorbeeld de pagina bijwerken wanneer gebruikers inhoud willen of delen naar Twitter of Facebook, of wanneer nieuwe inhoud wordt geplaatst.

Hier is een voorbeeld van hoe u de gebeurtenissen kunt ontvangen. Vervang `console.log` door uw code om de gebeurtenis toe te wijzen en naar uw analytische integratie te verzenden (Dynamic Tag Management, Adobe Analytics JS, Google Analytics, enz.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lijst met ondersteunde Media Wall-gebeurtenissen:

## Media Wall-gebeurtenissen

| Gebeurtenis | Definitie |
|---|---|
| `Init` | Wanneer een mediamuur op een pagina is opgenomen. |
| `Load` | Wanneer de mediamuur ongeacht de positie op een pagina is geladen. |
| `PostButtonClick` | Wanneer een gebruiker op een Upload Knoop op een Muur van Media klikt. |
| `RequestMore` | Wanneer de gebruiker meer inhoud in een Muur van Media laadt. |
| `TwitterReplyClick` | Wanneer een gebruiker op de knop Reageren op Twitter klikt vanuit de mediamuur. |
| `TwitterRetweetClick` | Wanneer een gebruiker op de knop Twitter Retweet klikt vanuit de mediamuur. |
| `TwitterLikeClick` | Wanneer een gebruiker op de knop Twitter like/Favorite klikt vanuit de mediamuur. |
| `ModalView` | Wanneer de gebruiker klikt om de inhoud van de Muur van Media in een groter modaal venster te bekijken. |
| `Like` | Wanneer een gebruiker de als knoop van de Muur van Media klikt. |
| `ShareButtonClick` | Wanneer een gebruiker op de aandeelknoop op een kaart van de Muur van Media klikt. |
| `ShareURL` | Wanneer Delen naar URL-tekstgebied is geselecteerd/gekopieerd vanuit de mediamuur. |
| `ShareFacebook` | Wanneer u op Delen op Facebook klikt via de mediamuur. |
| `ShareTwitter` | Wanneer u op Delen op Twitter klikt via de mediamuur. |
