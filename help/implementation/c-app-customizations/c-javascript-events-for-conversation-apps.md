---
description: De beschikbare gebeurtenissen waaraan u JavaScript voor conversatieapps kunt binden (bijvoorbeeld Comments, Chat, Live Blog, Reviews en Sidenotes).
title: Javascript-gebeurtenissen voor conversie-apps
exl-id: 2497346e-b2cc-44b2-bcd9-906dd443fe38
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 8%

---

# Javascript-gebeurtenissen voor conversie-apps{#javascript-events-for-conversation-apps}

De beschikbare gebeurtenissen waaraan u JavaScript voor conversatieapps kunt binden (bijvoorbeeld Comments, Chat, Live Blog, Reviews en Sidenotes).

## Matrix voor conversie-apps en gebeurtenissen {#section_y4j_x4m_ybb}

Hieronder volgt een matrix van de gebeurtenissen die beschikbaar zijn voor conversatie-apps. Een X geeft aan dat de gebeurtenis beschikbaar is voor de App, N.v.t. geeft aan dat de gebeurtenis niet van toepassing is op de App en dat geen markering betekent dat de gebeurtenis niet beschikbaar is voor die App:

### Gesprek App-gebeurtenissen

| Gebeurtenissen | Opmerkingen | Chat | Liveblog | Revisies | Sidenotes | Opiniepeilingen | Trend |
|---|---|---|---|---|---|---|---|
| Init | X | X | X | X | X |  |  |
| Laden | X | X | X | X |  |  |  |
| Weergave | X | X | X | X |  |  |  |
| Post | X | X | X | X |  | N.v.t. | N.v.t. |
| Gepost | X | X | X | X | X | N.v.t. | N.v.t. |
| Twitter Reageren | X | X | X | N.v.t. | N.v.t. | N.v.t. | N.v.t. |
| Twitter like | X | X | X | N.v.t. | N.v.t. | N.v.t. | N.v.t. |
| LF-achtig | X | X | X | X | N.v.t. | N.v.t. | N.v.t. |
| LF in tegenstelling | X | X | X | X | N.v.t. | N.v.t. | N.v.t. |
| Delen op bericht | X | X |  | X | N.v.t. | N.v.t. | N.v.t. |
| Knop Delen | X | X | X | X |  | N.v.t. | N.v.t. |
| Twitter delen | X | X | X | X | X | N.v.t. | N.v.t. |
| Facebook delen | X | X | X | X | X | N.v.t. | N.v.t. |
| URL delen | X | X | X | X |  | N.v.t. | N.v.t. |
| ExpandReplies | X | N.v.t. | X | X | N.v.t. | N.v.t. | N.v.t. |
| Antwoorden samenvouwen | X | N.v.t. | X | X | N.v.t. | N.v.t. | N.v.t. |
| Knop Vlag | X | X | X | X | N.v.t. | N.v.t. | N.v.t. |
| Markering | X | X | X | X | X | N.v.t. | N.v.t. |
| Markering annuleren | X | X | X | X | N.v.t. | N.v.t. | N.v.t. |
| Volg | X | N.v.t. | X | X | N.v.t. | N.v.t. | N.v.t. |
| Ongedaan maken | X | N.v.t. | X | X | N.v.t. | N.v.t. | N.v.t. |
| RequestMore | X | X | X | X | N.v.t. | N.v.t. | N.v.t. |
| ModalView |  | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. |
| Twitter Retweet | X | X | X | N.v.t. | N.v.t. | N.v.t. | N.v.t. |
| Na klikken | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. |
| Aantal opmerkingen bijgewerkt | X | X | X | X | N.v.t. | N.v.t. | N.v.t. |
| Gebruiker aangemeld |  |  |  |  |  | N.v.t. | N.v.t. |
| Gebruiker afgemeld |  |  |  |  |  | N.v.t. | N.v.t. |
| Opmerking weergegeven |  | N.v.t. |  |  | N.v.t. | N.v.t. | N.v.t. |
| Opmerking ongewijzigd |  | N.v.t. |  |  | N.v.t. | N.v.t. | N.v.t. |
| Opmerking gestemd | N.v.t. | N.v.t. | N.v.t. | X | X | N.v.t. | N.v.t. |
| Selectie opiniepeiling | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. |  | N.v.t. |
| Trend item geselecteerd | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. |  |
| Netwerk-id |  |  |  |  |  |  |  |
| Toepassings-id | X | X | X | X |  |  |  |
| Context-id | X | X | X | X |  |  |  |
| App-type | X | X | X | X |  |  |  |
| Inhoudstype | X | X | X | X |  |  |  |
| Gepubliceerde datum voor app |  |  |  |  |  |  |  |
| Aangemeld bij de eindgebruikertoepassing |  |  |  |  |  |  |  |
