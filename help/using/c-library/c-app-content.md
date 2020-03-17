---
description: Inhoud beheren in uw LiveCycle-netwerk.
seo-description: Inhoud beheren in uw LiveCycle-netwerk.
seo-title: Tabblad App-inhoud
solution: Experience Manager
title: Tabblad App-inhoud
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Tabblad App-inhoud{#app-content-tab}

Inhoud beheren in uw LiveCycle-netwerk.

Op het tabblad App Content in uw bibliotheek kunt u zoeken naar inhoud die in uw apps is gepubliceerd en deze inhoud modereren. Op het **[!UICONTROL App Content]** tabblad vindt u verschillende zoekfilters met zoekopdrachten met jokertekens, zodat u sneller en gemakkelijker zoekparameters kunt definiëren.

Gebruik het tabblad App Content om:

* Inhoud zoeken
* Inhoudsgeschiedenis weergeven
* Moderne inhoud
* Een tag toevoegen
* Inhoud onderdeel
* Inhoud koppelen aan producten uit de productcatalogus

Zie voor meer informatie over het verkleinen van inhoud via het tabblad App Content [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Zoeken met jokertekens {#section_jvr_ntm_zz}

Live zoekvelden ondersteunen jokertekens, waarmee u een sterretje ( * ) aan woorden (of woordfragmenten) kunt toevoegen om gedeeltelijke overeenkomsten af te vangen.

Bijvoorbeeld:

* ball geeft alleen ball
* ball* geeft bal en ballon
* *ball retourneert bal en voetbal
* *ball* geeft bal en uniball en sneeuwballon

## Inhoud zoeken {#section_fw1_mtm_zz}

In het deelvenster App Content kunt u uw zoekopdracht beperken met behulp van verschillende filteropties voor inhoud.

![](assets/PublishedState-1024x367.png)

Gebruik de **[!UICONTROL Quick Filters]** keuzelijst om geretourneerde inhoud te beperken tot **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** of **[!UICONTROL Rights Requests]** status. Selecteer vervolgens een **[!UICONTROL Filter by]** optie en gebruik de selectievakjes of invoervelden die beschikbaar zijn om uw zoekopdracht te verfijnen.

Gebruik het keuzemenu om de inhoud in de lijst te sorteren op **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** of **[!UICONTROL Most liked]**.

## Filteren op opties {#section_aqn_xqm_zz}

Gebruik de **[!UICONTROL Filter by]** balk om met de volgende opties te filteren:

* **Staat** staat u toe om door de huidige moderatiestatus van de inhoud te filtreren:** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, of **[!UICONTROL Bozo]**.

* **Bron** Hiermee kunt u filteren op de bron van de inhoud. Selecteer deze optie **[!UICONTROL Livefyre]** om door de gebruiker gegenereerde inhoud weer te geven die rechtstreeks in de stream wordt geplaatst. Selecteer **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** of **[!UICONTROL RSS]** om inhoud op te nemen die vanuit deze bronnen in uw apps is opgehaald.

* **Met vlaggen** die vlaggen selecteren, kunt u filteren op **[!UICONTROL User Flags]** (Spam, Off-topic, Aanvallend of Niet akkoord), **[!UICONTROL System Flags]** toegepast door SAFE (Rendheid, Spam of Magisch GEMatificeerd), of **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Datum/tijd** Hiermee kunt u filteren op het tijdstip waarop de inhoud oorspronkelijk was **[!UICONTROL Created]** (of via SocialSync of een stream in de app werd gehaald) of op het laatste tijdstip **[!UICONTROL Modified]** (bewerkt, gemarkeerd of de gewijzigde status).

* **Met Auteur** kunt u filteren op het **[!UICONTROL IP]** adres van de auteur, **[!UICONTROL Display Name]** (in het deelvenster Gebruikers of boven de inhoud die door de auteur is gepost) of **[!UICONTROL User ID]**(in het deelvenster Gebruikers).

* **Bevat** Hiermee kunt u de meest recente 90 dagen met inhoud filteren op **[!UICONTROL Keyword]** of **[!UICONTROL Content Tag]**. Schakel het **[!UICONTROL Media]** selectievakje in om alleen inhoud met Media te retourneren. (Als u naar alle inhoud wilt zoeken, schuift u omlaag door alle inhoud in de lijst en klikt u op **[!UICONTROL Search full data]**.)

   **Opmerking:** Het zoeken naar meerdere trefwoorden en inhoudscodes wordt niet ondersteund. Als er meerdere trefwoorden of tags zijn ingevoerd, wordt het laatste woord gebruikt voor de zoekopdracht.

   Als u op Inhoud-tag zoekt, worden voorgestelde tags automatisch ingevuld wanneer u in het zoekveld typt. De zoekresultaten retourneren alle inhoud waaraan ooit de tag is toegewezen. (Gebruik dit veld om te zoeken naar aanbevolen inhoud of klik op het **[!UICONTROL Featured]** label van aanbevolen inhoud in Studio.)

   **Opmerking:** Gebruik een minteken (-) vóór een labelnaam om te zoeken naar inhoud die die tag niet bevat. Bijvoorbeeld: Zoek naar &#39;-Miley&#39; om naar alle inhoud te zoeken die niet de &quot;Miley&quot;-tag bevat.

* **Met de app** kunt u filteren op **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** of **bovenliggende id**. Filteren op bovenliggende id retourneert alle inhoud die een antwoord is op de invoer-inhoud-id. (Filteren op meerdere tags door tags in te voeren die worden gescheiden door een komma.)

* **Rechten** Hiermee kunt u filteren op de status Rechtenverzoeken:** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]** of **[!UICONTROL Expired]**.

## Bozo-inhoud {#section_afl_vqm_zz}

In Apps, wordt de **[!UICONTROL Bozo]** inhoud getoond slechts aan de auteur van de inhoud. Hierdoor kan de gebruiker geloven dat de inhoud ervan is goedgekeurd, terwijl deze voor alle andere gebruikers en moderatoren wordt verborgen.

>[!NOTE]
>
>Sociale inhoud die afkomstig is van SocialSync of Streams **[!UICONTROL cannot]** wordt ingesteld op Bozo.

U kunt Bozo-inhoud om de volgende redenen gebruiken:

* Inhoud die door SAFE als spam wordt aangeduid, wordt automatisch ingesteld op de status Bozo.
* Alle inhoud van Verboden gebruikers wordt automatisch ingesteld op Bozo.
* Inhoud kan van Studio Bozo worden gemarkeerd.
* Moderatoren kunnen Bozo-inhoud rechtstreeks in de stream opnemen.

## Inhoudsgeschiedenis weergeven {#section_ayz_tqm_zz}

Met het deelvenster Inhoud kunt u de geschiedenis van alle vermelde inhoud controleren, inclusief voormatiging, spamfiltering, postdatum en eventuele gebruikersmarkeringen of notities die aan het item zijn toegewezen.

Met de tabbladen onder aan het inhoudspaneel kunt u de historie van het deelvenster weergeven.

* **[!UICONTROL More Info:]** geeft een lijst weer van alle activiteit op deze inhoud, met inbegrip van voorlegging, het uitgeven, spamcontrole, staatsverandering, en nota&#39;s. De livefyre Inhoud identiteitskaart en het IP van de gebruiker adres worden ook getoond in deze sectie.
* **[!UICONTROL Replies:]** bevat maximaal zes reacties. Klik **[!UICONTROL Show all replies]** om alle reacties op de advertentie weer te geven.

* **[!UICONTROL Flags & Reports:]** bevat een lijst met alle vlaggen van gebruikers, met de avatar van de gebruiker die de inhoud heeft gemarkeerd, en eventuele rapporten (notities die door de gebruiker zijn toegevoegd bij het markeren van de inhoud).
* **[!UICONTROL Add a note:]** staat u toe om een nota toe te voegen, zichtbaar aan andere Admins of Moderators.
* **[!UICONTROL Request Rights:]** Hiermee opent u het **[!UICONTROL New Rights Request]** dialoogvenster waarin een aanvraag voor rechten kan worden ingediend.

* **[!UICONTROL Save as Asset:]**opent het **[!UICONTROL Advanced Options]** dialoogvenster waarin u het geselecteerde item kunt opslaan in de bibliotheek met middelen, het item kunt publiceren naar een app of hergebruiksrechten van de auteur kunt aanvragen.

![](assets/PublishedMoreInfo-1024x462.png)

## Een label toevoegen aan inhoud {#section_xb4_mxr_rdb}

Door de inhoud te labelen kunt u de inhoud indelen en ordenen, zodat u deze eenvoudig kunt ophalen en opmaken, of de inhoud kunt markeren zoals deze is aanbevolen.

Als u tags wilt toevoegen, klikt u gewoon op de plusknop ( **[!UICONTROL +]**) onder inhoud. Voer een nieuwe tag in of selecteer een bestaande tag.

![](assets/PublishedAddTag-1024x338.png)

## Zoeken naar afbeeldingen in alle elementen {#section_zxf_hsf_wcb}

Nadat u de inhoud aan de bibliotheek hebt toegevoegd, kunt u de inhoud doorzoeken op slimme tags.

In de Bibliotheek, onder Alle Middelen, kunt u bestaande beelden zoeken door op te klikken **[!UICONTROL Show Filters]** en dan:

* Tekst invoeren om te zoeken in het zoekveld
* Sorteren op relevantie
* Tekst in het **[!UICONTROL Tags]** veld invoeren om te zoeken op slimme tags. Met het algoritme voor slimme tags wordt de inhoud gefilterd op basis van een vertrouwensscore voor slimme tags, hoe nieuw de inhoud is en hoeveel sterren een gebruiker de inhoud heeft gegeven.

## Aanbevolen inhoud {#section_emb_kqm_zz}

Selecteer het standaardlabel om de inhoud te markeren zoals deze is aanbevolen en markeer deze zo belangrijk voor uw gebruikers. **[!UICONTROL Featured]** Als u eenmaal labels hebt toegewezen, kunt u aangepaste opmaakopties gebruiken om aanbevolen inhoud in uw apps aan te passen.

## Inhoud van functie of functie opheffen {#section_ojx_3qm_zz}

* Klik in Studio op het **[!UICONTROL +]** teken naast een stuk inhoud, selecteer de **[!UICONTROL Featured]** tag in de vervolgkeuzelijst en klik **[!UICONTROL Enter]** op Feature-inhoud. De tag wordt opgeslagen en weergegeven naast de inhoud.

* Als u de functie wilt opheffen, klikt u op de code **[!UICONTROL x]** op de **[!UICONTROL Featured]** code die op het stuk inhoud wordt weergegeven.

* Vanuit de app Live Blog of Revisies kunt u vanuit een Opmerking de muisaanwijzer boven de inhoud plaatsen die u wilt gebruiken en op **[!UICONTROL Feature]** deze knop klikken. Houd de muisaanwijzer boven de inhoud en klik om de functie ongedaan te maken **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>Wegens ruimtebeperkingen, kan de inhoud van het Praatje slechts worden kenmerkt of onuitgerust gebruikend Studio, en kan niet van binnen App zelf worden voorzien.

## Aanbevolen inhoud bewerken {#section_pyw_hqm_zz}

De meeste gewone acties met betrekking tot inhoud kunnen worden uitgevoerd op aanbevolen inhoud, met uitzondering van:

* Aanbevolen inhoud kan niet worden gemarkeerd.
* Gebruikers kunnen hun inhoud na Topaanbieding niet bewerken, maar ze kunnen de inhoud desgewenst nog wel verwijderen. Moderatoren kunnen aanbevolen inhoud bewerken.

