---
description: Retourneert een object Collection dat is geïnstantieerd als een chattype. Voer create_or_update() uit vanaf het object Collection om het constructieproces te voltooien.
seo-description: Retourneert een object Collection dat is geïnstantieerd als een chattype. Voer create_or_update() uit vanaf het object Collection om het constructieproces te voltooien.
seo-title: Site-methode buildChatCollection
solution: Experience Manager
title: Site-methode buildChatCollection
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# buildChatCollection Site Method{#buildchatcollection-site-method}

Retourneert een object Collection dat is geïnstantieerd als een chattype. Voer create_or_update() uit vanaf het object Collection om het constructieproces te voltooien.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| titel | String | De titel voor de verzameling. |
| artikelId | String | Een unieke artikel-id die u hebt gekozen om een verzameling binnen uw site te identificeren. |
| url | String | De canonieke absolute URL voor deze verzameling. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python-voorbeeld {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
