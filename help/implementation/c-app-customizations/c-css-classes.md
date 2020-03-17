---
description: Gebruik beschikbare CSS-klassen om de weergave van uw apps aan te passen.
seo-description: Gebruik beschikbare CSS-klassen om de weergave van uw apps aan te passen.
seo-title: CSS-klassen
solution: Experience Manager
title: CSS-klassen
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS-klassen{#css-classes}

Gebruik beschikbare CSS-klassen om de weergave van uw apps aan te passen.

Beschikbaar voor Chat, Commentaren, Levende Blog, Recensies, en Duidelijkheden.

Gebruik CSS om uw LiveCycle Apps voor een volledigere integratie met uw pagina aan te passen, door eenvoudig de standaardCSS van de App met uw eigen stijlblad met voeten te treden. In deze sectie worden de beschikbare CSS-aanpassingen beschreven.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [CSS sorteeropties](#c_css_classes/section_btq_4rh_xz)
* [Opmerking-CSS](#c_css_classes/section_mlv_nrh_xz)
* [Aanbevolen opmerkingen, CSS](#c_css_classes/section_m2v_mrh_xz)
* [CSS voor gearchiveerde opmerkingen](#c_css_classes/section_bs5_lrh_xz)
* [CSS voor opmerkingenmelding](#c_css_classes/section_dy4_krh_xz)
* [CSS-klassen stabiliseren](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Gebruik deze klassen om de interface van de post redacteur te veranderen.

| Klasse | Beschrijving |
|---|---|
| .fyre-comment-count | De tekst waarin het aantal opmerkingen wordt weergegeven. |
| .fyre-login-bar | Het selectiekader dat de aanmeldbalk en opties bevat. |
| .fyre-live-container | Het selectiekader rond het aantal mensen dat luistert en hun avatars. |
| .fyre-editor | Het selectiekader rond de .fyre-login-bar, .fyre-live-container en het tekstgebied waar de gebruikers hun commentaren schrijven. |
| .fyre-stream-sortering | Het selectiekader rond de sorteeropties. |

U kunt stijlen ook bewerken in de toepassingsconfiguratie zelf, zoals de achtergrondkleur van het bewerkingsveld en de lettertypekleur, -grootte en -familie van de tekst die in de editor wordt weergegeven.

Als u de commentaareditor wilt aanpassen, voegt u het object editorCss:{} toe aan fyre.conv.load() en neemt u de gewenste opmaak op. Bijvoorbeeld, om de redacteur met uw douaneCSS bij te werken:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## CSS sorteeropties {#section_btq_4rh_xz}

| Klasse | Beschrijving |
|---|---|
| .fyre-stream-sortering | De volledige sorteeropties div. |
| .fyre-stream-sort-newest | De optie Nieuwst. |
| .fyre-stream-sort-oldest | De optie &quot;Oudst&quot;. |
| .fyre-stream-sort-bar | De scheidingsbalk tussen de opties. |
| .fyre-stream-sort-selected | De momenteel geselecteerde sorteeroptie. |

HTML-structuur:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Verberg het scheiden van de sorteeropties met ‘|’.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Opmerking-CSS {#section_mlv_nrh_xz}

| Klasse | Beschrijving |
|---|---|
| .fyre-comment-schrijver-markering- *`custom tag name`* | Livefyre zal een CSS klasse in dit formaat voor elke gebruikersmarkering tot stand brengen die door de Studio van Livefyre, [de Synchronisatie](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)van het Profiel wordt toegevoegd. Deze klasse kan worden gebruikt om de achtergrond op te maken voor alle inhoud die wordt geplaatst door gebruikersaccounts, inclusief de tag. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre zal een CSS klasse in dit formaat voor elke inhoudstag creëren die door Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)wordt toegevoegd. Deze klasse kan worden gebruikt om de inhoud op te maken waaraan u de tag hebt toegevoegd. |
| .fyre-comment-user | Het selectiekader dat de afbeelding van het gebruikersprofiel bevat. |
| .fyre-comment-username | De gebruikersnaam. |
| .fyre-moderator | Het omsluitende kader van de moderator. |
| .fyre-comment | Selectiekader rond de tekst/koppeling van de opmerking. |
| .fyre-comment-article | Het selectiekader voor de gehele inhoud van de opmerking. |
| .fyre-comment-date | De tag die is gekoppeld aan het element &#39;time since postted&#39;. |
| .fyre-comment-media | Het selectiekader rond de media-inhoud. |
| .fyre-comment-actions | Het selectiekader rond de beschikbare acties die moeten worden uitgevoerd op een opmerking. |
| .fyre-comment-als | Het selectiekader rond de koppeling ‘Soortgelijk’. |
| .fyre-comment-response | Het selectiekader rond de koppeling Reageren. |

## Aanbevolen opmerkingen, CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>Alle CSS-klassen voor opmerkingen kunnen ook worden toegepast op aanbevolen inhoud.

| Klasse | Beschrijving |
|---|---|
| .fyre-gekenmerkte-inhoud-omslag | De container div voor de lezer. |
| .fyre-featured-header | De titelbalk voor de regelafstand. |
| .fyre-featured-header-icon | Het quill-pictogram van de koptekst. |
| .fyre-featured-title | De koptekst. |
| .fyre-featured body | De container div voor aanbevolen inhoud in de lezer. |
| .fyre-featured-quote | Het aanhalingspictogram dat met elk inhoudsitem begint. |

## CSS voor gearchiveerde opmerkingen {#section_bs5_lrh_xz}

>[!NOTE]
>
>Alle inhoud-CSS-klassen kunnen ook worden toegepast op gearchiveerde inhoud.

| Klasse | Beschrijving |
|---|---|
| .fyre-archive-stream-title | De tekst &#39;Van het Archief&#39;. |
| .fyre-archive-stream-title-icon | Het logo voor de koptekst &#39;Van het archief&#39;. |

## CSS voor opmerkingenmelding {#section_dy4_krh_xz}

Met deze klassen kunt u de Livefy Comment Notifier aanpassen.

| Klasse | Beschrijving |
|---|---|
| .fyre-notification | De div voor het lijstitem (zowel nieuwe als archiefinhoud). |
| .fyre-kennisgever | De omslag voor de inhoud van de Notifier. |
| .fyre-notifier-archive | De omslag voor alle nieuwe inhoud buiten de meest recente post. |
| .fyre-notifier-avatar | De afbeelding voor de avatar. |
| .fyre-notifier-avatar-container | De container div voor de gebruiker avatar. Hiermee kunt u positionering definiëren. |
| .fyre-notifier-avatar-shading | De arcering voor de avatar div. |
| .fyre-notifier-banner | De container voor de voorvertoningsinhoud van de Notifier, die de gebruikersavatar en een inhoudsfragment voor het laatst geposte item weergeeft. |
| .fyre-notifier-base | De container voor het informatiegedeelte van de Notifier, die van het aantal nieuwe commentaren, de Notifier titel, en de dichte knoop een lijst maakt. |
| .fyre-notifier-base-close | De container div voor de sluitknop (x) voor de Notifier. |
| .fyre-notifier-base-shadow | De schaduw voor de Notifier-basis. |
| .fyre-notifier-caption | De tekst die voor de kennisgever wordt getoond. &quot;Nieuwe opmerking(en)&quot; standaard. |
| .fyre-notifier-close | Een knop waarmee de kennisgever wordt gesloten. |
| .fyre-notifier-container | De container voor de Notifier, omvat zowel de banner als de basis. |
| .fyre-notifier-counter | De container voor het nummer in de Notifier. |
| .fyre-notifier-list | De container voor het meest recente stuk inhoud. |
| .fyre-notifier-message | De eerste ~30 tekens van de weergegeven inhoud. |
| .fyre-notifier-message-container | De container div voor het koptekstbericht. |
