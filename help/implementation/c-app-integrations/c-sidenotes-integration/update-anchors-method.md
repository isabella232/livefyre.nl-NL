---
description: De kernbibliotheek van Livefyre die wordt gebruikt om Livefyre op uw plaats aan te drijven.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# methode updateAnchors {#updateAnchorsMethod}

Gebruik de methode updateAnchors om dynamisch inhoud aan de pagina toe te voegen.

Deze methode is handig voor paginering of in andere gevallen waarin inhoud die naast elkaar kan worden geplaatst, dynamisch aan de pagina wordt toegevoegd. Deze methode definieert nieuwe ankers voor de overeenkomende elementen en gebruikt één argument: newSelectors.

**newSelectors**. De kiezers die moeten worden toegevoegd aan Sidenotes. Dit kan een selecteurstekenreeks, een voorwerp jQuery, of een serie van elementen (om het even welke die types door het selecteursargument worden goedgekeurd tijdens de toepassingsbouw wordt overgegaan) zijn.
Indeling:

```
app.updateAnchors(newSelectors);
```

Voorbeeld:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
