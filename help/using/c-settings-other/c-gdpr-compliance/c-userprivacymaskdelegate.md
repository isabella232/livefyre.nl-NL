---
description: U kunt de waarschuwingstekst wijzigen die op videomaskers wordt weergegeven.
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

U kunt de waarschuwingstekst wijzigen die op videomaskers wordt weergegeven.

Deze tekst is in overeenstemming met de GDPR-verordening. Als een bron geen proxy ondersteunt, wordt deze tekst en een masker op de inhoud weergegeven in LiveCycle, tenzij een gebruiker op de video klikt en de mogelijke tracering vanuit die bron goedkeurt.

Als u `userPrivacyMaskDelegate` niet gebruikt, wordt de volgende standaardtekst weergegeven:

`userPrivacyMaskDelegate` toevoegen na `userPrivacyOptOut`. U kunt alle privacymarkeringen voor Livefyre tegelijk toevoegen als onderdeel van één Livefyre-object.

Hier is een voorbeeld van hoe te om `userPrivacyMaskDelegate` te gebruiken:

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
