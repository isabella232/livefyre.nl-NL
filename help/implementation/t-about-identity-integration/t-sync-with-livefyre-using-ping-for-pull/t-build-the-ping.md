---
description: Bouw pingelen zodat pingelt uw pagina Leven wanneer de gebruikers hun profiel bijwerken.
seo-description: Bouw pingelen zodat pingelt uw pagina Leven wanneer de gebruikers hun profiel bijwerken.
seo-title: Pingelen samenstellen
solution: Experience Manager
title: Pingelen samenstellen
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Ping{#build-the-ping} samenstellen

Bouw pingelen zodat pingelt uw pagina Leven wanneer de gebruikers hun profiel bijwerken.

Wanneer Livefyre een updatebericht met `networkName` en `user_id` ontvangt, zal het systeem een Pull- verzoek naar uw Ping voor Pull URL verzenden.

>[!NOTE]
>
>403/Niet geautoriseerd in antwoord op uw pingelen wijst op ongeldig `lftoken` toegevoegd aan het pingsverzoek. Zorg ervoor dat de `lftoken` bedoeld is voor een `user_id` met bevoegdheden voor de netwerkeigenaar of de systeemgebruiker. Als u bibliotheken Livefy gebruikt, gebruik `buildLivefyreToken` methode om een geldig systeemteken voor het verzoek te produceren.

1. Voeg code toe aan uw pagina die LiveCycle pingelt wanneer de gebruikers hun profiel bijwerken. Construeer de URL op deze manier:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Uw door Livefyre opgegeven netwerknaam.
   * **[!UICONTROL user_id:]** De gebruikersnaam.
   * **[!UICONTROL token:]** Geldige systeemtoken.

1. Trek de aanvraagstructuur uit.
