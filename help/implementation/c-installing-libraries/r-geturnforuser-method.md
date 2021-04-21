---
description: Deze methode keert URN voor de gebruiker van dit netwerk terug.
title: getUrnForUser Netwerkmethode
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# getUrnForUser Network Method{#geturnforuser-network-method}

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

## NodeJS-voorbeeld {#section_xkd_gds_rz}

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

## Python-voorbeeld {#section_dwg_gds_rz}

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
