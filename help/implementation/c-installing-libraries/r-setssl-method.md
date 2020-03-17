---
description: Plaatst SSL voor API vraag om of weg te zijn.
seo-description: Plaatst SSL voor API vraag om of weg te zijn.
seo-title: setSSL-netwerkmethode
solution: Experience Manager
title: setSSL-netwerkmethode
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setSSL-netwerkmethode{#setssl-network-method}

Plaatst SSL voor API vraag om of weg te zijn.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| ssl | Boolean | De standaardwaarde is true. als u SSL wilt inschakelen, anders false. <br><ul><li>Waar - SSL ingeschakeld </li><li>Onwaar - SSL uitgeschakeld</li></ul> |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Voorbeeld van NodeJS {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Voorbeeld van Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
network.ssl = false 
```
