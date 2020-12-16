---
description: Het pakket Livefyre.js Auth zorgt ervoor dat alle sociale componenten op uw pagina één enkele authentificatieintegratie kunnen ontdekken.
seo-description: Het pakket Livefyre.js Auth zorgt ervoor dat alle sociale componenten op uw pagina één enkele authentificatieintegratie kunnen ontdekken.
seo-title: Livefyre-identiteit initialiseren
title: Livefyre-identiteit initialiseren
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Livefyre Identity initialiseren{#initialize-livefyre-identity}

Het pakket Livefyre.js Auth zorgt ervoor dat alle sociale componenten op uw pagina één enkele authentificatieintegratie kunnen ontdekken.

Livefyre verstrekt een `lfep-auth-delegate` pakket dat een aangewezen auteafgevaardigde voor u zal maken. Auth moet een voorwerp worden verstrekt AuthDelegate dat weet hoe te om authentificatieacties, zoals login en logout uit te voeren.

1. Voeg Livefyre.js aan uw webpagina toe.
1. Om Auth te vertellen om deze acties aan de Identiteit van het Leven te delegeren, voeg het volgende toe:

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
