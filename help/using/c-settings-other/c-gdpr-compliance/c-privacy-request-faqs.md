---
description: Antwoorden op Veelgestelde vragen (FAQs) over GDPR-Klaar de Verzoeken van de Privacy.
title: Veelgestelde vragen over privacyverzoeken
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Veelgestelde vragen over privacyverzoeken{#privacy-request-faqs}

Antwoorden op Veelgestelde vragen (FAQs) over GDPR-Klaar de Verzoeken van de Privacy.

* **Hoe kunnen bezoekers van de site ervoor kiezen niet te worden bijgehouden op een site die gebruikmaakt van LiveCycle Apps?** Wanneer een sitebezoeker het programma uitschakelt, moet de implementatie van de klant bij LiveCycle aangeven dat de gebruiker het programma heeft uitgeschakeld voordat een app wordt gemaakt. Livefyre heeft een manier gecreeerd om dit met de optie te doen JavaScript, `userPrivacyOptOut`. Zie [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md) voor meer informatie over het gebruik van `userPrivacyOptOut`.

   Wanneer de markering `userPrivacyOptOut` is ingesteld op true, verzendt Apps op de pagina geen gegevens naar LiveCycle-servers met behulp van cookies of een andere methode. De lokale opslag wordt dan niet bijgewerkt met gegevens die kunnen worden gebruikt om bezoekers van de site bij te houden. Als een bron geen volmacht steunt, dan toont Livefyre een masker op de inhoud tenzij een gebruiker op de video klikt en het potentiële volgen van die bron goedkeurt.

   Als u LiveCycle Identity gebruikt, kunnen gebruikers ervoor kiezen om hun profiel te verwijderen of een rapport te maken met gegevens die voor hun gebruikersaccount worden bijgehouden.

* **Hoe kan ik voorkomen dat ik toekomstige inhoud verzamel van een bezoeker van de site die ervoor gekozen heeft?** Gebruik deze  `userPrivacyOptOut` met  `livefyre.js` op een webpagina die LiveCycle Apps gebruikt. Zie [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md) voor meer informatie over `userPrivacyOptOut`.

* **Hoe kan ik een rapport genereren en de gegevens voor App-gebruikers of eigenaars van sociale accounts verwijderen?** [Privacy-](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) aanvragen om een rapport te genereren en gebruikersgegevens uit Apps te verwijderen.

* **Hoe verwijder ik alle inhoud voor een bezoeker?** Livefyre houdt geen permanente informatie bij over sitebezoekers, behalve in de vorm van cookies om deze op unieke wijze te identificeren voor Livecount-functies. Livecount is een tijdelijk en realtime aantal bezoekers op de site. Er blijft geen geschiedenis behouden nadat de bezoeker cookies verlaat of wist.

   Maak een [Privacyverzoeken](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) om de account te verwijderen. LiveCycle verwijdert of maakt het gebruikersprofiel en de bijbehorende records anoniem.

* **Hoe verwijder ik inhoud voor een geregistreerde gebruiker?** Maak een  [privacyaanvraag ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) om het account te verwijderen. Het gebruikersprofiel en de bijbehorende records worden volledig vernietigd.

   >[!NOTE]
   >
   >Deze handeling kan niet ongedaan worden gemaakt.

* **Hoe kan ik een rapport opstellen met gegevens die worden bijgehouden van een huidige of voormalige werknemer?** [Een privacyrapport weergeven ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) om een rapport te genereren met gegevens die zijn bijgehouden voor een gebruikersaccount.

* **Voldoet Livefyre social stream?** Wanneer een gebruiker een bericht of tweet verwijdert uit het sociale netwerk, wordt de inhoud binnen 24 uur ook verwijderd uit alle bronnen in LiveCycle. Dit geldt voor Twitter en Facebook.
