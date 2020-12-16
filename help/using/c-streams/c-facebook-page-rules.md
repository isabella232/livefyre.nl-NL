---
description: U kunt stroomregels maken die inhoud ophalen van Facebook-pagina's.
seo-description: U kunt stroomregels maken die inhoud ophalen van Facebook-pagina's.
seo-title: Regels voor Facebook-pagina
solution: Experience Manager
title: Regels voor Facebook-pagina
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# Facebook Page Rules{#facebook-page-rules}

U kunt stroomregels maken die inhoud ophalen van Facebook-pagina&#39;s.

U kunt Facebook-paginalijnen gebruiken om openbaar geposte inhoud te streamen vanaf Facebook-pagina&#39;s. De inhoud wordt met dezelfde frequentie als SocialSync in de app of map geplaatst, die wordt gewijzigd op basis van Facebook-pagina- en postverkeerspatronen. Koppelingen in Facebook-pagina&#39;s worden ook ondersteund en worden weergegeven in de stream.

Als u Facebook-paginalijnen wilt maken om inhoud van Facebook-pagina&#39;s in uw app of map te plaatsen, kunt u filteren op:

* **[!UICONTROL Facebook Page]**

   * Voer de **[!UICONTROL Name]** voor de pagina in. Voer alleen de navolgende tekst voor de URL in. **Bijvoorbeeld:** om inhoud van toe te voegen  `https://facebook.com/KellysSuperFunFanPage`, typ  ** KellysSuperFunFanPage in het  **[!UICONTROL Name]** gebied.

   * Schakel **[!UICONTROL Include Facebook Comments for each post]** in als u opmerkingen van gebruikers wilt opnemen in paginaposten.
   * Schakel **[!UICONTROL Only Show Author Posts]** in als u advertenties van andere gebruikers wilt uitsluiten.

Voor extra de regelopties van de Stroom voor alle regels van de Stroom, zie [de Opties van de Regel van de Stroom voor Alle Regels van de Stroom](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre is beperkt tot inhoud die van Facebook is ontvangen en kan daarom niet garanderen dat elke post op een Facebook-pagina in uw stream wordt opgenomen.

>[!NOTE]
>
>Als Facebook SocialSync en een Facebook Page Rule beide zijn ingeschakeld voor een specifieke Facebook-pagina en gebruikerscommentaren zijn ingeschakeld voor de Facebook-paginalijn, wordt de Stream Rule gebruikt voor het overschrijven van SocialSync. Inhoud wordt alleen gestreamd naar de app op basis van de Facebook Page Curate Rule en niet met behulp van SocialSync.

De volgende typen inhoud worden ondersteund door Facebook Page Curate:

* Eigenaar of beheerder van pagina

   * Status
   * Foto&#39;s
   * Video&#39;s als koppelingen

* Standaardgebruiker van Facebook

   * Status
   * Foto&#39;s
   * Video&#39;s als koppelingen

* Derde partijen

   * Status

