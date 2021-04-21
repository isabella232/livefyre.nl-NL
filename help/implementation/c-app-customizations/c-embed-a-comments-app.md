---
description: Het insluiten van de Comments App volgt het proces voor het insluiten van een Core App.
title: Een app voor opmerkingen insluiten
exl-id: 5eb191f8-ee52-4a9d-9180-90457a49fd4e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Een toepassing voor opmerkingen insluiten{#embed-a-comments-app}

Het insluiten van de Comments App volgt het proces voor het insluiten van een Core App.

Het insluiten van de Commentaarstoepassing volgt het proces voor het inbedden van een Kernapp die in [wordt beschreven een App ](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) inbedden

## Voorbeeld

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Zoals vermeld in de sectie Building CollectionMeta, is CollectionMeta een gecodeerd JSON-object. In het bovenstaande voorbeeld heeft het JSON-object de volgende indeling voordat JWT-codering wordt uitgevoerd:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```
