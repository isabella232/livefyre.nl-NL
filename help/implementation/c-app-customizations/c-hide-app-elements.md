---
description: Verwijder standaard LiveCyre App-componenten uit uw app.
title: App Elements verbergen
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# App Elements verbergen{#hide-app-elements}

Verwijder standaard LiveCyre App-componenten uit uw app.

Gebruik CSS om de standaardelementen van LiveCycle App van uw pagina te verbergen, zodat u de gebruikerservaring kunt aanpassen aan uw behoeften.

Als u elementen in de app wilt verbergen, stelt u de weergave in op Geen.

Voorbeelden:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
