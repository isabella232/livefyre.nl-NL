---
description: Gebruikers toestaan hun berichtfrequentie en inhoud te selecteren.
seo-description: Gebruikers toestaan hun berichtfrequentie en inhoud te selecteren.
seo-title: E-mailmeldingen
solution: Experience Manager
title: E-mailmeldingen
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# E-mailmeldingen{#email-notifications}

Gebruikers toestaan hun berichtfrequentie en inhoud te selecteren.

**Schakel e-mailmeldingen in voor uw gebruikers en moderatoren.**

Met LiveCycle Apps kunt u e-mailmeldingen inschakelen voor uw gebruikers en moderatoren, op basis van specifieke acties. Meldingen zijn gebaseerd op de tijd waarop inhoud naar de stream wordt gepost, zodat uw gebruikers betrokken kunnen blijven bij gesprekken die ze belangrijk vinden en op de hoogte kunnen worden gesteld wanneer iemand een van hun opmerkingen leuk vindt of erop reageert.

Gebruikers en moderatoren kunnen ervoor kiezen om e-mailmeldingen in of uit te voeren en kunnen de frequentie instellen waarmee e-mailberichten worden ontvangen. In deze sectie wordt beschreven hoe u deze e-mailmeldingen configureert en aanpast.

* E-mailopties gebruiker: beschikbare opties voor gebruikersmeldingen.
* E-mailopties voor moderator: de beschikbare opties voor moderatormeldingen.
* Opties voor e-mails met identiteit van live-gebruiker: e-mails verzonden als onderdeel van de Livefyre Identity. Deze e-mails zijn alleen relevant voor klanten met een identiteit van Livefy.
* Gegevenssynchronisatie met LiveCycle: het handhaven van voorkeur synchroniseert met Livefyre.
* E-mails aanpassen: e-mailaanpassingen beschikbaar.

Met de opties **Instellingen > Integratie-instellingen > Instellingen** voor e-mailmeldingen kunt u e-mailmeldingen aanpassen voor uw netwerk.

>[!NOTE]
>
>Om ervoor te zorgen dat uw eindgebruikers geen onbedoelde e-mail ontvangen, worden geen e-mailmeldingen verzonden vanuit de Livefyre UAT-omgeving.

**E-mailopties gebruiker**

Met LiveCycle kunt u gebruikers in staat stellen e-mailmeldingen over siteactiviteiten te ontvangen. Met de instellingen voor de integratie van het door Livefy geleverde gebruikersprofiel kunnen gebruikers hun voorkeuren voor meldingsschema&#39;s selecteren.

>[!NOTE]
>
>E-mails worden alleen verzonden voor inhoud die handmatig in de stream wordt geplaatst, en niet voor inhoud die vanuit SocialSync is opgehaald.

Als u gebruikers wilt toestaan hun berichtvoorkeuren in te stellen, neemt u een sectie E-mailmelding op in de Gebruikersinstellingen voor het gebruikersprofielsysteem. Voeg de corresponderende velden toe aan het databaseschema van het gebruikersprofiel en beheer de gebruikersinstellingen met Ping for Pull. (Werk met uw Technische Manager van de Integratie om standaardfrequenties voor uw netwerk te bepalen. Als u een klant van Profielen van de Onderneming bent, ga uw geselecteerde gebreken aan uw leveringsteam van Livefy voor configuratie in het gegevensbestand van de Bibliotheek over.)

Gebruikers op uw site kunnen dan een gesprek volgen en e-mailmeldingen ontvangen door op de **[!UICONTROL +Follow]** knop in de commentaareditor te klikken. De voorkeuren voor meldingen worden gedefinieerd op het niveau van het Livefy-netwerk. Om het even welke gebruikersmontages zullen op alle plaatsen en gesprekken over uw netwerk van toepassing zijn.

**Aanbevolen standaardinstellingen**

* Iemand schrijft in een gesprek dat ik volg:** uuroverzicht***
* Iemand houdt van één van mijn opmerkingen:** uuroverzicht**
* Iemand antwoordt op één van mijn opmerkingen:** onmiddellijk**
* Auto-follow conversaties wanneer ik een opmerking achterlaat:** off* (uitgeschakeld)

**Opmerking**: E-mailmeldingen zijn gebaseerd op de tijd dat inhoud is goedgekeurd voor opname in de stream.

Livefyre biedt twee opties voor e-mailfrequentie:

* Meteen
* Uurdigest

**Meteen**

E-mails die direct worden verzonden, geven de tekst, de titel van het artikel, de gebruikersnaam van de auteur en een koppeling **Reageren** weer waarmee de gebruiker naar de inhoud op de pagina gaat. Deze e-mailberichten bevatten ook een koppeling voor **afmelden** in de voettekst, waarmee gebruikers zich kunnen afmelden voor e-mailberichten voor die verzameling. Als u op **unsubscribe **klikt, worden de gebruikers doorgestuurd naar een bevestigingspagina waarop ze weten dat ze niet zijn geabonneerd op de verzameling.

**Uurdigest**

E-mails die in een uuroverzicht worden verzonden, geven alle inhoud, antwoorden op inhoud en dergelijke op de inhoud weer binnen het laatste uur (of zo) per app die de gebruiker volgt. Als de gebruiker meerdere apps in uw netwerk volgt, ontvangen zij één digest-e-mail voor elke app.

>[!NOTE]
>
>In gesprekken zonder nieuwe inhoud gedurende meer dan verscheidene uren, zullen de gebruikers met toegelaten uursamenvatting onmiddellijk bericht op een nieuwe inhoudspost ontvangen.

**Moderator e-mailopties**

Moderatoren kunnen zich aanmelden om e-mails te ontvangen voor inhoud die is gepost in een toepassing die zij volgen, en voor opmerkingen die zijn gemarkeerd als spam of offensief in een app die zij modereren. **Opmerking:** Er worden geen e-mailberichten verzonden wanneer gebruikers een opmerking markeren met Afwijzen of Buiten-onderwerp, omdat deze categorieën niet belangrijk worden geacht voor moderatormeldingen.

De moderator_comments en moderator_flags gebieden zouden ook aan uw de montages van het de paginadatabase van het gebruikersprofiel van de moderator moeten worden toegevoegd om uw moderatoren toe te staan om de frequentie van hun e-mailberichten bij te werken, en te weigeren als zij wensen. Livefyre adviseert dat u deze twee gebieden van het moderator e-mailbericht aan **nooit** plaatst. De opties omvatten **nooit** (gebrek), **onmiddellijk**, en **vaak**.

**Moderator-e-mail (gemarkeerde inhoud):**

Wanneer inhoud wordt gemarkeerd in een gemodereerde App, zal de e-mail die naar de moderator wordt verzonden de inhoud tonen die werd gemarkeerd, de gebruikersbenaming die de inhoud, en een verbinding terug naar de inhoudspagina verwees.

Wanneer een gebruiker zijn voorkeuren voor e-mailmeldingen op uw site in uw profielsysteem wijzigt, synchroniseert u de update naar het Levenverafgelegen profielsysteem met Livefyre Ping for Pull.

**Gegevenssynchronisatie met LiveCyre**

## E-mails aanpassen {#section_jxb_c5k_yy}

Het is mogelijk dat verschillende velden in de sjablonen voor e-mailmeldingen worden gewijzigd zodat ze aan uw stijl en merk voldoen.

* **[!UICONTROL From Email Address]**

   Het e-mailadres &#39;Van&#39; voor alle e-mailberichten kan worden aangepast aan uw merk. Livefefyre raadt **noreply@customerdomain.com** aan en vervangt **** customerdomain door uw domeinnaam. (De standaardwaarde is **noreply@livefyre.com**.) Geef uw voorkeur &quot;van e-mailadres&quot;aan uw Technische Manager van de Integratie voor configuratie in het gegevensbestand van de Levensstijl voor uw netwerk door.

   >[!NOTE]
   >
   >Laat dit veld leeg om e-mailmeldingen voor uw netwerk uit te schakelen

* **[!UICONTROL Email Logo]**

   Het logo dat in e-mailmeldingen wordt weergegeven, kan worden aangepast om uw bedrijfslogo weer te geven in plaats van het standaardlogo van Livefyre. Dit doet u op het tabblad Branding van de pagina **Netwerkinstellingen** van Studio. Deze aanpassing is alleen beschikbaar op netwerkniveau, niet op siteniveau en is alleen beschikbaar voor klanten met een betaald Livefyre.

* **[!UICONTROL Custom Templates]**

   U kunt desgewenst een volledig aangepaste e-mailsjabloon implementeren. Dit vereist echter enige ontwikkelingsinspanningen en kan kosten voor professionele dienstverlening met zich meebrengen. Neem contact op met uw accountmanager voor meer informatie.



Toepassingen die deze functie gebruiken:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Opmerkingen](/help/using/c-about-apps/c-comments/c-comments.md)
* [Functiekaart](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mediumwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Revisies](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

