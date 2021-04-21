---
description: Aangepaste stijlen worden toegepast via een object dat in de constructor Sidenotes wordt geïnjecteerd.
title: Aangepaste stijlen voor markeringen
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Aangepaste stijlen zoeken{#sidenotes-custom-styles}

Aangepaste stijlen worden toegepast via een object dat in de constructor Sidenotes wordt geïnjecteerd.

De &quot;sleutels&quot; zijn objectsleutels die DOM-elementen vertegenwoordigen, terwijl &quot;eigenschappen&quot; ondersteunde CSS-eigenschappen zijn voor de specifieke sleutel. Als u bijvoorbeeld de stijl van blockBtn wilt aanpassen (de knop waarmee de pop-up Sidenotes wordt gestart), maakt u een object zoals:

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **Sleutel** | **Eigenschappen** | Beschrijving |
|---|---|---|
| `anonymousAvatar` | &quot;height&quot;, &quot;width&quot; | Anonieme avatarafbeelding, links van de tekstgebiededitor. |
| `blockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Het pictogram &quot;Launcher&quot; dat naast de elementen wordt geplaatst die als sidenote-able zijn opgegeven. |
| `blockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Startpictogram als de status actief is. |
| `commentAvatar` | &quot;height&quot;, &quot;width&quot; | Avatar beeld links van hoogste niveaunota&#39;s. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tekst van verbonden notities. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | De naam van de vertoning van gebruiker die een nota heeft verlaten. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Knop Downloaden naar een notitie. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Knop voor het uitbreiden van draden met een groot aantal reacties. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tags over een gebruiker op een notitie. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Knop Uploaden naar een notitie. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tekstgebiedinvoervak voor het verlaten van notities. |
| `mediaBlockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Media-startpictogram boven op een media-item (img, video). |
| `mediaBlockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Pictogram voor het starten van media in actieve toestand. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Klik op de knop die het aantal vertoningen in de verzameling weergeeft. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Maak een pop-up met een korte uitleg van Sidenotes voor de gebruiker. |
| `popover` | &quot;backgroundColor&quot; | Popover die omhoog wordt gebracht wanneer het lanceringspictogram aanhaalde. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Pijlelement naar links op de pop-up dat wijst naar het DOM-element dat een opstartpictogram bevat. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Pijlelement rechts op de pop-up dat naar het DOM-element verwijst dat een opstartpictogram bevat. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Het bovenste pijlelement in de pop-up dat naar het DOM-element verwijst dat een opstartpictogram bevat. |
| `replyAvatar` | &quot;height&quot;, &quot;width&quot; | Avatarafbeelding links van opmerkingen op antwoordniveau. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Voettekst met de optie Aangedreven door. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Knop om aan te geven wanneer nieuwe notities in een open pop-up worden gestreamd. |
| `userAvatar` | &quot;height&quot;, &quot;width&quot; | De voor authentiek verklaarde afbeelding van de gebruiker avatar, links van de redacteur van het tekstgebied. |
