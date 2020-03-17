---
description: Teksttekenreeksen aanpassen voor LiveCycle Sidenotes
seo-description: Teksttekenreeksen aanpassen voor LiveCycle Sidenotes
seo-title: Geeft tekstreeksen aan
solution: Experience Manager
title: Geeft tekstreeksen aan
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Geeft tekstreeksen aan{#sidenotes-text-strings}

Teksttekenreeksen aanpassen voor LiveCycle Sidenotes

Deze pagina bevat een overzicht en beschrijving van alle tekenreeksen die beschikbaar zijn voor aanpassing in Sidenotes-apps. Zie Tekenreeksaanpassingen voor informatie over tekenreeksen die beschikbaar zijn voor de kerntoepassingen van LiveCycle.

ImplementationAuthStream InfoAuthor / Content InfoUser ActionsPost FunctionsModerator InterfaceErrors

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

## Informatie auteur/inhoud {#section_dhb_gl4_xz}

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
|  | datetimeMonths | Een array. Standaard =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplanation | U kunt nu opmerkingen rechtstreeks lezen en schrijven over zinnen, alinea&#39;s, afbeeldingen en aanhalingstekens.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Markeer tekst</span> en klik op het <span class="&rdquo;fycon-write&rdquo;"></span> pictogram of klik op het <span class="&rdquo;fycon-action-view&rdquo;"></span> pictogram aan het einde van elke alinea. |
|  | questionMockText | Wat &quot;bekend&quot; is, is niet bekend, alleen omdat het &quot;bekend&quot; is. |
|  | questionTitle | Wat is een Sidenote? |

## Handelingen van gebruikers {#section_qxd_fl4_xz}

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
|  | sliderLoading | Laden... |
|  | sliderWriteText | Wat denk je? Tik om te schrijven. |

## Functies {#section_xzf_2l4_xz}

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

