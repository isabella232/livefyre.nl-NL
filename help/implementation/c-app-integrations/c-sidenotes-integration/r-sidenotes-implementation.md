---
description: Sidenotes implementeren met .js-implementatie.
seo-description: Sidenotes implementeren met .js-implementatie.
seo-title: Sidenotes-implementatie
solution: Experience Manager
title: Sidenotes-implementatie
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sidenotes-implementatie{#sidenotes-implementation}

## Sidenotes implementeren met .js-implementatie

Als u deze functie wilt implementeren, geeft u een 1-1-objecttoewijzing van de tekenreeksen die u wilt overschrijven, door aan het Javascript-configuratieobject. Als u geen veld opgeeft, wordt de standaardtekst gebruikt.

### Voorbeeld

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
