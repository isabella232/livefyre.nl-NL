---
description: Voeg LiveCycle toe aan uw native iOS-app.
seo-description: Voeg LiveCycle toe aan uw native iOS-app.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Voeg LiveCycle toe aan uw native iOS-app.

Gebruik deze opensource-bibliotheek om LiveCycle-services te integreren in uw native iOS-app. De Live StreamHub iOS SDK biedt een dunne laag rond onze gemeenschappelijke API-mechanismen, gebaseerd op de uitstekende AFNetworking-bibliotheek.

Livefyre biedt ook twee iOS-voorbeeldtoepassingen op basis van deze SDK: een commentaarstroom en een revisiesvoorbeeld-app.

## De SDK in uw project integreren als een cacaopod (aanbevolen) {#section_qc5_h3v_zz}

De gemakkelijkste manier om StreamHub-iOS SDK aan uw project toe te voegen is CocoaPods te gebruiken. Als u geen CocoaPods hebt, voert u de installatie van gem voor coapods en pod uit. Hier volgt een voorbeeld van Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

U moet ook een opslagplaats Specs toevoegen aan uw installatie CocoaPod (dit zal het aan `~/.cocoapods/repos` folder klonen):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Als uw Podfile is gemaakt in de hoofdmap van uw toepassingsproject en de opslagplaats hierboven is toegevoegd, voert u het volgende uit:

```
pod install
```

Hiermee worden alle afhankelijkheden gedownload en een bestand in MyApp.xcworkspace gemaakt. U moet het bestand vanaf nu gebruiken om uw app-project in Xcode te openen.

## Als Xcode-subproject {#section_jcm_g3v_zz}

U kunt ook de opslagplaats klonen:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Vervolgens voegt u het Xcode-project (LFSClient.xcodeproj) als een subproject toe aan uw toepassing (eenvoudig gedaan door het bestand LFSClient.xcodeproj naar het deelvenster Projectnavigator in Xcode te slepen).

U zult ook het zelfde met om het even welke gebiedsdelen ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)) moeten doen.

## Alles tegelijk downloaden (niet aanbevolen) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Als u tests wilt uitvoeren in Xcode 6, moet u $(PLATFORM_DIR)/Developer/Library/Frameworks toevoegen aan FRAMEWORK_SEARCH_PATHS in Pods-test-XCTest+OHHTTPStubSuiteCleanUp[podhttps://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

U hebt het bestand LFSTestConfig.plist van Livefyre nodig, dat Livefyre op verzoek verschaft.

## Xcode-documentatie {#section_arl_b3v_zz}

U kunt door de [documentatie](https://livefyre.github.com/StreamHub-iOS-SDK/) bladeren of u kunt het doel &quot;Documentatie&quot;in uw Xcode (vereist dat appledoc wordt geïnstalleerd) op uw systeem bouwen.

## Vereisten {#section_m5l_13v_zz}

Voor versies van StreamHub iOS SDK sinds v0.2.0 is iOS 6.0 of hoger vereist.

## Bijlage (JSON-ondersteuning) {#section_pcd_5hv_zz}

Voor degenen die de internals van StreamHub-iOS SDK bekijken, gelieve te merken op dat wij een gewijzigde versie van [JSONKit](https://github.com/escherba/JSONKit) als standaardJSON parser (in plaats van Apple-Geleverde NSJSONSerialization) gebruiken. We moesten dit doen omdat de door Apple verschafte parser geen decodering van JSON-bestanden ondersteunt die gehele getallen of drijvende-kommagetallen bevatten die groter zijn dan die welke door het systeem kunnen worden weergegeven. Onze gewijzigde versie van JSONKit beknot zeer grote aantallen aan het overeenkomstige systeemmaximum, in plaats van het werpen van een uitzondering.