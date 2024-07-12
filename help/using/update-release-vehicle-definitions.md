---
title: Definities van releasevoertuig bijwerken
description: Dit artikel detailleert de diverse types van  [!DNL Experience Manager]  versies, met inbegrip van volledige versies, eigenschappakken, en de dienstpakken.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 2%

---

# [!DNL Experience Manager] definities van releasevoertuigen bijwerken {#update-release-vehicle-definitions}

Dit document bevat informatie over de verschillende typen [!DNL Adobe Experience Manager] -releases, waaronder volledige releases, functiepakketten en servicepakketten die [!DNL Adobe] aan klanten levert.

>[!NOTE]
>
>Voor versieschema van [!DNL Experience Manager] updateversies, verwijs naar [[!DNL Experience Manager]  update versies roadmap ](update-releases-roadmap.md)

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
| Documentatie | <ul> <li> Opmerkingen bij de release zijn beschikbaar op het documentatieportaal </li> <li> Documentatie over functies, verbeteringen en foutoplossingen op het documentatieportaal </li> </ul> |
| Cadence | Driemaandelijks |
| Beschikbaarheid en installatie | <ul> <li> Geleverd als pakket </li> <li> Beschikbaar op softwaredistributie</li> <li>  Vereist bestaande functionele installatie </li> </ul> |
| Testniveau | <ul> <li> Alle oplossingen voor gevalideerde kwaliteitscontrole </li> <li>  Algemene saniteit van pakketten met automatiseringsprestaties </li> </ul> |

## Cumulatief reparatiepakket {#cumulative-fix-pack-aem}

| Item | Beschrijving |
|-----|-----|
| Definitie | <ul> <li> Single Deliasing Model of releasing fixes </li> <li> Aggregator-inhoudspakket met inhoudspakket van afzonderlijke componenten </li> <li>  GFP&#39;s zijn rollover van hotfixes en er zijn geen verbeteringen in opgenomen.  </li> </ul> |
| Naamgeving | X.Y.Z.CFPx <br> Waar X het primaire versienummer is, is Y het secundaire versienummer en Z het patchnummer. x is het cumulatieve aantal van het de dienstpak. |
| Inclusies | GFP is een cumulatief fixpack dat fixes van alle componenten door gespecificeerde data bevat. Bijvoorbeeld, als een klant GVB3 toepast, dan GFP3 = GFP1 + GFP2. |
| Documentatie | Opmerkingen bij de release zijn beschikbaar op het documentatieportaal |
| Cadence | Driemaandelijks |
| Beschikbaarheid en installatie | <ul> <li> Geleverd als pakket </li> <li>  Beschikbaar op softwaredistributie </li> <li>  Afhankelijk van het nieuwste servicepakket dat wordt uitgebracht </li> <li>  Het GVB is onafhankelijk. Klanten hoeven zich geen zorgen te maken over het vinden/oplossen van afhankelijkheden. GFP zou op het recentste vrijgegeven de dienstpak moeten worden geïnstalleerd. </li> <li>  GFP kan als één enkel pakket worden geïnstalleerd, dat klantenervaring verbetert.  </li> </ul> |
| Testniveau | QA gevalideerd op integratieniveau en regressietests |

## Bedekking {#overlay}

| Item | Details |
|-------|--------|
| Naamgeving | bedekking-&lt;ticket-id> |
| Inclusies | Opgeloste problemen voor een JS- of JSP-bestand |
| Documentatie | Geen |
| Cadence | Indien nodig |
| Beschikbaarheid en installatie | <ul> <li> Wordt geleverd als pakket door de [!DNL Experience Manager] klantenservice  </li> <li> Niet noodzakelijk inbegrepen in de dienstpakken of volledige versies </li> </ul> |
| Testniveau | Gevalideerd door de klantenservice |

## Functiepakket {#feature-pack}

| Items | Details |
|--------|-----|
| Definitie | <ul> <li>De Pakken van de eigenschap zijn toe:voegen-op functionaliteit en door een de dienstpakken geleverd. Als een [!DNL Experience Manager] -versie zijn laatste servicepack heeft uitgebracht, levert Adobe in de toekomst geen functiepakket voor dit pakket. </li> <li> FPs bevatten productverhogingen, die voor een verdere productversie, maar vroege geleverd op basis van het besluit van [!DNL Adobe's] Product Management worden gepland.</li> <li>  Functies worden altijd samengevoegd met de volgende grote release. Deze worden vervolgens naar de door de klant vereiste [!DNL Experience Manager] versie verzonden </li> <li>  De gemeenschappelijke belangen en de eigenschapspakketten van GA worden samengevoegd in het volgende de dienstpak  </li> </ul> |
| Naamgeving | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusies | <ul> <li> Nieuwe functies </li> <li> Verbeteringen </li> <li> Bugfixes (incrementele productupdates) </li> </ul> |
| Documentatie | Documentatie is beschikbaar op adobe.com. |
| Cadence | Varieert met het gebied van het Product |
| Beschikbaarheid en installatie | <ul> <li>Wordt geleverd via servicepacks </li> <li> Beschikbaar op softwaredistributie. Klanten accepteren [!DNL Adobe's] Voorwaarden via softwaredistributie. </li> </ul> |
| Testniveau | De algemene eigenschapspakketten van de Beschikbaarheid zijn gevalideerd QA. |

* 1: Oak-oplossingen worden niet als afzonderlijke hotfixes geleverd. Deze worden echter wel opgenomen in de volgende Cumulatieve hotfix voor Oak. Indien nodig kan een diagnose worden gesteld die bovenop de nieuwste COFP is gebouwd. Voorwaarde is dat de klant de nieuwste COFP heeft die wordt uitgevoerd. Diagnostische builds bieden alleen hetzelfde niveau van kwaliteitsborging als een hotfix. Daarom bieden zij niet zo veel kwaliteitsgarantie als een cumulatief fixpack, de dienstpak, of productversie. De laatste oplossing wordt geleverd bij het volgende GVB.
