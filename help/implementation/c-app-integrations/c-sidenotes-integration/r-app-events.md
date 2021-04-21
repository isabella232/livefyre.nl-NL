---
description: U kunt naar gebeurtenissen luisteren in een instantie van Sidenotes.
title: Sidenotes App Events
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Sidenotes App Events {#sidenotes-app-events}

U kunt naar gebeurtenissen luisteren in een instantie van Sidenotes.

Callbacks kunnen met `onmethod` worden geregistreerd en unregistered met de `removeListener` methode. Een `once` methode is beschikbaar voor gemak als callback slechts eenmaal moet worden geroepen en dan unregistered.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Zie de pagina JavaScript-gebeurtenissen in de sectie Referentie voor meer informatie over LiveCycle-gebeurtenissen.

| Sleutel | Beschrijving |
|--- |--- |
| sidenotes.initialized | Wordt geactiveerd wanneer de app wordt geïnstantieerd, gegevens bevat en zich op de pagina bevindt. |
| sidenotes.commentFlagged | Wordt geactiveerd wanneer een opmerking is gemarkeerd. Gegevens bevatten: <br><ul><li>`targetId`: id van de opmerking die is gemarkeerd</li><li>`type`: markering type string  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Wordt geactiveerd wanneer een opmerking is geplaatst. Gegevens bevatten: <br><ul><li> `authorId`: id van de auteur van de opmerking </li><li>`bodyHtml`: hoofdtekst van de opmerking </li><li> `parent`: id van het bovenliggende element van de opmerking of null</li></ul> |
| `sidenotes.commentShared` | Wordt geactiveerd wanneer een opmerking is gedeeld. Gegevens bevatten: <br><ul><li>`targetId`: id van de opmerking die is gedeeld </li><li> `sharedToFacebook`: of de opmerking aan Facebook is doorgegeven </li><li>`sharedToTwitter`: of de opmerking aan Twitter is doorgegeven</li></ul> |
| `sidenotes.commentVoted` | Wordt geactiveerd wanneer er over een opmerking wordt gestemd. Gegevens bevatten: <br><ul><li>`targetId`: id van de opmerking waarover is gestemd </li><li> `targetAuthorId`: id van de auteur van wie het commentaar is aangenomen</li><li> `type`: type numerieke stemming: 0: &quot;clear&quot;, 1: &quot;upvoice&quot;, of 2: &quot;neerslag&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Wordt geactiveerd wanneer een gebruiker zich aanmeldt. Gegevens bevatten: <br><ul><li>`avatar`: avatar url voor de gebruiker </li><li>`displayName`: weergavenaam van de gebruiker</li><li>`id`: id van de gebruiker</li><li> `isModerator`: of de gebruiker een moderator van de huidige inzameling is</li></ul> |
| `sidenotes.userLoggedOut` | Wordt geactiveerd wanneer een gebruiker zich afmeldt |
