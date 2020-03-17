---
description: Livefyre.require beschikt over een insteekmodule waarmee auth naar de Janrain Backplane bus kan luisteren.
seo-description: Livefyre.require beschikt over een insteekmodule waarmee auth naar de Janrain Backplane bus kan luisteren.
seo-title: Janrain verbinden met Livefyre met gebruik van AuthDelegate
title: Janrain verbinden met Livefyre met gebruik van AuthDelegate
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain verbinden met Livefyre met gebruik van AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require beschikt over een insteekmodule waarmee auth naar de Janrain Backplane bus kan luisteren.

Wanneer een identiteit/login bericht op het Backplane kanaal wordt uitgezonden, zal auth.authenticate () voor u met het teken van de Authentificatie van de Bibliotheek van de gebruiker worden geroepen. U moet nog een AuthDelegate uitvoeren.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>Het object window.Backplane moet op de pagina zijn gedefinieerd voordat u Auth.plugin aanroept met de plug-in Livefyre Backplane. Om ervoor te zorgen dat het Backplane-object beschikbaar is, roept u de LiveCyre-instantiecode aan vanuit een onReady-callback. Raadpleeg uw Janrain-contactpersoon om te bepalen wanneer andere toepassingen het Backplane-object kunnen gebruiken.

Hieronder volgen enkele voorbeelden van hoe een auteafgevaardigde kan zoeken naar integratie met Janrain Capture.

>[!NOTE]
>
>Uw auteur zal afhankelijk van uw instantie van Janrain variëren.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* De callback ging tot de login van uw auteur van uw auteur methode over
* De verwijzing naar uw Janrain capture-variabele.
* : Een verwijzing naar het object Backplane.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

Afmelden

* **finishLogout:** De callback ging tot de login van uw auteur methode over.

* **window.Backplane:** Een verwijzing naar het object Backplane.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

Profiel bewerken

Dit kan worden gekoppeld aan welk deel van de site u gebruikers wilt laten bezoeken om hun eigen profielpagina te bekijken. In dit voorbeeld wordt alleen het doorgegeven auteursobject afgedrukt.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Profiel weergeven

Net als Profiel bewerken, moet u deze koppeling maken naar de pagina van een gebruiker die afwijkt van de momenteel aangemelde gebruiker. Dit kan worden geïmplementeerd, maar u ziet het juist. In dit voorbeeld wordt de parameter van de auteur gewoon bij de console geregistreerd.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

