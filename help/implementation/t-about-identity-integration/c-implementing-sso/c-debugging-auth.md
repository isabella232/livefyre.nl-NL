---
description: U kunt een gebruiker binnen door de console tijdens integratie en het testen registreren om vergunning te zuiveren.
title: Foutopsporing Auth Delegate
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

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
