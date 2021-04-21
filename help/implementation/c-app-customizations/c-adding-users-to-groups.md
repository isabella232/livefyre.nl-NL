---
description: Voeg een gebruikerstag toe aan een account om een gebruiker aan een groep toe te voegen.
title: Gebruikers toevoegen aan groepen
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Gebruikers toevoegen aan groepen{#adding-users-to-groups}

Voeg een gebruikerstag toe aan een account om een gebruiker aan een groep toe te voegen.

De tags van de gebruiker kunnen voor zowel merkgebonden als ondernemingsprofielsystemen worden uitgevoerd, en kunnen aan rekeningen op verscheidene manieren worden toegevoegd:

* Als u eigenaars en moderatoren via Studio maakt, wordt de gebruikerstag Moderator aan de account toegewezen.
* Wanneer u gebruikersgroepen maakt en gebruikers aan deze groepen toevoegt via Studio, worden automatisch gebruikerstags met de naam van de groep toegepast op de geselecteerde gebruikers.
* De Markeringen van de gebruiker kunnen ook direct op Rekeningen worden toegepast gebruikend [voeg de vraag van HTTP](https://api.livefyre.com/docs#add-user-tag) van de Markering van de Gebruiker toe, of pingelt voor Pull.

>[!NOTE]
>
>Beide API-methoden, de HTTP Add User Tag-aanroep en de Ping for Pull-methode, overschrijven alle tags die eerder aan de Account zijn toegewezen via andere methoden. Selecteer daarom één methode en gebruik deze consistent gedurende het hele proces.

## Voeg een gebruiker aan een Groep van de pagina van Gebruikers in Studio {#section_qgq_nbw_xz} toe

* Klik op **[!UICONTROL Add Group]** of het groeplabel onder een gebruikersnaam om het menu Groepen te openen.
* Blader door de lijst en zoek de groep waaraan u de gebruiker wilt toevoegen. U kunt een groepsnaam invoeren in het vak **[!UICONTROL Search]** boven aan het vervolgkeuzemenu.
* Klik op het selectievakje naast de groep(en) waaraan de gebruiker moet worden toegevoegd en klik op Enter.

In het gebruikersprofiel wordt de naam van de groep (als de gebruiker slechts in één groep is) of het aantal groepen weergegeven waartoe de gebruiker behoort.

## Voeg een gebruiker aan een groep toe gebruikend de Add vraag van de Markering van de Gebruiker {#section_kn3_gbw_xz}

Geef de LFToken van de gebruiker en de naam van de geselecteerde tag door met de aanvraag van de POST

Bijvoorbeeld:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Zie API-naslaggids > [Gebruikerstag toevoegen](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post) voor meer informatie.

## Een gebruiker toevoegen aan een groep met Ping for Pull {#section_kyj_11w_xz}

Gebruik de array met tags om gebruikers toe te wijzen aan gebruikersgroepen. (Tags kunnen 1-63 alfanumerieke tekens en onderstrepingstekens bevatten.)

Bijvoorbeeld:

```
"tags": ["moderator", "brand_advocate"],
```

## Een gebruiker aan een groep toevoegen met Externe profielen {#section_uyn_scv_xz}

Voeg gebruikerstags toe aan het externe profiel, waarmee gebruikersgegevens voor specifieke gebruikers worden gesynchroniseerd tussen het aangepaste profielsysteem en het LiveCycle.
