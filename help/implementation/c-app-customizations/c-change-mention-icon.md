---
description: Wijzig het pictogram dat voor Livefyre-gebruikers wordt weergegeven in het vervolgkeuzemenu @mention.
seo-description: Wijzig het pictogram dat voor Livefyre-gebruikers wordt weergegeven in het vervolgkeuzemenu @mention.
seo-title: Pictogram @mention wijzigen
solution: Experience Manager
title: Pictogram @mention wijzigen
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 30%

---


# Pictogram `@mention` wijzigen {#change-mention-icon}

Wijzig het pictogram dat wordt weergegeven voor Live-gebruikers in het keuzemenu `@mention`.

Wijzig het pictogram LiveCycle dat in het vervolgkeuzemenu `@mention` wordt gebruikt in een pictogram van uw keuze, zodat u de leden van de gebruikersgemeenschap kunt aangeven met uw eigen pictogram.

## Voorbeeld

Als u dit pictogram wilt wijzigen, voegt u de volgende CSS toe aan uw stijlpagina. Vervang &lt;*uw resource*> URL door de URL van de afbeelding die u hebt geselecteerd om de standaardbadge van de bibliotheek te vervangen.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
