---
description: 'null'
seo-description: 'null'
seo-title: E-mails voor identiteit LiveCycle
solution: Experience Manager
title: E-mails voor identiteit LiveCycle
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# E-mails voor identiteit LiveCycle{#emails-for-livefyre-identity}

Met LiveCyre Identity worden de volgende e-mails verzonden:

* [E-mail opnieuw instellen](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verificatiebericht](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [E-mailverificatie verzenden voor gebruikers](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Welkom-e-mail](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Welkom-e-mail naar gebruikers sturen](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

U kunt de vormgeving van alle e-mails met de identiteit van uw levensstijl aanpassen in **[!UICONTROL Integration Settings > Email Notifications.]**

## E-mail opnieuw instellen {#section_nd1_whs_p1b}

LiveCycle stuurt automatisch een e-mail waarin een wachtwoord opnieuw wordt ingesteld wanneer een gebruiker zijn wachtwoord opnieuw probeert in te stellen.

De e-mail voor het opnieuw instellen van wachtwoorden ziet er als volgt uit:

**Betreft:** Wachtwoord opnieuw instellen

**Lichaam:**

Hey daar *&lt;username>*,

Er is een verzoek ingediend om het wachtwoord van uw profiel op *&lt;network name>* te wijzigen.

Klik op de volgende koppeling om een nieuw wachtwoord te kiezen als u dit hebt aangevraagd: *&lt;password reset URL>*.

*&lt;Gebruikersnaam>*, *&lt;netwerknaam>*, en *&lt;wachtwoord het terugstellen URL>* allen worden dynamisch geproduceerd gebaseerd op de plaatsbezoeker en uw netwerk.

## Verificatiebericht {#section_ak5_xhs_p1b}

U kunt een e-mail verzenden waarin het e-mailadres van een gebruiker wordt geverifieerd. Als u verificatie-e-mails wilt verzenden, moet u de optie inschakelen in **Integratie-instellingen > Live-identiteit**.

De verificatie-e-mail ziet er als volgt uit:

**Betreft:** E-mailverificatie

**Lichaam:**

Hello *&lt;username>*,

Klik op de volgende koppeling (of plak deze in uw browser) om uw account te verifiëren: *&lt;verificatie-URL>*.

Deze koppeling verloopt over 24 uur.

Bedankt,

Het *&lt;klantnaam>* Team

*&lt;gebruikersnaam>*, *&lt;netwerknaam>* en *&lt;verificatie-URL>* worden allemaal dynamisch gegenereerd op basis van de bezoeker van de site en uw netwerk.

## Een e-mailverificatie naar gebruikers sturen {#section_vyv_yhs_p1b}

U kunt een e-mail naar een gebruiker sturen om het e-mailadres te verifiëren dat deze gebruikt om u aan te melden voor een account. Een verificatiebericht verzenden:

1. Klik in Studio op het tandwielpictogram om de netwerkinstellingen te wijzigen.
1. Klik op **Integratie-instellingen > LiveCycle-identiteit.**

1. Navigeer naar **aanmeldingstypen**.
1. Klik op E-mailverificatie **** vereisen om een e-mail te verzenden naar gebruikers die het e-mailadres verifiëren dat zij gebruiken om zich aan te melden voor een account.
1. Navigeer naar **Netwerk-e-mail** om het **logo voor e-mail**, het e-mailadres dat als adres van het adres (**E-mail van**) moet worden gebruikt en de weergavenaam voor het adres van e-mailadres (**E-mailweergavenaam**) te configureren.

## Welkom-e-mail {#section_z2v_zhs_p1b}

U kunt een welkomstbericht naar gebruikers sturen. Als u welkome e-mailberichten wilt verzenden, moet u de optie inschakelen in **Integratie-instellingen** > **Live-identiteit**.

De welkomstmail ziet er als volgt uit:

**Betreft:** Welkom bij *&lt;naam klant>*

**Lichaam:**

Hello *&lt;username>*,

Er is een account voor u gemaakt op *&lt;naam van klant>*.

Dit account is gemaakt op *&lt;verwijzing URL>* van IP-adres *&lt;IP Address>*.

Als je dit hebt gedaan, kun je deze e-mail veilig negeren.

Neem contact op met `support@livefyre.com`

Bedankt

Het *&quot;klantennaam&quot;* Team

*De &quot;Gebruikersnaam&quot;, &quot;klantnaam&quot;, &quot;verwijzing URL&quot;* en &quot;IP Adres&quot;worden allen dynamisch geproduceerd gebaseerd op de plaatsbezoeker en uw netwerk.

## Een welkomstbericht verzenden naar een gebruiker {#section_kjp_c3s_p1b}

U kunt een welkomstbericht verzenden naar een gebruiker nadat deze zich heeft aangemeld voor een account. Studio verzendt dit e-mailbericht nadat het een verificatiebericht heeft verzonden als u een verificatiebericht hebt ingesteld. Een welkomstbericht verzenden:

1. Klik in Studio op het tandwielpictogram om de netwerkinstellingen te wijzigen.
1. Klik op **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Ga naar **[!UICONTROL Email Settings]**.

1. Klik **[!UICONTROL Send Welcome Emails To New Users]** om het verzenden van e-mails in te schakelen.
1. Navigeer om het **[!UICONTROL Network Email]** Logo voor E-mail *, het e-mailadres te vormen om als adres van (* E-mail van **) te gebruiken, en de vertoningsnaam voor het van e-mailadres (de Naam** van de **** Vertoning E-mail) te gebruiken.
