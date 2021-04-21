---
description: Retourneert een object Collection dat is geïnstantieerd als een type Opmerkingen. Voer createOrUpdate() uit vanaf het object Collection om het constructieproces te voltooien.
title: buildCommentsCollection-sitemethode
exl-id: 9534c25a-fd1c-4a09-92e2-d196ac218ef3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# buildCommentsCollection Site Method{#buildcommentscollection-site-method}

Retourneert een object Collection dat is geïnstantieerd als een type Opmerkingen. Voer createOrUpdate() uit vanaf het object Collection om het constructieproces te voltooien.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| titel | String | De titel voor de verzameling. |
| artikelId | String | Een unieke artikel-id die u hebt gekozen om een verzameling binnen uw site te identificeren. |
| url | String | De canonieke absolute URL voor deze verzameling. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python-voorbeeld {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
