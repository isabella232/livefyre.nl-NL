---
description: U kunt stroomregels maken die inhoud ophalen uit Instagram.
seo-description: U kunt stroomregels maken die inhoud ophalen uit Instagram.
seo-title: Installatieregels
title: Installatieregels
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Installatieregels{#instagram-rules}

U kunt stroomregels maken die inhoud ophalen uit Instagram.

>[!NOTE]
>
>Voordat u een Instagram-stream maakt, moet u ten minste één Instagram-bedrijfsaccount aan de **[!UICONTROL Social Accounts]** sectie in toevoegen **[!UICONTROL Network Settings]**. Zie [Informatie over Instagram-accounts](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)voor meer informatie over het configureren van een Instagram-account.

Instagramregels maken op basis van @mtifications of hashtag.

>[!NOTE]
>
>Voor alle Instagram-regels is minstens één hashtag vereist. Wanneer u trefwoorden en een gebruikersnaam voor de regel toevoegt, wordt inhoud met beide vermeldingen geretourneerd.

Als u Instagram-regels wilt maken om inhoud van Instagram-feeds naar uw app of map te halen, filtert u op:

* **[!UICONTROL Words]**

   * Voer **[!UICONTROL hashtags]** in om te worden opgenomen in of uitgesloten van uw Instagram-stream. Als u waarden opgeeft voor zowel het veld **[!UICONTROL Contains]** als het **[!UICONTROL Does not contain]** veld, worden afbeeldingen geretourneerd die het eerste bevatten en niet het tweede.

   * Als u bijvoorbeeld trefwoorden Giants, Posey en **[!UICONTROL Contains]** **[!UICONTROL Does not contain]** trefwoord Dodger invoert, worden alle berichten geretourneerd die het woord Giants of Posey bevatten, maar niet het woord Dodger.

      >[!NOTE]
      >
      >Instagram Rules retourneert berichten die de vermelde hashtag in de opmerkingen van de auteur bevatten en die mogelijk niet in de stream worden weergegeven.

* **[!UICONTROL Mentions]**

   * Voer in **[!UICONTROL @mentions]** om in de stream te gaan of om de stream uit te sluiten.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Als u de zoekopdracht Auteur in een Instagram-stroomregel wilt gebruiken, moet er een zakelijke account in LiveCycle zijn ingesteld. Zie [Informatie over Instagram-accounts](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)voor meer informatie over het instellen van Instagram-bedrijfsaccounts in LiveCycle.

   * Voer in **[!UICONTROL @usernames]** om in de stroom te trekken. De account die aan de **@gebruikersnaam** is gekoppeld, moet een zakelijke account in Instagram zijn.

   * Voer de **@gebruikersnamen** in die u van de stream wilt uitsluiten.

* **[!UICONTROL Additional Filters]**

   * Selecteer of u **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]****[!UICONTROL Photos Only]** of in uw stroom wilt omvatten.

Zie Opties [stroomregel voor alle stroomregels](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)voor aanvullende stroomregelopties voor alle stroomregels.
