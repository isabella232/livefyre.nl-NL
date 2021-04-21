---
description: Pak het aantal posten en opmerkingen voor bepaalde verzamelingen die op de indexpagina's moeten worden weergegeven.
title: Aantal opmerkingen weergeven
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Aantal opmerkingen weergeven{#display-comment-count}

Pak het aantal posten en opmerkingen voor bepaalde verzamelingen die op de indexpagina&#39;s moeten worden weergegeven.

Met de `CommentCount.js` van Livefyre kunt u het aantal inhoud ophalen voor verzamelingen op uw site. Hoewel Apps de commentaartelling voor de huidige inzameling zullen tonen, kan het hebben van deze tellingen die over uw plaats worden gesynchroniseerd nuttig zijn. Deze functie is vooral handig als u de inhoud van uw database niet wilt behouden (of als uw CMS-database niet is gesynchroniseerd met LiveCycle).

1. Laad het JavaScript.

   Als u `CommentCount.js` wilt gebruiken, sluit u eerst het JavaScript-bestand in de sectie `<head>` van de pagina of sjabloon in waar u het wilt gebruiken.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Bind het HTML-element.

   Wanneer het script is geladen, wordt geprobeerd andere elementen op de pagina te zoeken met de klassenaam `livefyre-commentcount`. Voor elk van deze elementen zoekt het script naar de HTML-kenmerken `data-lf-site-id` en `data-lf-article-id` en gebruikt het deze om inhoud van LiveCycle op te halen en elk element bij te werken met de laatste waarde.

   Het volgende element wordt bijvoorbeeld bijgewerkt:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >De code `CommentCount.js` controleert of een numerieke waarde met het daadwerkelijke aantal moet bijwerken. Zorg ervoor dat u een numerieke waarde tussen de tags opneemt.

   **Voorbeeld 1**  (URL gebruiken als artikel-id):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Voorbeeld 2**  (Een genummerd systeem gebruiken als de artikel-id):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configureer opties.

   Voor meer controle over hoe de inhoudsaantallen worden vervangen, vraag `LF.CommentCount()` en ga in een voorwerp over dat de configuratieopties bevat. Zorg ervoor dat u de functie aanroept nadat alle elementen die moeten worden vervangen zich in het DOM bevinden. De beste plaats om deze methode aan te roepen is in footer, zodat gebeurt het wanneer DOM wordt geladen, maar voorafgaand aan document en venster klaar gebeurtenissen.

   Wij staan de volgende configuratieopties toe:

* **replacer:** Function of Regex gebruikt om de tekst van elk inhoudaantal te vervangen.

* **functie:** gebruikt om de vervanging op elk element uit te voeren. De argumenten van de functie zijn:

   **element:** het HTML-element dat wordt bijgewerkt.
   **aantal:** het aantal inhoud voor dit element.

* **regex:** gebruikt om te bepalen welk deel van de elementtekst door de telling zou moeten worden vervangen.

   **Voorbeeld**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Gebruik de vervanger om het bericht voor het tellen van opmerkingen aan te passen of te internationaliseren.
