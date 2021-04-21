---
description: Hiermee wordt Livefyre gevraagd om gebruikersgegevens van een eerder ingestelde URL voor gebruikerssynchronisatie te halen. Retourneert een Booleaanse waarde.
title: syncUser-netwerkmethode
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# syncUser Network Method{#syncuser-network-method}

Hiermee wordt Livefyre gevraagd om gebruikersgegevens van een eerder ingestelde URL voor gebruikerssynchronisatie te halen. Retourneert een Booleaanse waarde.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| userId | String | De gebruikersnaam die gesynchroniseerd moet worden met LiveCycle. U moet een URL voor gebruikerssynchronisatie hebben ingesteld met LiveCycle voordat u deze methode aanroept. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Voorbeelduitvoer:

```
true
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Voorbeelduitvoer:

```
true
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Voorbeelduitvoer:

```
true
```

## Python-voorbeeld {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Voorbeelduitvoer:

```
True
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Voorbeelduitvoer:

```
True
```
