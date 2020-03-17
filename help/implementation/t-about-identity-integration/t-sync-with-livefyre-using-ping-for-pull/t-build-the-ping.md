---
description: Bouw pingelen zodat pingelt uw pagina Leven wanneer de gebruikers hun profiel bijwerken.
seo-description: Bouw pingelen zodat pingelt uw pagina Leven wanneer de gebruikers hun profiel bijwerken.
seo-title: Pingelen samenstellen
solution: Experience Manager
title: Pingelen samenstellen
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Pingelen samenstellen{#build-the-ping}

Bouw pingelen zodat pingelt uw pagina Leven wanneer de gebruikers hun profiel bijwerken.

Wanneer Livefyre een updatebericht met `networkName` en `user_id`ontvangt, zal het systeem een Pull- verzoek naar uw Ping voor Pull URL verzenden.

>[!NOTE]
>
>403/Niet geautoriseerd in antwoord op uw pingelen wijst op een ongeldig `lftoken` toegevoegd aan het Ping verzoek. Zorg ervoor dat het bestand `lftoken` bestemd is voor een `user_id` netwerk met bevoegdheden voor de eigenaar of de systeemgebruiker. Als u bibliotheken Livefy gebruikt, gebruik de `buildLivefyreToken` methode om een geldig systeemteken voor het verzoek te produceren.

1. Voeg code toe aan uw pagina die LiveCycle pingelt wanneer de gebruikers hun profiel bijwerken. Construeer de URL op deze manier:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Uw door Livefyre opgegeven netwerknaam.
* **[!UICONTROL user_id:]** De gebruikersnaam.
* **[!UICONTROL token:]** Geldige systeemtoken.

1. Trek de aanvraagstructuur uit.
