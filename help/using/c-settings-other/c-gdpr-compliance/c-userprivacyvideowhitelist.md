---
description: U kunt een whitelist van uw videodomein gebruiken.
seo-description: U kunt een whitelist van uw videodomein gebruiken.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Als u uw eigen aangepaste video&#39;s en spelers gebruikt als onderdeel van de video&#39;s die worden weergegeven in een Livefyre-visualisatie-app, kunt u een whitelist maken van uw videodomein. Wanneer u een whitelisting uitvoert op uw videodomein, verwijdert u het videomasker voor uw aangepaste video&#39;s en spelers.

>[!NOTE]
>
>Gebruik specifieke paden om ervoor te zorgen dat alleen de video&#39;s die veilig zijn, worden gewhitelist. Als u een breed pad plaatst (bijvoorbeeld voorbeelddomein.com), kunt u onveilige video&#39;s whitelist.

* Toevoegen `userPrivacyVideoWhitelist` na `userPrivacyOptOut`. U kunt alle privacymarkeringen voor Livefyre tegelijk toevoegen als onderdeel van één Livefyre-object.
* `userPrivacyVideoWhitelist` is alleen van toepassing op inhoud die niet is ingesloten via sociale media.

In het volgende voorbeeld worden video&#39;s die in Apps met het `sampledomain.com/cdn/videos` pad worden weergegeven, gewhitelliseerd:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
