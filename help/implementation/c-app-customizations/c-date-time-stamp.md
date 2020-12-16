---
description: Pas datum- en tijdstempels aan met Livefyre.js.
seo-description: Pas datum- en tijdstempels aan met Livefyre.js.
seo-title: De datum- en tijdstempel aanpassen
solution: Experience Manager
title: De datum- en tijdstempel aanpassen
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# De datum- en tijdstempel aanpassen{#customize-the-date-and-time-stamp}

Pas datum- en tijdstempels aan met Livefyre.js.

LiveCycle Apps biedt de parameter option, datetimeFormat, waarmee u de datumnotatie kunt opgeven zoals hieronder wordt beschreven.

* [Terminologie](#c_date_time_stamp/section_xsk_jn4_xz)
* [Opmaak](#c_date_time_stamp/section_ynx_gn4_xz)
* [Symboolaanduiding](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologie {#section_xsk_jn4_xz}

* **Absolute** tijdstempels worden gedefinieerd als exacte en specifieke tijden (bijvoorbeeld 1 januari 2012, 12:00pm)
* **Relatieve** tijdstempels worden gedefinieerd als algemene en minder precieze tijden (bijvoorbeeld 25 seconden geleden, 14 minuten geleden, 1 dag geleden, 1 jaar geleden, enz.)

## Opmaak {#section_ynx_gn4_xz}

De parameter datetimeFormat heeft het volgende standaardgedrag wanneer geen argument wordt gegeven:

* Datumtijdnotatie van: d MMMM yyyy (voor 8 januari 2012)
* 20160 Minuten (14 dagen) tot absolute tijd (14 dagen tot relatieve tijdstempels absolute tijdstempels worden)

De parameter datetimeFormat accepteert drie mogelijke argumenttypen: datetime, format en string.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Een object dat absoluteFormat en/of minutesUntilAbsoluteTime opgeeft. A minutesUntilAbsoluteTime met een waarde van -1 zal de tijd absolute tijd onmiddellijk maken.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Een functie die als argument een voorwerp van de Datum neemt en een datetime koord terugkeert dat moet worden getoond

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Symboolaanduiding {#section_inq_2n4_xz}

De opmaakfuncties van de datumtijd die de patroonspecificatie volgen zoals die in JDK, ICU en CLDR wordt bepaald, met kleine wijziging voor typisch gebruik in JS. Zie de [Google Closure Library Documentation](https://developers.google.com/closure/library/docs/overview) voor meer informatie.

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Items met een ‘*’ worden nog niet ondersteund.

Objecten die zijn gemarkeerd met ‘#’, werken anders dan Java.

De notatie wordt bepaald door het aantal patroonletters.

* **Tekst:** 4 of meer, volledige vorm gebruiken. Minder dan 4, gebruik korte of afgekorte vorm als het bestaat. (Bijvoorbeeld: &quot;EEEE&quot; produceert &quot;maandag&quot;, &quot;EEE&quot; produceert &quot;maan&quot;.)
* **Getal:** het minimum aantal cijfers. Kortere getallen worden met nul opgevuld (bijvoorbeeld: Als &quot;m&quot; &quot;6&quot; produceert, produceert &quot;mm&quot; &quot;06&quot;.) Het jaar wordt speciaal afgehandeld; Wanneer het aantal &quot;y&quot; 2 is, wordt het jaar ingekort tot 2 cijfers. (Bijvoorbeeld: als &quot;yyyy&quot; &quot;1997&quot; produceert, produceert &quot;yy&quot; &quot;97&quot;.) In tegenstelling tot andere velden worden fractionele seconden rechts met nul opgevuld.
* **Tekst en nummer:** 3 of hoger, gebruik tekst. Minder dan 3, gebruik aantal. (Bijvoorbeeld: &quot;M&quot; produceert &quot;1&quot;, &quot;MM&quot; produceert &quot;01&quot;, &quot;MMM&quot; produceert &quot;Jan&quot; en &quot;MMMM&quot; produceert &quot;Januari&quot;.)

Tekens in het patroon die niet binnen het bereik van [&quot;a&quot; vallen.&quot;z&quot;] en [&quot;A&quot;.&quot;Z’] wordt behandeld als geciteerde tekst. Tekens als &#39;:&#39;, &#39;.&#39;, &#39;, &#39;#&#39; en &#39;@&#39; worden bijvoorbeeld in de resulterende tekst weergegeven, ook al worden ze niet binnen enkele aanhalingstekens geplaatst.
