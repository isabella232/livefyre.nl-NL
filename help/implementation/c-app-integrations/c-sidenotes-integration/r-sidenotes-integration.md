---
description: Integreer een Sidenotes-app door een proces te volgen dat vergelijkbaar is met Core-toepassingen.
seo-description: Integreer een Sidenotes-app door een proces te volgen dat vergelijkbaar is met Core-toepassingen.
seo-title: Sidenotes-integratie
solution: Experience Manager
title: Sidenotes-integratie
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---


# Sidenotes Integration{#sidenotes-integration}

Integreer een Sidenotes-app door een proces te volgen dat vergelijkbaar is met Core-toepassingen.

Als algemene regel geldt dat als de integratie van uw kerntoepassing is voltooid, de code die is geschreven om het object `collectionMeta` te genereren, opnieuw kan worden gebruikt voor Sidenotes.

U kunt uw bestaande `auth` afgevaardigden ook hergebruiken door `auth` afgevaardigde te leveren die met `fyre.conv` aan Sidenotes in het (facultatieve) `authDelegate` gebied wordt gecreeerd.

>[!NOTE]
>
>Met identificaties kunt u `network`, `siteId` en `articleId` in één object opnemen in plaats van ze afzonderlijk door te geven in andere delen van de constructor.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Zoals vermeld in de sectie Building `collectionMeta`, is `collectionMeta` een gecodeerd JSON-object. In het bovenstaande voorbeeld heeft het JSON-object de volgende indeling voordat JWT-codering wordt uitgevoerd.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Zie de token `collectionMeta` voor meer informatie.

## Mobiele instellingen

Sidenotes zijn geoptimaliseerd voor gebruik op mobiele apparaten. Voor de beste resultaten met mobiele versies van uw LiveCycle-app stelt u de schaalbare optie voor de gebruiker in op Nee. Bijvoorbeeld:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
