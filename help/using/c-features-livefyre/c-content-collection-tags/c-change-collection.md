---
description: Gebruikers mogen via één pagina-indeling en URL op Verzamelingen klikken.
title: Verzameling wijzigen
exl-id: 5cfae2c6-e328-4d2c-b08b-709be94e4c54
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Verzameling wijzigen{#change-collection}

Gebruikers mogen via één pagina-indeling en URL op Verzamelingen klikken.

Met de Change Collection Delegate kunt u de verzameling wijzigen die op een pagina wordt weergegeven, zonder de URL te wijzigen, terwijl er al een LiveCycle-toepassing is geladen. Met deze functie kunt u foto- of videogalerieën of andere toepassingen weergeven waarin de weergegeven verzameling na een actie van de gebruiker moet veranderen.

Als u bijvoorbeeld op een video of foto in een galerie klikt, wordt een verzameling geladen die specifiek is voor die selectie, terwijl de URL van de pagina niet wordt gewijzigd.

Om één van drie Inzamelingen van één enkele [commentaartelling](/help/implementation/c-advanced-topics/t-display-comment-count.md) pagina te laden:

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
