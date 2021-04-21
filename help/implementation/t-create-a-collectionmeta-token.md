---
description: Maak een nieuwe verzameling door een token collectionMeta te maken dat wordt doorgegeven aan LiveCycle.
title: Creeer een Inzameling gebruikend de Token CollectionMeta
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Creeer een Inzameling gebruikend de Token CollectionMeta{#create-a-collection-using-the-collectionmeta-token}

Maak een nieuwe verzameling door een token collectionMeta te maken dat wordt doorgegeven aan LiveCycle.

1. Maak het token collectionMeta.
1. Maak de controlesom.

   De controlesom is vereist als u Livefyre op de hoogte wilt brengen van wijzigingen die u hebt aangebracht in uw verzameling. Livefyre zal uw Inzameling slechts bijwerken als de geleverde controlesom verschillend is dan de eerder verzonden controlesom. Het creëren van een controlesom is enkel als het creëren van een `collectionMeta` teken maar in plaats van het roepen `buildCollectionMetaToken` roept u `buildChecksum`.

Maak gebruikerstokens voor verificatie in LiveCycle.
