---
description: Hiermee wordt Livefyre gevraagd om gebruikersgegevens van een eerder ingestelde URL voor gebruikerssynchronisatie te halen. Retourneert een Booleaanse waarde.
seo-description: Hiermee wordt Livefyre gevraagd om gebruikersgegevens van een eerder ingestelde URL voor gebruikerssynchronisatie te halen. Retourneert een Booleaanse waarde.
seo-title: syncUser-netwerkmethode
solution: Experience Manager
title: syncUser-netwerkmethode
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# syncUser-netwerkmethode{#syncuser-network-method}

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

## Voorbeeld van NodeJS {#section_xkd_gds_rz}

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

## Voorbeeld van Python {#section_dwg_gds_rz}

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
