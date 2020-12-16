---
description: U kunt stroomregels maken die inhoud ophalen uit Tumblr.
seo-description: U kunt stroomregels maken die inhoud ophalen uit Tumblr.
seo-title: Tumblr-regels
solution: Experience Manager
title: Tumblr-regels
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Tumblr Rules{#tumblr-rules}

U kunt stroomregels maken die inhoud ophalen uit Tumblr.

Maak Tumblr-regels op basis van een Tumblr-blog en gefilterd op tag. Tumblr-streams worden elke 5 minuten bijgewerkt en zoeken naar inhoud die nog niet bestaat in LiveCycle uit de eerste 20 items in de feed. Livefyre negeert alles voorbij de eerste 20 voorwerpen in het voer.

Als u Tumblr-regels wilt maken om inhoud van Tumblr aan uw app of map te koppelen, kunt u filteren op:

* **[!UICONTROL Blog]**

   * Voer de **[!UICONTROL Blog Name]** voor de Tumblr-blog in. Voer de URL (*staff.tumblr.com*) of de naam van de blog (*staff*) in.

   * Neem maximaal één **[!UICONTROL Tag]** op om resultaten te filteren op posten inclusief een bepaalde tag.

* **[!UICONTROL Include recent items.]** Als deze is ingesteld op:

   * **[!UICONTROL Enabled]**, voegt Livefyre de eerste 20 inhoudselementen in uw voer aan de stroom toe, ongeacht de publicatiedatum.
   * **[!UICONTROL Disabled]**, voegt Livefyre de eerste 20 inhoudselementen in uw voer aan de stroom met een publicatiedatum toe die het zelfde als de de aanmaakdatum van de stroomregel of later is.

Voor extra de regelopties van de Stroom voor alle regels van de Stroom, zie [de Opties van de Regel van de Stroom voor Alle Regels van de Stroom](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
