---
description: Registreer het URL-eindpunt zodat LiveCycle de URL kan gebruiken om bijgewerkte profielinformatie te verkrijgen.
title: Registreer het Eindpunt met Studio
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Registreer het Eindpunt met Studio{#register-the-endpoint-with-studio}

Registreer het URL-eindpunt zodat LiveCycle de URL kan gebruiken om bijgewerkte profielinformatie te verkrijgen.

Registreer Ping voor Pull URL slechts eenmaal per netwerk. Zodra reeks, zou deze waarde niet moeten veranderen tenzij het eindpunt voor het halen van gegevens van het gebruikersprofiel van uw systeem van het gebruikersbeheer verandert.

1. Gebruik Studio om dit URL-eindpunt bij Livefyre te registreren.
1. Registreer de URL vanwaar LiveCyre bijgewerkte gegevens van het gebruikersprofiel ophaalt, ga naar **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**, en ga het in het **[!UICONTROL Ping for Pull URL]** gebied in.

   De URL kan er bijvoorbeeld als volgt uitzien: `https://example.yoursite.com/some_path/?id={id}`
