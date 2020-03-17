---
description: Wijzig de grootte, breedte en interactieopties van de Media Wall-app.
seo-description: Wijzig de grootte, breedte en interactieopties van de Media Wall-app.
seo-title: Aanpassingen aan de mediamuur
solution: Experience Manager
title: Aanpassingen aan de mediamuur
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aanpassingen aan de mediamuur{#media-wall-customizations}

Wijzig de grootte, breedte en interactieopties van de Media Wall-app.



Media Walls streamen live beelden en andere inhoud naar een sociale muur in real time, waardoor alle activiteit rondom een gebeurtenis zichtbaar wordt.

Als deze optie is ingeschakeld, kunnen gebruikers tekst, afbeeldingen of video rechtstreeks naar deze app posten. Tot de ondersteunde bestandstypen behoren:

* Afbeelding: JPEG, GIF, PNG
* Video: QuickTime/MOV, MP4, MPEG, WebM
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Hiermee stelt u het aanvankelijke aantal weergegeven inhoudsitems in.

* **[!UICONTROL Load content with animation.]** Schakel deze optie in om de mediamuur te laden op een pagina met animatie. Schakel deze optie uit om de mediamuur zonder animatie op een pagina te laden.
* **[!UICONTROL Number of columns.]** Stel het aantal kolommen in voor de mediamuur. Het aantal kolommen blijft gelijk, ongeacht de grootte van het venster of de browser. Als u Automatisch selecteert, wordt het aantal kolommen aangepast om een geoptimaliseerd aantal kolommen voor de schermgrootte weer te geven.
* **[!UICONTROL Fit content to width]**. Als deze optie is uitgeschakeld, wordt de inhoud uitgesneden tot een vierkant. Schakel deze optie in om een volledige afbeelding op de kaart weer te geven, of de hele kaart nu wordt gevuld of niet.
* **[!UICONTROL Include content modal]**

   Hiermee kunnen gebruikers op een foto in de stream klikken om deze te openen in een overlappend pop-upvenster.

* **[!UICONTROL Require rights]**. Schakel deze optie in om alleen inhoud weer te geven met de status &quot;Granted&quot; (Verleend verzoek om rechten).
* **[!UICONTROL Hide social branding when rights granted]** Schakel deze optie in om het logo voor het oorspronkelijke sociale-medianetwerk (Twitter of Instagram) te verwijderen wanneer rechten voor een stuk inhoud worden toegekend.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Selecteer of gebruikers tekst, foto of video mogen posten met de uploadknop.
   * **[!UICONTROL Require Media]**. Schakel deze optie in als u wilt dat gebruikers alleen foto- of video-inhoud hoeven te uploaden met de knop Uploaden.
   * U kunt de standaardtekst voor de volgende velden van de knop Uploaden bewerken:

      * **[!UICONTROL Upload Button Text]**. Tekst voor de knop Uploaden. De standaardtekst is &quot;Wat is er aan uw hoofd?&quot;
      * **[!UICONTROL Comment Modal Title]**. De titel voor de modale site die bezoekers gebruiken om inhoud te posten. De standaardtekst is &#39;&#39;Plaats uw opmerking&#39;&#39;.
      * **[!UICONTROL Comment Modal Button]**. De tekst van de knopsitebezoekers klikt om inhoud te posten. De standaardtekst is &#39;&#39;Plaats uw opmerking&#39;&#39;.

* **[!UICONTROL Call-to-action button]** U kunt de vraag-aan-actie knoop met een productcatalogus gebruiken om gebruikers aan een product of aan uw plaats voor verdere actie te leiden.

   * **[!UICONTROL Call-to-action button]** Schakelaar de knevel aan op om de vraag-aan-actie knoop te tonen.
   * **[!UICONTROL Require rights to display products]** Schakel de knevel aan op om te vereisen dat de inhoudseigenaar rechten voor de inhoud heeft verleend alvorens een vraag-aan-actie knoop voor de inhoud verschijnt.

      >[!NOTE]
      >
      >De inhoud toont zelfs als de rechten niet voor de inhoud worden verleend, maar de vraag-aan-actie knoop zal niet met de inhoud tonen tenzij de rechten voor de inhoud worden verleend.

   * **[!UICONTROL Call-to-action header text]** De woorden in de kopbal boven de vraag-aan-actie knoop in inhoud modaal te tonen. De standaardformulering is &quot;Deze producten kopen:&quot;.
   * **[!UICONTROL Call-to-action button text]** De woorden in de vraag-aan-actie knoop in de inhoud modaal te tonen. Standaardtekst is: &quot;Nu kopen:&quot;.
   * **[!UICONTROL Product display options]** Kies of u de Naam van de Foto en van het Product met de Vraag-aan-actie knoop wilt tonen.

      >[!NOTE]
      >
      >De knoppen Foto en Productnaam markeren blauw als ze zijn ingeschakeld.

   * **[!UICONTROL Product URL referral tracking]** Schakel de schakeloptie in om verwijzingen van deze app naar de bijbehorende productpagina bij te houden.
   * **[!UICONTROL Referral tracking key-value pairs]** Voeg parameters toe om verwijzing van uw inhoud van de App aan de bijbehorende productpagina verder te specificeren.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Selecteer deze optie om één app voor meerdere productpagina&#39;s te maken. Filter productspecifieke UGC voor elke productpagina naar de App. U kunt een of meer mappen selecteren om specifieke verzamelingen aan de app te koppelen.
   * **[!UICONTROL Select Product folders]**. Selecteer de productmappen op het hoogste niveau die u wilt gebruiken om UGC te filteren. Gebruik CTRL/Command + klik om meerdere mappen te selecteren. LiveCycle gebruikt de map om te bepalen welke producten in die map in de app op verschillende pagina&#39;s moeten worden weergegeven.
   * **[!UICONTROL Show related content]**. Schakel deze optie in om inhoud weer te geven die is gepubliceerd naar de app, maar die is gelabeld met een andere product-id. Nadat de productspecifieke inhoud voor de app wordt weergegeven, geeft LiveCyre inhoud weer voor andere producten en inhoud die niet aan een product is gekoppeld. Livefyre geeft eerst prioriteit aan de inhoud met dezelfde product-id en vervolgens aan inhoud die met andere product-id&#39;s naar de app is gepubliceerd, waarna inhoud die zonder product-id&#39;s naar de app is gepubliceerd.

U kunt de Muur van Media aanpassen gebruikend:

* **[!UICONTROL Style]** en **[!UICONTROL Config]** opties voor alle toepassingen in de **[!UICONTROL App Designer]** toepassing. Zie Apps aanpassen voor meer informatie over de standaard **[!UICONTROL Style]** en **[!UICONTROL Config]** opties voor alle apps in de **[!UICONTROL App Designer]**.

* Integratiegereedschappen. Zie de Integratie [van de Muur van](/help/implementation/c-app-integrations/c-media-wall-integration.md) Media voor meer op hoe te om een Muur van Media aan te passen gebruikend de Hulpmiddelen van de Integratie.

