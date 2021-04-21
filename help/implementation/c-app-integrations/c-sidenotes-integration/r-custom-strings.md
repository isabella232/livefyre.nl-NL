---
title: Aangepaste strings
description: Aangepaste strings
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Aangepaste tekenreeksen zoeken{#sidenotes-custom-strings}

Aangepaste tekenreeksen worden toegepast via een object dat wordt geïnjecteerd in de constructor Sidenotes en overschrijven de standaardtekenreeksen die door de toepassing worden gebruikt. U kunt hiermee elk onderdeel van de taal aanpassen aan uw stijl- of taalspecificaties. Tekenreeksen worden automatisch samengevoegd met de standaardwaarden.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Sleutel | Standaard |
|---|---|
| appName | Sidenotes |
| commentModeratorTag | Mod |
| commentPendingTag | In behandeling |
| commentReadMoreLink | Meer informatie |
| commentReplyLink | Zie {number} reacties |
| commentReplyLinkSing | Zie antwoord |
| commentStepCount | stemmen |
| commentStemCountSing | stemmen |
| editorPlaceholder | Wat denk je? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Post |
| editorPosting | Plaatsen... |
| editorReplyBtn | Antwoord plaatsen |
| editorReplyTitle | Reactie schrijven |
| editorTitle | Notitie schrijven |
| emptyImageBlockTxt | Wat denk je? |
| emptyTextBlockTxt | + |
| errorConnection | Eh-oh. U hebt blijkbaar geen goede verbinding. |
| errorDuplicate | We houden ook van uw notitie, maar u kunt deze niet twee keer plaatsen. |
| errorGeneral | Er is een fout opgetreden. Probeer het opnieuw. |
| errorServer | Er ging iets mis met onze server. Probeer dat opnieuw? |
| facebookShareCaption | SideNotes on &quot;{title}&quot; |
| menuAuthSignedInMsg | U moet zijn aangemeld bij {action} |
| menuAuthSignInBtn | Aanmelden |
| menuBackBtn | Vorige |
| menuConfirmAccept | Ja, {action} |
| menuConfirmCancel | Annuleren |
| menuConfirmTitle | Weet je het zeker? |
| menuEventOptionApple | Goedkeuren |
| menuEtcOptionDelete | Verwijderen |
| menuEventOptionEdit | Bewerken |
| menuEtcOptionFlag | Markering |
| menuEtcOptionShare | Delen |
| menuEtcPostedAt | Gepost op {date} |
| menuEtcTitle | Meer |
| menuFlagOptionDisagreement | Niet akkoord |
| menuFlagOptionOffsive | Aanstootgevend |
| menuFlagOptionOffTopic | Uit onderwerp |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Vlag als... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Help |
| menuInfoLiveLink | Bezoek Livefyre.com |
| menuRepliesViewReply | Antwoord op Gesprek |
| menuRepliesViewTitle | Details |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Permalink kopiëren |
| menuShareOptionLinkComplete | Gekopieerd |
| menuShareOptionLinkFailed | Kopiëren mislukt |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Delen |
| notificationApproved | Goedgekeurd |
| notificationDelted | Verwijderd |
| notificationFlagged | Met vlag |
| permalinkBackBtn | Alles |
| permalinkTitle | Permalink |
| questionExplanation | U kunt nu opmerkingen rechtstreeks lezen en schrijven over zinnen, alinea&#39;s, afbeeldingen en aanhalingstekens.<br><br>Markeer tekst en klik op het pictogram ‘fycon-write’ of klik op het pictogram ‘fycon-action-view’ aan het einde van elke alinea. |
| questionMockText | Wat &quot;bekend&quot; is, is niet bekend, alleen omdat het &quot;bekend&quot; is. |
| questionTitle | Wat is een Sidenote? |
| queueCommentsPlural | {number} Nieuwe id&#39;s |
| queueCommentsSingular | 1 Nieuwe id |
| queueRepliesPlural | {number} Nieuwe reacties |
| queueRepliesSingular | 1 nieuwe reactie |
| responseBtn | Reageren |
| signInToPost | Aanmelden om een sidenote te schrijven |
| sliderCommentTally | van |
| sliderInviteRead | Lezen |
| sliderInviteWrite | Schrijven |
| sliderWriteText | Wat denk je? Tik om te schrijven |
| threadCollapseBtn | Samenvouwen |
| threadExpandBtnPlural | {number} reacties uitvouwen |
| threadExpandBtnSingular | 1 reactie uitvouwen |
| threadReplyBtn | Antwoord op Gesprek |
