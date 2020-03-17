---
description: Voeg aangepaste handelingen toe aan uw LiveCycle-apps.
seo-description: Voeg aangepaste handelingen toe aan uw LiveCycle-apps.
seo-title: Aangepaste knoppen toevoegen
solution: Experience Manager
title: Aangepaste knoppen toevoegen
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aangepaste knoppen toevoegen{#add-custom-buttons}

Voeg aangepaste handelingen toe aan uw LiveCycle-apps.

Met LiveCycle kunt u aangepaste knoppen toevoegen naast de bestaande actieknoppen (zoals **[!UICONTROL Share]** en **[!UICONTROL Flag]**) op een stuk inhoud.

Gebruik het argument mobile om te bepalen of de knop op mobiele apparaten wordt weergegeven.

Als u bijvoorbeeld een aangepaste actieknop wilt toevoegen voor de interface van uw mobiele apparaat:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Geef een extra argument door in uw ConvConfig-object met de naam actionButtons, dat een array bevat met objecten die elke knop beschrijven die u wilt toevoegen.
1. Definieer een toets voor de tekst die voor elke knop moet worden weergegeven.
1. Voeg een callback toe die op een klikgebeurtenis voor elke knoop zal worden aangehaald.

De callback wordt aangeroepen met een object met twee toetsen: `authorId` en `contentId`.
