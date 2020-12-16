---
description: U kunt stroomregels maken die inhoud ophalen uit Instagram.
seo-description: U kunt stroomregels maken die inhoud ophalen uit Instagram.
seo-title: Installatieregels
title: Installatieregels
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Installatieregels{#instagram-rules}

U kunt stroomregels maken die inhoud ophalen uit Instagram.

>[!NOTE]
>
>Voordat u een Instagram-stream maakt, moet u ten minste één Instagram-bedrijfsaccount toevoegen aan de sectie **[!UICONTROL Social Accounts]** in **[!UICONTROL Network Settings]**. Zie [Informatie over Instagram-accounts](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts) voor meer informatie over het configureren van een Instagram-account.

Instagramregels maken op basis van @mtifications of hashtag.

>[!NOTE]
>
>Voor alle Instagram-regels is minstens één hashtag vereist. Wanneer u trefwoorden en een gebruikersnaam voor de regel toevoegt, wordt inhoud met beide vermeldingen geretourneerd.

Als u Instagram-regels wilt maken om inhoud van Instagram-feeds naar uw app of map te halen, filtert u op:

* **[!UICONTROL Words]**

   * Voer **[!UICONTROL hashtags]** in om te worden opgenomen in of uitgesloten van uw Instagram-stream. Als u waarden opgeeft voor zowel de velden **[!UICONTROL Contains]** als **[!UICONTROL Does not contain]**, worden afbeeldingen geretourneerd die de eerste bevatten en die de tweede niet bevatten.

   * Als u bijvoorbeeld **[!UICONTROL Contains]** trefwoorden Giants, Posey en **[!UICONTROL Does not contain]** trefwoord Dodger invoert, worden alle berichten geretourneerd die het woord Giants of Posey bevatten, maar niet het woord Dodger.

      >[!NOTE]
      >
      >Instagram Rules retourneert berichten die de vermelde hashtag in de opmerkingen van de auteur bevatten en die mogelijk niet in de stream worden weergegeven.

* **[!UICONTROL Mentions]**

   * Voer **[!UICONTROL @mentions]** in om in de stream te gaan, of sluit deze uit van de stream.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Als u de zoekopdracht Auteur in een Instagram-stroomregel wilt gebruiken, moet er een zakelijke account in LiveCycle zijn ingesteld. Zie [Informatie over Instagram-accounts](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts) voor meer informatie over het instellen van Instagram-bedrijfsaccounts in LiveCycle.

   * Voer **[!UICONTROL @usernames]** in om in de stream te gaan. De account die is gekoppeld aan de **@gebruikersnaam** moet een zakelijke account in het installatieprogramma zijn.

   * Voer **@usernames** in om uit te sluiten van de stream.

* **[!UICONTROL Additional Filters]**

   * Selecteer of u **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]**, of **[!UICONTROL Photos Only]** in uw stroom wilt omvatten.

Voor extra de regelopties van de Stroom voor alle regels van de Stroom, zie [de Opties van de Regel van de Stroom voor Alle Regels van de Stroom](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
