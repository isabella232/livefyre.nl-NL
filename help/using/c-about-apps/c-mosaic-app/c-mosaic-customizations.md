---
description: Wijzig de grootte, breedte en interactieopties van de mozaïek-app.
seo-description: Wijzig de grootte, breedte en interactieopties van de mozaïek-app.
seo-title: Mozaïekaanpassingen
solution: Experience Manager
title: Mozaïekaanpassingen
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mozaïekaanpassingen{#mosaic-customizations}

Wijzig de grootte, breedte en interactieopties van de mozaïek-app.

Alle toepassingen gebruiken **[!UICONTROL Style]** en **[!UICONTROL Config]** opties in de **[!UICONTROL App Designer]**. Zie Apps aanpassen voor meer informatie over de standaard **[!UICONTROL Style]** en **[!UICONTROL Config]** opties voor alle apps in het dialoogvenster **[!UICONTROL App Designer.]**

U kunt Mozaïek aanpassen met de volgende aanvullende opties in App Designer:

* **[!UICONTROL Content interaction]**. Hiermee stelt u de stijl in waarmee nieuwe inhoud op de pagina wordt geladen:

   * **[!UICONTROL Hover Fade]** om naar de andere kant van een kaart te vervagen wanneer een bezoeker van de site de muis boven de inhoud houdt.
   * **[!UICONTROL Hover Flip]** om naar de andere kant van een kaart te draaien wanneer een bezoeker van de site de muis boven de inhoud houdt.
   * **[!UICONTROL Click]** om de andere zijde van een kaart weer te geven wanneer een bezoeker van de site met de muis op de inhoud klikt.

* **[!UICONTROL Number of Tiles to Load]**. Het aantal tegels dat in een mozaïek moet worden geladen. Dit kan van invloed zijn op de uitvoerweergave. Mozaïek wordt alleen weergegeven in een raster als u het juiste aantal tegels kiest dat overeenkomt met de containerbreedte. Mogelijk moet u deze instellingen aanpassen om het raster correct weer te geven.
* **[!UICONTROL Hide social branding when rights granted]** Schakel deze optie in om het logo voor het oorspronkelijke sociale-medianetwerk (Twitter of Instagram) te verwijderen wanneer rechten voor een stuk inhoud worden toegekend.

* **[!UICONTROL Call-to-action button]** U kunt de vraag-aan-actie knoop met een productcatalogus gebruiken om gebruikers aan een product of aan uw plaats voor verdere actie te leiden.

   * **[!UICONTROL Call-to-action button]** Schakelaar de knevel aan op om de vraag-aan-actie knoop te tonen.

   * **[!UICONTROL Require rights to display products]** Schakel de knevel aan op om te vereisen dat de inhoudseigenaar rechten voor de inhoud heeft verleend alvorens een vraag-aan-actie knoop voor de inhoud verschijnt.

      >[!NOTE]
      >
      >De inhoud toont zelfs als de rechten niet voor de inhoud worden verleend, maar de vraag-aan-actie knoop zal niet met de inhoud tonen tenzij de rechten voor de inhoud worden verleend.

   * **[!UICONTROL Show call-to-action in tile]**. Kies of om vraag-aan-actie knoop op een tegel van de Filmstrook in plaats van het tonen van vraag-aan-actie slechts te tonen wanneer de bezoeker van de plaats op een kaart klikt en de inhoud in een groter venster opent.
   * **[!UICONTROL Call-to-action indication text]** De tekst aan vertoning om de gebruiker ertoe aan te zetten om op de kaart te klikken om vraag-aan-actie modaal te openen.

   * **[!UICONTROL Call-to-action header text]** De woorden in de kopbal boven de vraag-aan-actie knoop in inhoud modaal te tonen. De standaardformulering is &quot;Deze producten kopen:&quot;.

   * **[!UICONTROL Call-to-action button text]** Pas de tekst op de vraag-aan-actie knoop aan. De standaardtekst is &#39;&#39;Nu kopen&#39;&#39;.

   * **[!UICONTROL Product display options]** Kies of u de **[!UICONTROL Photo]** en **[!UICONTROL Product name]** met de vraag-aan-actie knoop wilt tonen.

   * **[!UICONTROL Product URL referral tracking]** Schakel de schakeloptie in om verwijzingen van deze app naar de bijbehorende productpagina bij te houden.

   * **[!UICONTROL Referral tracking key-value pairs]** Voeg parameters toe om verwijzing van uw inhoud van de App aan de bijbehorende productpagina verder te specificeren.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selecteer deze optie om één app voor meerdere productpagina&#39;s te maken. Filter productspecifieke UGC voor elke productpagina naar de App. U kunt een of meer mappen selecteren om specifieke verzamelingen aan de app te koppelen.
   * **[!UICONTROL Select Product folders]**. Selecteer de productmappen op het hoogste niveau die u wilt gebruiken om UGC te filteren. Gebruik CTRL/Command + klik om meerdere mappen te selecteren. LiveCycle gebruikt de map om te bepalen welke producten in die map in de app op verschillende pagina&#39;s moeten worden weergegeven.
   * **[!UICONTROL Show related content]**. Schakel deze optie in om inhoud weer te geven die is gepubliceerd naar de app, maar die is gelabeld met een andere product-id. Nadat de productspecifieke inhoud voor de app wordt weergegeven, geeft LiveCyre inhoud weer voor andere producten en inhoud die niet aan een product is gekoppeld. Livefyre geeft eerst prioriteit aan de inhoud met dezelfde product-id en vervolgens aan inhoud die met andere product-id&#39;s naar de app is gepubliceerd, waarna inhoud die zonder product-id&#39;s naar de app is gepubliceerd.

Zie [Mozaïekopties](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) voor meer informatie over het aanpassen van een mozaïek met Livefyre.js.
