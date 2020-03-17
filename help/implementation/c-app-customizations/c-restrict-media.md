---
description: Beperk het type media dat in de App-stream terechtkomt.
seo-description: Beperk het type media dat in de App-stream terechtkomt.
seo-title: Media beperken
solution: Experience Manager
title: Media beperken
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Media beperken{#restrict-media}

Beperk het type media dat in de App-stream terechtkomt.

Standaard kunnen alle mediabijlagen worden ingesloten in apps. Met LiveCycle kunt u deze optie wijzigen om te voorkomen dat gebruikers geselecteerde typen bijlagen naar uw apps posten.

>[!NOTE]
>
>Livefyre werkt samen met Embedly voor media-integratie. Zie Content Integration > Embedly Integration voor meer informatie. Neem contact op met uw technische accountmanager voor vragen over het uitbreiden van koppelingen of bronnen.

In dit voorbeeld worden YouTube- en Vimeo-insluiten van uw commentaarstream geblokkeerd:

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

Bij het laden van het gesprek:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

