---
description: Maak Android-apps met Livefyre.
seo-description: Maak Android-apps met Livefyre.
seo-title: Android-SDK
solution: Experience Manager
title: Android-SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android-SDK{#android-sdk}

Maak Android-apps met Livefyre.

Gebruik deze bibliotheek om LiveCycle-services te integreren in uw systeemeigen Android-app. De [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) verstrekt een dunne laag rond onze gemeenschappelijke API mechanismen, die op de Gradle/Android Studio ontwikkelomgeving worden gebaseerd.

Livefyre biedt ook een voorbeeldapp voor [revisies](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) op basis van deze SDK.

Deze Livefyre Android-SDK kan zowel in Eclipse als in Android Studio worden gebruikt.

>[!NOTE]
>
>Voordat u de Livefyre Android-SDK installeert, moet de [Android-SDK](https://developer.android.com/sdk/index.html) op uw omgeving zijn geïnstalleerd. U moet ook enkele extra Android SDK-pakketten opnemen, zoals beschreven in de documentatie voor Android-ontwikkelaars > .
>[SDK-pakketten toevoegen](https://developer.android.com/sdk/installing/adding-packages.html)

Gebruik Android SDK Manager (beschikbaar op de werkbalk Android Studio of Eclipse) om alle aanbevolen pakketten te installeren. Zorg ervoor dat u ook de Android Support Repository opneemt.

## Eclipse {#section_dtm_slv_zz}

U kunt als volgt de Livefyre Android-SDK toevoegen aan uw project in Eclipse:

1. Krijg de recentste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) van GitHub.
1. Begin met een bestaand project of maak een nieuw project.
1. Ga naar **[!UICONTROL File > Import > General > Existing Project into Workspace]** om StreamHub-Android-SDK in uw werkruimte te importeren.
1. Blader en selecteer StreamHub-Android-SDK; het moet nu in de pakketverkenner worden getoond .
1. Klik met de rechtermuisknop op uw project en selecteer **[!UICONTROL Properties,]** vervolgens het tabblad Android.
1. Onder de sectie van de Bibliotheek, selecteer **[!UICONTROL Add button,]** dan StreamHub-Android-SDK van de lijst van bibliotheken.
1. Klik op **[!UICONTROL Apply]** en **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

U voegt als volgt de Livefyre Android SDK toe aan uw project in Android Studio:

1. Krijg de recentste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) van GitHub.
1. Begin met een bestaand project of maak een nieuw project.
1. Klik met de rechtermuisknop op uw project en selecteer **[!UICONTROL Open Module Settings]**.
1. Selecteer de **[!UICONTROL +]** knop in de linkerbovenhoek van het venster.
1. Selecteer **[!UICONTROL Import Existing Project.]** (In een nieuwe versie van Android-studio vindt u **[!UICONTROL Import Existing Project]** onder **[!UICONTROL More Modules]**.)

1. Blader en selecteer StreamHub-Android-SDK.

Android Studio kan u vragen de SDK om te zetten in een grijze versie. Als dit gebeurt, selecteert u **[!UICONTROL next]** vervolgens **[!UICONTROL finish]**.

Ga naar **projectmap > toepassingsmap > build.gradle** onder afhankelijkheden om de volgende afhankelijkheid toe te voegen:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Zorg ervoor dat de volgende regel in uw **projectomslag > settings.gradle** dossier is:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>U kunt configuraties aanpassen vanuit Config.java.

## Clients {#section_yfq_blv_zz}

De StreamHub Android SDK stelt verscheidene cliëntklassen bloot die kunnen worden gebruikt om levende API eindpunten aan te vragen:

* **AdminClient** Exchange a user authentication token for user information, keys, and other metadata.

* **BootstrapClient** krijgt recente inhoud en meta-gegevens over een bepaalde Inzameling.

* **De Opiniepeiling van StreamClient** een stroom voor een Inzameling om nieuwe, bijgewerkte, en geschrapte inhoud terug te winnen.

* **WriteClient** Post, vlag, en als inhoud in een Inzameling.

