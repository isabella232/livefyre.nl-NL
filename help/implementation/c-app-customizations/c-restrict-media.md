---
description: Beperk het type media dat in de App-stream terechtkomt.
title: Media beperken
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

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
