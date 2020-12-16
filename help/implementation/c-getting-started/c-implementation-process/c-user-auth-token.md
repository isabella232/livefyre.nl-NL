---
description: In deze sectie wordt beschreven hoe u het JSON-object UserAuth genereert dat het token User Authentication (Gebruikersverificatie) maakt dat nodig is om gebruikers aan te melden bij uw apps.
seo-description: In deze sectie wordt beschreven hoe u het JSON-object UserAuth genereert dat het token User Authentication (Gebruikersverificatie) maakt dat nodig is om gebruikers aan te melden bij uw apps.
seo-title: Token van auteur
solution: Experience Manager
title: Token van auteur
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# Token van auteur{#user-auth-token}

In deze sectie wordt beschreven hoe u het JSON-object UserAuth genereert dat het token User Authentication (Gebruikersverificatie) maakt dat nodig is om gebruikers aan te melden bij uw apps.

In deze sectie wordt beschreven hoe u het JSON-object UserAuth genereert dat het token User Authentication (Gebruikersverificatie) maakt dat nodig is om gebruikers aan te melden bij uw apps.

Als u het token wilt maken, gebruikt u de voorkeurstaalbibliotheek om de volgende parameters door te geven:

| Parameter | Type | Beschrijving |
|---|---|---|
| networkName | Tekenreeks *required* | De naam van het Livefyre-netwerk (verstrekt door Livefyre). |
| networkKey | Tekenreeks *required* | De geheime sleutel voor dit specifieke netwerk (verstrekt door Livefyre). |
| userId | Tekenreeks *required* | De id van de gebruiker die zich aanmeldt als opgeslagen in uw gebruikersbeheersysteem (alleen alfanumerieke tekens, streepjes, onderstrepingstekens en punttekens zijn toegestaan: [a-zA-Z0-9_-.]). **Opmerking:** de gebruikersnaam moet uniek zijn. |
| verloopt | Geheel *vereist* | Wanneer het token vanaf nu (in seconden) moet verlopen. **Opmerking:** deze waarde kan ook als een zwevende waarde worden doorgegeven. Deze waarde wordt opgeslagen in de JSON-webtoken die wordt gemaakt in de tijdperk UNIX. |
| displayName | Tekenreeks *required* | Tekst om deze gebruiker te identificeren in de gebruikersinterface en in opmerkingen. (Maximum aantal tekens: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>De sleutels van het netwerk worden niet gedeeld voor Livefyre demosite rekeningen. U ontvangt een netwerksleutel zodra LiveCycle een omgeving voor u heeft ingericht. Deze sleutel moet privé blijven.

