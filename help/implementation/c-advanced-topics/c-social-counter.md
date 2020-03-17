---
description: Telt het aantal gekrulde sociale items.
seo-description: Telt het aantal gekrulde sociale items.
seo-title: Sociale teller
solution: Experience Manager
title: Sociale teller
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sociale teller{#social-counter}

Telt het aantal gekrulde sociale items. Voor een volledige lijst met beschikbare eindpunten raadpleegt u de sectie LiveCyre [API-naslaggids](https://api.livefyre.com/docs) .

De sociale tegendeel API retourneert tellingen voor overeenkomende curatieregels in een bepaalde verzameling voor intervallen over een bepaalde periode.

>[!NOTE]
>
>Deze API is alleen beschikbaar voor Twitter-hashtags.

API voor sociale telfunctie:

* Resource
* Regeltypen
* Antwoord

## Resource {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** Uw door Livefyre opgegeven netwerknaam. Bijvoorbeeld: *labs* in `labs.fyre.co`.
* **query:** De url-veilige base64 gecodeerde knoeiboel van alle plaats, artikel identiteitskaart, regel-type tuples waarvoor tellingsinformatie zou moeten worden gehaald (vooraf gecodeerd)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >De vraag is beperkt tot 10 plaats, artikel identiteitskaart, regel-type leerprogramma&#39;s. (Het vorige voorbeeld zou 3 tuples bevatten.)

* **van** `(optional)` de relatieve of absolute tijdsperiode tot de grafiek; van geeft het begin aan en de standaardinstellingen zijn 24 uur geleden, indien weggelaten.
* **tot** `(optional)` de relatieve of absolute tijdsperiode voor de grafiek wordt aangegeven; totdat het begin wordt opgegeven en standaard wordt ingesteld op de huidige tijd (nu), indien weggelaten.

### Relatieve tijd

| Afkorting | Eenheid |
|---|---|
| s | Seconden |
| min | Minuten |
| h | Uren |
| d | Dagen |
| w | Weken |
| molen | 30 dagen (maand) |
| y | 365 dagen (jaar) |

Voorbeeld:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Absolute tijd {#section_xqr_jgc_11b}

INDELING: HH:MM_JJJJMMDD

| Afkorting | Betekenis |
|---|---|
| HH | Uren (in 24u klokformaat) |
| MM | Minuten |
| JJJJ | Jaar met vier cijfers |
| MM | Maand |
| DD | Dag |

Voorbeeld:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Regeltypen {#section_v53_xqb_11b}

| Waarde | Type |
|---|---|
| 2 | Twitter |

Voorbeeld:

Om tellingen over de laatste minuut voor plaats `123456` en artikel identiteitskaart `some-article-id` en regel-type `2`, bijvoorbeeld te verkrijgen: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Voorbeeld van reactie:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
