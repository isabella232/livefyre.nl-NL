---
description: 'null'
seo-description: 'null'
seo-title: Filter Winst gebruiken
solution: Experience Manager
title: Filter Winst gebruiken
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Filter Winst gebruiken{#using-the-profanity-filter}

Alle inhoud die in een Livefyre-app wordt gepost, wordt op rijkdom gecontroleerd. Als een woord dat is opgenomen in de lijst met eigenschappen wordt gevonden in inhoud of in de weergavenaam van een gebruiker, wordt die inhoud gemarkeerd als &#39;Winstgevendheid&#39;, zodat u het kunt filteren op Voormatiging, Regels, ModQ of algemene zoekopdrachten in App Content.

>[!NOTE]
>
>De inhoud van de Beheerders van Studio en van Managers&#39; is niet onderworpen aan de controle van de Regel van de Winst, en de inhoud die door een Moderator wordt gepost zal niet worden gemarkeerd.

Livefyre biedt een standaardwoekerlijst. U kunt verkiezen om deze lijst op het netwerkniveau toe te passen, uw eigen lijst te verstrekken, of een totaal van twee te gebruiken. De individuele plaatsen binnen uw netwerk kunnen de lijst van de netwerkwinst erven, of een lijst gebruiken die wordt aangepast om plaats-specifiek te zijn.

Om uw eigen lijst van de douanerijkdom als uw netwerkgebrek te verstrekken, te verzenden gelieve het aan uw Livefyre rekeningsmanager.

## Profiteer van het filteren van winsten {#section_yqc_qsk_f1b}

Laat en vorm de dieptefilter op zowel het netwerk als plaatsenniveau toe. Schakel het dieptefilter op het netwerkniveau uit om het dieptefilter voor alle sites die van het netwerk overerven automatisch uit te schakelen.

>[!NOTE]
>
>Alle inhoud die door Livefyre wordt doorgegeven, wordt gecontroleerd op willekeur. Als er inhoud wordt gevonden die woorden bevat die voorkomen in de standaardlijst met SAFE-profielen of in uw lijst met aangepaste profielen, wordt deze gemarkeerd als &#39;Winst&#39;. Als u LiveCycle wilt instellen om automatisch actie te ondernemen met betrekking tot deze items, gaat u **[!UICONTROL Enable Profanity Checking]** naar **[!UICONTROL ON]**.

## Laat de Filter van de Winst voor een Netwerk toe {#section_twd_ssk_f1b}

1. Selecteer **[!UICONTROL Network]** uit het keuzemenu van het netwerk.
1. Ga naar **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Schuif omlaag naar de map **[!UICONTROL Profanity List]** en stel **[!UICONTROL Enable Profanity Checking]** deze in op **[!UICONTROL ON]**.

1. Gebruik het **[!UICONTROL Update Network Profanity List]** veld om woorden aan de lijst toe te voegen of klik op een woord om het uit de lijst te verwijderen.

>[!NOTE]
>
>Het uitgeven van de Lijst van de Winstgevendheid van het netwerkniveau zal geen plaats-vlakke Lijsten beïnvloeden die reeds op zijn plaats zijn. Om ervoor te zorgen dat de veranderingen van het netwerk aan de plaats worden aangebracht, selecteer **[!UICONTROL Restore Network List]** voor de plaats nadat de veranderingen zijn aangebracht.

## Het filter Winstgevendheid voor een site inschakelen {#section_fld_wsk_f1b}

1. Selecteer de site in het keuzemenu van het netwerk.
1. Ga naar **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Schuif omlaag naar de map **[!UICONTROL Profanity List]** en stel deze in **[!UICONTROL Enable Profanity Checking]** op **[!UICONTROL ON]**.

1. Kies een van de volgende opties:

   * Om de Lijst van de Winst van het netwerk (dit is niet gemeenschappelijk) over te erven, reeks **[!UICONTROL Use Site Profanity List]** aan **[!UICONTROL OFF]**.

   * Als u de lijst met percentages specifiek voor de site wilt bewerken, opent u **[!UICONTROL Use Site Profanity List]** het **[!UICONTROL On]** veld **[!UICONTROL Update Profanity List]** waarin u de lijst kunt bewerken:

      * Als u een woord wilt verwijderen, klikt u op het woord.
      * Als u een woord wilt toevoegen, typt u het woord in het **[!UICONTROL Add new word]** vak en klikt u op **[!UICONTROL Return]**.

      * Als u wilt zien of een woord is opgenomen in de lijst, typt u het woord in het **[!UICONTROL Test profanity filter]** vak.
   * Om de lijst van de netwerkwinst opnieuw in te voeren en het op de plaats toe te passen, klik **[!UICONTROL Restore Network List]**.
   * Als u alle inhoud uit de lijst wilt verwijderen en opnieuw wilt beginnen, klikt u op **[!UICONTROL Clear List]**.


## Werken met inhoud die winstgevendheid bevat {#section_epy_dtk_f1b}

Gebruik de Lijst van de Winstgevendheid helpen uw inhoudsonderzoeken filtreren en de Regels van de Premoderatie voor ModQ tot stand brengen.

Als u wilt zoeken naar inhoud met diepte, gaat u naar **[!UICONTROL Library > App Content]** en schakelt u het **[!UICONTROL Filter by Flags]** **[!UICONTROL Profanity]** selectievakje in. Alle inhoud die is afgevangen door het filter Winstgevendheid voor de geselecteerde site of het geselecteerde netwerk, wordt weergegeven. Deze lijst bevat inhoud die met sociale synchronisatie en streams in de app is geplaatst.

Om de regels van de Premoderatie tot stand te brengen, van Studio uitgezocht **[!UICONTROL Settings > Network Settings > Moderation]**. Nadat het filter Schildbaarheid is ingeschakeld, wordt een nieuwe regel weergegeven, waarmee u inhoud met een vlag of een beperking met een diepte kunt markeren. Standaard schakelt deze regel automatisch **[!UICONTROL Premoderate]** voor profaaninhoud in. Deze kan worden gewijzigd in **[!UICONTROL Trash it]** of **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Als één stuk van inhoud aan veelvoudige regeltypes (zoals zowel VEILIGE als de regels van de Vlag) onderworpen is, zal strenger worden toegepast. Bijvoorbeeld: Als uw regel van Premoderatie zegt om een stuk inhoud te premodereren, maar een VEILIGE Regel zegt aan het Afvoeren van het, zal het worden afgevoerd.

## Bekijk en werk de Lijst van de Winstgevendheid voor een Netwerk bij {#section_qdb_btk_f1b}

1. Ga naar **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Schuif omlaag naar de **[!UICONTROL Profanity List]** sectie.
1. Stel deze optie in **[!UICONTROL Enable Profanity Checking]** **[!UICONTROL On]** om de lijst weer te geven die voor uw netwerk is ingeschakeld (standaard LiveCycle of uw geüploade aangepaste lijst) en bewerk deze lijst. U kunt de lijst op de volgende manieren bewerken:
   * Als u een woord wilt verwijderen, klikt u op het woord.
   * Als u een woord wilt toevoegen, typt u het woord in het **[!UICONTROL Add new word]** vak en klikt u op **[!UICONTROL Return]**.
   * Als u wilt zien of een woord is opgenomen in de lijst, typt u het woord in het **[!UICONTROL Test profanity filter]** vak.

>[!NOTE]
>
>Slechts kunnen de Beheerders van Studio en de Moderatoren van de Studio Rentelijsten uitgeven.
