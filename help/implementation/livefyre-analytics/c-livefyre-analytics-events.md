---
title: Gebeurtenissen van Livefyre Analytics
description: Gebeurtenissen van Livefyre Analytics
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Gebeurtenissen van Livefyre Analytics

## Gebeurtenisobjectdefinitie {#section_dh1_yhn_pdb}

De volgende code definieert de velden in het gebeurtenisobject die door de handler Analytics op een pagina worden ontvangen.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Gebeurtenissen en gebeurtenissen voor Livefyre-analyse {#section_u3k_tft_mcb}

De volgende Livefy-gebeurtenissen moeten worden toegewezen aan aangepaste gebeurtenissen die moeten worden gebruikt in rapporten met de rapportsuite Manager. Voor meer informatie over de Reeksen van het Rapport in Adobe Analytics, zie [de Manager van de Reeks van het Rapport](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html). Raadpleeg [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb) voor meer informatie over het gebruik van LiveCycle-gebeurtenissen met Report Suite Manager.

## Gebeurtenissen van Livefyre Analytics

| Gebeurtenis | Beschrijving |
|---|---|
| Init | Wanneer een pagina met ten minste één LiveCycle-app wordt geladen |
| Laden | Elke keer dat een app op een pagina is geladen, ongeacht de weergave van de gebruiker |
| Weergave | Wanneer een app de viewport voor de eerste keer heeft ingevoerd. |
| Post | Elke keer dat een gebruiker een opmerking of inhoud, zoals bijvoorbeeld: berichttekst op hoofdniveau, antwoorden, revisies, uploaden naar mediamuur |
| Gepost | Toen een bericht succesvol was. |
| Twitter_Reageren | Elke keer dat een gebruiker op Twitter heeft gereageerd |
| Twitter_like | Waar inhoud is gedeeld naar: Retweet |
| Livefre_like | Elke keer dat de levensechte functie wordt gebruikt in een app |
| Livefyre_Unlike | Elke keer dat een gebruiker een levensstijl niet leuk vindt |
| ShareOnPost | Telkens wanneer een gebruiker inhoud plaatst en de functie Delen op post gebruikt |
| ShareButtonClick | Wanneer een gebruiker op de deelknop klikt voor een opmerking |
| ShareTwitter | Wanneer op Delen naar Twitter wordt geklikt |
| ShareFacebook | Wanneer op Delen naar Facebook wordt geklikt |
| ShareURL | Wanneer Delen naar URL-tekstgebied is geselecteerd/gekopieerd. |
| ExpandReplies | Wanneer een gebruiker op + of breid verbinding uit om alle reacties op een hoogste post te bekijken |
| CollapseReplies | Wanneer een gebruiker op de koppeling - of Samenvouwen klikt om alle reacties op een bovenste bericht weer te geven |
| FlagClick | Elke keer dat een gebruiker de Vlagmodus opent |
| FlagSpam | Wanneer een gebruiker inhoud markeert als spam |
| FlagDisagreement | Wanneer een gebruiker inhoud markeert als ongelijk |
| FlagOffsive | Wanneer een gebruiker inhoud als aanstootgevend markeert |
| FlagOffTopic | Wanneer een gebruiker inhoud als buiten onderwerp markeert |
| FlagCancel | Wanneer een gebruiker op X of &quot;Annuleren&quot; klikt bij het verzenden van een markering |
| FollowCollection | Elke keer dat een gesprek wordt gevolgd (&quot;Ik ben geïnteresseerd&quot; in Revisies) |
| UnfollowCollection | Wanneer een gesprek niet wordt gevolgd |
| RequestMore | Op elk moment dat een gebruiker meer inhoud in een app heeft geladen (dit moet ook voor hoge snelheid zijn) |
| ModalView | Wanneer een gebruiker klikt om inhoud in een modaal weer te geven |
| TwitterRetweetClick | Waar inhoud is gedeeld naar: Retweet |
| PostButtonClick | Wanneer een gebruiker op de post klikt (&quot;Wat in je geest?&quot;) knop |
| Aanmelden | Op elk moment dat een gebruiker zich heeft aangemeld |
| Afmelden | Elke keer dat een gebruiker zich afmeldt |

Hieronder volgt een lijst met conversievariabelen (eVars) die door Livefyre worden verschaft.

## Conversievariabelen - Vars

| Gebeurtenis | Beschrijving |
|--- |--- |
| Netwerk-id | Netwerk-id/naam in LiveCyre |
| Toepassings-id | De URL van de app |
| Context-id | Inhoud-id in LiveCyre |
| App-type | Livefyre App Type. Opties: <br><ul><li>Live blog  </li><li> Functiekaart</li><li>Carousel</li><li>Chat </li><li>Opmerkingen</li><li>Filmstrip</li><li>Kaart</li><li>Mozaïek</li><li>Mediumwand</li><li>Trend</li><li>Knop Uploaden</li></ul> |
| Inhoudstype | Instagram, Twitter, Facebook, LiveFyre, YouTube, enz. |

## Meer informatie {#section_b3d_4yl_pdb}

Voor meer informatie over de onderwerpen die op deze pagina worden besproken, zie:

* [Report Suite ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[ManagerDTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [Regels](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
