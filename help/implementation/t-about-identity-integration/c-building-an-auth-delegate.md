---
description: Het voorwerp AuthDelegate voert uw gewenst gedrag voor uit hoe te om authentificatieacties en gebeurtenissen uit te voeren zodat kunt u integratie met het bestaande authentificatiesysteem van uw plaats aanpassen.
seo-description: Het voorwerp AuthDelegate voert uw gewenst gedrag voor uit hoe te om authentificatieacties en gebeurtenissen uit te voeren zodat kunt u integratie met het bestaande authentificatiesysteem van uw plaats aanpassen.
seo-title: Object AuthDelegate
solution: Experience Manager
title: Object AuthDelegate
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Object AuthDelegate{#authdelegate-object}

Het voorwerp AuthDelegate voert uw gewenst gedrag voor uit hoe te om authentificatieacties en gebeurtenissen uit te voeren zodat kunt u integratie met het bestaande authentificatiesysteem van uw plaats aanpassen.

## Een Auth-delegatie maken {#section_wmn_tv2_gz}

Het autepakket moet van een auteafgevaardigde worden voorzien alvorens het een actie kan uitvoeren. Een auth afgevaardigde is om het even welk voorwerp JavaScript dat één van de methodes in dit onderwerp uitvoert.

## .login(finishLogin) {#section_mpk_lv2_gz}

Meld u aan bij een geldige gebruiker en activeer de functie finishLogin met een Error-object als er een fout is opgetreden, of de LiveLogin-referenties van de gebruiker. De gemeenschappelijke implementaties van deze methode richten de gebruiker aan een login pagina om of openen een nieuw venster of modaal.

In dit voorbeeld wordt de auth van een LiveCyre-gebruiker automatisch op de hoogte gebracht van het verificatietoken, het token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

De eenvoudigste login afgevaardigde zou de eindgebruiker voor hun teken van de Authentificatie van het Leven kunnen vragen.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logout(finishLogout) {#section_uqz_2v2_gz}

Log uit een gebruiker en roep de functie finishLogout met of een voorwerp van de Fout aan als er een fout was, of ongeldig om auth mee te delen dat de logout succesvol was.

Bijvoorbeeld:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(gebruiker) {#section_kkv_dv2_gz}

Handeling uitvoeren om het profiel van een gebruiker weer te geven.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(gebruiker) {#section_bkx_pq2_gz}

Handeling uitvoeren om het profiel van een gebruiker te bewerken.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Door alle hierboven vermelde methodes uit te voeren, kan de auth met een douaneauthedgedelegeerde worden gevormd. Zodra een afgevaardigde is geconstrueerd, kan het aan auth worden verstrekt gebruikend de afgevaardigde methode.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

