---
description: Stel referenties in waarmee uw gebruikers inhoud kunnen delen met verschillende sociale netwerken.
seo-description: Stel referenties in waarmee uw gebruikers inhoud kunnen delen met verschillende sociale netwerken.
seo-title: Sociaal delen inschakelen
solution: Experience Manager
title: Sociaal delen inschakelen
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---


# Sociaal delen inschakelen {#enabling-social-sharing}

Stel referenties in waarmee uw gebruikers inhoud kunnen delen met verschillende sociale netwerken.

Als u gebruikers wilt toestaan inhoud te delen op sociale-mediasites, implementeert u de functie voor sociaal delen van LiveCycle en maakt u een OAuth-systeem voor correcte verificatie van deze sites. Met dit systeem handelt LiveCyre namens de gebruiker wanneer deze ervoor kiest inhoud te delen via sociale media.

>[!NOTE]
>
>Verschillende providers hebben verschillende OAuth-vereisten. Raadpleeg uw providers voor informatie over de implementatie van OAuth.

## Vereiste sociale referenties {#section_gff_cjm_b1b}

Als u een aangepast identiteitssysteem voor gebruikers gebruikt, moet u uw sociale gegevens opgeven om gebruikers in staat te stellen vanuit een LiveCycle-app te delen naar Twitter, Facebook of LinkedIn.

>[!NOTE]
>
>Klanten die Janrain Engage gebruiken, hoeven alleen hun Engage Domain en Engage API Key te verstrekken.

Gebruik het deelvenster Integratie-instellingen van de Admin Console om de volgende sociale gegevens in te voeren of bij te werken.

### Vereiste referenties:

* **** FacebookClient ID Client Secret OAuth Proxy Redirect
* **API-beveiligingssleutel** LinkedInAPI
* **TwitterAccess Token Access Token Secret API Key Secret Secret** API Secret

## Twitter {#section_qp5_1yl_b1b}

Twitter-referenties zijn beschikbaar op het Twitter App Dashboard. U kunt als volgt deze referenties vinden:

* Open [Twitter&#39;s App Dev Page](https://dev.twitter.com/apps) als eigenaar van de app, zoek de toepassing en klik op de titel.
* De rol neer aan &quot;Uw toegangstoken&quot;en grijpt de waarden van &quot;het teken van de Toegang&quot;en &quot;het symbolische geheim van de Toegang.&quot;

U moet:

* Voer een waarde in voor het veld URL voor terugbellen in de Twitter-app. Hoewel dit veld een eenvoudige plaatsaanduiding kan zijn, mag het niet leeg blijven.
* Plaats het Type van Toepassing om zowel **read** als **write** toegang te hebben.
* Controleer of de URL van de Twitter App-website zich op hetzelfde hostdomein bevindt als de Livefyre Core-app.

>[!NOTE]
>
>Alle toepassingen die Twitter-inhoud weergeven, zijn vereist om aan de vereisten voor weergave te voldoen. Zie [Twitter-weergaverichtlijnen](https://dev.twitter.com/terms/display-requirements) voor meer informatie.

## LinkedIn {#section_lfz_zxl_b1b}

LinkedIn geloofsbrieven zijn beschikbaar bij de sectie van Sleutels OAuth van uw Sleutels van API LinkedIn van de Toepassing.

* Meld u aan bij uw account op de pagina [https://developer.linkedin.com/](https://developer.linkedin.com/) van LinkedIn&#39;s Developers.
* Houd de muisaanwijzer boven uw naam in de rechterbovenhoek en selecteer API-toetsen in het vervolgkeuzemenu.
* Klik op de titel Toepassing.
* De waarden voor de API-sleutel en de geheime sleutel ophalen uit de sectie OAuth-toetsen

## Facebook {#section_zyb_gpl_b1b}

Facebook-referenties zijn beschikbaar op de pagina Developer Apps.

* Open [De pagina Developer Apps Page](https://developers.facebook.com/apps) van Facebook als eigenaar van de app, zoek de toepassing en klik op de titel.
* Pak de waarden voor de toepassings-id en het toepassingsgeheim vast. Voor App Secret, kunt u de knoop van de Show moeten klikken om het te tonen.

Als u bestanden wilt delen op Facebook, moet u een pagina voor omleiding instellen om Facebook-verzoeken in te dienen en zich aan de domeinpraktijken te houden die vereist zijn door [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). De pagina moet op uw domein worden gehost, zodat Facebook kan controleren of de aanvraag afkomstig is van een legitieme bron.

### Facebook Redirect

De gehoste pagina moet de volgende code bevatten:

### Ruby

Dit is een voorbeeld van het gebruik van Ruby en Rails om de Facebook OAuth omleiding te doen.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

Dit is een voorbeeld van het gebruik van Python en Django om de OAuth-omleiding op Facebook uit te voeren.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Dit is een voorbeeld van het gebruik van NodeJS en Sail/Express voor het omleiden van Facebook OAuth.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Dit is een voorbeeld van het gebruik van Java- en lentecontrollers om de Facebook OAuth-omleiding uit te voeren.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## &quot;Post to&quot;-providers {#section_rdk_dpl_b1b} configureren

Standaard worden de knoppen Facebook, LinkedIn en Twitter &quot;Post to&quot; weergegeven in de Livefyre Core-toepassingen. Gebruik de parameter postToButtons om te configureren welke providers worden weergegeven bij het insluiten van de Livefyre-app.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` is een array met een subset van de volgende opties:

* tw: Twitter
* fb: Facebook
* li: LinkedIn
