---
description: U kunt naar gebeurtenissen luisteren in een instantie van Sidenotes.
seo-description: U kunt naar gebeurtenissen luisteren in een instantie van Sidenotes.
seo-title: Sidenotes App Events
solution: Experience Manager
title: Sidenotes App Events
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Sidenotes App Events {#sidenotes-app-events}

U kunt naar gebeurtenissen luisteren in een instantie van Sidenotes.

Callbacks kunnen bij de `onmethod` en niet geregistreerd met de `removeListener` methode worden geregistreerd. Een `once` methode is beschikbaar voor gemak als de callback slechts eenmaal moet worden geroepen en dan niet geregistreerd.

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
| sidenotes.commentFlagged | Wordt geactiveerd wanneer een opmerking is gemarkeerd. Gegevens bevatten: <br><ul><li>`targetId`: id van de opmerking die is gemarkeerd</li><li>`type`: markering type string `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Wordt geactiveerd wanneer een opmerking is geplaatst. Gegevens bevatten: <br><ul><li> `authorId`: id van de auteur van de opmerking </li><li>`bodyHtml`: hoofdtekst van de opmerking </li><li> `parent`: id van het bovenliggende element van de opmerking of null</li></ul> |
| `sidenotes.commentShared` | Wordt geactiveerd wanneer een opmerking is gedeeld. Gegevens bevatten: <br><ul><li>`targetId`: id van de opmerking die is gedeeld </li><li> `sharedToFacebook`: of de opmerking is gedeeld aan Facebook </li><li>`sharedToTwitter`: of de opmerking is gedeeld aan Twitter</li></ul> |
| `sidenotes.commentVoted` | Wordt geactiveerd wanneer er over een opmerking wordt gestemd. Gegevens bevatten: <br><ul><li>`targetId`: id van de opmerking waarover is gestemd </li><li> `targetAuthorId`: id van de auteur van wie het commentaar is aangenomen</li><li> `type`: type numerieke stemming: 0: &quot;clear&quot;, 1: &quot;upvoice&quot;, of 2: &quot;neerslag&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Wordt geactiveerd wanneer een gebruiker zich aanmeldt. Gegevens bevatten: <br><ul><li>`avatar`: avatar url voor de gebruiker </li><li>`displayName`: weergavenaam van de gebruiker</li><li>`id`: id van de gebruiker</li><li> `isModerator`: of de gebruiker een moderator van de huidige inzameling is</li></ul> |
| `sidenotes.userLoggedOut` | Wordt geactiveerd wanneer een gebruiker zich afmeldt |
