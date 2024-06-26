---
title: Definities van releasevoertuig bijwerken
description: In dit artikel worden de verschillende typen [!DNL Experience Manager] versies, met inbegrip van volledige versies, eigenschapspakken, en de dienstpakken.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 125bfbeb881fb86097a609d198098585f6212570
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 2%

---

# [!DNL Experience Manager] definities van releasevoertuigen bijwerken {#update-release-vehicle-definitions}

Dit document bevat details over de verschillende typen [!DNL Adobe Experience Manager] versies, met inbegrip van volledige versies, eigenschapspakken, en de dienstenpakketten die [!DNL Adobe] levert aan zijn klanten.

>[!NOTE]
>
>Voor releaseplanning van [!DNL Experience Manager] update-releases, zie [[!DNL Experience Manager] update-releases roadmap](update-releases-roadmap.md)

## Volledige release {#full-release}

| Items | Beschrijving |
|-------|------|
| Definitie | <ul> <li> Geplande release </li> <li> Ondersteunt upgradepaden voor specifieke versies die zijn gedefinieerd in de releaseopmerkingen </li> </ul> |
| Naamgeving | <ul> <li> De aantallen van de versie voor belangrijke versies stijgen gebaseerd op de formule X+1.Y.Z. </li> <li> De aantallen van de versie voor minder belangrijke versieverhoging gebaseerd op formule X.Y+1.Z </li> </ul> Waar X het primaire versienummer is, is Y het secundaire versienummer, en Z het flardaantal. |
| Inclusies | <ul> <li> Nieuwe functies </li> <li>  Verbeteringen </li> <li>  Bugfixes </li> </ul> |
| Documentatie | <ul> <li> Opmerkingen bij de release zijn beschikbaar op het documentatieportaal </li> <li> Documentatie over functies, verbeteringen en foutoplossingen is beschikbaar op het documentatieportaal </li> </ul> |
| Cadence | Jaarlijks |
| Beschikbaarheid en installatie | <ul> <li> Wordt geleverd als een zelfstandig productinstallatieprogramma </li> <li>  Beschikbaar op de website voor licentieverlening en Managed Services </li> <li> Licentiewebsite vereist mogelijk migratie van opslagplaats voor inhoud </li> </ul> |
| Testniveau | Volledig gevalideerd door QA |

## Service Pack {#service-pack}

| Item | Beschrijving |
|-----|-----|
| Definitie | <ul> <li> Geplande release </li> <li> Kan momenteel niet terugdraaien </li> </ul> |
| Naamgeving | <ul> <li> Reparatienummer is één cijfer </li> <li> Na installatie zal het geïnstalleerde de flardcijfer van het versienummer, gebaseerd op de formule X.Y.Z.SPx verhogen </li> </ul> Waar X het primaire versienummer is, is Y het secundaire versienummer, en Z het flardaantal. x is het aantal van het de dienstpak. |
| Inclusies | <ul> <li> Nieuwe functies</li> <li>  Verbeteringen </li> <li> Bugfixes </li> <li> Pakketten met kenmerken van algemeen belang (indien aanwezig) </li> </ul> |
| Documentatie | <ul> <li> Opmerkingen bij de release beschikbaar op het documentatieportaal </li> <li> Documentatie over functies, verbeteringen en foutoplossingen op het documentatieportaal </li> </ul> |
| Cadence | Driemaandelijks |
| Beschikbaarheid en installatie | <ul> <li> Geleverd als pakket </li> <li> Beschikbaar op softwaredistributie</li> <li>  Vereist bestaande functionele installatie </li> </ul> |
| Testniveau | <ul> <li> Alle oplossingen voor gevalideerde kwaliteitscontrole </li> <li>  Algemene saniteit van pakketten met automatiseringsprestaties </li> </ul> |

## Cumulatief reparatiepakket  {#cumulative-fix-pack-aem}

| Item | Beschrijving |
|-----|-----|
| Definitie | <ul> <li> Single Deliasing Model of releasing fixes </li> <li> Aggregator-inhoudspakket met inhoudspakket van afzonderlijke componenten </li> <li>  GFP&#39;s zijn rollover van hotfixes en er zijn geen verbeteringen in opgenomen.  </li> </ul> |
| Naamgeving | X.Y.Z.CFPx  <br> Waar X het primaire versienummer is, is Y het secundaire versienummer, en Z het flardaantal. x is het cumulatieve aantal van het de dienstpak. |
| Inclusies | GFP is cumulatieve fixpack die fixes van alle componenten door gespecificeerde data bevat. Bijvoorbeeld, als een klant GVB3 toepast, dan GFP3 = GFP1 + GFP2. |
| Documentatie | Opmerkingen bij de release beschikbaar op het documentatieportaal |
| Cadence | Driemaandelijks |
| Beschikbaarheid en installatie | <ul> <li> Geleverd als pakket </li> <li>  Beschikbaar op softwaredistributie </li> <li>  Afhankelijk van het nieuwste servicepakket dat wordt uitgebracht </li> <li>  Het GVB is onafhankelijk. Klanten hoeven zich geen zorgen te maken over het vinden/oplossen van afhankelijkheden. GFP zou op recentste vrijgegeven Service Pack moeten worden geïnstalleerd. </li> <li>  GFP kan als één enkel pakket worden geïnstalleerd, dat klantenervaring verbetert.  </li> </ul> |
| Testniveau | QA gevalideerd op integratieniveau en regressietests |

## Bedekking {#overlay}

| Item | Details |
|-------|--------|
| Naamgeving | bedekking-&lt;ticket id=&quot;&quot;> |
| Inclusies | Opgeloste problemen voor een JS- of JSP-bestand |
| Documentatie | Geen |
| Cadence | Indien nodig |
| Beschikbaarheid en installatie | <ul> <li> Geleverd als pakket per [!DNL Experience Manager] Klantenservice  </li> <li> Niet noodzakelijk inbegrepen in de dienstpakken of volledige versies </li> </ul> |
| Testniveau | Gevalideerd door de klantenservice |

## Functiepakket {#feature-pack}

| Items | Details |
|--------|-----|
| Definitie | <ul> <li>De Pakken van de eigenschap zijn toevoegings-functionaliteit en worden geleverd via de Pakken van de Dienst. Als een [!DNL Experience Manager] versie heeft zijn laatste de dienstpak vrijgegeven, zal de Adobe geen eigenschapspak voor het in de toekomst leveren. </li> <li> KP&#39;s bevatten productverbeteringen, gepland voor een volgende productrelease, maar vroegtijdig geleverd op basis van het besluit van [!DNL Adobe's] Productbeheer.</li> <li>  Functies worden altijd samengevoegd met de volgende hoofdrelease en vervolgens naar de [!DNL Experience Manager] versie vereist door de klant </li> <li>  De gemeenschappelijke belangen en de eigenschapspakketten van GA worden samengevoegd in het volgende de dienstpak  </li> </ul> |
| Naamgeving | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusies | <ul> <li> Nieuwe functies </li> <li> Verbeteringen </li> <li> Bugfixes (incrementele productupdates) </li> </ul> |
| Documentatie | Documentatie is beschikbaar op adobe.com. |
| Cadence | Varieert met het gebied van het Product |
| Beschikbaarheid en installatie | <ul> <li>Wordt geleverd via servicepacks </li> <li> Beschikbaar op softwaredistributie. Klanten accepteren [!DNL Adobe's] Voorwaarden via softwaredistributie. </li> </ul> |
| Testniveau | De algemene eigenschapspakketten van de Beschikbaarheid zijn gevalideerd QA. |

* 1: eiken fixes worden niet als afzonderlijke hotfixes geleverd. Zij worden echter wel opgenomen in de daaropvolgende Cumulatieve oak-hotfix. Indien nodig kan een diagnose worden gesteld die bovenop de nieuwste COFP is gebouwd. Voorwaarde is dat de klant de nieuwste COFP heeft die wordt uitgevoerd. Diagnostische builds bieden alleen dezelfde kwaliteitsgarantie als een hotfix. Daarom bieden zij niet zo veel kwaliteitsgarantie als een cumulatief fixpack, de dienstpak, of productversie. De laatste oplossing wordt geleverd bij het volgende GVB.
