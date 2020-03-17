---
description: Pak het aantal posten en opmerkingen voor bepaalde verzamelingen die op de indexpagina's moeten worden weergegeven.
seo-description: Pak het aantal posten en opmerkingen voor bepaalde verzamelingen die op de indexpagina's moeten worden weergegeven.
seo-title: Aantal opmerkingen weergeven
solution: Experience Manager
title: Aantal opmerkingen weergeven
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# Aantal opmerkingen weergeven{#display-comment-count}

Pak het aantal posten en opmerkingen voor bepaalde verzamelingen die op de indexpagina&#39;s moeten worden weergegeven.

Met Livefyre `CommentCount.js` kunt u het aantal inhoud ophalen voor verzamelingen op uw site. Hoewel Apps de commentaartelling voor de huidige inzameling zullen tonen, kan het hebben van deze tellingen die over uw plaats worden gesynchroniseerd nuttig zijn. Deze functie is vooral handig als u de inhoud van uw database niet wilt behouden (of als uw CMS-database niet is gesynchroniseerd met LiveCycle).

1. Laad het JavaScript.

   Als u het JavaScript-bestand wilt gebruiken, moet u het eerst insluiten in de `CommentCount.js``<head>` sectie van de pagina of sjabloon waar u het wilt gebruiken.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Bind het HTML-element.

   Wanneer het script is geladen, wordt geprobeerd andere elementen op de pagina te zoeken met de klassenaam `livefyre-commentcount`. Voor elk van deze elementen zoekt het script naar `data-lf-site-id` en `data-lf-article-id` HTML-kenmerken en gebruikt het deze om inhoud van LiveCycle op te halen en elk element bij te werken met de laatste waarde.

   Het volgende element wordt bijvoorbeeld bijgewerkt:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {Important=&quot;high&quot;}
   >
   >De `CommentCount.js` code controleert of een numerieke waarde wordt bijgewerkt met het werkelijke aantal. Zorg ervoor dat u een numerieke waarde tussen de tags opneemt.

   **Voorbeeld 1** (URL gebruiken als artikel-id):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Voorbeeld 2** (Een genummerd systeem gebruiken als de artikel-id):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configureer opties.

   Voor meer controle over hoe de inhoudsaantallen worden vervangen, vraag `LF.CommentCount()` en ga in een voorwerp over dat de configuratieopties bevat. Zorg ervoor dat u de functie aanroept nadat alle elementen die moeten worden vervangen zich in het DOM bevinden. De beste plaats om deze methode aan te roepen is in footer, zodat gebeurt het wanneer DOM wordt geladen, maar voorafgaand aan document en venster klaar gebeurtenissen.

   Wij staan de volgende configuratieopties toe:

* **vervanger:** Functie of Regex die wordt gebruikt om de tekst van elk inhoudaantal te vervangen.

* **functie:** Gebruikt om de vervanging op elk element te doen. De argumenten van de functie zijn:

   **element:** Het HTML-element dat wordt bijgewerkt.
   **aantal:** The content count for this element.

* **regex:** Wordt gebruikt om te bepalen welk deel van de tekst van het element moet worden vervangen door de telling.

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
