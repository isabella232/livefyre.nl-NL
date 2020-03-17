---
description: Gebruik Livefyre.js om voor uw LiveCyre-apps paginabrede verificatie toe te voegen.
seo-description: Gebruik Livefyre.js om voor uw LiveCyre-apps paginabrede verificatie toe te voegen.
seo-title: Verificatie toevoegen aan een app met Livefyre.js
solution: Experience Manager
title: Verificatie toevoegen aan een app met Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Verificatie toevoegen aan een app met LiveCyre.js{#add-authetication-to-an-app-using-livefyre-js}

Gebruik Livefyre.js om voor uw LiveCyre-apps paginabrede verificatie toe te voegen.

`Livefyre.js Aut`Dit is een JavaScript-pakket dat door LiveCycle is ontwikkeld en waarmee alle toepassingen op uw website één verificatie-integratie kunnen delen. Auth staat u toe om te bepalen hoe uw gebruikers zouden moeten registreren, login, en logout door deze stromen aan een voorwerp te delegeren AuthDelegate dat u bepaalt.

## Stap 1: Verificatie inschakelen voor een pagina {#section_pgp_jtt_bbb}

Gebruik deze optie `Livefyre.js` om verificatie voor een pagina in te schakelen, zodat gebruikers zich kunnen aanmelden en met toepassingen kunnen communiceren via uw bestaande verificatiesysteem.

1. Als u verificatie op een pagina wilt inschakelen, voegt u `Livefyre.js` het element *&lt;head>* van uw webpagina of websitesjabloon toe.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Gebruik deze optie `Livefyre.require` om verificatie in te schakelen. Het gebruiken `Livefyre.require` is gelijkaardig aan het gebruiken vereist om andere pakketten te roepen. De integratiecode die auth vereist ziet er als volgt uit:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Stap 2: Een AuthDelegate registreren {#section_oqm_15t_bbb}

Om authentificatie toe te laten creeer een `AuthDelegate` en ga het tot `Livefyre.js` Authentificatie over.

Een `AuthDelegate` object is een object dat u definieert en dat bepaalt hoe gebruikers zich aanmelden, afmelden en profielen weergeven.

1. Maak een `AuthDelegate`. De manier waarop u een document maakt, `AuthDelegate` hangt af van uw identiteitsprovider. Zie Identiteitsintegratie voor meer gedetailleerde instructies.

1. Geef het `AuthDelegate` door aan `Livefyre.js` Authentificatie. De eenvoudigste `AuthDelegate` logboeken de zelfde gebruiker in wanneer een gebruiker de gemachtigde login methode van een App teweegbracht:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Stap 3: Gebruikersgegevens synchroniseren {#section_u4m_j5t_bbb}

Synchroniseer de gebruikersprofielgegevens tussen LiveCycle en uw identiteitsprovider.

U moet de gebruikersprofielgegevens synchroniseren tussen LiveCycle en uw identiteitsprovider. Zie [Janrain Capture Integration](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)voor meer informatie.
