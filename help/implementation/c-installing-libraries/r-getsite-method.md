---
description: Retourneert een nieuw Site-object.
seo-description: Retourneert een nieuw Site-object.
seo-title: getSite-netwerkmethode
solution: Experience Manager
title: getSite-netwerkmethode
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# getSite-netwerkmethode{#getsite-network-method}

Retourneert een nieuw Site-object.
|Variabele|Type|Beschrijving|
|— |— |— |
|siteId|String|De door LiveCycle verschafte id voor de website of toepassing waartoe de verzameling behoort. Bijvoorbeeld: 303617.  |
|siteKey|String|De door LiveCycle verstrekte geheime sleutel voor siteId.  |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python-voorbeeld {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

