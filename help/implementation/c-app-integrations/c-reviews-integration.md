---
description: Klanten toestaan uw productaanbod te beoordelen en beoordelen.
seo-description: Klanten toestaan uw productaanbod te beoordelen en beoordelen.
seo-title: Revisies
solution: Experience Manager
title: Revisies
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# Revisies {#reviews}

Klanten toestaan uw productaanbod te beoordelen en beoordelen.

Met beoordelingen kunnen leden van uw community een score en kwalitatieve beoordelingen toevoegen voor elk product of elke service.

## Integratie {#section_kk5_15b_c1b}

Als u een Revisies-app wilt integreren, volgt u de procedure voor het integreren van een Conversation-app. Zie [Een toepassing insluiten](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Hieronder ziet u een voorbeeld van een ingesloten Revisies-app.

### Voorbeeld

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Zoals vermeld in de sectie Building `CollectionMeta`, is `CollectionMeta` een gecodeerd JSON-object. In het bovenstaande voorbeeld heeft het JSON-object de volgende indeling voordat JWT-codering wordt uitgevoerd:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig-object {#section_pzv_ytb_c1b}

Als u de sectie Aan de slag al hebt voltooid, bent u bekend met het ConvConfig-object. Als u Revisies wilt inschakelen, werkt u ConvConfig bij met de volgende velden:

* **** ** alwaysShowEditoroptionalboolean: Standaard wordt de redacteur voor revisies alleen weergegeven nadat de gebruiker op de knop &quot;revisie schrijven&quot; heeft gedrukt. Stel deze parameter in op true als u de editor altijd wilt weergeven.

* **** ** toegepaste tekenreeks: De naam van de app die moet worden gebruikt voor revisies. Moet &quot;recensies&quot; zijn.

* **** ** defaultSortoptionalstring: Hiermee kunt u de standaardoptie voor het sorteren van revisies selecteren. Mogelijke waarden zijn: mostHelpful, hoogsteRated, lowerRated, Nieuwst, en oudst.

* **** ** disableTitleoptionalboolean: Hiermee schakelt u het titelveld in de redacteur voor revisies uit en verbergt u dit veld. Dit veld is standaard vereist en zichtbaar. De standaardwaarde is true.

* **** ** enableHalfRatingoptionalboolean: Wordt gebruikt om halve classificaties in te schakelen op de standaardselectiemodule voor sterren. De standaardwaarde is true.

* **** ** hideShowReviewButtonoptionalboolean: Bepaalt of de  [!UICONTROL Show My Review] knop wordt weergegeven. Ingesteld op true om uw gebruikers toe te staan te selecteren of ze hun eigen revisies moeten weergeven of weergeven.

* **** ** maxRatingoptionalinteger Wordt gebruikt om het aantal sterren in te stellen dat wordt weergegeven in de standaardselectiemodule voor sterren. De standaardwaarde is 5. Dit kan tot 100 worden gevormd.

* **** ** ratingSummaryEnabledoptionalboolean: Wordt gebruikt om de overzichtsweergave voor beoordelingen weer te geven boven Revisies App. Dit moet worden toegelaten om ratingSummaryDelegate te gebruiken. De standaardwaarde is true.

## Metagegevens verzameling controleren {#section_k1s_sqb_c1b}

* **type:** ** vereiste tekenreeks: Definieert het type verzameling. Moet `reviews` zijn.

* **** ** ratingDimensionsoptionalarray: Een array van tekenreeksen voor elk type dimensie dat deze verzameling gebruikt. Als dit niet wordt gespecificeerd, zal slechts 1 afmeting worden toegestaan.

   Stel de array in op: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger: Aantal partities dat moet worden weergegeven in het tekstvak van de revisie. De subonderdeellabels worden doorgegeven met de parameter, zoals hieronder wordt weergegeven.

   >[!NOTE]
   >U moet labels definiëren voor elk subdeel.

* **** ** ratingSubpartsIdsoptionalarray: Hiermee kunt u een id definiëren voor elk subdeel in uw Beoordelingsverzameling. Deze id kan worden gebruikt om deze subdeel-elementen in uw CSS en JavaScript als doel in te stellen. Wanneer gebruikers revisies posten, zal elk `ratingSubpart` het &quot;`data-lf-subpart-id`&quot;attribuut op het hebben, bevolkt met deze identiteitskaart

>[!NOTE]
>
>Als u `ratingSubpartsIds` wilt gebruiken, moet de `ratingSubparts`-parameter ook worden gedefinieerd en moet de lengte van de twee arrays overeenkomen.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Als u `ratingDimensions` gebruikt, MOET u `ratingSelectionDelegate`, `ratingDisplayDelegate`, en `ratingSummaryDelegate` gebruiken (als u het beoordelingsoverzicht wilt tonen).

## Revisies aanpassen {#section_khz_xmb_c1b}

### Sterrenafbeeldingen configureren

Als u de afbeelding voor volledige sterren wilt wijzigen, is de klasse `goog-ratings-star`. Wijzig de achtergrondafbeelding in de gewenste afbeelding. Standaard zijn de sterren 28 x 28 pixels.

### Sterrenafbeeldingen met halve sterren configureren

Met halve sterren zijn er twee klassen, één voor elke zijde van de ster. De linkerzijde van de halve ster is `fyre-rating-half-odd` en de rechterzijde is `fyre-rating-half-even`. De halve sterren zijn standaard 28 x 14 pixels.

### De knopinfo-waarden voor sterren configureren

Om de tooltip waarden voor de sterren te vormen, volg de douanetekst die in de Aanpassingen van het Koord wordt beschreven. Wanneer u die instelling hebt, gebruikt u de toets `ratingValues` en de waarde van een array die de knopinfo-tekenreeksen bevat. Als u halve sterren hebt uitgeschakeld, moet het aantal elementen in de array hetzelfde zijn als `maxRating` (boven). Als u halve sterren hebt ingeschakeld, moet het aantal elementen 2x `maxRating` zijn. Het eerste element in de array komt overeen met het element met de meest linkse ster (of halve ster) en gaat verder van links naar rechts.

### De optie Mijn revisie tonen in-/uitschakelen

Als u de optie [!UICONTROL Show My Review] wilt in- of uitschakelen, wijst u de parameter `hideShowReviewButton` aan in de App-configuratie.

### Teksteditor standaard weergeven

De redacteur van overzichten verschijnt slechts nadat de gebruiker [!UICONTROL write review] knoop drukt. Om deze vorm door gebrek te tonen, richt de `alwaysShowEditor` parameter in de configuratie van de App.
