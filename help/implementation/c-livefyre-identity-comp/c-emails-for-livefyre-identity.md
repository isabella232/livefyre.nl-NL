---
description: 'null'
seo-description: 'null'
seo-title: E-mails voor identiteit LiveCycle
solution: Experience Manager
title: E-mails voor identiteit LiveCycle
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---


# E-mails voor LiveCycle Identity{#emails-for-livefyre-identity}

Met LiveCyre Identity worden de volgende e-mails verzonden:

* [E-mail opnieuw instellen](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verificatiebericht](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [E-mailverificatie verzenden voor gebruikers](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Welkom-e-mail](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Welkom-e-mail naar gebruikers sturen](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

U kunt de vormgeving van alle e-mails met LiveCycle Identity aanpassen in **[!UICONTROL Integration Settings > Email Notifications.]**

## Wachtwoord opnieuw e-mail {#section_nd1_whs_p1b}

LiveCycle stuurt automatisch een e-mail waarin een wachtwoord opnieuw wordt ingesteld wanneer een gebruiker zijn wachtwoord opnieuw probeert in te stellen.

De e-mail voor het opnieuw instellen van wachtwoorden ziet er als volgt uit:

**Betreft: Wachtwoord** opnieuw instellen

**Lichaam:**

Hey daar *&lt;username>*,

Er was een verzoek om het wachtwoord van uw profiel op *&lt;network name>* te veranderen.

Klik op de volgende koppeling om een nieuw wachtwoord te kiezen als u dit hebt aangevraagd: *&lt;password reset URL>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>* en  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* worden allemaal dynamisch gegenereerd op basis van de sitebezoeker en uw netwerk.

## Verificatiebericht {#section_ak5_xhs_p1b}

U kunt een e-mail verzenden waarin het e-mailadres van een gebruiker wordt geverifieerd. Als u verificatie-e-mails wilt verzenden, moet u de optie inschakelen in **Integratie-instellingen > Live-identiteit**.

De verificatie-e-mail ziet er als volgt uit:

**Betreft:** E-mailverificatie

**Lichaam:**

Hello *&lt;username>*,

Klik op de volgende koppeling (of plak deze in uw browser) om uw account te verifiëren: *&lt;verificatie URL>*.

Deze koppeling verloopt over 24 uur.

Bedankt,

Het *&lt;klantnaam>* Team

*&lt;username>*,  *&lt;network name=&quot;&quot;>* en  *&lt;verification URL=&quot;&quot;>* worden allemaal dynamisch gegenereerd op basis van de sitebezoeker en uw netwerk.

## Een e-mailverificatie verzenden naar gebruikers {#section_vyv_yhs_p1b}

U kunt een e-mail naar een gebruiker sturen om het e-mailadres te verifiëren dat deze gebruikt om u aan te melden voor een account. Een verificatiebericht verzenden:

1. Klik in Studio op het tandwielpictogram om de netwerkinstellingen te wijzigen.
1. Klik **Integratie-instellingen > LiveCycle Identity.**

1. Navigeer naar **Aanmeldingstypen**.
1. Klik **E-mailverificatie vereisen** om een e-mail te verzenden naar gebruikers die het e-mailadres verifiëren dat zij gebruiken om zich aan te melden voor een account.
1. Navigeer naar **Netwerk-e-mail** om het **logo voor e-mail**, het e-mailadres voor gebruik als adres (**E-mail van**), en de weergavenaam voor het adres van e-mailadres (**E-mailweergavenaam**) te configureren.

## Welkom-e-mail {#section_z2v_zhs_p1b}

U kunt een welkomstbericht naar gebruikers sturen. Als u welkome e-mailberichten wilt verzenden, moet u de optie inschakelen in **Integratie-instellingen** > **LiveCycle Identity**.

De welkomstmail ziet er als volgt uit:

**Betreft:** Welkom bij  *&lt;customer name=&quot;&quot;>*

**Lichaam:**

Hello *&lt;username>*,

Er is een account voor u gemaakt op *&lt;naam klant>*.

Dit account is gemaakt op *&lt;verwijzing URL>* van IP-adres *&lt;IP-adres>*.

Als je dit hebt gedaan, kun je deze e-mail veilig negeren.

Neem contact op met `support@livefyre.com` als u dit niet hebt gedaan

Bedankt

Het *&quot;klantnaam&quot;* Team

*De &quot;Gebruikersnaam&quot;, &quot;klantnaam&quot;, &quot;verwijzings-URL&quot;* en &quot;IP-adres&quot; worden allemaal dynamisch gegenereerd op basis van de sitebezoeker en uw netwerk.

## Een welkomstbericht verzenden naar een gebruiker {#section_kjp_c3s_p1b}

U kunt een welkomstbericht verzenden naar een gebruiker nadat deze zich heeft aangemeld voor een account. Studio verzendt dit e-mailbericht nadat het een verificatiebericht heeft verzonden als u een verificatiebericht hebt ingesteld. Een welkomstbericht verzenden:

1. Klik in Studio op het tandwielpictogram om de netwerkinstellingen te wijzigen.
1. Klik op **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Ga naar **[!UICONTROL Email Settings]**.

1. Klik **[!UICONTROL Send Welcome Emails To New Users]** om het verzenden van e-mails in te schakelen.
1. Navigeer naar **[!UICONTROL Network Email]** om het *Logo voor E-mail*, het e-mailadres te vormen om als adres van de uitgang (**E-mail van**) te gebruiken, en de vertoningsnaam voor de van e-mailadres (**E-mailvertoningsnaam**) te gebruiken.
