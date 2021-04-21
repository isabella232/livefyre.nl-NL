---
description: Het pakket Livefyre.js Auth zorgt ervoor dat alle sociale componenten op uw pagina één enkele authentificatieintegratie kunnen ontdekken.
title: Livefyre-identiteit initialiseren
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
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
