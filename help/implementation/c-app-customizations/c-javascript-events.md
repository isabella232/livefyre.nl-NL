---
description: De beschikbare gebeurtenissen waaraan u JavaScript voor conversatieapps kunt binden (bijvoorbeeld Comments, Chat, Live Blog, Reviews en Sidenotes).
title: Definities en voorbeelden van JavaScript-gebeurtenissen
exl-id: 5b865974-69aa-4d51-ac26-60f1d8a114fc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 11%

---

# Definities en voorbeelden van JavaScript-gebeurtenissen{#javascript-events-definitions-and-examples}

De beschikbare gebeurtenissen waaraan u JavaScript voor conversatieapps kunt binden (bijvoorbeeld Comments, Chat, Live Blog, Reviews en Sidenotes).

LiveCycle biedt JavaScript-gebeurtenissen om de gebruikersactiviteit in uw LiveCycle-apps te volgen. U kunt bijvoorbeeld de pagina bijwerken wanneer gebruikers inhoud willen of delen naar Twitter of Facebook, of wanneer nieuwe inhoud wordt geplaatst.

Met LiveCycle kunt u ook gebeurtenissen toevoegen aan analytische integratie van derden (Adobe Analytics JS, Google Analytics, Dynamic Tag Management, enzovoort) om App-gebeurtenissen bij te houden. Voor meer informatie, werk met uw derde integratiemanager om de correcte gebeurtenissen te leveren.

Om aan deze gebeurtenissen te binden, voeg de volgende code aan de pagina toe wanneer het concretiseren van uw App op een pagina. Vervang de naam van de gebeurtenis voor `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Gegevensobjecten worden verschaft voor alle gebeurtenishandlers. Voorbeeldgegevensobjecten volgen elke gebeurtenis.

## commentPosted {#section_qfr_51p_xz}

Een gebruiker heeft een opmerking geplaatst.

* Een bovenliggend item van null is een nieuwe opmerking.
* Een bovenliggend item van Geen is een opmerking die is bewerkt.
* Een getal voor bovenliggend element is de bovenliggende id van het antwoord.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## commentFlagged {#section_szy_s1p_xz}

Een gebruiker heeft een opmerking gemarkeerd.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

Een gebruiker vond een opmerking leuk.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Een gebruiker heeft een opmerking van de stream gedeeld. (Deze gebeurtenis wordt niet geactiveerd wanneer gebruikers deze delen via de commentaareditor.) Deze gebeurtenis wordt geactiveerd wanneer op de knop Delen wordt geklikt.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

Het totale aantal zichtbare opmerkingen in dit gesprek is gewijzigd (verhoogd of verlaagd).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

Een gebruiker heeft zich aangemeld.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

Een gebruiker heeft zich afgemeld.

gegevens zijn ongedefinieerd.

## socialMention {#section_a1w_tz4_xz}

Een gebruiker heeft een @comment in een commentaar opgenomen. Retourneert een array van de volgende elementen:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

Een moderator-gebruiker heeft een opmerking toegevoegd. Retourneert een array van de volgende elementen:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

De commentaarstroom is geladen, en de aanvankelijke reeks inhoud is opgehaald van de server en aan de gebruiker getoond.

gegevens zijn ongedefinieerd.

## showMore {#section_pqg_nz4_xz}

Een gebruiker heeft op de knop **[!UICONTROL Show More]** geklikt.

gegevens zijn ongedefinieerd.

## userFollowed {#section_xxw_jz4_xz}

Retourneert true wanneer de gebruiker op de knop **[!UICONTROL Follow]** klikt en false wanneer inhoud naar de stream wordt gepost.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnfollowed {#section_wm1_gz4_xz}

Retourneert true wanneer een gebruiker op de knop **Onvolgen** klikt en false wanneer inhoud naar de stream wordt gepost.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```
