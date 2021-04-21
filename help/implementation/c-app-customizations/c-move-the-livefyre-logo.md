---
description: Verander de positie van het Livefyre-logo op de pagina.
title: Het Livefyre-logo verplaatsen
exl-id: dc6c26cf-e0b9-4af3-8a3c-e58ea4ecbc44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Het Livefyre-logo{#move-the-livefyre-logo} verplaatsen

Verander de positie van het Livefyre-logo op de pagina.

Als uw overeenkomst met Livefyre dit toestaat, kunt u het Livefyre-logo van de bovenkant van de inhoudsstroom naar de onderkant verplaatsen.

Voeg bijvoorbeeld de volgende HTML toe aan uw pagina direct na het element dat de Livefyre-app bevat:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Voeg vervolgens het volgende toe aan het stijlblad van uw pagina:

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```
