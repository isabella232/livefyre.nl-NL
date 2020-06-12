---
description: U kunt een lijst met uw videodomein toestaan en weergeven.
seo-description: U kunt een lijst met uw videodomein toestaan en weergeven.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Als u uw eigen aangepaste video&#39;s en spelers gebruikt als onderdeel van de video&#39;s die worden weergegeven in een Livefyre-visualisatie-app, kunt u het videodomein toestaan en weergeven. Wanneer u uw videodomein wilt weergeven, verwijdert u het videomasker voor uw aangepaste video&#39;s en spelers.

>[!NOTE]
>
>Gebruik specifieke paden om ervoor te zorgen dat alleen de video&#39;s die veilig zijn, worden weergegeven in de lijst met toegestane items. Als u een breed pad plaatst (bijvoorbeeld voorbeelddomein.com), kunt u onveilige video&#39;s toestaan en weergeven.

* Toevoegen `userPrivacyVideoWhitelist` na `userPrivacyOptOut`. U kunt alle privacymarkeringen voor Livefyre tegelijk toevoegen als onderdeel van één Livefyre-object.
* `userPrivacyVideoWhitelist` is alleen van toepassing op inhoud die niet is ingesloten via sociale media.

In het volgende voorbeeld worden video&#39;s die in Apps met het `sampledomain.com/cdn/videos` pad worden weergegeven, weergegeven met de optie allow:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
