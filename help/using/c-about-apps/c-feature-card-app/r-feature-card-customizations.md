---
description: Wijzig de grootte, breedte en interactieopties van de app Map.
seo-description: Wijzig de grootte, breedte en interactieopties van de app Map.
seo-title: Aanpassing van functiekaarten
solution: Experience Manager
title: Aanpassing van functiekaarten
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# Aanpassingen voor functiekaarten{#feature-card-customizations}

Wijzig de grootte, breedte en interactieopties van de app Map.

<!-- 
r_feature_card_customization.dita
 -->

De Apps van de Kaart van de eigenschap omvatten slechts standaardaanpassingen:** [!UICONTROL Theme]**, de kleur van het Merk, de familie van de Doopvont, en de grootte van de Doopvont.

U kunt de kaarten van de Eigenschappen aanpassen gebruikend:

* **[!UICONTROL Style]** en  **[!UICONTROL Config]** opties voor alle toepassingen in de  **[!UICONTROL App Designer]** toepassing. Zie Apps aanpassen voor details over de standaard **[!UICONTROL Style]** en **[!UICONTROL Config]** opties voor alle Apps in **[!UICONTROL App Designer]**.

* Integratiegereedschappen. Zie Toepassingsintegratie voor meer informatie over het aanpassen van toepassingen met behulp van integratieprogramma&#39;s.
* **[!UICONTROL Call-to-action button]** U kunt de vraag-aan-actie knoop met een productcatalogus gebruiken om gebruikers aan een product of aan uw plaats voor verdere actie te leiden.

   * **[!UICONTROL Call-to-action button]** Schakelaar de knevel aan op om de vraag-aan-actie knoop te tonen.
   * **[!UICONTROL Require rights to display products]** Schakel de knevel aan op om te vereisen dat de inhoudseigenaar rechten voor de inhoud heeft verleend alvorens een vraag-aan-actie knoop voor de inhoud verschijnt.

      >[!NOTE]
      >
      >De inhoud toont zelfs als de rechten niet voor de inhoud worden verleend, maar de vraag-aan-actie knoop zal niet met de inhoud tonen tenzij de rechten voor de inhoud worden verleend.

   * **[!UICONTROL Call-to-action header text]** De woorden in de kopbal boven de vraag-aan-actie knoop in inhoud modaal te tonen. De standaardformulering is &quot;Deze producten kopen:&quot;.
   * **[!UICONTROL Call-to-action button text]** Pas de tekst op de vraag-aan-actie knoop aan. De standaardtekst is &#39;&#39;Nu kopen&#39;&#39;.
   * **[!UICONTROL Product display options]** Kies of u de vraag  **[!UICONTROL Photo]** en  **[!UICONTROL Product name]** met de vraag-aan-actie knoop wilt tonen.
   * **[!UICONTROL Product URL referral tracking]** Schakel de schakeloptie in om verwijzingen van deze app naar de bijbehorende productpagina bij te houden.
   * **[!UICONTROL Referral tracking key-value pairs]** Voeg parameters toe om verwijzing van uw inhoud van de App aan de bijbehorende productpagina verder te specificeren.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecteer deze optie om één app voor meerdere productpagina&#39;s te maken. Filter productspecifieke UGC voor elke productpagina naar de App. U kunt een of meer mappen selecteren om specifieke verzamelingen aan de app te koppelen.
   * **[!UICONTROL Select Product folders]**. Selecteer de productmappen op het hoogste niveau die u wilt gebruiken om UGC te filteren. Gebruik `CTRL/Command + click` om meer dan één map te selecteren. LiveCycle gebruikt de map om te bepalen welke producten in die map in de app op verschillende pagina&#39;s moeten worden weergegeven.
   * **[!UICONTROL Show related content]**. Schakel deze optie in om inhoud weer te geven die is gepubliceerd naar de app, maar die is gelabeld met een andere product-id. Nadat de productspecifieke inhoud voor de app wordt weergegeven, geeft LiveCyre inhoud weer voor andere producten en inhoud die niet aan een product is gekoppeld. Livefyre geeft eerst prioriteit aan de inhoud met dezelfde product-id en vervolgens aan inhoud die met andere product-id&#39;s naar de app is gepubliceerd, waarna inhoud die zonder product-id&#39;s naar de app is gepubliceerd.

