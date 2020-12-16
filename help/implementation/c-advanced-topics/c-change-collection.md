---
description: Gebruikers mogen via één pagina-indeling en URL op Verzamelingen klikken.
seo-description: Gebruikers mogen via één pagina-indeling en URL op Verzamelingen klikken.
seo-title: Verzameling wijzigen
solution: Experience Manager
title: Verzameling wijzigen
uuid: 81c8a554-375f-4659-9e25-5b3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Verzameling {#change-collection} wijzigen

Gebruikers mogen via één pagina-indeling en URL op Verzamelingen klikken.

Met de Change Collection Delegate kunt u de verzameling wijzigen die op een pagina wordt weergegeven, zonder de URL te wijzigen, terwijl er al een LiveCycle-toepassing is geladen. Met deze functie kunt u foto- of videogalerieën of andere toepassingen weergeven waarin de weergegeven verzameling na een actie van de gebruiker moet veranderen.

Als u bijvoorbeeld op een video of foto in een galerie klikt, wordt een verzameling geladen die specifiek is voor die selectie, terwijl de URL van de pagina niet wordt gewijzigd.

Aan [laad één van drie Inzamelingen van één enkele pagina](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
