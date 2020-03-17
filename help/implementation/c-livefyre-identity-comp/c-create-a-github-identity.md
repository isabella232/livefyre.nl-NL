---
description: U kunt Livefyre Identiteit met Identiteit gebruiken GitHub om gebruikers toe te staan om hun logins te gebruiken GitHub om Apps op uw plaats in wisselwerking te staan.
seo-description: U kunt Livefyre Identiteit met Identiteit gebruiken GitHub om gebruikers toe te staan om hun logins te gebruiken GitHub om Apps op uw plaats in wisselwerking te staan.
seo-title: Een GitHub Identity-app maken voor gebruik met LiveCyre-identiteit
title: Een GitHub Identity-app maken voor gebruik met LiveCyre-identiteit
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Een GitHub Identity-app maken voor gebruik met LiveCyre-identiteit{#create-a-github-identity-app-for-use-with-livefyre-identity}

U kunt Livefyre Identiteit met Identiteit gebruiken GitHub om gebruikers toe te staan om hun logins te gebruiken GitHub om Apps op uw plaats in wisselwerking te staan.

Om gebruikers toe te staan om met hun geloofsbrieven van de Identiteit te registreren GitHub, vereist Livefyre de volgende Informatie van de Identiteit GitHub:

* Client-id (persoonlijke sleutel)
* Clientgeheim (wachtwoord)

Een GitHub Identity-app maken voor gebruik met LiveCyre-identiteit:

1. Creeer of onderteken binnen aan een rekening GitHub bij [](https://github.com/settings/developers).
1. Registreer een nieuwe of selecteer een bestaande app voor gebruik met LiveCycle Identity.
1. Voer alle gegevens in op het formulier. Ga in, gebruikend uw netwerknaam in plaats van **[!UICONTROL Authorization callback URL]**`{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. Schakel in **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, de **[!UICONTROL Enable GitHub Login]** schakeloptie in op **[!UICONTROL On]**.

1. Ga identiteitskaart van de Cliënt GitHub en Geheim van de Cliënt GitHub in.
1. Klik op **[!UICONTROL Save Settings]**.

Wanneer volledig, zal de de toepassingsdetailpagina van GitHub van Identiteit een lijst maken van identiteitskaart van de Cliënt van de App (Consumentensleutel) en Geheim van de Cliënt (Consumentengeheim) voor gebruik in de pagina van de Montages van de Integratie van Studio.
