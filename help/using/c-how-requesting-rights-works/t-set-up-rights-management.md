---
description: Definieer de instellingen voor het aanvragen van rechten voor Instagram- en Twitter-berichten.
seo-description: Definieer de instellingen voor het aanvragen van rechten voor Instagram- en Twitter-berichten.
seo-title: Rights Management instellen
solution: Experience Manager
title: Rights Management instellen
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---


# Rights Management instellen{#set-up-rights-management}

Definieer de instellingen voor het aanvragen van rechten voor Instagram- en Twitter-berichten.

Voordat u Instellingen voor rechtenaanvraag kunt definiëren, moet u een of meer sociale accounts configureren voor Instagram of Twitter. Zie [Een sociale account toevoegen](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram) voor meer informatie over het configureren van een sociale account.

>[!NOTE]
>
>U kunt het rechtenbeheer op het niveau van het Netwerk slechts vormen. U kunt het beheer van sitespecifieke rechten niet configureren.

1. Navigeer in LiveCycle Studio naar **[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >U zult moderator of beheerder netwerk-vlakke toestemmingen nodig hebben om de Rekeningen van het Rights Management te plaatsen.

1. Selecteer **[!UICONTROL +Add New Account]** als er geen Rights Management accounts zijn ingesteld.
1. Klik **[!UICONTROL Create New Setting]** onder het sociale netwerk u voor Rights Management wilt gebruiken.

   >[!NOTE]
   >
   >Voor Instagram-accounts hebt u een Instagram-bedrijfsaccount nodig om rechten met gedeeltelijke automatisering aan te vragen. Zie [Informatie over Instagram-accounts](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts) voor meer informatie over de verschillende soorten Instagram-accounts en hoe u deze kunt gebruiken.

1. Vul de weergegeven velden in. Alle velden zijn verplicht.

   * **[!UICONTROL Display name:]** Voer een weergavenaam in ter identificatie van het Twitter- of Instagram-account dat u voor uw Rights Request-account wilt gebruiken. Deze naam is alleen intern.
   * **[!UICONTROL Enabled:]**Standaard ingeschakeld. Hiermee schakelt u rechtenbeheer voor de account in.
   * **[!UICONTROL Approval hashtag:]** De hashtag die de eigenaar van de inhoud gebruikt om aan te geven dat hij of zij ermee instemt de inhoud te gebruiken.
   * **[!UICONTROL Terms and conditions:]** Een verbinding aan de Voorwaarden van uw netwerk voor het hergebruik van inhoud. Dit veld is hoofdlettergevoelig.
   * **[!UICONTROL Network and sites:]** Het netwerk of de site waarvoor deze account rechten voor hergebruik van inhoud kan aanvragen. Om deze rekening beschikbaar te maken over uw volledig netwerk, selecteer het eerste punt in de lijst, of grens tot specifieke plaatsen gebruikend de sleutel Command/CTRL.
   * **[!UICONTROL Default message:]** Een bericht dat met uw Verzoek van Rechten wordt getoond. U kunt dit bericht negeren wanneer u rechten aanvraagt.

      * Het leven stelt één van de standaardberichten aan moderatoren voor wanneer een moderator een verzoek aan een inhoudauteur uitgeeft. De moderatoren kunnen een ander standaardbericht produceren of het bericht uitgeven alvorens te verzenden. Berichten moeten de handgreep Twitter of Instagram van de auteur ({handle}), de hashtag voor goedkeuring ({GrantTag}) en een koppeling naar uw Voorwaarden en Voorwaarden ({termsLink}) bevatten.

         **[!UICONTROL Note:]** {handle} , {GrantTag} en {termsLink} zijn allemaal hoofdlettergevoelig.

         **[!UICONTROL Note:]** Om kwaadwillig gebruik te voorkomen, verpakt Twitter om het even welke inbegrepen URLs met  [t.](https://t.co/) coformatting. Als u wilt voorkomen dat uw standaardbericht langer is dan 140 tekens, wordt u aangeraden geen URL&#39;s op te nemen in uw standaardbericht.

      * Aanbevolen procedures voor het schrijven van rechtenaanvraagberichten:

         * Maak meerdere standaardberichten, zodat u niet als een robot klinkt. Sla elk standaardbericht op voordat u het volgende standaardbericht maakt.
         * Moedig uw moderatoren aan om deze nota te personaliseren alvorens te verzenden, om de verzoeken van uw netwerk te verhinderen worden geëtiketteerd Spam.

1. Klik **[!UICONTROL Save Settings]** om uw rekening van het Verzoek van Rechten toe te voegen.
Verzend een verzoek om rechten van de Bibliotheek van Activa. Zie [Een verzoek van Rechten verzenden](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) voor meer informatie over hoe te om een rechtenverzoek van de Bibliotheek van Activa te verzenden.