---
description: Deze opties zijn van toepassing op stroomregels van alle sociale netwerken of postingsmethoden.
seo-description: Deze opties zijn van toepassing op stroomregels van alle sociale netwerken of postingsmethoden.
seo-title: Opties voor stroomregel voor alle stroomregels
solution: Experience Manager
title: Opties voor stroomregel voor alle stroomregels
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# De Opties van de Regel van de stroom voor Alle Regels van de Stroom{#stream-rule-options-for-all-stream-rules}

Deze opties zijn van toepassing op stroomregels van alle sociale netwerken of postingsmethoden.

Functies zoeken voor tekst en trefwoordvelden:

* Wanneer u trefwoorden invoert, gebruikt LiveCycle automatisch de Booleaanse operator **OR** wanneer voor afzonderlijke woorden. Als u bijvoorbeeld artikelen wilt zoeken met het woord *cake* of *recipe*, voert u *cake* in en *recipe* in het veld **[!UICONTROL keyword]**.

* U kunt zoeken naar exacte woordgroepen door de exacte woordtekst tussen aanhalingstekens te plaatsen. Als u bijvoorbeeld naar de exacte uitdrukking *cake recipe* wilt zoeken, voert u *&quot;cake recipe&quot;* in het veld **[!UICONTROL keyword]** in.

* U kunt de zoekopdrachten voor Booleaanse en exacte woordgroepen combineren in één streamregel. U kunt bijvoorbeeld zoeken naar *cake*, *recept* en *&quot;koekjesrecept&quot;* door elke uitdrukking één voor één in te voeren.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selecteer een van de volgende opties:

   * **[!UICONTROL All Content.]** Inhoud toestaan.
   * **[!UICONTROL Media Required.]** Alleen inhoud met afbeeldingen en video&#39;s toestaan. (Voor Instagram- en Facebook-inhoud kunt u alleen **[!UICONTROL Photos]** of **[!UICONTROL Videos]** opgeven).

* **[!UICONTROL Language]**. Kies de taal waarin u wilt zoeken. Engels is de standaardtaal.
* **[!UICONTROL Smart Tags]**. Kies de tags die u wilt gebruiken om de inhoud te identificeren. LiveCycle gebruikt computergezichtstechnologie om foto&#39;s en video&#39;s met specifieke slimme tags te identificeren en deze zoekopdracht preciezer te maken. Gebruik de **[!UICONTROL ANY]** bepaling om inhoud in de stroom te filtreren gebruikend om het even welke markering of **[!UICONTROL ALL]** bepaling om inhoud in de stroom te filtreren die alle markeringen gebruikt. Gebruik het veld **[!UICONTROL Image contains none of these smart tags]** om tags in te voeren voor foto&#39;s met inhoud die u niet in de stream wilt opnemen. Deze optie werkt niet voor tekstinhoud.

* **[!UICONTROL Products]**. Voeg productcodes toe die overeenkomen met de streaming regel met producten uit uw productcatalogus.
* **[!UICONTROL Premoderate]**. Selecteer een van de volgende opties:

   * **[!UICONTROL On]**. Alle binnenkomende regelinhoud voorbehouden. U kunt vooraf gemodereerde inhoud van de sectie van Streams van ModQ bekijken. **[!UICONTROL On]** Hiermee overschrijft u de instellingen in App Settings.
   * **[!UICONTROL Off]**. Voormatig geen binnenkomende regelinhoud. **[!UICONTROL Off]** Hiermee overschrijft u de instellingen in App Settings.
   * **[!UICONTROL Inherited (Off)]**. Gebruik de vooraf gemiddelde instellingen van de site (onder **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selecteer een van de volgende opties:
   * **[!UICONTROL Apply SAFE Rules]**. Pas alle SAFE-regels toe op deze stream.
   * **[!UICONTROL Apply SAFE Rules for:]** Selecteer een of meer opties om VEILIGE regels toe te passen op deze streamregel.
   * **[!UICONTROL Disable SAFE Rules]**. Pas geen VEILIGE Regels op deze stroom toe.

Zie de volgende documentatie voor het respectievelijke sociale netwerk of inhoudssoort voor opties voor de stroomregel die specifiek zijn voor een sociaal netwerk of inhoudssoort:

* [Facebook-pagina&#39;s](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-mail](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
