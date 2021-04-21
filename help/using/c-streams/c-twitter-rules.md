---
description: U kunt stroomregels maken die inhoud uit Twitter ophalen.
title: Twitter-regels
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Twitter Rules{#twitter-rules}

U kunt stroomregels maken die inhoud uit Twitter ophalen.

Maak Twitter-regels op basis van hashtags, trefwoorden, @mnotifications of auteur.

Als u **[!UICONTROL Words]** en **[!UICONTROL Username]** voor uw regel toevoegt, wordt inhoud geretourneerd die beide items bevat.

>[!NOTE]
>
>Livefyre volgt de Twitter-weergaverichtlijnen en klanten zijn ook verantwoordelijk voor het naleven van deze richtlijnen. Raadpleeg de documentatie bij Twitter op de [Weergavevereisten](https://dev.twitter.com/terms/display-requirements) voor meer informatie.

Als u Twitter Rules wilt maken om inhoud van Twitter-feeds naar uw app of map te halen, kunt u filteren op:

* **[!UICONTROL Keywords]**
   * Voer **[!UICONTROL Keywords]** in om te worden opgenomen in of uitgesloten van uw Twitter-stream. Als u waarden opgeeft voor zowel de velden **[!UICONTROL Contains any of these words]** als **[!UICONTROL Does not contain any of these words]**, worden tweets geretourneerd die de eerste bevatten en die de tweede niet bevatten. Er kunnen meerdere waarden voor één veld worden ingevoerd en dit levert resultaten op die een van de waarden bevatten. Als u de Booleaanse operator AND wilt gebruiken om te zoeken naar tweets met twee of meer woorden in de tweets, gebruikt u twee ampersanden (*&amp;&amp;*) om de twee woorden van elkaar te scheiden.
   * Als u bijvoorbeeld het trefwoord **[!UICONTROL Contains any of these words]** Giants, Posey en **[!UICONTROL Does not contain any of these words]** Dodger invoert, worden alle tweets geretourneerd die het woord *Giants* of *Posey* bevatten en niet het woord *Dodger*.
Als u wilt zoeken naar tweets die zowel de woorden *Giants* als *Posey* bevatten, voert u &quot;Giants &amp;&amp; Posey&quot; in. Deze functie wordt alleen ondersteund voor de velden **[!UICONTROL Contains any of these words]** en **[!UICONTROL Does not contain any of these words]** in Twitter-regels.

* **[!UICONTROL Hashtags]**.
   * Voer **[!UICONTROL Hashtags]** in om te worden opgenomen in of uitgesloten van uw Twitter-stream. Als u waarden opgeeft voor zowel de velden **[!UICONTROL Contains any of these words]** als **[!UICONTROL Does not contain any of these words]**, worden tweets geretourneerd die hashtags bevatten in het eerste veld en die geen hashtags bevatten in het tweede veld. U kunt meerdere waarden invoeren voor één veld. De stream retourneert resultaten die een van de waarden bevatten.

* **[!UICONTROL Usernames]**
   * Typ **[!UICONTROL @mentions]** of **[!UICONTROL authors]** om in de stream te gaan of sluit deze uit van de stream. Gebruik de selectievakjes om te definiëren of **[!UICONTROL Retweets]** of **[!UICONTROL replies]** van geselecteerde auteurs ook moet worden opgenomen.

   >[!NOTE]
   >
   >U kunt auteurs opnemen of uitsluiten. U kunt deze twee velden niet combineren tot één Twitter-regel.

* **[!UICONTROL Minimum number of followers.]** Selecteer het minimum aantal volgers dat de gebruiker nodig heeft om informatie van zijn berichten te halen.
* **[!UICONTROL Location]**

   * Voer de locatie in (plaats, postcode, adres of geocode in de algemene notatie Breedtegraad/lengtegraad (+/- 90, +/- 180) ). Typ een locatie voor een vervolgkeuzelijst met suggesties. Selecteer een locatie in het keuzemenu. Op de kaart wordt een punt van die locatie weergegeven. Pas de schuifregelaar aan om een straal van 1 tot 25 mijl voor elke locatie te selecteren. Als u geen straal kiest, kiest Livefyre automatisch een gebrek van acht mijl.
   >[!NOTE]
   >
   >Voor beide velden wordt de afstand berekend vanaf het midden van de invoerlocatie.

   * U kunt meerdere locaties en straal toevoegen. U kunt een locatie verwijderen door op de X naast de naam van een locatie in het vak te klikken.
   * Combineer de velden **[!UICONTROL Is near this location]** en **[!UICONTROL Is not near this location]** om inhoud te trekken binnen locaties in het veld **[!UICONTROL Is near this location]**, maar niet dichtbij de locaties in het veld **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Gebruik extra filters om de Twitter-regel verder te verfijnen. Bepaal of u:
      * Neem **[!UICONTROL Replies]** op bij de beoogde tweets (als de stream hoge snelheid krijgt, wordt deze functie automatisch uitgeschakeld.)
      * Tweets opnemen van **[!UICONTROL Verified Twitter accounts only.]**
      * Inclusief **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]** of **[!UICONTROL Images Only.]**
      * Neem alleen Tweets op die afkomstig zijn van accounts met de geselecteerde **[!UICONTROL Minimum number of followers]** (alle, 100, 500, 1000, 10.000 of 100.000).

Voor extra de regelopties van de Stroom voor alle regels van de Stroom, zie [de Opties van de Regel van de Stroom voor Alle Regels van de Stroom](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
