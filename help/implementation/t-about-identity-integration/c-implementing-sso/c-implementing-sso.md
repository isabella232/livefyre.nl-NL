---
description: Om een gebruiker met Livefyre door een stroom voor authentiek te verklaren die niet door een Toepassing Livefyre wordt teweeggebracht, adviseert Livefyre dat u de forEachAuthentication methode op uw voorwerp AuthDelegate uitvoert.
title: Implementatie van SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# SSO{#implementing-sso} implementeren

Om een gebruiker met Livefyre door een stroom voor authentiek te verklaren die niet door een Toepassing Livefyre wordt teweeggebracht, adviseert Livefyre dat u de forEachAuthentication methode op uw voorwerp AuthDelegate uitvoert.

Dit zal worden aangehaald wanneer `authDelegate` wordt overgegaan tot `auth.delegate`, en zal een voor authentiek verklaren functie worden overgegaan die veelvoudige tijden kan worden overgegaan. Deze methode verstrekt een inversie van controle voor authentificatiegebeurtenissen zodat uw `AuthDelegateobject` met alle accomodatie zonder een globale verwijzing naar auth kan worden vereist.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

LiveCycle is afhankelijk van gebruikerstokens om verificatie te coördineren. Dientengevolge, moet dit teken door uw identiteitsdienst zijn teruggekeerd om een gebruiker met Livefyre voor authentiek te verklaren. Zie Een gebruikersverificatietoken maken voor meer informatie over het maken van een gebruikerstoken voor LiveCycle.

>[!NOTE]
>
>Na een geslaagde aanmelding maakt auth een sessie voor de gebruiker en probeert een gebruikerssessie te laden wanneer de pagina wordt vernieuwd en opnieuw wordt geladen. `auth.logout()` zal deze sessie wissen. Dit betekent dat het niet nodig is om de sessie van een gebruiker onafhankelijk van de autorisatie te beheren.
