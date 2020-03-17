---
description: Leer hoe te om tokens van Livefyre te produceren gebruikend ` C#' taal.
seo-description: Leer hoe te om tokens van Livefyre te produceren gebruikend ` C#' taal.
seo-title: Het creëren van de Tokens van Livefyre ` C# `
solution: Experience Manager
title: Het creëren van de Tokens van Livefyre ` C# `
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre Tokens maken C\# {#creating-livefyre-tokens-c}

Leer hoe u Livefyre-tokens kunt genereren met de taal ``C#``.

U kunt oude documentatie en voorbeeldcode gebruiken `C#.NET` om methoden te schrijven voor het maken van tokens.

Als u wilt verwijzen naar de officiële bibliotheken van Livefyre, gebruikt u de [Java-bibliotheek](https://github.com/Livefyre/livefyre-java-utils) als beginpunt voor `C#` ontwikkelaars.

U kunt ook overwegen om de Bibliotheek [](https://github.com/Livefyre/livefyre-nodejs-utils) Node.js van de bevellijn te gebruiken om verwijzingstokens voor zich te produceren, en vertrouwd met de methodestructuur te worden.

* [Springen naar meta-token voor verzameling](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Springen naar auteur-token](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Afhankelijkheden {#section_c15_fnh_xz}

* U hebt het [JWT-nugetpakket](https://www.nuget.org/packages/JWT) in uw project nodig om de tokens te genereren.
* Codevoorbeelden op deze pagina gebruiken het [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) -pakket.

## CollectionMeta-token {#section_dzt_4mh_xz}

De token CollectionMeta wordt doorgegeven aan LiveCycle wanneer u opmerkingen op een pagina insluit en verschaft ons systeem de vereiste metagegevens voor uw nieuwe verzameling. Daarnaast maakt u een MD5 van deze gegevens, die door LiveCyre wordt gecontroleerd om te controleren of de metagegevens zijn gewijzigd. `checksum` (bijvoorbeeld als de titel of URL van het artikel is bewerkt).

Deze token is ondertekend met uw `Site Key`account, die u van uw technische accountmanager bij Livefyre hebt ontvangen.

Zie ook:

* Officiële CollectionMeta Symbolische Docs
* [Voorbeeld](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Maak een woordenboek met de metagegevens voor de verzameling. In deze stap voegen we slechts enkele van de benodigde velden toe, omdat we een controlesom van dit object willen maken VOORDAT we de artikelid toevoegen.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **titel** *vereist*:  De titel van de verzameling, doorgaans de titel van het artikel. De maximale lengte is 255 tekens. Biedt geen ondersteuning voor html-entiteiten. Codeer speciale tekens met UTF-8.
   * **URL** *vereist*:  De canonieke URL van uw artikel. Dit wordt gebruikt door de functie voor het delen van opmerkingen en de functie voor sociale synchronisatie en door koppelingen naar uw artikel via het dashboard voor beheerders. Houd er bij lokale tests rekening mee dat Livefyre &quot;localhost&quot; niet accepteert als domein.
   * **tags** *optioneel*:  Een door komma&#39;s gescheiden lijst met tags die u wilt toevoegen aan de verzameling op het dashboard Livefyre. Tags mogen geen spaties bevatten. Gebruik onderstrepingstekens als u een spatie wilt weergeven op het dashboard voor beheerders.
   * **type** *optioneel*:  Een tekenreeks die aangeeft welk type verzameling moet worden gemaakt. Geldige waarden zijn:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Als u deze optie niet opgeeft, wordt standaard een LiveComments-verzameling gemaakt.


1. JSON codeert dit woordenboek en genereert een controlesom md5.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Voeg de **articleId** toe aan het woordenboek. De **controlesom** gaat niet in het token collectionMeta, maar moet als een afzonderlijke parameter in het object convConfig worden verzonden.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleId** *vereist*:  Een unieke id voor uw verzameling binnen uw Livefyre-site. Gewoonlijk wordt de unieke artikelid gebruikt in uw CMS. (bijvoorbeeld uw WordPress post-id) Deze waarde mag nooit worden gewijzigd. De bibliotheek identificeert unieke inzamelingen door de combinatie siteId en articleId.

1. Genereer een ondertekend JWT-token van het woordenboek met de sitetoets die u van Livefyre hebt ontvangen. Houd er rekening mee dat u het juiste hash-algoritme moet opgeven, aangezien het JWT-pakket standaard geen HS256 gebruikt.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Het token Gebruikersauteur {#section_g1d_43h_xz}

De gebruiker Auth Token wordt gebruikt om een gebruiker in Livefyre te ondertekenen. Wanneer een gebruiker zich op uw site aanmeldt, genereert de site een gebruikerstoken voor de auteur die wordt doorgegeven aan de widget Livefyre op de pagina. (Zie Externe profielen voor meer informatie over het verificatieproces.)

Dit token vereist uw netwerknaam (network.fyre.co) en is ondertekend met uw netwerksleutel die u ontvangt van uw technische accountmanager bij Livefyre.

Zie ook:

* Officiële documenten van Auth Token
* [Voorbeeld](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Maak een woordenboek met de benodigde informatie.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **domein:** De naam van uw netwerk (verstrekt door Livefyre.) bijv. mijnnetwerk.fyre.co
   * **user_id:** De unieke gebruikers-id voor de gebruiker in het profielsysteem van uw site. Alleen alfanumerieke tekens (A-Z, a-z, 0-9). Als de gebruikers-id&#39;s van uw systeem ongeldige tekens bevatten, kunt u overwegen Livefyre een md5-hash van de gebruikers-id of een base64-gecodeerde versie ervan te verzenden. (Laat uw accountmanager weten of u dit doet.)
   * **verloopt:** De datum (in Epoch-tijd) waarop het token verloopt. Deze moet overeenkomen met de sessietijd van de aanmeldingen op uw site, zodat de aanmeldingsstatus van Livefyre synchroon blijft met die van uw site.
   * **display_name:** De weergavenaam van de gebruiker in uw profielsysteem, zoals deze moet worden weergegeven in de opmerkingenstroom.

1. Genereer een ondertekend JWT-token van het woordenboek met de netwerksleutel die u van Livefyre hebt ontvangen. Houd er rekening mee dat u het juiste hash-algoritme moet opgeven, aangezien het JWT-pakket standaard geen HS256 gebruikt.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```