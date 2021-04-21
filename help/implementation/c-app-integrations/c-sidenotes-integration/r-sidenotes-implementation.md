---
description: Sidenotes implementeren met .js-implementatie.
title: Sidenotes-implementatie
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 20%

---

# Sidenotes-implementatie{#sidenotes-implementation}

## Sidenotes implementeren met .js-implementatie

Als u deze functie wilt implementeren, geeft u een 1-1-objecttoewijzing van de tekenreeksen die u wilt overschrijven, door aan het Javascript-configuratieobject. Als u geen veld opgeeft, wordt de standaardtekst gebruikt.

### Voorbeeld

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
