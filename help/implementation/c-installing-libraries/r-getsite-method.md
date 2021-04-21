---
description: Retourneert een nieuw Site-object.
title: getSite-netwerkmethode
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
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
