---
description: Met vertaalsets kunt u een alternatieve taal opgeven voor Apps.
title: Vertaalsets
exl-id: 1de99602-b97e-42e9-8450-39abd4ba2f9b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# Vertaalsets{#translation-sets}

Met vertaalsets kunt u een alternatieve taal opgeven voor Apps.

Gebruik vertaalinstellingen om apps in verschillende talen te lokaliseren of om alternatieve tekst voor verschillende apps vanaf één locatie in Studio op te geven. U kunt er bijvoorbeeld voor zorgen dat alle sites in het Spaans de Spaanse taal gebruiken voor alle App-velden. U kunt de tekst ook wijzigen zodat alle velden overeenkomen met de stem en het gevoel van uw site of netwerk.

U kunt vertaalinstellingen opgeven voor alle apps, behalve Storify 2. Zie [Tekenreeksen lokaliseren](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings) voor meer informatie over welke velden u kunt lokaliseren.

Opmerkingen, Live Blog en Chat delen dezelfde set tekenreeksen binnen een vertaalset.

Geef een vertaalset op voor een netwerk, site, app of API.

De vertaalsets op verschillende niveaus overschrijven elkaar als volgt:

API-vertaalset overschrijft alle vertaalsets op elk niveau (app, netwerk en site)
De vertaalreeks van de toepassing treedt netwerk-vlakke en plaats-vlakke vertaalreeksen met voeten.
Vertaalsets op siteniveau overschrijven de vertaalsets op netwerkniveau.

## Tekstreeksen {#c_review_text_strings} controleren

De tekstreeksen aanpassen voor LiveRevisies.

Deze pagina bevat een overzicht en beschrijving van de tekenreeksen die beschikbaar zijn voor aanpassing in revisie-apps. De hier vermelde tekenreeksen komen bovenop en overschrijven voor de standaardtekenreeksen voor LiveCycle-kerntoepassingen, die worden vermeld in String Customizations. Waar duplicaten worden vermeld, zijn de tekenreeksen in deze tabellen de standaardinstelling voor revisieapps.

Implementatie
Revisie-/beoordelingsinterface
Stream-info
Informatie auteur/inhoud
Handelingen van gebruikers
Functies
Fouten

## Implementatie {#section-vsy-1k4-xz}

Als u deze functie wilt implementeren, geeft u een 1-1-objecttoewijzing van de tekenreeksen die u wilt overschrijven, door aan het Javascript-configuratieobject. Als u geen veld opgeeft, wordt de standaardtekst gebruikt.

Voorbeeld:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Revisie-/beoordelingsinterface {#section_iyv_zj4_xz}

Tekenreeksen beschikbaar voor de gebruikersinterface voor revisie en beoordeling.

| Element | Sleutel | Standaardtekst |
|--- |--- |--- |
| Knoppen | editReviewBtn | Revisie bewerken |
|  | reviewBtn | Revisie schrijven |
|  | beoordelingenGesloten | Revisies gesloten |
|  | showReviewBtn | Revisie tonen |
|  | volgen | Ik ben geïnteresseerd |
|  | shareText | Ik schreef net een revisie. Kijk eens! |
| Knopinfo voor classificaties | ratingValues | Een array. Standaard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Opmerking: Waarden in de array moeten worden gedupliceerd om aan de linker- en rechterhelft van elke ster dezelfde naam toe te wijzen. |
| Onderdelen van classificaties | ratingSubpartPlaceholders | Een array. Standaard = [] |
|  | ratingSubpartTitles | Een array. Standaard = [] |
|  | reviewStreamTitle | Standaard leeg. Titel van de samenvatting van de evaluatie. |
| Dic | averageRating | Gemiddelde beoordeling door gebruiker |
|  | breakHeader | Classificatie-indeling |
|  | nuttig | %s van %s is nuttig gevonden |
|  | NuttigePlural | %s van %s is nuttig gevonden |
|  | outOf | / |
|  | ratingType | ster |

## Stream-info {#section_wmv_yj4_xz}

Tekenreeksen beschikbaar voor informatie en weergave van de inhoudsstroom.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Sorteren | sortBy | *Standaard leeg.* |
|  | sortHighestRated | [Hoogste beoordeling](https://d.pr/i/huTd) |
|  | sortLowestRated | [Laagste classificatie](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Meeste handigheid](https://d.pr/i/huTd) |
| Stream misc. | showMore | Meer weergeven |
| Hoge snelheid streamen | newComment | Nieuwe revisie |
|  | newComments | Nieuwe revisies |
| Aantal listeners | listenerCount | persoon die luistert |
|  | listenerCountPlural | mensen luisteren |
| Aantal opmerkingen | commentCountLabel | LiveRevisies<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveRevisies<strong> | </strong>%s |
| Telling van opmerkingenkennisgever | commentNotifier | Nieuwe revisie |
|  | commentNotifierPlural | Nieuwe revisies |

## Info auteur/inhoud {#section_osx_xj4_xz}

Stings beschikbaar voor auteur en individuele inhoudsinformatie.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Doorbraak van thread | reviewsContentNotFoundMsg | [Deze revisie is niet meer zichtbaar](https://d.pr/i/svXs) |
|  | backToComments | Terug naar Revisies |

## Gebruikershandelingen {#section_tlx_wj4_xz}

Tekenreeksen beschikbaar voor gebruikersacties: bestaande inhoud toewijzen, delen en markeren als handig.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Voettekst voor opmerkingen | wasReviewHelpful | [Nuttig?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Nuttig? |
|  | ownIsReviewHelpful | [Gevonden nuttig.](https://d.pr/i/Q0mA) |
|  | reviewIsHelpful | [Ja](https://d.pr/i/Q0mA) |
|  | NuttigeScheider | [&amp;Omkeren;](https://d.pr/i/Q0mA) |
|  | reviewIsNotHelpful | [Nee](https://d.pr/i/Q0mA) |
| Stemmen over modaal | voiceTitle | Was deze herziening nuttig? |
|  | stemmenDownloaden | Nee |
|  | voiceReplyTitle | Was dit antwoord nuttig? |
|  | voiceTitle | Was deze opmerking nuttig? |
|  | stemonthouding | Ja |
| Markering — modaal | flagTitle | Revisie van %s markeren |
|  | flagSuccessMsg | Revisie is gemarkeerd. |
| Markering mobiel | flagConfirmationMessage | Revisie van %s markeren als %s? |
| Meningmodaal | notifyDefaultText | Ik heb u in een Livefyre-revisie genoemd! |
| Delen, modaal | shareTitle | Revisie delen |

## Functies {#section_yl1_wj4_xz} plaatsen

Tekenreeksen beschikbaar voor gebruikers die revisies plaatsen.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Editor | bodyPlaceholder | Revisie schrijven... |
|  | postEditButton | Bewerken |
|  | postEditCancelButton | Annuleren |
|  | postAsButton | Herziening achteraf als... |
|  | postButton | Na revisie |
|  | postReplyAsButton | Plaatsen als... |
|  | postReplyButton | Post |
|  | shareButton | Delen |
|  | titlePlaceholder | Titel... |

## Fouten {#section_jbc_vj4_xz}

Tekenreeksen beschikbaar voor algemene foutberichten.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Fouten | errorAlreadyPosted | Je kunt slechts één revisie plaatsen. |
|  | errorAuthError | U bent niet bevoegd om een revisie op dit gesprek te plaatsen |
|  | errorCommentsNotAllowed | Revisies kunnen op dit moment niet worden gepost |
|  | errorDislikeOwnComment | Je kunt je eigen beoordeling niet opheffen |
|  | errorDuplicate | U mag de revisie niet tweemaal plaatsen, wat u ook leuk vindt. |
|  | errorEditDuplicate | U moet de hoofdtekst van de revisie wijzigen wanneer u de revisie bewerkt. |
|  | errorEditNotAllowed | U bent niet gemachtigd revisies op dit gesprek te bewerken. |
|  | errorEditTimeExceeded | De revisiebewerkingsperiode is verlopen. |
|  | errorEmpty | Het lijkt erop dat u een lege revisie wilt plaatsen. |
|  | errorEmptyTitle | Het lijkt erop dat u een lege titel wilt plaatsen |
|  | errorFieldRating | sterrenwaardering |
|  | errorFieldReview | revisie |
|  | errorFieldTitle | titel |
|  | errorMaxChars | Je beoordeling is te lang. Bewerk het bestand en probeer het opnieuw. |
|  | errorMissingFields | Voer een |
|  | errorRatingEmpty | Je kunt geen lege beoordeling verzenden |
|  | errorRatingNotSet | Alle classificaties moeten worden ingesteld |
|  | errorRatingNotValid | De classificatie moet een object zijn |
|  | errorShowMore | Er is een fout opgetreden bij het laden van meer revisies. |
|  | errorTitleMaxChars | Je titel is te lang. Bewerk het bestand en probeer het opnieuw. |
|  | errorStemOwnComment | Je kunt niet op je eigen beoordeling stemmen |

## Geeft tekstreeksen {#c_sidenotes_text_strings} aan

Teksttekenreeksen aanpassen voor LiveCycle Sidenotes

Deze pagina bevat een overzicht en beschrijving van alle tekenreeksen die beschikbaar zijn voor aanpassing in Sidenotes-apps. Zie Tekenreeksaanpassingen voor informatie over tekenreeksen die beschikbaar zijn voor de kerntoepassingen van LiveCycle.

Implementatie
Auth
Stream-info
Informatie auteur/inhoud
Handelingen van gebruikers
Functies
Moderatorinterface
Fouten

## Implementatie {#section_wp2_ql4_xz}

Als u deze functie wilt implementeren, geeft u een 1-1-objecttoewijzing van de tekenreeksen die u wilt overschrijven, door aan het Javascript-configuratieobject. Als u geen veld opgeeft, wordt de standaardtekst gebruikt.

Voorbeeld:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Verificatie {#section_pqf_3l4_xz}

Tekenreeksen beschikbaar voor het verificatieproces en in de geverifieerde gebruikersmenu&#39;s.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Autom. menutekenreeksen | menuAuthSignInBtn | Aanmelden |
|  | menuAuthSignedInMsg | U moet zijn aangemeld bij {action} |
|  | menuUserEditProfile | Profiel bewerken |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Afmelden |
|  | menuUserBackBtn | Alles |

## Stream-info {#section_wpy_gl4_xz}

Tekenreeksen beschikbaar voor informatie en weergave van de inhoudsstroom.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Opties in het menu Info | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Help |
|  | menuInfoLiveLink | Bezoek Livefyre.com |

## Info auteur/inhoud {#section_dhb_gl4_xz}

Stings beschikbaar voor auteur en individuele inhoudsinformatie.

| Element | Sleutel | Standaardtekst |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | In behandeling |
|  | commentReadMoreLink | Meer informatie |
|  | commentReplyLink | Zie {number} reacties |
|  | commentReplyLinkSing | Zie antwoord |
|  | commentStepCount | stemmen |
|  | commentStemCountSing | stemmen |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | Een array. Default =[ &quot;January&quot;, &quot;February&quot;, &quot;March&quot;, &quot;April&quot;, &quot;May&quot;, &quot;June&quot;, &quot;juli&quot;, &quot;August&quot;, &quot;September&quot;, &quot;Oktober&quot;, &quot;November&quot;, &quot;December&quot; ] |
|  | questionExplanation | U kunt nu opmerkingen rechtstreeks lezen en schrijven over zinnen, alinea&#39;s, afbeeldingen en aanhalingstekens.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Markeer </span> tekst en klik op het  <span class="&rdquo;fycon-write&rdquo;"></span> pictogram of klik op het  <span class="&rdquo;fycon-action-view&rdquo;"></span> pictogram aan het einde van elke alinea. |
|  | questionMockText | Wat &quot;bekend&quot; is, is niet bekend, alleen omdat het &quot;bekend&quot; is. |
|  | questionTitle | Wat is een Sidenote? |

## Gebruikershandelingen {#section_qxd_fl4_xz}

Tekenreeksen beschikbaar voor gebruikersacties: het markeren, delen, en het houden van bestaande inhoud.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Opties in het menu Reageren | menuRepliesViewTitle | Details |
|  | menuRepliesViewReply | Antwoord op Gesprek |
| Opties in het menu Delen | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Delen |
| Opties in het menu Vlag | menuFlagOptionDisagreement | Niet akkoord |
|  | menuFlagOptionOffsive | Aanstootgevend |
|  | menuFlagOptionOffTopic | Uit onderwerp |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Vlag als... |
|  | facebookShareCaption | Sidenotes op &quot;{title}&quot; |
| Opties voor mobiele gebruikers | sliderCommentTally | van |
|  | sliderInviteRead | Lezen |
|  | sliderInviteWrite | Schrijven |
|  | sliderLoading | Bezig met laden... |
|  | sliderWriteText | Wat denk je? Tik om te schrijven. |

## Functies {#section_xzf_2l4_xz} plaatsen

Tekenreeksen beschikbaar voor gebruikers die inhoud posten.

| Element | Sleutel | Standaardtekst |
|---|---|---|
|  | editorEditBtn | Opslaan |
|  | editorEditPosting | Opslaan... |
|  | editorEditReplyTitle | Reactie bewerken |
|  | editorEditTitle | Sidenote bewerken |
|  | editorPlaceholder | Wat denk je? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Post |
|  | editorPosting | Plaatsen... |
|  | editorReplyBtn | Antwoord plaatsen |
|  | editorReplyTitle | Reactie schrijven |
|  | editorTitle | Sidenote schrijven |
|  | emptyImageBlockTxt | Wat denk je? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Reageren |
|  | threadReplyBtn | Antwoord op Gesprek |
| Menuopties verwijderen | menuConfirmAccept | Ja, {action} |
|  | menuConfirmCancel | Annuleren |
|  | menuConfirmTitle | Weet je het zeker? |
| Opties in het menu Etc | menuEventOptionApple | Goedkeuren |
|  | menuEtcOptionDelete | Verwijderen |
|  | menuEventOptionEdit | Bewerken |
|  | menuEtcOptionFlag | Markering |
|  | menuEtcOptionShare | Delen |
|  | menuEtcPostedAt | Gepost op {date} |
|  | menuEtcTitle | Meer |

## Moderatorinterface {#section_o5f_dl4_xz}

Koorden beschikbaar aan de user-authenticated moderatorinterface.

| Element | Sleutel | Standaardtekst |
|---|---|---|
| Bevestigingsberichten via het menu Meer | notificationApproved | Goedgekeurd |
|  | notificationDelted | Verwijderd |
|  | notificationFlagged | Met vlag |

## Fouten {#section_gtk_cl4_xz}

Tekenreeksen beschikbaar voor algemene foutberichten.

| Element | Sleutel | Standaardtekst |
|---|---|---|
|  | errorConnection | Eh-oh. U hebt blijkbaar geen goede verbinding. |
|  | errorDuplicate | We houden ook van uw notitie, maar u kunt deze niet twee keer plaatsen. |
|  | errorGeneral | Er is een fout opgetreden. Probeer het opnieuw. |
|  | errorServer | Er ging iets mis met onze server. Probeer dat opnieuw? |
