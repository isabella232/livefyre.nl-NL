---
description: Meerdere verzamelingen op één pagina weergeven.
seo-description: Meerdere verzamelingen op één pagina weergeven.
seo-title: Meerdere verzamelingen
solution: Experience Manager
title: Meerdere verzamelingen
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Meerdere verzamelingen {#multiple-collections}

Meerdere verzamelingen op één pagina weergeven.

U kunt meerdere verzamelingen op één pagina op uw site opnemen. Als u bijvoorbeeld een gebeurtenis wilt publiceren, hebt u tijdens de gebeurtenis mogelijk een Live-blog of chatgesprek, met een aparte app aan de zijkant van de pagina, waarin gerelateerde, gekromde inhoud wordt weergegeven op het sociale web. U kunt ook een toepassing met opmerkingen onder een artikel plaatsen, met een chat aan de zijkant.

Om veelvoudige gesprekken op een pagina te krijgen, voeg één of meerdere configuraties in een serie toe en ga de serie tot de ladingsvraag over. Bijvoorbeeld.

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
