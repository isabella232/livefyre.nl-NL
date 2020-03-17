---
description: U kunt een gebruiker binnen door de console tijdens integratie en het testen registreren om vergunning te zuiveren.
seo-description: U kunt een gebruiker binnen door de console tijdens integratie en het testen registreren om vergunning te zuiveren.
seo-title: Foutopsporing Auth Delegate
solution: Experience Manager
title: Foutopsporing Auth Delegate
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Foutopsporing Auth Delegate{#debugging-auth-delegate}

U kunt een gebruiker binnen door de console tijdens integratie en het testen registreren om vergunning te zuiveren.

Meld een gebruiker aan via de console met behulp van de volgende `auth.authenticate` (token) en geef een gebruikerstoken van LiveCycle door om gebruikers op de pagina te verifiëren.

U kunt het hierboven getoonde voorbeeld ook wijzigen, en het volgende fragment in-lijn in uw JavaScript toevoegen om een gebruiker in Livefyre (vereist een verwijzing naar auth) snel te registreren.

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

