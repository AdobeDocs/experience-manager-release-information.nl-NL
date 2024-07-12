---
title: AEM 6.2 Cumulatieve Fix Pack
description: Meer informatie over de opmerkingen bij de AEM 6.2 Cumulative Fix Pack-release.
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '21044'
ht-degree: 0%

---

# AEM 6.2 Opmerkingen bij de release Cumulative Fix Pack{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived by way of UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Gegevens vrijgeven {#release-information}

| **Product** | Adobe Experience Manager |
|---|---|
| **Versie** | 6,2 |
| **Versie** | Cumulatief Fix Pack 6.2 SP1-GVB20 |
| **Vereiste** | [ AEM 6.2 Service Pack 1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **Algemene beschikbaarheid** | 6 juni 2019 |

### Cumulatief reparatiepakket {#cumulative-fix-pack}

De Adobe introduceerde één-leveringsmodel voor het vrijgeven van moeilijke situaties. In plaats van hotfixes voor individuele kwesties vrij te geven, geeft de Adobe nu een Cumulatief Pak van de Correctie (GVB) elke maand (onderworpen aan het overgaan kwaliteitscontroles) vrij. Een gestreken gemeenschappelijk visserijbeleid is een geaggregeerd inhoudspakket voor veelvoudige moeilijke situaties. GFPs omvat hoofdzakelijk insectenmoeilijke situaties maar zou ook de Pakken van de Eigenschap kunnen omvatten. Ze hebben de volgende voordelen ten opzichte van afzonderlijke hotfix-releases:

* Gecumuleerd van aard (een GVB bevat bijvoorbeeld vastleggingen die via eerdere GVB&#39;s zijn geleverd)
* Meer kwaliteitsborging
* Vereenvoudigde installatie (de gebruiker installeert een gestreken fijn-wit als één enkel pakket dat geen gebiedsdelen, behalve het recentste de dienstpak heeft)

Voor meer informatie over GFP en andere soorten versies, zie {het Voertuig van de Versie van het 0} Onderhoud ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).[

## Over de release {#about-the-release}

AEM Cumulatief Pak 6.2 SP1-GVB20 van de Moeilijke situatie is het laatste Cumulatieve Pak van de Fix voor AEM 6.2 en is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van [ AEM 6.2 SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) worden vrijgegeven.

>[!CAUTION]
>
>Het toepassen van GVB zonder verenigbaarheid tussen de geïnstalleerde Packs van de Eigenschap te bevestigen kan in systeemmislukking of verlies van douaneconfiguraties resulteren, die van steun zouden kunnen vereisen om te herstellen.

>[!NOTE]
>
>* Een nieuwe bundel `discovery- api` Sling Johnzon 1.0.0 is inbegrepen met AEM Cumulative Fix Pack 6.2 SP1-GVB10. Bovendien wordt een gebruiker van de dienstgebruiker sling-Discovery toegevoegd met lees en schrijf voorrechten voor de knoop */var/discovery* in de bewaarplaats van CRX.
>
>* De e-mailbundel van Apache komt **org.apache.commons/commons-email/1.5** is toegevoegd die **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002** vervangt.
>
>* Adobe raadt u aan om gestreken fijn papier in te zetten in de installatiemap voor klanten die AEM veel gebruikers hebben.
>

## Ingesloten problemen {#issues-included}

In deze sectie worden alle problemen en hotfixes vermeld die in het huidige GVB zijn opgenomen.

Bovendien omvat dit GFP hotfixes die in [ vorige cumulatieve fixpakken ](#previous) worden geleverd.

### Integratie {#integration}

* Het steunen van veelvoudige Campagne gericht op verpersoonlijkingsverbeteringen. NPR-29163: Hotfix voor CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler gaat in een oneindige lijn en veroorzaakt updates aan knopen op publicatieinstanties. NPR-28561: Hotfix voor CQ-4263096

### DAM - Algemeen {#dam-general}

* Kan de replicatieknop voor gebruikers die geen beheerder zijn, niet weergeven/verbergen in specifieke dammappen. NPR-29026: Hotfix voor CQ-4265361

### Kwetsbaarheid {#vulnerability}

* Het CSRF-beschermingskader werkt niet met AEM stichtingsvormen. NPR-28612: Hotfix voor GRANITE-22231

### Forms {#forms}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package}

>[!NOTE]
>
>Voor AEM Forms-klanten is het van essentieel belang dat het invoegpakket voor AEM Forms wordt geïnstalleerd nadat AEM Service Pack, Cumulative Fix Pack of Feature Pack zijn geïnstalleerd.

>[!NOTE]
>
>AEM Forms add-on pakketten helpen de formulierfunctionaliteit uit te lijnen met AEM servicepacks en Cumulatieve Fix Packs. Daarom is het noodzakelijk om AEM insteekmodules te installeren nadat u een AEM Service Pack, Cumulative Fix Pack of Feature Pack hebt geïnstalleerd.

#### Adaptieve Forms {#adaptive-forms}

* Gebruiksproblemen met krabbelonderdelen voor iOS 12.1-apparaten. NPR-29082: Hotfix voor CQ-4261765

#### Forms - Documentbeveiliging {#forms-document-security}

* Wanneer alle handtekeningen in een PDF worden gecontroleerd met behulp van PDF Advanced Electronic Signatures (PAdES), wordt InvalidOperationException gegenereerd. NPR-27848: Hotfix voor CQ-4244837

#### Forms - Correspondentie {#forms-correspondence}

* Als de letter als PDF wordt voorvertoond, wordt in het tekstveld op de primaire pagina de waarde die is ingevoerd op het tabblad Gegevens of op basis van de opgegeven gegevenskoppeling, niet gerespecteerd. NPR-29239: Hotfix voor CQ-4266856.

#### Forms - Interactieve communicatie {#forms-interactive-communication}

* Wanneer een apostrof-teken wordt toegevoegd, worden de voorgevulde velden in de letter weergegeven als ASCII-tekens in plaats van als gewone alfabeten. NPR-28863: Hotfix voor CQ-4262900

### Forms JEE Installer {#forms-jee-installer}

* Geen nieuwe oplossingen in AEM Forms JEE-installatieprogramma.

## Hotfixes en de Pakken van de Eigenschap inbegrepen in vorige Cumulatieve Pakken van de Moeilijke situatie {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulatief Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulatief Pak 6.2 SP1-GVB19 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van [ AEM 6.2 SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Ondersteuning ingeschakeld voor MS® Translator API v3.0-ondersteuning tot AEM 6.2
* Logbericht toegevoegd na de succesvolle installatie van het pakket voor alle SPs, GVBs, en HFs.

### Assets {#assets}

* U kunt de naam van een DAM-map niet wijzigen als de machtiging ACL bewerken ontbreekt. NPR-27555: Hotfix voor CQ-104652
* Het gereedschap Voorinstellingseditor voor afbeeldingen reageert niet in 6.2.1 GVB 17 en hoger. NPR-28147: Hotfix voor CQ-4261041

### Sites {#sites}

* De koppelingencontrole voltooit de taak niet en zit vast met koppelingen die niet reageren. NPR-27373: Hotfix voor CQ-4256030
* Het segmentbestand wordt niet correct geladen vanwege een extra hoofdpad dat het pad van het segment verbreekt. NPR-28014: Hotfix voor CQ-4260332

### Integratie {#integration-1}

* LiveCopy-overervingsannulering werkt niet goed bij doelcontainers. NPR-28129: Hotfix voor CQ-4259813
* `cq:actions` wordt niet in overweging genomen voor een doelcomponent. NPR-27616: Hotfix voor CQ-4257497

* De weergave van pictogrammen voor het verbreken van overerving is niet consistent. NPR-27671: Hotfix voor CQ-4257779

### Felix {#felix}

* De componentendetail van de console van het Web ontbreekt met 500 na de installatie van GFP 18 op AEM 6.2 SP1 instantie. NPR-28350: Hotfix voor CQ-4261095

### Vertaling {#translation}

* Ondersteuning voor MS® Translator-service inschakelen in AEM 6.3 na upgrade van MS® Translator naar API v3.0. NPR-28123: Hotfix voor CQ-4259096

### UI - Foundation {#ui-foundation}

* De kalender van OTB-sites bevat onjuiste datums. NPR-28392

### Graniet {#granite}

* Woordenboek wordt niet ongeldig gemaakt voor bronnenbundels die `sling:basename` gebruiken. NPR-27624

### Sustenance {#sustenance}

* Logboeken van de de activiteit van de Manager van het pakket zouden in een afzonderlijk logboekdossier moeten worden gehaald. NPR-27323: Hotfix voor graniet-14866
* Een gestandaardiseerde uitdrukking/formulering/loglijn(en) in error.log die moet worden weergegeven wanneer de installatie is voltooid. NPR-27835
* De insteekmodule voor het granietpakket kiest afhankelijkheid van een lagere versie van org.apache.sling.i18n. Hotfix voor CQ-4263245
* com.adobe.cq.com.adobe.cq.ui.commons-bundel wordt verwijderd bij de installatie van het nieuwste GVB na 6.2SP1-GVB15. Hotfix voor CQ-4258808

### Forms {#forms-1}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-1}

#### Adaptieve Forms {#adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27843: Hotfix voor CQ-4257315

### Forms JEE Installer {#forms-jee-installer-1}

* Geen nieuwe oplossingen in AEM Forms JEE-installatieprogramma.

### SDAB-pakketten en -inhoudspakketten {#osgi-bundles-and-content-packages-included}

In de volgende tekst wordt de lijst met OSGI-bundels en -inhoudspakketten in het GVB opgenomen.

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB19

[Bestand ophalen](assets/do-not-localize/cfp19_osgi_bundles.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB19

[Bestand ophalen](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulatief Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulatief Pak 6.2 SP1-GVB18 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van [ AEM 6.2 SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Toegevoegde steun in DAM CommandLineProcess om het langdurige proces te doden.
* Het lek in ReplicationEventListener is gecorrigeerd voor een sessie.
* Ondersteuning voor omleiding is toegevoegd aan de basispaginacomponent.

### Assets {#assets-1}

* `Camera RAW` -processen blijven vastzitten tijdens perioden van enorme inname, waardoor alle workflowverwerking uiteindelijk wordt geblokkeerd. NPR-26990: Hotfix voor NPR-23860
* Voor de downloadfunctionaliteit wordt AEM Assets gebruikt via een assetdownloadserver waarmee anonieme gebruikers alle middelen kunnen downloaden. NPR-27054, Hotfix voor CQ-4254732
* Speciale tekens worden in de onderwerpregel van e-mailsjablonen in AEM afgebroken weergegeven. NPR-26470: Hotfix voor CQ-4252368

### Sites {#sites-1}

* Door onjuist gedrag van de klasse ConfigPostProcessor verwijdert het opschorten van de bovenliggende afbeelding `cq:LiveRelationship` het mengen van tekst van de onderliggende pagina. NPR-26745: Hotfix voor CQ-4254163
* Voeg ondersteuning voor omleiding toe aan de basispaginacomponent. NPR-26576: Hotfix voor CQ-110529
* Contexthub migreren naar `jQuery` 3. NPR-26956: Hotfix voor CQ-4255472
* De invoervelden van het anker verschijnen uit de zichtbare sectie van de browsers in het dialoogvenster totdat het is gemaximaliseerd. NPR-26852: Hotfix voor CQ-4255019
* Kopieer de plak van tekst die ongewenste &lt;br> in het inhoudsfragment invoegt. NPR-26660: Hotfix voor CRTE-151
* Bij klassieke sitebeheer wordt de lijst in het rechtervenster voor sommige pagina&#39;s niet weergegeven. NPR-27247: Hotfix voor CQ-4251621
* (Klassieke UI) Pogingen om pagina&#39;s te bewegen/anders te noemen produceren een fout, &quot;een fout voorkwam terwijl het bewegen van pagina.&quot; NPR-27179: Hotfix voor CQ-4235907

### Integratie {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever loopt de volledige boom om de beschikbare merken te verzamelen. NPR-27060: Hotfix voor CQ-4255790

### WCM - Elementen van de Stichting {#wcm-foundation-components}

* Probleem met zoekfunctionaliteit met de lijstcomponent Foundation. NPR-26817: Hotfix voor CQ-4250324

### Platform {#platform}

* Vanwege het speciale em-streepje heeft de uitgever een probleem dat de cache leegt. NPR-27199: Hotfix voor CQ-4242790

### Graniet {#granite-1}

* De Validator van het pakket bevestigt geen pakketten inbegrepen in GVB/SP. NPR-26775: hotfix voor graniet-22825

### Replicatie {#replication}

* JCR-sessie lekt in ReplicationListener. NPR-27063: Hotfix voor CQ-4232088

### Forms {#forms-2}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-2}

* Geen nieuwe oplossingen in het AEM Forms-invoegtoepassingspakket.

### Forms JEE Installer {#forms-jee-installer-2}

* Geen nieuwe oplossingen in AEM Forms JEE-installatieprogramma.

#### SDAB-pakketten en -inhoudspakketten {#osgi-bundles-and-content-packages-included-1}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB18

[Bestand ophalen](assets/do-not-localize/62cfp18updated_bundles.txt)

Lijst met inhoudspakketten opgenomen in AEM 6.2 SP1-GVB18

[Bestand ophalen](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulatief Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulatief Pak 6.2 SP1-GVB17 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van [ AEM 6.2 SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Extra ondersteuning voor URL&#39;s zonder site-extensie in at-integration.js
* De opiniepeilingimporter van S7 uit de configuratie van de cloudservice.
* Veranderingen in de publieksmening om omslagstructuur voor multi-huurdersimplementatie te steunen.
* Update aan jqueryui clientlib v1.12.1.

### Assets {#assets-2}

* Voor het starten van workflows vanuit de gebruikersinterface van middelen moet de gebruiker beschikken over de machtigingen voor schrijven, verwijderen en wijzigen. NPR-25688: Hotfix voor CQ-4250140
* Publish- en publicatieknoppen blijven zichtbaar, zelfs voor gebruikers zonder replicatiemachtigingen. NPR-25094
* (Workflow) De workflow Slim tagelement wordt niet verwerkt door de AEM proxyconfiguratie. NPR-25915: Hotfix voor CQ-4248202
* Verwijder de S7-opiniepeilingimportmodule uit de S7-cloudserviceconfiguratie. NPR-25239: Hotfix voor CQ-95236

### Sites {#sites-2}

* Workflows die zijn gestart vanuit de Editor -> Pagina-informatie bevatten het contextpad in de payload. NPR-26389: Hotfix voor CQ-76804
* (Externe koppelingencontrole) Ongeldige https-koppelingen worden weergegeven als geldige koppelingen. NPR-25541: Hotfix voor CQ-4201333
* (Klassieke UI) Wanneer het creëren van een standalone pagina onder een Levende Exemplaar, wordt de pagina gecreeerd als Levende Exemplaar. NPR-25610: Hotfix voor CQ-4249801
* Problemen met het publiceren van bronnen die zijn gekoppeld aan de component Design Importer wanneer een pagina wordt geactiveerd. NPR-25638: Hotfix voor CQ-102532
* De werkbalk van de RTE Rich Text Editor beslaat de lijst met selecties. NPR-25165: Hotfix voor CQ-4248948
* Contexthub migreren naar jQuery 3. NPR-25059: Hotfix voor graniet-19902
* Voor een genestelde component Parsys, altijd wordt het eerste (met minst genestelde weg) bevredigende ontwerp toegepast van veelvoudige beschikbare componenten. Voor meer informatie, zie {de Resolutie van de Weg van het 0} Ontwerp ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). [ NPR-25250: Hotfix voor CQ-4246276

### Integratie {#integration-3}

* Als u de OOTB-doelintegratie gebruikt en een component als doel instelt, wordt de hele pagina weergegeven in plaats van een lege doelcomponent. NPR-25273: Hotfix voor CQ-4248003
* In de modus Aanwijzen wordt bij het verbreken van de overerving nog steeds de component weergegeven die als doel is ingesteld met de overerving die niet is verbroken in de bewerkingsmodus. NPR-25324: Hotfix voor CQ-4248162
* Wanneer een verpersoonlijking op een pagina wordt bepaald en een publiek wordt opgelost, wordt de overeenkomstige ervaring getoond in geef wijze uit. NPR-25731: Hotfix voor CQ-4249465
* Onjuiste teaser-URL bij gebruik van AEM met een niet-standaard contextpad. NPR-25971: Hotfix voor CQ-4250953
* Lege rendering bij gebruik van de optie Weigeren. NPR-25295: Hotfix voor CQ-4246792
* Ervaringen die uit de auteursomgeving zijn verwijderd, worden nooit van de gepubliceerde site verwijderd als de pagina wordt geactiveerd. NPR-24869: Hotfix voor CQ-4247832

### DAM - DM-client {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer negeert muisklikken op apparaten met aanraakbediening. Hotfix voor CQ-4247370

### Platform {#platform-1}

* Toestaan dat u het maximale aantal pogingen voor het ophalen/vrijgeven van een pakket configureert. NPR-25328: Hotfix voor graniet-22376
* Onjuist registreren als er replicatiefouten zijn. NPR-25308: Hotfix voor CQ-4249402
* Apache POI zal mislukken door de Forms AEM 6.2 Forms GVB8 te installeren op het GVB14. NPR-25053: Hotfix voor graniet-21771

### Graniet {#granite-2}

* Het synchronisatieproces van de gebruiker ontbreekt met uitzondering OakConstraint0022. NPR-25729: Hotfix voor Oak-7428

### Gemeenschappen {#communities}

* cq-social-as-provider-bundle begint niet met Mongo-stuurprogramma 3.x-versies. NPR-26271: Hotfix voor CQ-4252710

### UI - Foundation {#ui-foundation-1}

* Update aan jqueryui clientlib v1.12.1. NPR-25090: hotfix voor graniet-21981, CQ-4248897

* (Openbaar onderzoek): de eigenschap &#39;Title&#39; is kwetsbaar voor XSS-scripting (Cross-site) in sites. NPR-24994: Hotfix voor graniet-19933

### Forms {#forms-3}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-3}

#### Aangepaste formulieren {#adaptive-forms-2}

* Onjuiste codering bij het verzenden van gegevens uit adaptief formulier. NPR-25539

#### Forms - Beheer {#forms-management}

* Niet-verwante formulierelementen die als verwijzingen worden gerapporteerd tijdens het publiceren van de pagina. NPR-26167: Hotfix voor CQ-4251004

### Forms - JEE Installer {#forms-jee-installer-3}

#### Documentbeveiliging {#document-security}

* De variabele wordt gevuld met het gegevenstype List, het subtype is een tekenreeks, maar de fout &#39;kan geen object dwingen&#39; treedt op. NPR-26194: Hotfix voor CQ-4252287
* Kan geen toegang krijgen tot watermerkconfiguraties na installatie van 6.2-SP1-GVB15. NPR-26130: Hotfix voor CQ-4250984

### SDAB-pakketten en -inhoudspakketten {#osgi-bundles-and-content-packages-included-2}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB17

[Bestand ophalen](assets/do-not-localize/62cfp17updated_bundles.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB17

[Bestand ophalen](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulatief Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulatief Pak 6.2 SP1-GVB16 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van [ AEM 6.2 SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Extra STARTTLS-ondersteuning in CQ Mail Service op dag.
* Vaste uitlijning van ContextHub-pictogrammen in profielpop-up.
* Oplossingen in de functionaliteit voor weergeven/verbergen van een vervolgkeuzelijst.
* Upgrade naar nieuwste Jackson versie 2.8.11

### Assets {#assets-3}

* Kan geen workflow starten vanuit een lijstweergave. NPR-24393: Hotfix voor CQ-4245788
* (Firefox/Chrome) Kan elementen niet downloaden op de pagina voor het delen van bedrijfsmiddelen. NPR-24523: Hotfix voor CQ-4224408
* Verbeterde standaardkwaliteit voor videovoorvertoning in AEM. NPR-24148: Hotfix voor CQ-4244310

### Integratie {#integration-4}

* Wanneer een component wordt gericht op een publicatie-instantie, lijkt flikkering de standaardervaring te tonen vóór de beoogde instantie. NPR-23992: Hotfix voor CQ-4242038
* Ervaringen die uit de auteursomgeving zijn verwijderd, worden nooit van de gepubliceerde site verwijderd als de pagina wordt geactiveerd. NPR-24869: Hotfix voor CQ-4247832

### Platform {#platform-2}

* Patch jQuery 1.12.4 van clientlib om beveiligingsoplossingen op te nemen. NPR-24129: Hotfix voor graniet-20058
* Extra STARTTLS-ondersteuning in CQ Mail Service op dag. NPR-23941: Hotfix voor CQ-4240397
* Verwijder standaard MERGE_PRESERVE aclHandling. NPR-24593: Hotfix voor graniet-21889
* LineChecker kan koppelingen niet extern maken wanneer een aanvraag ongeldige queryparameters bevat. NPR-24127: Hotfix voor CQ-4241893

### MSM {#msm}

* Proactieve hotfixes aan dwars-plaats scripting aanvallen (XSS). NPR-21893: Hotfix voor CQ-4223385
* MSM LiveRelationship: efficiënte RolloutConfig is verkeerd als BluprintConfig op wortel is. NPR-23999: Hotfix voor CQ-4243000

### Sites {#sites-3}

* Als u een ervaring wilt maken in een gebied van Live Copy, moet de overerving eerst worden verbroken, zodat deze kan worden geconfigureerd. NPR-24995, Hotfix voor CQ-4248209
* (Tik op de gebruikersinterface) Enkele pictogrammen op de bovenste werkbalk verdwijnen terwijl een pagina wordt vergrendeld of ontgrendeld. NPR-23954: Hotfix voor CQ-4243345
* De velden worden niet correct uitgelijnd in de contexthub. NPR-23958
* Publish-actie op de vergrendelde pagina breekt het ontwerpen af. NPR-23970: Hotfix voor CQ-4243203
* OOTB-rapporten in /etc/reports/ werken niet correct en tonen geen historische gegevensgrafiek. NPR-20035: Hotfix voor CQ-420180
* Het starten van een project mislukt tijdens het starten van de workflow voor het starten van een project. NPR-24255: Hotfix voor CQ-4245030
* HTML tags en kenmerken die worden genegeerd door e-mails na de installatie van GFP10. NPR-24287: Hotfix voor CQ-4240028
* TagPicker: tagsuggestie in het tagveld voor metagegevens van tags vraagt labelbare knooppunten op, waardoor het lang duurt om te laden. NPR-24347: Hotfix voor CQ-4244291
* De integratie van Salesforce mislukt bij proxyconfiguraties. NPR-24418: Hotfix voor CQ-4245300
* (WCM) PageManager laat Pagina ingeschakeld op Uitzondering tijdens het maken van Herziening. NPR-24565: Hotfix voor CQ-4246203
* De knop Emulator van apparaat verdwijnt uit de modus Bewerken en Voorvertoning na toepassing van GFP14. NPR-24566: Hotfix voor CQ-4247060
* (Klassieke UI) De volledige markeringen tonen als leeg zodra authored in de dialoogdoos. NPR-24688, Hotfix voor CQ-4246407
* Kan geen versie maken bij de eerste poging. NPR-24774: Hotfix voor CQ-4232176
* OOTB-rapporten in /etc/reports/ werken niet correct en tonen geen historische gegevensgrafiek. NPR-24138: Hotfix voor CQ-420180

### Kwetsbaarheid {#vulnerability-1}

* De integratie van Salesforce is kwetsbaar aan de Smederij van het Verzoek van de Server (SSRF). NPR-24289: Hotfix voor CQ-4245277
* Server Side Request-kwetsbaarheid (SSRF) in ReportingServicesProxyServlet. NPR-24657: Hotfix voor CQ-4246880

### Graniet {#granite-3}

* De bewerkingen voor het lezen van metagegevens worden niet beëindigd. NPR-24240: hotfix voor graniet-19866
* Werk de functionaliteit bij naar 9.4.11.v20180605 om kwetsbaarheden te verhelpen. NPR-25033: Hotfix voor graniet-22120

### WCM - Elementen van de Stichting {#wcm-foundation-components-1}

* PageComparator die ClassCastException werpt terwijl het sorteren van pagina&#39;s. NPR-24123: Hotfix voor CQ-4244048
* De functionaliteit tonen/verbergen van de formuliervervolgkeuzelijst werkt niet zoals u had verwacht. NPR-24562: Hotfix voor CQ-422853

### Gebruikersinterface {#user-interface}

* Een hoog CPU-gebruik wordt waargenomen als gevolg van veel verzoeken in de zoekfunctie van Admin. NPR-23588: Hotfix voor graniet-21286
* (Klassieke UI) De component toont de standaardwaarden zelfs als de bijbehorende modeldienst van vormgegevens aan een leeg gebied wordt geplaatst. NPR-21903: Hotfix voor GRANITE-19744
* Meerveld dat NPE werpt wanneer geen FormData voor verzoek aanwezig is. NPR-24513: Hotfix voor graniet-21055

## Forms {#forms-4}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-4}

#### Kern {#core}

* (OSGI) AEM Forms OSGI had invloed op Jackson data binding security alert. NPR-24274: Hotfix voor CQ-4230245

#### Rights Management {#rights-management}

* Apache POI mislukt na installatie AEM 6.2 SP1-GVB14. NPR-25054, NPR-25052: Hotfix voor CQ-4245898, CQ-4244778

#### HTML5 Forms {#html-forms}

* De gegevens worden niet gevuld met vooraf ingevulde velden van meerdere regels in de HTML-voorvertoning. NPR-23357: Hotfix voor CQ-4244212
* Wanneer een voorvertoning van een letter wordt weergegeven in een standaardvoorvertoning, wordt de toewijzing van lay-outfragmenten niet weergegeven. Als u op Voorvertoning klikt, wordt dit op de juiste wijze weergegeven. NPR-22993: Hotfix voor CQ-4237745
* Probleem met een HTML-voorvertoning van een tekstveld wanneer een patroon voor een socialezekerheidsnummer op een sjabloon wordt toegepast. NPR-23205

#### Adaptieve Forms {#adaptive-forms-3}

* De fout van &quot;Guidelib is niet bepaald&quot;terwijl het toevoegen van AEM vorm aan de component Parsys. NPR-24269: Hotfix voor CQ-4244546

### Forms JEE Installer {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* De lijneinden van het venster in het manuscriptdossiers van Shell veroorzaken LCM om niet in UNIX® te lopen. NPR-22958

### SDAB-pakketten en -inhoudspakketten {#osgi-bundles-and-content-packages-included-3}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB16

[Bestand ophalen](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB16

[Bestand ophalen](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulatief Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulatief Pak 6.2 SP1-GVB15 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van [ AEM 6.2 SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* De pro-actieve veiligheidsmoeilijke situaties in de lijst van de Stichting om ontwerpconsistentie te handhaven.
* Toegevoegde ondersteuning voor typeHint om waarden als tekenreeks op te slaan.
* Biedt uitgebreide beveiliging voor de Forms Prefill-service
* Werk het nieuwste bestand adobe-reader-extensions-dsc.jar bij voor oplossingen in de reader-extensie.
* Aangepaste validatiehaak om `:invalid` items te overwegen voor de invoer van het verhogingsgetal.

### Assets {#assets-4}

* De EmbedXMP-gegevens worden altijd ingesteld op &quot;actief&quot; voor het genereren van de TIFF-piramide. NPR-22776: Hotfix voor CQ-4234498
* Kan meerdere standaardwaarden niet instellen in velden met meerdere waarden. NPR-22900: Hotfix voor CQ-4239000
* (Dynamic Media) Als u het selectievakje Dynamische uitvoeringen inschakelt, geeft het gedownloade ZIP-bestand de oorspronkelijke TIFF-afbeelding weer met een bestand van nul bytes. NPR-22410: Hotfix voor CQ-4198471
* (Aanraakinterface) Standaarduploadlocatie voor elementen in de kolomweergave. NPR-23475: Hotfix voor CQ-4237057

### Integratie {#integration-5}

* In de modus Doel kunnen auteurs een component die van de blauwdruk is overerfd, wijzigen zonder de overerving te annuleren. NPR-22751: Hotfix voor CQ-4237907
* De padvariabele is niet correct gecodeerd, wat leidt tot niet-persistente XSS (Cross-site scripting). NPR-22851

### MSM {#msm-1}

* Tijdens rollout van een LiveCopy met veelvoudige uitrolconfiguraties, als een ResourceNameConflict zich onder de wortel voordoet, eindigt de uitrolstroom zonder alle takken te omvatten. NPR-22842: Hotfix voor CQ-4236188

### Platform {#platform-3}

* Voer een opiniepeilingsgrens in één verzoek om omgekeerde toepassing uit. NPR-23351: hotfix voor graniet-21135***
* Wijzigingen in berichtpatroon worden niet weerspiegeld in aangepaste loggers. NPR-23486: Hotfix voor CQ-4241974

### Sites {#sites-4}

* Het maken van een koppeling in een tekst in een RTF-editor naar een document met spaties of andere speciale tekens werkt niet. NPR-22289: Hotfix voor CQ-4224321
* Als u het segment opslaat met een enorme waarde (10000000000), wordt de versterking ingesteld op 0, waardoor een foutbericht wordt gegenereerd. NPR-22524: Hotfix voor CQ-4237006
* Kan niet klikken op Item toevoegen in component Multifield. NPR-22552: Hotfix voor CQ-4237404
* De horizontale schuifbalk is niet zichtbaar wanneer een segment een lange titel heeft. NPR-22615: Hotfix voor CQ-4237001
* Wanneer een leeg publiek wordt geladen, wordt een onjuiste JavaScript-code gegenereerd. NPR-22974: Hotfix voor CQ-4238734
* Bij het plannen van een activering of deactivering is de titel van de workflow verplicht. De titel van de aangepaste workflow wordt daarom niet vertaald in de tijdlijn. NPR-23121: Hotfix voor CQ-4237552
* Verzoek om moeilijke situaties aan kwesties rond de segmenten van het Doel in Plaatsen. NPR-23128
* (Firefox) Het selectievakje voor de geselecteerde persona is niet het juiste. NPR-23345
* De etiketten voor de verschillende wijzen worden getoond samen met pictogrammen. NPR-23275
* Fout bij &#39;Ongeldige waarde van recursieselectiekader&#39; tijdens het migreren van een component van AEM 6.0 naar AEM 6.2. NPR-23503: Hotfix voor CQ-4241258

### Gemeenschappen {#communities-1}

* Web- en e-mailmeldingen worden niet geactiveerd vanwege een fout met het bericht aan de groepen. NPR-23447: Hotfix voor CQ-4242880

### Vertaling {#translation-1}

* Elementtaalkopieën worden gemaakt wanneer het element &quot;Niet vertalen&quot; is ingesteld in de vertaalconfiguratie. NPR-22540: Hotfix voor CQ-4237962

### Gebruikersinterface {#user-interface-1}

* Als u Omngelijkzoek gebruikt met een afbreekquery, wordt een serverfout geretourneerd. NPR-22999: Hotfix voor graniet-19674
* DatePicker biedt geen ondersteuning voor het handmatig instellen van hint voor externe typen die door een verborgen veld zijn ingesteld. Als u de teksthint wijzigt, treedt er een omzettingsfout op. NPR-2333: Hotfix voor graniet-21194

### WCM - Elementen van de Stichting {#wcm-foundation-components-2}

* De component CAPTCHA is nu afgekeurd voor betere beveiliging. Als u de component CAPTCHA gebruikt, wordt het bericht &quot;component Captcha is afgekeurd en zou niet moeten worden gebruikt&quot;getoond na het installeren van 6.2 SP2-GVB15 of recentere versie. AEM component kan worden aangepast om reCAPTCHA op te nemen voor betere beveiliging NPR-22151: Hotfix voor CQ-4220052
* De component van de Stichting WCM &quot;Lijst&quot;is kwetsbaar aan Opgeslagen dwars-Plaats Scripting. NPR-23206: Hotfix voor CQ-4240760

### Kwetsbaarheid {#vulnerability-2}

* XSS (cross-site scripting) in Admin UI-projectkoppelingen. NPR-23272: Hotfix voor CQ-4241795

## Forms {#forms-5}

### Forms-invoegtoepassing {#forms-add-on-package-5}

#### Correspondentenbeheer {#correspondence-management}

* Wanneer een voorvertoning van een letter wordt weergegeven in een standaardvoorvertoning, wordt de toewijzing van lay-outfragmenten niet weergegeven, terwijl dit op de juiste wijze wordt weergegeven wanneer u op de knop Voorvertoning klikt. NPR-2335: Hotfix voor CQ-4237745
* Gegevens in de letter die overeenkomen met bindingen die zijn gedefinieerd in XDP, worden niet gevuld met de directe letter URL. NPR-24145: Hotfix voor CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Correspondentiebeheer) Gegevensuitlijning is onjuist tijdens het laden van de letter met de doel-XML. NPR-22993: Hotfix voor CQ-4237663

#### Reader Extensions-service {#reader-extensions-service}

* Kan de lezerextensie niet toepassen op Adobe PDF. NPR-23067

#### Forms Manager {#forms-manager}

* Forms die is ingesloten in de site, wordt niet gepubliceerd wanneer de sitepagina opnieuw wordt gepubliceerd. NPR-23014: Hotfix voor CQ-4236566

#### Kwetsbaarheid {#vulnerability-3}

* Proactieve hotfixes voor cross-site scripting. NPR-20624: Hotfix voor CQ-4206055
* XSS (Storage Cross-site scripting)-kwetsbaarheid opgeslagen op het tabblad Notities van Forms Manager. NPR-27157: Hotfix voor CQ-4255556

#### Coderingsservice {#encryption-service}

* (OSGI) [ JEE ] Onjuiste handtekeningsstatus voor PDF met gehechtheid terwijl het verifiëren van het gebruiken van &quot;Valideer het proces van PDF.&quot; NPR-23269, 23737

### Forms JEE Installer {#forms-jee-installer-5}

#### Kern {#core-1}

* De in de statische codeanalyse van Core-ext gerapporteerde problemen moeten worden vastgesteld. NPR-13947

#### PDFG-service {#pdfg-service}

* De convertor HTML naar PDF werkt niet. NPR-21545

### SDAB-pakketten en -inhoudspakketten {#osgi-bundles-and-content-packages-included-4}

In de volgende tekst wordt de lijst met OSGI-bundels en -inhoudspakketten in het GVB opgenomen.

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB15

[Bestand ophalen](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB15

[Bestand ophalen](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulatief Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulatief Pak 6.2 SP1-GVB14 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Verbeterde bewerkbaarheid van eigenschappen van metagegevens van elementen.
* De taak Wachtwoordvervalmelding is opnieuw geconfigureerd voor elementen die al zijn verlopen.
* Aangepaste UI-console voor het uitbreiden van meer landinstellingen.
* Bijgewerkte cq-msm-core voor efficiënte synchronisatie Livecopyindex.
* Gestroomlijnde replicatiefunctionaliteit voor verschillende rollouts.

### Assets {#assets-5}

* Gebruikers kunnen geen elementen downloaden met een disclaimer- en lange bestandsnaam. NPR-22163: Hotfix voor CQ-4235274
* Eén aanhalingsteken voorkomt dat de metagegevens in de bulkweergave worden bijgewerkt. De interface wordt verbroken wanneer u de eigenschappen van een element opent met de snelle werkbalkhandelingen. NPR-22317, NPR-22353: Hotfix voor CQ-4236990, CQ-4236469
* De functie Bericht bij aflopen van element deactiveert de verlopen elementen niet. NPR-22346: Hotfix voor CQ-4237188
* Downloaden van middelen mislukt wanneer Digital Rights Management in Assets op Safari wordt gebruikt. NPR-22378: Hotfix voor CQ-4236460
* Webuitvoering voor kleine afbeeldingen heeft een onjuiste pixelgrootte. NPR-22435: Hotfix voor CQ-4236742

### Sites {#sites-5}

* (Aanraakinterface) De verplaatste tag wordt op oude en nieuwe locaties weergegeven in pagina-eigenschappen. NPR-21921, Hotfix voor CQ-4238598
* (Aanraakinterface) De RTF-editor verwijdert alle andere kenmerken dan id uit de &lt;a>-tag. NPR-22045: Hotfix voor CQ-4234133
* Als u inhoud rechtstreeks in de RTF-editor plakt met CTRL+V, worden regeleinden overgeslagen. NPR-22117: Hotfix voor CUI-5881
* (Touch UI) Kan niet meer dan 40 tags weergeven onder een naamruimte. NPR-22290: Hotfix voor CQ-99114
* RSS Feed Issues, port -1 to AEM 6.2 NPR-22158: Hotfix for CQ-4233339
* (IE) Wanneer u voor het eerst een teken in het tekstveld RTF ontwerpt, wordt een spatie aan het teken toegevoegd. NPR-22443: Hotfix voor CQ-4235343
* Wanneer wordt geprobeerd de pakketnaam aan te passen, bevriest het Java™-object Use de SightlyJavaCompilerService vanwege een spatieteken aan het einde in de pakketdeclaratie. NPR-22557: Hotfix voor graniet-20836
* De Touch UI-console haalt geen nieuwe talen op voor codering. NPR-22250: Hotfix voor CQ-4239194

### Mobiel op aanvraag {#mobile-on-demand}

* (Digital Publishing Suite) Voor folio&#39;s zijn zowel de publicatiedatum als de omslagdatum vereist voordat ze naar DPS worden geüpload. NPR-22484

### Commerce {#commerce}

* Meerdere XSS-kwetsbaarheden (cross-site scripting) op de handel: de wizard Catalogus maken. NPR-22344: Hotfix voor CQ-4237017

### MSM {#msm-2}

* De synchronisatie LiveCopyIndex leidt tot congestie van draden tijdens lange indexupdates. NPR-22214: Hotfix voor CQ-90667
* De eigenschap `cq:cugEnabled` wordt uitgeschakeld wanneer een ander veld in een live kopie wordt bewerkt. Hierdoor wordt de pagina onbeveiligd. NPR-22246: Hotfix voor CQ-4236050
* De actie Pagina-uitrol kan onderliggende items niet bijwerken wanneer een pagina wordt opgeschort. NPR-22483: Hotfix voor CQ-4236956
* Uitrol van een structuur die in een primaire map is verplaatst, leidt tot een onjuiste `cq:moveTarget` . NPR-22373: Hotfix voor CQ-4232536

### Integratie {#integration-6}

* Wanneer u aanbiedingen in de bibliotheek met aanbiedingsselecties probeert te sorteren, resulteert dit in onregelmatig gedrag. NPR-22208: Hotfix voor CQ-4235439
* TargetContentImpl maakt AEM tijdens langdurige query&#39;s traag. NPR-22361: Hotfix voor CQ-4236907
* De doelengine (mbox.js, at.js) gebruikt geen beheerde URL&#39;s en gebruikt URL&#39;s die dubbele punten bevatten die mogelijk mislukken bij bepaalde implementaties. NPR-22366: Hotfix voor CQ-4237854
* Voor paginagropersonalisatie is de publicatierecht op het merkknooppunt vereist. NPR-22370: Hotfix voor CQ-4236895

### Stichting {#foundation}

* Apache het Schuiven Scripting Sightly Models gebruikt de bundel van de Leverancier **org.apache.sling.scripting.siely.models.provider/1.0.18**. NPR-22614: Hotfix voor Sling-5944, Sling-6866

### Projecten {#projects}

* De Starter van het werkschema kan niet de waarde TypeHint van Koord goedkeuren. NPR-22436: Hotfix voor CQ-4237855

### Vertaling {#translation-2}

* Problemen met de voorvertoningsfunctie onderzoeken. NPR-22201: Hotfix voor CQ-4223753

### Gebruikersinterface {#user-interface-2}

* (Klassieke UI) De component toont de standaardwaarden zelfs als de bijbehorende modeldienst van vormgegevens aan een leeg gebied wordt geplaatst. NPR-21903: Hotfix voor GRANITE-19744

### WCM - Elementen van de Stichting {#wcm-foundation-components-3}

* Fout bij het publiceren van een pagina van Actieve kopie die naar een pagina van de Importeur in de Campagnes van Adobe wijst. NPR-22470: Hotfix voor CQ-4237164
* JavaScript-fouten tijdens het openen van de Experience Fragments Editor. NPR-22598: Hotfix voor CQ-4238415

### Workflow {#workflow}

* De Day CQ Workflow Email Notification Service leidt tot één e-mail per Mongo-knooppunt voor WorkflowCompleted- en WorkflowAborted-meldingen. NPR-22486: Hotfix voor CQ-4238172

## Forms {#forms-6}

### Forms-invoegtoepassing {#forms-add-on-package-6}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

#### Adaptieve Forms {#adaptive-forms-4}

* Inconsistentie in de plaatsaanduidingswaarde voor vervolgkeuzelijsten in adaptieve vorm in IE11 en Chrome. NPR-22405: Hotfix voor CQ-4227096

### Forms JEE-installatieprogramma {#forms-jee-installer-6}

#### LCM installeren {#install-lcm}

* Jsafe Jars bijwerken naar Cryptoj 6.1.3.1 in installatieprogramma en LCM. NPR-2274

### Inclusief functiepakketten {#feature-packs-included}

#### Procesbeheer {#process-management}

* (HTML Workspace) Wanneer een gebruiker een taak claimt, wordt het aantal van de wachtrij alleen voor die specifieke gebruiker vernieuwd. Dat wil zeggen, tenzij de pagina wordt vernieuwd. NPR-1978: Hotfix voor CQ-4233665

### SDAB-pakketten en -inhoudspakketten in GVB14 {#osgi-bundles-and-content-packages-included-in-cfp}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB14

[Bestand ophalen](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB14

[ krijgt Dossier ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
AEM Cumulatief Pak 6.2 SP1-GVB13 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* De toegelaten Statische het gebiedsconfiguratie van de Parameter binnen de Montages van de Component van het Doel terwijl het gebruiken van AT.js als cliëntbibliotheek.
* Oplossingen in de functionaliteit voor weergeven/verbergen van een vervolgkeuzelijst.
* Oplossingen voor het gebruik van doelsynchronisatiepubliek.
* Meer veelzijdigheid voor Correspondentiebeheer om speciale tekens te kunnen gebruiken.

### Assets {#assets-6}

* Versie wissen kan oude versies van elementen niet verwijderen. NPR-21682: Hotfix voor CQ-4212996
* Het opnieuw ordenen van mappen onder een map die opnieuw kan worden geordend, duurt niet voort. NPR-21964: Hotfix voor CQ-4231761

### Sites {#sites-6}

* (TouchUI)(ClassicUI) Meerdere XSS-kwetsbaarheden (cross-site scripting) in HTML en kerncomponenten. NPR-21532: Hotfix voor CQ-4232305 en CQ-4232511
* Het maken/opmaken van inhoud (bijvoorbeeld het toewijzen/verwijderen van nieuwe lijststijlen) voor een geselecteerde tekst werkt niet goed in Internet Explorer 11. NPR-21533: Hotfix voor CQ-4230689
* (Safari) Gebruikers kunnen niet alle elementen in het deelvenster Asset Finder weergeven. NPR-21981: Hotfix voor CQ-4213720
* Timewarp retourneert een fout &quot;RecursionToDeepException&quot; met een verstoorde pagina en er wordt geen nieuwe versie gemaakt, zelfs niet wanneer de datum wordt gewijzigd. NPR-21707: Hotfix voor CQ-4199536
* Wanneer het laden van een pagina in de redacteur, wordt WorkflowStatusProvider (pageinfo.json) geladen drie keer, veroorzakend de AEM instantie langzaam. NPR-21778: Hotfix voor CQ-59232

### Integratie {#integration-7}

* Het maken van soorten publiek van Mobile Type &amp; Browser in de ontwerpmodus van Doel werkt niet in AEM. NPR-21676, NPR-21681: Hotfix voor CQ-4232100
* Onder hoge latentie tijdens verfrissen van een gerichte component, is het mogelijk om een andere aanbieding toe te voegen alvorens de component volledig wordt verfrist. NPR-21744: Hotfix voor CQ-4233158/CQ-4234293
* Gebruikers kunnen de statische parameterwaarden van de test in de mbox vraag niet zien die wanneer het testen met AT.js als cliëntbibliotheek in wolkenconfiguratie kan worden gezien. NPR-21930: Hotfix voor CQ-4234520

### Platform {#platform-4}

* Prestatieproblemen met gebruikerssynchronisatie wanneer het aantal gebruikers of groepen groot is. NPR-20431: Hotfix voor CQ-4223282
* Gebruikers kunnen niet synchroniseren met gebruikerssynchronisatie met Sling Distribution. NPR-21911: Hotfix voor graniet-20404
* Voorkomen dat stopwoorden worden gemarkeerd in zoekfragmenten (op een Geometrixx-pagina). NPR-21835: Hotfix voor graniet-21067
Opmerking: voor deze correctie is Oak GVB 1.4.20 of hoger vereist.

### Vertaling {#translation-3}

* De eigenschap jcr ontbreekt voor de gebruikers-id van de initiator tijdens het maken van een vertaalproject. NPR-21715: Hotfix voor CQ-4230713

### WCM - Elementen van de Stichting {#wcm-foundation-components-4}

* De functionaliteit tonen/verbergen van de formuliervervolgkeuzelijst werkt niet zoals u had verwacht. NPR-22164: Hotfix voor CQ-4235288

## Forms {#forms-7}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-7}

#### Adaptieve Forms {#adaptive-forms-5}

* XML External Entity Injection (XXE) injectie in Adaptive Forms. NPR-21982: Hotfix voor CQ-109878
* (iOS11) Wanneer u op de component voor bestandsbijlagen klikt, wordt de camera in de bestandsbijlage geopend in plaats van de browser van het apparaatbestand. NPR-21926: Hotfix voor CQ-4214348
* De ontbrekende titel in de interface voor het maken van thema&#39;s veroorzaakt een uitzondering en leidt tot het niet weergeven van het dialoogvenster. Hotfix voor CQ-4236143

#### Correspondentenbeheer {#correspondence-management-1}

* Rendering geeft problemen met XML-gegevens met speciale tekens. NPR-21712: Hotfix voor CQ-4229137

### Forms JEE-installatieprogramma {#forms-jee-installer-7}

#### Assembler-service {#assembler-service}

* Het met `6.2.0-ASM-1017-003` gegenereerde PDF-bestand is beschadigd. NPR-21427: Hotfix voor CQ-4228046

#### PDFG-service {#pdfg-service-1}

* OCR-fout door onverwachte paginagrootte (PDF) van PNG-, JPEG- en TIFF-bestanden. NPR-19489: Hotfix voor CQ-4209079

## SDAB-pakketten en -inhoudspakketten in GVB13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB13

[Bestand ophalen](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB13

[Bestand ophalen](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulatief Pak 6.2 SP1-GVB12.1 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Verbeterde verwerking van metagegevens voor velden met meerdere waarden.
* Ondersteuning voor meertalig (meer dan twee) landcodes in vertaalworkflows.
* Verbeterde weergave van pagina&#39;s met meerdere geneste componenten.
* Verbeterde synchronisatie van publicatiedata voor middelen tussen AEM en Adobe Digital Publishing Suite.

### Assets {#assets-7}

* Te veel tekens in OmniSearch kunnen ertoe leiden dat de AEM server vastloopt. NPR-21083: Hotfix voor CQ-4223602
* Waarden die zijn opgegeven in de tweede optie in een veld Meerdere waarden in het metagegevensschema, worden niet toegevoegd aan de eerder opgegeven waarden in CRX-de. NPR-21220: Hotfix voor CQ-4224526
* Downloaden van middelen mislukt wanneer Digital Rights Management in Assets op Safari wordt gebruikt. NPR-21387: Hotfix voor CQ-4230287

### Sites {#sites-7}

* (DAM) (ClassicUI) Veelvoudige XSS-kwetsbaarheden (cross-site scripting) in sommige SWF-bestanden in AEM CQ-auteur/Publish quickstart. NPR-21073, NPR-21074: Hotfix voor NPR-20612
* De tagkiezer vertaalt de tags die beschikbaar zijn in meerdere talen niet. NPR-21221: Hotfix voor CQ-78855
* Renderproblemen met AEM artikelconsole als het gebruik van meerdere geneste componenten maken het traag. NPR-21271: Hotfix voor CQ-4224158

### Integratie {#integration-8}

* Als u een doelframework toevoegt, is de modus Doel niet beschikbaar in de lijst Modus Selecteren in de editor. NPR-21047

### Mobiel-op-aanvraag {#mobile-on-demand-1}

* (Digital Publishing Suite) Publicatiedata voor folio&#39;s in AEM komen niet overeen met de datums die worden weergegeven in de Folio Producer. NPR-21145

### MSM {#msm-3}

* Het herstelproces van Live kopie wordt gestopt nadat de eerste lokale pagina in de LC is verwijderd. NPR-21276: Hotfix voor CQ-4229743

### Platform {#platform-5}

* Aangepaste tag lib die referentietags implementeert als script, worden niet gevonden na upgrade naar AEM 6.3. NPR-20149: Hotfix voor graniet-18433

### Vertaling {#translation-4}

* Workflows voor vertaling mislukken wanneer lang_country-codes langer zijn dan twee tekens. NPR-21088: Hotfix voor CQ-4197439
* Verzend geen Middelenpagina opnieuw aan een vertaalproject tot het project voltooit. NPR-21219: Hotfix voor CQ-4209908

### Gebruikersinterface {#user-interface-3}

* De component Select verwijdert de eigenschap target niet tijdens het verzenden van het formulier. NPR-21163: Hotfix voor GRANITE-14125
* HTTP.encodePathOfURI breidt dubbele codering uit van het plusteken &#39;+&#39;. NPR-21417: Hotfix voor GRANITE-16340

### Kwetsbaarheid {#vulnerability-4}

* XSS (Cross-site scripting) in de DAM-metagegevenseditor. NPR-21434: Hotfix voor CQ-83472
* Meerdere SWF-bestanden zijn kwetsbaar voor XSS (cross-site scripting). NPR-20612: Hotfix voor CQ-4213297

## Forms {#forms-8}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-8}

#### Correspondentenbeheer {#correspondence-management-2}

* (IE11) De eerste rendering van de HTML-inhoud vindt alleen aan de linkerkant plaats, terwijl de rechterkant periodiek wordt geladen nadat de volledige gebruikersinterface is geladen. NPR-21554
* De knop Letter preview submit wordt uitgeschakeld na installatie van AEM 6.2 SP1-GVB9. NPR-21547
* Als u het koppelingstype Element selecteert, wordt het venster Asset Selector niet geopend in de wizard Letterlijke gegevensbinding bewerken. NPR-21164: Hotfix voor CQ-4194567
* Tik op het desbetreffende pictogram Bewerken of dubbelklik op de relevante tekstmodule in de lettertypevoorvertoning om een inline- of bewerkbare tekstmodule te bewerken. NPR-21402

#### Adaptieve Forms {#adaptive-forms-6}

* De AEM Forms submit button component toont type=&quot;button&quot; in plaats van type=&quot;submit&quot;. NPR-21007
* Gegevens blijven blijvend bij het toevoegen of verwijderen van nieuwe deelvensters voor herhaalbare deelvensters. NPR-21408

### Forms JEE-installatieprogramma {#forms-jee-installer-8}

#### Kern {#core-2}

* Als u een upgrade uitvoert naar de nieuwste Java™ 8 Update 131, wordt een uitzondering gegenereerd: &quot;JsafeJCE provider is disabled, a FIPS 140 required self-integriteitscontrole failed.&quot; NPR-2135

**Nota:** Deze NPR vereist meer montages. Zie [ Meest recente update Java™ 8 ](#latest-java-update-throws-an-exception-npr).

* De Jsafe Jars zijn bijgewerkt naar CryptoJ 6.1.3.1 in Core, Encryption, Signature &amp; Document Security. NPR-21360, 21361, NPR-21356, NPR-21358

#### LCM installeren {#install-lcm-1}

* Werk Jsafe Jars bij naar CryptoJ 6.1.3.1 in installer &amp; LCM. NPR-21362

#### PDFG-service {#pdfg-service-2}

* Werk Jsafe Jars bij naar CryptoJ 6.1.3.1 in PDFG. NPR-21359

#### Procesbeheer {#process-management-1}

* (HTML Workspace) Het inschakelen van kolomformaatwijziging zodat de naamcategorie niet wordt afgekapt. NPR-19770: Hotfix voor CQ-4233668

#### Reader Extensions-service {#reader-extensions-service-1}

* De Jsafe Jars zijn in RE bijgewerkt naar CryptoJ 6.1.3.1. NPR-21357

## SDAB-pakketten en -inhoudspakketten opgenomen in GVB12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB12.1

[Bestand ophalen](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2 SP1-GVB12.1

[Bestand ophalen](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulatief Pak 6.2 SP1-GVB11 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Bijgewerkte cq-msm-core voor efficiënte synchronisatie Livecopyindex.
* Verbeterde bewerkingsefficiëntie voor inhoudsfragmenten.
* Het verstrekt een bevestigingsoptie in de Manager van het Pakket voor het ontdekken van ACL toestemmingen.
* Introduceerde de capaciteit van Campagne om e-mailidentiteitskaart voor klantencorrespondentie te omvatten.
* Verbeterde mogelijkheden voor videocodering voor Dynamic Media-bestanden.
* Oplossingen in de component Sightly en LiveCopies.

### Assets {#assets-8}

* Dynamic Media video encoding failed for files that include spaces in their names. NPR-20818: Hotfix voor CQ-102469
* Meerdere XSS-kwetsbaarheden (cross-site scripting) in sommige SWF-bestanden in AEM CQ-auteur/Publish quickstart. NPR-21071, 21072
* Gebruikers kunnen geen elementen downloaden met een disclaimer- en lange bestandsnaam. NPR-20255: Hotfix voor CQ-422139

### Sites {#sites-8}

* Integratie van AEM en campagne: in Adobe Campaign worden speciale koppelingen herschreven, zodat klanten geen mailto kunnen sturen: hyperlinks in hun e-mails. NPR-20787: Hotfix voor CQ-4225760
* (Aanraakinterface) AEM problemen met de bruikbaarheid en prestaties wanneer de taal op Frans wordt ingesteld. NPR-20854: Hotfix voor CQ-4227628
* Als u een gecodeerd elementbestand koppelt met een koppelingsplug-in in RTE, wordt een lege koppeling geretourneerd. NPR-20626, NPR-21059: Hotfix voor CQ-4223011
* De metagegevenseditor voor inhoudsfragmenten voorkomt dat auteurs van inhoud wijzigingen opslaan in inhoudsfragmenten. NPR-20641: Hotfix voor CQ-4224755
* Alias voor pagina-eigenschap leidt tot Request-publicatie/Request-publicatie. NPR-20731: Hotfix voor CQ-4226227
* Tekstcomponentproblemen met codering van koppeling in RTE-element. NPR-20755: Hotfix voor CQ-4224321

### Platform {#platform-6}

* ResourceResolverImpl.map() roept ResourceDecorator niet aan. NPR-20788: Hotfix voor GRANITE-19718
* `org.apache.sling.i18n.DefaultLocaleResolver` kan aanvragen niet verwerken via org.apache.sling.engine.SlingRequestProcessor. NPR-20706: Hotfix voor CQ-94880
* Verzoek om een bevestigingsoptie in de Manager van het Pakket toe te voegen om te ontdekken als om het even welke ACL toestemmingen/voorrechten op een bepaald pakket worden veranderd. Hotfix voor CQ-4229196

### Workflow {#workflow-1}

* Stabiliteitsproblemen met AEM implementatie van productieservers. NPR-20979: Hotfix voor graniet-19104

### Projecten {#projects-1}

* (Touch UI) Teamleden kunnen niet aan een project worden toegevoegd. NPR-20990: Hotfix voor CQ-4205375

### WCM-stichtingscomponenten {#wcm-foundation-components-5}

* De juiste afbeeldingscomponent &#39;link to&#39; genereert een fout van 403 omdat de extensie .html ontbreekt. NPR-20823: Hotfix voor CQ-4195909
* Als u een formuliercomponent probeert te verwijderen op een blauwdruksite met LiveCopy, wordt een NullPointerException gegenereerd en wordt de component Form toegevoegd in plaats van verwijderd. NPR-20855: Hotfix voor CQ-4204628
* De synchronisatie LiveCopyIndex leidt tot congestie van draden tijdens lange indexupdates. NPR-20634: Hotfix voor CQ-90667

### Beveiliging {#security}

* Proactieve XSS-bibliotheekupdate. NPR-21174
* Voer een upgrade uit naar Apache Commons Email 1.5, die een vereenvoudigde API biedt voor het verzenden van e-mail. NPR-20509: Hotfix voor graniet-18240
* Beveiligingspatch toegepast op Apache Sling XSS Protection API om de mogelijkheid van XSS-omzeilen uit te sluiten. NPR-21290: Hotfix voor GRANITE-19924
* XSS bypass in XSSAPI#getValidHref functie. NPR-21174: Hotfix voor graniet-19924

### Mobiele apps {#mobile-apps}

* Correctie van problemen met curl Head-aanvragen voor OOTB-middelen in AEM. NPR-20511: Hotfix voor CQ-4221520 en CQ-103024

## Forms {#forms-9}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

De belangrijkste markeringen voor AEM Forms zijn:

* Certificaatverificatie ingeschakeld voor Workbench-gebruikers.
* Oplossingen voor bruikbaarheid voor Correspondentiebeheer, HTML5-formulieren en de AEM Forms-werkruimte.

### Forms-invoegtoepassing {#forms-add-on-package-9}

#### HTML5 Forms {#html-forms-1}

* Gebruiksproblemen met krabbelonderdelen op iOS 10- en 11-apparaten. NPR-21092

#### Correspondentenbeheer {#correspondence-management-3}

* (Interface van correspondentie) Schakel de verzendknop uit na één klik. NPR-21078

### Forms JEE-installatieprogramma {#forms-jee-installer-9}

#### Assembler-service {#assembler-service-1}

* docConvertor produceert geen PDF/A met de fout &quot;Het voorvoegsel &quot;stEvent&quot; voor element `stEvt:action` is niet gebonden.&quot; NPR-21032: Hotfix voor CQ-422540
* Er wordt een uitzondering gegenereerd met de naam `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` bij het oproepen van service OMPFSubmission/PDFA/PDFtoPDFA. Deze uitzondering voorkomt dat het kortstondige verificatieproces voor handtekeningen wordt voltooid totdat de server opnieuw wordt gestart. NPR-20792

#### Workbench {#workbench}

* Certificaatverificatie inschakelen voor Workbench-gebruikers. NPR-17548: Hotfix voor CQ-4214486

#### Procesbeheer {#process-management-2}

* Het voorbereiden van het gegevensproces roept meerdere keren aan wanneer een mobiel formulier wordt weergegeven met dataref-parameters. NPR-19801: Hotfix voor CQ-4230427: CQ-4230400

## SDAB-pakketten en -inhoudspakketten in GVB11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB11

[Bestand ophalen](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2 SP1-GVB11

[Bestand ophalen](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulatief Pak 6.2 SP1-GVB10 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Er is een hulpprogrammafunctie onDialogLoaded toegevoegd voor tests.
* De frontend eenheidtests en configuraties aan ClientLibraryProxyServlet werden toegevoegd.
* Prestaties worden hersteld in de component Multiple image in-place Editor.
* Configuratie-updates in Apache Sling JCR ResourceBundleProvider.

### Assets {#assets-9}

* De voorvertoning van elementen werkt niet als workflows voor het bijwerken van elementen zijn uitgeschakeld. NPR-20543: Hotfix voor CQ-4204986
* Renderproblemen met klasse toegevoegd aan graniet: klasseneigenschap (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix voor CQ-4219238
* Miniatuurmiddelen met speciale tekens in de titel tonen Java™-object in alt-kenmerk van NPR-20347: Hotfix voor CQ-4223620
* Vervang de vergelijkingscode van de versie met de merkgebonden code van de Adobe wegens vergunningskwesties. NPR-20273: Hotfix voor CQ-4223758
* Problemen bij het uploaden van CMYK PSB-bestanden met meerdere alpha-lagen worden verwerkt. NPR-20251: Hotfix voor CQ-4220869
* Internationalisatiewoordenboeken werken als de server opnieuw wordt opgestart in org.apache.sling.i18n 2.5.6. NPR-20525: Hotfix voor graniet - 19490
* Geen draaddumps worden geproduceerd volgens de plannerperiode met het gebrek van de Verzameling van de Stortel van de Dia (gebrek AEM opstarten). NPR-20288: Hotfix voor GRANITE-1948/GRANITE-12741 CQ-90647.

### Sites {#sites-9}

* Als het filter voor gewijzigde datum wordt gewijzigd nadat de opgeslagen zoekopdracht is geopend, heeft dit geen invloed op de resultaten. En de weergegeven resultaten zijn gelijk aan de vorige opgeslagen waarde van het gewijzigde datumfilter. NPR-19739: Hotfix voor CQ-4219425
* Pagina&#39;s met geneste componenten kunnen niet worden geladen. NPR-20312
* Verzoek tot verwijdering wordt geactiveerd wanneer werkstroompakketten worden verwijderd. NPR-20266: Hotfix voor CQ-4221686
* (Aanraakinterface) Probleem met kopiëren/plakken met systeemklembord en intern AEM klembord. NPR-20228: Hotfix voor CQ-4220383
* AEM instantie wordt traag in de lijstweergave wanneer meerdere elementen (meer dan 100) worden geladen. NPR-20034: Hotfix voor CQ-422695
* (Interface van de aanraking) schrapping van lanceringen door de Klassieke console UI maakt alle pagina&#39;s onbewerkbaar. NPR-20520: Hotfix voor CQ-4225074
* De drop-down van het doel werkt niet met veelvoudige componenten RTE in een dialoogdoos. NPR-20345: Hotfix voor CQ-4220981

### Platform {#platform-7}

* Wanneer betreden gebruikend een anonieme zitting, ClientLibraryProxyServlet geen volmachtsverzoeken aan cliëntbibliotheken op de gepubliceerde instantie en werpt HTTP 404 niet gevonden fout. NPR-20195: Hotfix voor graniet-14409

### Integratie {#integration-10}

* Als u de doelengine selecteert als Adobe Target, wordt de component niet geladen en wordt een fout weergegeven in het serverlogbestand. NPR-20058: Hotfix voor CQ-88071,CQ-109698,CQ-4201600

### Commerce {#commerce-1}

* Er verschijnt geen bevestiging of omleiding voor pop-upberichten wanneer u producten maakt op dezelfde pagina. NPR-20257: Hotfix voor CQ-4223414

### Gebruikersinterface {#user-interface-4}

* Wanneer de Datumkiezer een veld in een meerdere velden is, worden de waarden die in de datumvelden zijn opgeslagen, niet voortgezet tijdens het bewerken van de component. NPR-2007: Hotfix voor GRANITE-19147
* Vorige query&#39;s worden niet afgebroken als opeenvolgende query&#39;s worden geactiveerd, wat leidt tot onjuiste resultaten. NPR-20397: Hotfix voor GRANITE-19306

### WCM - Elementen van de Stichting {#wcm-foundation-components-6}

* De eigenschap ImageMap bestaat nog steeds, zelfs nadat de afbeeldingen zijn verwijderd uit de component Multiple image in-place Editor. NPR-20142: Hotfix voor CQ-4222982

## Forms {#forms-10}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-10}

#### Adaptieve Forms {#adaptive-forms-7}

* valueCommit Script wordt tweemaal uitgevoerd voor DropDownList wanneer veranderd door UI. NPR-19989: Hotfix voor CQ-110212

### Forms JEE Installer {#forms-jee-installer-10}

**Beheer van het Proces**

* Het GVB-pakket bevat AEM Forms HTML Workspace versie 2.2.26. NPR-2009
* Een vooraf ingevuld formulier werkt niet wanneer het mobiele formulier is geconfigureerd om te worden weergegeven als PDF. NPR-20566

**Rights Management**

* Het dialoogvenster CAC/Wederzijdse verificatie-certificaatselectie moet certificaten met Enhanced Key Usage (EKU) weergeven als client-auth- of smartcard-aanmelding. NPR-20708
* Forms JEE biedt ondersteuning voor PKCS#11-wederzijdse verificatie. NPR-15001

## SDAB-pakketten en -inhoudspakketten in GVB10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Lijst van OSGi-bundels opgenomen in AEM GVB 6.2 SP1-GVB10

[Bestand ophalen](assets/do-not-localize/bundle-list-cfp10.txt)

Lijst met inhoudspakketten die zijn opgenomen in AEM GVB 6.2 SP1-GVB10

[Bestand ophalen](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulatief Pak 6.2 SP1-GVB9 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Aangepaste Klassieke UI-configuratie Analytics voor geheime invoer.
* Oplossingen voor onafhankelijke persistentiecache voor contexthub.
* Nauwkeurige berekening van de dimensies van activa.
* Geoptimaliseerde AEM prestaties bij het publiceren van middelen naar Brand Portal.
* Hiermee wordt de waarde van `Resourcetype` in het canvasknooppunt gecorrigeerd.
* Ingeschakelde hoofdlettergevoelige en speciale zoekfunctionaliteit voor tekens voor inhoud van documentfragment.
* Enhanced Adaptive Forms to attach PDF as attachments in Safari.
Deze ervaring biedt een nieuwe Dynamic Media die verbinding maakt met de nieuwe Dynamic Media Publishing Infrastructure voor snellere en schaalbaardere replicatie.

### Assets {#assets-10}

* AEM Assets kan subelementverwijzingen voor InDesign-elementen niet extraheren door dubbele koppelingen naar het element te maken. NPR-19006: Hotfix voor CQ-4204186
* De sorteeroptie werkt niet voor elementen in de verzameling onder Commerce. NPR-19508: Hotfix voor CQ-4213622
* Wanneer een element met dezelfde naam als een reeds bestaand element naar dezelfde locatie wordt verplaatst, wordt de waarde van `cq:lastReplicationAction` voor de elementen tussen elkaar gewisseld, waardoor onjuiste metagegevens worden gemaakt. NPR-19531
* Er wordt een foutbericht weergegeven wanneer u een groot aantal elementen publiceert, ook al worden alle elementen correct gepubliceerd. NPR-19629: Hotfix voor CQ-4219611
* Statische uitvoeringen worden weergegeven met vaste afmetingen en geven niet de grootte van de eigenlijke vertoning weer. NPR-2004
* AEM wordt traag wanneer meerdere elementen (meer dan 4) naar Brand Portal worden gepubliceerd. NPR-2009

### Sites {#sites-10}

* AEM geeft onverwacht gedrag weer wanneer een gebruiker `/unpublish/create` -versie probeert te publiceren van een pagina die is vergrendeld door een andere gebruiker. NPR-19249; hotfix voor CQ-4215298 en CQ-4203856
* Tijdens het handmatig promoten van de geneste opstart wordt de onderliggende pagina verwijderd. NPR-19704
* De persistentie kwesties wanneer de opslag ContextHub de standaardpersistentielaag tijdens initialisatie overschrijft. NPR-19979: Hotfix voor CQ-4218399
* Inhoudsfragmenten overlappen met andere knoppen. NPR-19980: Hotfix voor CQ-4221519
* De sitepagina wordt niet weergegeven bij weergave met een alias in SiteAdmin. NPR-20053: Hotfix voor CQ-4221478
* Fout bij het publiceren van een pagina van Actieve kopie die naar een pagina van de Importeur in de Campagnes van Adobe wijst. NPR-2006: Hotfix voor CQ-4220846

### Platform {#platform-8}

* Upgrade van Apache POI naar versie 3.16 ter ondersteuning van het opnemen van achtergrondafbeeldingen van PPT-dia&#39;s in uitvoeringen. NPR-18286
* Rendering geeft problemen met Internet Browser 11 en Edge wanneer meerdere middelen in dezelfde map worden geüpload. NPR-20062

### Integratie {#integration-11}

* Aangepast bestand at.js publiceert niet wanneer het wordt geopend met de anonieme gebruiker. NPR-19542: Hotfix voor CQ-4219592
* Het migreren Analytics bestaande geloofsbrieven aan Authentificatie WSSE. NPR-1962

### Brand Portal {#brand-portal}

* Publicatietags van AEM naar Brand Portal inschakelen vanuit de tagbeheer-/tagingconsole. NPR-20271

## Forms {#forms-11}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

### Forms-invoegtoepassing {#forms-add-on-package-11}

#### Correspondentenbeheer {#correspondence-management-4}

* Functionaliteit ingeschakeld om te zoeken naar werkelijke tekst in documentfragmenten wanneer een voorvertoning van een letter wordt weergegeven. NPR-19712

#### Adaptieve Forms {#adaptive-forms-8}

* Enhanced Adaptive Forms to attach PDF as attachments in Safari. Als u dezelfde mogelijkheden in bestaande formulieren wilt ondersteunen, wijzigt u de configuratie in de bijlage-widget en in &quot;Ondersteunde bestandstypen&quot; de waarde application/pdf in plaats van .pdf. NPR-19623

#### Forms Manager {#forms-manager-1}

* Als validationState ongedefinieerd is in een veld van een adaptief formulier en de gebeurtenis elementFocusChanged plaatsvindt, wordt een foutgebeurtenis (errorState) geretourneerd aan de Adobe Analytics-server. NPR-19513

### Forms JEE Installer {#forms-jee-installer-11}

#### Kern {#core-3}

* De manager van de Verbinding is niet beschikbaar tijdens de sluiting. JBoss® snijdt de JDBC-afhankelijkheid weg voordat de auteur EAR wordt gedeactiveerd, wat leidt tot corruptieproblemen. NPR-19703

## Functiepakketten inbegrepen {#feature-packs-included-1}

* Verbeterde miniatuurcorrectie en transparantie in Dynamic Media. NPR-15207

## SDAB-pakketten en -inhoudspakketten opgenomen in GVB9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Lijst met inhoudspakketten bijgewerkt in AEM 6.2SP1-GVB9

[Bestand ophalen](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Lijst met OSGi-bundels bijgewerkt in AEM 6.2SP1-GVB9

[Bestand ophalen](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-GVB8 is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Tags toevoegen aan aangepaste gebruikerssjablonen in de Adobe-e-mailsjabloonservice.
* Verbeteringen aan TouchUI-knoppen in de bureaubladtoepassing.
* Schakel de knop Verzenden uit als u klikt om te voorkomen dat meerdere formulieren op een vertaalpagina worden verzonden.
* De gevormde veelvoudige componenten van RTE in een dialoogdoos.
* Versterkte ReferenceUpdates in Live Copy.
* Ingeschakelde hoofdlettergevoelige zoekfunctionaliteit voor inhoud van documentfragment.
* Lijst met Linux®-bibliotheken toegevoegd aan de installatiedocumentatie van AEM Forms.

### Assets {#assets-11}

* Problemen met het toepassen van het filter Onderzoek op slimme verzamelingen in Safari. NPR-19511
* Metagegevens van het trefwoord PDF worden niet correct geëxtraheerd en gewijzigd wanneer er meerdere trefwoorden zijn gekoppeld aan een element PDF. Om het probleem op te lossen, is de eigenschap voor metagegevens van het veld Onderwerp verwijderd voor PDF Assets. U kunt echter wel het metagegevensschema bewerken om een tekstveld met meerdere waarden toe te voegen voor het veld Onderwerp. NPR-19126
* De workflowmeldingsservice codeert de koppelingen niet in e-mail, waardoor ze niet kunnen worden geladen nadat gebruikers erop hebben geklikt. NPR-19490: Hotfix voor CQ-4218055
* Kan geen volledige lijst met pagina&#39;s/middelen laden in de kolomweergave met Chrome. NPR-19458: Hotfix voor CQ-4214248
* Het onjuiste pictogram Uittijd wordt weergegeven in het AEM Inbox wanneer de workflow &quot;Verzoek om activering&quot; wordt geactiveerd. NPR-19365: CQ-4216174
* Problemen met sorteren in de lijstweergave. NPR-19217: CQ-95602
* Als u de titel of miniatuurafbeelding wijzigt in de instellingen van de elementenmap, worden de oorspronkelijke groep en machtigingen van de map overschreven. NPR-19283: Hotfix voor CQ-4216080
* `Windows 10` -werkstations schakelen automatisch over op de aanraakmodus, waardoor sommige knoppen niet meer werken. NPR-19183

### Sites {#sites-11}

* Kwesties met het hebben van veelvoudige componenten RTE in een dialoogdoos. NPR-1931: NPR-19587
* Automatische versieopruiming in vanilla AEM 6.2 werkt slechts eenmaal nadat VersionManagerImpl is geïnitialiseerd. NPR-19315: Hotfix voor CQ-4217175
* Werkstroominstantie blijft vastzitten in de stap voor de workflow &quot;Salesforce.com exporteren&quot;. NPR-1922: Hotfix voor CQ-4212976
* Pagina&#39;s die zijn gemaakt met Live kopieën kunnen niet worden bewerkt. NPR-18967
* ReferencesUpdateAction kan geen koppelingen bijwerken naar een geneste LiveCopy met een gewijzigde hiërarchie. NPR-18715: Hotfix voor CQ-4214105

### Platform {#platform-9}

* De Adobe-e-mailsjabloonservice voegt codes toe aan aangepaste gebruikerssjablonen. NPR-19190: Hotfix voor CQ-4217113

### Projecten {#projects-2}

* Projecteditors kunnen geen elementen kopiëren/plakken in de map met projectmiddelen. NPR-19619
* Kan voorvertoning voor vertaalprojecten niet genereren na installatie van 6.2 SP1-GVB1. NPR-16481: CQ-4204655

### Integratie {#integration-12}

* Toegangseigenschappen voor artikelen die onjuist zijn ingesteld in Adobe Digital Publishing Solution op klassieke UI. NPR-1936
* Trage weergave van miniaturen vanwege artikelen op volledige grootte in AEM artikelconsole. NPR-19086: CQ-4217148
* Onjuist gedrag van automatisch vouwen tijdens het aanpassen van aanbiedingen via Campagne als gebruikers toegang hebben tot meerdere gebieden. NPR-19290: Hotfix voor CQ-4218029
* Het doeldialoogvenster wordt niet weergegeven in de doelmodus wanneer een doelmodule meerdere keren wordt bewerkt en opgeslagen. NPR-19144: Hotfix voor CQ-4216708

### Workflow {#workflow-2}

* Gebruikers kunnen meldingen in Postvak IN niet filteren op gebruiker/groep in de klassieke gebruikersinterface van Inbox. NPR-1912: Hotfix voor CQ-4215374
* Met Afbeeldingskaart blijven de geselecteerde coördinaten in de HTML-afbeeldingscomponent niet behouden. NPR-18911: CQ-4211584

## Forms {#forms-12}

* AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-12}

* Wanneer inhoud van Microsoft® Word of een Webbrowser aan de Redacteur van de Tekst van de Manager van de Correspondentie wordt gekopieerd, wordt de stijl verloren. NPR-19530
* Inhoud zonder regeleinde in de Teksteditor kan niet worden omlopen. NPR-19481
* Functionaliteit ingeschakeld om te zoeken naar werkelijke tekst in documentfragmenten wanneer een voorvertoning van een letter wordt weergegeven. NPR-17792: Hotfix voor CQ-4214501

#### Correspondentenbeheer {#correspondence-management-5}

>[!NOTE]
>
>Deze zoekfunctie voor tekstfragmenten kent een aantal beperkingen:-
>
>* De inhoud van het Fragment van het document is case-sensitive en de titels zijn niet case-sensitive.
>* De zoekresultaten worden niet gemarkeerd wanneer een deel van het gezochte woord in een andere opmaak staat of een speciaal teken bevat zoals &quot; of &quot; of &quot; of \.
>* Zoeken werkt niet voor dynamische inhoud in het documentfragment (zoals elementwaarden voor gegevenswoordenboeken of waarden voor variabelen).

#### Forms Manager {#forms-manager-2}

* De eigenschappen van het XML-schema van Adaptive Forms kunnen niet worden bewerkt nadat GVB6 op AEM 6.2 is toegepast. Hotfix voor CQ-4219684
* Bij het opnieuw opstarten van de server wordt niet begonnen met alle services van de AEM Forms Manager-kernbundel. Hotfix voor CQ-4217014

### Forms JEE Installer {#forms-jee-installer-12}

#### LCM installeren {#install-lcm-2}

* In het beheerdersscherm op Microsoft® Windows wordt versie 6.0 weergegeven na de installatie van GFP6. Hotfix voor CQ-4217573

## Functiepakketten inbegrepen {#feature-packs-included-2}

* Verbeteringen aan TouchUI-knoppen in de bureaubladtoepassing. NPR-18676

## OSGi-bundels in GVB8 {#osgi-bundles-included-in-cfp}

Lijst van OSGi-bundels bijgewerkt in AEM 6.2SP1-GVB8

[Bestand ophalen](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Lijst met inhoudspakketten bijgewerkt in AEM 6.2SP1-GVB8

[Bestand ophalen](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulatief Pak 6.2 SP1-GVB7 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Gedragswijziging bij het weergeven van titels op afbeeldingskaart voor afbeelding met dc: eigenschap title ingesteld op String (multifield).
* Oplossingen in prestatieproblemen met Dynamic Media-Cloud Servicen, Touch UI en de interface voor beveiliging.
* Oplossingen in Apache Felix HTTP Bridge 3.0.8
* BLR (binary-less Replication) tussen de auteur- en publicatieomgeving is opgelost.
* De steun voor het dossier van de Bibliotheek van het Doel AT.JS, een implementatiebibliotheek voor cliënt-zijintegratie met Adobe Target, wordt ontworpen voor zowel typische Webimplementaties als enig-paginatoepassingen.
* Verbeterde AEM door een door de gebruiker configureerbare time-outperiode voor de verbinding voor Analytics, DTM en Target in te voeren.

### Assets {#assets-12}

* Tijdens het testen van videoinvoer met AEM 6.3 geconfigureerd met Dynamic Media-Cloud Servicen wordt de uitzondering &#39;Te veel geopende bestanden&#39; veroorzaakt. NPR-18734; hotfix voor CQ-4211407
* De vanity URL-instelling voor elementen op een pagina werkt niet nadat de AEM opnieuw is gestart. NPR-18634; hotfix voor graniet-18085
* In TouchUI wordt de knop Publish weergegeven voor gebruikers zonder toestemming om elementen te publiceren. NPR-18620; hotfix voor CQ-4214042
* De optie voor dynamische vertoning is niet aanwezig in het dialoogvenster voor downloaden van een element als de licentieovereenkomst eenmaal voor dit element is ingesteld. NPR-18607; hotfix voor CQ-4212342
* Dynamische uitvoering kan niet worden gedownload voor elementen die spaties in hun namen opnemen. NPR-18571; hotfix voor CQ-4211738
* Kan niet meer dan één gebruiker opslaan wanneer u de elementenmap deelt met de creative cloud. NPR-18489; hotfix voor CQ-103297
* dc: title &amp; dc: beschrijving verandert niet in een waarde voor meerdere velden in crx/de. NPR-18474; hotfix voor CQ-4209086
* De bewerking Elementen verplaatsen leidt tot een verslechtering van de prestaties. NPR-18346
* Er worden geen items weergegeven in de tijdlijn wanneer deze wordt geopend met de standaardoptieset Alles tonen. NPR-18302; hotfix voor CQ-4211957
* Er treedt een fout op wanneer een tekstbestand met ASCII/UTF-8-codering naar AEM Assets wordt geüpload en het genereren van miniaturen mislukt. NPR-18006: GVB voor CQ-4209345
* Publish-actieknoppen zijn ook zichtbaar wanneer de gebruiker geen replicaattoegang heeft. NPR-17353; hotfix voor CQ-4209269
* Zowel Sitebeheerder als Misc admin werken niet wanneer minificatie is ingeschakeld met min:gcc;obfuscate=true. NPR-18593; hotfix voor CQ-4209220
* Aangepaste menu-items worden pas weergegeven wanneer het scherm telkens wordt vernieuwd. NPR-18500; hotfix voor CQ-4213581
* Upgrade moment.js naar 2.10.6. NPR-18596; hotfix voor graniet-11881
* Wanneer u machtigingen voor DM-macro&#39;s toepast, wordt de weergave voor de Admin-gebruiker verbroken. NPR-18544; hotfix voor CQ-4211729
* Publish Later voor elementen genereert Illegal ArgumentException. CQ-4214532

### Sites {#sites-12}

* Op een actief-actieve auteurcluster met MongoDB, beide auteurs proberen om replicatie voor de zelfde inhoud teweeg te brengen, wanneer de tijd de On-time reeks voor de inhoud bereikt. NPR-18708; hotfix voor CQ-4210982
* NPE wanneer het bewegen van een middel met een verwijzing die geen jcr heeft: inhoudsknoop. NPR-18664
* Placeholders zijn niet zichtbaar in een pagina die veelvoudige componenten Parsys bevat. NPR-18645; hotfix voor CQ-110253
* Gelijktijdige problemen in AbstractCopyMoveCommand. NPR-18591
* Wanneer het kopiëren van tekst aan een component Parsys van een andere AEM instantie, wordt Parsys gecreeerd zonder enige resourceType reeks. NPR-18511; hotfix voor CQ-4212306

### Platform {#platform-10}

* JCR Installer werkt de bundelversie niet bij na de installatie van het pakket. NPR-18728; hotfix voor NPR-15135
* BLR (Binaryless Replication) werkt niet met binaire bestanden zonder de auteur- en publicatieomgeving. NPR-18704
* Apache Felix Http Bridge Resolution request in an AEM environment. NPR-18297
* De replicatie mislukt wanneer meerdere pagina&#39;s met een vergelijkbare structuur tegelijkertijd met de distributie van de inhoud worden gerepliceerd. NPR-18665; hotfix voor graniet-13712
* Verspreidingspakketten opbouwen en niet zelfgereinigd. NPR-18601; hotfix voor graniet-16183

### Integratie {#integration-13}

* Het bekijken van aanbiedingen die van bibliotheekomslagen worden gepubliceerd resulteert in NPE. NPR-18732; hotfix voor CQ-4214593
* De begin- en einddatum voor een activiteit wordt niet bijgewerkt in JCR en Target wanneer deze worden gewijzigd van een specifieke datum in &quot;Indien geactiveerd/gedeactiveerd.&quot; NPR-18612; hotfix voor CQ-104831
* De integratie van Analytics met AEM heeft geen verbinding of contactdoosonderbrekingen die voor de httpclient verbindingen worden geplaatst. NPR-18497
* Voor de DTM-integratie met AEM zijn geen time-outs voor verbindingen of sockets ingesteld voor de httpclient-verbindingen. NPR-18495
* Voor de doelintegratie met AEM zijn geen time-outs voor verbindingen of sockets ingesteld voor de httpclient-verbindingen. NPR-18494
* De doelactiviteit wordt gedeactiveerd na het toevoegen van een extra ervaring. NPR-18227; hotfix voor CQ-4201895

### WCM-stichtingscomponenten {#wcm-foundation-components-7}

* Bij afbeeldingen met hyperlinks blijven de geselecteerde coördinaten in de HTML-afbeeldingscomponent niet behouden. NPR-18530; hotfix voor CQ-4211584

### Vertaling {#translation-5}

* De resultaten van het vertaalonderzoek omvatten geen namen van vertaalprojecten. NPR-18224; hotfix voor CQ-4210658

### Brand Portal {#brand-portal-1}

* Publicatietags van AEM naar Brand Portal inschakelen vanuit de tagbeheer-/tagingconsole. CQ-4212165

## Forms {#forms-13}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-13}

#### Correspondentenbeheer {#correspondence-management-6}

* Correcte gegevens worden pas in het bewerkingspaneel weergegeven als het fragment is opgeslagen. NPR-19092
* Het toevoegen van documentfragment aan een letter kost veel tijd. NPR-18958
* Als een XML-declaratie bestaat in een XML-bestand met gegevens en de uitvoering van een letter wordt geïnitieerd via een POST-aanvraag, worden de gegevens niet weergegeven in de corresponderende letter. NPR-18870
* Er worden geen auditlogboeken gegenereerd voor acties die op CM-middelen worden uitgevoerd. NPR-16618

>[!NOTE]
>
>Installeer dit GFP Add-on Pakket niet als u met de hieronder twee kwesties wordt beïnvloed:
>
>* Met Plakken van Word/Web kopiëren naar de CM-teksteditor wordt de inhoud van regeleinden weergegeven. NPR-19530
>* Inhoud zonder regeleinde in de CM Text Editor kan geen omloop hebben. NPR-1949
>

#### Adaptieve Forms {#adaptive-forms-9}

* Wanneer u een deelvenster voor herhaalbare deelvensters toevoegt, wordt de waarde van het vervolgkeuzeveld in het vorige deelvenster verwijderd. NPR-1872
* Aangepaste formuliervelden die zijn gemarkeerd om alleen gehele getallen te accepteren, accepteren ook enkele speciale tekens van het numerieke toetsenblok. NPR-18680
* Een script om de knoptitel te wijzigen bij de initialiseringsgebeurtenis van het hoofddeelvenster van de hulplijn werkt niet. NPR-18476
* De schuifbalk wordt niet weergegeven in het rechterdeelvenster voor regels die zijn gemaakt in de Regeleditor. NPR-18716

#### AEM Forms App {#aem-forms-app}

* Forms wordt niet correct gerenderd in AEM Forms App wanneer deze zich in de offline modus bevindt of niet is verbonden met het netwerk. CQ-4218368

### Forms JEE Installer {#forms-jee-installer-13}

#### PDFG-service {#pdfg-service-3}

* PDF Generator kan geen PDF-documenten met opgegeven bladwijzerniveaus maken. Hotfix voor CQ-4211102

## OSGi-bundels in GVB7 {#osgi-bundles-included-in-cfp-1}

Lijst met OSGi-bundels bijgewerkt in AEM 6.2SP1-GVB7

[Bestand ophalen](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Lijst met inhoudspakketten bijgewerkt in AEM 6.2SP1-GVB7

[Bestand ophalen](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-GVB6 is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Efficiënt beheer van verborgen onderdelen in de lay-outmodus van de tablet.
* Maak kennis met snelle acties op hybride apparaten.
* Synchronisatieproblemen op componentniveau oplossen met Live kopieën.

### Assets {#assets-13}

* Een klant wordt geblokkeerd wanneer een gebruiker die niet de vereiste toestemming heeft, probeert om verrichting op activa te bewegen. NPR-18330; hotfix voor CQ-4212560
* Het samenvoegen van meerdere configuraties voor slimme-inhoudservices veroorzaakt bruikbaarheidsproblemen. NPR-18273; hotfix voor CQ-4201557
* Uitchecken/workflows zijn niet beschikbaar in de tijdlijnconsole na ongeveer. 80 fragmenten worden toegevoegd aan de map Assets. NPR-18257; hotfix voor CQ-4211214 en NPR-18251; hotfix voor CQ-4211216.
* Systeem loopt vast als onvoldoende geheugen en heeft geen paginering tijdens Assets-rapporten. NPR-17865; hotfix voor CQ-4209759
* De gepubliceerde video kan niet worden afgespeeld op gecodeerde video-elementen. NPR-17849; hotfix voor CQ-4210739
* Er wordt geen miniatuur voor de PDF gegenereerd. NPR-17831, NPR-17750; hotfix voor CQ-4210547
* Met de Adobe CQ DAM-verloopmeldingstaak worden verlopen middelen niet gedeactiveerd. NPR-17666; hotfix voor CQ-107766
* De vervalactiviteiten van Assets stoppen als een actief geen toegewezen eigenaar heeft. NPR-17665; hotfix voor CQ-4197946
* Een null pointer-uitzondering wordt weergegeven wanneer een elementmap met meer dan 150 binnenkomende verwijzingen wordt verplaatst. CQ-4200981

### Sites {#sites-13}

* Personalization werkt slechts voor eerste IP wanneer de segmentatieregel voor een IP waaier wordt geplaatst. NPR-18121; hotfix voor CQ-83767
* Aanmelding mislukt vanwege NumberFormatException wanneer de eigenschap historyShow is ingeschakeld. NPR-18073; hotfix voor CQ-101965
* Verwijderde pagina&#39;s die zijn gemarkeerd, zijn zichtbaar in de aanraakinterface. NPR-18025; hotfix voor CQ-86694
* Prestatieproblemen bij het laden van een pagina met een groot (2000+) publiek. NPR-17884; hotfix voor CQ-4209567
* U kunt geen afbeelding selecteren nadat u een andere afbeelding op de pagina hebt verwijderd. NPR-17711; hotfix voor CQ-4201323

### Platform {#platform-11}

* Aanraakbesturingselementen voor UI zijn verborgen voor gebruikers die over de vereiste machtigingen beschikken. NPR-17945; hotfix voor CQ-4211231
* Japanse tags ontbreken in veld tagkiezer. NPR-17768; hotfix voor CQ-4210456
* De query getsize() retourneert onjuiste resultaten wanneer FastQuerySize is ingeschakeld. NPR-18018
* De webconsole in de stand-byinstantie is niet toegankelijk. NPR-17861; hotfix voor graniet-14582

### Commerce {#commerce-2}

* Het doorlopen van de vraag gebeurt wanneer een catalogusblauwdruk geen bepaalde voorwaarde voor een sectie heeft. NPR-18229; hotfix voor CQ-4211924

### Gemeenschappen {#communities-2}

* PollingImporterImpl. vertragingen AEM sluiting. NPR-18298; hotfix voor CQ-96133

### Integrations {#integrations}

* Opgeloste AEM de componentenfouten van het Onderzoek die kunnen voorkomen wanneer AEM Cliënt 3.1 van HTTP van Dag OSGI met een Volmacht wordt gevormd die de Authentificatie van de Samenvatting vereist. NPR 18128
* Selectievakje ontbreekt, zodat u de overerving kunt herstellen. NPR-17753; Hotfix-verzoek voor CQ-4210139
* Gebruikers kunnen de prioriteit niet instellen wanneer zij zich richten op één component met meerdere activiteiten. NPR-18658; hotfix voor CQ-4210727
* Gebruikers kunnen niet door de map /etc/segmentation bladeren om een publiek te selecteren dat is gemaakt onder de map /etc/segmentation/group1. NPR-1852

### Beveiliging {#security-1}

* De wizard Element verplaatsen loopt vast als de gebruiker geen schrijfmachtigingen heeft voor de doelmap. NPR-18300
* Verzoek om een geüpgrade versie van org.apache.sling.servlets.post servlet (2.3.22) in de Apache Sling API te gebruiken om een XSS-kwetsbaarheid te voorkomen. NPR-18963

### Vertaling {#translation-6}

* Indiening van de elementenpagina hoeft voor een vertaalproject niet opnieuw te worden uitgevoerd totdat het project is voltooid. NPR-18249; hotfix voor CQ-4209908

### WCM-stichtingscomponenten {#wcm-foundation-components-8}

* Kan de component WCM foundation Iparsys niet gebruiken in bewerkbare sjablonen. NPR-18223; hotfix voor CQ-4210384
* Met Afbeeldingskaart blijven de geselecteerde coördinaten in de HTML-afbeeldingscomponent niet behouden. NPR-18032; hotfix voor CQ-4211584
* Wanneer een HTML-afbeeldingscomponent wordt gerenderd, wordt de naam van de bestandsnaam in de URL gewijzigd, waardoor een verbroken URL ontstaat. NPR-17908; hotfix voor CQ-4211587
* Kan pagina-eigenschappen niet afsluiten nadat wijzigingen zijn aangebracht. NPR-17832; hotfix voor CQ-96110

## Forms {#forms-14}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Voor details, zie [ de Versies van AEM Forms ](aem-forms-releases.md).

### Forms-invoegtoepassing {#forms-add-on-package-14}

**het Beheer van de Correspondentie**

* Het gegevenswoordenboek wordt herhaaldelijk gelezen tijdens het renderen van letters. NPR-18482, Hotfix voor CQ-4210805
* JavaDocs toegevoegd voor de klasse com.adobe.livecycle.content. NPR-18467
* Bij het maken van een letter wordt de beschrijving van de letter niet opgeslagen. NPR-18039
* Wanneer een tekstmodule wordt opgeslagen en een expressie in de tekstmodule geen openings- of afsluitende expressietags bevat, wordt geen foutbericht weergegeven. In de tekstmodule wordt een foutbericht weergegeven en kan de letter niet worden weergegeven. NPR-17798
* Onverwachte fouten worden gezien in logboeken bij installatie van een add-on pakket. NPR-18295

**de Manager van Forms**

* De gebruikersinterface van AEM Forms bevat alle elementen in de oudste eerste volgorde. Gebruikers kunnen de middelen niet opnieuw rangschikken in de nieuwste eerste volgorde. NPR-18451

### Forms JEE Installer {#forms-jee-installer-14}

**de Dienst van de Output**

* Verbeterde prestaties van de uitvoerservice voor AEM formulieren 6.2. NPR-1803

**de Dienst van Handtekeningen**

* Kan een PDF-document niet ondertekenen met een externe Hardware Security Module. NPR-18017

## OSGi-bundels in GVB6 {#osgi-bundles-included-in-cfp-2}

Lijst van OSGi-bundels bijgewerkt in AEM 6.2SP1-GVB6

[Bestand ophalen](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Lijst met inhoudspakketten bijgewerkt in AEM 6.2SP1-GVB6

[Bestand ophalen](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-GVB5 is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Verschillende gebruikersinterfaceproblemen met het delen, verplaatsen, publiceren en downloaden van middelen zijn opgelost.
* Verbeterde capaciteit van het dialoogvenster Verplaatsen bij de weergave van middelen waarnaar wordt verwezen.
* Verschillende problemen met WCM-componenten en -workflows zijn opgelost, zoals Unpublish en Version Purge.
* Verbeterde responsiviteit van de actiebalk bij het weergeven van werkbalkhandelingen en koraalcomponenten.

### Assets {#assets-14}

* Prestatieverbeteringen in de functie Publiceren naar Brand Portal. NPR-17189; hotfix voor CQ-4204150
* Als u middelen deelt met de optie Koppeling delen, wordt er geen zip-bestand met een platte mapstructuur gemaakt om te downloaden. NPR-17513; hotfix voor CQ-4209381
* Als u een element selecteert in DAM en op Publish klikt, wordt de optie Publish naar Brand Portal niet weergegeven op de pagina Asset Details. NPR-17351; hotfix voor CQ-94905
* In de DAM-workflowstappen moeten binaire streams die zijn opgehaald van Session of ResourceResolver, worden gesloten in een definitief blok. Zo zorgt u ervoor dat er geen bronlekken optreden. NPR-17385; hotfix voor CQ-4209452
* Als u een Word-document in DAM uploadt, resulteert dit in een null pointer-uitzondering en blijft de werkstroominstantie vastzitten in de status Running. NPR-17160; hotfix voor CQ-4207358
* De knoppen Delen, Verplaatsen, Publish en Downloaden zijn zichtbaar voor verlopen elementen op de pagina Metagegevenseditor voor gebruikers die geen beheerder zijn. NPR-16903; hotfix voor CQ-101440/CQ-104535
* Handelingen als Delen, Verplaatsen, Publish en Kopiëren moeten zichtbaar zijn voor gebruikers met beheerdersrechten in de Assets-console. NPR-16902; hotfix voor CQ-4207111

### Sites {#sites-14}

* Tijdens het verplaatsen van een pagina met gebruik van de klassieke modus en de aanraakinterface, bevat het dialoogvenster Verplaatsen geen verwijzingen naar een waarde hoger dan 150. Hierdoor kunnen gebruikers deze verwijzingen niet bijwerken en de pagina opnieuw publiceren. Dit probleem is verholpen door een eigenschap voor de klassieke UI te introduceren: &#39;maxRefNo&#39; die kan worden geconfigureerd op het knooppunt voor sitebeheer: `'/libs/wcm/core/content/siteadmin'` . This property specifies the maximum number of references (default value 150) that is displayed before a large move operation. Als een pagina meerdere verwijzingen bevat, worden deze niet weergegeven in het dialoogvenster movePage. Deze configuratie werkt ook voor beheer van dammen en voor beheer van misc door configuratie toe te passen op de knooppunten: `'/libs/wcm/core/content/damadmin'` respectievelijk `'/libs/wcm/core/content/miscadmin'` . NPR-17222; hotfix voor CQ-85878

* Wanneer u werkt met WCM-componenten, worden hyperlinks met spaties verwijderd uit de Touch UI Rich Text Editor. NPR-17698, NPR-17570; hotfix voor CQ-4206768
* Tijdens het activeren van de Request for Unpublication-workflow vanuit pagina-eigenschappen worden JavaScript-fouten weergegeven voor gebruikers zonder replicatierechten. NPR-17294; hotfix voor CQ-102064
* Wanneer een HTML-afbeeldingscomponent wordt gerenderd of geëxporteerd, verandert de URL in een getal, waardoor de bestandsnaam wordt gewijzigd. Hierdoor worden koppelingen verbroken. NPR-17245; hotfix voor CQ-59616
* Als u een opstart verwijdert in een geneste opstart, worden subopstarters wees. NPR-17228; hotfix voor CQ-4202639
* Bij uitvoering van Version Purge in AEM 6.2 met Oak 1.4.13 wordt een voortdurende waarschuwing weergegeven in de logboeken. NPR-17391; hotfix voor CQ-4206870
* Na het installeren van hotfix of een verbetering voor de component ContextHub, beschrijft het inhoudspakket alle segmenten in /etc/segmentation/contexthub, resulterend in een verlies van alle segmenten van douaneContextHub. NPR-17250; hotfix voor CQ-79958
* Tijdens het uitvoeren van een workflow met geneste groepen als workflowgebruikers zorgt de WorkflowStatusProvider (pageinfo.json) ervoor dat de workflowinstantie vergrendeld wordt. NPR-17555; hotfix voor CQ-4202056
* Wanneer u de WCM-Page editorcomponenten gebruikt, is er aan het einde van de pagina in de aanraakmodus voor gebruikersinterface van de auteur veel ruimte beschikbaar. NPR-17510; hotfix voor CQ-4205441
* Als u een HTML-afbeeldingscomponent rendert of exporteert, verandert de URL in een getal, waardoor verbroken koppelingen ontstaan. NPR-17245; hotfix voor CQ-59616

### UI {#ui}

* Als u een element selecteert en op Gereedschappen voor ontwikkelaars klikt, worden de werkbalkhandelingen niet altijd in trage verbindingen in de actiebalk weergegeven en moet de pagina opnieuw worden geladen. NPR-17568; hotfix voor CQ-108365
* De actiebalk dient te worden aangepast zodat twee containers worden gebruikt: koraal-actionbar-primair en coral-actionbar-secundair, in plaats van de koraal-actionbar-container. NPR-17591; hotfix voor GRANITE-15225

### Mobiel-op-aanvraag {#mobile-on-demand-2}

* Gebruikers met de machtiging Alleen-lezen voor de AEM Mobile-toepassing kunnen geen voorvertoning van inhoud weergeven via de pagina AEM Mobile Content Management. NPR-17390; hotfix voor CQ-4209690

### Beveiliging {#security-2}

* XSS-kwetsbaarheid in de uitvoer die wordt gegenereerd door HTMLRendererServlet. NPR-17136
* Verzoek om AEM versiedetectie in AEM pagina van de Beelden van de Syndicatie van het Web te verhinderen. NPR-16219

### Forms {#forms-15}

#### Forms-invoegtoepassing {#forms-add-on-package-15}

AEM Forms-oplossingen worden geleverd via invoegpakketten en andere patchinstallatieprogramma&#39;s die bij de release worden geleverd. Zie AEM Forms-releases voor meer informatie.

**Aangepaste Forms**

* Voor een adaptief formulier met bijlage worden dubbele vermeldingen voor de afSubmissionInfo-tags gemaakt in de verzonden XML wanneer het formulier voor de tweede keer wordt verzonden. NPR-17364
* Als u tijdens het gebruik van de Google Chrome-browser een bijlage uit een formulier verwijdert en probeert dezelfde bijlage opnieuw te koppelen, treedt er een fout op. NPR-17297
* Als er geneste, herhaalbare, lazy geladen deelvensters zijn in op XSD gebaseerde of op geen formulier gebaseerde adaptieve Forms, blijven de waarden die in het formulier zijn ingevuld niet behouden in het Document of Record (DOR). NPR-17176
* Fouten die in het foutenlogboek voor de Redacteur van de Regel worden getoond zouden in het vangstblok van een poging/vangstblokJavaScript code moeten worden toegevoegd. NPR-16757
* Als u op een bestandsbijlage in een formulier klikt, wordt een browserconsolefout gegenereerd en wordt de voorvertoning van de bijlage niet weergegeven. NPR-17174

**het Beheer van de Correspondentie**

* De functionaliteit van de gebruikersinterface Correspondentie maken wordt afgebroken als er inline tekst of een lege regel wordt toegevoegd aan de gebruikersinterface. NPR-17748
* De browser flikkert wanneer een brief voor het uitgeven wordt geopend. NPR-17576
* Wanneer u externe functies toevoegt in gegevenswoordenboekelementen die zijn berekend en het aantal functies groter is dan de lengte van het tabblad waarop externe functies worden weergegeven, wordt de schuifbalk niet weergegeven op het tabblad. NPR-17359
* De API-methode `com.adobe.icc.services.api.LetterInstanceService` voor importeren werkt niet. NPR-17922, 16008
* Een variabele die wordt toegevoegd in een tekstmodule, is niet zichtbaar in het deelvenster Gegevensbinding tijdens het bewerken van een letter. NPR-17940
* De interface voor het beheer van correspondentie wordt niet gestart wanneer een HTML-verzendactie de methode POST gebruikt. NPR-17595

**de Manager van Forms**

* Als een adaptief formulier is geconfigureerd voor AB-tests, wordt de test niet gestart als u op AB Testing starten klikt. Er wordt dan een browserconsolefout gegenereerd. NPR-17838

**de Dienst van Forms**

* De in de statische codeanalyse van OSGI-formulieren vermelde problemen moeten worden vastgesteld. NPR-13951

#### Forms JEE Installer {#forms-jee-installer-15}

**de Dienst van de Output**

* Het gebruik van AEM formulieren 6.2 Output Service voor het samenvoegen van een specifiek formulier met een XML-gegevens kost 20 keer meer tijd. Het is nu opgelost in Windows- en Linux®-omgevingen. NPR-17501

**installeer LCM**

* Nadat u AEM Forms 6.2 GM hebt geïnstalleerd en de AEM 6.2 GFP hebt toegepast, wordt door Configuratiebeheer van het LiveCycle een ongewenste puntkomma weergegeven in de versiegegevens en wordt de installatiedatum van de patch niet bijgewerkt. NPR-1432

**Beheer van het Proces**

* De TaskContext-variabele wordt niet gevuld voor AEM Forms-processen. CQ-421857

#### AEM Forms JEE-bundelpakket {#aem-forms-jee-bundles-package}

* De mogelijkheden van formuliergebruikers moeten hetzelfde zijn, ongeacht of ze de UI-console van JEE Admin of de OSGi-console gebruiken. NPR-17670

### Functiepakketten in GVB5 {#feature-packs-included-in-cfp}

**Forms JEE Pakket**

Process Management - HTML Workspace

* Tijdens het toewijzen van een werkruimtesstap moet op het tabblad Werkruimtelijsten een teller voor de bijlagen of notities worden weergegeven als er meer dan één bijlage of notitie is. NPR-1771
* Verzoek om ondersteuning van Office 365 in AEM JEE Forms voor e-mailmogelijkheden in de formulierworkflow. NPR-1386

**Forms toe:voegen-op Pakket**

Correspondentenbeheer

* Tijdens het bewerken van fragmenten in de Teksteditor tijdens een lettertypevoorvertoning, moet de verwerkte tekst worden weergegeven voor bewerking in plaats van de inline-voorwaarden die in fragmenten worden gebruikt. NPR-15748, NPR-17504

### OSGi-bundels in GVB5 {#osgi-bundles-included-in-cfp-3}

Lijst met OSGi-bundels bijgewerkt tussen AEM6.2 SP1-GVB5

[Bestand ophalen](assets/do-not-localize/cfp5_osgi_bundles.txt)

Lijst met inhoudspakketten bijgewerkt tussen AEM6.2 SP1-GVB5

[Bestand ophalen](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulatief Pak 6.2 SP1-GVB4 van de Moeilijke situatie is een belangrijke update die zeer belangrijke klantenmoeilijke situaties omvat die sinds de algemene beschikbaarheid van AEM 6.2 SP1 worden vrijgegeven.

De belangrijkste kenmerken van dit Cumulative Fix Pack zijn:

* Oplossingen in elementen voor Camera Raw bestandsuitvoering, tijdlijnweergave en afdrukstand
* Verbetering van

   * WCM-lanceringen voor sites
   * Workflow voor projecten
   * ContextHub-componenten

* Oplossingen voor campagne, mobiel op aanvraag en vertalen
* Verbeteringen op gebied van bruikbaarheid in de Editor voor adaptieve formulieren
* Verbeterde Inline Condition Editor voor Correspondentenbeheer in formulieren
* Oplossingen voor procesbeheer en uitvoerservice voor AEM formulieren op JEE
* Aan Forms Designer gerelateerde correctie voor Scripteditor

### Platform {#platform-12}

* Het toevoegen van of het aanpassen van kolommen aan **Assets OmniSearch** resultaten door binnen te bedekken `/apps` werkt niet. NPR-16737: Hotfix voor CQ-4206785
* Het **hulpmiddel van de Diagnose** pagina werkt niet na een op zijn plaats verbetering van AEM 6.1 SP2 aan AEM 6.2 SP1. NPR-17121; hotfix voor CQ-4196786
* HTL: Als u een Forum selecteert, een Onderwerp maakt en een Post, voegt de eigenschap `Sightly SightlyCompiledScript` een onjuiste `addSelectors` -eigenschap toe aan `RequestDispatcherOption` . NPR-17008: Hotfix voor GRANITE-16384

* Extra ondersteuning voor `CRON expressions` in `ManagedPollConfigs` die door de `ReportImporter` wordt gebruikt. NPR-16608: Hotfix-verzoek voor CQ-4206066

* Het uploaden van een avatar-afbeelding voor een LDAP-gebruiker mislukt. NPR-16561; hotfix voor graniet-17013
* Het aantal resultaten dat wordt weergegeven op het scherm Gebruikersbeheer, verschilt in de Kaart- en lijstweergave. NPR-16241; hotfix voor GRANITE-16914
* Workflowmeldingen kunnen niet lui worden geladen wanneer ze in de Google Chrome-browser worden weergegeven in de modus Volledig scherm. NPR-17013: Hotfix voor CQ-4207567

### Assets {#assets-15}

* De richting van de afbeelding wordt niet correct toegepast tijdens het importeren van een afbeelding met een gedefinieerde richting. NPR-16750: Hotfix voor CQ-4204356
* In de tijdlijnweergave van Assets worden geen elementen weergegeven, ook al is Alles tonen standaard ingesteld. NPR-16957: Hotfix voor CQ-98780
* `Camera RAW` -bestanden (waaronder ARW, CR2, NEF, DNG en EPS) kunnen niet worden geselecteerd of verwijderd als ze worden toegevoegd als uitvoering in elementen. Dergelijke bestanden worden automatisch gedownload wanneer de gebruiker erop klikt. NPR-16949: Hotfix voor CQ-4206846
* Als u een PDF maakt binnen een andere PDF in de Assets-gebruikersinterface, worden de gemaakte PDF niet weergegeven in de DAM-gebruikersinterface. De PDF zijn echter wel zichtbaar in de CRX-opslagplaats. NPR-16833: Hotfix voor CQ-4206501
* Het uploaden van een element als een rechtstreeks onderliggend knooppunt van zichzelf via de aanraakinterface veroorzaakt een probleem. Het element wordt geüpload als een direct onderliggend element van het eerder geselecteerde element. NPR-16534: Hotfix voor CQ-4204287
* In de DAM-gebruikersinterface wordt geen e-mailmelding gegenereerd wanneer u opmerkingen maakt over een element en een gebruiker in de opmerking van tags voorziet. NPR-16589: Hotfix voor CQ-102318

### Projecten {#projects-3}

De het werkschemaconsole van Projecten toont een NullPointerException op de pagina wanneer de werkschema&#39;s worden gewist. NPR-17017: Hotfix voor CQ-4194269

### Sites {#sites-15}

* Bestanden in de `ContextHub` worden niet geminimaliseerd voor de auteurinstantie. NPR-17022: Hotfix voor CQ-79456
* De WCM-Launches-lanceringsbevordering neemt lange tijd voor het bevorderen van een lancering die uit een grote boom van een pagina bestaat. NPR-16480: Hotfix voor CQ-82731
* `ClientContext` Renderer voor segmentvoorwaarde loopt vast wanneer een segment (of publiek) wordt gemaakt met een niet-werkende of niet-voltooide regel. NPR-16759: Hotfix voor CQ-4205104
* In WCM Lanches kunnen de pagina&#39;s die aan een Lancering zijn gekoppeld niet worden gepubliceerd wanneer de handeling wordt gestart vanuit de pagina-eigenschappen in de aanraakinterface. NPR-16560: Hotfix voor CQ-4204681
* Koppeling Rewriter herschrijft onjuist href-waarden die een dubbele punt bevatten, ervan uitgaande dat de dubbele punt &quot;:&quot; een JCR-naamruimte definieert. NPR-16753: Hotfix voor CQ-4203762
* Als u in WCM-Design Importer een testpagina voor importmodule opent en probeert een ZIP-bestand te uploaden, kan dit problemen veroorzaken als deze eerder is geüpload en verwijderd. NPR-16486: Hotfix voor CQ-90962
* Als u naar het deelvenster **[!UICONTROL Global Navigation]** navigeert met Firefox- of Google Chrome-browsers, hebt u een andere gebruikerservaring. In de browser Firefox wordt het menu **[!UICONTROL Tools]** weergegeven. In de Google Chrome-browser wordt het menu **[!UICONTROL Navigation]** weergegeven. NPR-16770; hotfix voor CQ-4200456

### Campagne {#campaign}

* Terwijl het testen van AEM campagnemalplaatjes en het wijzigen van zaadadressen om &quot;Extra Gegevens te omvatten,&quot;verdwijnt de drop-down Adobe Campaign in de Hub van de Context van de Aanraak UI. NPR-16771: Hotfix voor CQ-105748

### Mobiel op aanvraag {#mobile-on-demand-3}

* Wanneer Preflighting een publicatie van AEM auteur, een Preflight actie die langer dan vijf seconden duurt veroorzaakt een ongewone spiek op AEMM - AEM Dashboard van het Splunk van de Integratie van PECS met een hoog aantal statusverzoeken. NPR-16908: Hotfix voor CQ-4207055
* Het configuratiebeheer van AEM Mobile ontbreekt na het installeren van AEM-6.2-SP1-gestreken-1.0 update. NPR-16909: Hotfix voor CQ-4204892

### Vertaling {#translation-7}

* Het voorvertonen van vertaaltaken werkt niet na het installeren van 6.2 SP1 - GVB1. NPR-16481; hotfix voor CQ-4204655
* De taalkopie die u maakt met Vertaling, verwijst naar de hoofdmap in plaats van naar de lokale kopie van het bestand Live. NPR-17257; hotfix voor CQ-4208287

### Beveiliging {#security-3}

* Er wordt geen MIME-typevalidatie uitgevoerd wanneer binaire bestanden naar AEM worden geüpload. NPR-16617
* Problemen met het uploaden van avatar-afbeeldingen voor LDAP-gebruikers. NPR-16561

### Forms {#forms-16}

#### Forms-invoegtoepassing {#forms-add-on-package-16}

**Aangepaste Forms**

* In de AanpassingsRedacteur van Forms, zou het Plaatsende Doel commentaar in head.jsp met de nieuwe verklaring van de contexthub moeten worden vervangen. NPR-17173
* In de Adaptive Forms Rule Editor geeft de **[!UICONTROL Choose an Item]** de gebeurtenis als &#39;null&#39; weer. NPR-17139
* Het verzonden formulier wordt opnieuw verzonden door naar voren te navigeren met de pijl-vooruit (>). NPR-17080
* Bij het verzenden van een adaptief formulier als AJAX wordt de callback-functie &#39;error&#39; nooit aangeroepen als er een fout is opgetreden. NPR-17034
* Als u tijdens runtime op de knop **[!UICONTROL Save Form]** klikt in de Regeleditor, wordt het formulier niet opgeslagen. NPR-16905
* Statische tekst moet worden uitgesloten van de tabvolgorde in adaptieve vorm. NPR-16749
* De berekende waarde van een decimaal veld wordt onjuist weergegeven. NPR-16596
* Het pictogram voor het weergeven van Help-inhoud moet worden opgenomen in de tabvolgorde in adaptieve formulieren. NPR-16484
* Ondersteuning voor reguliere expressie van het type `dataRef=C:/Users/` in de **[!UICONTROL Default Prefill Service Configuration]** . Dit type is voor vooraf ingevulde gegevens voor Adaptive Forms. NPR-16425

* Validaties worden niet op de juiste wijze geactiveerd voor alle deelvensters als er een genest lazy-load scenario is. NPR-15821

**het Beheer van de Correspondentie**

* Letter-uitvoering mislukt als een letter een lege tekstmodule bevat (een zonder tekst). NPR-17054
* Regeleinden en tabruimten worden uit de inhoud verwijderd nadat deze in de Teksteditor zijn geplakt. NPR-17039
* De weergave van verwijzingen van een tekstmodule kost veel tijd als er in veel letters naar de tekstmodule wordt verwezen. NPR-17035
* Het bewerken, opslaan, verwijderen en instellen van verwijzingen voor documentfragmenten kost veel tijd. NPR-17033
* Uitgevulde tekst wordt weergegeven in een ander lettertype wanneer een voorvertoning van de letter wordt weergegeven. NPR-16976
* De zoekfunctie werkt niet goed als de gezochte tekst meerdere keren voorkomt. NPR-16920
* De werkbalk van de Teksteditor wordt periodiek in de browser weergegeven. NPR-16919
* De constructie **[!UICONTROL Save Form]** in de regeleditor werkt niet. NPR-16905
* In de vervolgkeuzelijst Lettertype wordt de lettertypefamilie niet gevuld bij het maken van een tekstmodule op basis van een gegevenswoordenboek met Internet Explorer. NPR-1694
* Nadat u een tekstfragment hebt gemaakt, verandert het lettertype van de letter wanneer u een voorbeeld van de letter bekijkt. NPR-16830
* Letters met tabspaties in het begin of tussen expressies in het documentfragment kunnen niet worden weergegeven of voorvertoond. NPR-16769

**Mobiele Forms**

* In de voorvertoning van mobiele formulieren wordt overlappende inhoud weergegeven, maar het formulier wordt correct weergegeven voor PDF-rendering. NPR-17105

**Forms Portal**

* Als u op de koppeling **[!UICONTROL Download]** voor een verzonden formulier klikt, wordt een HTML-pagina in plaats van een PDF-formulier geopend. NPR-17082

* `Upload Comments` voor bestandsbijlagen wordt niet weergegeven in de gebruikersinterface voor verzonden exemplaren, hoewel deze voorkomen in de XML-gegevens die zijn opgeslagen in de CRX-opslagplaats. NPR-17075

**Dienst van de Uitbreidingen van de Reader**

* Een specifiek bestand is niet Reader Extended voor AEM OSGI-installatie. NPR-16625

#### Forms JEE Installer {#forms-jee-installer-16}

**Kern**

* Tijdens het verbeteringsproces, ontbreekt de Manager van de Configuratie met onderbreking. NPR-16774 (zie [ het Vormen onderbreking voor verrichtingen op componentenniveau ](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Beheer van het Proces - HTML Workspace**

* Het startpunt van een Taak van het Begin begint niet met de gegevens die op het tijdstip van startpuntvoorlegging worden voorgelegd. NPR-16917
* Als u op de knop **[!UICONTROL Return]** klikt voor een formulier in de HTML Workspace, wordt het formulier niet gesloten, maar wordt het teruggestuurd naar de bijbehorende Group Queue.
NPR-16352

**Beheer van het Proces**

* Gebruikers toestaan de weergavenaam van vorige taken in te stellen op een van de volgende taken in een procesinstantie. NPR-15382

**de Dienst van de Output**

* Uitvoerservice kan een PDF die is gewijzigd om een extra veld &#39;milliseconden&#39; op te nemen in de metagegevens van `date-time format` , niet verwerken. NPR-16838

#### Forms Designer {#forms-designer}

* AEM de Scripteditor van Designer voldoet niet aan de standaardinstellingen voor Formuliereigenschappen voor `Calculate Event` en `Validate Event` . NPR-15921

### Functiepakketten in GVB4 {#feature-packs-included-in-cfp-1}

**Forms toe:voegen-op Pakket**

* Verbetering in de Inline Condition Editor voor Correspondentiebeheer. NPR-10981

### OSGi-bundels in GVB4 {#osgi-bundles-included-in-cfp-4}

Lijst van OSGi-bundels bijgewerkt tussen AEM 6.2 SP1 en GVB4

De belangrijkste kenmerken van GVB3 zijn:

* Efficiëntere zoekfunctionaliteit voor de klassieke gebruikersinterface en voor de AEM zoekcomponent met proxy met digest-verificatie
* Problemen verholpen tijdens het uploaden van elementen en het weergeven van metagegevens van elementen
* Hiermee worden problemen verholpen tijdens het maken van mappen en het verplaatsen van pagina&#39;s voor het geval de titel speciale tekens bevat.
* Oplossingen voor het gebruiken van gericht-synchroniserend publiek, het publiceren campagnes, en het selecteren van Goal Metric in Touch UI
* Synchronisatieproblemen voor vertaaltaken oplossen
* Biedt uitgebreide beveiliging voor de Forms Prefill-service
* Verbeteringen in het concept en de verzendingscomponent van de Forms Portal en in de Barcoded Forms Service
* Verbeteringen in bruikbaarheid voor adaptieve formulieren die widgets voor bestandsbijlagen of wazig geladen fragmenten bevatten.
* Verbeteringen op gebied van bruikbaarheid in Correspondentiebeheer, waaronder verbeterde zoekmogelijkheden, registratie van verwijderde elementen en het importeren van gegevenswoordenboeken.

### Platform {#platform-13}

* Een rasvoorwaarde in **ModelAdapterFactory**, die mogelijk is wanneer twee draden proberen om het zelfde gebied te injecteren, in mislukking resulteert om het model te construeren. NPR-16443: Hotfix voor SLING-6584
* Validatieoptie in Pakketbeheer om eventuele conflicten te detecteren tussen het overlappende bestand (JSP- of JavaScript-bestand) onder `/apps` en het bestand dat zich in een hotfix onder `/libs` bevindt. Betrokken bedekking kan vervolgens opnieuw worden gebaseerd om wijzigingen van het bestand onder `/libs` op te nemen. NPR-16216: Hotfix voor CQ-81729
* Het registreren in error.log houdt soms een paar seconden na de aanvang van de uitgever tegen en moet worden ontruimd om opnieuw te lopen. Verzoek om het registratieframework bij te werken en logboekregistratie te bieden. NPR-15913: Hotfix voor graniet-15452
* Verzoek om de JavaScript ‘ `use"` API bij te werken om fouten in de HTML JavaScript Use API-implementatie te voorkomen. NPR-16461: Hotfix voor SLING-6780

### Sites {#sites-16}

* Na bevordering van AEM 6.0 aan AEM 6.2, toont Klassieke UI langzame prestaties terwijl het zoeken van markeringen toe te schrijven aan talrijke vragen. Om de kwestie op te lossen, kunnen de stappen onder [ worden vermeld replicatiestatus in de etiketterende console (Klassieke UI) onbruikbaar maken ](#disable-replication-status-in-tagging-console-classic-ui-npr) worden gevolgd. NPR-15842: Hotfix voor CQ-4201748.

* Tijdens het maken van een pagina in de Touch-gebruikersinterface controleert de invoercontrole voor het veld &#39;name&#39; niet het speciale teken &#39;Apostrof&#39; (hetzelfde als in de klassieke gebruikersinterface). De pagina kan daarom niet worden verplaatst. NPR-16404: Hotfix voor CQ-4205321.
* Wanneer u verschillende stijlen toepast op twee rijen in de Rich Text Editor en deze vervolgens samenvoegt, wordt de stijl verwijderd die op de tweede rij is toegepast. NPR-16389: Hotfix voor CQ-4203835.
* Als u in het scherm Touch UI Sites een pagina probeert te plakken in een pagina zonder subpagina&#39;s, werkt dit niet omdat de knop Plakken niet beschikbaar is. NPR-15894: Hotfix voor CQ-4201696.
* Tijdens het schuiven door het tabblad Pagina&#39;s in het venster Inhoudszoeker worden een paar paginasets oneindig weergegeven in de klassieke gebruikersinterface, terwijl in de aanraakinterface een beperkte set van weinig niet-herhalende pagina&#39;s wordt weergegeven. NPR-16271: Hotfix voor CQ-4202371
* Als u de Pagina-eigenschappen van een LiveCopy opent in de Touch-gebruikersinterface en op Opslaan klikt zonder wijzigingen, wordt een willekeurig tabblad van LiveCopy geschreven en wordt een knooppunt van LiveSync Config gemaakt. NPR-16327: Hotfix voor CQ-108562
* Formulierbeperking kan de eigenschap `ConstraintMessage` niet lezen. NPR-16388: Hotfix voor CQ-101330
* De `wcm/foundation/components/parsys` -component geeft geen placeholder van **[!UICONTROL 'Drag components here]** weer. NPR: 16748: Hotfix voor CQ-4205187

### Assets {#assets-16}

* De pdf-rasterizer werkt niet meer en veroorzaakt na de installatie van 6.2 SP1 of Hotfix 12430 problemen. NPR-15991
* De metagegevens voor een tekenreekseigenschap, `documentNumber` wordt weergegeven als een datum, terwijl dit een getal moet zijn. NPR-16134: Hotfix voor GRANITE-16916
* Tekstafbrekingen in de gebeurtenisballon van de tijdlijn. NPR-16226: Hotfix voor CQ-85226
* Wanneer een map onder de inhoudshiërarchie wordt gemaakt met een titel die speciale tekens bevat, wordt de gecodeerde versie van die tekens weergegeven. NPR-15935: Hotfix voor CQ-4202987
* De gebruiker kan tijdens het navigeren door elementen geen elementen uploaden of mappen maken vanwege inconsequent gedrag bij het gebruik van de knop Maken. NPR-16410: Hotfix voor CQ-4204793
* Er worden onverwachte fouten aangetroffen tijdens het uploaden van gedeelde HTML-bronnen vanuit de artikelweergave in AEM Authoring. NPR-16133: Hotfix voor AEMM-4155970

### Integratie {#integration-14}

* Wanneer het toelaten van volmachtsauthentificatie met de Authentificatie van de Samenvatting, werpt de AEM component van het Onderzoek een GelijktijdigeModificationException. NPR-15309: Hotfix voor CQ-4199191
* Wanneer het creëren van een Activiteit van de Test van het Doel A/B in AEM, synchroniseert het publiek niet aan het Doel en toont &quot;geen publiek.&quot; NPR-16229: Hotfix voor CQ-4204210
* Nadat u SP1+NPR-11577 v1.2 hebt geïnstalleerd, wordt de vervolgkeuzelijst met meetgegevens nooit geladen wanneer u &#39;Een metrische analyse gebruiken&#39; kiest voor de algemene metrische functie wanneer u een abonnement neemt op de TouchUI. NPR-16129: Hotfix voor CQ-4204316
* Als u doelgericht werkt, publiceert de campagne niet automatisch de gehele boom, inclusief het merk en het primaire deel. NPR-15855: Hotfix voor CQ-94630

### Vertaling {#translation-8}

* De functie Vertaling synchroniseren wordt nu automatisch geactiveerd en AEM opiniepeiling vindt nu plaats zonder de vertaalprojecten te hoeven opzoeken. NPR-15163: Hotfix voor CQ-90856

### Forms {#forms-17}

#### Forms-invoegtoepassing {#forms-add-on-package-17}

**Aangepaste Forms**

* Wanneer u een adaptief formulier opslaat met een bijlage, wordt het volledige pad van de bijlage toegevoegd in de `fileAttachment` -tag van de gegenereerde XML in plaats van de naam van de bijlage. NPR-16529
* In op XDP gebaseerde adaptieve formulieren is de `afData/afBoundData` -wrapper aanwezig in het verzonden XML-bestand, ook al heeft Prefill XML geen `afData/afBoundData` -wrappers. NPR-1618

* Exponentiële notatie in het veld Nummer: wanneer u adaptieve formulieren gebruikt en een getal met een decimale breuk van meer dan tien tekens in totaal invoert, verandert het getal in exponentiële notatie in de verzonden XML. NPR-16106
* Voor formulieren die zowel een bestandsbijlage als een lazy geladen fragment bevatten, bevat het verzonden data-xml niet de informatie voor de bestandsbijlage. NPR-16022
* Voor een lazy geladen herhaalbaar paneel dat geen herhaalbare voorouder heeft, kunnen de herhaalbare kinderen binnen een tweede instantie van het paneel niet herhalen. NPR-1594
* Wanneer u een fragment probeert op te slaan in een fragment in een formuliereditor, wordt de waarde van het onderliggende fragment niet gevuld door de hoofdmap van het fragmentmodel. NPR-15943
* Als u een selectievakje maakt met slechts één item en de titel van het selectievakje probeert weer te geven terwijl de itemtitel verborgen blijft, genereert de actie Woordenboek maken een `ArrayIndexOutOfBoundException` als de itemtekst leeg is. Het woordenboek wordt niet gemaakt en er wordt geen foutreactie gegenereerd op het scherm. NPR-15816
* Voor adaptieve formulieren met bestandsbijlagen worden sommige delen van het formulier uitgeschakeld nadat een voorvertoning van het bijgevoegde bestand is weergegeven.
NPR: 16611

* Voor bestandsbijlagen die meerdere bijlagen toestaan, leidt het verzenden van een nieuw formulierexemplaar met een bijlage op een widget die al een vorige bijlage heeft, tot een weergegeven foutcode. Deze fout treedt op wanneer de toegevoegde bijlage wordt geopend in plaats van de feitelijke inhoud. NPR-16258
* Beveiliging van formulieren vóór de service van onbevoegde toegang via protocollen zoals `file://` , `http://` en `ftp://` . Zie [ Vormend de Prefill dienst gebruikend de Manager van de Configuratie ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15414

* Verzoek om het adaptieve formulier te genereren in de PDF-indeling in plaats van HTML in de verificatiestap en alle bijlagen toe te voegen aan de PDF, zodat het volledige formulier wordt weergegeven bij de afdruk. NPR-9011

**het Beheer van de Correspondentie**

* Wanneer u in de modus Voorbeeld of Bewerken met tekstfragment werkt in een letter en tekst wordt omgezet in een lijst, wordt de volledige letterfunctionaliteit afgebroken. Er wordt een JavaScript-fout gegenereerd. NPR-16460
* Het importeren van een XSD-bestand om een gegevenswoordenboek te maken in het knooppunt Correspondence Management mislukt wanneer de browser telkens niet reageert wanneer de XSD wordt geüpload en het hoofdknooppunt wordt geselecteerd. Deze kwestie is browser onafhankelijk en verschijnt niet in serverlogboeken. NPR-16452
* Tijdens het voorvertonen van een brief met de browser van Internet Explorer en het bewerken van de lettergrootte van inhoud, worden dubbele waarden weergegeven van 8 tot 72 in het vervolgkeuzemenu voor tekengrootte. NPR-16387
* Als een zwevend veld wordt weergegeven als een invoerveld van een XDP-fragment, wordt het veld in de lettertypevoorvertoning niet vergroot wanneer de browser van Internet Explorer wordt gebruikt. NPR-16367
* Wanneer u probeert een brief rechtstreeks vanuit de voorvertoning te verzenden, wordt de pop-up voor de letternaam niet correct weergegeven omdat deze is verborgen. NPR-16353
* De lijnruimten die tijdens het uitgeven van een brief worden toegevoegd worden niet weerspiegeld in het venster van de Voorproef. Voor lijsten in tekstfragmenten geeft de uitvoer van de PDF niet de juiste afstand weer. NPR-16267
* Wanneer u met de Internet Explorer-browser aan een tekstdocumentfragment werkt, mislukt het opgeven van inspringing voor de tekst omdat de cursor geen tekstinspringing toestaat. NPR-16128
* Het toevoegen of wijzigen van een gegevenswoordenboek aan een bestaand tekstdocumentfragment kost veel tijd en de gebruiker wordt niet altijd op de hoogte gesteld. NPR-16102
* Wanneer u een voorvertoning weergeeft van een letter die schuifbare inhoud bevat via de browser van Internet Explorer, overlapt de schuifbalk van de browser met de schuifbalk van de letter. De volledige inhoud kan daarom niet worden weergegeven voor fragmenten aan de rechterkant. NPR-16068
* Als u tekstdocumentfragmenten maakt of bewerkt met de Google Chrome-browser, wordt de vervolgkeuzelijst met kleurselectie automatisch weergegeven en kan deze niet worden verwijderd. De gebruiker moet de lijst selecteren als het type gegevensinvoer om het fragment te kunnen bewerken. NPR-16067
* Wanneer u de `Letterinstance` API gebruikt, werkt de methode `import com.adobe.icc.services.api.LetterInstanceService` niet. NPR-16008
* Het wijzigen van de datumweergave-indelingen in `locale=en_US; dateFormat=MMM dd,yyyy;` in de Configuratie van de Asset Composer werkt niet zoals verwacht en de datumnotatie wordt weergegeven als ongewenste tekens. NPR-16007
* Het type gegevenskoppeling in letters tijdens het opnieuw ontwerpen wordt weergegeven als &#39;Gebruiker&#39;, zelfs als deze koppeling eerder anders is ingesteld. NPR-16619

**Forms Portal**

* De scenario&#39;s van de verbetering voor ontwerp en postingscomponenten werken niet met de implementatie van de gegevensbestandsteekproef. NPR: 16752

**Barcoded Dienst van Forms (BCF)**

* De statische codeanalyse van Barcoded Forms Service (BCF) meldt kwesties. NPR-1385

#### Forms JEE Installer {#forms-jee-installer-17}

**Beheer van het Proces - HTML Workspace**

* De vooraf ingevulde dienst van formulieren beveiligen tegen onbevoegde toegang door protocollen zoals &quot;file://,&quot;http://,&quot;en ftp://. Voor details, zie [ Vormend Prefill de Dienst gebruikend de Manager van de Configuratie ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15434

**Gebruikersbeheer **

* In het SAML-aanmeldingsscherm wordt een onjuiste versie (6.1.0) op de AEM 6.2-server weergegeven. NPR-13825
* Met AEM Forms dat voor Single Sign On (Kerberos) authentificatie wordt gevormd, als de gebruikersauthentificatie terwijl het proberen om binnen te loggen ontbreekt, is een foutencode &quot;404&quot;teruggekeerd. De gebruiker wordt pas omgeleid naar de aanmeldingssite nadat de pagina is vernieuwd. NPR-15015

#### Forms Designer {#forms-designer-1}

* Het wijzigen van de formulierlandinstelling in het Frans (Canada) in de woordenboekspellingcontrole werkt niet in AEM Forms Designer.
NPR-15896

### Functiepakketten die zijn opgenomen in GVB3 {#feature-packs-included-in-cfp-2}

**Forms toe:voegen-op Pakket**

* Bij het verwijderen van middelen in Correspondentiebeheer moet een waarschuwingsbericht worden aangemeld bij het bestand error.log. NPR-1325
* Verbeter de zoekfunctionaliteit terwijl u een voorbeeld van een letter weergeeft in Correspondence Management om het zoeken naar tekst in de tekstfragmentinhoud mogelijk te maken in plaats van alleen in de lettertitel of het label te zoeken. NPR-16103

### OSGi-bundels in GVB3 {#osgi-bundles-included-in-cfp-5}

Lijst van OSGi-bundels bijgewerkt tussen AEM 6.2 SP1 en GVB3

[ krijgt Dossier ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt).
De belangrijkste kenmerken van Cumulative Fix Pack 2 zijn:

* Stabiliteitsoplossingen en prestatieverbeteringen in het AEM platform, inclusief Sling-raamwerk en -activiteiten
* Verbeterd middelenbeheer met verschillende oplossingen voor het openen, verplaatsen, zoeken, uploaden en publiceren van middelen
* Verbeterde creatie en beheer van Plaatsen met moeilijke situaties in de componenten van de Fragmenten van de Inhoud, van het Anker, Diapresentatie, en van de Hub van de Context
* Verschillende correcties in Touch UI, waaronder teksteditor, Omnsearch en het aanmaakproces van varianten
* Verbeterde vertaalworkflows; verbeterde Microsoft®-connector voor het gebruik van nieuwe vertaal-API&#39;s voor de Azure-portal
* Oplossingen in projecten en campagnes
* Verbeterd ontwerp en beheer met oplossingen in adaptieve formulieren, correspondentiebeheer en functies voor formulierportalen
* Oplossingen in Forms JEE Core-, XTG- en HTML-werkruimtecomponenten

### Platform {#platform-14}

* `SlingPostProcessor` wordt geactiveerd als de pagina die rechtstreeks naar het Sling-framework verwijst, wordt bewerkt. NPR-15754: Hotfix voor CQ-104153

* De waarde voor tags met de eigenschap `tagBasePath` wordt niet opgehaald in het dialoogvenster Klassieke gebruikersinterface tijdens het navigeren naar een pagina-component. NPR-15543: Hotfix voor CQ-4199950

* Wanneer u Sling-bewerkingen uitvoert, wordt een segment met de naam &#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk` in een eindeloze lus met lege brokken uitgevoerd. NPR-15455: Hotfix voor SLING-5701

* Wanneer een interface een andere interface uitbreidt, worden de injecteerbare methodes op de super interface niet correct geïnjecteerd. NPR-15202: Hotfix voor SLING-5710
* Een potentiële ongeldige wijzeruitzondering wordt niet verhinderd wanneer het gebruiken van de `com.adobe.granite.infocollector.impl.FilesTraversal` functievraag. NPR-15169 Hotfix voor CQ-4197640
* De workflowstatus is inconsistent voor sommige secundaire knooppunten en er wordt een fout weergegeven bij het verzenden van observatiegebeurtenissen voor dat knooppunt. NPR-15701: Hotfix voor GRANITE-13786
* Een gebruiker selecteert een knooppunt in CRXDE (bijvoorbeeld `/content/dam/` ). Klik vervolgens op het tabblad Toegangsbeheer, zodat er een lijst met toegangsbeheer bestaat. Wanneer u nu bepaalde elementen sleept en neerzet, worden de elementen verplaatst, niet de geselecteerde. NPR-15696 Hotfix voor GRANITE-16300
* Als u een gebruiker in de vervolgkeuzelijst selecteert wanneer u probeert zich voor te doen, verdwijnt de volledige gebruikerspop. NPR-15774: HotFix voor CQ-4201738/GRANITE-11895
* Het zoeken op tags met automatisch ingevulde suggesties werkt niet in de zoekopdracht. NPR-15088: Hotfix voor GRANITE-14426.
Opmerking: voor deze correctie is Oak GVB 1.4.11 of hoger vereist.

### Mobiele AEM {#mobile-aem-author}

* Wanneer u AEM Mobile- en ContentSync-pakketten gebruikt met een hybride toepassing, reageert AEM op een aanvraag voor het ophalen (met tijdstempels) die door de toepassing is gemaakt met het oudste pakket in plaats van het pakket dat door de toepassing wordt aangevraagd. NPR-15749: Hotfix voor CQ-104153

### Sites {#sites-17}

* De wijzigingsstatus voor Workflow Inbox in de WCM-kern verandert niet als een gebruiker een pagina wijzigt nadat een workflow is geactiveerd. NPR-15684: hotfix voor CQ-4196974
* De Ankerplug-in in de RTF-editor voor de aanraakinterface genereert niet-compatibele HTML5 wanneer de gebruiker op het ankerpictogram klikt en een naam toevoegt. Het moet een kenmerk &#39;id&#39; toevoegen in plaats van het kenmerk &#39;name&#39; in de HTML5-tag voor het ankerelement. NPR-15650: Hotfix voor CQ-89782
* Wanneer een metagegevensschema met een groot aantal velden wordt gemaakt en toegepast op de metagegevens van het inhoudsfragment, wordt er geen schuifbalk gemaakt in het scherm met metagegevens van het inhoudsfragment, zodat de velden niet kunnen worden bewerkt. NPR-15478: Hotfix voor CQ-4202622
* Als u `TagInput` -veldcomponent bewerkt, worden de eerder geconfigureerde waarden niet weergegeven in de dialoogvenstervelden. NPR-15464: Hotfix voor CQ-4200360

* Wanneer er in de gebruikersinterface van de inhoudsfragmenteditor variaties van een inhoudsfragment worden gemaakt, wordt in het zijpaneel niet de schuifbalk weergegeven om door alle variaties te navigeren. NPR-15445: HotFix voor CQ-4199444
* Wanneer gebruikers worden verwijderd uit directe groepen, worden ze toegevoegd aan overgenomen groepen. NPR-15400: Hotfix voor CQ-98758
* WCM-authoring: Touch UI-auteur staat bewerken van pagina&#39;s met komma&#39;s in de naam niet toe. NPR-15396: Hotfix voor CQ-4199723
* Als de functie `Granite.author.editableHelper.doSelectParent` de aanraakinterface gebruikt om te ontwerpen, geeft deze argumenten in de verkeerde volgorde door, wat resulteert in een JavaScript-fout. NPR-15349: Hotfix voor CQ-4198594
* Het segment van ContextHub toont de ervaring zelfs als het opt-out koekje aanwezig is. NPR-15293: Hotfix voor CQ-4198024
* De component Presentatie in de klassieke gebruikersinterface kan geen dia&#39;s maken of afbeeldingen slepen en neerzetten om dia&#39;s te maken. NPR-15281: Hotfix voor CQ-4194164
* Ongeacht de machtiging worden de opties bij &#39;Maken&#39; weergegeven, zoals Pagina maken, Site maken, Live kopie maken, Starten en Catalogusmenu maken in de Site-Admin Console. NPR-15278: Hotfix voor CQ-94436
* Nadat u AEM 6.2 Service Pack 1 hebt geïnstalleerd, werkt de schuifregelaar Subpagina&#39;s opnemen niet meer voor het starten van pagina&#39;s. NPR-15230: Hotfix voor CQ-4198449
* Verzoek om Versie te verbeteren zuivert om versies in blokken te halen en te verwerken en een gespecificeerd weg in een vraag van XPath te kunnen gebruiken. NPR-15186: Hotfix voor CQ-109205
* De knop Wissen ontbreekt op het tabblad met pagina-eigenschappen in de component Sites. NPR-15143 Hotfix voor CQ-419697
* Als u voor een site die Live-kopieën gebruikt het selectievakje &#39;Live kopie&#39; in het deelvenster Kolommen van de site Admin Console selecteert, wordt de status van Live kopie niet correct weergegeven en wordt alleen de HTML-opmaak weergegeven. NPR-15108: Hotfix voor CQ-97086
* Als de gebruiker tijdens het bewerken van Inhoudsfragmenten klikt op Gereed (&#39;&#39;) om te bewerken voordat de Post hierop reageert, wordt de bewerkte inhoud niet correct opgeslagen. NPR-15014: Hotfix voor CQ-4194095
* Als u de pagina Bewerken sluit in de modus Tijdlijn verdraaien en probeert deze opnieuw te openen vanuit Sitebeheer, treedt er een fout op met de status `500` . NPR-14965: Hotfix voor CQ-109647:
* In de DAM-gebruikersinterface (Digital Asset Manager) leidt de zoekopdracht &#39;Volgorde van autorisaties zoeken&#39; tot de uitzondering &#39;Onvoldoende geheugen&#39;. NPR: 15307: HotFix voor CQ-98542

### Assets {#assets-17}

* Na het zoeken van een activa in Onderzoek, die een activa selecteren en proberen om eigenschappen uit te geven door **Eigenschappen van de Mening** te klikken, dan richt **sparen** knoop gebruikers aan een lege pagina opnieuw. NPR-15900: Hotfix voor CQ-4202372
* Assets-gebruikersinterface reageert niet op gebeurtenissen. Het selecteren van een element en klikken op &#39;Publish&#39; of &#39;Uitvoeringen&#39; leidt niet tot enige activiteit. NPR-15828: Hotfix voor CQ-4202247
* Wanneer u een element publiceert vanuit de Kaartweergave, wordt de Kaart niet bijgewerkt met een gepubliceerde status. In plaats daarvan wordt de pagina vernieuwd. NPR-15826: Hotfix voor CQ-102732
* Cumulatieve hotfix die Assets Hotfixes bevat. NPR-1525
* Als een en-teken (&#39;&amp;&#39;) is opgenomen in de naam van een elementenmap, wordt de mapnaam niet correct weergegeven wanneer u naar het element navigeert. NPR-15775: Hotfix voor CQ-4201735
* Het gebruik van het en-teken (&#39;&amp;&#39;) in de naam van een elementbestand veroorzaakt problemen bij de toegang tot de eigenschappen ervan. NPR-15770: Hotfix voor CQ-4201737
* Als de gebruiker tijdens het navigeren door Assets en met de weergavemodus &#39;Kolomweergave&#39; de pagina vernieuwt na het selecteren en klikken op een element, worden de elementdetails weergegeven in plaats van de vernieuwde inhoud. NPR-15768: Hotfix voor CQ-4201727
* PDS-opname neemt 100% CPU-gebruik in beslag met een pakket bibliotheken voor PDF-services. NPR-15606 HotFix voor GRANITE-12929
* Als u de interface Mijn koppelingsaandelen opent via de Firefox-browser, worden de gedeelde items of gebruikers niet weergegeven en is het scherm onbruikbaar. NPR-15539: HotFix voor CQ-420092
* Als tijdens het gebruik van Digital Asset Manager een pagina is gekoppeld aan een set afbeeldingen, wordt de koppeling naar de pagina verbroken wanneer de afbeeldingen naar een nieuwe map worden verplaatst. Hierdoor ontbreken enkele afbeeldingen op de gekoppelde pagina. NPR-15538: Hotfix voor CQ-111479
* In de component Dam Viewer leidt het gebruik van de uitvoermodus &#39;nosamplcontent&#39; tot fouten met dynamische media. NPR-15449: Hotfix voor CQ-4195425
* Als u tijdens het maken van videoprofielen zowel een voorinstelling voor videocodering van hoge kwaliteit als een voorinstelling voor videocodering van gemiddelde kwaliteit kiest, worden de aangebrachte wijzigingen niet opgeslagen. NPR-15447: Hotfix voor CQ-4195482
* Hoewel het uploaden van een element naar Brand Portal mislukt als gevolg van een reactie op een serverfout, wordt de status bijgewerkt naar &#39;Published&#39; in de Brand Portal-gebruikersinterface, waardoor het moeilijk wordt om het gemiste bestand bij te houden. NPR-15442: Hotfix voor CQ-4197968
* Wanneer u een map met middelen publiceert naar de Brand Portal, waar het publiceren meer dan een uur duurt, kunnen sommige bestanden niet worden gepubliceerd. NPR-15441: Hotfix voor CQ-4199493
* Wanneer u de console van Asset Finder in de kolomweergave gebruikt, mislukt het maken van een map een keer, hoewel het lukt om het opnieuw te proberen. NPR-15370: Hotfix voor CQ-4199448
* Als een element of map die is geselecteerd in de DAM-gebruikersinterface een komma in de naam heeft, is het tabblad Referenties niet beschikbaar en wordt het bericht &quot;Lijst met referenties is niet beschikbaar voor meerdere selecties.&quot; weergegeven. NPR-15362: Hotfix voor CQ-4199721
* Als u een map naar Brand Portal publiceert, verandert de gepubliceerde status van de map niet, ook al worden de middelen in de map gepubliceerd. NPR-15292: Hotfix voor CQ-4197667
* Tijdens het navigeren naar de Assets-console in Touch UI wordt een uitzondering weergegeven bij het activeren van bepaalde middelen. NPR-15217: Hotfix voor CQ-108779
* Een video publiceren naar YouTube wanneer de verbinding via een proxyserver wordt gemaakt. NPR-15109: HotFix voor CQ-10332
* Een element gebruiken met een naam die een punt of punt (.) bevat in data-Smart-resource wordt niet omgezet naar hetzelfde element en het uitvoerpad wordt beëindigd op de punt. NPR-15069: Hotfix voor CQ-4195914
* Na de upgrade van AEM 6.2 naar Service Pack 1 mislukt de synchronisatie van de middelen naar Scene7. De eigenschap `dam:Scene7FileStatus` geeft de `UploadFailed` -status zelfs voor gepubliceerde elementen weer. NPR-15269: Hotfix voor CQ-4197708

### Gebruikersinterface {#user-interface-5}

* In **[!UICONTROL Touch UI]** wordt de opgeslagen datum weergegeven voor datumvelden die nu type=&#39;datetime&#39; hebben terwijl u Internet Chrome-browserversie 56.0.2924.87 gebruikt. NPR-15383: Hotfix voor GRANITE-16481
* In **[!UICONTROL Touch UI]** verwijdert de Rich Text Editor de thread- en bijschriftelementen uit HTML-tabellen tijdens het renderen. NPR-15267: Hotfix voor CRTE-41
* In `FileUpload Validator` worden geen gevallen afgehandeld wanneer de functie voor automatisch starten true is of wanneer `uploadFile()` handmatig wordt aangeroepen. In deze gevallen wordt een ongeldig validatierapport gegenereerd. NPR-15295: Hotfix voor GRANITE-13499

* Bij Omnsearch kunnen klanten die `/apps` gebruiken, geen kolomgegevensbron toevoegen omdat ervan wordt uitgegaan dat de locatieconfiguratie wordt vermeld onder */libs/granite/omnissearch/content/metadata/* . NPR-13188 Hotfix voor GRANITE-16479
* Wanneer u **[!UICONTROL Touch UI]** gebruikt, worden productvarianten niet op hetzelfde niveau gemaakt als het product. De gebruiker wordt niet geïnformeerd over de status van het proces voor het maken van varianten. NPR-15345: HotFix voor CQ-4198948

**Scene7**

* Als u de Scene7-workflow uitvoert, worden geopende bestanden niet gesloten. Verzoek om de dienst te verbeteren AEM-S7 zodat het één enkele instantie HttpClient met gedeelde het pooling configuratie handhaaft en hergebruikt. NPR-15357: Hotfix voor CQ-109958

### Vertaling {#translation-9}

* Wanneer het gebruiken van vertaalprojecten, produceert het bijwerken van taalexemplaren van de Engelse primaire 11 afzonderlijke lanceringen allen met de zelfde naam en bronwortel. Ze hebben echter elk een iets andere startbasis, voor het geval de paginanaam een setpatroon volgt. NPR-15605: Hotfix voor CQ-4200699
* Vertaalprojecten worden niet gemaakt voor pagina&#39;s wanneer de taalwortels afbreekstreepjes en streepjes in de naam hebben. NPR-15171: Hotfix voor CQ-96286
* Vraag om de Microsoft®-connector bij te werken zodat deze de Microsoft® Translator API&#39;s kan gebruiken, die door Microsoft® beschikbaar worden gesteld op de Azure-portal. NPR-15320: Hotfix voor CQ-101010

### Projecten {#projects-4}

* Slechts 20 inactieve projecten zijn zichtbaar in het Scherm van Projecten hoewel meer dan 20 inactieve projecten in de bewaarplaats bestaan. NPR-15656: Hotfix voor CQ-4200903

### Campagne {#campaign-1}

* Wanneer u de integratiecomponenten Campagne - gericht en `MAC` - Testen en Doel gebruikt, wordt de activiteitsstatus in de primaire gebruikersinterface niet bijgewerkt wanneer u de activiteiten depubliceert. NPR-15401: Hotfix voor CQ-4199839
* Tijdens het verplaatsen van een product in AEM Commerce, mist de wizard Product Move de vooraf ingevulde waarden voor de productnaam, titel, pagina&#39;s waarnaar wordt verwezen, de auteur en de gemaakte datum. NPR-15228: Hotfix voor CQ-98617

### Beveiliging {#security-4}

* CSRF-tokenparameter toegevoegd aan formulieren met een methode GET. NPR-1529

### Forms {#forms-18}

#### Forms-invoegtoepassing {#forms-add-on-package-18}

`**Adaptive Forms**`

* Standaardwaarden worden overschreven door lege waarden in xml als het Adaptief formulier wordt ingevuld met invoer-XML. NPR-15721
* De `afData/afBoundData` -wrapper is aanwezig in verzonden XML, hoewel zelfs vooraf ingevulde XML geen `afData/afBoundData` wrapper heeft in op XML-schema gebaseerde adaptieve formulieren. NPR-15541

* De titels in de bar van de Accordeon zouden editable HTML &quot;h2&quot;rubrieken in plaats van &quot;a&quot;markering moeten zijn. NPR-15475
* De accordeonindeling van een formuliervenster is niet toegankelijk voor schermlezers. Gebruikers kunnen niet alleen met het toetsenbord naar het accordeontabblad navigeren met schermlezersoftware zoals JAWS of NVDA. NPR-15474

`**Correspondence Management**`

* Het opslaan, verwijderen en instellen van verwijzingen voor een documentfragment kost veel tijd. NPR-15939
* Tabuitlijning die is ingesteld in Assets beheren op tekst die meerdere headers-einden bevat in de CCR-gebruikersinterface. NPR-15818
* In miniaturen van tekstmodules wordt geen uitgelijnde inhoud weergegeven, hoewel de tekst uitgelijnde inhoud bevat die is gemaakt met Tabs in Google Chrome. NPR-15819

`**Forms Portal**`

* De Prefill-service werkt niet voor XDP Forms. NPR-15466
* Bij het opslaan van concepten en verzendingen van adaptieve formulieren naar de database wordt de status van het adaptieve formulier beschadigd wanneer de databaseconnectiviteit om welke reden dan ook mislukt (bijvoorbeeld na een lange periode van inactiviteit). NPR-15297

#### Forms JEE Installer {#forms-jee-installer-18}

`**Core**`

* Na de upgrade naar de nieuwste versie van Java™ 1.8.0_121-b13 is de Admin-gebruikersinterface niet toegankelijk in AEM Forms. NPR-1530

`**XTG**`

* Terwijl het gebruiken van de dienst van de Output om een specifieke vorm met dataxml samen te voegen, is de reactietijd 20 keer vergeleken bij de tijd die door een ES4 SP1 server wordt genomen. NPR-15283

#### AEM Forms App {#aem-forms-app-1}

* Wanneer het terugkrijgen van niet-bewaarde taken, moet het bericht dat bij terugwinning van niet bewaarde taken wordt getoond duidelijker worden gemaakt om gebruikersfout te verminderen. NPR-1537
* AEM Forms-app genereert geen formulieren die zijn gemaakt van aangepaste sjablonen. NPR-15892
* Gebruikers kunnen zich niet aanmelden bij de AEM Forms-app. NPR-15891

De belangrijkste hoogtepunten van AEM 6.2 SP2-GVB1 zijn:

* Streamlines-replicatiefunctionaliteit in sites:

* Oplossingen voor verschillende problemen met rollout, LiveCopy en schrijven bij fouten

* Verbetert de responsiviteit van de aanraakinterface tijdens:

* Zoeken van middelen
* sorteren op basis van grootte

* Verbetert tagbeheer in slimme verzamelingen
* Verbeterde toegangsbesturingselementen tijdens CRUD-bewerkingen op mappen

### Platform {#previous}

* Verzoek om verwijdering van `ReplicationQueue#forceRetry` API vraag tijdens opstarten van replicatieagenten omdat dergelijke vraag beduidend de instantie vertraagt, vooral wanneer het vele replicatieagenten heeft. NPR-14032: Hotfix voor GRANITE-13095
* Verzoek om `DurboImportConfigurationProviderService` configuratie OSGi om gebieden te steunen die een serie van waarden kunnen opslaan. NPR-14570: Hotfix voor CQ-108684
* Wanneer u de component Scorrect op een pagina gebruikt nadat u naar AEM 6.2 hebt gemigreerd, werkt het dialoogvenster Eigenschappen van de pagina niet meer. NPR-14328: Hotfix voor CQ-108355
* Als u een eerder geplande taak ongedaan maakt, wordt het corresponderende knooppunt onder */var/eventing/scheduled-tasks* niet verwijderd. NPR-14253: Hotfix voor SLING-5666
* Wanneer een beheerder probeert zich als geschrapte gebruiker voor te doen, verfrist het gebruikersinterface zich niet. NPR-14247: Hotfix voor CQ-107446
* XSS-beveiligingscontrole veroorzaakt onjuiste codering in de component Sightly. NPR-14004: Hotfix voor CQ-93821
* Verzoek om de kluis van het Dossier van het Jasje aan 3.1.30 te bevorderen om veelvoudige kwesties op te lossen. NPR-13454
* De fout van het geheime voorgeheugen komt voor wanneer het Verdelen van Distributie de distributiepakketten van auteur synchroniseert om te publiceren. NPR-13034: Hotfix voor GRANITE-13970

### Sites {#sites-18}

* Problemen met het zuiveren van VersionManagerImpl van onjuiste versies uit versiegeschiedenis. NPR-14372
* De component van Parsys van de Stichting van WCM recht negeert de namen van de componentenverklaring van de markeringsmarkering, `cq:htmlTag / cq:tagName`. NPR-1425
* Wanneer Juist Parsys wordt gebruikt om componenten terug te geven die door JavaScript in Aanraking UI worden opgenomen, wordt de douaneversiering genegeerd nadat de pagina wordt verfrist. NPR-14122
* De vervolgkeuzelijsten voor het doel werken niet in het dialoogvenster Aanraakinterface wanneer meerdere RTF-velden, zoals koppelingen, worden gemaakt. NPR-13911
* Wanneer u een tekstveld bewerkt met meerdere Rich Text Editor (RTE)-eigenschappen in een dialoogvenster (Touch UI), wordt de focus willekeurig verschoven naar een specifieke RTE-eigenschap. NPR-13703
* De standaardvideo-component buiten de box rendert de videominiatuur niet. NPR-14976
* Informatie wordt langzaam geladen in het Levende lusje van Beelden in de Redacteur van het Malplaatje. NPR-14880: Hotfix voor CQ-83417
* Door Hotfix-10936 te installeren op een AEM 6.2-instantie, wordt de component Iparsys uitgeschakeld. NPR-14330: Hotfix voor CQ-106982
* De veelvoudige kwesties van de component Rollout en een Levende kwestie van het Exemplaar na migratie aan AEM 6.1 SP1. NPR-15256
* De actie van de Roll-out van de Pagina ontbreekt om kinderen voorbij het eerste niveau zelfs voor veelvoudige configuraties tot stand te brengen Roll-out. PR-15055
* Wanneer u het dialoogvenster Pagina-eigenschappen vanuit de Editor verzendt, worden ongewijzigde gegevens op de tabbladen van LiveCopy opnieuw geschreven. NPR-14693
* Wanneer het dialoogvenster Pagina-eigenschappen wordt verzonden vanuit de Editor, schrijft MSM Post Processor enkele parameters uit de aanvraag in plaats van de parameter `msm:writeLiveCopyConfig` . NPR-14434
* Meerdere problemen met betrekking tot de component Rollout, actieve kopieën en andere aspecten van MSM. NPR-12235

### Assets {#assets-18}

* Werkstroom uitpakken kan afbeeldingen met speciale tekens in de naam van het afbeeldingsbestand niet verwerken. NPR-15227: Hotfix voor CQ-103887
* Assets met expressie Herhalen met voorwaarde wordt niet correct weergegeven. Wanneer de gebruiker een voorvertoning weergeeft van de sjabloon voor de `*CDN3835RLCEN*` letter, worden geen elementen weergegeven die zich in het doelgebied Body bevinden. Voor bestandsbijlagen-widgets die meerdere bijlagen toestaan, leidt het verzenden van een nieuw formulierexemplaar met een bijlage op een widget die al een vorige bijlage heeft, tot de weergave van een foutcode. NPR-1484

* Wanneer u een slimme verzameling maakt, blijft de stijltag niet behouden wanneer de slimme verzameling wordt opgeslagen. NPR-15081: Hotfix voor CQ-4195494
* Zoekopdrachten voor middelen worden langzaam uitgevoerd in de aanraakinterface tijdens gelijktijdige zoekopdrachten door meerdere gebruikers. NPR-15019: Hotifx voor CQ-4195405
* Metagegevens die zijn geëxtraheerd voor een eigenschap van het type `Long[]` worden omgezet in type `String[]` wanneer het oorspronkelijke element opnieuw wordt geüpload naar een andere locatie. NPR-15016: Hotfix van CQ-4195005

* Gebruikers kunnen een opgeslagen zoekopdracht of een slimme verzameling niet verwijderen. NPR-14924: Hotfix voor CQ-108494
* Als u metagegevens voor elementen in bulk bewerkt (toevoegmodus) terwijl u een Booleaanse waarde voor TypeHint gebruikt in een vervolgkeuzelijst in het onderliggende metagegevensschema, treedt er een fout op. NPR-14529: Hotfix voor CQ-106876
* Gebruikers met replicatierechten kunnen nu de mappen Asset verwijderen. NPR-14321: Hotfix voor CQ-88271
* Wanneer u probeert de videoprofielen voor een video te bewerken in de Kanaaleditor, wordt het dialoogvenster voor het ontwerp niet geopend en wordt een null pointer-uitzondering in het foutenlogboek weergegeven. NPR-14144: Hotfix voor CQ-81101
* De door het systeem gegenereerde tijdstempeleigenschap &#39;Gemaakt&#39; die op de eigenschappenpagina voor een element wordt weergegeven, is onjuist. NPR-13992: Hotfix voor CQ-95029
* Verzoek om detectie van dubbele middelen voor gebruikers zonder leestoegang in AEM Assets NPR-13851: Hotfix voor CQ-102281
* Gebruikers kunnen geen metagegevens voor elementen in bulk op de pagina Eigenschappen bewerken. NPR-13721: Hotfix voor CQ-100703
* Onjuist foutbericht in klassieke gebruikersinterface wanneer een dubbel element wordt geüpload. Het foutbericht geeft niet aan waarom het uploaden is mislukt. NPR-13691: Hotfix voor CQ-99272
* AEM Assets kan niet meer dan 50 elementen tegelijk op grootte sorteren in de lijstweergave wanneer de map een groot aantal elementen bevat. CQ-10058
* Als u meerdere elementen selecteert, treedt een fout op met antwoordcode - 414 (aanvraag-URI te lang) als de URI van het element/de map te lang is. NPR-13516: Hotfix voor CQ-76076
* De pagina Assets-rapport reageert niet wanneer de gebruiker alle keuzen in het dialoogvenster `Configure Columns` selecteert. NPR-13187: Hotfix voor CQ-95589
* Onverwacht gedrag van tagkiezer in Safari en Internet Explorer. NPR-13134
* Als u opgeslagen zoekopdrachten bewerkt vanuit de Assets Admin Search-rail, kunt u deze opslaan als geneste slimme selecties, wat problemen met de stabiliteit van de omgeving veroorzaakt. NPR-13119: Hotfix voor CQ-99460
* Nadat u een bestand (of map) hebt verplaatst en de naam ervan hebt gewijzigd, komen de metagegevens van `cq:name` niet meer overeen met de nieuwe bestandsnaam (mapnaam). NPR-13036: Hotfix voor CQ-99141
* Element met namen die speciale tekens bevatten, kan niet worden gedownload van de downloadkoppeling die via e-mail wordt gedeeld. NPR-12872: Hotfix voor CQ-95795
* Rapporten over bedrijfsmiddelen die buiten de box worden gegenereerd wanneer er een aanzienlijk aantal elementen is, veroorzaken zware verplaatsingen waarbij de zoekopdracht geen index- en CPU-gebruikspieken raakt. NPR-12811: Hotfix voor CQ-84409
* Gebruikers van AMS AEM Assets-auteur hebben toegang tot verschillende netwerken. Ze kunnen hun middelen niet uploaden via een &#39;chunk upload&#39; zonder machtigingen voor mappen te verwijderen. NPR-12768: Hotfix voor CQ-82715
* Bij zoekopdrachten op basis van tags naar elementen met behulp van de Asset Search-rail beperkt de functie Type Ahead zich niet tot het hoofdpad en worden er tags van alle naamruimten weergegeven. NPR-1266
* De component StaticRenditions heft een ongeldige wijzeruitzondering op. NPR-12665
* Verzoek om MissingMetadataNotificationJob uit te schakelen omdat de Bodge Notification UI hierdoor de pagina breekt met de runtimeuitzondering &quot;Kan invoer niet scannen.&quot; NPR-12500: Hotfix voor CQ-93573
* De optie Bewerken uitschakelen voor een tagveld werkt niet op pagina&#39;s met eigenschappen van elementen op TouchUI. NPR-12429: Hotfix voor CQ-88835
* API-oplossingen in AEM Assets 6.2 voor Companion App SMB-implementatie. NPR-11099
* Sinds de update van `Jquery` kunnen gebruikers geen elementverzameling selecteren en de selectie van een inhoudsfragment in het deelvenster Inhoud koppelen bevestigen. NPR-14847: Backport voor CQ-4194209
* Ondanks het aanroepen van oneindig sorteren aan de clientzijde, worden alleen de artikelen/banners/verzamelingen die momenteel in de gebruikersinterface worden weergegeven, gesorteerd. NPR-14493: Hotfix voor CQ-109926
* Verzoek om de onderzoekseigenschap voor AEM mobiel-op-bestelling dienst uit te voeren. Bij het zoeken met trefwoorden naar artikelen, verzamelingen of banners worden geen overeenkomsten geretourneerd. NPR-14093: Hotfix voor CQ-101394
* Wanneer het gebruiken van de koraal-uitgezochte component (*granite/ui/components/koral/foundation/form/select*) in een dialoogdoos, werkt de waardeinitialisering niet correct op Internet Explorer (browsers IE11 of Edge) wanneer de geselecteerde waarde één enkel punt bevat. NPR-13395: Hotfix voor CQ-101013

### Projecten {#projects-5}

* Wanneer het uitvoeren van een vertaalproject dat met de Methode van de Vertaling als &quot;mens&quot;en Vertaalleverancier als &quot;niets wordt gecreeerd, wordt geen vertaling_export_summary.xml- dossier geproduceerd omdat het GUID-mappingdossier mist. NPR-13137: Hotfix voor CQ-91976
* In de Projecten van de AEM, wanneer het creëren van een project met de vervaldatum geplaatste bezit, plaatst de datumomzetting de tijd verkeerd toe te schrijven aan verschil in timezone tussen server en cliënt. NPR-13003: Hotfix voor CQ-98288
* De optie &#39;Tonen in sites&#39; wordt niet opgenomen in de vertaaltaak wanneer een vertaalproject wordt bijgewerkt. NPR-12966: Hotfix voor CQ-93740
* Wanneer een vertaalproject wordt gemaakt voor een geëxporteerde sitepagina, wordt dit niet correct weergegeven in de voorvertoning. NPR-12964: Hotfix voor CQ-84627

### Workflow {#workflow-3}

* De payload-koppeling op het tabblad Archief van de Workflowconsole geeft een fout weer met antwoordcode &#39;404&#39; wanneer erop wordt geklikt. NPR-14993: Hotfix voor CQ-4194977
* Als u AEM standaardworkflows gebruikt, verzendt de CQ-server geen e-mailbericht naar de groep die het e-mailadres van één lid mist. NPR-14804: Hotfix-verzoek voor CQ-91499
* Prestatieverbeteringen voor inbox en meldingsbadge in de aanraakinterface. NPR-14145: Hotfix voor CQ-101125
* Gebruikers kunnen tijdens het starten van workflows geen voorvertoning van de payload weergeven via de Workflow Inbox-console. NPR-13226: Hotfix voor CQ-100275
* Het cookie &#39;saml_request_path&#39; dat is geconfigureerd met de SAML-verificatiehandler geeft een cookie weer die is ingesteld met een extra `?` -teken. Wanneer een SAML-reactie naar AEM wordt gepost, retourneert het cookie AEM &#39;saml_request_path&#39; een ongeldige waarde vanwege al gecodeerde tekens. NPR-13517: proactieve hotfix voor GRANITE-11722 en GRANITE-14414

### Dynamic Media {#dynamic-media}

* Talrijke `AEM-Scene7` slingertaken die zijn gemaakt en geannuleerd wanneer tijdens AEM activering als archieftaken tijdens replicatie wordt geregistreerd. NPR-12835: Hotfix voor CQ-86115

### Beveiliging {#security-5}

* Verzoek om invoervalideringsprobleem in WCMDebug-filter op te lossen. NPR-12444: Hotfix-verzoek voor CQ-94890
* Proactieve aanvraag voor het corrigeren van het XSS-gedrag tijdens het gebruik van de wizard Start maken.
NPR-13062: Hotfix-verzoek voor CQ-99577

#### Forms-invoegtoepassing {#forms-add-on-package-19}

`Adaptive Forms`

* Wanneer u een herhaalbaar deelvenster maakt met behulp van adaptieve formulieren, kan de titel van het deelvenster niet worden bijgewerkt tijdens runtime. NPR-15325
* Als u een standaardwaarde voor een keuzerondje instelt en tijdens het opslaan of verzenden een andere waarde selecteert, wordt de geselecteerde waarde niet weergegeven in de voorvoegsel. NPR-15304
* Google Chrome geeft een onjuist gedrag weer bij het gebruik van de gebeurtenis options voor het dynamisch vullen van de vervolgkeuzelijst en het verzenden van de waarde van het geselecteerde item. NPR-15198
* Wanneer u een herhaalbaar deelvenster maakt met behulp van adaptieve formulieren, kan de titel van het deelvenster niet worden bijgewerkt tijdens runtime. NPR-15181
* Bij gebruik van de bewerkingsmodus voor adaptieve formulieren worden JavaScript-fouten aangetroffen, zoals - &#39;Handler of component is invalid&#39; en &#39;guidelib is undefined&#39;. NPR-15112
* Het laden van een fragment in een herhalend deelvenster werkt niet zoals u had verwacht. NPR-13916, NPR-14785

`Correspondence Management`

* De activa van het Beheer van de correspondentie met `'Repeat with condition'` uitdrukkingsreeks worden niet behoorlijk getoond. NPR-1484
* Bij het zoeken naar een Correspondence Management-element (zoals een letter, documentfragment of een ander type) ontbreekt het pictogram Wachtrij voor downloaden op de werkbalk. NPR-14745
* Bij het maken van een lijstmodule werkt het in- en uitschakelen van de elementspecifieke eigenschappen (zoals bewerkbaar, verplicht) niet. NPR-14689
* Het paneel van Elementen van Gegevens in het nut van de Bouwer van de Uitdrukking blijft ladend voor het geval dat een voorwaardemodule wordt gecreeerd zonder een gegevenswoordenboek te selecteren. NPR-14688
* Als gebruikers een voorbeeld van een letter bekijken, kunnen ze geen tabruimten gebruiken om inhoud in tabelvorm uit te lijnen. NPR-14481
* Bij het bulksgewijs exporteren van Correspondence Management-elementen vanuit de gebruikersinterface, genereert AEM Forms Server onnodige logbestanden. NPR-15226
* Wanneer een voorvertoning van een letter wordt weergegeven, wordt uitgevulde tekst in een ander lettertype weergegeven. NPR-15468

`**Forms Portal**`

* Bijlagen van verzonden formulieren in de Forms Portal zijn niet zichtbaar wanneer een nieuw concept van de portalverzending wordt verzonden. NPR-13515

`**Forms Manager**`

* Terwijl het navigeren in de *Formulieren enDocuments* folder, wordt de knoop van het Deeg niet getoond wanneer de gebruiker om het even welke activa kopieert en dan aan een verschillende omslag navigeert. CQ-111327

#### Forms JEE Installer {#forms-jee-installer-19}

`Rights Management`

* De gebruikerslogin-gerelateerde controlegebeurtenis wordt geregistreerd met ongeldige tijd. De juiste tijd voor een auditgebeurtenis is niet traceerbaar. NPR-13107
* Adobe Acrobat Reader en Microsoft® Office kunnen geen documenten openen die zijn beveiligd met uitgebreide verificatie. NPR-14482

`Process Management`

* Wanneer een doorgestuurde concepttaak in HTML Workspace wordt geretourneerd aan de eerste gebruiker, wordt de taak niet weergegeven in de wachtrij van de eerste gebruiker. NPR-15178

`Assembler Service`

* AEM Forms kan een PDF/A-2b met meer dan twee handtekeningen niet valideren. NPR-14101

`XTG`

* Wanneer u een document afdrukt met een printeromlooplade, schakelt de functie `GeneratePrintedOutput` het ophalen van papier uit de rechteromlooplade niet in. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer loopt vast wanneer de gebruiker het hulpprogramma Spellingcontrole uitvoert met de optie Landinstelling formulier als Frans (Canada). NPR-13740
* Forms Designer loopt vast wanneer de gebruiker de gebeurtenis calculate of validate selecteert voor een formulierveld en de taal wijzigt in JavaScript en `this.` invoert in het **[!UICONTROL Script Editor]** -venster. NPR-12974

### Functiepakketten die zijn opgenomen in GVB1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms Add-on Package):

* Wanneer een adaptief formulier wordt gemaakt op basis van een XDP-bestand, wordt een setpatroon niet gevolgd bij het gebruik van de Tab-toets voor toegankelijkheid. NPR-12562

`Adaptive forms` (Forms Add-on Package):

* De Bouwer van de regel voor adaptieve vormen verleent geen op rol-gebaseerde toegang. Wijzigingen die door een auteur zijn aangebracht, kunnen niet worden bijgehouden. NPR-12840

`Core` (Forms JEE Installer):

* De functionaliteit CoreCross Origin Resource Sharing (CORS) als servletfilter wordt niet ingeschakeld voor JBoss®+. NPR-13050

## Instructies voor gestreken fijn papier downloaden via softwaredistributie {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Voor AEM Forms-klanten is het van essentieel belang dat het invoegpakket voor AEM formulieren wordt geïnstalleerd nadat AEM Service Pack, Cumulative Service Pack of Feature Pack is geïnstalleerd.

U kunt het GVB-pakket direct van de Distributie van de Software downloaden of de volgende stappen uitvoeren:

1. Open [ Distributie van de Software ](https://experience.adobe.com/downloads). U hebt een Adobe ID nodig om u aan te melden bij de softwaredistributie.
1. Tik **[!UICONTROL Adobe Experience Manager]** beschikbaar in het koptekstmenu.
1. Tik op de pakketnaam, selecteer **[!UICONTROL Accept EULA Terms]** en tik op **[!UICONTROL Download]** .

## Installatie-instructies voor GVB {#installation-instructions-for-cfp}

Deze sectie doorloopt u door de vereisten en de stappen om GVB te installeren.

### Voordat u gaat installeren {#before-you-install}

>[!NOTE]
>
>Optionele functiepakketten die door de Adobe worden geleverd, zijn afhankelijk van de releaseversie en het Cumulative Fix Pack. Als u om het even welk Pak van de Eigenschap geïnstalleerd hebt, contacteer het [ team van de Zorg van de AEM van de Klant ](https://experienceleague.adobe.com/?support-solution=General#support) om de verenigbaarheid met dit Cumulatieve Pak van de Fix voor AEM 6.2 te bevestigen.

>[!NOTE]
>
>U wordt aangeraden validatie uit te voeren voor elk nieuw installatiepakket voordat u probeert het pakket te installeren. Voorafgaande validatie analyseert en rapporteert eventuele fouten die vóór de installatie zijn gevonden, en waarschuwt de gebruikers proactief voor dergelijke fouten, overlays en machtigingen.
>

* AEM 6.2 Service Pack 1 is een voorwaarde voor het GVB. Voor installatieinstructies, zie de versienota&#39;s voor [ AEM 6.2 Service Pack 1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

* De cumulatieve download van het Pak van de Fix is beschikbaar op [ Distributie van de Software ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html), die u tot direct van de AEM instantie kunt toegang hebben.
* Voor een clusterplaatsing die (RDBMK of MongoDB) gebruikt, kan het pakket van GFP op om het even welke instanties van de Auteur worden geïnstalleerd die de Manager van het Pakket gebruiken.

* Voordat u het Cumulative Fix Pack installeert, moet u zorgen dat u een momentopname maakt of een back-up maakt van uw AEM.
* Het verwijderen van het GVB wordt niet ondersteund.

### Het GVB installeren door middel van softwaredistributie {#install-the-cfp-via-package-share}

Voer de volgende stappen uit om het Cumulative Fix Pack op een bestaande AEM 6.2 SP1-instantie te installeren:

1. Om het pakket te downloaden, klik [ Distributie van de Software ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip).

1. Open [ Manager van het Pakket ](http://localhost:4502/crx/packmgr/index.jsp) en klik **[!UICONTROL Upload Package]** om het pakket te uploaden.

1. Selecteer de pakketnaam en klik op **[!UICONTROL Install]** .

### Automatische installatie {#automatic-installation}

Het GVB kan automatisch in een lopende instantie op de volgende manieren worden geïnstalleerd:

* Plaats het pakket in ../crx-quickstart/install terwijl de server actief is. Het pakket wordt automatisch geïnstalleerd.
* Gebruik [ HTTP API van de Manager van het Pakket ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) - zorg ervoor dat u `cmd=install&recursive=true` gebruikt - zodat wordt het genestelde pakket geïnstalleerd.

### Installatie valideren {#validate-installation}

1. Op de pagina Productinformatie (/system/console/productinfo) moet nu de bijgewerkte versietekenreeks &quot;Adobe Experience Manager, Version 6.2.0.SP1-GVB20&quot; onder Geïnstalleerde producten worden weergegeven.
1. Alle bundels OSGI zijn of ACTIEF of FRAGMENT in de Console OSGi (de Console van het Gebruik: /system/console/bundels).

>[!NOTE]
>
>Bij een geslaagde installatie van het pakket wordt een informatief bericht weergegeven met de melding dat het inhoudspakket is geïnstalleerd, zoals &quot;Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-GVB20 is geïnstalleerd.&quot;

>[!NOTE]
>
>Sinds AEM 6.2 SP1-GVB1, is het logboekniveau in Jackrabbit FileVault veranderd van INFO in DEBUG voor de meeste berichten. Om installatielogboeken voor een inhoudspakket te verkrijgen dat op AEM 6.2 SP1-GVB1 of hoger wordt geïnstalleerd, laat het niveau van het FOUTOPSPORINGSlogboek voor `org.apache.jackrabbit.vault.packaging.impl` toe.

### AEM Forms installeren {#install-forms}

>[!NOTE]
>
>Sla deze sectie over als u AEM Forms niet gebruikt.

#### AEM Forms-invoegtoepassing installeren {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms op JEE slechts**) De procedure om een GFP op AEM Forms op JEE te installeren wordt beschreven in [ het Installeren van GFP op AEM Forms JEE ](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Zorg ervoor dat u het AEM 6.2 SP1 pakket van GFP hebt geïnstalleerd.
1. Download het overeenkomstige Forms toe:voegen-op pakket dat bij [ wordt vermeld de versies van AEM Forms ](aem-forms-releases.md) voor uw werkend systeem.
1. Installeer het toe:voegen-op pakket van Forms zoals die in [ wordt beschreven het Installeren AEM vormen toe:voegen-op pakketten ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

#### AEM Forms JEE-bundelpakket installeren {#install-aem-forms-jee-bundles-package}

Correcties in AEM Forms JEE worden geleverd via een afzonderlijk installatieprogramma. Voor informatie over het installeren van GFP op AEM Forms op JEE, zie [ Installing GFP op AEM Forms JEE ](install-cfp-aem-forms-jee.md).

#### Forms Designer-installatieprogramma {#designer-installer}

1. Als u de update wilt installeren, voert u het bestand Designer6.2.0_&lt;Language>_Cumulative_QF.msp uit.
1. Voor het welkomstscherm, klik **update**. De installatie wordt gestart.
1. Nadat de installatie voltooit, klik **beëindigen**.

## Door de gebruiker configureerbare time-outparameters voor DTM, Analytics, Target Connections {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Met AEM Cumulatieve Pak 6.2 SP1-GFP7 van de Moeilijke situatie en recentere versies, zijn de onderbrekingsperiodes van de verbindingsperiode configureerbaar gemaakt op alle bovengenoemde verbindingen zoals hieronder beschreven:

| **Verbindingen** | **tijd van de Verbinding uit&#42;** | **tijd van de Zak uit&#42;&#42;** |
|---|---|---|
| DTM | 30000 milliseconden | 30000 milliseconden |
| Analyse | 30000 milliseconden | 30000 milliseconden |
| Doel | 60000 milliseconden | 30000 milliseconden |

* **tijd van de Verbinding uit&#42;** - tijd uit in milliseconden tot een verbinding wordt gevestigd. Een time-outwaarde nul wordt geïnterpreteerd als een oneindige time-out.
* **Tijd van de Zak uit&#42;&#42;** - Tijd uit in milliseconden voor het wachten op gegevens of een maximumperiode van inactiviteit tussen twee opeenvolgende gegevenspakketten.

## Replicatiestatus uitschakelen in taggen-console (Classic UI) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Voor het geval u GVB3 of later gebruikt, volg deze instructies om de Status van de Replicatie in de Tagingconsole in Klassieke UI onbruikbaar te maken:

* Bedekking *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* in *`/apps`*

* Voeg `replicationStateRequired` toe: &quot;false&quot; na regel #416.

```js
415 baseParams: {
416 count: "false",
417 "replicationStateRequired": "false"
418 },
```

## De nieuwste Java™ 8 Update 131 genereert een uitzondering (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Deze configuratie-instellingen zijn specifiek voor AEM Forms-klanten die gebruikmaken van Documentbeveiliging.

NPR-21355 is opgenomen in GVB12.1. Als u GVB12.1 of later installeert, dan voer de hieronder procedure uit om NPR-21355 op de JBoss® toepassingsserver te vormen. Als u CFP12.1 installeert op AEM Forms Server die op de toepassingsservers van WebLogic of IBM® WebSpehere van het Oracle draait, wordt geen extra configuratie vereist:

1. Maak een back-up van het bestand module.xml, verwijder het bestand en maak het bestand module.xml. De standaardplaats van het dossier is [ AEM_Forms_Installation_directory ] /jbaas/modules/system/layers/base/com/adobe/livecycle/main/

1. Open het nieuwe module.xml- dossier voor het uitgeven. Voeg de volgende code toe aan het bestand:

```xml
<module xmlns="urn:jboss:module:1.1"
name="com.adobe.livecycle">
<resources>
<resource-root path="cryptojcommon.jar"/>
<resource-root path="cryptojce.jar"/>
<resource-root path="jcmFIPS.jar"/>
<resource-root path="certj.jar"/>
<resource-root path="cglib.jar"/>
</resources>
<dependencies>
<module name="javax.api"/>
<module name="asm.asm"/>
</dependencies>
</module>
```

1. Creeer een steun van `jsafeFIPS.jar`, `jsafeJCEFIPS.jar`, en `certjFIPS.jar` dossiers bij [ AEM_Forms_Installation_directory ]`/jboss/modules/system/layers/base/com/adobe/livecycle/main/` en schrap de dossiers van de eerder vermelde folder.

De Steun van de Adobe van het contact ](https://experienceleague.adobe.com/?support-solution=General#support) zodat kunt u nieuwe JAR dossiers krijgen. [ Plaats de JAR dossiers die van [ worden verkregen de Steun van de Adobe ](https://experienceleague.adobe.com/?support-solution=General#support) bij [ AEM_Forms_Installation_directory ]/jreliëf/modules/system/layers/base/com/adobe/livecycle/main/

1. (Alleen Windows) Wijzig de `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` - of `domain.conf.bat` -configuratiebestanden:

* Voor JBoss® server in standalone configuratie, open standalone.conf.bat voor het uitgeven.
* Voor JBoss® server in clusterconfiguratie, open domain.conf.bat voor het uitgeven.

  Voeg de volgende regels aan het einde toe en sla het bestand op:

  Instellen `JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true`

  Instellen `JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE`

1. (Op Linux-Gebaseerd OS slechts) wijzig [ AEM_Forms_Installation_directory ] /jboss/standalone.conf of domain.conf configuratiedossiers:

* Voor JBoss® server in standalone configuratie, open standalone.conf voor het uitgeven.
* Voor JBoss® server in clusterconfiguratie, open domain.conf voor het uitgeven.

  Voeg de volgende regels aan het einde toe en sla het bestand op:

  `JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"`

  `JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"`

## Voor NPR-1978 vereiste configuratie-instellingen {#configuration-settings-required-for-npr}

>[!NOTE]
>
>De NPR-1978 maakt deel uit van GVB14.

De telling voor gedeelde Rij verfrist zich niet voor andere gebruikers wanneer een gebruiker een taak eist. Als zodanig heeft de Adobe een nieuwe eigenschap ingevoerd. Voer de onderstaande stappen uit om deze eigenschap op uw AEM-instantie te configureren:

1. Ga naar Beheer UI -> Services -> Workspace -> Wereldwijd beheer.
1. Algemene instellingen exporteren.
1. Voeg de tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>` toe in het gedownloade XML-bestand. Ten is de voorbeeldwaarde in seconden. U kunt het dienovereenkomstig wijzigen.
1. Sla het bestand op.
1. Ga terug naar de interface van Admin -> Services -> Workspace -> Wereldwijd beheer.
1. Importeer het XML-bestand in het gedeelte Algemene instellingen importeren.
1. U kunt zich nu afmelden bij het systeem en u opnieuw aanmelden.
1. De telling voor gedeelde rij begint voor andere gebruikers in de werkruimte te verfrissen.
1. Als u de opiniepeiling wilt uitschakelen, wijzigt u de waarde in 0 en importeert u het XML-bestand opnieuw.

## UI-wijzigingen {#ui-changes}

* Gedragswijziging bij het weergeven van titels op afbeeldingskaart voor afbeelding waarbij de eigenschap `dc:title` is ingesteld op String [] ( multifield ): alleen de meest recente gewijzigde titel wordt weergegeven op de afbeeldingskaart in de gebruikersinterface, hoewel alle titels zijn opgeslagen in CRX. Hotfix voor CQ-4217165

## Bekende problemen {#known-issues}

* Het bijwerken AEM 6.2SP1-GVB19 en AEM 6.2SP1-GFP20 van GFP18 verandert de wortelomleiding aan de Klassieke UI welkomstpagina in plaats van /sites.html/inhoud. Mogelijk moet u sling corrigeren: doeleigenschap van /welcome.html naar /index.html met CRX Explorer. Dit probleem wordt niet waargenomen bij de bijwerking van de versie van GVB17 of ouder.

De volgende voorbijgaande fouten kunnen voorkomen wanneer u AEM 6.2 SP1-GVBx installeert. Voor deze fouten is echter geen resolutie vereist, omdat deze geen invloed hebben op uw AEM-exemplaar en worden verwijderd nadat het GVB is geïnstalleerd:

* Bij het bevorderen van AEM 6.2SP1-GVB20 instantie aan AEM 6.5, kunnen sommige ijdelheid URLs niet als werken:

* */projects.html*
* */sites.html*

De oplossing is echter om de AEM na een upgrade opnieuw te starten.

* De interne Fout van de Server van HTTP 500 wordt ontvangen wanneer de de componentendetailpagina van de Console van het Web wordt geopend.
* De fouten zoals **creëren componenteninstantie** en **de fabriek van de Dienst teruggekeerde ongeldig** komt toe toe te schrijven aan het nieuwe begin van de gegevensopslagruimte:

* com.day.cq.cq-verpersoonlijking [ com.day.cq.personalization.impl.DefaultProfileProvider (938) ] kan componenteninstantie tot stand brengen toe te schrijven aan gebrek om verwijzing profileManager te binden
* org.apache.sling.commons.planner FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Component: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* De fout die in de installatie van GFP in Mongo en DB2® wordt waargenomen: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Uitzondering: java.lang.NullPointerException**. Deze fout treedt niet op na de installatie van een GVB op GVB8.
* (Adobe Granite Maintenance Scheduler Update Task) com.adobe.granite.Maintenance.impl.TaskScheduler: Geen onderhoudstaak gevonden met naam WorkflowPurgeTask voor venster `granite:weekly`
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* Wanneer u GVBx op AEM 6.2 SP1 installeert die het Slimme Pak van de Eigenschap van Markeringen omvat, wordt de eerder toegevoegde werkschemastap voor Slimme Markering Assets geschrapt van het werkschema van de Activa van de Update DAM.

## Uber Jar {#uber-jar}

Uber Jar voor 6.2 SP1-GVB20 is beschikbaar bij de Adobe Public Maven bewaarplaats.

Om Uber Jar in een Geweven project te gebruiken, omvat het volgende gebiedsdeel in uw project POM:

```XML
<dependency>
 <groupId>com.adobe.aem</groupId>
 <artifactId>uber-jar</artifactId>
 <version>6.2.SP1-CFP20</version>
 <classifier>apis</classifier>
 <scope>provided</scope>
</dependency>
```

## SDAB-pakketten en -inhoudspakketten {#osgi-bundles-and-content-packages-included-5}

In de volgende tekst wordt de lijst met OSGI-bundels en -inhoudspakketten in het GVB opgenomen.

* [Lijst van OSGi-bundels opgenomen in AEM 6.2 SP1-GVB20](assets/do-not-localize/updated.txt)
* [Lijst met inhoudspakketten die zijn opgenomen in AEM 6.2SP1-GVB20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [ AEM 6.2 hotfixes pagina ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [ AEM 6.2 de versienota&#39;s van SP1 ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [ AEM 6.2 versienota&#39;s ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [ AEM productpagina ](https://business.adobe.com/products/experience-manager/adobe-experience-manager.html)
>* [ AEM 6.2 documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [ Updates van het Product van de Prioriteit van de Adobe de Updates ](https://experienceleague.adobe.com/en/docs/release-notes/experience-cloud/current)
