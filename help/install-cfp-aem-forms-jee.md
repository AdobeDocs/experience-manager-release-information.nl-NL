---
title: Cumulatieve herstelpakketten installeren op AEM Forms JEE
description: Overzicht van stappen voor installatie en configuratie van Cumulative Fix Pack (GVB) op AEM Forms JEE
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 69f4db4e2ef94c370ed590ec7e9859781a909270
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Cumulatieve herstelpakketten installeren op AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## GFP installeren op AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Voer de volgende stappen uit, in de gespecificeerde opeenvolging, om cumulatief fixpak op AEM 6.3 [!DNL Forms JEE] te installeren.

1. Neem contact op met [Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html) voor het installatieprogramma van AEM 6.3 [!DNL Forms JEE] voor het GVB.
1. Voer het GVB-installatieprogramma uit en configureer AEM [!DNL Forms JEE] zoals beschreven in [AEM installeren en configureren [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installeer de nieuwste AEM GVB [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. Het [!DNL Forms] Add-on-pakket installeren voor AEM GVB [6.3.3.x](aem-forms-releases.md)

### AEM [!DNL Forms JEE] bundelpakket installeren {#install-aem-forms-jee-bundles-package}

AEM [!DNL  Forms JEE]-pakket (aemfd-jee-bundles-package-6.3GVB1; versie 1.0.2) biedt [!DNL Forms] Gebruiker op AEM [!DNL Forms JEE] dezelfde rechten en mogelijkheden als op AEM [!DNL Forms OSGi]. Controleer de geïnstalleerde pakketten in Package Manager en installeer het pakket als dit nog niet is geïnstalleerd.

### Aanvullende instructies voor CQ-4208044 {#additional-instructions-for-cq}

Als u AEM 6.3 [!DNL Forms JEE] server met het gegevensbestand van het Oracle gebruikt, vorm de volgende montages na plaatsing van GVB1, namelijk nadat de Manager van de Configuratie in werking wordt gesteld. Deze instelling is vereist voor het synchroniseren van gebruikers, groepen en groepsleden wanneer de domeinsynchronisatie van de onderneming wordt uitgevoerd. Zie CQ-4208044 in [AEM 6.3 release notes](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Meld u aan bij de gebruikersinterface **Admin**.
1. Ga naar **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Exporteer het bestand config.xml.
1. Wijzig de ingang voor &quot; `groupMemberDBQueryBatchSize`&quot;onder uw domeinconfiguraties in *config.xml*. Voorbeeld:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. Importeer het gewijzigde bestand opnieuw en voer vervolgens de synchronisatie opnieuw uit.

## GFP installeren op AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Voer de volgende stappen uit, in de gespecificeerde opeenvolging, om cumulatief fixpak op AEM 6.2 [!DNL Forms JEE] te installeren.

>[!NOTE]
>
>Als u AEM 6.2 [!DNL Forms OSGi] gebruikt, volgt u de installatie-instructies in [AEM 6.2 Opmerkingen bij de GFP-release.](release-notes-aem-6-2-cumulative-fix-pack.md)

1. Neem contact op met [Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html) voor het installatieprogramma van AEM 6.2 [!DNL Forms JEE] voor het GVB.
1. Voer het GVB-installatieprogramma uit en configureer AEM [!DNL Forms JEE] zoals beschreven in [AEM installeren en configureren [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installeer AEM Hotfix 12785 versie 7.0.
1. Installeer [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Installeer de nieuwste [AEM 6.2 Service Pack1 GVB](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Installeer het [!DNL Forms] Add-on-pakket voor [AEM 6.2 Service Pack 1 GVB](aem-forms-releases.md).

### AEM [!DNL Forms JEE] bundelpakket installeren {#install-aem-forms-jee-bundles-package-1}

AEM Forms JEE-pakket (aemfd-jee-bundles-package-6.2GVB5; versie 1.0.2) biedt [!DNL Forms] Gebruiker op AEM [!DNL Forms JEE] dezelfde rechten en mogelijkheden als op AEM [!DNL Forms OSGi]. Controleer de geïnstalleerde pakketten in Package Manager en installeer het pakket als dit nog niet is geïnstalleerd.

### Time-out configureren voor bewerkingen op componentniveau (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Post AEM 6.2 GFP4, kunt u de volgende instructies gebruiken om onderbreking voor de verrichtingen van DSC te vormen voor het geval u problemen wegens onderbreking tijdens het verbeteringsproces ziet. (Zie NPR-16774 in [AEM 6.2 Opmerkingen bij de release van GVB4](release-notes-aem-6-2-cumulative-fix-pack.md)).

De plaatsing van DSC vergt een veranderlijke tijd toe te schrijven aan welke het zou kunnen ontbreken. Als u de time-out van DSC-bewerkingen zoals Installeren, Laden, Starten en Stoppen wilt wijzigen, moet u `adobe.component.registry.timeout` instellen met behulp van het JVM-argument met de optie -D.

Geef de waarde voor de toets op in seconden. Bijvoorbeeld: `-Dadobe.component.registry.timeout=300`

U kunt de onderbrekingen op componentenniveau ook veranderen gebruikend de volgende drie eigenschappen:

1. `adobe.all-component.timeout`: beschrijft de onderbrekingen van alle Diensten van het Product.
1. `adobe.<serviceName>.timeout`: overschrijft de onderbreking slechts voor de dienst (&lt;servicename>) die in de sleutel wordt vermeld. Als de waarde op de dienstniveau wordt geplaatst, dan beschrijft het gebruiken van dit bevel slechts de onderbrekingswaarde voor de gespecificeerde dienst als het op het niveau van de Toepassing wordt geplaatst.
1. `adobe.<serviceName>.<operationName>.timeout`: Het beschrijft slechts de onderbreking voor de specifieke verrichting van de dienst(&lt;servicename>.&lt;operationname>) genoemd in de sleutel. Als de waarde op het niveau van de Verrichting wordt geplaatst, dan beschrijft het gebruiken van dit bevel slechts de onderbrekingswaarde voor de gespecificeerde dienst als het op het niveau van de Toepassing of het niveau van de Dienst wordt geplaatst.

**Voorbeelden:**

Gebruik de volgende opdrachten om de time-out in te stellen op componentniveau:

1. Om de onderbreking van alle de dienstverrichtingen aan 600 sec te plaatsen:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Als u de time-out van de `DesigntimeService`-bewerkingswaarden wilt instellen op 500 sec, gebruikt u:

   &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot; instellen

1. Als u de time-out van de `DesigntimeService's previewLCA`-bewerkingswaarden wilt instellen op 700 sec, gebruikt u:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Als u `DSC operations` zoals laden, installeren enzovoort wilt instellen op 600 sec., gebruikt u:

   &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot; instellen

## AEM [!DNL Forms JEE] installeren en configureren {#install-and-configure-aem-forms-jee}

1. Maak een back-up van de map /Implementeren. Dit is vereist als u besluit de snelle oplossing te verwijderen.
1. Stop uw toepassingsserver.
1. Pak het archiefbestand van het patch-installatieprogramma uit op de vaste schijf.
1. In de map met de naam volgens het besturingssysteem dat u gebruikt:

   **Windows**

   Navigeer naar de juiste map op de installatiemedia of -map op de vaste schijf waarnaar u het installatieprogramma hebt gekopieerd:

   * (Windows 32-bits): Disk1\InstData\Windows\VM
   * (Windows 64-bits): Disk1\InstData\Windows_64bit\VM

   Dubbelklik vervolgens op het bestand met de naam:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Navigeer naar de juiste map:

   * (Linux): Disk1/InstData/Linux/ NoVM
   * (Solaris): Disk1/InstData/Solaris/ NoVM
   * (AIX): Disk1/InstData/AIX/VM

   Van een bevelherinnering, type:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Hiermee wordt een installatiewizard gestart die u door de installatie begeleidt.

1. Klik in het deelvenster Inleiding op **[!UICONTROL Next]**.
1. Controleer in het scherm Installatiemap kiezen of de standaardlocatie die wordt weergegeven juist is voor uw bestaande installatie of klik op **[!UICONTROL Browse]** om de alternatieve map te selecteren waarin AEM [!DNL Forms] momenteel is geïnstalleerd en klik op **[!UICONTROL Next]**.
1. Lees de informatie van het Overzicht van de Reparatie van de Snelle Moeilijke situatie en klik **[!UICONTROL Next]**.
1. Lees de informatie over het Pre-Installation Summary en klik op **[!UICONTROL Install]**.
1. Wanneer de installatie is voltooid, klikt u op **[!UICONTROL Next]** om de snelle reparatie-updates toe te passen op de geïnstalleerde bestanden.
1. Het selectievakje Configuratiebeheer starten is standaard ingeschakeld. Klik **[!UICONTROL Done]** om de Manager van de Configuratie in werking te stellen.

   Als u Configuratiebeheer later wilt uitvoeren, schakelt u de optie **[!UICONTROL Start Configuration Manager]** uit voordat u **[!UICONTROL Done]** klikt. U kunt de Manager van de Configuratie later beginnen gebruikend het aangewezen manuscript in *`[AEM_forms_root]`/configurationManager/bin* folder.

1. Afhankelijk van uw toepassingsserver kiest u een van de volgende documenten en volgt u de instructies in de sectie *AEM configureren en implementeren[!DNL Forms]*.

   Voor AEM [!DNL Forms] 6.3, verwijs naar:

   * [AEM [!DNL Forms] voor JBoss installeren en implementeren](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [AEM [!DNL Forms] for WebSphere installeren en implementeren](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [AEM [!DNL Forms] for WebLogic installeren en implementeren](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   Voor AEM [!DNL Forms] 6.2 raadpleegt u:

   * [AEM [!DNL Forms] voor JBoss installeren en implementeren](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [AEM [!DNL Forms] for WebSphere installeren en implementeren](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [AEM [!DNL Forms] for WebLogic installeren en implementeren](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   Zie voor AEM Forms 6.1:

   * [AEM [!DNL Forms] voor JBoss installeren en implementeren](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [AEM [!DNL Forms] for WebSphere installeren en implementeren](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [AEM [!DNL Forms] for WebLogic installeren en implementeren](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Start AEM [!DNL Forms] JEE-server opnieuw.
