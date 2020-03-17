---
description: Retourneert een gecodeerde token voor gebruikersverificatie voor het netwerk waaruit de token wordt aangeroepen.
seo-description: Retourneert een gecodeerde token voor gebruikersverificatie voor het netwerk waaruit de token wordt aangeroepen.
seo-title: buildUserAuthToken Netwerkmethode
solution: Experience Manager
title: buildUserAuthToken Netwerkmethode
uuid: 8828d356-c3c6-46a6-91bf-83bd59e35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildUserAuthToken Netwerkmethode{#builduserauthtoken-network-method}

Retourneert een gecodeerde token voor gebruikersverificatie voor het netwerk waaruit de token wordt aangeroepen.

| Variabele | Type | Beschrijving |
|--- |--- |--- |
| userId | String | De gebruikersnaam voor de gebruiker tot wie dit token behoort. |
| displayName | String | De weergavenaam voor de gebruiker. |
| verloopt | Dubbel | Wanneer het token in seconden verloopt. |

## Java-voorbeeld {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Voorbeelduitvoer:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Voorbeeld van NodeJS {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Voorbeelduitvoer:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP-voorbeeld {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Voorbeelduitvoer:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Voorbeeld van Python {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Voorbeelduitvoer:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ruby-voorbeeld {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Voorbeelduitvoer:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
