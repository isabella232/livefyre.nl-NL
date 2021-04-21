---
description: Telt het aantal gekrulde sociale items.
title: Sociale teller
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Sociale teller{#social-counter}

Telt het aantal gekrulde sociale items. Zie de sectie Live [API Reference](https://api.livefyre.com/docs) voor een volledige lijst met beschikbare eindpunten.

De sociale tegendeel API retourneert tellingen voor overeenkomende curatieregels in een bepaalde verzameling voor intervallen over een bepaalde periode.

>[!NOTE]
>
>Deze API is alleen beschikbaar voor Twitter-hashtags.

API voor sociale telfunctie:

* Resource
* Regeltypen
* Antwoord

## Bron {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** Uw Leven verstrekte netwerknaam. Bijvoorbeeld: *labs* in `labs.fyre.co`.
* **query:** De URL-safe base64 gecodeerde hash van alle site, artikel-id, regeltype tuples waarvoor de telinformatie moet worden opgehaald (vooraf gecodeerd)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >De vraag is beperkt tot 10 plaats, artikel identiteitskaart, regel-type leerprogramma&#39;s. (Het vorige voorbeeld zou 3 tuples bevatten.)

* **geeft de relatieve of absolute tijdsperiode** `(optional)` aan de grafiek aan; van geeft het begin aan en de standaardinstellingen zijn 24 uur geleden, indien weggelaten.
* **geeft** `(optional)` niet de relatieve of absolute tijdsperiode aan voor de grafiek; totdat het begin wordt opgegeven en standaard wordt ingesteld op de huidige tijd (nu), indien weggelaten.

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

U kunt als volgt tellingen verkrijgen over de laatste minuut voor site `123456` en artikel-id `some-article-id` en regeltype `2`, bijvoorbeeld: `123456:some-article-id;2:`

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
