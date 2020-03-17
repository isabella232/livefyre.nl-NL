---
description: Als u aangepaste stijlinhoud voor gebruikersgroepen wilt gebruiken, moet u eerst een gebruikerstag aan de account toevoegen en de inhoud vervolgens opmaken met CSS.
seo-description: Als u aangepaste stijlinhoud voor gebruikersgroepen wilt gebruiken, moet u eerst een gebruikerstag aan de account toevoegen en de inhoud vervolgens opmaken met CSS.
seo-title: Aangepaste stijlen toepassen
solution: Experience Manager
title: Aangepaste stijlen toepassen
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aangepaste stijlen toepassen{#applying-custom-styles}

Als u aangepaste stijlinhoud voor gebruikersgroepen wilt gebruiken, moet u eerst een gebruikerstag aan de account toevoegen en de inhoud vervolgens opmaken met CSS.

Voor elke gebruikerstag die via Studio of Ping for Pull wordt toegevoegd, maakt LiveCyre twee CSS-klassen die beide kunnen worden gebruikt om de inhoud van de groep op te maken.

Bij het converteren van gebruikerstags naar CSS-klassen:

* Met Livefyre maakt u twee klassen: voormalige auteur-tag-***&lt;your_group>** en fyre-tag-auteur-***&lt;your_group>***. Beide kunnen worden gebruikt om de inhoud op te maken.

* Alle spaties in de tag worden omgezet in onderstrepingstekens. Bijvoorbeeld: &quot;Favoriete gebruiker&quot; wordt favoriete_gebruiker.
* Unicode-tekens die in groepsnamen zijn opgenomen, worden niet omgezet en worden in de klassennamen als Unicode weergegeven. Bijvoorbeeld: De gebruikersgroep &quot;modérateur&quot; wordt fyre-comment-auteur-tag-modérateur.

Nadat uw gebruikersgroepen zijn gemaakt, gebruikt u de CSS-klassen van LiveCyre om aangepaste opmaak voor de inhoud toe te passen.

## Stijlinhoud voor moderatoren (en eigenaars) {#section_vjv_2cv_xz}

* Gebruik de CSS-klasse .fyre-moderator.

   >[!NOTE]
   >
   >Eigenaars, omdat ze ook Moderatoren zijn, hebben deze klasse ook toegepast op hun inhoud in de stream.

* Maak een CSS-regel om een badge voor de groep weer te geven of op te maken:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Stijlinhoud voor gebruikersgroepen {#section_ghn_s1v_xz}

Maak een CSS-regel om een badge voor de groep weer te geven of op te maken:

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Gebruik de CSS-klasse fyre-schrijver-tag-***&lt;your_group>*** of fyre-tag-auteur-***&lt;your_group>*** om het lettertype en de achtergrond op te maken voor elk item dat is gepost via een account dat is gekoppeld aan de geselecteerde tag.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

