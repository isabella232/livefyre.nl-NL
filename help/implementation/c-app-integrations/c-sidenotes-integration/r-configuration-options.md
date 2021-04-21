---
description: Het Sidenotes config-object is een JSON-object dat wordt gebruikt om de inhoud op te geven die de Livefyre App op de pagina rendert.
title: Opties voor Sidenotes-configuratie
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Sidenotes configuratieopties{#sidenotes-configuration-options}

Het Sidenotes config-object is een JSON-object dat wordt gebruikt om de inhoud op te geven die de Livefyre App op de pagina rendert.

Het object bevat de volgende parameters:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| authDelegate | ** requiredobject | Nieuwe of oude stijl geïnitialiseerde authentificatieafgevaardigde. |
| collectionMeta | ** requiredobject | Zie collectionMeta token voor meer informatie. |
| customIcon | ** optionele tekenreeks | Hiermee stelt u de URL in van een aangepast startpictogram. Standaard wordt er een Livefyre bubble ingesteld. |
| customStyles | ** optioneel object | Hiermee voegt u aangepaste stijlen toe om de vormgeving van Sidenotes te wijzigen. Zie Aangepaste stijlen voor meer informatie. |
| disableStream | ** optionalBoolean | Indien waar (true), wordt streaming in realtime uitgeschakeld in deze instantie Sidenotes (niet in andere commentaarstreams). De standaardwaarde is false. |
| milieu | ** optionele tekenreeks | Geeft de UAT-omgeving van Livefyre aan. De enige mogelijke waarde is `t402.livefyre.com`. Voor de productie moet deze parameter worden verwijderd. |
| iconVisibility | *Optioneel object of* optionele tekenreeks | Bepaalt of het pictogram van Duidelijkheden bij aanwijzen of statisch zichtbaar zal zijn. Als dit een tekenreeks is, wordt deze gebruikt voor beide versies van het blokpictogram (leeg en heeft Sidenotes). Wanneer een object is, moet u elk type opgeven: {leeg: &quot;hover&quot;, num: &quot;static&quot;}. Standaard is dit statisch. |
| inlineThreads | ** optionalboolean | Indien waar, worden de draden van Sidenote direct opgenomen na het blok waaraan zij worden geassocieerd. De standaardwaarde is false. |
| numSidenotesEl | *Optioneel* object, tekenreeks of array | Hiermee wordt opgegeven welk element door de widget voor het tellen van identificaties wordt gedecoreerd. (Deze widget toont het aantal voorzitterschappen op de pagina en informatie over Sidenotes.) Als de tekenreekskiezer overeenkomt met meerdere elementen, wordt de eerste gekozen. (Gebruikt CSS3 DOM-selectiespecificatie.) |
| position | ** optionele tekenreeks | Hiermee bepaalt u de positie van de pop-up wanneer op een element wordt geklikt waarvoor Sidenotes is ingeschakeld. Mogelijke waarden zijn &quot;smart&quot;, &quot;left&quot;, &quot;right&quot; en &quot;bottom&quot;. De standaardinstelling is ‘slim’. Hiermee wordt de pop-up rechts van de pagina uitgelijnd, tenzij er onvoldoende ruimte is (in dat geval wordt de pop-up naar onder de inhoud verplaatst). |
| kiezers | ** requiredobject, string of array | Hiermee geeft u de elementen op waarop de opstartpictogrammen moeten worden weergegeven. (Gebruikt CSS3 DOM-selectiespecificatie.) Als het object een include-sectie en een uitsluitingssectie bevat die de CSS-kiezer voor alle overeenkomende include-bestanden toepassen, en alle elementen die overeenkomen met de uitsluitingen verwijderen. Als de tekenreeks overeenkomt, worden alle overeenkomende elementen op de pagina opgenomen. Als array, worden de elementen weergegeven die moeten worden opgenomen. |
| tekenreeksen | ** optioneel object | Voegt aangepaste tekstreeksen toe om een taal of tekst in de hele toepassing te wijzigen. Zie Aangepaste strings voor meer informatie. |
| threadContainerEl | *Optioneel* object, tekenreeks of array | Geeft een element aan waar de verbinding van de voorzitterschappen wordt weergegeven. Met deze parameter kunt u de verbinding verplaatsen. Als de tekenreekskiezer overeenkomt met meerdere elementen, wordt de eerste gekozen. (Gebruikt CSS3 DOM-selectiespecificatie.) |
