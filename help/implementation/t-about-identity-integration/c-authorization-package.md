---
description: Installeer het verificatiepakket om gebruikersverificatie in te schakelen, zodat gebruikers kunnen communiceren met uw apps.
seo-description: Installeer het verificatiepakket om gebruikersverificatie in te schakelen, zodat gebruikers kunnen communiceren met uw apps.
seo-title: Verificatiepakket
solution: Experience Manager
title: Verificatiepakket
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# Verificatiepakket{#authentication-package}

Installeer het verificatiepakket om gebruikersverificatie in te schakelen, zodat gebruikers kunnen communiceren met uw apps.

LiveCycle Apps gebruiken het algemene audiopakket om gebruikers aan App-acties te koppelen. Het autepakket is beschikbaar via `Livefyre.require`.

Als u verificatie op uw pagina wilt inschakelen, voegt u eerst `Livefyre.js` toe aan het `<head>`-element van uw webpagina of websitesjabloon.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Het gebruiken van Livefyre.require om auth toe te laten is gelijkaardig aan het gebruiken vereist om andere pakketten te roepen. De integratiecode die auth vereist ziet er als volgt uit:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Methoden {#section_ojx_1lz_fz}

Zodra inbegrepen zoals hierboven gebruikend `Livefyre.require`, stelt de module van de Auth de volgende methodes bloot die u kunt roepen om andere Apps op de pagina over authentificatie-verwante gebeurtenissen op de hoogte te brengen.

| Methode | Beschrijving |
|--- |--- |
| `.login(callback)` | Trigger de login stroom zoals die door geregistreerde AuthDelegate wordt uitgevoerd. Gewoonlijk zullen alleen auth-enabled Apps dit, en niet de gastheerpagina zelf roepen. |
| `.logout(callback)` | Waarschuwen dat de eindgebruiker zich op een externe manier heeft afgemeld en dat alle vertrouwde Apps hun verificatiestatus moeten wissen tot de volgende aanmelding. Hierdoor wordt de interne sessie van Auth gewist. |
| `.authenticate(credentials)` | Waarschuwen Auth dat een gebruiker door één of andere externe middelen voor authentiek is verklaard, en een Token van de Authentificatie van de Bibliotheek is verworven voor de eindgebruiker. Gebruik dit als u een cookie instelt met het token LiveCycle of een token hebt voor de gebruiker en u de gebruiker expliciet wilt aanmelden. Bijvoorbeeld: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Wijs de implementatiedetails van authentificatie (bijvoorbeeld, uw stroom van de douaneauthentificatie) aan een voorwerp toe dat u bepaalt. Deze moet door de hostpagina worden aangeroepen om interactieve functies van LiveCycle Apps in te schakelen. |

