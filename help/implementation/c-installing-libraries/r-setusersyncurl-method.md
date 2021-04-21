---
description: Hiermee wordt Livefyre gevraagd de URL voor de gebruikerssynchronisatie van het netwerk bij te werken naar de URL die wordt opgegeven. Retourneert een Booleaanse waarde.
title: setUserSyncUrl Netwerkmethode
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# setUserSyncUrl Netwerkmethode{#setusersyncurl-network-method}

Hiermee wordt Livefyre gevraagd de URL voor de gebruikerssynchronisatie van het netwerk bij te werken naar de URL die wordt opgegeven. Retourneert een Booleaanse waarde.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| urlTemplate | String | De URL die bij LiveCycle moet worden geregistreerd voor het synchroniseren van gebruikers-id&#39;s. Vereist &quot;`{id}`&quot;deel van het verstrekte koord URL uit te maken. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Voorbeelduitvoer:

```
true
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

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

## Python-voorbeeld {#section_dwg_gds_rz}

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
