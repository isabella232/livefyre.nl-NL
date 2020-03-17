---
description: Verander de positie van het Livefyre-logo op de pagina.
seo-description: Verander de positie van het Livefyre-logo op de pagina.
seo-title: Het Livefyre-logo verplaatsen
solution: Experience Manager
title: Het Livefyre-logo verplaatsen
uuid: 807304ae-6070-4505-87db-169a925f714c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Het Livefyre-logo verplaatsen{#move-the-livefyre-logo}

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

