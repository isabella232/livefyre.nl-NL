---
description: De spoor klikt terug naar uw pagina van verwijzingsverkeer.
seo-description: De spoor klikt terug naar uw pagina van verwijzingsverkeer.
seo-title: Verwijzing bijhouden
solution: Experience Manager
title: Verwijzing bijhouden
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Verwijzing bijhouden{#referral-tracking}

De spoor klikt terug naar uw pagina van verwijzingsverkeer.

Livefyre voegt een verwijzingsvariabele aan URL toe wanneer een commentaar wordt gepost of aan een sociaal netwerk wordt gedeeld, en voor permalinks inbegrepen in de e-mails van Livefyre. Gebruik deze variabele om het verwijzingsverkeer van LiveCyre Apps aan uw sociale of bezeten eigenschappen te volgen.

Met LiveCycle Apps kunt u gegevensstromen volgen die het gevolg zijn van verwijzingsverkeer, zodat u het verkeer van uw site kunt analyseren.

## Verkeer van LiveCycle-verwijzing bijhouden {#section_nsy_qp4_xz}

Het verwijzingsverkeer van het leven van sociale netwerken en e-mails kan worden gevolgd door de parameters van het vraagkoord in URLs van uw pagina&#39;s te inspecteren en code op uw pagina uit te voeren om dit door uw analyseleverancier te volgen. Livefyre voegt een verwijzingsverbinding aan URL toe wanneer een commentaar wordt gepost of aan een sociaal netwerk wordt gedeeld, en voor permalinks inbegrepen in de e-mails van Livefyre.

## Voorbeeld van implementatie {#section_xvs_x44_xz}

Als het verkeer van een bericht stroomHub-aangedreven was, zal er een hubRefSrc parameter van het vraagkoord met een waarde van e-mail, facebook, twitter, linkedin, of permalink zijn. De hubRefSrc parameternaam kan op het netwerkniveau door uw leveringsteam worden gevormd.

Om met een analyseplatform te integreren, moet uw pagina hubRefSrc bij lading zoeken, en het verkeer registreren als het aanwezig is.

Bijvoorbeeld:

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```



Toepassingen die deze functie gebruiken:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Opmerkingen](/help/using/c-about-apps/c-comments/c-comments.md)
* [Revisies](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

