---
description: Wijzig het pictogram dat voor Livefyre-gebruikers wordt weergegeven in het vervolgkeuzemenu @mention.
seo-description: Wijzig het pictogram dat voor Livefyre-gebruikers wordt weergegeven in het vervolgkeuzemenu @mention.
seo-title: Pictogram @mention wijzigen
solution: Experience Manager
title: Pictogram @mention wijzigen
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Pictogram `@mention` wijzigen {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

Wijzig het pictogram LiveCycle dat wordt gebruikt in het keuzemenu in een pictogram van uw keuze, zodat u uw leden van de gebruikersgemeenschap kunt aangeven met uw eigen pictogram. `@mention`

## Voorbeeld

Als u dit pictogram wilt wijzigen, voegt u de volgende CSS toe aan uw stijlpagina. Vervang &lt;*uw resource*> url door de URL van de geselecteerde afbeelding om de standaard livefyre-badge te vervangen.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
