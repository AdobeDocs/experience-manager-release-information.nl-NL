---
title: AEM 6.3 Cumulatieve Fix Pack
description: AEM 6.3 Opmerkingen bij de release Cumulative Fix Pack.
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
source-git-commit: 53803f61394144ed81367a5c050814223fc6d565
workflow-type: tm+mt
source-wordcount: '17337'
ht-degree: 0%

---

# AEM 6.3 Opmerkingen bij de release Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Gegevens vrijgeven {#release-information}

| **Product** | Adobe Experience Manager |
|---|---|
| **Versie** | 6,3 |
| **Versie** | Cumulatief Pak 6.3.3.8 van het Fix op [ Distributie van de Software ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Vereiste** | [ AEM 6.3 Service Pack 3 (6.3.3.0) ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **Algemene beschikbaarheid** | 5 maart 2020 |

### Cumulatief reparatiepakket {#cumulative-fix-pack}

De Adobe introduceerde één-leveringsmodel voor het vrijgeven van moeilijke situaties. In plaats van hotfixes voor individuele kwesties vrij te geven, geeft de Adobe nu een Cumulatief Pak van de Correctie (GVB) elke maand (onderworpen aan het overgaan kwaliteitscontroles) vrij. Een gestreken gemeenschappelijk visserijbeleid is een geaggregeerd inhoudspakket voor veelvoudige moeilijke situaties. GFPs omvat hoofdzakelijk insectenmoeilijke situaties maar zou ook de Pakken van de Eigenschap kunnen omvatten. Ze hebben de volgende voordelen ten opzichte van afzonderlijke hotfix-releases:

* Gecumuleerd van aard (een GVB bevat bijvoorbeeld vastleggingen die via eerdere GVB&#39;s zijn geleverd)
* Meer kwaliteitsborging
* Vereenvoudigde installatie (de gebruiker installeert een gestreken fijn-wit als één enkel pakket dat geen gebiedsdelen, behalve het recentste de dienstpak heeft)

Voor meer informatie over GFP en andere soorten versies, zie {de Definities van het Voertuig van de Versie van het 0} Onderhoud.](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)[

## Over de release {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018 omvat.

AEM Cumulative Fix Pack 6.3.3.8 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.20.

>[!CAUTION]
>
>Het toepassen van GVB zonder verenigbaarheid tussen de geïnstalleerde Packs van de Eigenschap te bevestigen kan in systeemmislukking of verlies van douaneconfiguraties resulteren, die van steun zouden kunnen vereisen om te herstellen.

>[!NOTE]
>
>Voor AEM instanties met een versie lager dan 6.3.3.0, adviseert de Adobe het opstellen van SP/GVB als installatiemap voor klanten die vele gebruikers op AEM instantie hebben.

>[!NOTE]
>
>MongoDB Enterprise 3.6 wordt ondersteund vanaf AEM versie 6.3.3.1.

## Lijst met problemen {#changes}

In deze sectie worden alle problemen en hotfixes vermeld die in het huidige GVB zijn opgenomen.

Bovendien omvat dit GFP hotfixes die in [ vorige cumulatieve fixpakken ](#previous) worden geleverd.

### Assets {#assets}

* Add aan de pagina van de Inzameling toont niet alle beschikbare inzamelingen in de Mening van de Kaart terwijl het toevoegen van activa aan de inzameling (NPR-32537).

### Sites {#sites}

* Wanneer u Parsys en een component binnen het selecteert en de toetsenbordkortere weg gebruikt om geselecteerde punten te schrappen, schrapt de actie zowel de component als zijn ouderParsys (NPR-32071).
* Wanneer de eigenschappen van een pagina worden opgeslagen, wordt een onjuist knooppunt gemaakt (NPR-31774).

### Integrations {#integrations}

* ReportSuitesServlet is kwetsbaar voor SSRF (NPR-32162).

### Campagne gericht {#campaign-targeting}

* De inhoud van een component wordt veranderd in de instantie van de Auteur en dan geactiveerd is niet zichtbaar in de instantie van Publish tot de component **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 en NPR-32232) opnieuw is begonnen.
* Prestaties van de Context Hub crashen bij het publiceren (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe Developer is niet geïntegreerd met Adobe Experience Manager 6.3 voor Brand Portal (NPR-32056).

### Forms {#forms}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

#### Forms-invoegtoepassing {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het absoluut noodzakelijk om het AEM Forms add-on pakket te installeren nadat AEM Service Pack, Cumulative Fix Pack of Feature Pack zijn geïnstalleerd.

* Designer: Als de optie Tags toevoegen is ingeschakeld, verdwijnt de rand van het subformulier in de gegenereerde PDF (NPR-32324 en NPR-32545).
* Designer: als een tabel samengevoegde cellen bevat, mislukt de toegankelijkheidstest voor het PDF-uitvoerbestand dat vanuit een XDP-formulier is geconverteerd met behulp van de uitvoerservice (NPR-32068).
* Documentbeveiliging: een beveiligd PDF-bestand kan niet offline worden geopend als de optie `DisableGlobalOfflineSynchronizationData` is ingesteld op `True` (NPR-32080).

**Vaste Kwesties in 6.3.0-0047**

* (Alleen JEE) Er zijn kritieke beveiligingskwetsbaarheden (CVE-2021-44228 en CVE-2021-45046) gemeld voor Apache `Log4j2`.

## Hotfixes en de Pakken van de Eigenschap inbegrepen in vorige Cumulatieve Pakken van de Moeilijke situatie {#previous}

### Cumulatief Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018 omvat.

AEM Cumulative Fix Pack 6.3.3.7 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

### Assets {#assets-1}

* Assets is geselecteerd (in de kolomweergave in de aanraakinterface) voordat u de filteroptie selecteert in de vervolgkeuzelijst Alleen inhoud en vervolgens de verplaatsingsoptie selecteert, wordt ook verplaatst (NPR-30693).
* De variabele `${extension}` wordt niet gerenderd in auteurinstantie bij werkschemaverwerking (NPR-31694).
* De vervalwaarde (de tijd van het cliëntgeheime voorgeheugen aan levende) die voor de Hybride wijze van Dynamic Media wordt gevormd wordt niet herhaald aan de leveringsmilieu van Dynamic Media (NPR-31114).
* Assets wordt via een Author-instantie naar een Publish-instantie gerepliceerd die op Dynamic Media-Scene7-implementatie wordt uitgevoerd, zelfs na het gebruik van standaardfilters (NPR-30856).

### Sites {#sites-1}

* Pagina-eigenschappen van een primaire pagina kunnen niet worden geladen en er wordt een NullPointerException geretourneerd. Het probleem wordt opgelost bij het toevoegen van het `cq:blueprin` t bezit (NPR-30901).
* De configuraties van de rollout worden niet behoorlijk teruggewonnen van blueprintConfig op de wortelknoop. De deactivering wordt geactiveerd voor zowel blauwdrukken als live kopieën. Alleen deactivering voor de blauwdruk activeren (NPR-30866).
* Wanneer een gebruiker een pagina uitrolt, toont het de configuratievenster van de roll-out dubbele Levende wegen van het Exemplaar (NPR-30438).
* De basislijneditor (RTE) is uit het vak. past inline font-size toe op elementen, onverwacht (NPR-31283, NPR-30922).
* Kan de campagne in Adobe Campaign die de buiten de doos geplaatste ontwerpimportercomponent (NPR-30890) bevat, niet synchroniseren.
* In de Rich Text Editor (RTE) kunt u een ingesloten tabel niet invoegen als lijstitem (NPR-30878).
* Een gebruiker concentreert zich op de linkerspoorgebieden en gebruikt een toetsenbordkortere weg om inhoud te kleven. Hierbij wordt de inhoud van het klembord van de pagina-editor geplakt in plaats van de inhoud die is gekopieerd van de linkerspoorvelden (NPR-31173).
* Wanneer een gebruiker een inhoudsfragment bewerkt, wordt de reeds verwijderde variant van het inhoudsfragment hersteld (NPR-31272).
* AEM Site maakt geen taalkopie (NPR-30690).
* De acties van de pagina-editor bevatten niet de besturingselementen voor het live kopiëren (NPR-30613).

### Gemeenschappen {#communities}

* De titels van activiteiten en meldingen zijn inconsistent (NPR-30940).
* De analyserapporten worden niet ingevuld in de AEM-auteuromgeving. In plaats daarvan wordt een lege pagina weergegeven (NPR-30905).
* Paginering werkt niet correct in Gemeenschapsblogs (NPR-30827).

### Stichting {#foundation}

* Updates in de configuratie van de buffergrootte voor de op Jetty-Gebaseerde dienst van HTTP worden niet bewaard (NPR-30925).

### Forms {#forms-1}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het absoluut noodzakelijk om het AEM Forms add-on pakket te installeren nadat AEM Service Pack, Cumulative Fix Pack of Feature Pack zijn geïnstalleerd.

#### Adaptieve Forms {#adaptive-forms}

* Zwevende waarden die zijn berekend met een script, worden niet correct weergegeven in een vorm die deel uitmaakt van een formset (NPR-30802).

#### HTML5 Forms {#html-forms}

* Als u een HTML5-voorbeeld van een XDP-formulier genereert, wordt een flikkering weergegeven terwijl exemplaren van een subformulier worden toegevoegd (NPR-30908).

### Forms JEE-installatieprogramma {#forms-jee-installer}

#### Acrobat Services {#document-services}

* OutputService geeft een onjuiste reactie weer nadat een patch is toegepast om HTML op PDF-problemen te verhelpen (NPR-31504).

#### PDFG-service {#pdfg-service}

* Het maximale aantal hergebruik met JMX-console wordt niet weergegeven voor HTML2PDF-service (NPR-30305).

#### Foundation JEE {#foundation-jee}

* Maximale aantal hergebruik met JMX-console wordt niet weergegeven voor HTML2PDF-service (NPR-30136).

### Cumulatief Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018 omvat.

AEM Cumulative Fix Pack 6.3.3.6 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

### Assets {#assets-2}

* De videosamenvoeging door Dynamic Video keert slechts de hoogste 100 punten in de resultaatreeks terug. NPR-30441; hotfix voor CQ-4213561
* Verbindingsprobleem met slimme tags Adobe via gegevensstroom. NPR-30026: Hotfix voor CQ-4269457
* Het uitpakken van een archief met een map met een procentteken (%) in de naam kan niet worden geopend via de Assets-interface. NPR-29989: Hotfix voor CQ-4270467
* De verwerking van subassets van grote PDF dossiers veroorzaakt een uitzondering OutOfMemoryError (OOME). NPR-29851: Hotfix voor CQ-4269574

### Sites {#sites-2}

* ContextHub-fout tijdens AEM- en Campagneintegratie. NPR-30624: Hotfix voor CQ-4250790
* De metagegevenseigenschappen &#39;onTime&#39; of &#39;offTime&#39; die zijn opgeslagen op elementen, worden niet teruggeroepen als de AEM server opnieuw wordt gestart. NPR-30412: Hotfix voor CQ-4272784
* Terwijl het produceren van een uitvoer CSV, die douanekolommen voor de Mening van de Lijst toevoegt breken het rapport. NPR-30208: Hotfix voor CQ-4273344
* OOTB-rapporten in /etc/reports/ werken niet correct en de historische gegevensgrafiek wordt niet weergegeven. NPR-30016: Hotfix voor CQ-420180
* De waarde van de request-parameter resourceType wordt gekopieerd naar de waarde van een HTML-tagkenmerk dat is ingekapseld in dubbele aanhalingstekens. NPR-29832: Hotfix voor CQ-4255365

### Gemeenschappen {#communities-1}

* Dubbele inhoudskwestie met de AEM Communities moderatieconsole. NPR-30667: Hotfix voor CQ-4276829

### Vertaling {#translation}

* Probleem met vertaling - Slechts een paar componenten worden omgezet met behulp van Machine Translation. NPR-30079: Hotfix voor CQ-4273764
* Als u het vertaalframework gebruikt, treedt er een fout op wanneer u pagina&#39;s toevoegt aan meerdere vertaaltaken. NPR-29746: Hotfix voor CQ-4270953

### Forms {#forms-2}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het absoluut noodzakelijk om het AEM Forms add-on pakket te installeren nadat AEM Service Pack, Cumulative Fix Pack of Feature Pack zijn geïnstalleerd.

#### HTML5 Forms {#html-forms-1}

* Als u in de modus Bladeren een HTML5-formulier leest met toegang tot niet-visuele desktops, leest de Chrome-browser &quot;grafisch&quot; vóór elke schaalbare vectorafbeelding (SVG) in het formulierontwerp. NPR-30451: Hotfix voor CQ-4274732

#### Forms - Ondersteunende integratie {#forms-backend-integration}

* Kan de service/gegevensbron voor de databaseverbinding niet zien tijdens het maken van het FDM (Form Data Model). NPR-30108: Hotfix voor CQ-4273359

### Forms JEE-installatieprogramma {#forms-jee-installer-1}

#### Forms - Acrobat Services {#forms-document-services}

* Wanneer een ladingstest op de dienst van HTML aan PDF wordt uitgevoerd, ontbreekt het met een fout en de montages van het dossiertype worden verwijderd uit de Server van AEM Forms. NPR-3011, NPR-30086: Hotfix voor CQ-4271495

### Cumulatief Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.5 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.17.

### Assets {#assets-3}

* Bijgewerkte interface DAM DMGateway voor S3 multipart steun. NPR-29740: Hotfix voor Q-4226303
* Kan een afbeeldingsuitvoering op een video-element niet verwijderen van de pagina met elementdetails. NPR-29417: Hotfix voor CQ-4268675
* De eigenaar kan geen persoonlijke map in een privémap maken. NPR-29397: Hotfix voor CQ-4229830
* Als u een Adobe Illustrator-illustratiebestand van meer dan 2 GB uploadt, wordt een Java™-heapruimtefout gegenereerd. NPR-29265: Hotfix voor CQ-4226217
* Assets wordt onbruikbaar nadat de DAM CQ Mime Type Service tekst voor m3u8 toepast. NPR-29259: Hotfix voor CQ-4264052
* De optie Maken werkt niet bij het maken van verzamelingen in Edge. NPR-29248: Hotfix voor CQ-4265699 en CQ-4265438
* Bij Delen van koppelingen naar middelen worden voor bepaalde middelen in de map lege grijze kaarten weergegeven. NPR-29831: Hotfix voor CQ-4270187
* De nieuwe tags die aan elementen zijn toegevoegd, kunnen niet worden opgeslagen en verdwijnen uit de eigenschappen. Hotfix voor CQ-4271931, CQ-4270476

### Sites {#sites-3}

* CoralUI, wanneer gebruikt met Multifield, slaat fileReferenceParameter op het componentenniveau in plaats van het multifield niveau op. NPR-29535: Hotfix voor CQ-4266129
* Probleem tijdens het vergelijken van de nieuwste en huidige paginaversie op AEM 6.3.3.3. NPR-29532: Hotfix voor CQ-4269639
* Het padveld wordt geopend op het hoofdpad, ongeacht het pad dat u wilt zoeken. NPR-29398: Hotfix voor CQ-4268897
* (Experience Fragments) FacebookApplication#setUpApp gebruikt een verouderde API, die niet meer werkt. NPR-29213: Hotfix voor CQ-4266630
* Er wordt een foutmelding gegenereerd wanneer componenten aan de WCM-pagina worden toegevoegd wanneer minificatie op de instantie is ingeschakeld. NPR-29476: Hotfix voor CQ-4266197
* Lege eigenschappen en meerdere eigenschappen worden tijdens de rollout niet vanuit de blauwdruk doorgegeven. Actieve kopie herstellen met blauwdruk werkt niet voor componenten. NPR-29252: Hotfix voor CQ-4264928, CQ-4264926, CQ-4267722
* Het minimaliseren van Rich Text Editor van volledig scherm in de bronbewerkingsmodus leidt tot verlies van inhoud. NPR-28838: Hotfix voor CQ-4260584

### Gemeenschappen {#communities-2}

* Bezoekers en leden zonder moderatorrechten kunnen niet-goedgekeurde en hangende berichten zien door de URL te plakken. NPR-29726: Hotfix voor CQ-4271124
* Hoge responstijd tot 40-50 seconden wordt waargenomen bij het aanmelden bij de gebruiker voor de Gemeenschap. NPR-29679: Hotfix voor CQ-4269444
* Kan het wachtwoord niet opnieuw instellen wanneer u bent aangemeld met een andere gebruikersnaam en e-mail omdat de sleutel wordt gegenereerd met een verwisselde gebruikersnaam en e-mail. NPR-29281: Hotfix voor CQ-4268694

### Ervaar fragmenten {#experience-fragments}

* U kunt Experience Fragments niet naar doel exporteren wanneer een slimme afbeelding wordt gebruikt. Hotfix voor CQ-4269606

### Replicatie {#replication}

* De component van de Agent van de Replicatie is vatbaar voor een kwetsbaarheid die gevoelige informatie aan onbevoegde gebruikers openbaart. NPR-29613: Hotfix voor graniet-25070
* Gebruiker-verstrekte gegevens zijn niet ontsnapt aan output in de `cq/replication/components/agent` component, resulterend in een opgeslagen cross-site scripting (XSS) kwetsbaarheid. NPR-29452: Hotfix voor CQ-4266263

### Forms {#forms-3}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-3}

* Geen nieuwe oplossingen in het AEM Forms-invoegtoepassingspakket.

### Forms JEE-installatieprogramma {#forms-jee-installer-2}

* Geen nieuwe oplossingen in AEM Forms JEE-installatieprogramma.

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.5

[Bestand ophalen](assets/do-not-localize/6_5-bundle-list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.5

[Bestand ophalen](assets/do-not-localize/content_packages6335.txt)

### Cumulatief Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.4 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.16.
* Time-out voor socket toegevoegd en time-out voor verbinding in Brand Portal-replicatieagents.

### Assets {#assets-4}

* Als u een archief met dezelfde naam opnieuw uploadt, worden er geen uitvoeringen gegenereerd voor de nieuwe verwerkte elementen. NPR-28643: Hotfix voor CQ-4262286
* Workflow CommandLineProcess mislukt met een bestandsnaam met één aanhalingsteken. NPR-28805: Hotfix voor CQ-4262287
* De waarden verschillen tussen de verzamelingspagina en de verzamelingspagina wanneer u het filter gebruikt. NPR-28642: Hotfix voor CQ-4261405
* CommitFailedException triggers with upload of large zip archive assets. NPR-28528: Hotfix voor CQ-4260903
* Metagegevens van mappen kunnen niet worden opgeslagen wanneer een map met speciale tekens wordt bewerkt. NPR-28211: Hotfix voor CQ-4260401
* Kan afbeeldingsuitvoeringen van een video-element niet verwijderen van de pagina met elementdetails. NPR-29149: Hotfix voor CQ-4266073
* DMS7 desktop video delivery using DMComponent gebruikt progressieve download voor het afspelen van video in publish mode en streamt niet. NPR-28754: Hotfix voor CQ-4263732
* Kan voorinstellingen voor afbeeldingen niet maken/bewerken omdat de toegang tot /etc/dam/video/dynamicmedia wordt beperkt, schakelt functies voor afbeeldingsmanagers uit. NPR-28662: Hotfix voor CQ-4263022
* Als u Delen koppelt aan videobestanden die zijn gecodeerd met DMS7, ontstaan lege mappen. NPR-28851: Hotfix voor CQ-4206743
* De replicatie van AEM naar Brand Portal blijft lang vastzitten. NPR-28913: Hotfix voor CQ-4254932

### Gemeenschappen {#communities-3}

* Kan berichten met bijlagen niet openen in de map Outlook en inbox. NPR-28559: Hotfix voor CQ-4217072

### Sites {#sites-4}

* XSS (Cross-site scripting) in SuggestieHandler voor 6.3. NPR-28692: Hotfix voor CQ-4253821
* Diepe rollout eindigt zonder alle vertakkingen in respectieve LiveCopy te bevatten. NPR-29175: Hotfix voor CQ-4239472
* (MSM) Implementeer LiveCopyIndex met behulp van een eikenindex. NPR-29198: Hotfix voor CQ-422472
* Het bestand `coral.js` bevat een kwetsbare versie van de bibliotheek `handlebars.js` . NPR-26973: Hotfix voor CQ-4255377
* Als een doelcomponent wordt gebruikt met een geneste component Layout Container en Text, wordt een JavaScript-fout gegenereerd: &#39;Kan eigenschap currentPos van null niet lezen&#39; wanneer tekst wordt bewerkt of op de container wordt geklikt. NPR-29077: Hotfix voor CQ-4246594
* (Touch UI) Kan geen updatetags bulken op pagina&#39;s die al met verschillende tags zijn gecodeerd. NPR-28729: Hotfix voor CQ-4262922
* Als u de variatie in de kaartweergave opent, treedt er een fout van 500 op. NPR-28611: Hotfix voor CQ-4263571
* Uitrol van een structuur die in een primaire map is verplaatst, leidt tot een onjuiste `cq:moveTarget` . NPR-28968: Hotfix voor CQ-4265280

### Integratie {#integration}

* (Configuraties van de Cloud Service) checkbox &quot;geërft van&quot;die op het wortelniveau verschijnt zou moeten worden verwijderd. NPR-28771: Hotfix voor CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler gaat in een oneindige lijn en veroorzaakt updates aan knopen op publicatieinstanties. NPR-28561: Hotfix voor CQ-4263096
* Het gebruik van BrightStor Edge-referentie is mislukt vanwege een verbindingsfout. NPR-29167: Hotfix voor CQ-4265872
* Compilatieprobleem in OfferproxyTandtProvider.java vanwege ontbrekende importinstructie voor de klasse &#39;Resource&#39;: ontbrekende importinstructie: import org.apache.sling.api.resource.Resource. NPR-2872

### Commerce {#commerce}

* De sorteeroptie werkt niet voor elementen in de Commerce-verzameling. NPR-28755: Hotfix voor CQ-4213622

### Jetty {#jetty}

* Jetty uitzonderingen in error.log voor elke 302 omleidingen na het installeren van GVB2 bovenop 6.3.3. NPR-28606: Backport voor CQ-4262844

### UI - Foundation {#ui-foundation}

* Als u op een tag klikt, wordt de algemene mouseUp-gebeurtenis verwijderd en wordt het dialoogvenster vastgezet in de sleepbare modus. NPR-28641: Hotfix voor CUI-7294

### WCM - MSM {#wcm-msm}

* De uitrol van PushOnModify voor PageManager beweegt veelvoudige tijden van twee zittingen die een ras-voorwaarde veroorzaken. NPR-28880: Hotfix voor CQ-4266191

### Kwetsbaarheid {#vulnerability}

* Het CSRF-beschermingskader werkt niet met AEM stichtingsvormen. NPR-28612: Hotfix voor GRANITE-22231

### Forms {#forms-4}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

De belangrijkste markeringen voor AEM Forms zijn:

* Schakel de optie in om items per pagina te selecteren op de weergavepagina van de beleidsset.
* Functionaliteit voor gedeelde wachtrij voor alle browsers toegevoegd.

### Forms-invoegtoepassing {#forms-add-on-package-4}

#### Forms - Workflow {#forms-workflow}

* Een gedeelde de antwoordtaak van de rij opent een flitselement in de HTML5 werkruimte. NPR-29161: Hotfix voor CQ-4266498
* Kan niet verzenden vanuit Workspace als de knop een umlaut-teken bevat. NPR-29014: Hotfix voor CQ-4263172

#### Forms - Documentbeveiliging {#forms-document-security}

* Schakel de optie in om items per pagina te selecteren op de weergavepagina van de beleidsset. NPR-29243: Hotfix voor CQ-4268567 &amp; CQ-4265132

#### Forms - Acrobat Services {#forms-document-services-1}

* OSGi Forms Assembler werkt niet aan Acrobat-bestanden. NPR-29049: Hotfix voor CQ-4254426

#### HTML5 Forms {#html-forms-2}

* Er is een ander gedrag bij het voorvertonen van een XDP als PDF en niet hetzelfde XDP als HTML in Designer. NPR-28602: Hotfix voor CQ-4260239

### Forms JEE-installatieprogramma {#forms-jee-installer-3}

* Geen nieuwe oplossingen in AEM Forms JEE-installatieprogramma.

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.4

[Bestand ophalen](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.4

[Bestand ophalen](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulatief Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.3 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.16.
* Paginering van de lijst met beleidssets verandert om 50 records per pagina te beperken.
* Toegevoegde rep: cache plaatsen in onherstelbare knooppunten bij AEM Communities User Sync Listener bij publicatie-instanties.
* aria-label toegevoegd voor de knop Lijst en Kaartweergave.
* Er is een escape-teken opgenomen voor de komma wanneer een zoekopdracht wordt uitgevoerd.
* Toegelaten steun van synthetische middelen voor inhoudsbeleid.

#### Assets {#assets-5}

* Kan geen meerdere bestanden van het type `.jp2` , `.max` , `.oft` , `.msg` downloaden. NPR-28002: Hotfix voor CQ-4210856
* De publicatie-instellingen van ImageServer worden niet gerepliceerd naar hybride levering. NPR-28329: Hotfix voor CQ-4253030

#### Gemeenschappen {#communities-4}

* Toetsenbordnavigatie ingeschakeld voor AEM Communities Enablement-componenten op Publish. NPR-27739: Hotfix voor CQ-4253856
* Toegelaten toetsenbordnavigatie om het spelen van inhoud te teweegbrengen. NPR-27738: Hotfix voor CQ-4254026
* aria-label toegevoegd voor de knop Lijst en Kaartweergave. NPR-27736: Hotfix voor CQ-4254027
* (Backport) Added rep: cache in Ignorable Nodes bij AEM Communities User Sync Listener op publish instances. NPR-27841: Hotfix voor CQ-4247234
* De speciale tekens worden voorafgegaan door escape-teken (\) in het zoekvak. NPR-27839: Hotfix voor CQ-4259757
* Fout tijdens het zoeken naar tekens zoals `(` , `+` en `?` bij snel zoeken. NPR-28212: Hotfix voor CQ-4260969
* Kan opmerkingen in door de gebruiker gegenereerde inhoud niet verwijderen met behulp van API. NPR-28075: Hotfix voor CQ-4260534
* Opmerkingen die op de volgende pagina zijn geplaatst, worden geel gemarkeerd wanneer een nieuwe opmerking wordt geplaatst. NPR-28148: Hotfix voor CQ-4259681
* Kan geen berichten openen die bijlagen bevatten in verzonden vooruitzichten en inbox map. NPR-28559: Hotfix voor CQ-4217072

#### Sites {#sites-5}

* Het runnen van de Leegheid van de Versie in AEM 6.3 veroorzaakt een constant herhaalde waarschuwing in de logboeken. NPR-27750; hotfix voor CQ-4206870
* De stijlplug-in wordt niet ondersteund in de modus Volledig scherm van de RTF-editor. NPR-27622: Hotfix voor CQ-4258674
* Lijst `loaderPromises` wordt niet gewist nadat het inhoudsframe is geladen in editor.js NPR-27768: Hotfix voor CQ-4205337
* Onbekwaam om een malplaatjebeleid op genestelde Parsys te plaatsen zonder het op de oudercomponent te plaatsen. NPR-27987: Hotfix voor CQ-4246095
* De componentbrowser is geen bezig met het manipuleren van gebruikersinvoer en kan dus JavaScript-fouten genereren. NPR-27986: Hotfix voor CQ-4247590
* De pagina wordt leeg weergegeven wanneer de gebruiker het inhoudsfragment probeert te bewerken. NPR-2769
* De annotatiemarkering verdwijnt wanneer de gebruiker op de annotatie klikt. BPR-27196: Hotfix voor CQ-4254423

#### Integratie {#integration-1}

* ResourceResolver lost geen veelvoudige domeinen voor de component van het Doel op. NPR-28265: Hotfix voor CQ-107847
* LiveCopy-overervingsannulering werkt nu goed op doelcontainers wanneer acties worden weergegeven. NPR-28129: Hotfix voor CQ-4259813

#### Replicatie {#replication-1}

* DispatcherFlushRules broken replicatie in 6.3.3.1 NPR-28150: Hotfix voor CQ-4261401

#### Campagne - gericht {#campaign-targeting-1}

* NullPointerException in TargetContentManager. Hotfix voor CQ-4263485

#### Sociaal - SCORM {#social-scorm}

* Verwijzing naar SCORM-cloud (Shareable Content Object Reference Model) in de speler verwijderen. Hotfix voor CQ-4260779

#### DAM - Algemeen {#dam-general}

* Download via link share email retourneert leeg/corrupt zip. Hotfix voor CQ-4259686

#### `MAC` - Integratie testen en doel {#mac-test-target-integration}

* Het vormen van de de componentenoptie van het Doel is niet beschikbaar voor het publiek behalve Standaard publiek. Hotfix voor CQ-4261370

#### Vertaling {#translation-1}

* Ondersteuning voor MS® Translator-service inschakelen in AEM 6.3 na upgrade van MS® Translator naar API v3.0. NPR-28365: Hotfix voor CQ-4259096

### Forms {#forms-5}

### Forms-invoegtoepassing {#forms-add-on-package-5}

#### Forms - Workflow {#forms-workflow-1}

* Kan geen PDF forms renderen in de HTML5-werkruimte. NPR-28059: Hotfix voor CQ-4260373

#### Forms - Acrobat Services {#forms-document-services-2}

* Kan geen beleidssets zien die verder gaan dan de eerste 1000 die worden vermeld in de weergave Beleidssets in de Admin Console. NPR-28060, NPR-26047: Hotfix voor CQ-4249865
* Er wordt een uitzondering met de naam `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` gegenereerd, zodat het kortstondige proces niet kan worden voltooid. NPR-28652

#### Forms - Adaptieve Forms {#forms-adaptive-forms}

* Items in de vervolgkeuzelijst toevoegen of verwijderen wordt niet bijgewerkt wanneer de selectievakjes worden ingeschakeld. NPR-28224: Hotfix voor CQ-4252834

### Forms - JEE Installer {#forms-jee-installer-4}

* Geen nieuwe oplossingen in AEM Forms JEE-installatieprogramma.

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.3

[Bestand ophalen](assets/do-not-localize/6333_bundle_list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.3

[Bestand ophalen](assets/do-not-localize/content_package_list_6333.txt)

### Cumulatief Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.2 hangt van AEM 6.3 Service Pack 3 af. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie versienota&#39;s voor AEM 6.3 Service Pack 3.

De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.15.
* Toegevoegde steun voor het Lusje van Regels en zijn handhaving in de activaomslag aan het Schema van Meta-gegevens van de Omslag.
* Pagineringsondersteuning ingeschakeld om de pagina met lijsten te groeperen bij publicatie.
* Toegelaten bericht unreadCount dat met om het even welk aantal moet worden gevormd. De standaardwaarde is 20.
* Oplossingen in externe koppelingencontrole.

#### Assets {#assets-6}

* Cascading drop-down wordt niet gesteund op dynamische drop-down lijsten. NPR-27044; hotfix voor CQ-4252564
* Verbeterde de vraag zodat het de eigenschap ExiryNotification gebruikt. NPR-26999: Hotfix voor CQ-4251188
* Hiermee wordt migratie van Metagegevensschema naar Metagegevensschema van map geregeld. NPR-27771: Backport voor CQ-4257737, CQ-4257735, CQ-4259822
* De aanpassing van de verwijzing van activa ontbreekt om verwijzingen voor activa bij te werken die deel van Sling ResourceCollections uitmaken. NPR-26759: Hotfix voor CQ-4252605
* Als u via een koppeling wilt downloaden, wordt een leeg of beschadigd ZIP-bestand geretourneerd. NPR-27997: Hotfix voor CQ-4259686
* De hybride videocodering is niet voltooid en er wordt geen miniatuur gemaakt. NPR-27122: Hotfix voor CQ-4255080

#### Sites {#sites-6}

* Als de bovenliggende pagina wordt onderbroken, wordt het mixintype cq:LiveRelationship van de ontbrekende pagina verwijderd. NPR-26996: Hotfix voor CQ-4254113
* (Externe koppelingencontrole) Interne koppelingen worden op afzonderlijke pagina&#39;s als verbroken weergegeven, maar hetzelfde werkt niet voor externe koppelingen. NPR-27481: Hotfix voor CQ-4257780
* De overerving Cloud Service Config wordt onderbroken tijdens het bewerken van andere pagina-eigenschappen. NPR-27311: Hotfix voor CQ-4256785
* Null wijzeruitzondering wanneer het gebruiken van een vorm van de Componenten van de Kern samen met een Vorm van de Stichting. NPR-2733: Hotfix voor CQ-4249176
* De rijke Redacteur van de Tekst verwijdert de lege alt markering. NPR-26938: Hotfix voor CQ-4253267
* (Klassieke UI) De kwesties van prestaties met selectie, veranderde luisteraar als er veelvoudige drop-down waren. NPR-27115: Hotfix voor CQ-4237215
* Wanneer de Rich Text Editor wordt gecombineerd met meerdere velden, treedt de Uncaught TypeError: fieldAPI.getName geen functie op bij foundation.js-fout. NPR-27146: Hotfix voor CQ-4253155, CQ-4259967
* Focus/cursor blijft in de Rich Text Editor staan, zelfs wanneer u op een keuzerondje in de Safari-browser klikt. NPR-27144: Hotfix voor CQ-4249635
* De pagina wordt als leeg weergegeven wanneer de gebruiker het inhoudsfragment probeert te bewerken. NPR-2769
* Kan geen versie maken voor Experience Fragments. NPR-27689: Hotfix voor CQ-4259009

#### Integratie {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever loopt de volledige boom om de beschikbare merken te verzamelen. NPR-27060: Hotfix voor CQ-4255790
* `cq:actions` wordt niet overwogen voor een doelcomponent. NPR-27616: Hotfix voor CQ-4257497

#### Sling {#sling}

* Wanneer data-smart-use met klassen met een identieke naam wordt gebruikt, wordt de niet-compatibele code geproduceerd. NPR-27282: Hotfix voor Sling-7581

#### Commerce {#commerce-1}

* Update naar Apache Felix HTTP Jetty 4.0.6. NPR-26472: Hotfix voor graniet-22916

#### DAM - DM-client {#dam-dm-client}

* Een afbeelding wordt niet weergegeven na het opgeven van onderbrekingspunten in een Dynamic Media-component. Hotfix voor CQ-4256168

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet met verwante video wordt niet correct gesynchroniseerd. Hotfix voor CQ-4251650
* Video wordt niet afgespeeld in de Viewer Preset-editor voor gemengde mediaset. Hotfix voor CQ-4251442

#### DAM - Algemeen {#dam-general-1}

* De koppeling naar het model van het inhoudsfragment ontbreekt na het toepassen van de SP3-patch. Hotfix voor CQ-4259029

#### DAM - UI {#dam-ui}

* De gebruikersinterface van het schema voor metagegevens van mappen wordt verbroken nadat SP3 is geïnstalleerd. Hotfix voor CQ-4257737

#### Gemeenschappen {#communities-5}

* Voeg pagineringsondersteuning toe voor groepsaanbiedingen bij publicatie. NPR-26953: Hotfix voor CQ-4246525
* Ongelezen tellingsmelding kan niet na 21 worden geplaatst. NPR-27496: Hotfix voor CQ-4252829
* De limiet voor gebruikersabonnementen is beperkt tot 1000. NPR-27615: Hotfix voor CQ-4254689
* Er is een fout opgetreden tijdens het uploaden van een bijlage buiten de afbeelding (bijvoorbeeld .pdf) in het forum. NPR-27375: Hotfix voor CQ-4257753
* De koppeling voor antwoorden werkt niet bij een rijklik. NPR-24556: Hotfix voor CQ-4256138
* Relaties met UGC worden niet verwijderd als UGC wordt verwijderd. NPR-27631: Hotfix voor CQ-4258706
* Onbekwaam om door adreswaarde in het onderzoek van het Sleutelwoord te zoeken als de gemeenschap met de Leverancier van het Middel van de Opslag van het Gegevensbestand (DSRP) wordt geplaatst. NPR-27652: Hotfix voor CQ-4253261
* Als u op het prullenbakpictogram op de afbeelding klikt nadat u de bevestiging hebt verwijderd, wordt de bijlage permanent verwijderd. NPR-27340: Hotfix voor CQ-4255150
* Boven op de tweede pagina worden forumberichten en reacties toegevoegd en als het bericht wordt vernieuwd, wordt het naar de juiste locatie vóór de eerste pagina geplaatst. NPR-27341: Hotfix voor CQ-4247338
* Label voor de voltooiingsstatus van het scorebord wordt ingeschakeld. Dit label is leeg in de gebruikersinterface. NPR-27152: Hotfix voor CQ-4249994
* Bij het toelaten van **staat bevoorrechte** toe, zouden de bevoorrechte leden slechts voor gebruikers moeten kunnen samenstellen die communityleden zijn. NPR-27901: Hotfix voor CQ-4251235

#### Sustenance {#sustenance}

* Logboeken van de de activiteit van de Manager van het pakket zouden in een afzonderlijk logboekdossier moeten worden gehaald. NPR-27323: Hotfix voor graniet-14866

#### Vertaling {#translation-2}

* De voorvertoning van de vertaling werkt niet met de voorbeeldinhoud &#39;we.Retail&#39;. NPR-27170: Hotfix voor CQ-4241179

* Proactief platform.login lost op. NPR-26961
* Opslaan en sluiten op pagina-eigenschappen gaat niet terug naar de juiste pagina in AEM WAR met Tomcat. NPR-27567: Hotfix voor graniet-23671

* De ingevoerde tekst gaat na het opslaan verloren via de functie sourceEdit. Hotfix voor CQ-4259273

### Forms {#forms-6}

### Forms-invoegtoepassing {#forms-add-on-package-6}

#### Forms - Documentbeveiliging {#forms-document-security-1}

* Gelijktijdig probleem met JEE Client SDK. NPR-27572: Hotfix voor CQ-4247156

#### Forms - Acrobat Services {#forms-document-services-3}

* Het maken van een formuliergegevensmodel op basis van SOAP mislukt op WebSphere®. NPR-27692: Hotfix voor CQ-4253702

#### Forms - Adaptieve formulieren {#forms-adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27863: Hotfix voor CQ-4257315
* De AEM Forms Container-component wordt onzichtbaar wanneer het verkeerde formulier op de AEM Sites-pagina wordt geconfigureerd en het selectievakje &#39;Formulieren dekken de volledige breedte van de pagina&#39; is ingeschakeld. NPR-25972: Hotfix voor CQ-4239287, CQ-4249133

### Forms JEE-installatieprogramma {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* Het maken van een formuliergegevensmodel op basis van SOAP mislukt op WebSphere®. NPR-27692: Hotfix voor CQ-4253702

#### SDAB-pakketten en inhoudspakketten inbegrepen {#osgi-bundles-and-content-packages-included}

Lijst van OSGi-bundels opgenomen in AEM 6.3.3.2

[Bestand ophalen](assets/do-not-localize/63332bundle_list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.3.2

[Bestand ophalen](assets/do-not-localize/6332content_package.txt)

### Cumulatief Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 is een belangrijke update die verscheidene interne en klantenmoeilijke situaties omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 3 (6.3.3.0) in september 2018.

AEM Cumulative Fix Pack 6.3.3.1 is afhankelijk van AEM 6.3 Service Pack 3. Daarom moet u het pakket AEM Cumulative Fix Pack 6.3.3.x installeren nadat u AEM 6.3 Service Pack 3 hebt geïnstalleerd. Voor installatieinstructies, zie de versienota&#39;s in [ AEM 6.3 Service Pack 3 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.14.
* Prestatieverbeteringen in voorspellen en zoeken.
* Correctie van het probleem bij de verwerking van FormData voor de standaardwaarde.
* De Form Builder is bijgewerkt naar de nieuwste versie Handlebars.
* Toegevoegd config servlet voor uitgeeft config voor RTE op de wijze van de dialoogdoos.
* Toegevoegde ondersteuning voor samengestelde velden.
* Ingeschakelde/uitgeschakelde werkbalkitems van de Rich Text Editor met een inhoudsbeleid voor het dialoogvenster Bewerken.

#### Assets {#assets-7}

* Als IDS-ontkoppeling is ingeschakeld, worden verwijzingen niet meer gekoppeld in de workflow voor DAM-updatemiddelen. NPR-26135: Hotfix voor CQ-4250933
* Het uitpakken van een archief dat is gemaakt met de unarchiver-stap met een map met de naam a %, wordt niet geopend. NPR-26275: Hotfix voor CQ-4251482
* Eén aanhalingsteken voorkomt dat de metagegevens worden bijgewerkt. NPR-26808: Hotfix voor CQ-4254305
* (Openbaar Onderzoek) De problemen van prestaties wanneer het zoeken binnen een inzameling. NPR-26714: Hotfix voor CQ-4253408
* Het gebruik van GQLConverter met een full-text zoekopdracht met de letters OR in de tekst wordt onjuist verwerkt. NPR-26564: Hotfix voor CQ-4247362
* Door de elementkoppeling van meerdere huurders te delen, wordt de id van de huurder vooraf bijgewerkt en wordt een ongeldige URL gevormd. NPR-26482: Hotfix voor CQ-4253540
* Schakel &quot;Bedrijfsmappad&quot; uit in de gebruikersinterface voor configuratie van Dynamic Media Cloud. NPR-26361: Hotfix voor CQ-4249505
* De inname van .mos RAW-bestanden is verlengd. NPR-26296: Hotfix voor CQ-4250661
* Bij het delen van een elementkoppeling is het niet mogelijk meer dan één interne gebruiker met een numerieke gebruikers-id toe te voegen. NPR-26206: Hotfix voor CQ-4251466
* Corruptie in ZIP-bestanden die zijn gecomprimeerd met het algoritme deflate64. NPR-26793: Hotfix voor CQ-4253995
* Het genereren van miniaturen werkt niet correct voor complexe PDF-bestanden, waardoor miniaturen ontstaan waarin een deel van de afbeelding ontbreekt. NPR-26057: Hotfix voor CQ-4250944
* Probleem met het gebruik van heapgeheugen bij het genereren van miniaturen. NPR-25545: Hotfix voor CQ-4246960
* Als u veel relaties met een element maakt, treedt er een fout op. NPR-26309: Hotfix voor CQ-4250708
* De **optie van de Vertoning van de Schrapping** werkt niet en werpt een fout &quot;niets om te schrappen.&quot; NPR-26007: Hotfix voor CQ-4213414
* Kan standaardwaarden voor velden met meerdere waarden niet verwijderen. NPR-25116: Hotfix voor CQ-4247856
* (DM Hybrid) De replicatieonderbrekingen van de Catalogus voor AEM 6.3.2 met Dynamic Media. NPR-26406: Hotfix voor CQ-4251306

#### Sites {#sites-7}

* De pro-actieve Steun van Plaatsen lost op. NPR-26963
* Tags worden twee keer gemaakt wanneer er een verschil is in het hoofdlettertype Titel en Naam. NPR-26877: Hotfix voor CQ-4254134
* Het beleid bepaalt niet de eigenschappen van de Redacteur van de Tekst Rich in uitgeeft dialoogdoos. NPR-27059, NPR-26750: Hotfix voor CQ-4241130
* Clientcontextsegment.js in cache plaatsen tegenover vragen die niet in cache zijn geplaatst. NPR-26622: Hotfix voor CQ-4253486
* Activiteiten van segmentregel (/etc/segmentation) voor kinderregels in klassieke oorzaken die publicatie doet afnemen. NPR-26601: Hotfix voor CQ-4253588
* Als u &#39;Speciaal teken&#39; toevoegt, wordt het dialoogvenster Rich Text Editor naar de bovenkant verschoven. NPR-26435: Hotfix voor CQ-4249869
* (Aanraakinterface) De werkbalk wordt onbruikbaar met meerdere Rich Text Editor tijdens het schakelen van Volledig scherm naar zwevend dialoogvenster. NPR-25652: Hotfix voor CQ-4206008
* Als u de opstart van meerdere pagina&#39;s bevordert, worden er meerdere versies voor elke pagina gemaakt. NPR-26810: Hotfix voor CQ-4254663
* Tagvelden van het model van structuurcontentfragment geven geen verplaatsingen van tags aan. NPR-26801: Hotfix voor CQ-4251805
* (Aanraakinterface) Het ongedaan maken van de publicatie van de onderliggende pagina in de pagina-editor werkt niet nadat de naam van de pagina in de blauwdruk is gewijzigd. NPR-26774: Hotfix voor CQ-4254175
* Niet-gepubliceerde pagina werkt niet met verwijzingen. NPR-26749: Hotfix voor CQ-4254372
* Wanneer u een variatie als Live Copy maakt, moet de gebruiker de pagina vernieuwen om deze weer te geven. NPR-26663: Hotfix voor CQ-4254328
* (Klassieke gebruikersinterface) Als u teruggaat naar de pagina-eigenschappen, gebruikt de miniatuurafbeelding niet langer overerving en verdwijnt deze van sitebeheerder en -assistent. De afbeelding wordt dan leeg weergegeven. NPR-26562: Hotfix voor CQ-4252346
* Wanneer een versie van een pagina wordt gecreeerd en een vergelijking wordt teweeggebracht, zijn de knopen van /content/versionshistory vermeld in de lijst van levende exemplaren voor het Blauwdruk. NPR-26506: Hotfix voor CQ-4243957
* URL&#39;s in de Experience Fragment Admin Editor staan geen overlays toe. NPR-26318: Hotfix voor CQ-4252156

#### Platform {#platform}

* Sessilek in ReplicationEventListener met testgebeurtenissen. NPR-25937: Hotfix voor CQ-4251090
* De replicatie gebruikt het verlopen teken voor OAuth, veroorzakend veelvoudige fouten. NPR-25894: Hotfix voor GRANITE-22388

#### Integratie {#integration-3}

* TSDK ingebed met AEM einden met een verbetering aan Handlebars 4 toe te schrijven aan het gebruik van incompatibele malplaatjes. NPR-26699: Hotfix voor CQ-4248974
* Wanneer u een pagina met een nieuw element publiceert, wordt de onderliggende pagina van de publicatie-instantie gedeactiveerd zonder dat hiervan melding wordt gemaakt. NPR-24869: Hotfix voor CQ-4247832
* De replicatie gebruikt een verlopen teken voor OAauth. NPR-25984: Hotfix voor graniet-22388

#### Replicatie {#replication-2}

* Het HTTP-transport kan openstaande sessies lekken. Hotfix voor graniet-17434
* De gelijktijdige toegang door veelvoudige replicatieagenten veroorzaakt uitzonderingen in logboeken wanneer het toegang tot van de knoop van het toegangstoken. NPR-26964: Hotfix voor GRANITE-23276, graniet-23155

#### ContextHub {#contexthub}

* Het bestand `coral.js` bevat een kwetsbare versie van de bibliotheek `handlebars.js` . Hotfix voor CQ-425377

#### DAM - DM-client {#dam-dm-client-1}

* Als u een kopie van een afbeeldingselement verwijdert, is het oorspronkelijke afbeeldingselement onbruikbaar. Hotfix voor CQ-4251648
* Overbodige download van extra afbeeldingsinhoud van S7-servers. Hotfix voor CQ-4248770

#### Graniet {#granite}

* AEM OAuth Provider voert niet het geval-ongevoelige onderzoek uit. NPR-26133: Hotfix voor GRANITE-22650
* De Validator van het pakket bevestigt geen pakketten inbegrepen in GVB/SP. NPR-26775: hotfix voor graniet-22825

#### Gemeenschappen {#communities-6}

* Probleem met scheidingstekens in zoekresultaten. NPR-27051: Hotfix voor CQ-4248939
* Verander de drop-down waarde van Dallas in Virginia in de Leverancier van het Middel van de Opslag van de Adobe. NPR-26936: Hotfix voor CQ-4254434
* Ondersteuning inschakelen voor het zoeken naar gelokaliseerde titels in SocialTagManager. NPR-26932: Hotfix voor CQ-4250276
* In bijlageafbeeldingen wordt geen miniatuur weergegeven wanneer u een forumbericht maakt. NPR-26380: Hotfix voor CQ-4253105
* Met Plakken vanuit Word-plug-in kunnen meerdere afbeeldingen niet worden geladen. NPR-26728: Hotfix voor CQ-4253638
* Kan de inhoud niet filteren op de moderatiepagina. NPR-26697: Hotfix voor CQ-4213766
* (Beveiligingskwetsbaarheid) Accountovername als gevolg van verkeerde configuratie van JWT. NPR-26440: Hotfix voor CQ-4253314
* Het ophalen van gegevens van de Storage Resource Provider van de Adobe is traag. NPR-26237: Hotfix voor NPR-24152
* De privé pagina van de berichtsamenstelling is onregelmatig en langzaam. NPR-26120: Hotfix voor CQ-4250923
* Met het bericht &#39;Alles markeren gelezen&#39; wordt alleen de eerste 10 weergegeven als ongelezen zonder dat de pagina wordt vernieuwd. NPR-27036: Hotfix voor CQ-4254058
* De Paginering Klikken en laden van pagina&#39;s bij Sectie van opmerkingen van gemeenschappen. NPR-27030: Hotfix voor CQ-4251228
* (Forum Search) De knop Terug slaat de pagina over en gaat terug naar forum.html. NPR-26949: Hotfix voor CQ-4254804
* Ongelezen melding neemt niet meer dan 21 toe. NPR-26947: Hotfix voor CQ-4251251
* (De baan van SearchScheduledPosts) voegt toe laat/maakt schakelaar in ConfigMgr toe. NPR-26924: Hotfix voor CQ-4250463
* Tomcat-pad (/aempublish) daalt bij schuiven op de pagina Toewijzingen. NPR-26919: Hotfix voor CQ-4254345
* NullPointerException terwijl het creëren van een groep en een lid. NPR-26778: Hotfix voor CQ-4248095
* De moderator unpins en unfeatured inhoud werkt niet met het Enige Beginsel van de Verantwoordelijkheid MySQL (SRP). NPR-26767: Hotfix voor CQ-4251520
* Problemen met de zoekfunctionaliteit met bepaalde tekens. NPR-26726: Hotfix voor CQ-4247744
* Laat diepe verbindingen voor moderatie UI en enablement middelen toe. NPR-26705: Hotfix voor CQ-4251381
* Een kwestie met het zoeken op de forumcomponent. NPR-26577: Hotfix voor CQ-4251303
* Het zoeken met de eerste en achternaam samen in communautair overseinen keert niet de verwachte resultaten terug. NPR-26377: Hotfix voor CQ-4253150
* Paginering wordt niet bijgewerkt wanneer reacties worden verwijderd. NPR-26327
* Verwijderen van post werkt, maar geeft een fout op de console en de post blijft zichtbaar op de gebruikersinterface. NPR-26292: Hotfix voor CQ-4252803
* De paginering wordt niet dynamisch bijgewerkt en de lijst met reacties wordt steeds langer. NPR-26145: Hotfix voor CQ-4251586
* Groepsinstellingen worden niet geladen in een groep met duizenden gebruikers. NPR-25642: Hotfix voor CQ-4238426
* Catalog Resource Player mislukt voor contextpaden. NPR-25640: Hotfix voor CQ-4238426
* (Forum Search) - Gepagineerde koppelingen naar threads met veel berichten werken niet aan meldingen. Hotfix voor CQ-4254202
* De console van de modernisering toont slechts vijf ingangen met Firefox. Hotfix voor CQ-4254128
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
* (IE11) NaN wordt in het nummerveld weergegeven wanneer een negatieve waarde wordt ingevoerd. NPR-26701: Hotfix voor CQ-100826
* (Koraal. (Meerdere velden) Geneste meerdere velden gebruiken de verkeerde sjabloon om de items te maken. NPR-25649: Hotfix voor CUI-6743
* Werk graniet coralui2 en coralui3 clientlibs bij om Handlebars uit de build te verwijderen. NPR-25606: Hotfix voor graniet-22116

### Forms {#forms-7}

### Forms-invoegtoepassing {#forms-add-on-package-7}

#### Forms - Documentbeveiliging {#forms-document-security-2}

* Uitzonderingen op hoofd-sleutelrollover in serverlogboeken voor in-actieve sleutels. NPR-26748: Hotfix voor CQ-4253705
* Kan de watermerkinstellingen van Documentbeveiliging niet maken of bewerken. NPR-26267, NPR-26129: Hotfix voor CQ-4250234

#### Forms - Acrobat Services {#forms-document-services-4}

* PDF/A-validatie is niet geldig met &quot;validate PDF/A. NPR-25934: Hotfix voor CQ-4248558

#### Forms - Interactieve communicatie {#forms-interactive-communication}

* Als u een bewerkbare module bewerkt en opslaat en vervolgens de voorvertoning van de PDF opent of sluit, blijven de voorvertoning van de letter PDF en HTML zichtbaar. Beide voorvertoningen blijven functioneel in hetzelfde venster. NPR-26770: Hotfix voor CQ-4253217

#### Forms - Workflow {#forms-workflow-2}

* De werkruimte loopt periodiek vast en toont de beginpunten herhaaldelijk. NPR-26461: Hotfix voor CQ-4253439
* De uitzondering ESAPI wordt gegenereerd in de logboeken wanneer accolades worden gebruikt in de taaknaam. Hotfix voor CQ-4256627
* Een null pointer-uitzondering wordt gegenereerd wanneer een niet-vooraf ingevuld adaptief formulier of een aan het beginpunt gerelateerd formulier wordt geopend. Hotfix voor CQ-4256124
* Kan geen e-mail verzenden met de globale instelling. NPR-26163: Hotfix voor CQ-111110
* Kan de werkruimte niet openen nadat het bestand axis.jar is toegepast. NPR-26131: Hotfix voor CQ-4251126
* Met de knop Vernieuwen worden de meest recente gegevens van de server niet gesynchroniseerd met Adaptieve formulieren. Hotfix voor CQ-4255670
* Er wordt een uitzondering gegenereerd wanneer u een zoeksjabloon instelt via de beheerinterface en vervolgens hetzelfde gebruikt om te zoeken in de AEM Forms-werkruimte. Hotfix voor CQ-4255649
* Nadere gegevens over de processen die onder de toepassingen met het haakjessymbool in de naam worden uitgevoerd, worden niet weergegeven in HTML Workspace. Hotfix voor CQ-4242101
* Als u wijzigingen opslaat in het voorkeurenscherm van de HTML Workspace, wordt een uitzondering gegenereerd. Hotfix voor CQ-4241485
* Goedkeuring van bulkobjecten is verbroken bij de laatste JEE-instelling. Hotfix voor CQ-4241486
* Het concept van taak/beginpunt mislukt op de nieuwste 6.4 JEE-server. Hotfix voor CQ-4241484
* Stel de parameter Date().getTime().toString in om de sessie te initialiseren in plaats van Date.toString(). Hotfix voor CQ-4241483
* Bij het openen van /lc/ws wordt een uitzondering voor kwetsbare tekens waargenomen in de parameter HTML. Hotfix voor CQ-4241481

#### Kwetsbaarheid {#vulnerability-1}

* XSS-kwetsbaarheid (Storage Cross-Site Scripting) is opgeslagen op het tabblad Notities van Forms Manager. NPR-27157: Hotfix voor CQ-4255556

### Forms JEE-installatieprogramma {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Codeoverzicht voor Enterprise Security API. Hotfix voor CQ-4255638
* Kan esapi.properties niet laden als bron voor klassebestanden in WAS9. Hotfix voor CQ-4255631
* Als u tijdens de domeinconfiguratie op Verificatie toevoegen klikt, wordt een fout gegenereerd. Hotfix voor CQ-4255634
* Forms JEE biedt ondersteuning voor PKCS#11-wederzijdse verificatie. NPR-21372
* Oplossing voor de problemen die werden gerapporteerd in statische codeanalyse van Core. Hotfix voor CQ-104446
* De implementatie van adobe.livecycle.weblogic.ear en adobe.livecycle.websphere.ear mislukt tijdens het uitvoeren van LCM. Hotfix voor CQ-425629, CQ-4255630
* Ongeldige foutberichten in het toepassingsbeheer. NPR-23289: Hotfix voor CQ-4233163, CQ-4255636
* Als u tijdens de domeinconfiguratie op Verificatie toevoegen klikt, treedt er een fout op. Hotfix voor CQ-4255634

#### Forms - JEE-connector {#forms-jee-connector}

* Het bevestigen van de kwesties die in statische codeanalyse van Schakelaar worden gemeld. NPR-2260

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

AEM Cumulative Fix Pack 6.3.2.2 hangt van AEM 6.3 Service Pack 2 af. Daarom moet u het AEM Cumulatieve pakket van de Moeilijke situatie 6.3.2.x installeren na het installeren van AEM 6.3 Service Pack 2. Voor installatieinstructies, zie de versienota&#39;s in [ AEM 6.3 Service Pack 2 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.11.
* Submiddelen en viewer voor elementen met meerdere pagina&#39;s zijn ingeschakeld in Brand Portal.
* De lengte van veldtype is gewijzigd in 255 ter ondersteuning van alle mogelijke mime-typen voor de verschillende typen bijlagen.
* Foutbericht geconfigureerd van de server wanneer een afbeelding de uploadcriteria overtreedt.
* Extra STARTTLS-ondersteuning in CQ Mail Service op dag.
* Update naar de nieuwste versies van cq-wcm-content en com.adobe.cq.launches.it.serverside.
* Werk com.adobe.granite.ui.coralui3-rte bij naar de meest recente versie die is uitgebracht.
* De verzekerde rendervoorwaarde keert een normaal resultaat terug als expressionResolver ongeldig is.
* Coral.ColumnView: extra ondersteuning voor shift+klikken.

### Assets {#assets-8}

* Het veld CUG (Asset Folder Closed User Group) retourneert niet de groep &#39;Iedereen&#39;. NPR-23163: Hotfix voor CQ-4239377
* Zoeken naar opgeslagen zoekopdrachten in slimme verzamelingen retourneert niet alle resultaten. NPR-23243: Hotfix voor CQ-4240355
* (ExpiryNotificationJobImpl) Optimalisatie van de bestaande query. NPR-2330: Hotfix voor CQ-4205249
* (Metagegevensprofiel) Standaardwaarden voor tags die zijn ingesteld op het moment dat ze worden gemaakt, zijn niet beschikbaar na het opslaan. NPR-23370: Hotfix voor CQ-4235458
* (Aanraakinterface) Kan meerdere elementen niet verplaatsen vanwege een JS-fout. NPR-23395: Hotfix voor CQ-4241279
* De downloadgrootte komt niet overeen met de weergegeven informatie. NPR-23418: Hotfix voor CQ-4242774
* Geëxtraheerd mime-type voor bestandsextensie LSR en SKETCH is onjuist en leidt tot een ongeldige bestandsdownload. NPR-23644: Hotfix voor CQ-4243260
* (Firefox/Chrome) Kan elementen niet downloaden op de pagina voor het delen van bedrijfsmiddelen. NPR-23963: Hotfix voor CQ-4244391
* De zoekfacetten voor Asset Admin verdwijnen na de voorvertoning in de zoekvensters. NPR-23964: Hotfix voor CQ-4244410
* Als u de publicatie van het zoekformulier opheft, wordt het standaardzoekformulier volledig verwijderd. NPR-23291: Hotfix voor CQ-4241382
* (Brand Portal) Zoek in mapvoorspelling moet worden uitgefilterd op replicatie. NPR-23292: Hotfix voor CQ-4241385
* De gebruikersinterface van Publish naar Brand Portal is niet beschikbaar. NPR-23293: Hotfix voor CQ-4241161
* De knop Publish/Unpublish to Brand Portal mag niet beschikbaar zijn voor Content Fragments. NPR-23318: Hotfix voor CQ-4245086
* (Brand Portal) Schakel het maken van subelementen in wanneer een element wordt gepubliceerd. NPR-2331: Hotfix voor CQ-4242018
* Dynamic Media-aanvragen gebruiken geen proxy/HTTP-client. NPR-10727: Hotfix voor CQ-45695, CQ-88800
* Kan geen notitie maken van één uitvoering van MP4 Video-element in Dynamic Media S7 (DMS7). NPR-22046: Hotfix voor CQ-4215912
* De EmbedXMP-gegevens worden altijd ingesteld op &quot;actief&quot; voor TIFF, piramide-generatieproces. NPR-22903: Hotfix voor CQ-4234498
* Problemen met weergave/selectie van dynamische vertoning/selectie met grote aantallen voorinstellingen afbeelding. NPR-23151: Hotfix voor CQ-4217511
* Probleem met Dynamic Media Encode Video - Modification/Reupload launcher. NPR-23237: Hotfix voor CQ-4240260
* Proxy handling fix for HTTP forward in Dynamic Media S7. NPR-24001: Hotfix voor CQ-244140

### Sites {#sites-8}

* De discrepanties van de Bouwer van de vraag het resultaat van verschillende xPath vertaling tussen 6.2 en 6.3. NPR-23245: Hotfix voor CQ-4240396
* Het tabblad Miniatuur in de pagina-eigenschap werkt niet bij het uitbreiden van het dialoogvenster. NPR-22844: Hotfix voor CQ-4241474
* Parsys breekt de de kaderbreedte van het mededingerapparaat en gewassen van om het even welke die component aan het wordt toegevoegd. NPR-22926: Hotfix voor CQ-4238224
* Wanneer het uitvoeren van de veelvoudige lanceringen, bevordert de lancering in Auteur maar de veranderingen worden niet herhaald op de het Publiceren server wegens gebrek aan replicatiemachtigingen. NPR-22934: Hotfix voor CQ-4234746
* Een andere gebruiker in een andere sessie kan een pagina wijzigen die door een gebruiker in de eerste sessie is vergrendeld. NPR-23057; hotfix voor CQ-4199017
* Verbeter de opnieuw te ordenen optie in de Mening van de Lijst. NPR-23065: Hotfix voor CQ-4239321
* (Pagina-editor) De afbeelding op een afbeeldingscomponent verdwijnt wanneer u het dialoogvenster opnieuw opent. NPR-23156: Hotfix voor CQ-4239978
* De Redacteur van het malplaatje toont slechts 20 malplaatjes/omslagen en laadt niet andere wanneer het scrollen aan de bodem van de pagina. NPR-23185: Hotfix voor CQ-4238483
* (Klassieke UI) Er wordt een fout geproduceerd terwijl het bewegen van of het anders noemen van de pagina&#39;s. NPR-23213: Hotfix voor CQ-4240971
* Kan ContextHub-segmenten niet bewerken/maken. NPR-23218: Hotfix voor CQ-4226948
* (Rich Text Editor) - Vervang de bewerking om de opmaak van een woord te wijzigen. NPR-23271: Hotfix voor CQ-4239677
* De uitrollknop ontbreekt op het tabblad Vervagen voor XF-variaties. NPR-23320: Hotfix voor CQ-4240404
* Klassieke interface werkt niet om CUG te bewerken vanwege veroudering. NPR-24122: Hotfix voor 4241823
* Proactieve oplossing om te beschermen tegen ongewenste promoties van inhoud. NPR-24387: Hotfix voor 4244993
* Na ongeveer. Er worden 80 fragmenten toegevoegd aan een map in Assets. Er treden fouten op wanneer de workflow wordt geactiveerd vanuit de tijdlijnconsole. NPR-23393; hotfix voor CQ-4211216
* Kan geen afbeeldingen vanuit de zoekfunctie naar inhoud slepen en neerzetten in het dialoogvenster Rich Text Editor. NPR-23403: Hotfix voor CQ-4242094
* Fout bij &#39;Ongeldige waarde van recursieselectiekader&#39; tijdens het migreren van een component van AEM 6.0 naar AEM 6.2. NPR-23532: Hotfix voor CQ-4241258
* (Rich Text Editor) Knopinfo geeft de variabelenaam van de plug-in weer in plaats van de naam van de leesbare plug-in. NPR-23550: Hotfix voor CQ-4243269
* Kan dialoogvenster niet opslaan met de vereiste vervolgkeuzelijst voor mobiele apparaten/tablets. NPR-23904: Hotfix voor CQ-4243096
* Stijlsysteemopties worden weergegeven op alle pagina&#39;s na de installatie 6.3.2.1. NPR-23972: Hotfix voor CQ-4244394
* Klassieke interface werkt niet om CUG te bewerken vanwege veroudering. NPR-24122: Hotfix voor 4241823
* Proactieve oplossing om te beschermen tegen ongewenste promoties van inhoud. NPR-24387: Hotfix voor 4244993
* De elementverwijzingen worden niet bijgewerkt wanneer elementen worden verplaatst. NPR-23208: Hotfix voor CQ-4239879

### Platform {#platform-1}

* De slimme inzameling toont geen resultaten na sparen als het gebruiken van markeringen in de onderzoeksfacet voorspellen. NPR-23401: Hotfix voor graniet-21278
* Patch jQuery 1.12.4 van clientlib om beveiligingsoplossingen op te nemen. NPR-24128: Hotfix voor graniet-20058
* Internationalisatievertalingen worden nu bijgewerkt wanneer de bundel opnieuw wordt opgestart. NPR-23193: Hotfix voor Sling-7190
* Niet-afgesloten resource resolver in ReplicationEventListener. NPR-23240: Hotfix voor CQ-4241350
* STARTTLS ondersteunen in &quot;Day CQ Mail Service&quot;. NPR-23941: Hotfix voor CQ-4240397
* De naam van de JCR-klachtentag moet automatisch worden ingevuld op basis van de tagtitel. NPR-24173: Hotfix voor CQ-4199411

### Integratie {#integration-4}

* (Doel) Campagnes worden niet geactiveerd wanneer een API-type zoals XML wordt gebruikt. NPR-23199: Hotfix voor CQ-4240936***
* De de verwijzingsreplicatie van de configuratie ontbreekt met een middenomslagstructuur. NPR-23485: Hotfix voor CQ-4242751

### Kwetsbaarheid {#vulnerability-2}

* De integratie van Salesforce is kwetsbaar aan de Smederij van het Verzoek van de Server (SSRF). NPR-24289: Hotfix voor CQ-424527
* XSS (cross-site scripting) in Admin UI-projectkoppelingen. NPR-23272: Hotfix voor CQ-4241795

### WCM - Elementen van de Stichting {#wcm-foundation-components}

* De lijst van de stichting is kwetsbaar aan Opgeslagen Scripting over de hele site. NPR-23214: Hotfix voor CQ-4240760

### Vertaling {#translation-3}

* Eigenschappen van Live Copy worden niet verwijderd tijdens het maken van taalkopieën. NPR-23123: Hotfix voor CQ-4230641

### Gebruikersinterface {#user-interface-1}

* DatePicker biedt geen ondersteuning voor het handmatig instellen van hint voor externe typen die door een verborgen veld worden ingesteld. Als u de teksthint wijzigt, treedt er een omzettingsfout op. NPR-23371: Hotfix voor graniet-21194
* Coral.ColumnView: voeg steun voor shift toe+klik. NPR-23404: Hotfix voor graniet-13338
* Selecteer RT niet geldig wanneer een punt met een lege waarde wordt geselecteerd. NPR-23405: Hotfix voor graniet-21283
* (OMEGA) &quot;Functie&quot; alleen in het Engels rapporteren. NPR-23990: hotfix voor graniet-21231
* Oplossingen voor Coral.AutoComplete API. NPR-23516

### Graniet {#granite-1}

* Apache HTTP client tracking-verbindingen en high-heap-gebruik zorgen ervoor dat de AEM server vastloopt. NPR-23906: Hotfix voor graniet-21056

### Commerce {#commerce-2}

* Uitvoer van Campagne-json bevat geen servlet-contexthoofdmap. NPR-23733: Hotfix voor CQ-4243827

### Gemeenschappen {#communities-7}

* Het zoeken in gemeenschappen mislukt voor weinig woorden. NPR-23256: Hotfix voor CQ-4240717
* Kan geen groepen toewijzen voor de rolkwestie van communitymanagers. NPR-23317: Hotfix voor CQ-4241233: CQ-4221399
* Problemen bij het maken van bronnen met een vergelijkbare naam voor middelen. NPR-23319: Hotfix voor CQ-4240700
* (ContextPath) het breken van berichtfunctionaliteit voor configuraties van de Jetty en fout terwijl het zoeken van groepsleden in de lijst van het groepslid van de gemeenschap. NPR-2336: Hotfix voor CQ-4241519, CQ-4242080
* Het uploaden van een beeld aan een Forum van Gemeenschappen verschijnt niet in de Leverancier van het Middel van de Opslag van de Adobe (ASRP). NPR-23397: Hotfix voor CQ-4242497
* Verwijderde ideeën worden weergegeven als actieve koppelingen in Activiteiten. NPR-23406
* imsmanifest.xml kan niet worden geladen met AEM die met contextwortel lopen. NPR-23483: Hotfix voor CQ-4242193
* Beveiligingsproblemen in een oudere versie van Handlebars. NPR-23518: Hotfix voor CQ-4243055
* De tunnelservice werkt niet. NPR-23543: Hotfix voor CQ-4242217
* Problemen met componenten van gemeenschappen die via Dispatcher worden benaderd en dynamisch verkopen, zijn ook ingeschakeld. NPR-23586: Hotfix voor CQ-4242360, CQ-4241522
* Wanneer het zoeken naar een onderzoekstermijn die vele resultaten door onderzoek veroorzaakt en dan een nieuwe onderzoekstermijn ingaat, wordt het pagineren niet teruggesteld. NPR-23739: Hotfix voor CQ-422593
* Problemen tijdens het uitvoeren van een zoekopdracht op de forumcomponent. NPR-23838: Hotfix voor CQ-4243770
* (Markering voor Gemeenschapsmodernisering) Bulk Allow of flagged messages werkt niet. NPR-23845: Hotfix voor CQ-4243962
* De standaardgeselecteerde waarde wordt niet weergegeven in de knoptekst Sorteren ondanks het selecteren van de standaardsorteervolgorde. NPR-23881: Hotfix voor CQ-4243375
* Web- en e-mailmeldingen worden niet geactiveerd vanwege een fout met het bericht aan de groepen. NPR-23934: Hotfix voor CQ-4242880
* Geen details op de vlaggebruikers en de redenen worden getoond gebruikend de configuratie van DSRP. NPR-23973: Hotfix voor CQ-4243205
* Vlaggen van gebruikers zonder vlag blijven zichtbaar. NPR-23974: Hotfix voor CQ-4243822
* Als u twee bestanden met dezelfde naam twee keer aan een formulierbericht koppelt, treedt er een serverfout op. NPR-24166: Hotfix voor CQ-4244367
* Unable to store attachments with mime types more than 15 characters using Database Storage Resource Developer (DSRP). NPR-24174
* Wanneer een afbeelding die de uploadcriteria overtreedt, naar de posttekst wordt gesleept en neergezet, wordt een serverfout gegenereerd en wordt een algemeen foutbericht weergegeven aan de gebruiker. NPR-24243
* Hiermee worden diverse problemen met de AEM Communities-server opgelost. NPR-23971: Hotfix voor CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Hiermee verhelpt u verschillende Adobe Social-problemen. NPR-24242: Hotfix voor CQ-4245054, CQ-4245120, CQ-4245296

### Campagne {#campaign}

* Uitvoer van Campagne-json bevat geen servlet-contexthoofdmap. NPR-23733: Hotfix voor CQ-4243827

### MSM {#msm}

* Bij het uitrollen van de pagina worden in Live Copy niet de eigenschappen voor aan- en uittijd weergegeven die van de primaire pagina zijn overgenomen. NPR-23873: Hotfix voor CQ-4243431
* De bewerking LiveCopy negeert onderliggende knooppunten van verwijderde componenten niet. NPR-23058: Hotfix voor CQ-4211662

### Verschuiven {#offloading}

* Verzoek om een mechanisme om activa van de arbeidersinstanties na verwerking of regelmatig op te ruimen. NPR-23638: Hotfix voor graniet-21337

## Forms {#forms-8}

### Forms-invoegtoepassing {#forms-add-on-package-8}

#### Adaptieve Forms {#adaptive-forms-1}

* Verplaatsen `ReCaptchaConfigService` naar intern pakket. Hotfix voor CQ-4217459
* Een numeriek veld voldoet niet aan een minimumwaarde. NPR-23967: Hotfix voor CQ-4244830
* Ondersteuning voor Multi Shard in Adaptive Forms integration met Adobe Sign. NPR-23383

#### Backend-integratie {#backend-integration}

* (FDM) (WebService) het steunen van de uitbreidingsconstructie van WSDL in de Parser van WSDL. NPR-23640
* SDLInvokerParams opnemen in Forms Add-on Client SDK. NPR-23157

### Forms JEE Installer {#forms-jee-installer-7}

#### Procesbeheer {#process-management}

* Kan de werkruimte niet openen nadat het nieuwe bestand axis.jar is toegepast. NPR-23316
* LiveCycle dat gevoelig is voor XSS op PMAdmin. NPR-23267
* Na de upgrade naar AEM 6.1 Forms bevriest HTML Workspace bij het openen van Taaklijst voor specifieke gebruikers. NPR-23943

#### Kern {#core}

* Forms JEE biedt ondersteuning voor PKCS#11-wederzijdse verificatie. NPR-21372

#### PDFG-service {#pdfg-service-2}

* De service Documentdigitalisering crasht tijdens het verwerken van TIFF-bestanden (ongeveer 50 kilobyte). NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server Output - Alternatieve beschrijving ontbreekt voor annotaties. NPR-2207
* Voeg PDF/UA-ondersteuning toe aan XML-formulieren die worden gegenereerd door Designer en Output Service. NPR-23132

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}

Lijst van OSGi-bundels opgenomen in AEM 6.3.2.2

[Bestand ophalen](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.2.2

[Bestand ophalen](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulatief Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 2 (6.3.2.0) in April 2018.

De belangrijkste hoogtepunten van **AEM Cumulatief Pak van de Moeilijke situatie** zijn:

* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.10.
* Verbeterde rendering van Parsys-componenten in Classic UI.
* De bijgewerkte bundels van Modellen van het Verspreiden om karakterreeks te omvatten bevestigen.
* Publiceren naar Brand Portal asynchroon gemaakt voor alle elementtypen.
* Bijgewerkte coralui-component-richtexteditor.git van 0.1.15 tot 0.1.16
* Oplossingen in de functionaliteit voor weergeven/verbergen van een vervolgkeuzelijst.
* Omdraaien van afbeelding ingeschakeld voor de Core Image Component.
* Bijgewerkte Felix http-bundels om sessiekenmerken in te schakelen.

* Cache=true is verwijderd bij Sling Models vanwege problemen met geheugenverbruik.

### Assets {#assets-9}

* Als u de titel of miniatuurafbeelding wijzigt in de instellingen van de elementenmap, worden de oorspronkelijke groep en machtigingen van de map overschreven. NPR-22171: Hotfix voor CQ-4216080
* De gebruikersinterface genereert een fout &quot;Publish naar Brand Portal is mislukt&quot;, terwijl de taak wordt toegevoegd aan de replicatiewachtrij en de middelen worden gepubliceerd naar Brand Portal. NPR-22179: Hotfix voor CQ-4205273
* (Aanraakinterface) Standaarduploadlocatie voor elementen in de kolomweergave. NPR-22465: Hotfix voor CQ-4237057
* AEM genereert een StackOverflow-fout wanneer u probeert een elementschema te kopiëren van `/conf/global` naar `/conf/mytenant` . NPR-22489: Hotfix voor CQ-4235875
* Het uitpakken van een ZIP-archief mislukt als gevolg van de afsluitende ruimte aan het einde van de mapnaam. NPR-22522: Hotfix voor CQ-4238036
* Sorteren met de kolom Titel van element werkt niet voor zoekresultaten. NPR-22908: Hotfix voor CQ-4239076
* YouTube-video wordt gelabeld met het volledige pad in plaats van de tagnaam zelf. NPR-22976: Hotfix voor CQ-4238669
* Het opnieuw ordenen van mappen onder een map die opnieuw kan worden geordend, duurt niet voort. NPR-23125: Hotfix voor CQ-4231761
* HTTP 504: De fout van de Onderbreking van de gateway wanneer het proberen om inzamelingen te delen gebruikend een aandeelverbinding. NPR-21928: Hotfix voor CQ-4234507
* Metagegevens van het trefwoord PDF worden niet correct geëxtraheerd en gewijzigd wanneer er meerdere trefwoorden zijn gekoppeld aan een element PDF. Om het probleem op te lossen, is de eigenschap voor metagegevens van het veld Onderwerp verwijderd voor PDF Assets. U kunt het schema Metagegevens echter bewerken door een tekstveld met meerdere waarden toe te voegen voor het veld Onderwerp. NPR-21972: hotfix voor 4215741****
* Verkeerde elementen worden verwijderd als de geselecteerde map wordt gewijzigd tussen het moment dat de twee pop-ups worden weergegeven. NPR-21980: Hotfix voor CQ-4233675
* (DAM) Meerdere XSS-kwetsbaarheden (Cross-Site Scripting) tijdens het toevoegen aan de wizard Verzameling. NPR-22432: Hotfix voor CQ-4327086
* Downloaden van middelen mislukt wanneer Digital Rights Management in Assets op Safari wordt gebruikt. Gebruikers kunnen geen elementen downloaden met een disclaimer- en lange bestandsnaam. NPR-22747: Hotfix voor CQ-4236460 en CQ-4235274
* Openbaar maken als standaardoptie tijdens het publiceren van elementen naar Brand Portal. NPR-21931: Hotfix voor CQ-4218816

### Sites {#sites-9}

* Een nieuw item in Workflowinbox toont het paginapad in plaats van de titel van de pagina. NPR-21634: Hotfix voor CQ-4230672
* Bewerkbare structuurcomponenten verliezen de CSS-klassenamen die nodig zijn voor het responsieve raster wanneer deze worden bewerkt. NPR-21741: Hotfix voor CQ-4232374
* (TouchUI) Meerdere XSS-kwetsbaarheden (Cross-Site Scripting) voor HTML-componenten. NPR-21899: Hotfix voor CQ-4232511
* Kan het middeltype van de afbeeldingsbron voor het fragment met gemengde media van inhoud niet wijzigen. NPR-21907: Hotfix voor CQ-4233401
* RTE Volledig scherm voor het dialoogvenster Touch UI verbergt de RTE-plug-ins. NPR-22034: Hotfix voor CQ-4235457
* (Aanraakinterface) De RTF-editor verwijdert alle andere kenmerken dan id uit de &lt;a>-tag. NPR-22044: Hotfix voor CQ-4234133
* De veelvoudige gestapelde Parsys toe te schrijven aan langlopende vragen (meer dan 6) maakt AEM langzaam. NPR-22134: Hotfix voor CQ-4233904
* Kan machtigingen niet wijzigen voor knooppunten met dubbele punten in de naam. NPR-22136: Hotfix voor CQ-4236221
* (Klassieke UI) De uitvoer van de Rich Text Editor HTML voegt &#39;list-position-style: inside;&#39; als inline stijl toe aan de tag &lt;ul>. NPR-22145: Hotfix voor CRTE-114
* Laat TreeNode terugvallen naar het naamattribuut wanneer de tekst leeg is. NPR-22146: Hotfix voor CQ-4234724/CQ-4236300
* RSS-feed-problemen, poort -1 tot AEM 6.3. NPR-22176: Hotfix voor CQ-4233339
* (Klassieke UI) de kortere weg van het Plakken van tekst (Ctrl+V) werkt niet voor de component van de Tekst OTB (RTF). NPR-22224: Hotfix voor CQ-4236224
* Het filteren van het tagveld werkt niet zoals u had verwacht bij het typen van tekst. NPR-22236: Hotfix voor CQ-4236655
* (Pagina-editor) Bij het plakken van tekstgegevens in de component voor afbeeldingskaarten wordt de component Text ook geplakt bij het plakken van tekstgegevens in de component voor afbeeldingen met hyperlinks. NPR-22264: Hotfix voor CQ-4236230
* Vereist veld FileUpload van dialoogvenster veroorzaakt problemen bij het verzenden van het dialoogvenster. NPR-22464: Hotfix voor CQ-4222192
* Als u de verplaatsingsmachtigingen zonder replicatiemachtigingen verplaatst, wordt een aanvraag voor de activeringsworkflow gestart als de verplaatste pagina of de referenties niet kunnen worden geactiveerd. NPR-22467: Hotfix voor CQ-4211765
* Prestatieproblemen bij het laden van een pagina met een groot (2000+) publiek. NPR-22478; hotfix voor CQ-4209567
* De persistentie kwesties wanneer de opslag ContextHub de standaardpersistentielaag tijdens initialisatie overschrijft. NPR-22479: Hotfix voor CQ-4218399
* Bij starten met meerdere pagina&#39;s worden geen subpagina&#39;s naar publicatieservers gepubliceerd als &#39;subpagina&#39;s opnemen&#39; niet is ingeschakeld in de eerste hoofdmap van de inhoud. NPR-22482: Hotfix voor CQ-4237818
* (Interface van de aanraking) schrapping van lanceringen door de Klassieke console UI maakt alle pagina&#39;s onbewerkbaar. NPR-22491: Hotfix voor CQ-4225074
* Problemen met de component Image vanwege extra ruimte in het dialoogvenster. NPR-22528: Hotfix voor CQ-4238183
* Wanneer u de component opent in de inlinemodus, zijn eerder geladen plug-ins de tweede keer niet zichtbaar. NPR-22591: Hotfix voor CQ-4236850
* Als u een opstart verwijdert in een geneste opstart, worden subopstarters wees. NPR-22621; hotfix voor CQ-4202639
* (Klassieke UI sidekick) Het tabblad Workflow is uitgeschakeld wanneer de pagina zich in het werkstroomvergrendelingsstadium bevindt. NPR-22722: Hotfix voor CQ-4237557
* Nadat u een afbeelding die in de afbeeldingscomponent op een pagina is toegevoegd, hebt gespiegeld, worden de wijzigingen niet opgeslagen en wordt de oorspronkelijke afbeelding op de pagina weergegeven. Het teruggeven van steun is toegevoegd aan de component van de beeldkern als [ https://github.com/adobe/aem-core-wcm-components/pull/141 ](https://github.com/adobe/aem-core-wcm-components/pull/141). NPR-22801: Hotfix voor CQ-4221539
* Wanneer de gebruiker het bestaande anker probeert te verwijderen uit het ankermenu, wordt het venster van de component Rich Text Editor gesloten en blijven de wijzigingen niet opgeslagen. NPR-22802: Hotfix voor CQ-4238167
* Het filter van Onderzoek toont niet alle acties in de console van Plaatsen. NPR-22804: Hotfix voor CQ-4239007
* Probleem met kopiëren/plakken in aanraakinterface met systeemklembord en intern AEM klembord. NPR-22807: Hotfix voor CQ-4220383
* Inconsistentie in de uittrekmarkering die door Lucene Search is geretourneerd. NPR-22879: Hotfix voor CQ-4238513
* Als u een pagina met publicatieexemplaren activeert, krijgt u een groene status in plaats van een pagina te ambereren. NPR-22927: Hotfix voor CQ-4236310
* (StyleSystem) De schermpositie springt tijdens het selecteren van een stijl in het pop-upmenu. NPR-23183: Hotfix voor CQ-4238867
* (Publicatie beheren) Voor het verplaatsen naar de volgende maand van de kalender moeten meerdere klikken worden uitgevoerd. NPR-23508: Hotfix voor CQ-4242732

### Platform {#platform-2}

* Met het servlet Sling Exporter worden Japanse tekens niet correct geëxporteerd. NPR-22153: Hotfix voor CQ-4228920
* Blokkering van de planner tijdens het opstarten. NPR-22440: Hotfix voor Sling-7004
* Kan groepen niet synchroniseren tussen twee publicatie-instanties. NPR-21943: Hotfix voor graniet-19564
* Prestatieproblemen met org.apache.sling.i18n gedeelde sessie/resource resolver. NPR-23390: Hotfix voor Sling-7543

### Integratie {#integration-5}

* Unclosed ResourceResolver in com.day.cq.analytics.sitecatalyst. NPR-22323: Hotfix voor CQ-4236515
* TargetContentImpl maakt AEM tijdens langdurige query&#39;s traag. NPR-22361: Hotfix voor CQ-4236907
* De doelengine (mbox.js, at.js) gebruikt geen beheerde URL&#39;s. En, gebruikt URLs die dubbelepunten bevatten die met bepaalde plaatsingen zouden kunnen ontbreken. NPR-22366: Hotfix voor CQ-4237854
* Wanneer u een aangepaste tag at.js of mbox.js opgeeft, wordt het opgenomen script als tekst naar de pagina geschreven in plaats van als HTML-tags. NPR-22441: Hotfix voor CQ-4203691
* In de modus Doel kunnen auteurs een component die van de blauwdruk is overerfd, wijzigen zonder de overerving te annuleren. NPR-22751: Hotfix voor CQ-4237907
* PersonalizationDataSource genereert een null pointer uitzondering vanwege het ontbreken van `jcr:content` node. NPR-22850: Hotfix voor CQ-4222122
* AEM het richten ontbreekt wanneer het gebruiken van de niet-Engelse taal. NPR-22917: Hotfix voor CQ-4218213
* Bij het publiceren van een pagina met doelinhoud ontbreken gerelateerde bronnen. NPR-23064: Hotfix voor CQ-4227119
* Gebruikers kunnen de statische parameterwaarden van de test niet in de mbox vraag zien, die wanneer het testen met AT.js als cliëntbibliotheek in wolkenconfiguratie kan worden gezien. NPR-21930: Hotfix voor CQ-4234520

### WCM-stichtingscomponenten {#wcm-foundation-components-1}

* InParsys wordt de positieverschuiving gemaakt nadat het selectievakje Overerving annuleren/uitschakelen is uitgeschakeld. NPR-21905: Hotfix voor CQ-4230951
* De functionaliteit tonen/verbergen van de formuliervervolgkeuzelijst werkt niet zoals u had verwacht. NPR-22327: Hotfix voor CQ-422853
* De component CAPTCHA is vervangen voor betere beveiliging. Als u de component CAPTCHA gebruikt, dan wordt het bericht &quot;de component Captcha wordt afgekeurd en zou niet meer moeten worden gebruikt&quot;getoond na het installeren van 6.3.2.1 of recentere versie. AEM component kan worden aangepast om reCAPTCHA op te nemen voor betere beveiliging NPR-22151: Hotfix voor CQ-4220052

### WCM - Pagina-editor {#wcm-page-editor}

* Gespiegeld XSS (Cross-Site Scripting) bij gebruik van een ongeldige kiezer. Hotfix voor CQ-4270397

### Vertaling {#translation-4}

* Problemen met de voorvertoningsfunctie onderzoeken. NPR-22114: Hotfix voor CQ-4223753

### Gebruikersinterface {#user-interface-2}

* Problemen met de maandkiezer voor Coral Calendar wanneer het datumbereik &#39;min&#39; en &#39;max&#39; is ingesteld. NPR-22716: Hotfix voor CUI-7187
* (Klassieke UI) De component toont de standaardwaarden zelfs als de bijbehorende dienst van het Model van de Gegevens van de Vorm aan een leeg gebied wordt geplaatst. NPR-22272: Hotfix voor GRANITE-19744

### Graniet {#granite-2}

* Stabiliteitsproblemen met de uitgeversinstantie voor het delen van bedrijfsmiddelen die worden veroorzaakt door geheugenlek. NPR-22205, NPR-23178: Hotfix voor Sling-5668, Sling-7292 en Sling-7470.
* De instabiele dienst ID voor de namen van zittingsattributen zou niet moeten worden gebruikt. NPR-22821: Hotfix voor graniet-21059
* Wanneer een http whiteboard-managed zitting ongeldig wordt gemaakt, wordt de containerzitting ook ongeldig gemaakt als de zitting geen andere zittingsattributen heeft. NPR-23059: Hotfix voor FELIX-5819
* LogbackManager kan sommige OSGi config op het tijdstip van opstarten missen. NPR-23060: hotfix voor graniet-19791

### Commerce {#commerce-3}

* Schakel het maken van een workflow in het menu Experience Fragments in. NPR-22347: Hotfix voor CQ-4221661
* Ervaar Fragmentfouten die reproduceerbaar zijn op WeRetail. NPR-21958: Hotfix voor CQ-420061
* Wanneer een pagina met een verwijderd ervaringsfragment wordt geactiveerd, wordt een NullPointerException gegenereerd. NPR-23179: Hotfix voor CQ-4239939

### Projecten {#projects}

* (Meertalig project) Het project vermeldt geen vertaaltaken voor meer dan 19 talen. NPR-22498: Hotfix voor CQ-4229978

### Workflow {#workflow}

* (Klassieke UI) Het toelaten van of het onbruikbaar maken van een werkschemalancering leidt tot slecht gedrag. NPR-22907: Hotfix voor CQ-4239153

## Forms {#forms-9}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

De belangrijkste markeringen voor AEM Forms zijn:

* Toegevoegde ondersteuning voor invoertype HTML5.
* Correctie SOAP basiskoptekstverificatie.
* Toegevoegde ondersteuning voor titelkenmerk voor hyperlink.
* PDF/UA-id ingeschakeld in de toegankelijkheidsstructuur van Forms Designer.
* Certificaatverificatie ingeschakeld voor Workbench-gebruikers.
* Toegevoegde ondersteuning voor het produceren van PDF-bestanden die compatibel zijn met PDF/A-2a of PDF/A-3a.

### Forms-invoegtoepassing {#forms-add-on-package-9}

#### UI Forms-Admin {#forms-admin-ui}

* Het wachtwoord is zichtbaar in duidelijke teksten wanneer u het wachtwoordgebied op de pagina&#39;s van de Configuratie van de Verbindingen ECM inspecteert. NPR-22508: Hotfix voor CQ-4236065

#### Forms Service {#forms-service}

* Wanneer SSL is ingeschakeld, werken de gebeurtenissen Verzenden en Verlaten niet met Form Analytics. NPR-22637; hotfix voor CQ-4237973

#### Gebruikersbeheer {#user-management}

* Kan LDAP niet synchroniseren vanwege onjuiste cglib-nodep-versie. NPR-22493: Hotfix voor CQ-4234099

#### Adaptieve Forms {#adaptive-forms-2}

* De functies van de douane voor de Redacteur van de Regel voegen extra toe; na de functievraag. Daarom ontbreken zij de bevestiging alhoewel de douanefunctie waar terugkeert. NPR-22481: Hotfix voor CQ-4235499
* Ongeacht het geselecteerde datumpatroon volgt de component date-Picker het patroon niet bij het weergeven van minimum- en maximumvalidatieberichten. NPR-22444: Hotfix voor CQ-4236269
* De datumnotatie die wordt verzonden in de verzendaanvraag moet worden uitgelijnd op het patroon in de component date-picker. NPR-22384
* Het opgegeven maximum aantal tekens voor een adaptief tekstvak in een formulier wordt niet ondersteund op Android™ 6.0 Samsung-apparaten. NPR-22363, NPR-22364: Hotfix voor CQ-4235205
* (Microsoft® Edge) (IE11) De adaptieve vorm tekst-gebied component met multiline gebied toont `Null` als standaardwaarde in plaats van leeg. NPR-22284: Hotfix voor CQ-69107
* SOAP UTF-8 Input Encoding in Adaptive Forms retourneert fouten met verstoorde pagina. NPR-20105: Hotfix voor CQ-4222669
* De AEM Forms Container-component kan niet worden bewerkt nadat het verkeerde formulier op de AEM Sites-pagina is geconfigureerd. Hotfix voor CQ-4237456
* De tests van de ontwikkeling ontbreken wanneer looppas op servers JEE. Hotfix voor CQ-422082
* AF test het ontbreken op servers JEE wegens minificatiekwesties in het kader Calvin. Hotfix voor CQ-4217220

#### Forms Manager {#forms-manager}

* (Firefox) De eigenschappen van het XML-schema van Adaptive Forms kunnen niet worden bijgewerkt omdat de opties in het Document of Record (DOR) niet worden weergegeven als vooraf geselecteerd op de eigenschappenpagina. NPR-22298: Hotfix voor CQ-4237402
* Forms die na publicatie van de pagina is gewijzigd, wordt niet opnieuw gepubliceerd. NPR-23013: Hotfix voor CQ-4236566

#### Backend-integratie {#backend-integration-1}

* OOTB de basisauthentificatie voor de SOAP diensten werkt niet voor basisauthentificatie in integratie FDM. NPR-23238: Hotfix voor CQ-4241308

#### Correspondentenbeheer {#correspondence-management}

* Als de XDP&#39;s van OOTB in de letter worden gebruikt en als voorbeeld worden weergegeven, wordt de inhoud weergegeven die met de voettekst wordt overlapt. Hotfix voor CQ-4212414

#### Assembler-service {#assembler-service}

* Discrepancy tussen Acrobat DC en AEM rapporten over de fout van de PDF/A-1b nalevingscontrole. NPR-22051, NPR-22050: Hotfix voor CQ-4226128, CQ-4227671

### Forms JEE-installatieprogramma {#forms-jee-installer-8}

#### Workbench {#workbench}

* Certificaatverificatie ingeschakeld voor Workbench-gebruikers. NPR-20644: Hotfix voor CQ-4214486
* Het serverlogboek downloaden met Workbench werkt alleen voor de ene server, terwijl het voor de andere server niet werkt. NPR-21079: Hotfix voor CQ-4229842

#### Procesbeheer {#process-management-1}

* (HTML Workspace) Problemen met de schermgrootte met schuifbalken. NPR-2328
* (HTML Workspace) Beginpunten van processen worden niet in alfanumerieke volgorde gesorteerd. NPR-22841 Hotfix voor CQ-4238944
* (HTML Workspace) Bereid Gegevens voor die worden geactiveerd wanneer een formulier in de werkruimte wordt gesloten. NPR-21127: Hotfix voor CQ-4224574
* (HTML Workspace) Wanneer u een proces aanroept waarvoor lange beschrijvingen vereist zijn, werkt de knop Notities uitvouwen niet. Hotfix voor CQ-4241488

#### Kern {#core-1}

* Fout aangetroffen bij opstarten terwijl de planner wordt gestart. NPR-22990
* Browsers kunnen geen gegevens opslaan die zijn ingevoerd in HTML-formulieren. NPR-21762: Hotfix voor CQ-4206543
* De in de statische codeanalyse van Core gerapporteerde problemen moeten worden vastgesteld. Hotfix voor CQ-104446

#### PDFG-service {#pdfg-service-3}

* PDF Generator kan geen PDF-documenten met opgegeven bladwijzerniveaus maken. NPR-22921, NPR-22285: Hotfix voor CQ-4230562
* Toegevoegde ondersteuning voor het produceren van PDF-bestanden die compatibel zijn met PDF/A-2a of PDF/A-3a. NPR-23021: Hotfix voor CQ-4214172

#### Forms Designer {#forms-designer-1}

* De PDF/UA-id ontbreekt wanneer deze wordt opgeslagen als PDF in Designer. NPR-23137
* Padobjecten, bijvoorbeeld: randen, onderstrepingen en hyperlinks, worden niet gecodeerd wanneer ze vanuit Designer als PDF worden opgeslagen. NPR-23136
* Afbeeldingsobject heeft geen selectiekader wanneer het wordt opgeslagen als PDF van Designer. NPR-23134
* Inline-hyperlinks die zijn gedefinieerd in Designer, krijgen geen label of hebben alternatieve tekst wanneer ze worden opgeslagen als PDF vanuit Designer. NPR-2313
* Als u het XML-gegevenspakket opent met AEM 6.3 Forms Designer, wordt de XHTML-opmaak verwijderd uit de XML-bron. NPR-21178: Hotfix voor LC-3917046

#### LCM installeren {#install-lcm}

* Jsafe Jars bijwerken naar Cryptoj 6.1.3.1 in installatieprogramma en LCM. NPR-21370

#### Handtekeningenservice {#signatures-service}

* Er is een uitzondering opgetreden tijdens het digitaal ondertekenen van een PDF-document via HSM. NPR-21154: Hotfix voor CQ-4226978

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

### Assets {#assets-10}

* Gewijzigde interface voor ondersteuning van de implementatie van CUG-functionaliteit in AEM Assets. NPR-19485
* Het uploaden van een element als een rechtstreeks onderliggend knooppunt van zichzelf via de aanraakinterface veroorzaakt een probleem. Het element wordt geüpload als een direct onderliggend element van het eerder geselecteerde element. NPR-19736
* Datumbereik voorspellen en Bereik voorspellen werken niet bij het laden van een opgeslagen zoek-/slimme verzameling. NPR-19844: Hotfix voor CQ-4220808
* AEM wordt traag wanneer meerdere elementen (meer dan 4) naar Brand Portal worden gepubliceerd. NPR-2009: Hotfix voor CQ-4213426
* Kan geen elementen met spaties downloaden van de pagina met de licentiecontrole. NPR-20067: Hotfix voor CQ-4216557
* Problemen bij het uploaden van PSB-bestanden met meerdere alpha-lagen worden verwerkt. NPR-20250: Hotfix voor CQ-4220869
* Gebruikers kunnen geen elementen downloaden met lange gedefinieerde bestandsnamen en disclaimer. NPR-20254
* ProductAssetsUploader verlaat de tijdelijke bestanden van Java™ cache in de map Java™ TEMP. NPR-20256: Hotfix voor CQ-4221801
* Vervang de vergelijkingscode van de versie met de merkgebonden code van de Adobe wegens vergunningskwesties. NPR-20272: Hotfix voor CQ-4223758
* De meta-gegevens voor een koordbezit, documentNumber verschijnt als datum terwijl het een aantal zou moeten zijn. NPR-20291: Hotfix voor CQ-4223991
* Tekstomloop blijft vastzitten voor een beschadigde PDF. NPR-20416: Hotfix voor CTG-4150375
* Gecomprimeerde bestanden die elementen bevatten die niet compatibel zijn met UTF-8, worden niet correct gedownload. NPR-20420: Hotfix voor CQ-4219961
* Te veel tekens in OmniSearch kunnen ertoe leiden dat de AEM server vastloopt. NPR-20434: Hotfix voor CQ-4223602
* Metagegevens van de DAM Asset API-fout breekt de xmp-write-back API&#39;s. NPR-20607: Hotfix voor CQ-4220455
* Prestatieproblemen bij het toevoegen van gebruikers aan verzamelingen. NPR-20699: Hotfix voor CQ-4225733
* Publish naar Brand Portal van AEM mag niet worden toegestaan voor Dynamic Media-sets. NPR-20320: Hotfix voor CQ-4221147
* Video met spaties en accenten levert geen video op voor de pagina Renditions. NPR-19961: Hotfix voor CQ-4221014
* Oplossing voor meerdere problemen met de verwerking van mappen met Assets API&#39;s. NPR-20569
* AEM Dynamic Media Classic (voorheen Scene7) synchroniseert geen elementen van AEM server. Deze kwestie komt voor wanneer de bestemmingspad in de Configuratie van de Cloud Service aan een subfolder van de wortelweg richt. CQ-4228265
* E-mailbundel van Apache-opmerkingen `{org.apache.commons/commons-email/1.5}` is toegevoegd ter vervanging van `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}` .

### Sites {#sites-10}

* Problemen met beheerdersrechten: leden van gesloten gebruikersgroepen kunnen niet worden verwijderd uit pagina-eigenschappen. NPR-20631
* De getypte werkstroomnaam moet beschikbaar zijn in het vak Melding wanneer u een pagina publiceert via Publicatie beheren. NPR-20046: Hotfix voor CQ-4221586
* Als u opgemaakte tekst toepast op twee rijen in de Rich Text Editor en deze vervolgens samenvoegt in één alinea, worden de opgemaakte reeksen verwijderd. NPR-2010: Hotfix voor CQ-4223051
* Wijzigingen in veldeigenschappen op meerdere tabbladen van het dialoogvenster Eigenschappen bewerken worden soms niet opgeslagen. NPR-20286
* Onverwachte tag aan het einde van de geplakte inhoud in inhoudsfragment. NPR-20413: Hotfix voor CQ-4224014
* Implementeerde een mechanisme in Adobe Campaign om het beleid van een inhoudsbron van een externe doelbron op te halen. NPR-20667
* Plug-in voor RTF-bestanden werkt niet voor zowel inline als volledig scherm in Touch UI met meerdere velden. NPR-20973

### Campagne {#campaign-1}

* Placeholders zijn niet zichtbaar in een pagina die veelvoudige componenten Parsys bevat. NPR-20436; hotfix voor CQ-4215000

### Commerce {#commerce-4}

* De Fragmenten van de ervaring tonen niet behoorlijk in Internet Explorer 11. NPR-20161: Hotfix voor CQ-4223319
* In handelswerkstromen, wordt een leeg beeld automatisch opgenomen wanneer het creëren van een variant die op een primair product met veelvoudige beelden wordt gebaseerd. NPR-20068: Hotfix voor CQ-422048
* Filteren met tags op verzamelingspagina&#39;s in de productconsole werkt niet. NPR-20292: Hotfix voor CQ-4224023

### Gemeenschappen {#communities-8}

* Inconsistente zoekresultaten met zoekresultaatcomponent. NPR-20070: Hotfix voor CQ-4220913
* E-mailmeldingen worden niet geactiveerd voor een van de aan de moderator gerelateerde activiteiten met betrekking tot gepubliceerde componenten. NPR-2012
* De lege paginering zonder resultaten wordt getoond voor anonieme communautaire gebruikers. NPR-20136: Hotfix voor CQ-4220738
* Vorm waakzame trekker wanneer een UGC als spam wordt ontdekt of wanneer een gebruiker op een pre-gematigde plaats post. NPR-20274: Hotfix voor CQ-96850
* Meerdere problemen met AEM Communities-sitepagina&#39;s zijn opgelost, waaronder onjuiste omleidingen en problemen met het vernieuwen van pagina&#39;s. NPR-2034
* CommunityUserOperationExtension wordt uitgevoerd in een klassecasting. NPR-20532: Hotfix voor CQ-4224385
* Nadat gebruikers een Community-site hebben gemaakt, kunnen ze deze niet openen vanuit de sitemap omdat het contextpad niet wordt toegevoegd aan de URL. NPR-20730

### Integratie {#integration-6}

* Het migreren Analytics bestaande geloofsbrieven aan Authentificatie WSSE. NPR-19962: Hotfix voor CQ-4218071
* Het opnieuw activeren van het segment na een wijziging mislukt en er treedt een fout op. NPR-20054: Hotfix voor CQ-4218401
* In de configuratie van de cloudservice van Search&amp;Promote wordt de methode voor het ophalen van formulieren genegeerd, waardoor deze onbruikbaar wordt voor de instantie van de auteur. NPR-20447: Hotfix voor CQ-4206076
* Bij dubbelzinnige filterdefinitie in het inhoudspakket worden paden overschreven wanneer het Search&amp;Promote-onderdeel wordt geïnstalleerd. NPR-20808

### Mobiel op aanvraag {#mobile-on-demand}

* Eigenschappen van metagegevens voor elementen van het type TXT worden telkens weergegeven in verschillende metagegevenseditors wanneer de eigenschappen ervan worden weergegeven. NPR-20239

### Platform {#platform-3}

* Resolved an unclosed resource resolver uitzondering. NPR-19749: Hotfix voor graniet - 19143
* Verzoek om douanekaarten om samen met standaardgezondheidscontroles in het verrichtingendashboard worden getoond. NPR-20145
* De annotatielaag van de pagina-editor werkt niet goed in Internet Explorer 11. NPR-20222: Hotfix voor CQ-422818
* De lekken van de zitting bij het plaatsen van de Agent van de Gebruiker als admin in replicatieagent. NPR-20578
* requestAttributes is nu unset voor andere gegeven-slim-middel verklaringen. NPR-20639: Hotfix voor 4226206
* Correctie van problemen met curl Head-aanvragen voor OOTB-middelen in AEM. NPR-20781: Hotfix voor CQ-4221520

### Projecten {#projects-1}

* De toegang tot van verschillende projecten van de console van Projecten vergt een langere tijd om te laden. NPR-20314
* Wanneer u AEM 6.3.0.1 installeert, wordt het sleutelarchief van de gebruiker van `dam-update-service` verwijderd. NPR-2018
* In sommige douaneplaatsingen, nemen de gebruikers die proberen om een toegewezen in de addTask module te selecteren langer om de lijst in de gebruikersplukker te bevolken. NPR-20283: Hotfix voor CQ-4224193

### Gebruikersinterface {#user-interface-3}

* Het veld Kleur is ingesteld op &quot;altijd vereist&quot;, ondanks kenmerken in het dialoogvenster. NPR-19702
* De schuifbalk wordt niet in Internet Explorer 11 weergegeven voor component Multi-field in een volledig scherm. NPR-20261: Hotfix voor CQ-4219782
* Vorige query&#39;s worden niet afgebroken als opeenvolgende query&#39;s worden geactiveerd, wat leidt tot onjuiste resultaten. NPR-20398: Hotfix voor GRANITE-19306

### Workflow {#workflow-1}

* Gebruikers worden niet op de hoogte gesteld van de workflowtaken die ze in hun Postvak IN ontvangen. NPR-20213: Hotfix voor CQ-4221639
* De OTB-gebruikerkiezer voor graniet laadt geen gebruikers wanneer u in de stap Deelnemer Dialoogvenster op een vervolgkeuzelijst klikt. NPR-20236

## Forms {#forms-10}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-10}

#### Adaptieve Forms {#adaptive-forms-3}

* Ondersteuning voor samenvoegingsexpressie voor herhaalde deelvensters ontbreekt. NPR-20861
* In vervolgkeuzelijst wordt de laatst opgeslagen waarde weergegeven, zelfs als de bijbehorende service Formuliergegevensmodel geen waarde retourneert. NPR-20710
* Kan de bestaande regels niet bewerken met Booleaanse beperkingen in de regeleditor. NPR-21128

#### Formulierportal {#form-portal}

* HTML-profiel wordt weergegeven voor een adaptief formulier, zelfs als het elementtype niet XDP is. NPR-20079

#### Backend-integratie {#backend-integration-2}

* Kan de waarde van de component Switch niet instellen op true of false. NPR-2111

#### OSGI Workflow {#osgi-workflow}

* Met workflowverzending kunt u slechts tien toepassingen beheren. CQ-4230193

#### HTML5 Forms {#html-forms-3}

* De naam van een XDP-formulierobject als een subformulier wordt weergegeven als knopinfo als dit niet is gedefinieerd in de toegankelijkheidsconfiguraties. NPR-20523

### Forms JEE-installatieprogramma {#forms-jee-installer-9}

#### Procesbeheer {#process-management-2}

* Het startpunt van FormSetPrefillApp vult geen formuliervelden in de AEM Forms-app vooraf in. NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* Installeer de nieuwste CTJPEG2K-bibliotheek voor een kritieke beveiligingskwetsbaarheid. Dit is van invloed op de modules XMLFM (AEM en IfBA), RM en PDFG. NPR-20625: NPR-2137.

### Inclusief functiepakketten {#feature-packs-included}

#### AEM Forms App {#aem-forms-app}

* Ondersteuning voor OSGi-workflowtaken ingeschakeld in AEM Forms App. CQ-422638

### OSGI-pakketten en inhoudspakketten opgenomen in 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}

Lijst van OSGi-bundels opgenomen in AEM 6.3.1.2

[Bestand ophalen](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Lijst van inhoudspakketten opgenomen in AEM 6.3.1.2

[ krijgt Dossier ](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM Cumulative Fix Pack 6.3.1.1 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 Service Pack 1 (6.3.1.0) in oktober 2017.

De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* Publiceren naar Brand Portal-actie ingeschakeld voor het standaardformulier Metagegevensschema.
* Gedragswijziging bij het weergeven van titels op afbeeldingskaart voor afbeelding met dc: eigenschap title ingesteld op `String [] (multifield)` .
* Rendering van tijd op de server is vervangen door een basis-tijdcomponent.
* Publicatietags van AEM naar Brand Portal zijn ingeschakeld vanuit de tagbeheer-/tagingconsole.
* Gepubliceerde JSON API voor het gebruik van inhoudsfragmenten.
* De ingebouwde opslagplaats (Apache Jackrabbit Oak) wordt bijgewerkt naar versie 1.6.5.

### Assets {#assets-11}

* Als twee velden met dezelfde eigenschap worden toegewezen aan verschillende typen eigenschapvelden, treedt er een interne fout op. NPR-19462: HF voor CQ-4216828
* dc: titel en dc: beschrijving verandert niet in een waarde met meerdere velden in CRXDE Lite. NPR-19570: HF voor CQ-4209086
* De dynamische viewer laadt de video-uitvoering van de laagste kwaliteit voor het testen van het afspelen van video in de auteursmodus. NPR-1904
* Dynamische uitvoering kan niet worden gedownload voor elementen die spaties in hun namen opnemen. NPR-19433: Hotfix voor CQ-4211738
* Kan geen volledige lijst met pagina&#39;s/middelen laden in de kolomweergave met Chrome. NPR-19566: Hotfix voor CQ-4214248
* De optie Publish naar Brand Portal is niet beschikbaar bij het selecteren van schema&#39;s, zoekfacetten of voorinstellingen. NPR-1950
* Als u een element selecteert in de kolomweergave en op Bewerken klikt, wordt er een fout geretourneerd. NPR-20301: Hotfix voor CQ-4224052
* Weergave Vervaldatum van activa is uitgeschakeld wanneer positieve en negatieve tijdzones worden overschreden. NPR-20329: Hotfix voor CQ-4219333

### Campagne {#campaign-2}

* De componenten van de Slider van de campagne verschijnen niet wanneer de Standaardervaring voor een campagne wordt gekozen. NPR-19213

### Integratie {#integration-7}

* Aangepast bestand at.js publiceert niet wanneer het wordt geopend met de anonieme gebruiker. NPR-19542: Hotfix voor CQ-4219592
* Het het richten gebied van de Motor in de config tovenaar wordt geplaatst aan ContextHub (AEM) in plaats van Adobe Target. NPR-19320: HF voor CQ-4218465
* De publiekssectie wordt beschadigd tijdens het maken van de ervaring. NPR-1910
* Het dialoogvenster Doel wordt niet weergegeven in de doelmodus wanneer een doelmodule meerdere keren wordt bewerkt en opgeslagen. NPR-19144: Hotfix voor CQ-4216708
* Toegangseigenschappen voor artikelen die onjuist zijn ingesteld in Adobe Digital Publishing Solution op klassieke UI. NPR-19367
* Onjuist gedrag van automatisch vouwen tijdens het aanpassen van aanbiedingen via Campagne als gebruikers toegang hebben tot meerdere gebieden. NPR-19290: Hotfix voor CQ-4218029

### Sites {#sites-11}

* De meervoudige samengestelde gebiedsdrop-down waarden worden niet herhaald toe te schrijven aan veranderingscode in Sidekick.js na het bevorderen van de instantie aan AEM 6.1SP2-GVB3. NPR-19450: HF voor CQ-4194771
* WCMMode.EDIT werkt niet voor beoogde componenten in de ontwerpmodus. NPR-19387
* Gepubliceerde JSON API voor het gebruik van inhoudsfragmenten. NPR-19500
* De functie Vet, cursief en onderstrepen werkt niet voor RTF-velden in het dialoogvenster Schrijver. NPR-19670: NPR-19718: Hotfix voor CQ-4219088

### Mobiel op aanvraag {#mobile-on-demand-1}

* Het renderen van problemen met de AEM artikelconsole als het gebruik van afbeeldingen op volledige grootte maakt het traag. NPR-19088

### Vertaling {#translation-5}

* Kan geen voorvertoning genereren voor vertaalprojecten. NPR-19289

### Beveiliging {#security}

* SSL-verbindingsfout. Kan geen veilige verbinding maken met de server. NPR-19628

### Gemeenschappen {#communities-9}

* De post wordt teweeggebracht op inhoud het posten met pre-gematigde plaatsen. NPR-2008
* E-mailmeldingen werken voor geen van de aan de moderator gerelateerde activiteiten met betrekking tot gepubliceerde componenten. NPR-19767: HF voor CQ-4218060

### Platform {#platform-4}

* Stabiliteitsproblemen met AEM implementatie van productieservers. NPR-19707
* Aangepaste tag lib die referentietags implementeert als script, worden niet gevonden na upgrade naar AEM 6.3. NPR-19087
* Oplossingen voor HTL-fouten voor AEM 6.3.1. NPR-19161
* RTF-veld kan niet worden bewerkt in componenten met meerdere velden. NPR-19604: Hotfix voor graniet-16755
* De service E-mailsjabloon Adoben voegt codes toe aan aangepaste gebruikerssjablonen. NPR-19190
* Hotfix voor Oak 1.6.5. NPR-19148

### Commerce {#commerce-5}

* De knop Workflow starten nadat u een XF-variatie-editor hebt geselecteerd, heeft geen effect. NPR-19642: Hotfix voor CQ-4207796

### Projecten {#projects-2}

* Projecteditors kunnen geen elementen kopiëren en plakken in de map met projectmiddelen. NPR-19619: Hotfix voor CQ-4215321

### Beheer van webinhoud {#web-content-management}

* In het scherm Uitrollen kunnen selectievakjes die overeenkomen met pagina&#39;s van Live Copy niet worden in- of uitgeschakeld. NPR-19518
* Het bulksgewijs bewerken van pagina-eigenschappen is niet correct bruikbaar, aangezien momenteel alle tabbladen en velden beschikbaar zijn voor grote versies. NPR-19451
* OOTB-eigenschappen en eigenschappen voor uitlijning van afbeeldingen worden niet weergegeven wanneer u een afbeelding bewerkt in de klassieke gebruikersinterface. NPR-19488: HF voor CQ-4217914

### Gebruikersinterface {#user-interface-4}

* Als gebruikers de Google Chrome-browser gebruiken, kunnen ze de volledige lijst met pagina&#39;s/middelen niet laden met de kolomweergave in TouchUI. NPR-19566: Hotfix voor CQ-4214248

### Brand Portal {#brand-portal-1}

* Kan geen elementen van AEM met opmerkingen en annotaties publiceren. NPR-19590: Hotfix voor CQ-4218386
* Publicatietags van AEM naar Brand Portal inschakelen vanuit de tagbeheer-/tagingconsole. NPR-20271: Hotfix voor CQ-4223948
* Het veld &quot;enabled&quot; corrigeren in de configuratiegebruikersinterface van de Brand Portal-cloudservice. Hotfix voor CQ-4211101
* Het zoeken naar formulierreplicatie mislukt. Hotfix voor CQ-420080

## Forms {#forms-11}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-11}

#### Aangepaste formulieren {#adaptive-forms-4}

* Verzenden naar JEE-workflow retourneert geen uitvoerparameter van JEE-zijde naar AEM en genereert een fout met de tekst ‘Negeren omdat de waarde niet primitief is’. NPR-20265
* Adaptieve Forms staat geen PDF als bijlage toe in Safari. NPR-19625
* RestoreGuideState overschrijft de aangepaste contextProperty-kaart. CQ-422877
* Wanneer het vormen van Google `reCaptcha` gebruikend Cloud Service, in milieu&#39;s die configuratie van org.apache.http.proxyconfigurator voor externe verbindingen vereisen, schijnen de vraag van de POST niet door PROXY te gaan. NPR-20454
* Adaptieve Forms op basis van XSD-schema&#39;s verzendt onjuiste XML-waarden voor numerieke velden in installaties met landinstellingen met een ander decimaalteken dan punt (.) resulteert in fouten. NPR-2044
* Proxyinstellingen die zijn ingesteld voor &#39;Apache HTTP Components Proxy Configuration&#39; worden niet ondersteund wanneer een HTTP-aanvraag wordt ingediend bij een externe server. De onderbrekingskwesties van de verbinding gebruikend de vraag van de GET of van de POST van HTTP. NPR-20457, 20456, NPR-20455, NPR-20451

#### Forms-gegevensintegratie {#forms-data-integration}

* UTF-8-tekens als uitvoer van SOAP service worden niet correct gekopieerd naar Adaptieve Forms-velden voor niet-Engelse landinstellingen. NPR-20238: NPR-20103

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
* Tekstveld met meerdere regels (TextArea) behoudt geen nieuwe regeltekens of teksteinden na het verzenden van gegevens in HTML Workspace. NPR-20085

#### Procesrapportage {#process-reporting}

* Bij het rapporteren van processen worden gegevens niet correct opgehaald vanwege de null pointer-uitzondering. NPR-19759

>[!NOTE]
>
>Installeer het LiveCycle inbedden pakket dat in het [ wordt vermeld AEM Forms geeft ](aem-forms-releases.md) artikel vrij om de kwestie te bevestigen.

#### Standaardservices {#standard-services}

* docConvertor ondersteunt geen transparanties voor afvlakking in PDF en produceert geen PDF/A. NPR-16228: Hotfix voor CQ-4214488

#### Kern {#core-2}

* Wanneer AEM Forms Server die wordt uitgevoerd in een clusterconfiguratie in een JBoss®-toepassing wordt gestopt, wordt de verbinding van de toepassingsserver met de database verbroken. Dit kan leiden tot problemen met gegevensbeschadiging. NPR-19724

### Inclusief functiepakketten {#feature-packs-included-1}

* Het veld Metagegevensschema in de vervolgkeuzelijst kan niet verplicht worden gesteld, omdat validatie in verplichte velden ontbreekt voor elementen. NPR-17882: FP voor CQ-4208373

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
* Opgeloste problemen met validatie van inhoudsfragmenten
* Verbeterde bewerkbaarheid van metagegevensschema&#39;s op hybride apparaten
* Opgeloste problemen met synchronisatie op componentniveau in live kopieën
* Verbeterde bruikbaarheid van pagina&#39;s met veel inhoud in de kolomweergave
* Verbeterde compatibiliteit met de naamgevingsconventie voor pagina&#39;s met lange titels
* Verbeterde functionaliteit voor het aanpassen van campagnes op Touch UI
* Oplossingen voor verschillende projectoverlayproblemen

### Platform {#platform-5}

* Hotfix voor Oak 1.6.2. NPR-16993
* Wanneer u de zoekopdracht opent met een filter, wordt het pad niet meer ingesteld. NPR-17398: Hotfix voor CQ-4204870
* Verplichting voor de controleerbaarheid van wijzigingen in de gebruikerstoestemming in AEM. NPR-17061
* Lingingerverbindingen met DM-Cloud Servicen die uitzonderingen op &quot;Te veel geopende bestanden&quot; veroorzaken. CQ-421407

### Assets {#assets-12}

* Gebruiksproblemen met het configureren van services voor slimme inhoud met verschillende opties. NPR-18200: Hotfix voor CQ-4201557
* Het weglekken van middelen in binaire stromen aan S3 datastore. NPR-18041: Hotfix voor CQ-4209506
* Er treedt een fout op wanneer een tekstbestand met ASCII/UTF-8-codering naar AEM Assets wordt geüpload en het genereren van miniaturen mislukt. NPR-18006: GVB voor CQ-4209345
* Standaardmetagegevensschema veroorzaakt validatiefout van inhoudsfragment. NPR-17769: Hotfix voor CQ-4211111
* Niet-afgesloten resource resolver in com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: GVB voor CQ-4209018
* Verzoek om veelvoudige replicatieagenten voor het publiceren van activa aan Brand Portal te creëren. NPR-17189
* De taak van het overzicht voor activa onder de Japanse taalomslag werkt niet. CQ-4204782
* Een null pointer-uitzondering treedt op wanneer een element wordt verplaatst van de eigenschappenpagina. CQ-4204251
* AEM kan volgende verwijzingen naar een element op de eigenschappenpagina niet bijhouden als het meerdere keren is gekoppeld aan een InDesign-document. CQ-4204186
* Problemen met het toevoegen van nieuwe tabbladen in het formulier Metagegevensschema wanneer dit wordt bewerkt in Chrome op hybride apparaten. CQ-42018-10
* Wanneer dubbele elementen worden geüpload, wordt de optie (verwijderen/behouden) op alle elementen toegepast, zelfs als deze optie niet is geselecteerd in het dialoogvenster Gedetailleerde duplicaten. CQ-4201673
* Een null pointer-uitzondering wordt weergegeven wanneer een elementmap met meer dan 150 binnenkomende verwijzingen wordt verplaatst. CQ-4200981
* Als er een conflict optreedt bij het uitpakken van de inhoud van het ZIP-bestand, wordt voor een gedownloade elementmap de standaardoptie weergegeven als versie Maken in plaats van beide. CQ-97800
* Gebruikers met de machtiging Alleen-lezen kunnen geen voorvertoning van inhoud weergeven via AEM Mobile-inhoudsbeheer. NPR-17486: GVB voor CQ-4209690
* De knop Catalogus maken werkt niet in de kolomweergave in de Catalogusconsole. CQ-4209952

### Sites {#sites-12}

* Problemen met het insluiten van afbeeldings-/videocomponenten door middel van kenmerk data-smart-resource. NPR-18182: GVB voor CQ-4212100
* Gewijzigde gelokaliseerde componenten worden niet teruggezet naar hun oorspronkelijke vorm wanneer de overerving opnieuw wordt toegepast in een LiveCopy. NPR-18172: Hotfix voor CQ-4211379
* Problemen met het navigeren door een pagina met veel inhoud in de kolomweergave in Touch UI. NPR-17799: Hotfix voor CQ-4199611
* Niet-afgesloten resource resolver in `com.day.cq.wcm.core.impl.VersionManagerImpl` . NPR-17789: GVB voor CQ-4211152
* De paginanaam wordt niet gegenereerd volgens de conventie voor lange paginatitels. NPR-17633: Hotfix voor CQ-4209056
* Problemen met het maken van pagina&#39;s via Touch-gebruikersinterface in AEM 6.3 geïmplementeerd op JBoss® EAP 6.4. NPR-17589: Hotfix van CQ-4210137
* De workflowstatusprovider zorgt ervoor dat de instantie wordt vergrendeld wanneer geneste groepen aanwezig zijn. NPR-17556: GVB-verzoek voor CQ-4202056
* Niet-afgesloten resourceoplosser in de volgende objecten:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: GVB voor CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: GVB voor CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: GVB voor CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: GVB voor GRANITE-17404

### Integrations {#integrations-1}

* Opgeloste AEM de componentenfouten van het Onderzoek die kunnen voorkomen wanneer AEM Cliënt 3.1 van HTTP van Dag OSGI met een Volmacht wordt gevormd die de Authentificatie van de Samenvatting vereist. NPR 18128: Hotfix voor NPR-18029
* Kwesties met het personaliseren van campagnes en bijbehorende ervaringen door middel van Klassieke UI. NPR-18127: Hotfix voor CQ-4211559
* Wanneer u een merk/zone instelt op een hoofdpagina van een site, kan overerving na annulering niet worden hersteld voor Gebieden in subpagina&#39;s. NPR-17753: Hotfix voor CQ-4210139

### Workflow {#workflow-3}

* In een niet-transiënte workflow worden de procesgeschiedenis en wijzigingen in metagegevens die vóór een externe processtap zijn aangebracht, niet voortgezet. NPR-17848: Hotfix voor GRANITE-17757
* Waarden uit de dialoogvenstervelden van de workflow blijven niet behouden in het werkitemknooppunt. NPR-17734: Hotfix voor CQ-4210369
* Onscheidbare datumfout treedt op wanneer u een taak bewerkt vanuit het Postvak IN. CQ-4208749

### Projecten {#projects-3}

* Oplossingen voor verschillende projectoverlayproblemen. NPR-1773
* Herstructurering van de pods in de projectmodule maakt het minder configureerbaar. CQ-4209859
* Het pad naar elementen verandert in de respectievelijke gelokaliseerde sites wanneer pagina&#39;s worden toegevoegd aan de vertaaltaak. CQ-4206/07

### Beveiliging {#security-1}

* Problemen met het uploaden van avatar-afbeeldingen voor LDAP-gebruikers. NPR-16561
* Verzoek om een geüpgrade versie van org.apache.sling.servlets.post servlet (2.3.22) in de Apache Sling API te gebruiken om een XSS-kwetsbaarheid te voorkomen. NPR-18963

## Forms {#forms-12}

AEM Forms-oplossingen worden geleverd via het Forms-invoegpakket en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

De belangrijkste markeringen voor AEM Forms zijn:

* Oplossingen in de modules van de de tekstbeheerstekst van het correspondentiebeheer, Voorproeven van de Brief, en programmatic lancering om een brievenbeheer UI tot stand te brengen.
* Oplossingen voor PDF/A-1b-validatie, conversie van grote afbeeldingsbestanden naar PDF en PDF-documenten in de Japanse taal in PDF Generator.
* Oplossingen voor bruikbaarheid voor correspondentiebeheer, Documentbeveiliging en Forms Workflow.
* Extra ondersteuning voor het vastleggen van auditgebeurtenissen voor het handtekeningveld voor scripts.

### Forms-invoegtoepassing {#forms-add-on-package-12}

**het Beheer van de Correspondentie**

* Bij het bewerken van een correspondentiebeheerfragment worden in de Teksteditor inline voorwaarden weergegeven, samen met de verwerkte tekst. CQ-421930
* Bij het maken van een brief voor correspondentiebeheer wordt de beschrijving van de brief niet opgeslagen. NPR-18089
* De extra marge boven en onder een lijst met opsommingstekens is zichtbaar in de Teksteditor, maar niet in de uitvoering HTML en PDF. NPR-18126
* Wanneer HTML submit de methode van de POST gebruikte, creeer correspondentie UI niet om te lanceren. NPR-18202
* Wanneer een tekstmodule wordt opgeslagen en een expressie in de tekstmodule geen openings- of afsluitende expressietags bevat, wordt geen foutbericht weergegeven. In de tekstmodule wordt een foutbericht weergegeven en kan de letter niet worden weergegeven. NPR-18535
* Wanneer nieuwe inhoud wordt toegevoegd of op de toets `Enter` wordt gedrukt, wordt een label voor div toegevoegd aan de tekstmodule. NPR-18240

**Assembler**

* Bij het valideren van een PDF-document voor compatibiliteit met PDF/A-1b retourneert AEM Forms een validatiefout: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. Het PDF-document retourneert de fout niet wanneer deze wordt gevalideerd met Adobe Preflight en software van derden. NPR-18011
* Bij het valideren van PDF-documenten voor compatibiliteit met PDF/A-1b retourneert AEM Forms een validatiefout: formulierveld heeft meerdere weergaven. De PDF documenten zijn compatibel met PDF/A-1b. NPR-18013

**Controlemap**

* Als u tijdens het maken van een controlemap selecteert of u bestanden wilt verwerken met een workflow, wordt de keuzelijst van het workflowmodel afgekapt weergegeven. NPR-17566

**HTML5 Forms**

* AEM Forms legt geen controlegebeurtenissen vast voor het veld Scripthandtekening. NPR-15286

**de Manager van Forms**

* De gebruikersinterface van AEM Forms bevat alle elementen in de oudste eerste volgorde. Gebruikers kunnen de middelen niet opnieuw rangschikken in de nieuwste eerste volgorde. NPR-18450

**Java™ API Verwijzing**

JavaDocs toegevoegd voor de klasse com.adobe.livecycle.content. NPR-18468

### Forms JEE-installatieprogramma {#forms-jee-installer-11}

**PDF Generator**

* De service PDF Generator converteert afbeeldingen die groter zijn dan 100 MB niet naar PDF-documenten. CQ-4208628
* Bij het gebruiken van de dienst van de PDF Generator met Japanse Taal OCR, wordt een omgekeerde PDF geproduceerd. NPR-17602

**Beheer van het Proces**

* De TaskContext-variabele wordt niet gevuld voor AEM Forms-processen. NPR-18199

**Veiligheid van het Document**

* Microsoft® Excel en Microsoft® PowerPoint hebben meer tijd nodig om de documenten te openen die zijn beveiligd met AEM Document Security Extension voor Microsoft® Office. CQ-4212358
* Wanneer een nieuw beleid wordt gecreeerd en een beleid met de zelfde naam zoals bestaand, komt een interne serverfout voor. NPR-18247

## Functiepakketten inbegrepen {#feature-packs-included-2}

* Verplichting voor de controleerbaarheid van wijzigingen in de gebruikerstoestemming in AEM. NPR-17061

AEM Cumulatief Fix Pack 6.3.0.1 is een belangrijke update die verscheidene interne en klantenfixes omvat sinds de algemene beschikbaarheid van AEM 6.3 in April 2017. De belangrijkste kenmerken van het AEM Cumulative Fix Pack zijn:

* Verbeteringen op de volgende gebieden:

   * Inhoudsfragmenten, Sites en de Rich Text Editor, Regeleditor en Sjablooneditor
   * Sociale revisie en aanmelding bij Facebook
   * Vertaaltaken configureren en starten
   * Reactietijd voor toegang tot meldingen in sociale gemeenschappen
   * Weergave van controletaken in de DAM-gegevensopslagruimte

* Verstrekt bevestigingsoptie in de Manager van het Pakket voor het ontdekken van conflicten tussen bekleding en GFP

## Instructies voor gestreken fijn papier downloaden via softwaredistributie {#download-instructions-for-cfp-via-package-share}

U kunt het pakket van GFP van [ Distributie van de Software direct downloaden ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) of de volgende stappen uitvoeren:

1. Open [ Distributie van de Software ](https://experience.adobe.com/downloads). U hebt een Adobe ID nodig om u aan te melden bij de softwaredistributie.
1. Tik **[!UICONTROL Adobe Experience Manager]** beschikbaar in het koptekstmenu.
1. Tik op de pakketnaam, selecteer **[!UICONTROL Accept EULA Terms]** en tik op **[!UICONTROL Download]** .

## Installatie-instructies {#installation-instructions}

Deze sectie doorloopt u door de vereisten en de stappen om GVB te installeren.

### Voordat u gaat installeren {#before-you-install}

>[!NOTE]
>
>Optionele functiepakketten die door de Adobe worden geleverd, zijn afhankelijk van de releaseversie en het Cumulative Fix Pack. Als u om het even welk Pak van de Eigenschap geïnstalleerd hebt, contacteer het [ team van de Zorg van de AEM van de Klant ](https://experienceleague.adobe.com/?support-solution=General#support) om de verenigbaarheid met dit Cumulatieve Pak van de Fix voor AEM 6.3 te bevestigen.

>[!NOTE]
>
>Adobe raadt u aan validatie uit te voeren voor elk nieuw installatiepakket voordat u probeert het pakket te installeren. Vóór de validatie worden eventuele fouten die vóór de installatie zijn gevonden, geanalyseerd en gerapporteerd en worden gebruikers proactief gewaarschuwd voor dergelijke fouten.
>
>U kunt tot documentatie voor de Valideren optie toegang hebben in [ https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)

* AEM 6.3.3.0 is een voorwaarde voor het GVB. Zie de [ Documentatie van de Verbetering ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) voor gedetailleerde instructies over de bevordering van een AEM installatie aan AEM 6.3.
* Voor een clusterplaatsing die RDBMK of MongoDB gebruikt, kan het pakket van GFP op om het even welke instanties van de Auteur worden geïnstalleerd die de Manager van het Pakket gebruiken.
* Voordat u het Cumulative Fix Pack installeert, moet u zorgen dat u een momentopname maakt of een back-up maakt van uw AEM.
* Het verwijderen van het GVB wordt niet ondersteund.

### Nieuwe loggers toevoegen {#adding-new-loggers}

Om zuivert niveau registreren te vormen en een activiteitenlogboek tijdens installatie van SPs/GVBs terug te winnen, kunt u de hieronder stappen volgen:

* U kunt een registreerapparaat bij de standaardplaats [ http://localhost:4502/system/console/slinglog ](http://localhost:4502/system/console/slinglog) met de hieronder eigenschappen toevoegen:

   * Logniveau: foutopsporing
   * Additief: false
   * Logbestand: logs/activity.log
   * Logger: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

Activity.log wordt gecreeerd in crx-quickstart /logs omslag.

### Installeer het Cumulative Fix Pack via Software Distribution {#install-the-cumulative-fix-pack-via-package-share}

1. Klik de [ verbinding van de Distributie van de Software ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) zodat kunt u het pakket downloaden.

1. Open [ Manager van het Pakket ](http://localhost:4502/crx/packmgr/index.jsp) en klik **[!UICONTROL Upload Package]** om het pakket te uploaden.

1. Selecteer de pakketnaam en klik op **[!UICONTROL Install]** .

### Automatische installatie {#automatic-installation}

Het GVB kan automatisch in een lopende instantie op de volgende manieren worden geïnstalleerd:

* Plaats het pakket in `../crx-quickstart/install` terwijl de server wordt uitgevoerd. Het pakket wordt automatisch geïnstalleerd.
* Gebruik [ HTTP API van de Manager van het Pakket ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) - zorg ervoor dat u `cmd=install&recursive=true` gebruikt - zodat wordt het genestelde pakket geïnstalleerd.

### Installatie valideren {#validate-installation}

1. Op de pagina Productinformatie ( `/system/console/ productinfo` ) wordt nu de bijgewerkte versie van de tekenreeks &quot;Adobe Experience Manager, versie 6.3.3.8&quot; onder Geïnstalleerde producten weergegeven.
1. Alle OSGI-bundels zijn actief of FRAGMENT in de OSGI-console (Webconsole gebruiken: `/system/console/bundles`).

>[!NOTE]
>
>Bij succesvolle installatie van het pakket, verschijnt een informatiebericht op foutenlogboeken erop wijzend dat het inhoudspakket met succes, zoals &quot;het Pakket van de Inhoud **AEM-6.3.3-Cumulatief-Fix-pak-7** geïnstalleerd met succes heeft geïnstalleerd.&quot;

>[!NOTE]
>
>Sinds AEM 6.3.3.1 is het logniveau in Jackrabbit FileVault voor de meeste berichten veranderd van INFO in DEBUG. Als u installatielogboeken wilt verkrijgen voor een inhoudspakket dat is geïnstalleerd op AEM 6.3.3.1 of hoger, schakelt u het DEBUG-logniveau in voor org.apache.jackrabbit.vault.packaging.impl.

### AEM Forms installeren {#install-aem-forms}

>[!NOTE]
>
>Sla deze sectie over als u AEM Forms niet gebruikt.

#### AEM Forms-invoegtoepassing installeren {#install-forms}

1. Controleer of u het AEM 6.3.3.x-pakket voor gestreken fijn papier hebt geïnstalleerd.
1. Download het overeenkomstige Forms toe:voegen-op pakket dat bij [ wordt vermeld de versies van AEM Forms ](aem-forms-releases.md) voor uw werkend systeem.
1. Installeer het toe:voegen-op pakket van Forms zoals die in [ wordt beschreven het Installeren AEM vormen toe:voegen-op pakketten ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

#### AEM Forms JEE-bundelpakket installeren {#install-aem-forms-jee-bundles-package}

Correcties in AEM Forms JEE worden geleverd via een afzonderlijk installatieprogramma. Voor informatie over het installeren van GFP op AEM Forms op JEE, zie [ Installing GFP op AEM Forms JEE ](install-cfp-aem-forms-jee.md).

#### Forms Designer-installatieprogramma {#designer-installer}

1. Als u de update wilt installeren, voert u het bestand Designer 6.2.0_&lt;Language>_Cumulative_QF.msp uit.
1. Voor het welkomstscherm, klik **update**. De installatie wordt gestart.
1. Nadat de installatie voltooit, klik **beëindigen**.

## Configuratie-instellingen voor AEM Forms JEE (JBoss® EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Als u 6.3.3.0 of recentere versies installeert, voer de volgende procedure uit om montages voor de JBoss® toepassingsserver te vormen. Als u 6.3.3.0 installeert op AEM Forms Server die op de toepassingsservers van WebLogic of IBM® WebSpehere van het Oracle wordt uitgevoerd, wordt geen extra configuratie vereist. Voor verdere details, zie [ AEM 6.3.3.0 de Nota&#39;s van de Versie ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

## Configuratie-updates voor Search&amp;Promote-integratie {#configuration-updates-for-search-promote-integration}

Met AEM Cumulatieve die Pak 6.3.0.2 van de Fix en recentere versies, de configuratie OSGi voor de Integratie van de Search&amp;Promote wordt gebruikt is **Configuratie van de Volmacht van HTTP van de Componenten Apache**. De proxyconfiguratie van Day Commons HTTP Client 3.1 wordt niet meer gebruikt.

## Bekende problemen {#known-issues}

* De volgende fouten en waarschuwingen kunnen optreden tijdens de installatie van AEM GVB 6.3.3.x en kunnen veilig worden genegeerd:

   * &#42; WARN &#42; [ OsgiInstallerImpl ] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallaak-0.0.2-jar-with-dependences.jar verpletterde uitzondering.
   * &#42; FOUT &#42; [ OsgiInstallerImpl ] com.adobe.cq.social.cq-social-jcr-provider [ com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl (2174) ] Onderbreking wachtend op registratieverandering om unregistration te voltooien. 4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl service ServletResolver ontbreekt, kan geen serviceaanvragen verzenden, status 503 verzenden
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: kan resource [ /bin/receive ] niet controleren, paginanummer niet beschikbaar
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: Het aanroepen van de fouthandler heeft een fout tot gevolg
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Oorspronkelijke fout null
   * org.apache.sling.engine.impl.DefaultErrorHandler Error-handler mislukt:java.io.IOException
   * &#42; FOUT &#42; [ FelixDispatchQueue ] com.day.cq.dam.cq-dam-core FrameworkEvent FOUT (org.osgi.framework.ServiceException: De fabriek van de dienst keerde ongeldig terug. (Component: com.day.cq.dam.handler.standard.ps.PostScriptHandler)

**Brand Portal**

* Vanaf 6.3.1.2 is de knop Publish naar Brand Portal voor slimme verzamelingen verwijderd.

**Gebruikersinterface**

>[!NOTE]
>
>Voor het geval u met om het even welk van deze twee kwesties wordt beïnvloed, contacteer [ AEM de Zorg van de Klant ](https://experienceleague.adobe.com/?support-solution=General#support).

* Een hoog CPU-gebruik wordt waargenomen als gevolg van veel verzoeken in de zoekfunctie van Admin. NPR-2429
* PathField wordt niet geselecteerd in pathBrowser wanneer het heropenen van de component. NPR-2417

## Voor NPR-27692 vereiste configuratie-instellingen {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Deze configuratie-instelling is van toepassing op GVB 6.3.3.2 en hoger. Hiermee wordt u gevraagd de eigenschappen van de opstartdelegatie bij te werken in het eigenschappenbestand van `sling` .properties.

Voer de onderstaande stappen uit om wijzigingen in adobe-LiveCycle® cq -author.ear/ cq.war handmatig bij te werken:

* Stop de AEM server.
* Ga naar adobe-livecycle-cq.ear/cq.war
* Open adobe-livecycle-cq.ear/cq.war/WEB-INF/web.xml voor bewerking:

   * werk **sling.bootDelegatie.ibm** param-name waarde met bij:

   * `com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat`

   * Na de bovenstaande wijziging moet de init-param er als volgt uitzien:

     &lt;init-param>
&lt;param-name>sling.bootDelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>
&lt;/init-param>

* Verwijder het vorige dossier van het ondernemingsarchief (EAR) van de WebSphere® toepassingsserver en installeer het bijgewerkte dossier van het EAR na de stappen in Sectie 10.2 van [ https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Sla het bestand op en start de server opnieuw. [ https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Voor NPR-23208 vereiste configuratie-instellingen {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Deze configuratie-instelling is van toepassing op 6.3.2.2 en hoger. Het geeft u de opdracht om het beleid van de Lijsten van het Toegangsbeheer (ACL) manueel door CRX-DE bij te werken aangezien ACLs niet door de installatie van GFP toe te schrijven aan &quot;merge_preserve&quot;acHandling wordt bijgewerkt.

**Documentatie voor het toevoegen van ACL beleid manueel**

Om ACL beleid bij te werken, voeg de hieronder controles van de Toegang door CRX-DE toe:

`1)` Op pad &quot;/content&quot;
`a)` Principal : reference-adjustment-service
Type: Toestaan
Rechten : jcr:read, jcr:modifyProperties
Beperkingen : rep:glob=&quot;/&#42;/jcr:content&quot;
`b)` Principal : reference-adjustment-service
Type: Toestaan
Rechten : jcr:read, jcr:modifyProperties
Beperkingen : rep:glob=&quot;/&#42;/jcr:content/&#42;&quot;

`2)` Op pad &quot;/content/usergenerated&quot;
`a)` Principal : reference-adjustment-service
Type: Toestaan
Rechten: `jcr:write`

`3)` Op pad &quot;/etc&quot;
`a)` Principal : reference-adjustment-service
Type: Toestaan
Rechten : jcr:read, jcr:modifyProperties
Beperkingen : rep:glob=&quot;/&#42;/jcr:content&quot;
`b)` Principal : reference-adjustment-service
Type: Toestaan
Rechten : jcr:read, jcr:modifyProperties
Beperkingen : rep:glob=&quot;/&#42;/jcr:content/&#42;&quot;

## Voor NPR-19450 vereiste configuratie-instellingen {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Deze configuratie-instelling is van toepassing op GVB 6.3.1.1 en hoger.

**vorm het bezit CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

De eigenschap bepaalt de maximale diepte van de knoopsubstructuur onder het knooppunt page ` /jcr:content` , tot welke knooppunten in de repository worden gebruikt voor het ophalen van de pagina-eigenschappen. Alle knooppunten die zich onder de opgegeven diepte in deze eigenschap bevinden, worden genegeerd.

De standaardwaarde is 1. Hef de waarde op door het bestand constants.js (`/libs/cq/ui/widgets/source/constants.js`) te bedekken zonder opmerkingen over de eigenschap `CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL` . Vervolgens wijst u er de vereiste waarde aan toe (de maximale diepte onder de pagina `/jcr:content` die de gegevens van de pagina-eigenschappen bevat).

**als de gebruiker veelvoudige paginakarakters moet tot stand brengen dusdanig dat het aantal knopen onder de 1} knoop van de pagina groter wordt dan 1000, gebruik de volgende stappen om configuratieveranderingen te doen:**`/jcr:content`

* Configureer de eigenschap JSON Max-resultaten van Apache Sling.
* Get Servlet using `/system/console/ configMgr`.
* Stel de waarde ervan in op een getal > 1000 (de huidige standaardwaarde), zodat dit getal groter is dan het totale aantal knooppunten in de substructuur `/jcr:content` totdat de hierboven geconfigureerde diepte wordt bereikt.

Hierdoor kan de sling GET servlet alle vereiste knooppunten retourneren.

## Uber Jar {#uber-jar}

De Uber Jar voor 6.3.3.8 is beschikbaar bij de Adobe Public Maven repository

Om Uber Jar in een Geweven project te gebruiken, zie [ hoe te Jar van Uber ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) gebruiken en het volgende gebiedsdeel in uw projectPOM omvatten:

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

Deze sectie bevat een lijst met functies en mogelijkheden die zijn verwijderd of vervangen uit AEM 6.3.

| Gebied | Functie | Vervanging | Versie |
|----|-----|-----|-----|
| Integratie van Assets en Adobe Creative Cloud | [ AEM aan het delen van de omslag van het Creative Cloud ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) werd geïntroduceerd in AEM 6.2 als manier om creatieve gebruikers toegang tot activa van AEM te geven. Een nieuw vermogen dat in de toepassing van het Creative Cloud, de Verbinding van Activa van de Adobe wordt vrijgegeven, verstrekt een betere gebruikerservaring. Het biedt ook een krachtigere toegang tot middelen van AEM rechtstreeks vanuit Photoshop, InDesign en Illustrator.</br></br> Adobe maakt geen verdere verbeteringen in de mogelijkheid om mappen te delen. Terwijl de functie in AEM is opgenomen, wordt klanten aangeraden de vervangende functie te gebruiken. | Adobe Asset Link of Desktop App. Voor meer info, zie het [ AEM de integratie van het Creative Cloud ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) artikel. | AEM 6,3,3 x |

## OSGi-bundels en inhoudspakketten inbegrepen {#osgi-bundles-and-content-packages-included-1}

De volgende tekstdocumenten maken een lijst van de bundels OSGi en de Pakketten van de Inhoud inbegrepen in GVB.

* [Lijst van OSGi-bundels opgenomen in AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Lijst van inhoudspakketten opgenomen in AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [ AEM versies en updates ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [ AEM 6.3 hotfixes pagina ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [ AEM 6.3 versienota&#39;s ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [ AEM productpagina ](https://business.adobe.com/products/experience-manager/adobe-experience-manager.html)
>* [ AEM 6.3 documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* Abonneren op [ de Prioritaire productupdates van de Adobe ](https://www.adobe.com/subscription/priority-product-update.html)
