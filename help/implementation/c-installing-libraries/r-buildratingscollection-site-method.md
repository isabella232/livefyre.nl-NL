---
description: Retourneert een object Collection dat is geïnstantieerd als een type waardering. Voer create_or_update() uit vanaf het object Collection om het constructieproces te voltooien.
title: buildRatingsCollection-sitemethode
exl-id: 84af3bb2-95f0-40e0-9a4e-830772a71862
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# buildRatingsCollection Site Method{#buildratingscollection-site-method}

Retourneert een object Collection dat is geïnstantieerd als een type waardering. Voer create_or_update() uit vanaf het object Collection om het constructieproces te voltooien.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| titel | String | De titel voor de verzameling. |
| artikelId | String | Een unieke artikel-id die u hebt gekozen om een verzameling binnen uw site te identificeren. |
| url | String | De canonieke absolute URL voor deze verzameling. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Python-voorbeeld {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```
