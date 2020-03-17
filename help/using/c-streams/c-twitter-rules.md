---
description: U kunt stroomregels maken waarmee inhoud van Twitter wordt opgehaald.
seo-description: U kunt stroomregels maken waarmee inhoud van Twitter wordt opgehaald.
seo-title: Twitter-regels
solution: Experience Manager
title: Twitter-regels
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter-regels{#twitter-rules}

U kunt stroomregels maken waarmee inhoud van Twitter wordt opgehaald.

Maak Twitter-regels op basis van hashtags, trefwoorden, @mtifications of auteur.

Door inhoud toe te voegen **[!UICONTROL Words]** en een **[!UICONTROL Username]** waarde voor uw regel toe te voegen, worden beide items ingesloten.

>[!NOTE]
>
>Livefyre houdt zich aan de Twitter-weergaverichtlijnen en klanten zijn ook verantwoordelijk voor het naleven van deze richtlijnen. Raadpleeg de documentatie bij Twitter over hun [weergavevereisten](https://dev.twitter.com/terms/display-requirements)voor meer informatie.

Als u Twitter-regels wilt maken om inhoud van Twitter-feeds naar uw app of map te halen, kunt u filteren op:

* **[!UICONTROL Keywords]**
   * Voer **[!UICONTROL Keywords]** in om te worden opgenomen in of uitgesloten van uw Twitter-stream. Als u waarden opgeeft voor zowel het veld **[!UICONTROL Contains any of these words]** als het **[!UICONTROL Does not contain any of these words]** veld, worden tweets geretourneerd die het eerste bevatten en niet het tweede. Er kunnen meerdere waarden voor één veld worden ingevoerd en dit levert resultaten op die een van de waarden bevatten. Als u de Booleaanse operator AND wilt gebruiken om te zoeken naar tweets met twee of meer woorden in de tweets, gebruikt u twee ampersands (*&amp;&amp;*) om de twee woorden van elkaar te scheiden.
   * Als u bijvoorbeeld trefwoorden Giants, Posey en **[!UICONTROL Contains any of these words]** trefwoord Dodger invoert, worden alle tweets geretourneerd die het woord **[!UICONTROL Does not contain any of these words]** Giants *of* Posey *bevatten en niet het woord* Dodger **.
Als u wilt zoeken naar tweets die zowel de woorden *Giants* als *Posey* bevatten, voert u &quot;Giants &amp;&amp; Posey&quot; in. Deze functie wordt alleen ondersteund voor de **[!UICONTROL Contains any of these words]** **[!UICONTROL Does not contain any of these words]** velden en de velden in Twitter-regels.

* **[!UICONTROL Hashtags]**.
   * Voer **[!UICONTROL Hashtags]** in om te worden opgenomen in of uitgesloten van uw Twitter-stream. Als u waarden opgeeft voor zowel het veld **[!UICONTROL Contains any of these words]** als het **[!UICONTROL Does not contain any of these words]** veld, worden tweets geretourneerd die hashtags bevatten in het eerste veld en die geen hashtags bevatten in het tweede veld. U kunt meerdere waarden invoeren voor één veld. De stream retourneert resultaten die een van de waarden bevatten.

* **[!UICONTROL Usernames]**
   * Voer in **[!UICONTROL @mentions]** of **[!UICONTROL authors]** om in de stream te gaan of sluit het uit van de stream. Gebruik de selectievakjes om te bepalen of **[!UICONTROL Retweets]** of **[!UICONTROL replies]** van geselecteerde auteurs ook moet worden opgenomen.
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
   * Combineer de velden **[!UICONTROL Is near this location]** en **[!UICONTROL Is not near this location]** velden om inhoud te trekken binnen locaties in het **[!UICONTROL Is near this location]** veld, maar niet dichtbij de locaties in het **[!UICONTROL Is not near this location]** veld.


* **[!UICONTROL Additional Filters]**
   * Gebruik extra filters om uw Twitter-regel verder te verfijnen. Bepaal of u:
      * Opnemen **[!UICONTROL Replies]** in de beoogde tweets (als de stream een hoge snelheid krijgt, wordt deze functie automatisch uitgeschakeld.)
      * Tweeten opnemen van **[!UICONTROL Verified Twitter accounts only.]**
      * Inclusief **[!UICONTROL All Content]**, of **[!UICONTROL Vines Only]**, of **[!UICONTROL Images Only.]**
      * Neem alleen Tweets op die afkomstig zijn van accounts met de geselecteerde **[!UICONTROL Minimum number of followers]** (elke, 100, 500, 1000, 10.000 of 100.000).

Zie Opties [stroomregel voor alle stroomregels](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)voor aanvullende stroomregelopties voor alle stroomregels.
