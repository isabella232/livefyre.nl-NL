---
description: LiveCycle gebruikt een PUSH-interface om externe systeeminformatie over wijzigingen in gebruikersmachtigingen te verzenden.
title: Gebruikersmachtigingen naar externe systemen posten (optioneel)
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# Gebruikersmachtigingen naar externe systemen verzenden (optioneel){#posting-user-permissions-to-external-systems-optional}

LiveCycle gebruikt een PUSH-interface om externe systeeminformatie over wijzigingen in gebruikersmachtigingen te verzenden.

## Typen gebruikers in LiveCyre Studio

| Gebruikerstype | Beschrijving |
|--- |--- |
| eigenaar | Deze gebruiker is een eigenaar, en kan zowel inhoud matigen, als nieuwe moderatoren toewijzen. |
| beheerder | Deze gebruiker is een moderator, en kan inhoud matigen. |
| lid | Deze gebruiker staat op de lijst. Geposte inhoud gaat niet door spam- of dieptefilters en vereist geen goedkeuring in vooraf gemodereerde stromen. |
| none | Deze gebruiker is een standaardgebruiker en heeft geen speciale machtigingen. |
| uitzenden | Deze gebruiker mag niet deelnemen aan gesprekken. |

Als u gebruikersmachtigingen naar externe systemen wilt posten, moet u een URL registreren die machtigingsgegevens ontvangt als POST-aanvragen.

Bijvoorbeeld:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parameter | Beschrijving |
|--- |--- |
| networkName | Uw door Livefyre opgegeven netwerknaam. |
| token | Geldige systeemtoken. |
| url | URL om te registreren. |

De geregistreerde URL moet POST&#39;s met de volgende gegevens als inhoudstype accepteren: application/x-www-form-urlencoded.

| Parameter | Beschrijving |
|--- |--- |
| jid | JID van de gebruiker wiens aansluiting is gewijzigd. Een JID is een tekenreeks in de vorm `user_id@network`. |
| aansluiting | Naam van de toegewezen toestemmingen, die één van het volgende moet zijn:  `{admin | member | none | outcast | owner}` |

Zie [Referentie gebruikersassociatie-API toevoegen](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post) voor meer informatie over het bijwerken van instellingen voor gebruikersbinding.
