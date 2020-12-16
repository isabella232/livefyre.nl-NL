---
description: Automatiseer het proces met de functie-API's
seo-description: Automatiseer het proces met de functie-API's
seo-title: Functie-API's
title: Functie-API's
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Functie-API&#39;s{#feature-apis}

Automatiseer het proces met de functie-API&#39;s

Gebruik de functie-API&#39;s om het proces te automatiseren waarbij inhoud wordt aanbevolen. Bijvoorbeeld, wanneer het creëren van een Levende Blog of CommentaarApp, kenmerk alle inhoud die door een geselecteerde moderator wordt gepost om het gesprek te sturen, en consistentie binnen de stroom te vestigen.

LiveCycle biedt zowel functie- als functie-API&#39;s.

## Functie {#section_jpw_nqw_xz}

**Resource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; ga het gebruikerstoken voor uw geselecteerde moderator in.

**Gegevens verzenden**

```
{value: <number>} 
```

De waarde wordt gebruikt voor het sorteren van aanbevolen inhoud, het grootst tot het kleinst (10 wordt vóór 1 weergegeven in de lijst met aanbevolen inhoud). Deze waarde is standaard **now** in tijdperk, zodat aanbevolen opmerkingen doorgaans het nieuwste naar het oudste worden gesorteerd.

**Voorbeeld-reactie**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Het gegevensveld is nog niet in gebruik.

## Onbekend {#section_knh_mqw_xz}

**Resource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Ga het gebruikerstoken voor uw geselecteerde moderator in.

**Voorbeeld-reactie**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Het gegevensveld is nog niet in gebruik.

