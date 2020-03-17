---
description: Voer stresstests uit tegen het Livefyre-platform.
seo-description: Voer stresstests uit tegen het Livefyre-platform.
seo-title: Testbeleid voor stress
solution: Experience Manager
title: Testbeleid voor stress
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Testbeleid voor stress{#stress-test-policy}

Voer stresstests uit tegen het Livefyre-platform.

In dit document worden richtsnoeren gegeven voor het uitvoeren van stresstests op het Livefyre-platform. Ad-hoctests door klanten zonder kennisgeving zijn strikt verboden. Meer over [verboden en toegestane activiteiten](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstests zijn optioneel. U hoeft geen stresstest uit te voeren. Adobe Live voert als onderdeel van het releaseproces regelmatig stresstests en -validaties uit. Als u ervoor kiest om tests uit te voeren, worden in dit document de vereisten en beperkingen voor het uitvoeren van stresstests beschreven.

## Melding {#section_ihs_bfz_vdb}

U moet uw Livefyre-specialist voor succes van de Klant en Adobe Technical Consultant drie of meer weken van tevoren op de hoogte stellen van uw geplande tests wanneer u van plan bent te starten.

Als u Livefyre op de hoogte wilt brengen, stuurt u de volgende informatie naar uw Livefyre Customer Success Specialist en Adobe Technical Consultant:

* Doel en beschrijving van de test
* Het gebruiksgeval waarop u test
* Lijst met alle Livefyre-API&#39;s die u in de test wilt gebruiken
* Datum, tijd en duur van de test
* IP adressen waarvan u de tests zult in werking stellen

## Vereisten {#section_khs_bfz_vdb}

U mag alleen tests uitvoeren als deze aan de volgende vereisten voldoen:

* Een technische consultant van Adobe moet u drie weken of langer expliciet en schriftelijk goedkeuren voordat u met de test begint.
* **U kunt tests op het Netwerk van de UAT slechts uitvoeren.**
* U moet uittesten tegen realistische scenario&#39;s. Bijvoorbeeld, kunt u niet veronderstellen dat uw bezit *miljoenen* postverzoeken elke dag zal onderhouden, omdat dit geen realistisch scenario is. Als u hulp nodig hebt om te bepalen of uw scenario realistisch is of niet, vraag uw Specialist van het Succes van de Klant van Livefyre of de Technische Consultant van Adobe.
* Tests moeten worden uitgevoerd tijdens kantooruren voor de Pacific Standard Time Zone \(UTC -7\).
* U moet mogelijk gegevens en uw redenering voor de test overleggen.

## Bestuur {#section_mhs_bfz_vdb}

Livefyre behoudt zich het recht voor om een test op elk moment te beëindigen als u een test uitvoert:

* Op het Netwerk van de Productie.
* Zonder expliciete, schriftelijke goedkeuring van een technische consultant van Adobe drie weken of meer van tevoren.
* Tegen onechte scenario&#39;s.

Livefyre beëindigt tests door toegang tot APIs te blokkeren, de Netwerken van Livefyre onbruikbaar te maken, en een verzoek van de ladingstest te weigeren als het niet aan de vereisten voldoet.
