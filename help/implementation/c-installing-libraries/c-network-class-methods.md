---
description: Maak een Network-object.
seo-description: Maak een Network-object.
seo-title: Methoden van de netwerkklasse
solution: Experience Manager
title: Methoden van de netwerkklasse
uuid: 4130beda-dd09-49ae-aafb-f6b956e30b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Methoden van de netwerkklasse{#network-class-methods}

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
