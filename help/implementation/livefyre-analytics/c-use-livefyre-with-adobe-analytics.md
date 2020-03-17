---
description: 'null'
seo-description: 'null'
seo-title: LiveCycle gebruiken met Adobe Analytics en Dynamic Tag Manager (DTM), lk xavvefyre met Adobe Analytics en Dynamic Tag Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 987482066f1ca3c021a5c9f0fc0109edff616c0a

---


# LiveCycle gebruiken met Adobe Analytics en Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Stel Adobe Analytics en Dynamic Tag Manager (DTM) in om gegevens voor LiveCycle-apps te verzamelen.

## Stap 1: Gebeurtenissen instellen in Adobe Analytics {#section_iks_kgd_4cb}

Wijs Live-gebeurtenissen toe aan een of meer aangepaste succesgebeurtenissen in Adobe Analytics Report Suite Manager.

Zie [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)voor meer informatie over Report Suite Manager.

1. Meld u aan bij Adobe Analytics als beheerder.
1. Open Adobe Analytics Admin Report Suite Manager.
1. Maak een nieuwe rapportsuite of kies een bestaande rapportsuite.
1. Bewerk de rapportsuite door op de rapportsuite te klikken die u wilt wijzigen en navigeer vervolgens naar **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Wijs de Livefyre-gebeurtenissen toe aan een of meer aangepaste succesgebeurtenissen.

## Stap 2: Conversievariabelen instellen

Wijs bibliotheekconversievariabelen (eVars) toe aan conversievariabelen in Adobe Analytics Admin Report Suite Manager. Conversievariabelen fungeren als een sorteerfunctie om te bepalen hoe u gegevens wilt identificeren die uit LiveCycle-gebeurtenissen zijn verzameld.

1. Klik in Report Suite Manager **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Kies de aangepaste conversievariabelen (eVars) die u wilt gebruiken en wijs deze toe aan de bibliotheekconversievariabelen. U kunt als volgt een conversievariabele Livefyre toewijzen aan een aangepaste conversievariabele:
* De conversievariabele inschakelen
* De conversievariabele een naam geven
* De conversievariabele een type geven
1. Sla de aangepaste conversievariabelen op.

## Stap 3: DTM gebruiken om uw rapportsuite toe te voegen met LiveCycle Events {#section_t15_2hd_4cb}

Voeg Adobe Analytics toe aan DTM om Analytics te laten werken. Hiertoe maakt u een nieuwe eigenschap en een nieuw gereedschap en voegt u de nieuwe rapportsuite met LiveCycle-gebeurtenissen toe aan de eigenschap. Zie [DTM voor meer informatie over DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

U hoeft deze stap niet uit te voeren als u al een eigenschap of gereedschap hebt ingesteld voor de rapportsuite die u hebt ingesteld met LiveCycle-gebeurtenissen.

1. Maak of bewerk een bestaande eigenschap in DTM.
1. Maak of bewerk een bestaand hulpprogramma voor Adobe Analytics.
1. Als er geen bestaande Adobe Analytics Tool bestaat, klikt u op de **[!UICONTROL Add a Tool]** knop.
Stel de volgende parameters in voor het gereedschap:

   * Instellen **[!UICONTROL Tool Type]** op **[!UICONTROL Adobe Analytics]**.
   * Inschakelen **[!UICONTROL Automatic Configuration]**.
   * Inschakelen **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Voeg de naam van de rapportsuite met Livefyre-gebeurtenissen toe aan of bevestig deze aan het **[!UICONTROL Report Suites]** veld.

## Stap 4: Een regel voor het laden van pagina&#39;s instellen voor de verwerking van analysemogelijkheden {#section_jfj_j3d_4cb}

Stel een regel voor het laden van pagina in om alle gegevens op te halen. Met de regel Pagina laden kunt u aangepaste javascript in de regel plaatsen die de gebeurtenis vastlegt wanneer de pagina wordt geladen.

>[!NOTE]
>
>Gebruik geen op gebeurtenis gebaseerde Regels of Directe Regels van de Vraag.

1. Selecteer **[!UICONTROL Rules]** tab in DTM.
1. Klik op **[!UICONTROL Page Load Rules]**.
1. Klik op de **[!UICONTROL Create New Rule]** knop.
1. Open de **[!UICONTROL Conditions]** sectie door op de **[!UICONTROL Plus]** knop te klikken.
1. Trigger de regel. Kies **[!UICONTROL DOM Ready]** of **[!UICONTROL Onload]** triggertypen als u de regel asynchroon wilt vertragen of implementeren.
1. (Optioneel) Voeg aanvullende parameters toe om de pagina&#39;s te beperken die Live Apps weergeven. Voor meer informatie over extra configuratieopties, zie [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Klik onder **[!UICONTROL Javascript/ Third Party Tags]** op het **[!UICONTROL Non-sequential]** tabblad en klik vervolgens op **[!UICONTROL Add New Script]**.
1. Selecteer **[!UICONTROL Sequential HTML]** als scripttype.
1. Voeg het volgende script toe aan de code-editor en klik op **[!UICONTROL Save Code]**.

   Het volgende script roept de regel voor `livefyre_analytics` directe aanroepen aan nadat de LiveCycle JavaScript is geladen. In het volgende scriptvoorbeeld wordt om de 400 ms gecontroleerd of de pagina `livefyre.analytics` zich bevindt. Nadat de pagina is geladen, verzendt livefyre.analytics trackinggegevens.

   ```
   /** 
   * Poll for Livefyre.analytics object to exist since it gets loaded via the 
   * Livefyre.js JavaScript file. Depending on the timing, this could already 
   * exist or need a little time. 
   */ 
   function pollForAnalytics() {  
   if (Livefyre.analytics) { 
     _satellite.track('livefyre_analytics'); 
       return true; 
     } 
     setTimeout(pollForAnalytics, 400); 
   } 
   setTimeout(pollForAnalytics, 400);
   ```

1. Klik op **[!UICONTROL Save Code]**.
1. Klik op **[!UICONTROL Save Rule]**.

## Stap 5: Creeer een Directe Regel van de Vraag om de Configuratie van de Toewijzing van de Analyse van Adobe voor Levenslang samen te stellen {#section_gvp_b1g_pdb}

Er zijn andere manieren om LiveCycle met DTM te implementeren door aangepaste gebeurtenissen, Adobe Analytics UI-velden binnen DTM en gegevenselementen te gebruiken. In dit document wordt aangepaste JavaScript gebruikt om hetzelfde effect te bereiken.

1. In DTM selecteer het lusje van **Regels** en klik dan op de Regels **van de** Vraag Direct.
1. Click on the **Create New Rule** button.
1. Geef de nieuwe regel de naam **Livefyre Analytics**.
1. Vouw het configuratiegebied van de **voorwaarden** uit.
1. Typ in het veld **String** `livefyre_analytics`.
1. Vouw het gedeelte Javascript-/derde tag uit en klik op de knop Nieuw script **** toevoegen.
1. Voer **LiveCycle Analytics Config** in in het invoervak **Tagnaam** .
1. Selecteer **Niet-opeenvolgende JavaScript**.
1. Voer de volgende LiveCycle-configuratiecode in de code-editor in en klik op de knop Code **** opslaan.

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
     } 
     ]
   
     /** 
   ```

   * Voegt een analytische handler toe voor alle analytische gebeurtenissen van Livefyre. Voor elke gebeurtenis worden de gegevens op een globaal object ingesteld en wordt de gebeurtenis vervolgens verzonden.

   ```
   */ 
   function addAnalyticsHandler() {  
     Livefyre.analytics.addHandler(function (events) { 
       (events || []).forEach(function (data) {  
         console.log('Event handled:', data.type);  
         trackLivefyreEvent(data); 
       }); 
     }); 
   } 
   addAnalyticsHandler();  
   ```

1. Klik op Regel **** opslaan.

## Stap 6: Wijzigingen goedkeuren voor regel bij laden van pagina {#section_pxc_11t_ycb}

1. Ga naar **[!UICONTROL Approvals]** tabblad.
1. Klik op **[!UICONTROL Approve]**.
1. Klik **[!UICONTROL Yes, approve]** om uw goedkeuring te bevestigen.
1. Ga naar **[!UICONTROL Overview > Publish Queue]**.
1. Selecteer de regel die u wilt publiceren.
1. Klik op **[!UICONTROL Publish Selected]**.
1. Klik **[!UICONTROL Publish]** om te bevestigen dat u wilt publiceren.

## Script {#section_xkb_vft_mcb}

In de volgende voorbeeldcode worden de specifieke eVars toegewezen aan beschikbare LiveCyre Vars. De naam van de omzettingsvariabele Livefy ( `eVar`) (bijvoorbeeld, `appId`) brengt aan de naam toe u opstelling in de Manager van de Reeks van het Rapport (bijvoorbeeld, `eVar81`). Wijzig de `eVar` namen in dit script in de aangepaste conversievariabelen.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

In de volgende voorbeeldcode worden de specifieke gebeurtenissen die u instelt in Report Suite Manager toegewezen aan beschikbare LiveCycle-gebeurtenissen. In dit voorbeeld `event82` wordt ingesteld als een gebruikersinteractiegebeurtenis zonder onderscheid te maken tussen welk type gebruikersinteractiegebeurtenis (bijvoorbeeld het koppelen van inhoud). Dit is een efficiënte manier om alle informatie van de gebruikersinteractie in een blok te registreren. U kunt de gebeurtenissen in DTM Analytics UI met het Verwijzen van het Element van Gegevens ook in kaart brengen.

```
var eventMap = { 
  FlagCancel: 'event82',  
  FlagClick: 'event82',  
  FlagDisagree: 'event82',  
  FlagOffensive: 'event82',  
  FlagOffTopic: 'event82',  
  FlagSpam: 'event82',  
  Like: 'event82', 
  Load: 'event81',  
  RequestMore: 'event82',  
  ShareButtonClick: 'event82',  
  ShareFacebook: 'event82',  
  ShareOnPostClick: 'event82',  
  ShareTwitter: 'event82',  
  ShareURL: 'event82',  
  SortStream: 'event82',  
  TwitterLikeClick: 'event82', 
  TwitterReplyClick: 'event82',  
  TwitterRetweetClick: 'event82',  
  TwitterUserFollow: 'event82' 
};
```

In het volgende voorbeeld wordt aangegeven dat als er geen gebeurtenis in deze lijst staat, u niets hoeft te doen. U hoeft deze sectie met code niet te wijzigen.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

In de volgende code worden de gebeurtenistypen onderscheiden die worden `event82` vastgelegd. De conversievariabele, registreert het type van gebruikersinteractie, en het manuscript plaatst omhoog `eVar83` `eVar83` om de gegevens van de gebruikersinteractie door type te scheiden. Zo `eVar83` staat u toe om de geregistreerde gegevens in specifieke soorten gebruikersinteractie uit te breken.

```
  var vars = ['events'];  
  switch (event) { 
    case 'event82': s.eVar83 = data.type;  
      vars.push('eVar83');  
      break; 
    default: 
  } 
   
  ['generator', 'evars'].forEach(function (type) {  
    var obj = data[type]; 
    for (var d in obj) { 
      if (obj.hasOwnProperty(d) && evarMap[d]) {  
        s[evarMap[d]] = obj[d];  
        vars.push(evarMap[d]); 
      } 
    } 
  }); 
   
  s.linkTrackVars = vars.join(',');  
  s.linkTrackEvents = event;  
  s.events = event; 
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

Het volgende codevoorbeeld voegt een manager toe om aan alle gebeurtenissen te luisteren die gebeuren. De pagina wordt geladen volgens de regel voor het laden van de pagina, er wordt gewacht tot er gebeurtenissen zijn, en vervolgens wordt de handler voor alle gebeurtenissen vanuit de app ingesteld en bijgehouden. U hoeft deze code niet te wijzigen.

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## Meer informatie

Voor meer informatie over de onderwerpen die op deze pagina worden besproken, zie:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Regels](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
