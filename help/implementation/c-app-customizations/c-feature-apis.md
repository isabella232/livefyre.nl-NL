---
description: Automatiseer het proces met de functie-API's
title: Functie-API's
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
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
