---
description: Leer hoe u de door de gebruiker gegenereerde inhoud die door het Livefyre-systeem stroomt, kunt controleren en opslaan.
seo-description: Leer hoe u de door de gebruiker gegenereerde inhoud die door het Livefyre-systeem stroomt, kunt controleren en opslaan.
seo-title: Activiteitenstroom
solution: Experience Manager
title: Activiteitenstroom
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Activiteitenstroom {#activity-stream}

Leer hoe u de door de gebruiker gegenereerde inhoud die door het Livefyre-systeem stroomt, kunt controleren en opslaan.

Gebruik de Activiteitenstroom-API om door de gebruiker gegenereerde gegevens te gebruiken die via het LiveCycle-systeem op uw netwerk of site stromen. Bijvoorbeeld: gegevens van deze API gebruiken om uw zoekindices bij te werken op basis van beoordelingen of om gebruikersbadges te beheren in een systeem van derden op basis van hun activiteit.

Activiteitenstroom-API:

Zie de sectie LiveCyre API Reference voor een volledige lijst met beschikbare eindpunten.

## Bronnen {#section_aql_n4l_b1b}

Er zijn twee eindpunten, één voor de halteplaats, en één voor productie.

### Staging

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Productie

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parameters

* **resource:** *tekenreeks* A URN van het object waarvoor u activiteitsgegevens aanvraagt.

* **sinds:** Een 64-bits geheel *getal* dat de id vertegenwoordigt van de laatste gebeurtenis die u hebt ontvangen. Geef &quot;0&quot; op als u geen eerdere gegevens hebt.

## URN-tekenreeksen {#section_skl_q4l_b1b}

Voorbeelden:

* **urn:livefyre:** `example.fyre.co` De activiteitsstroom voor `example.fyre.co`.
* **urn:livefyre:** `example.fyre.co:site=54321` De activiteitsstroom voor plaats 54321 onder het `example.fyre.co` netwerk.

## Tokenbeleid {#section_nwh_c5j_11b}

De Activiteitenstroom-API gebruikt een OAuth-token voor verificatie. Dragertokens maken deel uit van de OAuth 2.0-specificatie en worden [hier](https://tools.ietf.org/html/rfc6750#section-1.2)officieel beschreven.

Een token bevat verschillende elementen:

* Wie heeft de token gemaakt.
* Wie kreeg een token.
* Een tijdstip waarop deze niet langer geldig is.
* Het ding waar we mee bezig zijn.
* Een lijst met machtigingen die zijn verleend.

### Stappen

De stappen om een Token van de Drager van OAuth tot stand te brengen omvatten:

* Maak een kaart/woordenboek met de uitgever, het publiek, het onderwerp, de vervaldatum en het bereik.
* Gebruik de JWT-bibliotheek, met uw geheim, om een JWT-token te coderen.
* &quot;Verificatie toevoegen: Drager&quot; aan uw HTTP-aanvraag.

In het onderstaande codevoorbeeld ziet u de bovenstaande stappen in Python:

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Wanneer de toonder-tokens als volgt worden gedefinieerd:

* **is** *(Uitgever)* Een entiteit met de bevoegdheid tokens te genereren. Dit kan Livefyre, een plaats of een netwerk zijn. (Een notitie die laat op school moet zijn, is uw ouder.)
* **aud** *(Publiek)* De persoon voor wie dit teken werd geproduceerd. Als u het token zelf maakt, is dit de site of het netwerk.
* **sub** *(Onderwerp)* Het onderwerp waarvoor toestemmingen moeten worden verleend. Als u bijvoorbeeld een verzameling gebruikt, moet het onderwerp de id voor de verzameling zijn. (In de notitie van het schoolvoorbeeld bent u het.)
* **exp** *(Expiration)* A point in time which the token is no longer valid.
* **scope** *(Scope)* This is a list of the permissions allowed on the subject. &quot;Te laat voor school&quot; is een voorbeeld. De naam van een API is een ander voorbeeld.

## Voorbeeld {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Antwoord {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Een reactie met nieuwe gegevens sinds het laatste verzoek:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Notities {#section_hj3_crj_11b}

* Een geslaagde aanroep van de API levert een HTTP 200-statuscode op. Alle andere statuscodes moeten als fouten worden beschouwd.
* Als de waarde niet null is, gebruikt u de waarde van `data.meta.cursor.next` als de `since` parameter van uw volgende aanvraag.
* Als de waarde van `data.meta.cursor.next` null is, betekent dit dat er geen nieuwe gegevens zijn om te verbruiken. U zou later met de zelfde `since` waarde opnieuw moeten verzoeken om te zien of zijn de nieuwe gegevens gearriveerd.
* In de praktijk moet u onmiddellijk om meer gegevens vragen als de `data.meta.cursor.next` waarde niet null is.
* Ongeveer twee uur van recente gegevens is beschikbaar door deze API in productie.
* U zou uw processen moeten opstelling om dit eindpunt regelmatig op baan te onderzoeken om ontbrekende gegevens te vermijden. Voor de meeste implementaties moet een interval van vijf minuten perfect toereikend zijn.
