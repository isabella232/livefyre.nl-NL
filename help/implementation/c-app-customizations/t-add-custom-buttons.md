---
description: Voeg aangepaste handelingen toe aan uw LiveCycle-apps.
title: Aangepaste knoppen toevoegen
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

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
