---
description: Registreer het URL-eindpunt zodat LiveCycle de URL kan gebruiken om bijgewerkte profielinformatie te verkrijgen.
seo-description: Registreer het URL-eindpunt zodat LiveCycle de URL kan gebruiken om bijgewerkte profielinformatie te verkrijgen.
seo-title: Registreer het Eindpunt met Studio
solution: Experience Manager
title: Registreer het Eindpunt met Studio
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Registreer het Eindpunt met Studio{#register-the-endpoint-with-studio}

Registreer het URL-eindpunt zodat LiveCycle de URL kan gebruiken om bijgewerkte profielinformatie te verkrijgen.

Registreer Ping voor Pull URL slechts eenmaal per netwerk. Zodra reeks, zou deze waarde niet moeten veranderen tenzij het eindpunt voor het halen van gegevens van het gebruikersprofiel van uw systeem van het gebruikersbeheer verandert.

1. Gebruik Studio om dit URL-eindpunt bij Livefyre te registreren.
1. Registreer de URL vanwaar LiveCyre bijgewerkte gegevens van het gebruikersprofiel ophaalt, ga naar **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**, en ga het in het **[!UICONTROL Ping for Pull URL]** gebied in.

   De URL kan er bijvoorbeeld als volgt uitzien: `https://example.yoursite.com/some_path/?id={id}`

