---
description: Klanten die Janrain Capture en Backplane gebruiken, kunnen Livefyre Auth for Single Sign On (SSO) gebruiken, zodat gebruikers direct contact kunnen opnemen met uw Livefyre Apps wanneer zij zich aanmelden bij uw site.
seo-description: Klanten die Janrain Capture en Backplane gebruiken, kunnen Livefyre Auth for Single Sign On (SSO) gebruiken, zodat gebruikers direct contact kunnen opnemen met uw Livefyre Apps wanneer zij zich aanmelden bij uw site.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

Klanten die Janrain Capture en Backplane gebruiken, kunnen Livefyre Auth for Single Sign On (SSO) gebruiken, zodat gebruikers direct contact kunnen opnemen met uw Livefyre Apps wanneer zij zich aanmelden bij uw site.

Als u wilt profiteren van deze ingebouwde integratie van Vastleggen/Backplane, moet u configuratiewijzigingen aanbrengen in zowel de app Capture als uw integratie met Livefyre.js.

>[!NOTE]
>
>Sla deze sectie over als u Janrain Capture niet gebruikt.

Raadpleeg de documentatie bij [het Backplane van](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)Janrain voor meer informatie.

1. [Vastleggen instellen.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Optioneel) [Voeg standaardinstellingen voor Livefyre toe aan de app](#c_janrain_capture_backplane/section_z2s_txt_bbb)Vastleggen.
1. [Bouw het voorwerp AuthDelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Synchroniseren met Livefyre met Ping for Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Stap 1: Vastleggen instellen {#section_r2f_kxt_bbb}

Livefyre heeft bepaalde gegevens nodig van uw app Janrain Capture.

1. Stel de app Janrain Capture in.
1. Verzamel de volgende informatie voor Livefyre:

   * Toegang tot uw exemplaar van Janrain Capture.
   * Toegang tot je dashboard van Janrain Engage.
   * Uw instellingen en referenties voor vastleggen.
   * Uw Inloggegevens.
   * Uw identiteit-URL.

>[!NOTE]
>
>Livefyre ontvangt gegevens rechtstreeks van CNAME; Daarom kan deze id-URL geen CNAMEd-record (een URL-naamruimte van ijl) zijn die wordt omgezet in de werkelijke CNAME van Janrain Capture.

## Stap 2: (Optioneel) Standaardwaarden voor Livefyre toevoegen aan de app Capture {#section_z2s_txt_bbb}

U kunt standaardinstellingen voor Livefyre toevoegen aan gebruikers die zijn opgeslagen in de app Vastleggen, zodat u gebruikers e-mailmeldingen kunt sturen of gebruikers automatisch gesprekken kunnen volgen waarop gebruikers opmerkingen plaatsen.

1. Volledige [stap 1: Vastleggen](#c_janrain_capture_backplane/section_r2f_kxt_bbb)instellen.
1. Voeg de volgende standaardvelden voor LiveCycle toe. Alle velden zijn optioneel.

| Parameter | Type | Beschrijving |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | String | De gebruiker op de hoogte stellen wanneer iemand opmerkingen maakt over een artikel dat hij of zij volgt. Kan onmiddellijk, vaak of nooit zijn. |
| **[!UICONTROL livefyre_likes]** | String | De gebruiker op de hoogte stellen wanneer iemand een bericht leuk vindt. Kan onmiddellijk, vaak of nooit zijn. |
| **[!UICONTROL livefyre_replies]** | String | De gebruiker op de hoogte stellen wanneer iemand op een van zijn berichten reageert. Kan onmiddellijk, vaak of nooit zijn. |
| **[!UICONTROL livefyre_moderator_comments]** | String | Waarschuw de moderator wanneer iemand op een gesprek opmerkt dat zij modereren.Kan onmiddellijk, vaak, of nooit zijn. |
| **[!UICONTROL livefyre_moderator_flags]** | String | Waarschuw de moderator wanneer iemand een post op een gesprek markeert dat zij modereren.Kan onmiddellijk, vaak, of nooit zijn. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Boolean | Heb de gebruiker automatisch een gesprek volgen wanneer zij een post verlaten. Kan waar of onwaar zijn. |

## Stap 3: Maak het AuthDelegate-object voor Janrain Integration {#section_asv_vyt_bbb}

Livefyre.require beschikt over een insteekmodule waarmee auth naar de Janrain Backplane bus kan luisteren.

### Aanmelden {#login}

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



>[!NOTE]
>
>Uw auteur zal afhankelijk van uw instantie van Janrain variëren.

Hieronder volgen enkele voorbeelden van hoe een auteafgevaardigde kan zoeken naar integratie met Janrain Capture.

* `errback`: De callback ging tot de login van uw auteur van uw auteur methode over
* `janrain`: De verwijzing naar uw Janrain capture-variabele.
* `window.Backplane`: Een verwijzing naar het object Backplane.

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

### Afmelden {#logout}

* `finishLogout`: De callback ging tot de login van uw auteur methode over.

* `window.Backplane`: Een verwijzing naar het object Backplane.

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

### Profiel bewerken {#editprofile}

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

### Profiel weergeven {#viewprofile}

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

## Stap 4: Synchroniseren met Livefyre met Ping for Pull voor Janrain Integration {#section_ilv_bzt_bbb}

Bij het synchroniseren van de externe livefyre-profielen met het beheersysteem van de gebruiker Capture wordt een aantal stappen uitgevoerd die Ping for Pull worden genoemd. Dit proces vereist dat u een geldig toegangstoken van Janrain verkrijgt, en dan dat teken tot een eindpunt doorgeeft dat in stap 3, hieronder wordt gespecificeerd.

1. Haal een toegangscode op uit Janrain.

   Om de toegangscode te krijgen, levering de noodzakelijke geloofsbrieven, specificeer user_type als &quot;gebruiker&quot;, en uuid als huidige gebruiker te bijwerken uuid. Zie [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)voor meer informatie.

1. Handel de toegangscode voor een toegangstoken in. Verstrek de noodzakelijke geloofsbrieven, de toegangscode die van stap 1 wordt ontvangen, en specificeer het Grant_type als &quot;authentication_code&quot;.

   Zie [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)voor meer informatie.

1. Druk op het eindpunt &quot;Ping to Pull Capture&quot; van Livefy.

   URL eindpunt: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] waarbij ***{networkName}*** de netwerknaam is die aan u door Livefyre wordt verstrekt, en jrtoken is het token dat in stap 2 van Janrain wordt ontvangen.

   Zodra u dit eindpunt raakt, ontvangt u een reactie 202 en Livefyre begint een asynchroon proces.

## Hoe het werkt {#concept_mty_f31_2cb}

Als u wilt profiteren van deze ingebouwde integratie van Vastleggen/Backplane, moet u een aantal configuratiewijzigingen aanbrengen in zowel de app Capture als uw integratie met Livefyre.js.

Janrain verzendt succesvolle login/logout berichten door de bus Backplane, waarop de Livefyre App, wanneer behoorlijk gevormd, luistert. Deze berichten bevatten alle informatie nodig om App-gebruikers te tonen dat ze zijn aangemeld of dat ze zich hebben afgemeld. De ontwikkelaars kunnen de busberichten bekijken Backplane door het lusje van het Netwerk in de ontwikkelaarsconsole van uw browser te inspecteren.

## Voorbeeld van inlogcode {#section_ftt_tvp_mz}

Verzoek:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Reactie:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Lege reactie:

```
Backplane.response([]);
```

## Voorbeeld van een afmeldingscode {#section_t52_svp_mz}

Verzoek:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Reactie:

```
Backplane.finishInit("{CHANNEL}");
```

Als deze berichten niet in uw netwerkverzoeken worden weergegeven, is Livefyre zich niet bewust van de aanmeldings-/aanmeldingspogingen en kan Livefyre de gebruiker daarom niet integreren in de app.
