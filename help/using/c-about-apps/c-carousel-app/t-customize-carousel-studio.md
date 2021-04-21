---
description: Wijzig de grootte, breedte en interactieopties van de Carousel-app.
title: Een carrousel aanpassen met Studio
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Een carrousel aanpassen met Studio{#customize-a-carousel-using-studio}

Wijzig de grootte, breedte en interactieopties van de Carousel-app.

Alle toepassingen gebruiken **[!UICONTROL Style]** en **[!UICONTROL Config]** opties in **[!UICONTROL App Designer]**. Zie Apps aanpassen voor meer informatie over de standaard **[!UICONTROL Style]**- en **[!UICONTROL Config]**-opties voor alle apps in **[!UICONTROL App Designer]**.

U kunt een carrousel aanpassen met behulp van de volgende aanvullende opties in App Designer:

* **[!UICONTROL Max Number of Items]**

   Hiermee stelt u het aantal items in dat in de carrousel moet worden weergegeven. De standaardwaarde is 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Alleen voor computerschermen

   * Als de inhoud groter is dan 600 pixels, wordt deze horizontaal weergegeven
   * Als de inhoud kleiner is dan 600 pixels, wordt deze verticaal weergegeven
   * **Verticaal.** Voor computerschermen of mobiele apparaten. Op mobiele apparaten wordt de kaart verkleind zodat deze op het scherm past.

* **[!UICONTROL Call-to-action button]** U kunt de vraag-aan-actie knoop met een productcatalogus gebruiken om gebruikers aan een product of aan uw plaats voor verdere actie te leiden.

   * **[!UICONTROL Call-to-action button]** Schakelaar de knevel aan op om de vraag-aan-actie knoop te tonen.
   * **[!UICONTROL Require rights to display products]** Schakel de schakeloptie in om te vereisen dat de eigenaar van de inhoud rechten voor de inhoud heeft verleend voordat een knop Aanroepen verschijnt voor de inhoud.

   >[!NOTE]
   >
   >De inhoud wordt ook weergegeven als er geen rechten zijn verleend voor de inhoud, maar de knop call-to-action wordt alleen weergegeven met de inhoud als er rechten voor de inhoud zijn verleend.

   * **[!UICONTROL Show call-to-action in tile]**. Kies of om vraag-aan-actie knoop op een tegel in plaats van het tonen van vraag-aan-actie knoop slechts te tonen wanneer de bezoeker van de plaats op een kaart klikt en de inhoud in een groter venster opent.
   * **[!UICONTROL Call-to-action indication text]** De tekst aan vertoning om de gebruiker ertoe aan te zetten om op de kaart te klikken om vraag-aan-actie modaal te openen.
   * **[!UICONTROL Call-to-action header text]** De woorden in de kopbal boven de vraag-aan-actie knoop in inhoud modaal te tonen. De standaardtekst is &quot;Deze producten kopen:&quot;.
   * **[!UICONTROL Call-to-action button text]** De woorden in de vraag-aan-actie knoop in de inhoud modaal te tonen. Standaardtekst is: &quot;Nu kopen:&quot;.
   * **[!UICONTROL Product display options]** Kies of u de vraag  **[!UICONTROL Photo]** en  **[!UICONTROL Product name]** met de vraag-aan-actie knoop wilt tonen.

   >[!NOTE]
   >
   >De knoppen Foto en Productnaam markeren blauw als ze zijn ingeschakeld.

   * **[!UICONTROL Product URL referral tracking]** Schakel de schakeloptie in om verwijzingen van deze app naar de bijbehorende productpagina bij te houden.
   * **[!UICONTROL Referral tracking key-value pairs]** Voeg parameters toe om verwijzing van uw inhoud van de App aan de bijbehorende productpagina verder te specificeren.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecteer deze optie om één app voor meerdere productpagina&#39;s te maken. Filter productspecifieke UGC voor elke productpagina naar de App. U kunt een of meer mappen selecteren om specifieke verzamelingen aan de app te koppelen.
   * **[!UICONTROL Select Product folders]**. Selecteer de productmappen op het hoogste niveau die u wilt gebruiken om UGC te filteren. Gebruik CTRL/Command + klik om meerdere mappen te selecteren. LiveCycle gebruikt de map om te bepalen welke producten in die map in de app op verschillende pagina&#39;s moeten worden weergegeven.
   * **[!UICONTROL Show related content]**. Schakel deze optie in om inhoud weer te geven die is gepubliceerd naar de app, maar die is gelabeld met een andere product-id. Nadat de productspecifieke inhoud voor de app wordt weergegeven, geeft LiveCyre inhoud weer voor andere producten en inhoud die niet aan een product is gekoppeld. Livefyre geeft eerst prioriteit aan de inhoud met dezelfde product-id en vervolgens aan inhoud die met andere product-id&#39;s naar de app is gepubliceerd, waarna inhoud die zonder product-id&#39;s naar de app is gepubliceerd.
