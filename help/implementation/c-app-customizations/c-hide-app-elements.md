---
description: Verwijder standaard LiveCyre App-componenten uit uw app.
seo-description: Verwijder standaard LiveCyre App-componenten uit uw app.
seo-title: App Elements verbergen
solution: Experience Manager
title: App Elements verbergen
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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

