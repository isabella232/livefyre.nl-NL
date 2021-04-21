---
description: Voer stresstests uit tegen het Livefyre-platform.
title: Testbeleid voor stress
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Testbeleid benadrukken{#stress-test-policy}

Voer stresstests uit tegen het Livefyre-platform.

In dit document worden richtsnoeren gegeven voor het uitvoeren van stresstests op het Livefyre-platform. Ad-hoctests door klanten zonder kennisgeving zijn strikt verboden. Voor meer informatie over [verboden en toegestane activiteiten](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstests zijn optioneel. U hoeft geen stresstest uit te voeren. Adobe Livefyre voert regelmatig stresstests en valideringen uit als onderdeel van het afgifteproces. Als u ervoor kiest om tests uit te voeren, worden in dit document de vereisten en beperkingen voor het uitvoeren van stresstests beschreven.

## Melding {#section_ihs_bfz_vdb}

U moet uw Livefyre-medewerker van de Successpecialist van het Succes van de Klant en van de Technische Adviseur van het Adobe van uw geplande tests drie of meer weken van tevoren op de hoogte brengen wanneer u van plan bent te beginnen.

Om Livefyre op de hoogte te brengen, dient u de volgende informatie in bij uw Livefyre Customer Success Specialist en Adobe Technical Consultant:

* Doel en beschrijving van de test
* Het gebruiksgeval waarop u test
* Lijst met alle Livefyre-API&#39;s die u in de test wilt gebruiken
* Datum, tijd en duur van de test
* IP adressen waarvan u de tests zult in werking stellen

## Vereisten {#section_khs_bfz_vdb}

U mag alleen tests uitvoeren als deze aan de volgende vereisten voldoen:

* Een technisch adviseur van Adobe moet u drie weken of langer expliciet en schriftelijk goedkeuren voordat u met de test begint.
* **U kunt tests op het Netwerk van de UAT slechts uitvoeren.**
* U moet uittesten tegen realistische scenario&#39;s. Bijvoorbeeld, kunt u niet veronderstellen dat uw bezit *miljoenen* van postverzoeken elke dag zal onderhouden, omdat dit geen realistisch scenario is. Als u hulp nodig hebt die bepaalt of uw scenario realistisch is of niet, vraag uw Specialist van het Succes van de Klant van Livefyre of de Technische Consultant van Adobe.
* Tests moeten worden uitgevoerd tijdens kantooruren voor de Pacific Standard Time Zone \(UTC -7\).
* U moet mogelijk gegevens en uw redenering voor de test overleggen.

## Bestuur {#section_mhs_bfz_vdb}

Livefyre behoudt zich het recht voor om een test op elk moment te beëindigen als u een test uitvoert:

* Op het Netwerk van de Productie.
* Zonder uitdrukkelijke schriftelijke toestemming van een technisch adviseur van Adobe drie weken of meer van tevoren.
* Tegen onechte scenario&#39;s.

Livefyre beëindigt tests door toegang tot APIs te blokkeren, de Netwerken van Livefyre onbruikbaar te maken, en een verzoek van de ladingstest te weigeren als het niet aan de vereisten voldoet.
