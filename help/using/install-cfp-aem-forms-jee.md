---
title: Cumulatieve herstelpakketten installeren op AEM Forms JEE
description: Overzicht van de stappen voor de installatie en configuratie van het cumulatieve fixpack (CFT) op AEM Forms JEE.
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 953752d32794cbc32fd6e9747928b809bfe68066
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Cumulatieve reparatiepakketten installeren op AEM [!DNL &#x200B; Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## GFP installeren op AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Voer de volgende stappen uit om het cumulatieve reparatiepakket te installeren op AEM 6.3 [!DNL Forms JEE] .

1. Om AEM 6.3 [!DNL Forms JEE] installer voor GVB te verkrijgen, contacteer [ Steun van Adobe ](https://experienceleague.adobe.com/nl?support-solution=General&support-tab=home#support).
1. Voer het gestreken installatieprogramma in werking en vorm AEM [!DNL Forms JEE] zoals die in [ wordt beschreven installeer en vorm AEM  [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installeer de nieuwste AEM GVB 6.3.3.x
1. Installeer het [!DNL Forms] toe:voegen-op pakket voor GFP van AEM [ 6.3.3.x ](aem-forms-releases.md)

### AEM [!DNL Forms JEE] -bundelpakket installeren {#install-aem-forms-jee-bundles-package}

Het AEM [!DNL &#x200B; Forms JEE] -pakket (aemfd-jee-bundles-package-6.3CFP1; versie 1.0.2) biedt [!DNL Forms] Gebruiker op AEM [!DNL Forms JEE] dezelfde rechten en mogelijkheden als in AEM [!DNL Forms OSGi] . Controleer de geïnstalleerde pakketten in Package Manager en installeer het pakket als dit nog niet is geïnstalleerd.

### Meer instructies voor CQ-4208044 {#additional-instructions-for-cq}

Als u de AEM 6.3 [!DNL Forms JEE] -server met de Oracle-database gebruikt, configureert u de volgende instellingen na de implementatie van het GVB1, dat wil zeggen nadat de Configuration Manager is uitgevoerd. Deze instelling is vereist voor het synchroniseren van gebruikers, groepen en groepsleden wanneer de domeinsynchronisatie van de onderneming wordt uitgevoerd.

1. Login aan **Admin** UI.
1. Ga naar **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Exporteer het bestand config.xml.
1. Wijzig de ingang voor &quot;`groupMemberDBQueryBatchSize`&quot;onder uw domeinconfiguraties in *config.xml*. Voorbeeld:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Importeer het gewijzigde bestand opnieuw en voer vervolgens de synchronisatie opnieuw uit.

## GFP installeren op AEM 6.2 [!DNL &#x200B; Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Voer de volgende stappen uit om het cumulatieve reparatiepakket te installeren op AEM 6.2 [!DNL Forms JEE] .

1. Om AEM 6.2 [!DNL Forms JEE] installer voor GFP te verkrijgen, contacteer [ Steun van Adobe ](https://experienceleague.adobe.com/nl?support-solution=General&support-tab=home#support).
1. Voer het gestreken installatieprogramma in werking en vorm AEM [!DNL Forms JEE] zoals die in [ wordt beschreven installeer en vorm AEM  [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installeer AEM Hotfix 12785 versie 7.0.
1. Installeer AEM 6.2 Service Pack 1.
1. Installeer de nieuwste release-notes-aem-6-2-cumulation-pack.md.
1. Installeer het [!DNL Forms] Add-on-pakket voor AEM 6.2 Service Pack 1 gestreken.

### AEM [!DNL Forms JEE] -bundelpakket installeren {#install-aem-forms-jee-bundles-package-1}

Het AEM Forms JEE-pakket (aemfd-jee-bundles-package-6.2CFP5; versie 1.0.2) biedt [!DNL Forms] Gebruiker op AEM [!DNL Forms JEE] dezelfde rechten en mogelijkheden als op AEM [!DNL Forms OSGi] . Controleer de geïnstalleerde pakketten in Package Manager en installeer het pakket als dit nog niet is geïnstalleerd.

### Time-out configureren voor bewerkingen op componentniveau (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Post AEM 6.2 GFP4, kunt u de volgende instructies gebruiken om onderbreking voor de verrichtingen van DSC te vormen voor het geval u problemen wegens onderbreking tijdens het verbeteringsproces ziet.

De plaatsing van DSC vergt een veranderlijke tijd toe te schrijven aan welke het zou kunnen ontbreken. Als u de time-out van DSC-bewerkingen zoals Installeren, Laden, Starten en Stoppen wilt wijzigen, moet u de `adobe.component.registry.timeout` instellen met behulp van het JVM-argument met de optie `-D` .

Geef de waarde voor de toets op in seconden. Bijvoorbeeld: `-Dadobe.component.registry.timeout=300`

U kunt de onderbrekingen op componentenniveau ook veranderen gebruikend de volgende drie eigenschappen:

1. `adobe.all-component.timeout`: overschrijft de time-outs van alle services van het product.
1. `adobe.<serviceName>.timeout`: overschrijft de time-out alleen voor de service (&lt;serviceName>) die in de sleutel wordt vermeld. Als de waarde op de dienstniveau wordt geplaatst, dan beschrijft het gebruiken van dit bevel slechts de onderbrekingswaarde voor de gespecificeerde dienst als het op het niveau van de Toepassing wordt geplaatst.
1. `adobe.<serviceName>.<operationName>.timeout`: hiermee wordt alleen de time-out voor de bewerking van de specifieke service overschreven (&lt;serviceName>.&lt;operationName>) die in de sleutel wordt vermeld. Als de waarde op het niveau van de Verrichting wordt geplaatst, dan beschrijft het gebruiken van dit bevel slechts de onderbrekingswaarde voor de gespecificeerde dienst als het op het niveau van de Toepassing of het niveau van de Dienst wordt geplaatst.

**Voorbeelden:**

Gebruik de volgende opdrachten om de time-out in te stellen op componentniveau:

1. Om de onderbreking van alle de dienstverrichtingen aan 600 sec te plaatsen:

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Als u de time-out voor de `DesigntimeService` -bewerking wilt instellen op 500 sec, gebruikt u:

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Als u de time-out voor de `DesigntimeService's previewLCA` -bewerking wilt instellen op 700 sec, gebruikt u:

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. U kunt als volgt de waarde van `DSC operations` (zoals laden en installeren) instellen op 600 sec:

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## AEM installeren en configureren [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Maak een back-up van de map /Implementeren. Dit is vereist als u besluit de snelle oplossing te verwijderen.
1. Stop uw toepassingsserver.
1. Pak het archiefbestand van het patch-installatieprogramma uit op de vaste schijf.
1. In de map met de naam volgens het besturingssysteem dat u gebruikt:

   **Vensters**

   Navigeer naar de map op de installatiemedia of in de map waarnaar u het installatieprogramma hebt gekopieerd.

   * (`Windows 32-bit`): `Disk1\InstData\Windows\VM`
   * (`Windows 64-bit`): `Disk1\InstData\Windows_64bit\VM`

   Dubbelklik vervolgens op het bestand met de naam:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®, Solaris™, AIX®**

   Navigeer naar de juiste map:

   * (Linux®): Disk1/InstData/Linux/NoVM
   * (Solaris™): Disk1/InstData/Solaris/NoVM
   * (AIX®): Disk1/InstData/AIX/VM

   Van een bevelherinnering, type:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   De installatiewizard wordt gestart om u door de installatie te begeleiden.

1. Klik in het deelvenster Inleiding op **[!UICONTROL Next]** .
1. Controleer in het scherm Install Folder kiezen of de standaardlocatie correct is voor uw bestaande installatie. Of klik op **[!UICONTROL Browse]** om de alternatieve map te selecteren waarin AEM [!DNL Forms] is geïnstalleerd en klik vervolgens op **[!UICONTROL Next]** .
1. Lees de informatie over het overzicht van reparaties in Snel repareren en klik op **[!UICONTROL Next]** .
1. Lees de informatie over het pre-installatieoverzicht en klik op **[!UICONTROL Install]** .
1. Wanneer de installatie is voltooid, klikt u op **[!UICONTROL Next]** om de snelle reparatie-updates toe te passen op de geïnstalleerde bestanden.
1. Het selectievakje Configuratiebeheer starten is standaard ingeschakeld. Klik op **[!UICONTROL Done]** om Configuratiebeheer uit te voeren.

   Als u Configuration Manager later wilt uitvoeren, schakelt u de optie **[!UICONTROL Start Configuration Manager]** uit voordat u op **[!UICONTROL Done]** klikt. U kunt de Manager van de Configuratie later beginnen gebruikend het aangewezen manuscript in *`[AEM_forms_root]`/configurationManager/bin* folder.

1. Afhankelijk van uw toepassingsserver, kies één van de volgende documenten en volg de instructies in *het Vormen en het Opstellen van AEM[!DNL Forms]* sectie.

   Voor AEM [!DNL Forms] 6.3 raadpleegt u:

   * AEM [!DNL Forms] voor JBoss® installeren en implementeren
   * AEM [!DNL Forms] voor WebSphere® installeren en implementeren
   * AEM voor WebLogic installeren en implementeren [!DNL Forms]

1. Start de AEM [!DNL Forms] JEE-server opnieuw.
