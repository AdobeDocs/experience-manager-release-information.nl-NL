---
title: AEM 6.3 Cumulatieve Fix Pack
description: AEM 6.3 Opmerkingen bij de release Cumulative Fix Pack.
source-git-commit: 3c798116db7314f4220f8a183a989c2b37678054
workflow-type: tm+mt
source-wordcount: '15906'
ht-degree: 0%

---

# AEM 6.3 Opmerkingen bij de release Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Gegevens vrijgeven {#release-information}

| **Product** | Adobe Experience Manager |
|---|---|
| **Versie** | 6,3 |
| **Geen** | Cumulatief Fix Pack 6.3.3.8 op [PackageShare](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8), [Software Distribution(Beta)](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Vereiste** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **Algemene beschikbaarheid** | 5 maart 2020 |

### Cumulatief reparatiepakket {#cumulative-fix-pack}

Adobe introduceerde een single-delivery model voor het vrijgeven van moeilijke situaties. In plaats van hotfixes voor individuele kwesties vrij te geven, geeft Adobe nu een Cumulatief Pak van de Correctie (GVB) elke maand (onderworpen aan het overgaan kwaliteitscontroles) vrij. Een gestreken gemeenschappelijk visserijbeleid is een geaggregeerd inhoudspakket voor veelvoudige moeilijke situaties. GFPs omvat hoofdzakelijk insectenmoeilijke situaties maar zou ook de Pakken van de Eigenschap kunnen omvatten. Ze hebben de volgende voordelen ten opzichte van afzonderlijke hotfix-releases:

* Gecumuleerd van aard (een GVB bevat bijvoorbeeld vastleggingen die via eerdere GVB&#39;s zijn geleverd)
* Meer kwaliteitsborging
* Vereenvoudigde installatie (de gebruiker installeert een gestreken fijn-wit als één enkel pakket dat geen gebiedsdelen, behalve het recentste de dienstpak heeft)

Zie [Definities van &quot;Maintenance Release Vehicle&quot;](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html) voor meer informatie over gestreken fijn papier en andere typen vrijkomingen.

## Over de release {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018 omvat.

AEM Cumulative Fix Pack 6.3.3.8 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.20.

>[!CAUTION]
>
>Het toepassen van GVB zonder verenigbaarheid tussen geïnstalleerde eigenschapspakketten te bevestigen kan in systeemmislukking of verlies van douaneconfiguraties resulteren, die van steun om kunnen vereisen te herstellen om op te lossen.

>[!NOTE]
>
>Voor AEM gevallen met een lagere versie dan 6.3.3.0 raadt Adobe aan om ing SP/GVB via de installatiemap te implementeren voor klanten met een groot aantal gebruikers op AEM.

>[!NOTE]
>
>MongoDB Enterprise 3.6 wordt ondersteund vanaf AEM versie 6.3.3.1.

## Lijst met problemen {#changes}

In deze sectie worden alle problemen en hotfixes vermeld die in het huidige GVB zijn opgenomen.

Bovendien omvat dit GVB hotfixes die in [vorige cumulatieve fixpakken](#previous) worden geleverd.

### Assets {#assets}

* Add aan de pagina van de Inzameling toont niet alle beschikbare inzamelingen in de Mening van de Kaart terwijl het toevoegen van activa aan inzameling (NPR-32537).

### Sites {#sites}

* Wanneer u een parsys en een component binnen het selecteert en de toetsenbordkortere weg gebruikt om geselecteerde punten te schrappen, schrapt de actie zowel de component als zijn ouderparsys (NPR-32071).
* Wanneer de eigenschappen van een pagina worden opgeslagen, wordt een onjuist knooppunt gemaakt (NPR-31774).

### Integrations {#integrations}

* ReportSuitesServlet is kwetsbaar voor SSRF (NPR-32162).

### Campagne gericht {#campaign-targeting}

* De inhoud van een component is gewijzigd, in de instantie Auteur en vervolgens geactiveerd, in de instantie Publish niet zichtbaar tot de component opnieuw is gestart **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 en NPR-32232).
* Contexthub-uitvoeringen crashen bij publicatie (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe I/O is niet geïntegreerd met Adobe Experience Manager 6.3 voor Brand Portal (NPR-32056).

### Forms {#forms}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie [AEM Forms Release](aem-forms-releases.md) voor meer informatie.

#### Forms-invoegtoepassing {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het absoluut noodzakelijk om het add-on pakket van AEM Forms te installeren na het installeren van om het even welk AEM Service Pack, Cumulative Fix Pack, of het Pak van de Eigenschap.

* Designer: Als de coderingsoptie is ingeschakeld, verdwijnt de subformulierrand in de gegenereerde PDF-uitvoer (NPR-32324 en NPR-32545).
* Designer: Als een tabel samengevoegde cellen bevat, mislukt de toegankelijkheidstest voor het PDF-uitvoerbestand dat is geconverteerd van een XDP-formulier met de uitvoerservice (NPR-32068).
* Documentbeveiliging: Een beveiligd PDF-bestand kan niet offline worden geopend met de optie `DisableGlobalOfflineSynchronizationData` ingesteld op `True` (NPR-32080).

## Hotfixes en de Pakken van de Eigenschap inbegrepen in vorige Cumulatieve Pakken van de Moeilijke situatie {#previous}

### Cumulatief Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018 omvat.

AEM Cumulative Fix Pack 6.3.3.7 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

### Activa {#assets-1}

* Elementen die zijn geselecteerd (in de kolomweergave in de aanraakinterface) voordat de filteroptie is geselecteerd in de vervolgkeuzelijst Alleen inhoud en vervolgens de verplaatsingsoptie is geselecteerd, worden ook verplaatst (NPR-30693).
* De variabele `${extension}` wordt niet gerenderd in auteurinstantie op werkschemaverwerking (NPR-31694).
* De vervalwaarde (de tijd van het cliëntgeheime voorgeheugen aan levende) die voor de Hybride wijze van Dynamic Media wordt gevormd wordt niet herhaald aan de leveringsmilieu van Dynamic Media (NPR-31114).
* Elementen worden gerepliceerd naar instantie Publiceren vanuit een instantie Auteur die wordt uitgevoerd op Dynamic Media - Scene7-implementatie, zelfs na gebruik van standaardfilters (NPR-30856).

### Sites {#sites-1}

* Pagina-eigenschappen van een master pagina kunnen niet worden geladen en er wordt een NullPointerException geretourneerd. Het probleem is opgelost door de eigenschap cq:blueprint (NPR-30901) toe te voegen.
* De configuraties van de rollout worden niet behoorlijk teruggewonnen van blueprintConfig op de wortelknoop. De deactivering wordt geactiveerd voor zowel blauwdrukken als live kopieën. De deactivering mag alleen worden geactiveerd voor de blauwdruk (NPR-30866).
* Wanneer een gebruiker een pagina rolt-uit, toont de de configuratiedialoog dubbele levende exemplaarwegen (NPR-30438).
* De basislijneditor (RTE) is uit het vak. past inline font-size toe op elementen, onverwacht (NPR-31283, NPR-30922).
* Kan de campagne niet synchroniseren in de Adobe-campagne met de ontwerpimportcomponent buiten de box (NPR-30890).
* Rich Text Editor (RTE). staat niet toe om een ingebedde Lijst als lijstitem (NPR-30878) op te nemen.
* Wanneer een gebruiker de linkerspoorgebieden concentreert en een toetsenbordkortere weg gebruikt om inhoud te kleven, kleeft het de inhoud van het paginageditor klembord in plaats van de inhoud die van de linkerspoorgebieden wordt gekopieerd (NPR-31173).
* Wanneer een gebruiker een inhoudsfragment bewerkt, wordt de reeds verwijderde variatie van het inhoudsfragment hersteld (NPR-31272).
* AEM Site heeft geen optie om een taalkopie te maken (NPR-30690).
* De acties van de pagina-editor bevatten niet de besturingselementen voor het live kopiëren (NPR-30613).

### Gemeenschappen {#communities}

* Activiteiten en aanmeldingstitels zijn inconsistent (NPR-30940).
* Rapporten over analysemogelijkheden worden niet gevuld in AEM auteursomgeving. Er wordt een lege pagina weergegeven (NPR-30905).
* Paginering werkt niet correct in Gemeenschapsblogs (NPR-30827).

### Stichting {#foundation}

* Updates in de configuratie van de buffergrootte voor de op Jetty-Gebaseerde dienst van HTTP worden niet bewaard (NPR-30925).

### Forms {#forms-1}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie [AEM Forms Release](aem-forms-releases.md) voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het absoluut noodzakelijk om het add-on pakket van AEM Forms te installeren na het installeren van om het even welk AEM Service Pack, Cumulative Fix Pack, of het Pak van de Eigenschap.

#### Adaptieve Forms {#adaptive-forms}

* Zwevende waarden die zijn berekend met een script, worden niet correct weergegeven in een vorm die deel uitmaakt van een formset (NPR-30802).

#### HTML5 Forms {#html-forms}

* Als u HTML5-voorbeeld van een XDP-formulier genereert, wordt een flikkering weergegeven terwijl exemplaren van een subformulier worden toegevoegd (NPR-30908).

### Forms JEE-installatieprogramma {#forms-jee-installer}

#### Document Services {#document-services}

* OutputService geeft een onjuiste reactie weer nadat een patch is toegepast om HTML-problemen op te lossen (NPR-31504).

#### PDFG-service {#pdfg-service}

* Maximale aantal hergebruik met JMX-console wordt niet weergegeven voor HTML2PDF-service (NPR-30305).

#### Foundation JEE {#foundation-jee}

* Max. aantal hergebruik met JMX-console wordt niet weergegeven voor HTML2PDF-service (NPR-30136).

### Cumulatief Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018 omvat.

AEM Cumulative Fix Pack 6.3.3.6 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

### Activa {#assets-2}

* De videosamenvoeging door Dynamische Video keert slechts de hoogste 100 punten in resultaatreeks terug. NPR-30441; Hotfix voor CQ-4213561
* Verbindingsprobleem met Adobe Smart Tag via Datapower. NPR-30026: Hotfix voor CQ-4269457
* Het uitpakken van een archief met een map met een procentteken (%) in de naam kan niet worden geopend via de interface Middelen. NPR-29989: Hotfix voor CQ-4270467
* De verwerking van subelementen van grote PDF-bestanden veroorzaakt een uitzondering OutOfMemoryError (OOME). NPR-29851: Hotfix voor CQ-4269574

### Sites {#sites-2}

* De fout van ContextHub tijdens AEM en de integratie van de Campagne. NPR-30624: Hotfix voor CQ-4250790
* De metagegevenseigenschappen &#39;onTime&#39; of &#39;offTime&#39; die zijn opgeslagen op elementen, worden niet teruggeroepen als de AEM server opnieuw wordt gestart. NPR-30412: Hotfix voor CQ-4272784
* Tijdens het produceren van een uitvoer CSV, die douanekolommen voor de lijstmening toevoegt breken het rapport. NPR-30208: Hotfix voor CQ-4273344
* OTB-rapporten in /etc/reports/ werken niet correct en de historische gegevensgrafiek wordt niet weergegeven. NPR-30016: Hotfix voor CQ-4220180
* De waarde van de requestType-parameter wordt gekopieerd naar de waarde van een HTML-tagkenmerk dat is ingekapseld in dubbele aanhalingstekens. NPR-29832: Hotfix voor CQ-4255365

### Gemeenschappen {#communities-1}

* Probleem met dubbele inhoud met AEM Communities-moderatieconsole. NPR-30667: Hotfix voor CQ-4276829

### Vertaling {#translation}

* Probleem met vertaling - Slechts een paar componenten worden omgezet met behulp van Machine Translation. NPR-30079: Hotfix voor CQ-4273764
* Als u het vertaalframework gebruikt, treedt er een fout op wanneer u pagina&#39;s toevoegt aan meerdere vertaaltaken. NPR-29746: Hotfix voor CQ-4270953

### Forms {#forms-2}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie [AEM Forms Release](aem-forms-releases.md) voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het absoluut noodzakelijk om het add-on pakket van AEM Forms te installeren na het installeren van om het even welk AEM Service Pack, Cumulative Fix Pack, of het Pak van de Eigenschap.

#### HTML5 Forms {#html-forms-1}

* Wanneer u in de modus Bladeren een HTML5-formulier leest met toegang tot niet-visuele desktops, wordt in de Chrome-browser vóór elke SVG (Scalable Vector Graphic) in het formulierontwerp &quot;graphic&quot; gelezen. NPR-30451: Hotfix voor CQ-4274732

#### Forms - Ondersteunende integratie {#forms-backend-integration}

* Kan de service/gegevensbron voor de databaseverbinding niet zien tijdens het maken van het FDM (Form Data Model). NPR-30108: Hotfix voor CQ-4273359

### Forms JEE-installatieprogramma {#forms-jee-installer-1}

#### Forms - Document Services {#forms-document-services}

* Wanneer een laadtest wordt uitgevoerd op HTML naar PDF-service, mislukt dit met een fout en worden instellingen voor bestandstypen verwijderd van AEM formulierserver. NPR-30111, NPR-30086: Hotfix voor CQ-4271495

### Cumulatief Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.5 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.17.

### Activa {#assets-3}

* Bijgewerkte interface DAM DMGateway voor S3 multipart steun. NPR-29740: Hotfix voor Q-4226303
* Kan een afbeeldingsuitvoering op een video-element niet verwijderen van de pagina met elementdetails. NPR-29417: Hotfix voor CQ-4268675
* De eigenaar kan geen persoonlijke map in een privémap maken. NPR-29397: Hotfix voor CQ-4229830
* Als u een Adobe Illustrator-illustratiebestand van meer dan 2 GB uploadt, wordt een Java-heap-ruimtefout gegenereerd. NPR-29265: Hotfix voor CQ-4226217
* Middelen worden onbruikbaar nadat de DAM CQ Mime Type Service tekst voor m3u8 toepast. NPR-29259: Hotfix voor CQ-4264052
* De optie Maken werkt niet wanneer u verzamelingen in Edge wilt maken. NPR-29248: Hotfix voor CQ-4265699 en CQ-4265438
* Bij Delen van koppelingen naar middelen worden voor bepaalde middelen in de map lege grijze kaarten weergegeven. NPR-29831: Hotfix voor CQ-4270187
* De nieuwe tags die aan elementen zijn toegevoegd, kunnen niet worden opgeslagen en verdwijnen uit de eigenschappen. Hotfix voor CQ-4271931, CQ-4270476

### Sites {#sites-3}

* CoralUI, wanneer gebruikt met Multifield, slaat fileReferenceParameter op componentenniveau in plaats van multifield niveau op. NPR-29535: Hotfix voor CQ-4266129
* Probleem tijdens het vergelijken van de nieuwste en huidige paginaversie op AEM 6.3.3.3. NPR-29532: Hotfix voor CQ-4269639
* Het padveld wordt geopend op het hoofdpad, ongeacht het pad dat u wilt zoeken. NPR-29398: Hotfix voor CQ-4268897
* (Experience Fragments) FacebookApplication#setUpApp gebruikt verouderde API, die niet meer werkt. NPR-29213: Hotfix voor CQ-4266630
* Er wordt een foutmelding gegenereerd wanneer componenten aan de WCM-pagina worden toegevoegd wanneer minificatie op de instantie is ingeschakeld. NPR-29476: Hotfix voor CQ-4266197
* Lege eigenschappen en meerdere eigenschappen worden tijdens de rollout niet door blauwdruk overgedragen. Actieve kopie herstellen met blauwdruk werkt niet voor componenten.NPR-29252: Hotfix voor CQ-4264928, CQ-4264926, CQ-4267722
* Het minimaliseren van Rich Text Editor van volledig scherm in de bronbewerkingsmodus leidt tot verlies van inhoud. NPR-28838: Hotfix voor CQ-4260584

### Gemeenschappen {#communities-2}

* Bezoekers en leden zonder moderatorrechten kunnen niet-goedgekeurde en hangende berichten zien door de URL te plakken. NPR-29726: Hotfix voor CQ-4271124
* Hoge responstijd tot 40-50 seconden wordt waargenomen bij het aanmelden bij de gebruiker voor de Gemeenschap. NPR-29679: Hotfix voor CQ-4269444
* Kan het wachtwoord niet opnieuw instellen wanneer u bent aangemeld met een andere gebruikersnaam en e-mail omdat de sleutel wordt gegenereerd met een verwisselde gebruikersnaam en e-mail. NPR-29281: Hotfix voor CQ-4268694

### Ervaringsfragmenten {#experience-fragments}

* Kan ervaringsfragmenten niet exporteren naar doel wanneer een slimme afbeelding wordt gebruikt. Hotfix voor CQ-4269606

### Replicatie {#replication}

* De component van de Agent van de replicatie is vatbaar voor een kwetsbaarheid die gevoelige informatie aan onbevoegde gebruikers openbaart. NPR-29613: Hotfix voor graniet-25070
* Door de gebruiker opgegeven gegevens worden niet beschermd bij uitvoer in de `cq/replication/components/agent`component, wat resulteert in een opgeslagen XSS-kwetsbaarheid (Cross-site scripting). NPR-29452: Hotfix voor CQ-4266263

### Forms {#forms-3}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie [AEM Forms Release](aem-forms-releases.md) voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-3}

* Geen nieuwe AEM Forms-oplossingen gevonden in Forms add-on-pakket.

### Forms JEE-installatieprogramma {#forms-jee-installer-2}

* Geen nieuwe AEM Forms-oplossingen gevonden in Forms JEE-installatieprogramma.

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.5

[Bestand ophalen](assets/do-not-localize/6_5-bundle-list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.5

[Bestand ophalen](assets/do-not-localize/content_packages6335.txt)

### Cumulatief Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.4 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.16.
* Time-out voor socket toegevoegd en time-out voor verbinding in Brand Portal-replicatieagents.

### Activa {#assets-4}

* Als u een archief met dezelfde naam opnieuw uploadt, worden er geen uitvoeringen gegenereerd voor de nieuwe verwerkte elementen. NPR-28643: Hotfix voor CQ-4262286
* Workflow CommandLineProcess mislukt met een bestandsnaam met één aanhalingsteken. NPR-28805: Hotfix voor CQ-4262287
* De waarden zijn verschillend tussen inzamelingspagina en de inzamelingspagina gebruikend filter. NPR-28642: Hotfix voor CQ-4261405
* CommitFailedException triggers with upload of big zip archive assets. NPR-28528: Hotfix voor CQ-4260903
* Metagegevens van mappen kunnen niet worden opgeslagen wanneer een map met speciale tekens wordt bewerkt. NPR-28211: Hotfix voor CQ-4260401
* Kan afbeeldingsuitvoeringen van een video-element niet verwijderen van de pagina Asset Details. NPR-29149: Hotfix voor CQ-4266073
* DMS7 desktop video delivery using DMComponent gebruikt progressieve download voor het afspelen van video in publish mode en streamt niet. NPR-28754: Hotfix voor CQ-4263732
* Kan voorinstellingen voor afbeeldingen niet maken/bewerken omdat de toegang tot /etc/dam/video/dynamicmedia wordt beperkt, schakelt functies voor afbeeldingsmanagers uit. NPR-28662: Hotfix voor CQ-4263022
* Als u Delen koppelt aan videobestanden die zijn gecodeerd met DMS7, ontstaan lege mappen. NPR-28851: Hotfix voor CQ-4206743
* De replicatie van AEM naar Brand Portal blijft lang vastzitten. NPR-28913: Hotfix voor CQ-4254932

### Gemeenschappen {#communities-3}

* Kan berichten met bijlagen niet openen in de map Contlook sent en inbox. NPR-28559: Hotfix voor CQ-4217072

### Sites {#sites-4}

* XSS (Cross-site scripting) in SuggestieHandler voor 6.3. NPR-28692: Hotfix voor CQ-4253821
* Diepe rollout eindigt zonder alle vertakkingen in respectieve LiveCopy te bevatten. NPR-29175: Hotfix voor CQ-4239472
* (MSM) Implementeer LiveCopyIndex met behulp van een eikenindex. NPR-29198: Hotfix voor CQ-4222472
* Het bestand &#39;koral.js&#39; bevat een kwetsbare versie van de bibliotheek &#39;handlebars.js&#39;. NPR-26973: Hotfix voor CQ-4255377
* Als een doelcomponent wordt gebruikt met een geneste container van de layout en een tekstcomponent, wordt een JavaScript-fout gegenereerd. De eigenschap currentPos of null kan niet worden gelezen wanneer tekst wordt bewerkt of op de container wordt geklikt. NPR-29077: Hotfix voor CQ-4246594
* (Aanraakinterface) Kan geen codes voor updates bulksgewijs toevoegen aan pagina&#39;s die al zijn gecodeerd met verschillende codes. NPR-28729: Hotfix voor CQ-4262922
* Als u de variatie in de weergave van de kaart opent, treedt er een fout van 500 op. NPR-28611: Hotfix voor CQ-4263571
* De rollout van een structuur die in een master map is verplaatst, leidt tot een onjuiste cq:moveTarget. NPR-28968: Hotfix voor CQ-4265280

### Integratie {#integration}

* (Cloud Service Configs) Het selectievakje &quot;geërfd van&quot; dat op het hoofdniveau wordt weergegeven, moet worden verwijderd. NPR-28771: Hotfix voor CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler gaat in een oneindige lijn en veroorzaakt updates aan knopen op publicatieinstanties. NPR-28561: Hotfix voor CQ-4263096
* Het gebruik van Brightedge-referentie mislukt vanwege een verbindingsfout. NPR-29167: Hotfix voor CQ-4265872
* Compilatieprobleem in OfferproxyTandtProvider.java vanwege ontbrekende importinstructie voor de klasse &#39;Resource&#39;: instructie missing import: import org.apache.sling.api.resource.Resource. NPR-28772

### Handel {#commerce}

* De optie Sorteren werkt niet voor elementen in de verzameling Handel. NPR-28755: Hotfix voor CQ-4213622

### Jetty {#jetty}

* Jetty uitzonderingen in error.log voor elke 302 omleidingen na het installeren van GVB2 bovenop 6.3.3. NPR-28606: Ondersteuning voor CQ-4262844

### UI - Foundation {#ui-foundation}

* Wanneer u op de tag klikt, wordt de algemene mouseup-gebeurtenis verwijderd en wordt het dialoogvenster vastgezet in de &#39;sleepbare modus&#39;. NPR-28641: Hotfix voor CUI-7294

### WCM - MSM {#wcm-msm}

* De plaatsing PushOnModify voor PageManager beweegt veelvoudige tijden van twee zittingen die een ras-voorwaarde veroorzaken. NPR-28880: Hotfix voor CQ-4266191

### Kwetsbaarheid {#vulnerability}

* Het CSRF-beschermingskader werkt niet met AEM stichtingsvormen. NPR-28612: Hotfix voor GRANITE-22231

### Forms {#forms-4}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie [AEM Forms Release](aem-forms-releases.md) voor meer informatie.

De belangrijkste markeringen voor AEM Forms zijn:

* Ingeschakelde optie om items per pagina te selecteren op de weergavepagina van de beleidsset.
* Functionaliteit voor gedeelde wachtrij voor alle browsers toegevoegd.

### Forms-invoegtoepassing {#forms-add-on-package-4}

#### Forms - Workflow {#forms-workflow}

* De gedeelde taak van de rijreactie opent een flitselement in de HTML5 werkruimte. NPR-29161: Hotfix voor CQ-4266498
* Kan niet verzenden vanuit Workspace als de knop een Umlaut-teken bevat. NPR-29014: Hotfix voor CQ-4263172

#### Forms - Documentbeveiliging {#forms-document-security}

* Schakel optie in om items per pagina te selecteren op de weergavepagina voor de beleidsset. NPR-29243: Hotfix voor CQ-4268567 &amp; CQ-4265132

#### Forms - Document Services {#forms-document-services-1}

* OSGi Forms Assembler werkt niet aan Acrobat-bestanden. NPR-29049: Hotfix voor CQ-4254426

#### HTML5 Forms {#html-forms-2}

* Er is een ander gedrag bij het voorvertonen van een XDP-bestand als PDF in vergelijking met dezelfde XDP als HTML in Designer. NPR-28602: Hotfix voor CQ-4260239

### Forms JEE-installatieprogramma {#forms-jee-installer-3}

* Geen nieuwe AEM Forms-oplossingen gevonden in Forms JEE-installatieprogramma.

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.4

[Bestand ophalen](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.4

[Bestand ophalen](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulatief Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.3 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.16.
* Paginering van de lijst met beleidsinstellingen wijzigt om 50 records per pagina te beperken.
* Toegevoegde rep: caching into Ignorable Nodes at AEM Communities User Sync Listener on publish instances.
* Label toegevoegd voor lijst- en kaartweergaveknop.
* Er is een escape-teken voor de komma opgenomen wanneer een zoekopdracht wordt uitgevoerd.
* Toegelaten steun van synthetische middelen voor inhoudsbeleid.

#### Activa {#assets-5}

* Kan geen meerdere bestanden van het type .jp2, .max, .oft, .msg downloaden. NPR-28002: Hotfix voor CQ-4210856
* De publicatie-instellingen van ImageServer worden niet gerepliceerd naar hybride levering. NPR-28329: Hotfix voor CQ-4253030

#### Gemeenschappen {#communities-4}

* Toetsenbordnavigatie ingeschakeld voor AEM Communities Enablement-componenten bij Publiceren. NPR-27739: Hotfix voor CQ-4253856
* Toegelaten toetsenbordnavigatie om het spelen van inhoud te teweegbrengen. NPR-27738: Hotfix voor CQ-4254026
* Label toegevoegd voor lijst- en kaartweergaveknop. NPR-27736: Hotfix voor CQ-4254027
* (Backport) Toegevoegde rep: caching into Ignorable Nodes at AEM Communities User Sync Listener on publish instances. NPR-27841: Hotfix voor CQ-4247234
* De speciale tekens worden voorafgegaan door escape-teken (\) in het zoekvak op UI-niveau. NPR-27839: Hotfix voor CQ-4259757
* Fout bij het zoeken naar tekens zoals ( , +,? in snel zoeken. NPR-28212: Hotfix voor CQ-4260969
* Kan opmerkingen in door de gebruiker gegenereerde inhoud niet verwijderen met behulp van API. NPR-28075: Hotfix voor CQ-4260534
* Opmerkingen die op de volgende pagina zijn geplaatst, worden geel gemarkeerd wanneer een nieuwe opmerking wordt geplaatst. NPR-28148: Hotfix voor CQ-4259681
* Kan geen berichten openen die bijlagen bevatten in verzonden vooruitzichten en inbox map. NPR-28559: Hotfix voor CQ-4217072

#### Sites {#sites-5}

* Het runnen van de Leegheid van de Versie in AEM 6.3 veroorzaakt een constant herhaalde waarschuwing in de logboeken. NPR-27750; Hotfix voor CQ-4206870
* De stijlplug-in wordt niet ondersteund in de modus Volledig scherm van de RTF-editor. NPR-27622: Hotfix voor CQ-4258674
* Lijst &#39;loaderPromises&#39; wordt niet gewist nadat het inhoudsframe is geladen in editor.js NPR-27768: Hotfix voor CQ-4205337
* Onbekwaam om malplaatjebeleid op genestelde parsys te plaatsen zonder op oudercomponent te plaatsen. NPR-27987: Hotfix voor CQ-4246095
* De componentbrowser is geen bezig met het manipuleren van gebruikersinvoer en kan daarom JavaScript-fouten genereren. NPR-27986: Hotfix voor CQ-4247590
* De pagina wordt leeg weergegeven wanneer de gebruiker het inhoudsfragment probeert te bewerken. NPR-27669
* De annotatiemarkering verdwijnt zodra de gebruiker op de annotatie klikt. BPR-27196: Hotfix voor CQ-4254423

#### Integratie {#integration-1}

* ResourceResolver lost geen veelvoudige domeinen voor de Component van het Doel op. NPR-28265: Hotfix voor CQ-107847
* LiveCopy-overervingsannulering werkt niet goed bij doelcontainers, omdat er geen acties worden weergegeven. NPR-28129: Hotfix voor CQ-4259813

#### Replicatie {#replication-1}

* DispatcherFlushRules break replicatie in 6.3.3.1 NPR-28150: Hotfix voor CQ-4261401

#### Campagne - gericht {#campaign-targeting-1}

* NullPointerException in TargetedContentManager. Hotfix voor CQ-4263485

#### Sociaal - SCORM {#social-scorm}

* Verwijzing naar SCORM-cloud (Shareable Content Object Reference Model) in de speler verwijderen. Hotfix voor CQ-4260779

#### DAM - Algemeen {#dam-general}

* Downloaden via e-mail voor delen van koppeling retourneert leeg/beschadigd postvak. Hotfix voor CQ-4259686

#### MAC - test&amp;Target-integratie {#mac-test-target-integration}

* De optie Doelcomponent configureren is niet beschikbaar voor het publiek, behalve voor het standaardpubliek. Hotfix voor CQ-4261370

#### Vertaling {#translation-1}

* Ondersteuning voor MS Translator-service inschakelen in AEM 6.3 na upgrade van MS Translator naar API v3.0. NPR-28365: Hotfix voor CQ-4259096

### Forms {#forms-5}

### Forms-invoegtoepassing {#forms-add-on-package-5}

#### Forms - Workflow {#forms-workflow-1}

* Kan geen PDF forms renderen in de HTML5-werkruimte. NPR-28059: Hotfix voor CQ-4260373

#### Forms - Document Services {#forms-document-services-2}

* Onbekwaam om het even welke Reeksen van het Beleid voorbij eerste 1000 te zien die in de mening van de Reeksen van het Beleid in de admin console wordt vermeld. NPR-28060, NPR-26047: Hotfix voor CQ-4249865
* Er wordt een uitzondering gegenereerd met de naam java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailedReason.SIGNED_IN_FUTURE, waarmee wordt voorkomen dat het kortstondige proces wordt voltooid. NPR-28652

#### Forms - Adaptieve Forms {#forms-adaptive-forms}

* Items in de vervolgkeuzelijst toevoegen/verwijderen wordt niet bijgewerkt wanneer de selectievakjes worden ingeschakeld. NPR-28224: Hotfix voor CQ-4252834

### Forms - JEE Installer {#forms-jee-installer-4}

* Geen nieuwe AEM Forms-oplossingen gevonden in Forms JEE-installatieprogramma.

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.3

[Bestand ophalen](assets/do-not-localize/6333_bundle_list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.3

[Bestand ophalen](assets/do-not-localize/content_package_list_6333.txt)

### Cumulatief Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.2 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie AEM 6.3 de versienota&#39;s van Service Pack 3.

De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.15.
* Toegevoegde steun voor het Lusje van Regels en zijn handhaving op de Omslag van Activa in het Schema van Meta-gegevens van de Omslag.
* Pagineringsondersteuning ingeschakeld om de pagina met lijsten bij publicatie te groeperen.
* Toegelaten bericht unreadCount dat met om het even welk aantal moet worden gevormd. Standaardwaarde ingesteld op 20.
* Oplossingen in externe koppelingencontrole.

#### Activa {#assets-6}

* Cascading dropdown wordt niet ondersteund op dynamische vervolgkeuzelijsten. NPR-27044; Hotfix voor CQ-4252564
* Verbeter vraag om de eigenschap te gebruiken ExpiryNotification. NPR-26999: Hotfix voor CQ-4251188
* Hiermee wordt migratie van Metagegevensschema naar Metagegevensschema van map geregeld. NPR-27771: Backport voor CQ-4257737, CQ-4257735, CQ-4259822
* De aanpassing van de verwijzing van activa ontbreekt om verwijzingen voor activa bij te werken die deel van Sling ResourceCollections uitmaken. NPR-26759: Hotfix voor CQ-4252605
* Downloaden via e-mail voor delen van koppeling retourneert een leeg/beschadigd ZIP-bestand. NPR-27997: Hotfix voor CQ-4259686
* De hybride videocodering is niet voltooid en er wordt geen miniatuur gemaakt. NPR-27122: Hotfix voor CQ-4255080

#### Sites {#sites-6}

* Opschorting bovenliggende pagina verwijdert cq: Het mixintype van LiveRelationship van de ontbrekende pagina. NPR-26996: Hotfix voor CQ-4254113
* (Externe koppelingencontrole) Interne koppelingen worden op afzonderlijke pagina&#39;s als verbroken weergegeven, maar hetzelfde werkt niet voor externe koppelingen. NPR-27481: Hotfix voor CQ-4257780
* De overerving Cloud Service Config wordt onderbroken tijdens het bewerken van andere pagina-eigenschappen. NPR-27311: Hotfix voor CQ-4256785
* Null-aanwijzeruitzondering bij gebruik van een Core Components-formulier naast een Foundation-formulier. NPR-27333: Hotfix voor CQ-4249176
* De rijke Redacteur van de Tekst verwijdert de lege alt markering. NPR-26938: Hotfix voor CQ-4253267
* (Klassieke UI) Prestatieproblemen met   selectie gewijzigd   listener in het geval van meerdere dropdowns. NPR-27115: Hotfix voor CQ-4237215
* Wanneer de rijke tekstredacteur met veelvoudige gebieden wordt gecombineerd, Uncaught TypeError: fieldAPI.getName is geen functie bij foundation.js fout komt voor. NPR-27146: Hotfix voor CQ-4253155, CQ-4259967
* Focus/cursor blijft in de Rich Text Editor staan, zelfs wanneer u op een keuzerondje in de Safari-browser klikt. NPR-27144: Hotfix voor CQ-4249635
* De pagina wordt als leeg weergegeven wanneer de gebruiker het inhoudsfragment probeert te bewerken. NPR-27669
* Kan geen versie maken voor Experience Fragments. NPR-27689: Hotfix voor CQ-4259009

#### Integratie {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever loopt de volledige boom om de beschikbare merken te verzamelen. NPR-27060: Hotfix voor CQ-4255790
* De   cq : acties worden niet overwogen voor een doelcomponent. NPR-27616: Hotfix voor CQ-4257497

#### Sling {#sling}

* Wanneer data-smart-use met klassen met een identieke naam wordt gebruikt, wordt de niet-compatibele code geproduceerd. NPR-27282: Hotfix voor Sling-7581

#### Handel {#commerce-1}

* Update naar Apache Felix HTTP Jetty 4.0.6. NPR-26472: Hotfix voor graniet-22916

#### DAM - DM-client {#dam-dm-client}

* Een afbeelding wordt niet weergegeven na het opgeven van onderbrekingspunten in de dynamische mediacomponent. Hotfix voor CQ-4256168

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet met verwante video wordt niet correct gesynchroniseerd. Hotfix voor CQ-4251650
* Video wordt niet afgespeeld in de Viewer Preset-editor voor gemengde mediaset. Hotfix voor CQ-4251442

#### DAM - Algemeen {#dam-general-1}

* De koppeling naar het model van het inhoudsfragment ontbreekt na het toepassen van een SP3-patch. Hotfix voor CQ-4259029

#### DAM - UI {#dam-ui}

* De interface van het schema voor metagegevens van de map wordt verbroken nadat SP3 is geïnstalleerd. Hotfix voor CQ-4257737

#### Gemeenschappen {#communities-5}

* Voeg pagineringsondersteuning toe voor groepsaanbiedingen bij publicatie. NPR-26953: Hotfix voor CQ-4246525
* Ongelezen tellingsmelding kan niet na 21 worden geplaatst. NPR-27496: Hotfix voor CQ-4252829
* De limiet voor gebruikersabonnementen is beperkt tot 1000. NPR-27615: Hotfix voor CQ-4254689
* Er is een fout opgetreden tijdens het uploaden van een bijlage buiten de afbeelding (bijvoorbeeld .pdf) in het forum. NPR-27375: Hotfix voor CQ-4257753
* De koppeling naar antwoorden werkt niet bij een rijklik. NPR-24556: Hotfix voor CQ-4256138
* Relaties met UGC worden niet verwijderd als UGC wordt verwijderd. NPR-27631: Hotfix voor CQ-4258706
* Onbekwaam om door adreswaarde in het onderzoek van het Sleutelwoord te zoeken als de gemeenschap met de Leverancier van het Middel van de Opslag van het Gegevensbestand (DSRP) wordt geplaatst. NPR-27652: Hotfix voor CQ-4253261
* Als u op het prullenbakpictogram op de afbeelding klikt nadat u de bevestiging hebt verwijderd, wordt de bijlage permanent verwijderd. NPR-27340: Hotfix voor CQ-4255150
* Boven op de tweede pagina worden forumberichten en reacties toegevoegd en als het bericht wordt vernieuwd, wordt het naar de juiste locatie vóór de eerste pagina geplaatst. NPR-27341: Hotfix voor CQ-4247338
* Label voor de voltooiingsstatus van Scoreschema inschakelen is leeg in de gebruikersinterface. NPR-27152: Hotfix voor CQ-4249994
* Bij het toelaten van &quot;sta bevoorrecht&quot;toe, zouden de bevoorrechte leden slechts voor gebruikers moeten kunnen samenstellen die lid van de gemeenschap zijn. NPR-27901: Hotfix voor CQ-4251235

#### Sustenance {#sustenance}

* Activiteitenlogbestanden voor pakketbeheer moeten worden uitgepakt in een afzonderlijk logbestand. NPR-27323: Hotfix voor graniet-14866

#### Vertaling {#translation-2}

* De voorvertoning van de vertaling werkt niet met de voorbeeldinhoud &#39;we.Retail&#39;. NPR-27170: Hotfix voor CQ-4241179

* Proactief platform.login lost op. NPR-26961
* Opslaan en sluiten op pagina-eigenschappen gaat niet terug naar de juiste pagina in AEM WAR met Tomcat. NPR-27567: Hotfix voor graniet-23671

* De ingevoerde tekst gaat verloren door de functie sourceEdit nadat deze is opgeslagen. Hotfix voor CQ-4259273

### Forms {#forms-6}

### Forms-invoegtoepassing {#forms-add-on-package-6}

#### Forms - Documentbeveiliging {#forms-document-security-1}

* Gelijktijdig probleem met JEE Client SDK. NPR-27572: Hotfix voor CQ-4247156

#### Forms - Document Services {#forms-document-services-3}

* Het maken van een formuliergegevensmodel op basis van SOAP mislukt op WebSphere. NPR-27692: Hotfix voor CQ-4253702

#### Forms - Adaptieve formulieren {#forms-adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27863: Hotfix voor CQ-4257315
* De AEM Forms Container-component wordt onzichtbaar zodra het verkeerde formulier op de sitepagina is geconfigureerd en het selectievakje &#39;Formulieren dekken de volledige breedte van de pagina&#39; is ingeschakeld. NPR-25972: Hotfix voor CQ-4239287, CQ-4249133

### Forms JEE-installatieprogramma {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* Het maken van een formuliergegevensmodel op basis van SOAP mislukt op WebSphere. NPR-27692: Hotfix voor CQ-4253702

#### SDAB-pakketten en inhoudspakketten inbegrepen {#osgi-bundles-and-content-packages-included}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.2

[Bestand ophalen](assets/do-not-localize/63332bundle_list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.2

[Bestand ophalen](assets/do-not-localize/6332content_package.txt)

### Cumulatief Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.1 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor installatie-instructies.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.14.
* Prestatieverbeteringen in voorspelling en zoekopdracht.
* Correctie van het probleem bij de verwerking van FormData voor de standaardwaarde.
* FormBuilder is bijgewerkt naar de nieuwste versie Handlebars.
* Toegevoegde config servlet voor geeft config voor RTE op dialoogwijze uit.
* Toegevoegde ondersteuning voor samengestelde velden.
* Ingeschakelde/uitgeschakelde werkbalkitems van de Rich Text Editor met een inhoudsbeleid voor het dialoogvenster Bewerken.

#### Activa {#assets-7}

* Als IDS-ontkoppeling is ingeschakeld, worden verwijzingen niet meer gekoppeld aan de workflow voor DAM-updatemiddelen. NPR-26135: Hotfix voor CQ-4250933
* Als u een archief dat is gemaakt met de unarchiver-stap uitpakt met een map met een naam van %, wordt dit archief niet geopend. NPR-26275: Hotfix voor CQ-4251482
* Eén aanhalingsteken voorkomt dat de metagegevens worden bijgewerkt. NPR-26808: Hotfix voor CQ-4254305
* (Openbaar Onderzoek) De kwestie van prestaties wanneer het zoeken binnen een inzameling. NPR-26714: Hotfix voor CQ-4253408
* Het gebruik van GQLConverter met een full-text zoekopdracht met de letters OR in de tekst wordt onjuist verwerkt. NPR-26564: Hotfix voor CQ-4247362
* Door de elementkoppeling van meerdere huurders te delen, wordt de id van de huurder vooraf bijgewerkt en wordt een ongeldige URL gevormd. NPR-26482: Hotfix voor CQ-4253540
* Schakel &quot;Bedrijfsmappad&quot; uit in de gebruikersinterface voor configuratie van Dynamic Media Cloud. NPR-26361: Hotfix voor CQ-4249505
* De inname van .mos RAW-bestanden is verlengd. NPR-26296: Hotfix voor CQ-4250661
* Bij het delen van een elementkoppeling is het niet toegestaan meer dan één interne gebruiker met een numerieke gebruikers-id toe te voegen. NPR-26206: Hotfix voor CQ-4251466
* Corruptie in ZIP-bestanden die zijn gecomprimeerd met het algoritme deflate64. NPR-26793: Hotfix voor CQ-4253995
* Het genereren van miniaturen werkt niet correct voor complexe PDF-bestanden. Dit leidt tot miniaturen, waar een deel van de afbeelding ontbreekt. NPR-26057: Hotfix voor CQ-4250944
* Probleem met het gebruik van heapgeheugen bij het genereren van miniaturen. NPR-25545: Hotfix voor CQ-4246960
* Het maken van een groot aantal relaties op een element veroorzaakt een fout. NPR-26309: Hotfix voor CQ-4250708
* De optie Vertoning verwijderen werkt niet en genereert een fout &quot;niets om te verwijderen&quot;. NPR-26007: Hotfix voor CQ-4213414
* Kan standaardwaarden voor velden met meerdere waarden niet verwijderen. NPR-25116: Hotfix voor CQ-4247856
* (DM Hybrid) De replicatieonderbrekingen van de Catalogus voor AEM 6.3.2 met Dynamic Media. NPR-26406: Hotfix voor CQ-4251306

#### Sites {#sites-7}

* De pro-actieve Steun van Plaatsen lost op. NPR-26963
* Tags worden twee keer gemaakt wanneer er een verschil is in het hoofdlettertype Titel en Naam. NPR-26877: Hotfix voor CQ-4254134
* De functies van de Rich Text Editor in het dialoogvenster Bewerken worden niet door het beleid beheerd. NPR-27059, NPR-26750: Hotfix voor CQ-4241130
* Clientcontextsegment.js in cache plaatsen tegenover vragen die niet in cache zijn geplaatst. NPR-26622: Hotfix voor CQ-4253486
* Activering van segmentregel (/etc/segmentatie) voor kinderregels in klassieke oorzaken moet worden gepubliceerd. NPR-26601: Hotfix voor CQ-4253588
* Als u &#39;speciaal teken&#39; toevoegt, wordt het dialoogvenster Rich Text Editor naar boven verschoven. NPR-26435: Hotfix voor CQ-4249869
* (Aanraakinterface) De werkbalk wordt onbruikbaar met meerdere Rich Text Editor tijdens het schakelen van Volledig scherm naar zwevend dialoogvenster. NPR-25652: Hotfix voor CQ-4206008
* Als u de opstart van meerdere pagina&#39;s bevordert, worden er meerdere versies voor elke pagina gemaakt. NPR-26810: Hotfix voor CQ-4254663
* Verplaatsingsbewerkingen voor tags worden niet weerspiegeld in labelvelden van het gestructureerde inhoudsfragmentmodel. NPR-26801: Hotfix voor CQ-4251805
* (Aanraakinterface) Het ongedaan maken van de publicatie van de onderliggende pagina in de pagina-editor werkt niet nadat de naam van de pagina in de blauwdruk is gewijzigd. NPR-26774: Hotfix voor CQ-4254175
* Niet-gepubliceerde pagina werkt niet met verwijzingen. NPR-26749: Hotfix voor CQ-4254372
* Wanneer u variatie als live kopie maakt, moet de gebruiker de pagina vernieuwen om deze te spiegelen. NPR-26663: Hotfix voor CQ-4254328
* (Klassieke gebruikersinterface) Als u teruggaat naar de pagina-eigenschappen, gebruikt de miniatuurafbeelding niet langer overerving en verdwijnt deze van de sitebeheerder en -assistent. De afbeelding wordt dan leeg weergegeven. NPR-26562: Hotfix voor CQ-4252346
* Wanneer een versie van een pagina wordt gecreeerd en een vergelijking wordt teweeggebracht, zijn de knopen van /content/versionshistory vermeld in de lijst van levende exemplaren voor het Blauwdruk. NPR-26506: Hotfix voor CQ-4243957
* URL&#39;s in de Experience Fragment Admin Editor staan geen overlays toe. NPR-26318: Hotfix voor CQ-4252156

#### Platform {#platform}

* Sessilek in ReplicationEventListener met testgebeurtenissen. NPR-25937: Hotfix voor CQ-4251090
* De replicatie gebruikt het verlopen teken voor OAuth die veelvoudige fouten veroorzaken. NPR-25894: Hotfix voor GRANITE-22388

#### Integratie {#integration-3}

* TSDK ingebed met AEM einden met een verbetering aan Handlebars 4 toe te schrijven aan het gebruik van incompatibele malplaatjes. NPR-26699: Hotfix voor CQ-4248974
* Wanneer u een pagina met een nieuw element publiceert, wordt de onderliggende pagina van de publicatie-instantie gedeactiveerd zonder dat hiervan melding wordt gemaakt. NPR-24869: Hotfix voor CQ-4247832
* De replicatie gebruikt een verlopen teken voor oauth. NPR-25984: Hotfix voor graniet-22388

#### Replicatie {#replication-2}

* Het HTTP-transport kan openstaande sessies lekken. Hotfix voor graniet-17434
* Uitzonderingen in logboeken terwijl de knoop van het toegangstoken gelijktijdig door meer dan één replicatieagenten wordt betreden. NPR-26964: Hotfix voor GRANITE-23276, graniet-23155

#### ContextHub {#contexthub}

* Het bestand &#39;koral.js&#39; bevat een kwetsbare versie van de bibliotheek &#39;handlebars.js&#39;. Hotfix voor CQ-4255377

#### DAM - DM-client {#dam-dm-client-1}

* Als u een kopie van een afbeeldingselement verwijdert, is het oorspronkelijke afbeeldingselement onbruikbaar. Hotfix voor CQ-4251648
* Overbodige download van extra afbeeldingsinhoud van S7-servers. Hotfix voor CQ-4248770

#### Graniet {#granite}

* AEM OAuth Provider voert niet het geval-ongevoelige onderzoek uit. NPR-26133: Hotfix voor GRANITE-22650
* De Validator van het pakket bevestigt geen pakketten inbegrepen in GVB/SP. NPR-26775: Hotfix voor graniet-22825

#### Gemeenschappen {#communities-6}

* Probleem met scheidingstekens in zoekresultaten. NPR-27051: Hotfix voor CQ-4248939
* Verander de drop-down waarde van Dallas in Virginia in de Leverancier van het Middel van de Opslag van Adobe. NPR-26936: Hotfix voor CQ-4254434
* Ondersteuning inschakelen voor het zoeken naar gelokaliseerde titels in SocialTagManager. NPR-26932: Hotfix voor CQ-4250276
* In bijlageafbeeldingen wordt geen miniatuur weergegeven bij het maken van een forumbericht. NPR-26380: Hotfix voor CQ-4253105
* Plakken vanuit Word-insteekmodule kan niet meerdere afbeeldingen laden. NPR-26728: Hotfix voor CQ-4253638
* Kan de inhoud niet filteren op de moderatiepagina. NPR-26697: Hotfix voor CQ-4213766
* (Beveiligingskwetsbaarheid) Accountovername als gevolg van verkeerde configuratie van JWT. NPR-26440: Hotfix voor CQ-4253314
* Het ophalen van gegevens van de Adobe Storage Resource Provider is traag. NPR-26237: Hotfix voor NPR-24152
* De pagina Privé bericht stelt zich samen gedraagt zich onregelmatig en langzaam. NPR-26120: Hotfix voor CQ-4250923
* Met het bericht &#39;Alles markeren gelezen&#39; wordt alleen de eerste 10 weergegeven als ongelezen zonder dat de pagina wordt vernieuwd. NPR-27036: Hotfix voor CQ-4254058
* De Paginering Klikken en laden van pagina&#39;s bij Sectie van opmerkingen van gemeenschappen. NPR-27030: Hotfix voor CQ-4251228
* (Forum Search) De knop Terug slaat de pagina over en gaat terug naar forum.html. NPR-26949: Hotfix voor CQ-4254804
* Ongelezen melding neemt niet meer dan 21 toe. NPR-26947: Hotfix voor CQ-4251251
* (De baan van SearchScheduledPosts) voegt toe laat/maakt schakelaar in ConfigMgr toe. NPR-26924: Hotfix voor CQ-4250463
* Tomcat-pad (/aempublish) daalt bij schuiven op de pagina Toewijzingen. NPR-26919: Hotfix voor CQ-4254345
* NullPointerException terwijl het creëren van een groep en een lid. NPR-26778: Hotfix voor CQ-4248095
* De moderator unpin en unfeatured inhoud werkt niet met het Enige Beginsel van de Verantwoordelijkheid MySQL (SRP). NPR-26767: Hotfix voor CQ-4251520
* Problemen met de zoekfunctionaliteit met bepaalde tekens. NPR-26726: Hotfix voor CQ-4247744
* Laat diepe verbindingen voor moderatie UI en enablement middelen toe. NPR-26705: Hotfix voor CQ-4251381
* Zoek in de forumcomponent naar problemen. NPR-26577: Hotfix voor CQ-4251303
* Het zoeken met de eerste en achternaam samen in het bericht van gemeenschappen keert niet de verwachte resultaten terug. NPR-26377: Hotfix voor CQ-4253150
* Paginering wordt niet bijgewerkt wanneer reacties worden verwijderd. NPR-26327
* Verwijderen van post werkt, maar geeft een fout op de console en post blijft zichtbaar op de gebruikersinterface. NPR-26292: Hotfix voor CQ-4252803
* De paginering wordt niet dynamisch bijgewerkt en de lijst met reacties wordt steeds langer. NPR-26145: Hotfix voor CQ-4251586
* Groepsinstellingen worden niet geladen in een groep met 50 kB~100 kB gebruikers. NPR-25642: Hotfix voor CQ-4238426
* Catalog Resource Player mislukt voor contextpaden. NPR-25640: Hotfix voor CQ-4238426
* (Forum Search) - Gepagineerde koppelingen naar threads met veel berichten werken niet aan meldingen. Hotfix voor CQ-4254202
* De console van de modernisering toont slechts 5 ingangen met Firefox. Hotfix voor CQ-4254128
* Groepen zijn niet zichtbaar tijdens het maken van een site. NPR-27148: Hotfix voor CQ-4251788
* Null-aanwijzeruitzondering tijdens het toevoegen van groep en leden aan Rolinstellingen en het toestaan van het geprivilegieerde lid in blogfunctie. NPR-21732, NPR-27176: Hotfix voor CQ-4255909
* Als u de site bewerkt en leden toevoegt in de rolinstellingen, wordt een null pointer-uitzondering gegenereerd. NPR-27132: Hotfix voor CQ-4255909

#### Gebruikersinterface {#user-interface}

* Oplossingen voor proactieve platformaanmelding. NPR-26961
* (Meerdere velden) Samengestelde items toestaan aangepaste namen te hebben. NPR-26493: Hotfix voor graniet-20568
* De kolomweergave wordt pas bijgewerkt nadat u een pagina hebt geplakt. NPR-26030: Hotfix voor CQ-4236346
* Proactieve granite.ui.commons-oplossingen. NPR-26960
* Oplossingen voor proactieve granite.ui.content. NPR-26959
* Oplossingen voor proactief CQ/Experience-logbestand. NPR-26943
* De pro-actieve Steun UI van de Stichting steunt. NPR-26942
* (IE11) NaN wordt in het nummerveld weergegeven wanneer een negatieve waarde wordt getypt. NPR-26701: Hotfix voor CQ-100826
* (Koraal. (Meerdere velden) Geneste meerdere velden gebruiken de verkeerde sjabloon om de items te maken. NPR-25649: Hotfix voor CUI-6743
* Werk graniet coralui2 en coralui3 clientlibs bij om Handlebars uit de build te verwijderen. NPR-25606: Hotfix voor graniet-22116

### Forms {#forms-7}

### Forms-invoegtoepassing {#forms-add-on-package-7}

#### Forms - Documentbeveiliging {#forms-document-security-2}

* Uitzonderingen op hoofd-sleutelrollover in serverlogboeken voor in-actieve sleutels. NPR-26748: Hotfix voor CQ-4253705
* Kan geen watermerkinstellingen voor Documentbeveiliging maken of wijzigen. NPR-26267, NPR-26129: Hotfix voor CQ-4250234

#### Forms - Document Services {#forms-document-services-4}

* PDF/A-validatie wordt niet geldig weergegeven met &quot;PDF/A valideren. NPR-25934: Hotfix voor CQ-4248558

#### Forms - Interactieve communicatie {#forms-interactive-communication}

* De PDF en de HTML-voorvertoning van de letter zijn zichtbaar en functioneren in hetzelfde venster wanneer een bewerkbare module wordt bewerkt, opgeslagen en vervolgens de PDF-voorvertoning wordt geopend/gesloten. NPR-26770: Hotfix voor CQ-4253217

#### Forms - Workflow {#forms-workflow-2}

* De werkruimte loopt periodiek vast en toont de beginpunten herhaaldelijk. NPR-26461: Hotfix voor CQ-4253439
* De uitzondering ESAPI wordt gegenereerd in de logboeken wanneer accolades worden gebruikt in de taaknaam. Hotfix voor CQ-4256627
* Een Null-aanwijzeruitzondering wordt gegenereerd wanneer het niet-vooraf ingevulde, aan het begin gekoppelde formulier/formset-punt wordt geopend. Hotfix voor CQ-4256124
* Kan geen e-mail verzenden met de globale instelling. NPR-26163: Hotfix voor CQ-111110
* Kan de werkruimte niet openen nadat het bestand axis.jar is toegepast. NPR-26131: Hotfix voor CQ-4251126
* Met de knop Vernieuwen worden de meest recente gegevens van de server niet gesynchroniseerd met Adaptieve formulieren. Hotfix voor CQ-4255670
* Als u een zoeksjabloon instelt via de interface van de beheerder en vervolgens dezelfde methode gebruikt om de taak in de werkruimte van AEM Forms te doorzoeken, wordt een uitzondering gegenereerd. Hotfix voor CQ-4255649
* Details bijhouden van de processen onder de toepassingen met een haakjessymbool in de naam wordt niet weergegeven in de HTML-werkruimte. Hotfix voor CQ-4242101
* Als u wijzigingen opslaat in het voorkeurenscherm van de HTML-werkruimte, wordt een uitzondering gegenereerd. Hotfix voor CQ-4241485
* Goedkeuring van bulkobjecten is verbroken bij de laatste JEE-instelling. Hotfix voor CQ-4241486
* Het concept van taak/beginpunt mislukt op de nieuwste 6.4 JEE-server. Hotfix voor CQ-4241484
* Stel de parameter Date().getTime().toString in om de sessie te initialiseren in plaats van Date.toString(). Hotfix voor CQ-4241483
* Bij het openen van /lc/ws wordt een uitzondering voor kwetsbare tekens waargenomen in de HTML-parameter. Hotfix voor CQ-4241481

#### Kwetsbaarheid {#vulnerability-1}

* XSS-kwetsbaarheid (Storage Cross-Site Scripting) is opgeslagen op het tabblad Notities van Forms Manager. NPR-27157: Hotfix voor CQ-4255556

### Forms JEE-installatieprogramma {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Codeoverzicht voor Enterprise Security API. Hotfix voor CQ-4255638
* Kan esapi.properties niet laden als bron voor klassebestanden in WAS9. Hotfix voor CQ-4255631
* Wanneer u tijdens de domeinconfiguratie op Verificatie toevoegen klikt, wordt een fout gegenereerd. Hotfix voor CQ-4255634
* Forms JEE biedt ondersteuning voor PKCS#11-wederzijdse verificatie. NPR-21372
* Oplossing voor de problemen die werden gerapporteerd in statische codeanalyse van Core. Hotfix voor CQ-104446
* De implementatie van adobe.livecycle.weblogic.ear en adobe.livecycle.websphere.ear mislukt tijdens het uitvoeren van LCM. Hotfix voor CQ-4255629, CQ-4255630
* Ongeldige foutberichten in het toepassingsbeheer. NPR-23289: Hotfix voor CQ-4233163, CQ-4255636
* Als u tijdens de domeinconfiguratie op Verificatie toevoegen klikt, treedt er een fout op. Hotfix voor CQ-4255634

#### Forms - JEE-connector {#forms-jee-connector}

* Het bevestigen van de kwesties die in statische codeanalyse van Schakelaar worden gemeld. NPR-22260

#### PDFG-service {#pdfg-service-1}

* org.jgroups.Message fout in logboeken na bevordering van LiveCycle aan AEM 6.2 vormen. NPR-26795: Hotfix voor CQ-4220415
* AEM formulieren - Fout tijdens het migreren van stijlen. Hotfix voor CQ-4251969
* Oplossing voor de problemen die werden gerapporteerd in het rapport voor statische codeanalyse van PDFG. NPR-23251: Hotfix voor CQ-4213930

#### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.1 {#osgi-bundles-and-content-packages-included-in-3}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.1

[Bestand ophalen](assets/do-not-localize/63sp3cfp1bundlelist.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.1

### Cumulatief Fix Pack 6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 2 (6.3.2.0) in April 2018.

AEM Cumulative Fix Pack 6.3.2.2 is afhankelijk van AEM 6.3 Service Pack 2. Daarom moet u AEM Cumulative pakket van de Moeilijke situatie 6.3.2.x installeren na het installeren AEM 6.3 Service Pack 2. Zie [AEM 6.3 Opmerkingen bij de release Service Pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) voor installatie-instructies.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.11.
* Submiddelen en viewer voor elementen met meerdere pagina&#39;s zijn ingeschakeld in Brand Portal.
* De lengte van het veldtype is gewijzigd in 255 ter ondersteuning van alle mogelijke mime-typen voor de verschillende typen bijlagen.
* Foutbericht geconfigureerd van de server wanneer een afbeelding de uploadcriteria overtreedt.
* Extra STARTTLS-ondersteuning in CQ Mail Service op dag.
* Update naar de nieuwste versies van cq-wcm-content en com.adobe.cq.launches.it.serverside.
* Update com.adobe.granite.ui.coralui3-rete naar de recentste versie die is uitgebracht.
* De verzekerde rendervoorwaarde keert een normaal resultaat terug als expressionResolver ongeldig is.
* Coral.ColumnView: Toegevoegde ondersteuning voor shift+klikken.

### Activa {#assets-8}

* Het veld CUG (Asset Folder Closed User Group) retourneert niet de groep &#39;Iedereen&#39;. NPR-23163: Hotfix voor CQ-4239377
* Zoeken naar opgeslagen zoekopdrachten in slimme verzamelingen retourneert niet alle resultaten. NPR-23243: Hotfix voor CQ-4240355
* (ExpiryNotificationJobImpl) Optimalisatie van de bestaande query. NPR-2330: Hotfix voor CQ-4205249
* (Metagegevensprofiel) Standaardwaarden voor tags die zijn ingesteld op het moment dat ze worden gemaakt, zijn niet beschikbaar na het opslaan. NPR-23370: Hotfix voor CQ-4235458
* (Aanraakinterface) Kan meerdere elementen niet verplaatsen vanwege een JS-fout. NPR-23395: Hotfix voor CQ-4241279
* Verkeerd overeenkomende gegevens in downloadgrootte versus weergegeven gegevens leiden tot verwarring bij de gebruikers. NPR-23418: Hotfix voor CQ-4242774
* Geëxtraheerd mimetype voor bestandsextensie LSR en SKETCH is onjuist en leidt tot een ongeldige bestandsdownload. NPR-23644: Hotfix voor CQ-4243260
* (Firefox/Chrome) Kan geen elementen downloaden op de pagina voor het delen van bedrijfsmiddelen. NPR-23963: Hotfix voor CQ-4244391
* De zoekfacetten voor middelenbeheer verdwijnen na de voorvertoning in de zoekvensters. NPR-23964: Hotfix voor CQ-4244410
* Als u de publicatie van het zoekformulier opheft, wordt het standaardzoekformulier volledig verwijderd. NPR-23291: Hotfix voor CQ-4241382
* (Brand Portal) Zoek in mapvoorspelling moet worden uitgefilterd op replicatie. NPR-23292: Hotfix voor CQ-4241385
* De actie Publiceren naar Brand Portal-gebruikersinterface is niet beschikbaar. NPR-23293: Hotfix voor CQ-4241161
* De knop Publiceren/Publiceren ongedaan maken naar Brand Portal mag niet beschikbaar zijn voor inhoudsfragmenten. NPR-23318: Hotfix voor CQ-4245086
* (Brand Portal) Schakel het maken van subactiva in wanneer een actief wordt gepubliceerd. NPR-2331: Hotfix voor CQ-424/2018
* Dynamic Media-aanvragen gebruiken geen proxy/HTTP common-client. NPR-10727: Hotfix voor CQ-45695, CQ-88800
* Unable to annoting single rendition MP4 Video Asset in Dynamic Media S7 (DMS7). NPR-22046: Hotfix voor CQ-4215912
* De EmbedXMP-gegevens worden altijd ingesteld op &quot;actief&quot; voor het genereren van profielen. NPR-22903: Hotfix voor CQ-4234498
* Problemen met dynamische weergave/selectie met grote voorinstellingen voor afbeelding. NPR-23151: Hotfix voor CQ-4217511
* Probleem met Dynamic Media Encode Video - Modification / Reupload launcher. NPR-23237: Hotfix voor CQ-4240260
* Proxy handling fix for HTTP forward in Dynamic Media S7. NPR-24001: Hotfix voor CQ-244140

### Sites {#sites-8}

* De discrepanties van de Bouwer van de vraag resulterend verschillende xPath vertaling tussen 6.2 en 6.3. NPR-23245: Hotfix voor CQ-4240396
* Het tabblad Miniatuur in de pagina-eigenschap werkt niet bij het uitbreiden van het dialoogvenster. NPR-22844: Hotfix voor CQ-4241474
* Parsys breekt de de kaderbreedte van het mededingerapparaat en gewassen van om het even welke die component aan het wordt toegevoegd. NPR-22926: Hotfix voor CQ-4238224
* Bij het uitvoeren van de meerdere keren starten wordt de introductie in Auteur bevorderd, maar de wijzigingen worden niet op de publicatieserver gerepliceerd omdat er geen replicatiemachtigingen zijn. NPR-22934: Hotfix voor CQ-4234746
* Een pagina die door een gebruiker in de eerste sessie is vergrendeld, kan door een andere gebruiker in een andere sessie worden gewijzigd. NPR-23057; Hotfix voor CQ-4199017
* Herstelbare optie corrigeren in lijstweergave. NPR-23065: Hotfix voor CQ-4239321
* (Pagina-editor) De afbeelding op een afbeeldingscomponent verdwijnt wanneer u het dialoogvenster opnieuw opent. NPR-23156: Hotfix voor CQ-4239978
* De Redacteur van het malplaatje toont slechts 20 malplaatjes/omslagen en laadt niet andere wanneer het scrollen aan de bodem van de pagina. NPR-23185: Hotfix voor CQ-4238483
* (Klassieke UI) Er wordt een fout geproduceerd terwijl het bewegen van of het anders noemen van de pagina&#39;s. NPR-23213: Hotfix voor CQ-4240971
* Kan ContextHub-segmenten niet bewerken/maken. NPR-23218: Hotfix voor CQ-4226948
* (Rich Text Editor) - Vervang de bewerking om de opmaak van een woord te wijzigen. NPR-23271: Hotfix voor CQ-4239677
* De knop Uitvoeren ontbreekt op het tabblad Vervagen voor XF-variaties. NPR-23320: Hotfix voor CQ-4240404
* Klassieke interface werkt niet om CUG te bewerken vanwege veroudering. NPR-24122: Hotfix voor 4241823
* Proactieve oplossing om te beschermen tegen ongewenste promoties van inhoud. NPR-24387: Hotfix voor 4244993
* Na ongeveer. 80 fragmenten worden toegevoegd aan een map in Elementen, fouten die optreden wanneer de workflow wordt geactiveerd vanaf de tijdlijnconsole. NPR-23393; Hotfix voor CQ-4211216
* Kan geen afbeeldingen vanuit de zoekfunctie naar inhoud slepen en neerzetten in het dialoogvenster Rich Text Editor. NPR-23403: Hotfix voor CQ-424/2094
* Fout bij &#39;Ongeldige waarde van recursieselectiekader&#39; tijdens het migreren van een component van AEM 6.0 naar AEM 6.2. NPR-23532: Hotfix voor CQ-4241258
* (Rich Text Editor) In de knopinfo wordt de variabelenaam van de plug-in weergegeven in plaats van de naam van de leesbare plug-in. NPR-23550: Hotfix voor CQ-4243269
* Kan dialoogvenster niet opslaan met de vereiste vervolgkeuzelijst voor mobiele apparaten/tablets. NPR-23904: Hotfix voor CQ-4243096
* Stijlsysteemopties worden weergegeven op alle pagina&#39;s na de installatie 6.3.2.1. NPR-23972: Hotfix voor CQ-4244394
* Klassieke interface werkt niet om CUG te bewerken vanwege veroudering. NPR-24122: Hotfix voor 4241823
* Proactieve oplossing om te beschermen tegen ongewenste promoties van inhoud. NPR-24387: Hotfix voor 4244993
* De elementverwijzingen worden niet bijgewerkt wanneer elementen worden verplaatst. NPR-23208: Hotfix voor CQ-4239879

### Platform {#platform-1}

* De slimme inzameling toont geen resultaten na sparen als het gebruiken van markeringen in de onderzoeksfacet voorspellen. NPR-23401: Hotfix voor graniet-21278
* Patch jQuery 1.12.4 van clientlib om beveiligingsoplossingen op te nemen. NPR-24128: Hotfix voor graniet-20058
* Internationalisatievertalingen worden alleen bijgewerkt als de bundel opnieuw wordt opgestart. NPR-23193: Hotfix voor Sling-7190
* Niet-afgesloten resource resolver in ReplicationEventListener. NPR-23240: Hotfix voor CQ-4241350
* STARTTLS ondersteunen in &quot;Day CQ Mail Service&quot;. NPR-23941: Hotfix voor CQ-4240397
* De naam van de JCR-klachtentag moet automatisch worden ingevuld op basis van de tagtitel. NPR-24173: Hotfix voor CQ-4199411

### Integratie {#integration-4}

* (Doel) Campagnes worden niet geactiveerd wanneer u API-type als XML gebruikt. NPR-23199: Hotfix voor CQ-4240936***
* De de verwijzingsreplicatie van de configuratie ontbreekt met middenomslagstructuur. NPR-23485: Hotfix voor CQ-4242751

### Kwetsbaarheid {#vulnerability-2}

* De integratie van Salesforce is kwetsbaar aan de Smederij van het Verzoek van de Server (SSRF). NPR-24289: Hotfix voor CQ-424527
* XSS (cross-site scripting) in Admin UI-projectkoppelingen. NPR-23272: Hotfix voor CQ-4241795

### WCM - Elementen van de Stichting {#wcm-foundation-components}

* De lijst van de stichting is kwetsbaar aan Opgeslagen Scripting over de hele site. NPR-23214: Hotfix voor CQ-4240760

### Vertaling {#translation-3}

* Eigenschappen voor live kopiëren zijn niet verwijderd tijdens het maken van taalkopieën. NPR-23123: Hotfix voor CQ-4230641

### Gebruikersinterface {#user-interface-1}

* DatePicker biedt geen ondersteuning voor het handmatig instellen van een hint voor externe tekst die door een verborgen veld wordt ingesteld. Als u de teksthint wijzigt, treedt er een omzettingsfout op. NPR-23371: Hotfix voor graniet-21194
* Coral.ColumnView: Voeg steun voor shift toe+klik. NPR-23404: Hotfix voor graniet-1338
* Selecteer RT niet valideren wanneer een item met een lege waarde wordt geselecteerd. NPR-23405: Hotfix voor graniet-21283
* (OMEGA) &quot;Functie&quot; alleen in het Engels rapporteren. NPR-23990: Hotfix voor graniet-21231
* Oplossingen voor Coral.AutoComplete API. NPR-23516

### Graniet {#granite-1}

* Apache Http client tracking-verbindingen en hoog heapgebruik zorgen ervoor dat AEM server vastloopt. NPR-23906: Hotfix voor graniet-21056

### Handel {#commerce-2}

* Uitvoer van Campagne-json bevat geen servlet-contexthoofdmap. NPR-23733: Hotfix voor CQ-4243827

### Gemeenschappen {#communities-7}

* Zoeken op gemeenschappen mislukt voor weinig woorden. NPR-23256: Hotfix voor CQ-4240717
* Kan geen groepen toewijzen voor de rolkwestie van communitymanagers. NPR-23317: Hotfix voor CQ-4241233: CQ-4221399
* Problemen bij het maken van bronnen met een vergelijkbare naam voor middelen. NPR-23319: Hotfix voor CQ-4240700
* (ContextPath) Het breken van berichtfunctionaliteit voor Jetty vormt en fout terwijl het zoeken van groepsleden in de lijst van het communautaire groepslid. NPR-2336: Hotfix voor CQ-4241519, CQ-4242080
* Het uploaden van een beeld aan een Forum van Gemeenschappen verschijnt niet in de Leverancier van het Middel van de Opslag van Adobe (ASRP). NPR-23397: Hotfix voor CQ-4242497
* Verwijderde ideeën worden weergegeven als actieve koppelingen in Activiteiten. NPR-23406
* imsmanifest.xml kan niet worden geladen met AEM die met contextwortel lopen. NPR-23483: Hotfix voor CQ-4242193
* Beveiligingskwetsbaarheden in een oudere versie van Handlebars. NPR-23518: Hotfix voor CQ-4243055
* De tunnelservice werkt niet. NPR-23543: Hotfix voor CQ-4242217
* Problemen met componenten van gemeenschappen die worden benaderd via een verzender en dynamische sling, zijn ingeschakeld. NPR-23586: Hotfix voor CQ-4242360, CQ-4241522
* Wanneer het zoeken naar een onderzoekstermijn die vele resultaten door onderzoek veroorzaakt en dan een nieuwe onderzoekstermijn ingaat, wordt het pagineren niet teruggesteld. NPR-23739: Hotfix voor CQ-4222593
* Problemen tijdens het uitvoeren van zoekopdrachten op de forumcomponent. NPR-23838: Hotfix voor CQ-4243770
* (Markering voor Gemeenschapsmodernisering) Bulk Allow of flagged messages werkt niet. NPR-23845: Hotfix voor CQ-4243962
* Tekst van de sorteerknop die de standaard geselecteerde waarde niet aangeeft   de standaardsorteervolgorde te selecteren. NPR-23881: Hotfix voor CQ-4243375
* Web- en e-mailmeldingen worden niet geactiveerd vanwege een fout met het bericht aan de groepen. NPR-23934: Hotfix voor CQ-4242880
* Geen details op de vlaggebruikers en de redenen worden getoond gebruikend de configuratie van DSRP. NPR-23973: Hotfix voor CQ-4243205
* De redenen van de vlag van gebruikers zonder vlag blijven zichtbaar/ NPR-23974: Hotfix voor CQ-4243822
* Als u twee bestanden met dezelfde naam twee keer aan een formulierbericht koppelt, treedt er een serverfout op. NPR-24166: Hotfix voor CQ-4244367
* Unable to store attachments with mime types more than 15 characters using Database Storage Resource Developer (DSRP). NPR-24174
* Wanneer een afbeelding die de uploadcriteria overtreedt, naar de posttekst wordt gesleept en neergezet, wordt een serverfout gegenereerd en wordt een algemeen foutbericht weergegeven aan de gebruiker. NPR-24243
* Hiermee worden diverse problemen met de AEM Communities-server opgelost. NPR-23971: Hotfix voor CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Hiermee verhelpt u verschillende Adobe Social-problemen. NPR-24242: Hotfix voor CQ-4245054, CQ-4245120, CQ-4245296

### Campagne {#campaign}

* Uitvoer van Campagne-json bevat geen servlet-contexthoofdmap. NPR-23733: Hotfix voor CQ-4243827

### MSM {#msm}

* Bij het uitrollen van de pagina worden in de livecopy geen eigenschappen voor aan- en uittijd weergegeven die van de master pagina zijn overgenomen. NPR-23873: Hotfix voor CQ-4243431
* Bij LiveCopy-bewerking worden onderliggende knooppunten van verwijderde componenten niet genegeerd. NPR-23058: Hotfix voor CQ-4211662

### Verschuiven {#offloading}

* Verzoek om een mechanisme om middelen van de arbeidersinstanties na verwerking of op regelmatige basis op te ruimen. NPR-23638: Hotfix voor graniet-21337

## Forms {#forms-8}

### Forms-invoegtoepassing {#forms-add-on-package-8}

#### Adaptieve Forms {#adaptive-forms-1}

* ReCaptchaConfigService naar intern pakket verplaatsen. Hotfix voor CQ-4217459
* Numeriek veld neemt de minimumwaarde niet in acht. NPR-23967: Hotfix voor CQ-4244830
* Ondersteuning voor Multi Shard in Adaptive Forms-integratie met AdobeSign. NPR-23383

#### Backend-integratie {#backend-integration}

* (FDM) (WebService) het steunen van de uitbreidingsconstructie van WSDL in de Parser van WSDL. NPR-23640, NPR:23236: Hotfix voor 4205821
* SDLInvokerParams opnemen in Forms Add-on Client SDK. NPR-23157

### Forms JEE Installer {#forms-jee-installer-7}

#### Procesbeheer {#process-management}

* Kan de werkruimte niet openen nadat het nieuwe bestand axis.jar is toegepast. NPR-23316
* LiveCycle is kwetsbaar voor XSS op PMAdmin. NPR-23267
* Na de upgrade naar AEM 6.1 Forms bevriest de HTML-werkruimte de toegang tot de Taaklijst voor specifieke gebruikers. NPR-23943

#### Kern {#core}

* Forms JEE biedt ondersteuning voor PKCS#11-wederzijdse verificatie. NPR-21372

#### PDFG-service {#pdfg-service-2}

* De service Documentdigitalisering crasht tijdens de verwerking van TIFF-bestanden (ongeveer 50 kB). NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server Output - Alternatieve beschrijving ontbreekt voor annotaties. NPR-22207
* Voeg PDF/UA-ondersteuning toe aan XML-formulieren die zijn gegenereerd via Designer en Output Service. NPR-23132

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}

Lijst van OSGi-bundels opgenomen in AEM 6.3.2.2

[Bestand ophalen](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.2.2

[Bestand ophalen](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulatief Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 2 (6.3.2.0) in April 2018.

De belangrijkste hoogtepunten van **AEM Cumulative Fix Pack** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.10.
* Verbeterde rendering van Parsys-componenten in Classic UI.
* Bijgewerkte slingmodellen bundelen om tekensetcorrectie op te nemen.
* Publiceren naar Brand Portal asynchroon gemaakt voor alle elementtypen.
* Bijgewerkte coralui-component-richtexteditor.git van 0.1.15 tot 0.1.16
* Oplossingen in de functionaliteit voor weergeven/verbergen van een vervolgkeuzelijst.
* Omdraaien van afbeelding ingeschakeld voor de Core Image Component.
* Bijgewerkt voorvoegsel   http-bundels om sessiekenmerken in te schakelen.

* Cache=true is verwijderd bij Sling Models vanwege problemen met geheugenverbruik.

### Activa {#assets-9}

* Wanneer u de titel of miniatuurafbeelding wijzigt in de instellingen voor de map Asset Folder, worden de oorspronkelijke groep en machtigingen van de map overschreven. NPR-22171: Hotfix voor CQ-4216080
* De gebruikersinterface genereert de fout &quot;Publiceren naar Brand Portal is mislukt&quot;, terwijl de taak wordt toegevoegd aan de replicatiewachtrij en de middelen worden gepubliceerd naar Brand Portal. NPR-22179: Hotfix voor CQ-4205273
* (Aanraakinterface) Standaarduploadlocatie voor elementen in de kolomweergave. NPR-22465: Hotfix voor CQ-4237057
* AEM werpt de fout StackOverflow wanneer het proberen om een activaschema van /conf/global aan /conf/myhuurder te kopiëren. NPR-22489: Hotfix voor CQ-4235875
* Het uitpakken van een ZIP-archief mislukt als gevolg van de afsluitende ruimte aan het einde van de mapnaam. NPR-22522: Hotfix voor CQ-4238036
* Sorteren met de kolom Titel van element werkt niet voor zoekresultaten. NPR-22908: Hotfix voor CQ-4239076
* YouTube-video wordt gelabeld met het volledige pad in plaats van de tagnaam zelf. NPR-22976: Hotfix voor CQ-4238669
* Het opnieuw ordenen van mappen onder een map die opnieuw kan worden geordend, duurt niet voort. NPR-23125: Hotfix voor CQ-4231761
* HTTP 504: De fout van de Onderbreking van de gateway wanneer het proberen om inzamelingen te delen gebruikend aandeelverbinding. NPR-21928: Hotfix voor CQ-4234507
* Metagegevens van PDF-trefwoorden worden niet correct geëxtraheerd en gewijzigd wanneer er meerdere trefwoorden aan een PDF-element zijn gekoppeld. Om dit probleem op te lossen, is de eigenschap voor metagegevens van het veld Onderwerp verwijderd voor PDF-elementen. U kunt echter wel het metagegevensschema bewerken om een tekstveld met meerdere waarden toe te voegen voor het veld Onderwerp. NPR-21972: Hotfix voor 4215741****
* Verkeerde elementen worden verwijderd als de geselecteerde map wordt gewijzigd tussen het moment dat de twee pop-ups worden weergegeven. NPR-21980: Hotfix voor CQ-4233675
* (DAM) Meerdere XSS-kwetsbaarheden (cross-site scripting) tijdens het toevoegen aan de wizard Verzameling. NPR-22432: Hotfix voor CQ-4327086
* Downloaden van middelen mislukt bij gebruik van Digital Rights Management in Middelen in Safari. Gebruikers kunnen geen elementen downloaden met een disclaimer- en lange bestandsnaam. NPR-22747: Hotfix voor CQ-4236460 en CQ-4235274
* Openbaar maken als standaardoptie voor delen tijdens het publiceren van elementen naar Brand Portal. NPR-21931: Hotfix voor CQ-4218816

### Sites {#sites-9}

* Het nieuwe item in het Postvak IN van workflow toont het paginapad in plaats van de titel van de pagina. NPR-21634: Hotfix voor CQ-4230672
* Bij bewerkbare structuurcomponenten gaan CSS-klassenamen verloren die nodig zijn voor het responsieve raster wanneer deze worden bewerkt. NPR-21741: Hotfix voor CQ-4232374
* (TouchUI) Meerdere XSS-kwetsbaarheden (cross-site scripting) voor HTML-componenten. NPR-21899: Hotfix voor CQ-4232511
* Kan inhoudsfragment voor gemengde media afbeelding niet wijzigen. NPR-21907: Hotfix voor CQ-4233401
* RTE Volledig scherm voor het dialoogvenster Touch UI verbergt de RTE-plug-ins. NPR-22034: Hotfix voor CQ-4235457
* (Aanraakinterface) De RTF-editor verwijdert alle andere kenmerken dan id uit de &lt;a>-tag. NPR-22044: Hotfix voor CQ-4234133
* De veelvoudige gestapelde Parsys toe te schrijven aan langlopende vragen (meer dan 6) maakt AEM langzaam. NPR-22134: Hotfix voor CQ-4233904
* Kan machtigingen niet wijzigen voor knooppunten met dubbele punten in de naam. NPR-22136: Hotfix voor CQ-4236221
* (Klassieke UI) uitvoer van de rijke tekstredacteur html voegt &quot;list-position-style toe: inside;&#39; als inline stijl voor de tag &lt;ul>. NPR-22145: Hotfix voor CRTE-114
* Maak een reserve TreeNode aan het naamattribuut wanneer de tekst leeg is. NPR-22146: Hotfix voor CQ-4234724/CQ-4236300
* RSS-feed-problemen, poort -1 tot AEM 6.3. NPR-22176: Hotfix voor CQ-4233339
* (Klassieke UI) de kortere weg van het Plakken van tekst (Ctrl+V) werkt niet voor de component van de Tekst OTB (RTF). NPR-22224: Hotfix voor CQ-4236224
* Het filteren van een veld werkt niet zoals u had verwacht bij het typen van de tekst. NPR-22236: Hotfix voor CQ-4236655
* (Pagina-editor) Bij het plakken van tekstgegevens in de component voor afbeeldingen met hyperlinks wordt de component Text ook geplakt bij het plakken van tekstgegevens in de component voor afbeeldingen met hyperlinks. NPR-22264: Hotfix voor CQ-4236230
* Dialog FileUpload vereiste gebied veroorzaakt problemen in dialoogvoorlegging. NPR-22464: Hotfix voor CQ-4222192
* Als u de verplaatsingsmachtigingen zonder replicatiemachtigingen verplaatst, wordt een aanvraag voor de activeringsworkflow gestart als de verplaatste pagina of de referenties niet kunnen worden geactiveerd. NPR-22467: Hotfix voor CQ-4211765
* Prestatieproblemen bij het laden van een pagina met een groot (2000+) publiek. NPR-22478; Hotfix voor CQ-4209567
* De kwesties van de persistentie wanneer de opslag ContextHub standaard persistentielaag tijdens initialisatie overschrijft. NPR-22479: Hotfix voor CQ-4218399
* Bij starten met meerdere pagina&#39;s worden geen subpagina&#39;s naar publicatieservers gepubliceerd als &#39;subpagina&#39;s opnemen&#39; niet is ingeschakeld in de eerste hoofdmap van de inhoud. NPR-22482: Hotfix voor CQ-4237818
* (Aanraakinterface) Door het verwijderen van opstarties via de klassieke UI-console zijn alle pagina&#39;s onbewerkbaar. NPR-22491: Hotfix voor CQ-4225074
* Problemen met de component Image vanwege extra ruimte in het dialoogvenster. NPR-22528: Hotfix voor CQ-4238183
* Wanneer u de component opent met de inline-modus, zijn eerder geladen insteekmodules de tweede keer niet zichtbaar. NPR-22591: Hotfix voor CQ-4236850
* Als u een opstart verwijdert in een geneste opstart, worden subopstarters wees. NPR-22621; Hotfix voor CQ-4202639
* (Klassieke UI sidekick) Het tabblad Workflow is uitgeschakeld wanneer de pagina zich in het werkstroomvergrendelingsstadium bevindt. NPR-22722: Hotfix voor CQ-4237557
* Nadat u een afbeelding die in de afbeeldingscomponent op een pagina is toegevoegd, hebt gespiegeld, worden de wijzigingen niet opgeslagen en wordt de oorspronkelijke afbeelding op de pagina weergegeven. Renderondersteuning is toegevoegd aan de kerncomponent van de afbeelding via [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141). NPR-22801: Hotfix voor CQ-4221539
* Wanneer de gebruiker het bestaande anker probeert te verwijderen uit het ankermenu, wordt het venster van de component Rich Text Editor gesloten en blijven de wijzigingen niet opgeslagen. NPR-22802: Hotfix voor CQ-4238167
* Het filter van Onderzoek toont niet alle acties in de console van Plaatsen. NPR-22804: Hotfix voor CQ-4239007
* Probleem met kopiëren/plakken in aanraakinterface met systeemklembord en intern AEM klembord. NPR-22807: Hotfix voor CQ-4220383
* Inconsistentie in de uittrekmarkering die door Lucene Search is geretourneerd. NPR-22879: Hotfix voor CQ-4238513
* Als u een pagina activeert terwijl publicatie-instanties zijn uitgeschakeld, krijgt u een groene status in plaats van een pagina te ambereren. NPR-22927: Hotfix voor CQ-4236310
* (StyleSystem) De schermpositie springt tijdens het selecteren van een stijl in het pop-upmenu. NPR-23183: Hotfix voor CQ-4238867
* (Publicatie beheren) Voor het verplaatsen naar de volgende maand van de kalender moeten meerdere klikken worden uitgevoerd. NPR-23508: Hotfix voor CQ-4242732

### Platform {#platform-2}

* Japanse tekens worden niet correct geëxporteerd door het servlet-object Sling Exporter. NPR-22153: Hotfix voor CQ-4228920
* Blokkering van de planner tijdens het opstarten. NPR-22440: Hotfix voor Sling-7004
* Kan groepen niet synchroniseren tussen twee publicatie-instanties. NPR-21943: Hotfix voor graniet-19564
* Prestatieproblemen met org.apache.sling.i18n gedeelde sessie/resource resolver. NPR-23390: Hotfix voor Sling-7543

### Integratie {#integration-5}

* Unclosed ResourceResolver in com.day.cq.analytics.sitecatalyst. NPR-22323: Hotfix voor CQ-4236515
* TargetContentImpl maakt AEM traag tijdens lange lopende vragen. NPR-22361: Hotfix voor CQ-4236907
* De doelengine (mbox.js, at.js) gebruikt geen beheerde URL&#39;s en gebruikt URL&#39;s die dubbele punten bevatten die mogelijk mislukken bij bepaalde implementaties. NPR-22366: Hotfix voor CQ-4237854
* Wanneer u een aangepast bestand at.js of mbox.js opgeeft, wordt het include-script als tekst naar de pagina geschreven in plaats van HTML-tags. NPR-22441: Hotfix voor CQ-4203691
* In de modus Doel kunnen auteurs een component die van de blauwdruk is overerfd, wijzigen zonder de overerving te annuleren. NPR-22751: Hotfix voor CQ-4237907
* PersonalizationDataSource werpt een Uitzondering van de Wijzer Null toe te schrijven aan ontbrekende jcr: inhoudsknooppunt. NPR-22850: Hotfix voor CQ-4222122
* AEM het richten ontbreekt wanneer het gebruiken van niet Engelse taal. NPR-22917: Hotfix voor CQ-4218213
* Bij het publiceren van een pagina met doelinhoud ontbreken gerelateerde bronnen. NPR-23064: Hotfix voor CQ-4227119
* Gebruikers kunnen de statische parameterwaarden van de test in de mbox vraag niet zien die wanneer het testen met AT.js als cliëntbibliotheek in wolkenconfiguratie kan worden gezien. NPR-21930: Hotfix voor CQ-4234520

### WCM-stichtingscomponenten {#wcm-foundation-components-1}

* InParsys wordt de positieverschuiving gemaakt nadat het selectievakje Overerving annuleren/uitschakelen is uitgeschakeld. NPR-21905: Hotfix voor CQ-4230951
* De functionaliteit tonen/verbergen van de formuliervervolgkeuzelijst werkt niet zoals u had verwacht. NPR-22327: Hotfix voor CQ-4222853
* De Component van CAPTCHA is afgekeurd voor betere veiligheid, als u component CAPTCHA gebruikt, dan bericht &quot;de component Captcha is afgekeurd en zou niet meer moeten worden gebruikt.&quot; wordt weergegeven na de installatie van versie 6.3.2.1 of hoger. AEM component kan worden aangepast om reCAPTCHA voor betere veiligheid NPR-22151 te omvatten: Hotfix voor CQ-4220052

### WCM - Pagina-editor {#wcm-page-editor}

* Gespiegeld XSS (Cross-site scripting) bij gebruik van een ongeldige kiezer. Hotfix voor CQ-4270397

### Vertaling {#translation-4}

* Problemen met Voorvertoning onderzoeken. NPR-22114: Hotfix voor CQ-4223753

### Gebruikersinterface {#user-interface-2}

* Problemen met de maandkiezer voor Coral Calendar wanneer het datumbereik &#39;min&#39; en &#39;max&#39; is ingesteld. NPR-22716: Hotfix voor CUI-7187
* (Klassieke UI) De component toont de standaardwaarden zelfs als de bijbehorende modeldienst van vormgegevens aan leeg gebied wordt geplaatst. NPR-22272: Hotfix voor GRANITE-1974

### Graniet {#granite-2}

* Stabiliteitsproblemen met de uitgeversinstantie voor het delen van bedrijfsmiddelen die worden veroorzaakt door geheugenlek. NPR-22205, NPR-23178: Hotfix voor Sling-5668, Sling-7292 en Sling-7470.
* De instabiele dienst identiteitskaart zou niet voor de namen van zittingsattributen moeten worden gebruikt. NPR-22821: Hotfix voor graniet-21059
* Wanneer een http   de door whiteboard beheerde sessie is ongeldig, de containersessie wordt ook ongeldig gemaakt als de sessie geen andere sessiekenmerken heeft. NPR-23059: Hotfix voor FELIX-5819
* LogbackManager kan sommige OSGi config in tijd van opstarten missen. NPR-23060: Hotfix voor graniet-19791

### Handel {#commerce-3}

* Schakel het maken van een workflow in het menu Experience Fragments in. NPR-22347: Hotfix voor CQ-4221661
* Ervaar Fragmentfouten die reproduceerbaar zijn op WeRetail. NPR-21958: Hotfix voor CQ-4220061
* Wanneer een pagina met een verwijderd ervaringsfragment wordt geactiveerd, wordt een NullPointerException gegenereerd. NPR-23179: Hotfix voor CQ-4239939

### Projecten {#projects}

* (Meertalig project) Het project vermeldt geen vertaaltaken voor meer dan 19 talen. NPR-22498: Hotfix voor CQ-4229978

### Workflow {#workflow}

* (Klassieke UI) Het toelaten van of het onbruikbaar maken van een werkschemalancering leidt tot slecht gedrag. NPR-22907: Hotfix voor CQ-4239153

## Forms {#forms-9}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

De belangrijkste markeringen voor AEM Forms zijn:

* Toegevoegde ondersteuning voor HTML5-invoertype.
* Correctie basisverificatie van SOAP-koptekst.
* Toegevoegde ondersteuning voor titelkenmerk voor hyperlink.
* PDF/UA-id ingeschakeld in de toegankelijkheidsstructuur van Forms Designer.
* Certificaatverificatie ingeschakeld voor Workbench-gebruikers.
* Toegevoegde ondersteuning voor het produceren van PDF-bestanden die compatibel zijn met PDF/A-2a of PDF/A-3a.

### Forms-invoegtoepassing {#forms-add-on-package-9}

#### UI Forms-Admin {#forms-admin-ui}

* Het wachtwoord is zichtbaar in duidelijke teksten op het inspecteren van wachtwoordgebied voor de pagina&#39;s van de Configuratie van de Verbindingen ECM. NPR-22508: Hotfix voor CQ-4236065

#### Forms Service {#forms-service}

* Wanneer SSL is ingeschakeld, werken de gebeurtenissen Verzenden en Verlaten niet met Form Analytics. NPR-22637; Hotfix voor CQ-4237973

#### Gebruikersbeheer {#user-management}

* Kan LDAP niet synchroniseren vanwege onjuiste cglib-nodep-versie. NPR-22493: Hotfix voor CQ-4234099

#### Adaptieve Forms {#adaptive-forms-2}

* De functies van de douane voor regelredacteur voegen extra toe; na functieaanroep mislukt de validatie, ook al retourneert de aangepaste functie true. NPR-22481: Hotfix voor CQ-4235499
* De component date-Picker volgt, ongeacht het geselecteerde datumpatroon, het patroon niet bij het weergeven van minimum- en maximumvalidatieberichten. NPR-22444: Hotfix voor CQ-4236269
* De datumnotatie die wordt verzonden in een verzendverzoek, moet worden uitgelijnd op het patroon in de component date-picker. NPR-22384
* Het opgegeven maximum aantal tekens voor een adaptief tekstvak in een formulier wordt niet ondersteund op Android 6.0 Samsung-apparaten. NPR-22363, NPR-22364: Hotfix voor CQ-4235205
* (Microsoft Edge) (IE11) De adaptieve component van het vorm-tekstgebied met multiline gebied toont &quot;Null&quot;als standaardwaarde in plaats van leeg. NPR-22284: Hotfix voor CQ-69107
* SOAP UTF-8 Input Encoding in Adaptive Forms retourneert fouten met verstoorde pagina. NPR-20105: Hotfix voor CQ-4222669
* De AEM Forms Container Component is niet beschikbaar om te bewerken zodra het verkeerde formulier op de sitepagina is geconfigureerd. Hotfix voor CQ-4237456
* De tests van de ontwikkeling ontbreken wanneer uitgevoerd op servers JEE. Hotfix voor CQ-4222082
* AF test het ontbreken op servers JEE wegens minificatiekwesties in het kader van Calvin. Hotfix voor CQ-4217220

#### Forms Manager {#forms-manager}

* (Firefox) De eigenschappen van het XML-schema van Adaptive Forms kunnen niet worden bijgewerkt omdat de opties in het Document of Record (DOR) niet worden weergegeven als vooraf geselecteerd op de eigenschappenpagina. NPR-22298: Hotfix voor CQ-4237402
* Forms die na publicatie van de pagina is gewijzigd, wordt niet opnieuw gepubliceerd wanneer u de site publiceert. NPR-23013: Hotfix voor CQ-4236566

#### Backend-integratie {#backend-integration-1}

* OOTB de basisauthentificatie voor de diensten van de ZEEP werkt niet voor basisauthentificatie in integratie FDM. NPR-23238: Hotfix voor CQ-4241308

#### Correspondentenbeheer {#correspondence-management}

* Als de XDP&#39;s van OOTB in de letter worden gebruikt en als voorbeeld worden weergegeven, wordt de inhoud weergegeven die met de voettekst wordt overlapt. Hotfix voor CQ-4212414

#### Assembler-service {#assembler-service}

* Discrepantie tussen Acrobat DC- en AEM-rapporten over de fout bij het controleren van de PDF/A-1b-compatibiliteit. NPR-22051, NPR-22050: Hotfix voor CQ-4226128, CQ-4227671

### Forms JEE-installatieprogramma {#forms-jee-installer-8}

#### Workbench {#workbench}

* Certificaatverificatie ingeschakeld voor Workbench-gebruikers. NPR-20644: Hotfix voor CQ-4214486
* Het serverlogboek downloaden met Workbench werkt alleen voor de ene server, maar voor de andere server werkt het niet. NPR-21079: Hotfix voor CQ-4229842

#### Procesbeheer {#process-management-1}

* (HTML-werkruimte) Problemen met de schermgrootte met schuifbalken. NPR-23288
* (HTML-werkruimte) Beginpunten van processen worden niet in alfanumerieke volgorde gesorteerd. NPR-22841 Hotfix voor CQ-4238944
* (HTML-werkruimte) Bereid gegevens voor die worden geactiveerd wanneer het formulier in de werkruimte wordt gesloten. NPR-21127: Hotfix voor CQ-4224574
* (HTML Workspace) Wanneer u een proces aanroept waarvoor notities met lange beschrijvingen nodig zijn, werkt de knop Notities uitvouwen niet. Hotfix voor CQ-4241488

#### Kern {#core-1}

* Fout aangetroffen bij opstarten terwijl de planner wordt gestart. NPR-22990
* Voorkomen dat browsers ingevoerde gegevens opslaan in HTML-formulieren. NPR-21762: Hotfix voor CQ-4206543
* De in de statische codeanalyse van Core gerapporteerde problemen moeten worden vastgesteld. Hotfix voor CQ-104446

#### PDFG-service {#pdfg-service-3}

* PDF Generator kan geen PDF-documenten met opgegeven bladwijzers maken. NPR-22921, NPR-22285: Hotfix voor CQ-4230562
* Toegevoegde ondersteuning voor het produceren van PDF-bestanden die compatibel zijn met PDF/A-2a of PDF/A-3a. NPR-23021: Hotfix voor CQ-4214172

#### Forms Designer {#forms-designer-1}

* PDF/UA-id ontbreekt wanneer deze wordt opgeslagen als PDF in Designer. NPR-23137
* Padobjecten, bijvoorbeeld: randen, onderstrepingen en hyperlinks worden niet gecodeerd wanneer deze worden opgeslagen als PDF in Designer. NPR-23136
* Afbeeldingsobject heeft geen selectiekader wanneer het vanuit Designer als PDF wordt opgeslagen. NPR-23134
* inline-hyperlinks die zijn gedefinieerd in Designer, krijgen geen label en hebben geen alternatieve tekst wanneer deze worden opgeslagen als PDF in Designer. NPR-23133
* Als u het XML-gegevenspakket opent met AEM 6.3 Forms Designer, wordt de XHTML-opmaak verwijderd uit de XML-bron. NPR-21178: Hotfix voor LC-3917046

#### LCM installeren {#install-lcm}

* Jsafe Jars bijwerken naar Cryptoj 6.1.3.1 in installatieprogramma en LCM. NPR-21370

#### Handtekeningenservice {#signatures-service}

* Er is een uitzondering opgetreden tijdens een poging een PDF-document digitaal te ondertekenen/certificeren via HSM. NPR-21154: Hotfix voor CQ-4226978

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.2.1 {#osgi-bundles-and-content-packages-included-in-5}

Lijst van OSGi-bundels opgenomen in AEM 6.3.2.1

[Bestand ophalen](assets/do-not-localize/bundle-list_002_.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.2.1

[Bestand ophalen](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 1 (6.3.1.0) in oktober 2017.

De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* Gewijzigde interface voor ondersteuning van de implementatie van CUG-functionaliteit in AEM Assets.
* Problemen met de gebruikersinterface op de pagina voor licentiecontrole zijn opgelost voor een betere ervaring.
* Ondersteuning voor OSGi-workflowtaken ingeschakeld in AEM Forms App.

### Activa {#assets-10}

* Gewijzigde interface voor ondersteuning van de implementatie van CUG-functionaliteit in AEM Assets. NPR-19485
* Het uploaden van een element als een rechtstreeks onderliggend knooppunt van zichzelf via de aanraakinterface veroorzaakt een probleem. Het element wordt geüpload als een direct onderliggend element van het eerder geselecteerde element. NPR-19736
* Datumbereik voorspellen en Bereik voorspellen werken niet bij het laden van een opgeslagen zoek-/slimme verzameling. NPR-19844: Hotfix voor CQ-4220808
* AEM wordt traag wanneer meerdere elementen (meer dan 4) naar Brand Portal worden gepubliceerd. NPR-2009: Hotfix voor CQ-4213426
* Kan elementen met spaties niet downloaden vanaf de pagina met licentiecontrole. NPR-20067: Hotfix voor CQ-4216557
* Problemen bij het uploaden van PSB-bestanden met meerdere alpha-lagen. NPR-20250: Hotfix voor CQ-4220869
* Gebruikers kunnen geen elementen downloaden met lange gedefinieerde bestandsnamen en disclaimer. NPR-20254
* ProductAssetsUploader verlaat de tijdelijke bestanden van JAVA-cache in de map Java TEMP. NPR-20256: Hotfix voor CQ-4221801
* Vervang de vergelijkingscode van de versie met de merkgebonden code van Adobe wegens vergunningskwesties. NPR-20272: Hotfix voor CQ-4223758
* De meta-gegevens voor een koordbezit, documentNumber verschijnt als datum terwijl het een aantal zou moeten zijn. NPR-20291: Hotfix voor CQ-4223991
* Het uitnemen van tekst blijft vastzitten voor een beschadigde PDF. NPR-20416: Hotfix voor CTG-4150375
* Gecomprimeerde bestanden die elementen bevatten die niet compatibel zijn met UTF-8, worden niet correct gedownload. NPR-20420: Hotfix voor CQ-4219961
* Te veel tekens in OmniSearch zorgen ervoor dat AEM server vastloopt. NPR-20434: Hotfix voor CQ-4223602
* Metagegevens van de DAM Asset-API onderbreken de xmp-write-back API&#39;s. NPR-20607: Hotfix voor CQ-4220455
* Prestatieproblemen bij het toevoegen van gebruikers aan verzamelingen. NPR-20699: Hotfix voor CQ-4225733
* Publiceren naar Brand Portal vanaf AEM is niet toegestaan voor Dynamic Media-sets. NPR-20320: Hotfix voor CQ-4221147
* Video met spaties en accenten levert geen video op voor de pagina Renditions. NPR-19961: Hotfix voor CQ-4221014
* Oplossing voor meerdere problemen met de verwerking van mappen met middel-API&#39;s. NPR-20569
* AEM Dynamic Media Classic (voormalig Scene7) synchroniseert geen elementen van AEM server wanneer het doelpad in de configuratie van de cloudservice naar een submap in het hoofdpad wijst. CQ-4228265
* De e-mailbundel met apache commons `{org.apache.commons/commons-email/1.5}` is toegevoegd ter vervanging van `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`.

### Sites {#sites-10}

* Problemen met beheerdersrechten: Kan leden van een gesloten gebruikersgroep niet verwijderen uit pagina-eigenschappen. NPR-20631
* De getypte werkstroomnaam moet beschikbaar zijn in het vak Melding wanneer u pagina publiceert via Publicatie beheren. NPR-20046: Hotfix voor CQ-4221586
* Als u opgemaakte tekst toepast op twee rijen in de Rich Text Editor en deze vervolgens samenvoegt in één alinea, worden de opgemaakte reeksen verwijderd. NPR-20110: Hotfix voor CQ-4223051
* Wijzigingen in veldeigenschappen op meerdere tabbladen van het dialoogvenster Eigenschappen bewerken worden soms niet opgeslagen. NPR-20286
* Onverwachte tag aan het einde van de geplakte inhoud in het inhoudsfragment. NPR-20413: Hotfix voor CQ-4224014
* Implementeerde een mechanisme in Adobe Campaign om het beleid van een inhoudsbron van een externe doelbron op te halen. NPR-20667
* De insteekmodule Richttekst werkt niet voor zowel inline als volledig scherm in de aanraakinterface met meerdere velden. NPR-20973

### Campagne {#campaign-1}

* Placeholders zijn niet zichtbaar in een pagina die veelvoudige parsys componenten bevat. NPR-20436; Hotfix voor CQ-4215000

### Handel {#commerce-4}

* De Fragmenten van de ervaring tonen niet behoorlijk in Internet Explorer 11. NPR-20161: Hotfix voor CQ-4223319
* In handelswerkstromen, wordt een leeg beeld automatisch opgenomen wanneer het creëren van een variant die op een primair product met veelvoudige beelden wordt gebaseerd. NPR-20068: Hotfix voor CQ-4222048
* Filteren met tags op verzamelingspagina&#39;s in de productconsole werkt niet. NPR-20292: Hotfix voor CQ-4224023

### Gemeenschappen {#communities-8}

* Inconsistente zoekresultaten met zoekresultaatcomponent. NPR-20070: Hotfix voor CQ-4220913
* E-mailmeldingen worden niet geactiveerd voor een van de aan de moderator gerelateerde activiteiten met betrekking tot gepubliceerde componenten. NPR-2012
* De lege paginering zonder resultaten wordt getoond voor anonieme communautaire gebruikers. NPR-20136: Hotfix voor CQ-4220738
* Vorm waakzame trekker wanneer een UGC als spam wordt ontdekt of wanneer een gebruiker op een pre-gematigde plaats post. NPR-20274: Hotfix voor CQ-96850
* Meerdere problemen met AEM Communities-sitepagina&#39;s zijn opgelost, waaronder onjuiste omleidingen en problemen met het vernieuwen van pagina&#39;s. NPR-20344
* CommunityUserOperationExtension wordt uitgevoerd in een klassecasting. NPR-20532: Hotfix voor CQ-4224385
* Na het maken van een Community-site kunnen gebruikers de site niet openen vanuit de sitemap omdat het contextpad niet wordt toegevoegd aan de URL. NPR-20730

### Integratie {#integration-6}

* Het migreren Analytics bestaande geloofsbrieven aan Authentificatie WSSE. NPR-19962: Hotfix voor CQ-4218071
* Het opnieuw activeren van het segment na een wijziging mislukt en er treedt een fout op. NPR-20054: Hotfix voor CQ-4218401
* In de configuratie van de cloudservice van Search&amp;Promote wordt de methode voor het ophalen van formulieren genegeerd, waardoor deze onbruikbaar wordt voor de instantie van de auteur. NPR-20447: Hotfix voor CQ-4206076
* Bij dubbelzinnige filterdefinitie in inhoudspakket worden paden overschreven wanneer het Search&amp;Promote-onderdeel wordt geïnstalleerd. NPR-20808

### Mobiel op aanvraag {#mobile-on-demand}

* Eigenschappen van metagegevens voor elementen van het type TXT worden telkens weergegeven in verschillende editors voor metagegevens wanneer de eigenschappen ervan worden weergegeven. NPR-20239

### Platform {#platform-3}

* Resolved an unclosed resource resolver uitzondering. NPR-19749: Hotfix voor graniet - 19143
* Verzoek om douanekaarten om samen met standaardgezondheidscontroles in het verrichtingendashboard worden getoond. NPR-20145
* De annotatielaag van de pagina-editor werkt niet goed in Internet Explorer 11. NPR-2022: Hotfix voor CQ-4222818
* De lekken van de zitting bij het plaatsen van de Agent van de Gebruiker als admin in replicatieagent. NPR-20578
* requestAttributes is niet unset voor andere gegeven-slim-middelverklaringen. NPR-20639: Hotfix voor 4226206
* Correctie van problemen met curl Head-aanvragen voor OOTB-middelen in AEM. NPR-20781: Hotfix voor CQ-4221520

### Projecten {#projects-1}

* De toegang tot van verschillende projecten van de console van Projecten duurt langer om te laden. NPR-20314
* Wanneer u AEM 6.3.0.1 installeert, wordt het sleutelarchief van de gebruiker met de update-service verwijderd. NPR-20018
* In sommige douaneplaatsingen, nemen de gebruikers die om een ontvanger in addTask module proberen te selecteren langer om de lijst in de gebruikersplukker te bevolken. NPR-20283: Hotfix voor CQ-4224193

### Gebruikersinterface {#user-interface-3}

* Kleurveld is ingesteld op &quot;altijd vereist&quot;, ondanks kenmerken in het dialoogvenster. NPR-19702
* De schuifbalk wordt niet op volledig scherm weergegeven voor een component met meerdere velden in Internet Explorer 11. NPR-20261: Hotfix voor CQ-4219782
* Vorige query&#39;s worden niet afgebroken als opeenvolgende query&#39;s worden geactiveerd, wat leidt tot onjuiste resultaten. NPR-20398: Hotfix voor GRANITE-19306

### Workflow {#workflow-1}

* Gebruikers worden niet op de hoogte gesteld van de workflowtaken die ze in hun Postvak IN ontvangen. NPR-20213: Hotfix voor CQ-4221639
* De OOTB-gebruikerkiezer in graniet laadt geen gebruikers wanneer u in de stap Deelnemer dialoogvenster op een vervolgkeuzelijst klikt. NPR-20236

## Forms {#forms-10}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-10}

#### Adaptieve Forms {#adaptive-forms-3}

* Ondersteuning voor samenvoegingsexpressie voor herhaalde deelvensters ontbreekt. NPR-20861
* In het vervolgkeuzemenu wordt de laatst opgeslagen waarde weergegeven, zelfs als de bijbehorende service voor het formuliergegevensmodel geen waarde retourneert. NPR-20710
* Kan de bestaande regels niet bewerken met Booleaanse beperkingen in de regeleditor. NPR-21128

#### Formulierportal {#form-portal}

* HTML-profiel wordt weergegeven voor een adaptief formulier, zelfs als het elementtype niet XDP is. NPR-20079

#### Backend-integratie {#backend-integration-2}

* Kan waarde van switch-component niet instellen tussen true/false. NPR-2111

#### OSGI Workflow {#osgi-workflow}

* Met workflowverzending kunt u slechts tien toepassingen beheren. CQ-4230193

#### HTML5 Forms {#html-forms-3}

* De naam van een XDP-formulierobject als subformulier wordt weergegeven als knopinfo wanneer dit niet is gedefinieerd in de toegankelijkheidsconfiguraties. NPR-20523

### Forms JEE-installatieprogramma {#forms-jee-installer-9}

#### Procesbeheer {#process-management-2}

* Het startpunt van FormSetPrefillApp vooraf instelt geen formuliervelden in de AEM Forms-app. NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* Installeer de nieuwste CTJPEG2K-bibliotheek voor een kritieke beveiligingskwetsbaarheid. Dit is van invloed op de modules XMLFM (AEM en IfBA), RM en PDFG. NPR-20625: NPR-21337.

### Inclusief functiepakketten {#feature-packs-included}

#### AEM Forms App {#aem-forms-app}

* Ondersteuning voor OSGi-workflowtaken ingeschakeld in AEM Forms App. CQ-4222638

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}

Lijst van OSGi-bundels opgenomen in AEM 6.3.1.2

[Bestand ophalen](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.1.2

[Get ](assets/do-not-localize/6_3_1_2-content-package-list.txt)
FileAEM Cumulative Fix Pack 6.3.1.1 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 1 (6.3.1.0) in oktober 2017 omvat.

De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* Publiceren naar Brand Portal ingeschakeld voor standaardformulier voor metagegevens.
* Gedragingen bij het weergeven van titels op de afbeeldingskaart voor afbeelding met dc: title, eigenschap ingesteld op String [] (multifield).
* Rendering van tijd aan de serverzijde vervangen door basis-tijdcomponent.
* Publicatietags van AEM naar Brand Portal vanuit tagbeheer-/tagingconsole ingeschakeld.
* Gepubliceerde JSON API voor het opnemen van inhoudsfragmenten.
* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.5.

### Activa {#assets-11}

* Als twee velden met dezelfde eigenschap worden toegewezen aan verschillende typen eigenschapvelden, treedt er een interne fout op. NPR-19462: HF voor CQ-4216828
* dc: titel en dc: de beschrijving verandert niet in een meerveldwaarde in crx /de. NPR-19570: HF voor CQ-4209086
* De dynamische viewer laadt de video-uitvoering van de laagste kwaliteit voor het testen van het afspelen van video in de auteursmodus. NPR-19004
* Dynamische uitvoering kan niet worden gedownload voor elementen die spaties in hun namen opnemen. NPR-19433: Hotfix voor CQ-4211738
* Kan geen volledige lijst met pagina&#39;s/middelen laden in de kolomweergave met Chrome. NPR-19566: Hotfix voor CQ-4214248
* De optie Publiceren naar Brand Portal is niet beschikbaar bij het selecteren van schema&#39;s, zoekfacetten of voorinstellingen. NPR-1950
* Als u een element selecteert in de kolomweergave en op Bewerken klikt, wordt er een fout geretourneerd. NPR-20301: Hotfix voor CQ-4220052
* Weergave Verlopen van activa is uitgeschakeld wanneer positieve en negatieve tijdzones worden overschreden. NPR-20329: Hotfix voor CQ-421933

### Campagne {#campaign-2}

* De componenten van de Slider van de campagne verschijnen niet wanneer de Standaardervaring voor een campagne wordt gekozen. NPR-19213

### Integratie {#integration-7}

* Aangepast bestand at.js publiceert niet wanneer het wordt geopend met de anonieme gebruiker. NPR-19542: Hotfix voor CQ-4219592
* Het gerichte gebied van de Motor in de config tovenaar wordt geplaatst aan ContextHub (AEM) in plaats van Adobe Target. NPR-19320: HF voor CQ-4218465
* De sectie Publiek wordt beschadigd tijdens het maken van ervaringen. NPR-19110
* Het doeldialoogvenster wordt niet weergegeven in de doelmodus wanneer een doelmodule meerdere keren wordt bewerkt en opgeslagen. NPR-19144: Hotfix voor CQ-4216708
* Toegangseigenschappen voor artikelen die onjuist zijn ingesteld in de Adobe Digital Publishing-oplossing op de klassieke gebruikersinterface. NPR-19367
* Onjuist gedrag van automatisch vouwen tijdens het aanpassen van aanbiedingen via Campagne als gebruikers toegang hebben tot meerdere gebieden. NPR-19290: Hotfix voor CQ-4218029

### Sites {#sites-11}

* De meervoudige samengestelde waarden van het gebieddropdown worden niet re-bevolkt toe te schrijven aan veranderingscode in Sidetrap.js na het bevorderen van de instantie aan AEM 6.1SP2-GVB3. NPR-19450: HF voor CQ-4194771
* WCMMode.EDIT werkt niet voor beoogde componenten op auteurswijze. NPR-19387
* Gepubliceerde JSON API voor het opnemen van inhoudsfragmenten. NPR-19500
* De functie Vet, cursief en onderstrepen werkt niet voor RTF-velden in het dialoogvenster Schrijver. NPR-19670: NPR-19718: Hotfix voor CQ-4219088

### Mobiel op aanvraag {#mobile-on-demand-1}

* Het renderen van problemen met AEM artikelconsole zoals het gebruik van afbeeldingen op volledige grootte maakt het traag. NPR-19088

### Vertaling {#translation-5}

* Kan geen voorvertoning genereren voor vertaalprojecten. NPR-19289

### Beveiliging {#security}

* SSL-verbindingsfout. Kan geen veilige verbinding maken met de server. NPR-19628

### Gemeenschappen {#communities-9}

* De post wordt teweeggebracht op inhoud het posten met pre-gematigde plaatsen. NPR-2008
* E-mailmeldingen werken voor geen van de aan de moderator gerelateerde activiteiten met betrekking tot gepubliceerde componenten. NPR-19767: HF voor CQ-4218060

### Platform {#platform-4}

* Stabiliteitsproblemen met AEM implementatie van productieservers. NPR-19707
* Aangepaste taglib die referentietags bevat die als script zijn geïmplementeerd, worden niet gevonden na de upgrade naar AEM 6.3. NPR-19087
* Oplossingen voor HTL-fouten voor AEM 6.3.1. NPR-19161
* Het veld Richtext kan niet worden bewerkt in de componenten met meerdere velden. NPR-19604: Hotfix voor graniet-16755
* De service Adobe-e-mailsjabloon voegt codes toe aan aangepaste gebruikerssjablonen. NPR-19190
* Hotfix voor eik 1.6.5. NPR-19148

### Handel {#commerce-5}

* De knoop van het Werkschema van het begin na het selecteren van een XF variatie redacteur heeft geen effect. NPR-19642: Hotfix voor CQ-4207796

### Projecten {#projects-2}

* Projecteditors kunnen geen elementen kopiëren/plakken in de map met projectmiddelen. NPR-19619: Hotfix voor CQ-4215321

### Web Content Management {#web-content-management}

* In het scherm Rollout kunnen selectievakjes die overeenkomen met livecopy-pagina&#39;s niet worden in- of uitgeschakeld. NPR-19518
* Het bulksgewijs bewerken van pagina-eigenschappen is niet correct bruikbaar, aangezien momenteel alle tabbladen en velden beschikbaar zijn voor grote versies. NPR-19451
* OOTB-eigenschappen en eigenschappen voor uitlijning van afbeeldingen worden niet weergegeven wanneer u een afbeelding bewerkt in een klassieke gebruikersinterface. NPR-19488: HF voor CQ-4217914

### Gebruikersinterface {#user-interface-4}

* Wanneer gebruikers de Google Chrome-browser gebruiken, kunnen ze de volledige lijst met pagina&#39;s/middelen niet laden met de kolomweergave in TouchUI. NPR-19566: Hotfix voor CQ-4214248

### Brand Portal {#brand-portal-1}

* Kan geen elementen van AEM met opmerkingen en annotaties publiceren. NPR-19590: Hotfix voor CQ-4218386
* Publicatietags van AEM naar Brand Portal inschakelen vanuit tagbeheer-/tagingconsole. NPR-20271: Hotfix voor CQ-4223948
* Het veld &quot;enabled&quot; corrigeren in de configuratiegebruikersinterface van de Brand Portal-cloudservice. Hotfix voor CQ-4211101
* Het zoeken naar formulierreplicatie mislukt. Hotfix voor CQ-4220080

## Forms {#forms-11}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-11}

#### Aangepaste formulieren {#adaptive-forms-4}

* Verzenden naar JEE-workflow retourneert geen uitvoerparameter van JEE-zijde naar AEM en genereert een fout met de tekst ‘Negeren omdat de waarde niet primitief is’. NPR-20265
* Adaptieve Forms staat PDF niet toe als bijlage in Safari. NPR-19625
* RestoreGuideState overschrijft de aangepaste contextProperty map. CQ-422877
* Wanneer het vormen van Google reCaptcha gebruikend Cloud Service, in milieu&#39;s die configuratie van org.apache.http.proxyconfigurator voor externe verbindingen vereisen, schijnen de vraag van de POST niet door PROXY te gaan. NPR-20454
* Adaptieve Forms op basis van XSD-schema&#39;s verzendt onjuiste XML-waarden voor numerieke velden in installaties met een ander decimaalteken dan &quot;&quot;. resulteert in fouten. NPR-20444
* Proxy-instellingen die zijn ingesteld voor &#39;Apache HTTP Components Proxy Configuration&#39; worden niet ondersteund wanneer een HTTP-aanvraag wordt ingediend bij een externe server. De onderbrekingskwesties van de verbinding gebruikend de vraag van de GET of van de POST van HTTP. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Forms-gegevensintegratie {#forms-data-integration}

* UTF-8-tekens als uitvoer van de SOAP-service worden niet correct gekopieerd naar Adaptieve Forms-velden voor niet-Engelse landinstellingen. NPR-20238: NPR-20103

#### Correspondentenbeheer {#correspondence-management-1}

* Bij het kopiëren van inhoud plakken uit het tekstbestand gaan de kleur en het lettertype van de inhoud verloren in de Teksteditor. NPR-19521

#### Assembler Services {#assembler-services}

* Verschil tussen de resultaten van Acrobat en AEM tijdens een compatibiliteitscontrole van een document naar de PDFA-1b-indeling. NPR-19280

#### Workflow {#workflow-2}

* De stap van het Ondertekenen van het werkschema om http vraag toe te staan om door de volmacht te verbinden. NPR-20529

#### HTML5 Forms {#html-forms-4}

* Toegevoegde ondersteuning voor gebeurtenis preSubmit. NPR-20604

### Forms JEE-installatieprogramma {#forms-jee-installer-10}

#### Procesbeheer {#process-management-3}

* De tabbladen Werkstroombijlage, Opmerkingen en Details functioneren niet in de werkruimte wanneer het formulier gemaximaliseerd/geminimaliseerd en als concept opgeslagen of doorgestuurd wordt. NPR-20243
* Tekstveld met meerdere regels (TextArea) behoudt geen teken voor nieuwe regels of tekstonderbreking na het verzenden van gegevens in de HTML-werkruimte. NPR-20085

#### Procesrapportage {#process-reporting}

* Bij het rapporteren van processen worden de gegevens niet correct opgehaald vanwege de Null-aanwijzeruitzondering. NPR-19759

>[!NOTE]
>
>Installeer het LiveCycle-insluitpakket in het artikel [AEM Forms Release](aem-forms-releases.md) om het probleem op te lossen.

#### Standaardservices {#standard-services}

* docConvertor ondersteunt geen transparanties voor afvlakking in PDF en kan geen PDF/A maken. NPR-16228: Hotfix voor CQ-4214488

#### Kern {#core-2}

* Wanneer AEM Forms-server die wordt uitgevoerd in een clusterconfiguratie in een JBoss-toepassing wordt gestopt, wordt de verbinding van de toepassingsserver met de database verbroken. Dit kan leiden tot problemen met gegevensbeschadiging. NPR-19724

### Inclusief functiepakketten {#feature-packs-included-1}

* Vervolgkeuzelijst met metagegevensschema kan niet verplicht worden gesteld, omdat verplichte veldvalidatie ontbreekt voor elementen. NPR-17882: KP voor CQ-4208373

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.1.1 {#osgi-bundles-and-content-packages-included-in-7}

Lijst van OSGi-bundels in AEM GVB 6.3.1.1

[Bestand ophalen](assets/do-not-localize/bundle-list.txt)

Lijst van inhoudspakketten die zijn opgenomen in AEM GVB 6.3.1.1

[Bestand ophalen](assets/do-not-localize/content-package-list.txt)

AEM Cumulatief Fix Pack 6.3.0.2 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 in April 2017.

De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* Controleerbaarheid van gebruikerstoegang
* Inclusief versie 1.6.2 van de ingebouwde opslagplaats (Apache Jackrabbit Oak)
* Opgeloste problemen met niet-afgesloten oplossing van bronnen
* Vereenvoudigde configuratie voor services voor slimme inhoud
* Opgeloste problemen met fragmentvalidatie voor inhoudsfragmenten
* Verbeterde bewerkbaarheid van metagegevensschema&#39;s op hybride apparaten
* Opgeloste problemen met synchronisatie op componentniveau in live kopieën
* Verbeterde bruikbaarheid van pagina&#39;s met veel inhoud in de kolomweergave
* Verbeterde compatibiliteit met de naamgevingsconventie voor pagina&#39;s met lange titels
* Verbeterde functionaliteit voor het aanpassen van campagnes op Touch UI
* Oplossingen voor verschillende projectoverlayproblemen

### Platform {#platform-5}

* Hotfix voor eik 1.6.2. NPR-16993
* Wanneer u de zoekopdracht opent met een filter, wordt het pad niet meer ingesteld. NPR-17398: Hotfix voor CQ-4204870
* Verplichting voor de controleerbaarheid van wijzigingen in de gebruikerstoestemming in AEM. NPR-17061
* Lingingerverbindingen met DM-Cloud Services die uitzonderingen op &quot;Te veel geopende bestanden&quot; veroorzaken. CQ-421407

### Activa {#assets-12}

* Gebruiksproblemen met het configureren van services voor slimme inhoud met behulp van verschillende opties. NPR-18200: Hotfix voor CQ-4201557
* Het weglekken van middelen in binaire stromen aan S3 datastore. NPR-18041: Hotfix voor CQ-4209506
* Er treedt een fout op wanneer een tekstbestand met ASCII/UTF-8-codering naar AEM Assets wordt geüpload en het genereren van miniaturen mislukt. NPR-18006: GVB voor CQ-4209345
* Standaardmetagegevensschema leidt tot validatie van inhoudsfragmenten. NPR-17769: Hotfix voor CQ-4211111
* Niet-afgesloten resource resolver in com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: GVB voor CQ-4209018
* Verzoek om veelvoudige replicatieagenten voor het publiceren van activa aan Brand Portal tot stand te brengen. NPR-17189
* De taak van het overzicht voor activa onder de Japanse taalomslag werkt niet. CQ-4204782
* Een null-aanwijzeruitzondering treedt op wanneer een element van de eigenschappenpagina wordt verplaatst. CQ-4204251
* AEM kan volgende verwijzingen naar een element op de eigenschappenpagina niet bijhouden als het meerdere keren is gekoppeld aan een InDesign-document. CQ-4204186
* Problemen met het toevoegen van nieuwe tabbladen in de vorm van het metagegevensschema wanneer deze worden bewerkt in Chrome op hybride apparaten. CQ-42018-10
* Wanneer dubbele elementen worden geüpload, wordt de optie (verwijderen/behouden) op alle elementen toegepast, zelfs als deze optie niet is geselecteerd in het dialoogvenster Gedetailleerde duplicaten. CQ-4201673
* Een null pointer-uitzondering wordt weergegeven wanneer een elementmap met meer dan 150 binnenkomende verwijzingen wordt verplaatst. CQ-4200981
* Als er een conflict optreedt bij het uitpakken van de inhoud van het ZIP-bestand, wordt voor een gedownloade elementmap de standaardoptie weergegeven als versie Maken in plaats van beide. CQ-97800
* Gebruikers met de machtiging Alleen-lezen kunnen geen voorvertoning van inhoud weergeven via AEM Mobile-inhoudsbeheer. NPR-17486: GVB voor CQ-4209690
* De knop Catalogus maken werkt niet in de kolomweergave in de Catalogusconsole. CQ-4209952

### Sites {#sites-12}

* Problemen met het insluiten van beeld-/videocomponenten via attribuut data-Snit-resource. NPR-18182: GVB voor CQ-4212100
* Gewijzigde gelokaliseerde componenten worden niet teruggezet naar hun oorspronkelijke vorm wanneer de overerving opnieuw wordt toegepast in een LiveCopy. NPR-18172: Hotfix voor CQ-4211379
* Problemen met het navigeren door een pagina met veel inhoud in de kolomweergave in Touch UI. NPR-17799: Hotfix voor CQ-4199611
* Niet-afgesloten resource resolver in `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: GVB voor CQ-4211152
* Paginanaam wordt niet gegenereerd volgens de conventie voor lange paginatitels. NPR-17633: Hotfix voor CQ-4209056
* Problemen met het maken van pagina&#39;s via Touch-gebruikersinterface in AEM 6.3 die zijn geïmplementeerd op Jreliëf EAP 6.4. NPR-17589: Hotfix van CQ-4210137
* De leverancier van de werkstroomstatus zorgt ervoor dat de instantie vergrendeld wordt wanneer geneste groepen aanwezig zijn. NPR-17556: Aanvraag van het GVB voor CQ-4202056
* Niet-afgesloten resourceoplosser in de volgende objecten:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: GVB voor CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: GVB voor CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: GVB voor CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: GVB voor GRANITE-17404

### Integraties {#integrations-1}

* Opgeloste AEM de componentenfouten van het Onderzoek die kunnen voorkomen wanneer AEM Cliënt 3.1 van HTTP van Dag OSGI met een Volmacht wordt gevormd die de Authentificatie van de Samenvatting vereist. NPR 18128: Hotfix voor NPR-18029
* Kwesties met het personaliseren van campagnes en bijbehorende ervaringen via Klassieke UI. NPR-18127: Hotfix voor CQ-4211559
* Wanneer u een merk/zone instelt op een hoofdpagina van een site, kan overerving na annulering niet worden hersteld voor Gebieden in subpagina&#39;s. NPR-17753: Hotfix voor CQ-4210139

### Workflow {#workflow-3}

* In een niet-transiënte workflow worden de procesgeschiedenis en wijzigingen in metagegevens die vóór een externe processtap zijn aangebracht, niet voortgezet. NPR-17848: Hotfix voor GRANITE-17757
* Waarden uit de dialoogvelden van de workflow blijven niet behouden in het knooppunt Werkitem. NPR-17734: Hotfix voor CQ-4210369
* Onscheidbare datumfout treedt op wanneer u een taak bewerkt vanuit Postvak IN. CQ-4208749

### Projecten {#projects-3}

* Oplossingen voor verschillende projectoverlayproblemen. NPR-17733
* Herstructurering van de pods in de projectmodule maakt het minder configureerbaar. CQ-4209859
* Het pad naar elementen verandert in de respectievelijke gelokaliseerde sites wanneer pagina&#39;s worden toegevoegd aan de vertaaltaak. CQ-4206007

### Beveiliging {#security-1}

* Problemen met het uploaden van avatar-afbeeldingen voor LDAP-gebruikers. NPR-16561
* Verzoek om een geüpgrade versie van org.apache.sling.servlets.post servlet (2.3.22) in Apache Sling API te gebruiken om een XSS-kwetsbaarheid te voorkomen. NPR-18963

## Forms {#forms-12}

AEM Forms-oplossingen worden geleverd via het Forms-invoegpakket en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie [AEM Forms Release](aem-forms-releases.md) voor meer informatie.

De belangrijkste markeringen voor AEM Forms zijn:

* Oplossingen in tekstmodules voor correspondentiebeheer, voorvertoningen van brieven en programmatically het lanceren leiden tot correspondentiebeheer UI.
* Hiermee wordt de PDF/A-1b-validatie, conversie van grote afbeeldingsbestanden naar PDF en PDF-documenten in de Japanse taal in PDF Generator gecorrigeerd.
* Oplossingen voor de bruikbaarheid van correspondentiebeheer, documentbeveiliging en de werkstroom van formulieren.
* Extra ondersteuning voor het vastleggen van auditgebeurtenissen voor het handtekeningveld voor scripts.

### Forms-invoegtoepassing {#forms-add-on-package-12}

**Correspondentenbeheer**

* Bij het bewerken van een correspondentiebeheerfragment worden in de teksteditor inline voorwaarden weergegeven, samen met de verwerkte tekst. CQ-421930
* Bij het maken van een brief voor correspondentiebeheer wordt de beschrijving van de brief niet opgeslagen. NPR-18089
* De extra marge boven en onder een lijst met opsommingstekens is zichtbaar in de teksteditor, maar niet in HTML- en PDF-uitvoering. NPR-18126
* Wanneer HTML verzenden de methode van de POST gebruikte, creeert correspondentie UI niet om te lanceren. NPR-18202
* Wanneer een tekstmodule wordt opgeslagen en een expressie in de tekstmodule geen openings- of afsluitende expressietags bevat, wordt geen foutbericht weergegeven. In de tekstmodule wordt een foutbericht weergegeven en kan de letter niet worden weergegeven. NPR-18535
* Wanneer nieuwe inhoud wordt toegevoegd of de Enter sleutel wordt geduwd op, wordt een div markering toegevoegd aan de tekstmodule. NPR-18240

**Assembler**

* Bij het valideren van een PDF-document op compatibiliteit met PDF/A-1b, retourneert AEM Forms een validatiefout: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. Het PDF-document retourneert de fout niet wanneer deze wordt gevalideerd met Adobe Preflight en software van derden. NPR-18011
* Bij het valideren van PDF-documenten op compatibiliteit met PDF/A-1b retourneert AEM Forms een validatiefout: Formulierveld heeft meerdere weergaven. De PDF-documenten zijn compatibel met PDF/A-1b. NPR-18013

**Controlemap**

* Als u tijdens het maken van een controlemap selecteert of u bestanden wilt verwerken met een workflow, wordt de keuzelijst van het workflowmodel afgekapt weergegeven. NPR-17566

**HTML5 Forms**

* AEM Forms legt geen controlegebeurtenissen vast voor het veld Scripthandtekening. NPR-15286

**Forms Manger**

* De gebruikersinterface van AEM Forms bevat alle elementen in de oudste eerste volgorde. Gebruikers kunnen de middelen niet opnieuw rangschikken in de nieuwste eerste volgorde. NPR-18450

**Java API-naslag**

JavaDocs toegevoegd voor de klasse com.adobe.livecycle.content. NPR-18468

### Forms JEE-installatieprogramma {#forms-jee-installer-11}

**PDF Generator**

* PDF Generator-service kan afbeeldingen van meer dan 100 MB niet converteren naar PDF-documenten. Ref. nr. CQ-4208628
* Als u de service PDF Generator gebruikt met OCR voor de Japanse taal, wordt een omgekeerde PDF gegenereerd. NPR-17602

**Procesbeheer**

* De TaskContext-variabele wordt niet gevuld voor AEM Forms-processen. NPR-18199

**Documentbeveiliging**

* Microsoft Excel en Microsoft PowerPoint hebben veel meer tijd nodig om de documenten te openen die zijn beveiligd met AEM Document Security Extension voor Microsoft Office. CQ-4212358
* Wanneer een nieuw beleid wordt gecreeerd en een beleid met de zelfde naam zoals bestaand, komt een interne serverfout voor. NPR-18247

## Functiepakketten inbegrepen {#feature-packs-included-2}

* Verplichting voor de controleerbaarheid van wijzigingen in de gebruikerstoestemming in AEM. NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 is een belangrijke update die verscheidene interne en klantenfixes omvat aangezien de algemene beschikbaarheid van AEM 6.3 in April 2017.De belangrijkste hoogtepunten van het AEM Cumulatieve Pak van de Fix zijn:

* Verbeteringen op het volgende gebied:

   * Inhoudsfragmenten, Sites en de Rich Text Editor, Regeleditor en de componenten van de Sjablooneditor
   * Sociale revisie en aanmelding bij Facebook
   * Vertaaltaken configureren en starten
   * Reactietijd voor toegang tot meldingen in sociale gemeenschappen
   * Weergave van controletaken in de DAM-gegevensopslagruimte

* Verstrekt bevestigingsoptie in de Manager van het Pakket voor het ontdekken van conflicten tussen bekleding en GFP

## Instructies voor gestreken fijn papier downloaden via softwaredistributie {#download-instructions-for-cfp-via-package-share}

U kunt het pakket van GFP direct van [Softwaredistributie](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8) downloaden of de volgende stappen uitvoeren:

1. Open [Softwaredistributie](https://experience.adobe.com/downloads). U hebt een Adobe ID nodig om u aan te melden bij de softwaredistributie.
1. Tik **[!UICONTROL Adobe Experience Manager]** beschikbaar in het koptekstmenu.
1. Tik op de pakketnaam, selecteer **[!UICONTROL Accept EULA Terms]** en tik **[!UICONTROL Download]**.

## Installatie-instructies {#installation-instructions}

Deze sectie doorloopt u door de vereisten en de stappen om GVB te installeren.

### Voordat u gaat installeren {#before-you-install}

>[!NOTE]
>
>De facultatieve Packs van de Eigenschap die door Adobe worden verstrekt hebben gebiedsdelen op de versieversie en Cumulatief Pak van de Moeilijke situatie. Als u een Feature Pack hebt geïnstalleerd, neemt u contact op met het [AEM Customer Care team](https://helpx.adobe.com/marketing-cloud/contact-support.html) om de compatibiliteit met dit Cumulative Fix Pack voor AEM 6.3 te valideren.

>[!NOTE]
>
>U wordt aangeraden validatie uit te voeren voor elk nieuw installatiepakket voordat u probeert het pakket te installeren. Vóór de validatie worden eventuele fouten die vóór de installatie zijn gevonden, geanalyseerd en gerapporteerd en worden gebruikers proactief gewaarschuwd voor dergelijke fouten.
>
>U hebt toegang tot documentatie voor de optie Valideren op [https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 is een voorwaarde voor het GVB. Ga naar [Upgrade Documentation](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html) voor gedetailleerde instructies over het upgraden van een AEM installatie naar AEM 6.3.
* Voor een clusterplaatsing die RDBMK of MongoDB gebruikt, kan het pakket van GFP op om het even welke instanties van de Auteur worden geïnstalleerd die de Manager van het Pakket gebruiken.
* Voordat u het cumulatieve reparatiepakket installeert, moet u zorgen dat u een momentopname maakt of een back-up maakt van uw AEM.
* Het verwijderen van het GVB wordt niet ondersteund.

### Nieuwe loggers toevoegen {#adding-new-loggers}

Om zuivert niveau registreren te vormen en een activiteitenlogboek tijdens installatie van SPs/GVBs terug te winnen, kunt u de hieronder stappen volgen:

* U kunt een nieuw logger bij de standaardplaats [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) met de hieronder eigenschappen toevoegen:

   * Logniveau: Foutopsporing
   * Additief: false
   * Logbestand: logs/activity.log
   * Logger: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

Activity.log wordt gemaakt in   crx -quickstart /logs.

### Installeer het Cumulative Fix Pack via Software Distribution {#install-the-cumulative-fix-pack-via-package-share}

Voer de volgende stappen uit om het Cumulative Fix Pack op een bestaand AEM 6.3 exemplaar te installeren:

1. Klik op de koppeling [Softwaredistributie](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) om het pakket te downloaden.

1. Open [Pakketbeheer](http://localhost:4502/crx/packmgr/index.jsp) en klik **[!UICONTROL Upload Package]** om het pakket te uploaden.

1. Selecteer de pakketnaam en klik op **[!UICONTROL Install]**.

### Automatische installatie {#automatic-installation}

Het GVB kan automatisch in een lopende instantie op de volgende manieren worden geïnstalleerd:

* Plaats het pakket in `../crx-quickstart/install` terwijl de server wordt uitgevoerd. Het pakket wordt automatisch geïnstalleerd.
* Gebruik [HTTP API van de Manager van het Pakket](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/package-manager.html) - zorg ervoor dat u `cmd=install&recursive=true` gebruikt - zodat wordt het genestelde pakket geïnstalleerd.

### Installatie valideren {#validate-installation}

1. Op de pagina Productinformatie ( `/system/console/  productinfo`) moet nu de bijgewerkte versietekenreeks &quot;Adobe Experience Manager, Version 6.3.3.8&quot; onder Geïnstalleerde Producten worden weergegeven.
1. Alle OSGI-bundels zijn actief of FRAGMENT in de OSGI Console (Webconsole gebruiken: `/system/console/bundles`).

>[!NOTE]
>
>Bij een geslaagde installatie van het pakket wordt in de foutlogboeken een informatief bericht weergegeven waarin wordt aangegeven dat het inhoudspakket is geïnstalleerd, zoals &quot;Content Package **AEM-6.3.3-Cumulative-Fix-Pack-7** is geïnstalleerd.&quot;

>[!NOTE]
>
>Sinds AEM 6.3.3.1 is het logniveau in Jackrabbit FileVault voor de meeste berichten veranderd van INFO in DEBUG. Als u installatielogboeken wilt verkrijgen voor een inhoudspakket dat is geïnstalleerd op AEM 6.3.3.1 of hoger, schakelt u het DEBUG-logniveau in voor org.apache.jackrabbit.vault.packaging.impl.

### AEM Forms installeren {#install-aem-forms}

>[!NOTE]
>
>Sla deze sectie over als u AEM Forms niet gebruikt.

#### AEM Forms-invoegtoepassing installeren {#install-forms}

1. Controleer of u het AEM 6.3.3.x-pakket voor gestreken fijn papier hebt geïnstalleerd.
1. Download het overeenkomstige Forms add-on pakket dat u vindt op [AEM Forms releases](aem-forms-releases.md) voor uw besturingssysteem.
1. Installeer het invoegpakket voor Forms zoals beschreven in [Invoegpakketten voor AEM formulieren installeren](https://helpx.adobe.com/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html).

#### AEM Forms JEE-bundelpakket installeren {#install-aem-forms-jee-bundles-package}

Correcties in AEM Forms JEE worden geleverd via een afzonderlijk installatieprogramma. Zie [GFP installeren op AEM Forms JEE](install-cfp-aem-forms-jee.md) voor informatie over het installeren van een GFP op AEM Forms op JEE.

#### Installatieprogramma van Forms Designer {#designer-installer}

1. Voer het bestand Designer 6.2.0_&lt;Language>_Cumulative_QF.msp uit om de update te installeren.
1. Klik in het welkomstscherm op **update**. De installatie wordt gestart.
1. Nadat de installatie is voltooid, klikt u op **finish**.

## Configuratie-instellingen voor AEM Forms JEE (JBoss EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Als u 6.3.3.0 of recentere versies installeert, voer de hieronder procedure uit om montages voor JBoss toepassingsserver te vormen. Als u 6.3.3.0 installeert op de AEM Forms-server die wordt uitgevoerd op WebLogic- of IBM WebSpehere-toepassingsservers van het Oracle, is geen aanvullende configuratie vereist. Zie [AEM 6.3.3.0 Release Notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) voor meer informatie.

## Configuratie-updates voor Search&amp;Promote-integratie {#configuration-updates-for-search-promote-integration}

Met AEM Cumulatieve die Pak 6.3.0.2 van de Moeilijke situatie en recentere versies, de configuratie OSGi voor de Integratie van de Search&amp;Promote wordt gebruikt is **Apache Configuratie van de Volmacht van HTTP Componenten**. De proxyconfiguratie van Day Commons HTTP Client 3.1 wordt niet meer gebruikt.

## Bekende problemen {#known-issues}

* De volgende fouten en waarschuwingen kunnen optreden tijdens de installatie van AEM GVB 6.3.3.x en kunnen veilig worden genegeerd:

   * *WARN* [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallaak-0.0.2-jar-with-dependences.jar runtime-uitzondering.
   * *ERROR* [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Time-out wachten op reg change om niet-geregistreerd te voltooien. CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver-service ontbreekt, kan geen serviceaanvragen verzenden en status 503 verzenden
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: kan bron [/bin/receive] niet controleren, paginabeheer niet beschikbaar
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: Het aanroepen van de fouthandler heeft geleid tot een fout
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Oorspronkelijke fout null
   * org.apache.sling.engine.impl.DefaultErrorHandler Error-handler mislukt:java.io.IOException
   * *ERROR* [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory heeft null geretourneerd. (Component: com.day.cq.dam.handler.standard.ps.PostScriptHandler)

**Brand Portal**

* Vanaf 6.3.1.2 is de knop Publiceren naar Brand Portal voor slimme verzamelingen verwijderd.

**Gebruikersinterface**

>[!NOTE]
>
>Neem contact op met de [AEM klantenservice](https://helpx.adobe.com/marketing-cloud/contact-support.html) voor het geval dat een van deze twee problemen gevolgen heeft voor u.

* Het hoge gebruik van cpu wordt gezien toe te schrijven aan veel verzoeken in de functionaliteit van het Onderzoek Admin. NPR-24229
* PathField wordt niet geselecteerd in pathBrowser wanneer het heropenen van de component. NPR-24177

## Voor NPR-27692 vereiste configuratie-instellingen {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Deze configuratie-instelling is van toepassing op GVB 6.3.3.2 en hoger. Het geeft u de opdracht om de eigenschappen van de laarsdelegatie in het .properties-bestand `sling` bij te werken.

Volg de onderstaande stappen om wijzigingen in adobe- livecycle - cq -author.ear/ cq.war handmatig bij te werken:

* Stop de AEM server.
* Ga naar adobe-livecycle-cq.ear/cq.war
* Open adobe-livecycle-cq.ear/cq.war/WEB-INF/web.xml voor bewerking:

   * de **sling.bootDelegatie.ibm** param-name waarde bijwerken met:

      * com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * Na de bovenstaande wijziging moet de init-param er als volgt uitzien:

      * &lt;init-param>\
         &lt;param-name>sling.bootDelegation.&lt;/param-name> &lt;param-value>ibmcom.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* Verwijder het vorige Enterprise Archive-bestand (EAR) van de websphere-toepassingsserver en installeer het bijgewerkte EAR-bestand volgens de stappen in Section 10.2 van [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Sla het bestand op en start de server opnieuw. [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Voor NPR-23208 vereiste configuratie-instellingen {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Deze configuratie-instelling is van toepassing op 6.3.2.2 en hoger. Het geeft u de opdracht om het beleid van de Lijsten van het Toegangsbeheer (ACL) manueel door CRX-DE bij te werken aangezien ACLs niet door de installatie van GFP wegens &quot;merge_preserve&quot;acHandling wordt bijgewerkt.

**Documentatie voor het toevoegen van ACL beleid manueel**

Om ACL beleid bij te werken, voeg de hieronder controles van de Toegang door CRX-DE toe:

`1)` Op pad &quot;/content&quot;\
`a)` Opdrachtgever: referentieaanpassingsdienst\
Type: Toestaan\
Bevoegdheden : jcr:read , jcr:modifyProperties\
Beperkingen : rep:glob=&quot;/*/jcr:content&quot;\
`b)` Opdrachtgever: referentieaanpassingsdienst\
Type: Toestaan\
Bevoegdheden : jcr:read , jcr:modifyProperties\
Beperkingen : rep:glob=&quot;/*/jcr:content/*&quot;

`2)` Op pad &quot;/content/usergenerated&quot;\
`a)` Opdrachtgever: referentieaanpassingsdienst\
Type: Toestaan\
Bevoegdheden : jcr:write

`3)` Op pad &quot;/etc&quot;\
`a)` Opdrachtgever: referentieaanpassingsdienst\
Type: Toestaan\
Bevoegdheden : jcr:read , jcr:modifyProperties\
Beperkingen : rep:glob=&quot;/*/jcr:content&quot;\
`b)` Opdrachtgever: referentieaanpassingsdienst\
Type: Toestaan\
Bevoegdheden : jcr:read , jcr:modifyProperties\
Beperkingen : rep:glob=&quot;/*/jcr:content/*&quot;

## Voor NPR-19450 vereiste configuratie-instellingen {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Deze configuratie-instelling is van toepassing op GVB 6.3.1.1 en hoger.

**Configureer de eigenschap CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

De eigenschap bepaalt de maximale diepte van de knoopsubstructuur onder het knooppunt ` /  jcr   :content`, tot welke knooppunten in de gegevensopslagruimte worden gebruikt voor het ophalen van de pagina-eigenschappen. Een knooppunt onder de opgegeven diepte in deze eigenschap wordt genegeerd.

De standaardwaarde is 1. De waarde kan worden overschreven door het bestand constants.js (`/libs/cq/ui/widgets/source/constants.js`) te bedekken zonder opmerkingen toe te voegen aan de eigenschap CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL en er de vereiste waarde aan toe te wijzen (de maximale diepte onder de eigenschap / jcr:content tot welke de pagina-eigenschappen gegevens zijn opgeslagen).

**Als de gebruiker meerdere pagina&#39;s moet maken, zodat het aantal knooppunten onder het inhoudknooppunt van de pagina / jcr :groter wordt dan 1000, voert u de volgende stappen uit om configuratiewijzigingen uit te voeren:**

* De JSON Max-resultaten van Apache Sling configureren
* Servlet ophalen met `/system/console/  configMgr`
* Stel de waarde ervan in op een getal > 1000 (de huidige standaardwaarde), zodat dit getal groter is dan het totale aantal knooppunten in de substructuur / jcr:content tot de hierboven geconfigureerde diepte.

Hierdoor kan de sling GET servlet alle vereiste knooppunten retourneren.

## Uber Jar {#uber-jar}

De Uber Jar voor 6.3.3.8 is beschikbaar bij [Adobe Public Maven repository](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/).

Om Uber Jar in een Geweven project te gebruiken, verwijs naar het artikel, [Hoe te om Uber jar](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) te gebruiken en de volgende gebiedsdeel in uw projectPOM te omvatten:

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## Verwijderde/vervangen functies {#deprecated}

Deze sectie bevat een lijst met functies en mogelijkheden die zijn verwijderd of verouderd uit AEM 6.3.

| Gebied | Functie | Vervanging | Versie |
|----|-----|-----|-----|
| Integratie van middelen en Adobe Creative Cloud | [AEM naar het ](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/creative-cloud.html) delen van mappen in Creative Cloud is in AEM 6.2 geïntroduceerd als een manier om creatieve gebruikers toegang te geven tot middelen van AEM. Een nieuwe mogelijkheid die wordt vrijgegeven in de Creative Cloud-toepassing, de Adobe Asset Link, biedt een veel betere gebruikerservaring en een krachtigere toegang tot middelen van AEM rechtstreeks vanuit Photoshop, InDesign en Illustrator.<br /> Adobe zal geen verdere verhogingen aan de omslag het delen capaciteit maken. Hoewel de functie in AEM is opgenomen, wordt klanten sterk aangeraden de vervangende functie te gebruiken. | Adobe Asset Link of Desktop App. Zie [AEM Creative Cloud integratie](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html) artikel voor meer informatie. | AEM 6.3.3.x |

## OSGi-bundels en inhoudspakketten inbegrepen {#osgi-bundles-and-content-packages-included-1}

De volgende tekstdocumenten maken een lijst van de bundels OSGi en de Pakketten van de Inhoud inbegrepen in GVB.

* [Lijst van OSGi-bundels opgenomen in AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Lijst van inhoudspakketten opgenomen in AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM releases en updates](https://helpx.adobe.com/experience-manager/aem-releases-updates.html)
>* [AEM 6.3-hotfixepagina](https://helpx.adobe.com/experience-manager/kb/aem63-available-hotfixes.html)
>* [Opmerkingen bij de release AEM 6.3](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM productpagina](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.3-documentatie](https://docs.adobe.com/content/docs/en/aem/6-3.html)
>* Abonneren op [Adobe prioritaire productupdates](https://www.adobe.com/subscription/priority-product-update.html)

