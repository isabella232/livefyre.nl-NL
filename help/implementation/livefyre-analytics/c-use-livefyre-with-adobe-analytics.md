---
description: Stel Adobe Analytics en Dynamic Tag Manager (DTM) in om gegevens voor LiveCycle-apps te verzamelen.
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
translation-type: tm+mt
source-git-commit: 24d016fbb2771487f8105b2ca0bb0d03dd60cfc1
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# LiveCycle gebruiken met Adobe Analytics en Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Stel Adobe Analytics en Dynamic Tag Manager (DTM) in om gegevens voor LiveCycle-apps te verzamelen.

## Stap 1: Gebeurtenissen instellen in Adobe Analytics {#section_iks_kgd_4cb}

Wijs livegebeurtenissen toe aan een of meer aangepaste succesgebeurtenissen in Adobe Analytics Report Suite Manager.

Voor meer informatie over de Manager van de Reeks van het Rapport, zie [de Manager van de Reeks ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html).

1. Meld u aan bij Adobe Analytics als beheerder.
1. Open Adobe Analytics Admin Report Suite Manager.
1. Maak een nieuwe rapportsuite of kies een bestaande rapportsuite.
1. Bewerk de rapportsuite door op de rapportsuite te klikken die u wilt wijzigen en navigeer vervolgens naar **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Wijs de Livefyre-gebeurtenissen toe aan een of meer aangepaste succesgebeurtenissen.

## Stap 2: Conversievariabelen instellen

Wijs bibliotheekconversievariabelen (eVars) toe aan conversievariabelen in Adobe Analytics Admin Report Suite Manager. Conversievariabelen fungeren als een sorteerfunctie om te bepalen hoe u gegevens wilt identificeren die uit LiveCycle-gebeurtenissen zijn verzameld.

1. Klik in Report Suite Manager op **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Kies de aangepaste conversievariabelen (eVars) die u wilt gebruiken en wijs deze toe aan de bibliotheekconversievariabelen. U kunt als volgt een conversievariabele Livefyre toewijzen aan een aangepaste conversievariabele:
* De conversievariabele inschakelen
* De conversievariabele een naam geven
* De conversievariabele een type geven
1. Sla de aangepaste conversievariabelen op.

## Stap 3: DTM gebruiken om uw rapportsuite toe te voegen met LiveCycle Events {#section_t15_2hd_4cb}

Voeg Adobe Analytics toe aan DTM om Analytics te laten werken. Hiertoe maakt u een nieuwe eigenschap en een nieuw gereedschap en voegt u de nieuwe rapportsuite met LiveCycle-gebeurtenissen toe aan de eigenschap. Zie [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html) voor meer informatie over DTM.

U hoeft deze stap niet uit te voeren als u al een eigenschap of gereedschap hebt ingesteld voor de rapportsuite die u hebt ingesteld met LiveCycle-gebeurtenissen.

1. Maak of bewerk een bestaande eigenschap in DTM.
1. Maak of bewerk een bestaand Adobe Analytics-gereedschap.
1. Als een bestaand Adobe Analytics-gereedschap niet bestaat, klikt u op de knop **[!UICONTROL Add a Tool]**.
Stel de volgende parameters in voor het gereedschap:

   * Stel **[!UICONTROL Tool Type]** in op **[!UICONTROL Adobe Analytics]**.
   * **[!UICONTROL Automatic Configuration]** inschakelen.
   * **[!UICONTROL Authenticate via Marketing Cloud]** inschakelen.
1. Voeg of bevestig de naam van de rapportsuite met LiveCycle-gebeurtenissen toe aan het veld **[!UICONTROL Report Suites]**.

## Stap 4: Opstelling een Regel van de Lading van de Pagina aan de Behandeling van de Analyse van de Opstelling {#section_jfj_j3d_4cb}

Stel een regel voor het laden van pagina in om alle gegevens op te halen. Met de regel Pagina laden kunt u aangepaste javascript in de regel plaatsen die de gebeurtenis vastlegt wanneer de pagina wordt geladen.

>[!NOTE]
>
>Gebruik geen op gebeurtenis gebaseerde Regels of Directe Regels van de Vraag.

1. Selecteer **[!UICONTROL Rules]** tab in DTM.
1. Klik op **[!UICONTROL Page Load Rules]**.
1. Klik op de **[!UICONTROL Create New Rule]** knoop.
1. Open de sectie **[!UICONTROL Conditions]** door op de **[!UICONTROL Plus]** knoop te klikken.
1. Trigger de regel. Kies **[!UICONTROL DOM Ready]** of **[!UICONTROL Onload]** trekkertypes als u de regel asynchroon wilt vertragen of uitvoeren.
1. (Optioneel) Voeg aanvullende parameters toe om de pagina&#39;s te beperken die Live Apps weergeven. Voor meer informatie over extra configuratieopties, zie [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).
1. Klik onder **[!UICONTROL Javascript/ Third Party Tags]** op het tabblad **[!UICONTROL Non-sequential]** en klik vervolgens op **[!UICONTROL Add New Script]**.
1. Selecteer **[!UICONTROL Sequential HTML]** als scripttype.
1. Voeg het volgende manuscript in de coderedacteur toe en klik **[!UICONTROL Save Code]**.

   Het volgende manuscript roept `livefyre_analytics` directe vraagregel nadat de Livefy JavaScript laadt. In het volgende scriptvoorbeeld wordt om de 400 ms gecontroleerd of `livefyre.analytics` op de pagina staat. Nadat de pagina is geladen, verzendt livefyre.analytics trackinggegevens.

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

## Stap 5: Creeer een Directe Regel van de Vraag om de Configuratie van de Toewijzing van Adobe Analytics voor Levensstijl {#section_gvp_b1g_pdb} te construeren

Er zijn andere manieren om Livefyre met DTM uit te voeren door aangepaste gebeurtenissen, de gebieden van Adobe Analytics UI binnen DTM, en gegevenselementen te gebruiken. In dit document wordt aangepaste JavaScript gebruikt om hetzelfde effect te bereiken.

1. In DTM selecteer **Rules** tabel en klik dan op **Directe Regels van de Vraag**.
1. Klik op de **Create Nieuwe Regel** knoop.
1. Noem de nieuwe regel **Livefyre Analytics**.
1. Vouw het configuratiegebied **conditions** uit.
1. Typ `livefyre_analytics` in het veld **String**.
1. Vouw de sectie Javascript/3rd Party-tag uit en klik op de knop **Nieuw script toevoegen**.
1. Typ **LiveCycle Analytics Config** in het invoervak **Tagnaam**.
1. Selecteer **Niet-opeenvolgende JavaScript**.
1. Voer de volgende LiveCycle-configuratiecode in de code-editor in en klik op de knop **Code opslaan**.

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

1. Klik op **Regel opslaan**.

## Stap 6: Wijzigingen goedkeuren voor regel bij laden van pagina {#section_pxc_11t_ycb}

1. Ga naar **[!UICONTROL Approvals]** tabblad.
1. Klik op **[!UICONTROL Approve]**.
1. Klik **[!UICONTROL Yes, approve]** om uw goedkeuring te bevestigen.
1. Ga naar **[!UICONTROL Overview > Publish Queue]**.
1. Selecteer de regel die u wilt publiceren.
1. Klik op **[!UICONTROL Publish Selected]**.
1. Klik **[!UICONTROL Publish]** om te bevestigen dat u wilt publiceren.

## Script {#section_xkb_vft_mcb}

In de volgende voorbeeldcode worden de specifieke eVars toegewezen aan beschikbare LiveCyre Vars. De naam van de omzettingsvariabele Livefyre ( `eVar`) (bijvoorbeeld `appId`) brengt aan de naam toe u opstelling in de Manager van de Reeks van het Rapport (bijvoorbeeld, `eVar81`). Wijzig de `eVar`-namen in dit script in de aangepaste conversievariabelen.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

In de volgende voorbeeldcode worden de specifieke gebeurtenissen die u instelt in Report Suite Manager toegewezen aan beschikbare LiveCycle-gebeurtenissen. In dit voorbeeld wordt `event82` ingesteld als een gebruikersinteractiegebeurtenis zonder onderscheid te maken tussen welk type gebruikersinteractiegebeurtenis (bijvoorbeeld het maken van een koppeling of het delen van inhoud). Dit is een efficiënte manier om alle informatie van de gebruikersinteractie in een blok te registreren. U kunt de gebeurtenissen in DTM Analytics UI met het Verwijzen van het Element van Gegevens ook in kaart brengen.

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

De volgende code maakt onderscheid tussen de gebeurtenistypen die `event82` registreert. De conversievariabele, `eVar83` registreert het type van gebruikersinteractie, en het manuscript plaatst omhoog `eVar83` om de gegevens van de gebruikersinteractie door type te scheiden. Zo `eVar83` staat u toe om de geregistreerde gegevens in specifieke soorten gebruikersinteractie uit te breken.

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

* [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [Regels](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
