---
description: Hiermee wordt Livefyre gevraagd de URL voor de gebruikerssynchronisatie van het netwerk bij te werken naar de URL die wordt opgegeven. Retourneert een Booleaanse waarde.
seo-description: Hiermee wordt Livefyre gevraagd de URL voor de gebruikerssynchronisatie van het netwerk bij te werken naar de URL die wordt opgegeven. Retourneert een Booleaanse waarde.
seo-title: setUserSyncUrl Netwerkmethode
solution: Experience Manager
title: setUserSyncUrl Netwerkmethode
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl Netwerkmethode{#setusersyncurl-network-method}

Hiermee wordt Livefyre gevraagd de URL voor de gebruikerssynchronisatie van het netwerk bij te werken naar de URL die wordt opgegeven. Retourneert een Booleaanse waarde.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| urlTemplate | String | De URL die bij LiveCycle moet worden geregistreerd voor het synchroniseren van gebruikers-id&#39;s. Vereist &quot;`{id}`&quot; om deel uit te maken van de opgegeven URL-tekenreeks. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Voorbeelduitvoer:

```
true
```

## Voorbeeld van NodeJS {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Voorbeelduitvoer:

```
true
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Voorbeelduitvoer:

```
true
```

## Voorbeeld van Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Voorbeelduitvoer:

```
True
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Voorbeelduitvoer:

```
True
```
