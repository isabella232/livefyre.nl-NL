---
description: U kunt stroomregels maken die inhoud ophalen van Facebook-pagina's.
seo-description: U kunt stroomregels maken die inhoud ophalen van Facebook-pagina's.
seo-title: Regels voor Facebook-pagina
solution: Experience Manager
title: Regels voor Facebook-pagina
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regels voor Facebook-pagina{#facebook-page-rules}

U kunt stroomregels maken die inhoud ophalen van Facebook-pagina&#39;s.

U kunt Facebook-paginalijnen gebruiken om openbaar geposte inhoud te streamen vanaf Facebook-pagina&#39;s. De inhoud wordt met dezelfde frequentie als SocialSync in de app of map geplaatst, die wordt gewijzigd op basis van Facebook-pagina- en postverkeerspatronen. Koppelingen in Facebook-pagina&#39;s worden ook ondersteund en worden weergegeven in de stream.

Als u Facebook-paginalijnen wilt maken om inhoud van Facebook-pagina&#39;s in uw app of map te plaatsen, kunt u filteren op:

* **[!UICONTROL Facebook Page]**

   * Voer de naam **[!UICONTROL Name]** voor de pagina in. Voer alleen de navolgende tekst voor de URL in. **Bijvoorbeeld:** Als u inhoud wilt toevoegen van `https://facebook.com/KellysSuperFunFanPage`, typt u *KellysSuperFunPage* in het **[!UICONTROL Name]** veld.

   * Schakel deze optie **[!UICONTROL Include Facebook Comments for each post]** in als u gebruikersopmerkingen wilt opnemen in paginarubrieken.
   * Schakel deze optie **[!UICONTROL Only Show Author Posts]** in als u berichten van andere gebruikers wilt uitsluiten.

Zie Opties [stroomregel voor alle stroomregels](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)voor aanvullende stroomregelopties voor alle stroomregels.

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

