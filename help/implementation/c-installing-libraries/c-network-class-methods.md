---
description: Maak een Network-object.
title: Methoden van de netwerkklasse
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 3%

---

# Methoden van de Klasse van het netwerk{#network-class-methods}

Maak een Network-object.

Zodra u een netwerkvoorwerp creeert, zal de rest van de pagina veronderstellen dat u een geconcretiseerd voorwerp van het Netwerk in uw zitting hebt.

## Netwerkobject

| Parameter | Type | Beschrijving |
|---|---|---|
| *`network`* | String | Uw Livefyre-netwerk. Bijvoorbeeld: “`labs.fyre.co`”. |
| *`networkKey`* | String | De Levenslang-verstrekte geheime sleutel voor het netwerk. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
