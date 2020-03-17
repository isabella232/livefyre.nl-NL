---
description: De kernbibliotheek van Livefyre die wordt gebruikt om Livefyre op uw plaats aan te drijven.
seo-description: De kernbibliotheek van Livefyre die wordt gebruikt om Livefyre op uw plaats aan te drijven.
seo-title: Methode updateAnchors
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Methode updateAnchors {#updateAnchorsMethod}

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
