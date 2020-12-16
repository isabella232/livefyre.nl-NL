---
description: Maak een uniek token op uw server dat elke verzameling identificeert die u maakt.
seo-description: Maak een uniek token op uw server dat elke verzameling identificeert die u maakt.
seo-title: CollectionMeta-token
solution: Experience Manager
title: CollectionMeta-token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: 6978f0f36b5698c9c599c1828edea67703423397
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---


# CollectionMeta Token{#collectionmeta-token}

Maak een uniek token op uw server dat elke verzameling identificeert die u maakt.

LiveCycle wijst een unieke id toe aan elke verzameling die u maakt. Livefyre wijst een titel, URL, en andere parameters toe, die omvatten:

## collectionMeta Token Parameters

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| networkName | Tekenreeks (optioneel) | De naam van het Livefyre-netwerk (beschikbaar via [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials]). Dit is optioneel wanneer u de bibliotheek gebruikt om een token voor collectionMeta te maken. |
| networkKey | Tekenreeks (optioneel) | De geheime sleutel voor het specifieke netwerk (beschikbaar bij Studio > Instellingen > Integratie-instellingen > Referenties). Dit is optioneel wanneer u de bibliotheek gebruikt om een token voor collectionMeta te maken. |
| siteId | Tekenreeks (optioneel) | De id voor de site (beschikbaar via [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Optioneel wanneer u de bibliotheek gebruikt om een token voor collectionMeta te maken. |
| siteKey | Tekenreeks (optioneel) | De geheime sleutel voor de site (beschikbaar via [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| artikelId | Tekenreeks (optioneel) | Een unieke id voor de verzameling. |
| titel | Tekenreeks (optioneel) | De titel die u op de verzameling wilt toepassen. Gewoonlijk komt dit overeen met de titel van de pagina waarop de app wordt weergegeven. <br>Bijvoorbeeld: &quot;Integratie is zo leuk!&quot; <br>Opmerking: De maximale tekenlengte voor de titel is 255 tekens. Het titelveld ondersteunt geen HTML-entiteiten. Codeer speciale tekens met UTF-8. |
| url | Tekenreeks (optioneel) | De canonieke absolute URL die u aan deze verzameling wilt koppelen. Deze URL wordt gebruikt om koppelingen naar de app te genereren op basis van inhoud die wordt gedeeld op Facebook en Twitter, e-mailmeldingen en LiveCyre Studio. <br>Opmerking: Gebruik een geldig basis-URL-domein voor lokale tests (bijvoorbeeld: geldig:  `https://customer.com`; ongeldig:  `https://localhost:5995`). |
| tags | Tekenreeks (optioneel) | Een door komma&#39;s gescheiden lijst met enkele trefwoorden of woordgroepen. Verzamelingen zoeken op tags met gebruik van Studio.  </br>Opmerking: Tags mogen geen spaties bevatten. Gebruik onderstrepingstekens als u een spatie wilt weergeven in de gebruikersinterface. |
| extensions | JSON (optioneel) | Een set params met JSON-indeling die aan de verzameling worden doorgegeven. |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre ontvangt het token collectionMeta dat u bouwt en bepaalt uniciteit door siteId (opgegeven bibliotheek) en articleId (opgegeven klant) te combineren.
