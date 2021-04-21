---
description: U kunt een lijst met uw videodomein toestaan en weergeven.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Als u uw eigen aangepaste video&#39;s en spelers gebruikt als onderdeel van de video&#39;s die worden weergegeven in een Livefyre-visualisatie-app, kunt u het videodomein toestaan en weergeven. Wanneer u uw videodomein wilt weergeven, verwijdert u het videomasker voor uw aangepaste video&#39;s en spelers.

>[!NOTE]
>
>Gebruik specifieke paden om ervoor te zorgen dat alleen de video&#39;s die veilig zijn, worden weergegeven in de lijst met toegestane items. Als u een breed pad plaatst (bijvoorbeeld voorbeelddomein.com), kunt u onveilige video&#39;s toestaan en weergeven.

* `userPrivacyVideoWhitelist` toevoegen na `userPrivacyOptOut`. U kunt alle privacymarkeringen voor Livefyre tegelijk toevoegen als onderdeel van één Livefyre-object.
* `userPrivacyVideoWhitelist` is alleen van toepassing op inhoud die niet is ingesloten via sociale media.

In het volgende voorbeeld worden video&#39;s die worden weergegeven in Apps met het pad `sampledomain.com/cdn/videos`, weergegeven in de lijst met toegestane items:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
