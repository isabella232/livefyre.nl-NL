---
description: U kunt Livefyre Identiteit met Identiteit gebruiken GitHub om gebruikers toe te staan om hun logins te gebruiken GitHub om Apps op uw plaats in wisselwerking te staan.
title: Een GitHub Identity-app maken voor gebruik met LiveCyre-identiteit
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# Creeer een App van de Identiteit van GitHub voor Gebruik met Identiteit Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

U kunt Livefyre Identiteit met Identiteit gebruiken GitHub om gebruikers toe te staan om hun logins te gebruiken GitHub om Apps op uw plaats in wisselwerking te staan.

Om gebruikers toe te staan om met hun geloofsbrieven van de Identiteit te registreren GitHub, vereist Livefyre de volgende Informatie van de Identiteit GitHub:

* Client-id (persoonlijke sleutel)
* Clientgeheim (wachtwoord)

Een GitHub Identity-app maken voor gebruik met LiveCyre-identiteit:

1. Creeer of onderteken binnen aan een rekening GitHub bij [](https://github.com/settings/developers).
1. Registreer een nieuwe of selecteer een bestaande app voor gebruik met LiveCycle Identity.
1. Voer alle gegevens in op het formulier. Voer **[!UICONTROL Authorization callback URL]** in met uw netwerknaam in plaats van `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. Schakel in **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]** de schakeloptie **[!UICONTROL Enable GitHub Login]** in op **[!UICONTROL On]**.

1. Ga identiteitskaart van de Cliënt GitHub en Geheim van de Cliënt GitHub in.
1. Klik op **[!UICONTROL Save Settings]**.

Wanneer volledig, zal de de toepassingsdetailpagina van GitHub van Identiteit een lijst maken van identiteitskaart van de Cliënt van de App (Consumentensleutel) en Geheim van de Cliënt (Consumentengeheim) voor gebruik in de pagina van de Montages van de Integratie van Studio.
