---
description: Deze methode keert URN voor deze Inzameling terug. U moet createOrUpdate() uitvoeren voordat u deze methode uitvoert.
seo-description: Deze methode keert URN voor deze Inzameling terug. U moet createOrUpdate() uitvoeren voordat u deze methode uitvoert.
seo-title: getUrn, verzamelingsmethode
solution: Experience Manager
title: getUrn, verzamelingsmethode
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# getUrn-verzamelingsmethode{#geturn-collection-method}

Deze methode keert URN voor deze Inzameling terug. U moet createOrUpdate() uitvoeren voordat u deze methode uitvoert.

## Java-voorbeeld {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## NodeJS-voorbeeld {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

Voorbeelduitvoer:

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python-voorbeeld {#section_dwg_gds_rz}

```
collection.urn() 
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
collection.urn
```

Voorbeelduitvoer:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

