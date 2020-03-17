---
description: Deze methode keert URN voor de gebruiker van dit netwerk terug.
seo-description: Deze methode keert URN voor de gebruiker van dit netwerk terug.
seo-title: getUrnForUser Netwerkmethode
solution: Experience Manager
title: getUrnForUser Netwerkmethode
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrnForUser Netwerkmethode{#geturnforuser-network-method}

Deze methode keert URN voor de gebruiker van dit netwerk terug.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| userId | String | De userId die in de URN moet worden gebruikt. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Voorbeeld van NodeJS {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Voorbeeld van Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
