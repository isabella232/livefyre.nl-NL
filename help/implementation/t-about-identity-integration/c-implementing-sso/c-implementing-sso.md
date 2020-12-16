---
description: Om een gebruiker met Livefyre door een stroom voor authentiek te verklaren die niet door een Toepassing Livefyre wordt teweeggebracht, adviseert Livefyre dat u de forEachAuthentication methode op uw voorwerp AuthDelegate uitvoert.
seo-description: Om een gebruiker met Livefyre door een stroom voor authentiek te verklaren die niet door een Toepassing Livefyre wordt teweeggebracht, adviseert Livefyre dat u de forEachAuthentication methode op uw voorwerp AuthDelegate uitvoert.
seo-title: Implementatie van SSO
solution: Experience Manager
title: Implementatie van SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '218'
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

