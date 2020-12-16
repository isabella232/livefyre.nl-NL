---
description: Maak een nieuwe verzameling door een token collectionMeta te maken dat wordt doorgegeven aan LiveCycle.
seo-description: Maak een nieuwe verzameling door een token collectionMeta te maken dat wordt doorgegeven aan LiveCycle.
seo-title: Creeer een Inzameling gebruikend de Token CollectionMeta
solution: Experience Manager
title: Creeer een Inzameling gebruikend de Token CollectionMeta
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Creeer een Inzameling gebruikend de Token CollectionMeta{#create-a-collection-using-the-collectionmeta-token}

Maak een nieuwe verzameling door een token collectionMeta te maken dat wordt doorgegeven aan LiveCycle.

1. Maak het token collectionMeta.
1. Maak de controlesom.

   De controlesom is vereist als u Livefyre op de hoogte wilt brengen van wijzigingen die u hebt aangebracht in uw verzameling. Livefyre zal uw Inzameling slechts bijwerken als de geleverde controlesom verschillend is dan de eerder verzonden controlesom. Het creëren van een controlesom is enkel als het creëren van een `collectionMeta` teken maar in plaats van het roepen `buildCollectionMetaToken` roept u `buildChecksum`.

Maak gebruikerstokens voor verificatie in LiveCycle.