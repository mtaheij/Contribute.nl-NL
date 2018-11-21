---
title: Bijdrageproces voor .NET-documentopslagplaatsen
description: In dit artikel vindt u een korte inleiding tot bijdragen aan de opslagplaatsen voor .NET-documenten. U krijgt informatie over de gebruikte opslagplaatsen, het proces voor het rangschikken van inhoud en de beleidsregels voor het beheren van codevoorbeelden en andere assets.
ms.date: 11/07/2018
ms.openlocfilehash: b83a3080f1abd4df8caaa9d10859760006216e86
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609757"
---
# <a name="process-for-contributing-to-net-docs"></a>Proces voor bijdragen aan .NET-documenten

We stellen bijdragen vanuit de community aan documenten zeer op prijs. De volgende lijst bevat een aantal richtlijnen waarmee u rekening moet houden wanneer u een bijdrage levert aan de .NET-documentatie:

- **NIET DOEN**: verras ons niet met grote pull-aanvragen. In plaats daarvan kunt u beter een actie-item aanmaken, zodat we in gesprek kunnen gaan over de richting die we op moeten gaan voordat u hier erg veel tijd in gaat steken.
- **DOEN**: volg deze instructies en de richtlijnen voor [stijl en stem](dotnet-voice-tone.md).
- **DOEN**: gebruik het [sjabloonbestand](dotnet-style-guide.md) als beginpunt van uw werk.
- **DOEN**: maak een aparte vertakking van uw fork voordat u aan de artikelen gaat werken.
- **DOEN**: volg de [GitHub Flow-workflow](https://guides.github.com/introduction/flow/).
- **DOEN**: plaats regelmatig blogs en tweets (of wat u maar wilt) over uw bijdragen.

Volg deze richtlijnen zodat we allemaal een betere ervaring hebben.

## <a name="make-a-contribution-to-net-docs"></a>Een bijdrage leveren aan .NET-documenten

**Stap 1**: sla deze stap over als u alleen kleine wijzigingen wilt aanbrengen. Als u nieuwe inhoud wilt gaan schrijven of bestaande inhoud grondig wilt reviseren, opent u een [actie-item](https://github.com/dotnet/docs/issues) waarin u beschrijft wat u wilt doen.

De inhoud in de map met **documenten** is in secties onderverdeeld. Deze secties vindt u terug in de inhoudsopgave. Definieer de locatie van het onderwerp in de inhoudsopgave. Krijg feedback over uw voorstel.

-of-

U kunt ook een van de bestaande actie-items kiezen waarvoor bijdragen uit de community kunnen worden geleverd. Onder [Projecten voor bijdragers uit de .NET-community](https://github.com/dotnet/docs/projects/35) staan veel van de actie-items die voor bijdragers uit de community beschikbaar zijn. Afhankelijk van uw interesse en mate van betrokkenheid kunt u actie-items kiezen in de volgende categorieën:

- **Onderhoud**. Deze categorie bevat redelijk eenvoudige bijdragen, zoals het herstellen van gebroken of onjuiste koppelingen, het toevoegen van ontbrekende codevoorbeelden of het oplossen van problemen met beperkte inhoud. In enkele gevallen gaat het bij deze actie-items om een groot aantal bestanden. In dat geval moet u ons, voor u begint, laten weten waaraan u wilt werken. Voeg een opmerking toe aan het actie-item om ons te melden dat u hieraan werkt.

- **Updates van de inhoud**. Gezien de grote omvang van de documentenset kan inhoud eenvoudig verouderd raken, waardoor revisie is vereist. Daarnaast kunnen, om tal van redenen, twee of zelfs drie exemplaren van hetzelfde inhoudsitem bestaan. Wanneer u inhoud bijwerkt, moet u ervoor zorgen dat afzonderlijke onderwerpen actueel zijn of inhoud in een functiegebied reviseren, om dubbele items te vermijden en ervoor te zorgen dat alle unieke inhoud in de kleinere documentenset wordt bewaard.

- **Nieuwe inhoud schrijven**. Als u uw eigen onderwerp wilt schrijven, vindt u bij deze actie-items een aantal onderwerpen die we graag aan onze documentenset willen toevoegen. Wel willen we graag dat u ons informeert voordat u aan een onderwerp gaat werken. Als u een onderwerp wilt gaan schrijven dat niet in de lijst staat, kunt u een actie-item openen.

Of bekijk onze lijst met [openstaande actie-items](https://github.com/dotnet/docs/issues) en werk vrijwillig aan een van de actie-items waarin u geïnteresseerd bent. We gebruiken het label [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) (beschikbaar) om actie-items te taggen waaraan de community een bijdrage kan leveren. Voor dergelijke actie-items is vaak maar minimale context nodig. Ze zijn zeer geschikt voor gebruikers die voor de eerste keer aan een actie-item werken. We stimuleren ervaren bijdragers in onze community om naar actie-items te kijken die mogelijk interessant voor hen zijn. Wanneer u een dergelijk actie-item vindt, voegt u een opmerking toe om te vragen of dit item openstaat.

Zodra u een taak hebt gekozen om aan te werken, volgt u de instructies om [aan de slag](get-started-setup-github.md) te gaan om een GitHub-account te maken en uw omgeving in te stellen.

**Stap 2:** maak waar nodig forks van de opslagplaatsen `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` of `dotnet/ml-api-docs` en maak een vertakking voor uw wijzigingen.

Voor kleine wijzigingen leest u de instructies voor bewerkingen in GitHub op de [startpagina](index.md#quick-edits-to-existing-documents) van de handleiding van de bijdrager.

**Stap 3:** breng de wijzigingen in deze nieuwe vertakking aan.

Als het een nieuw onderwerp is, kunt u dit [sjabloonbestand](dotnet-style-guide.md) als beginpunt gebruiken. Dit bestand bevat de schrijfrichtlijnen en uitleg over de metagegevens die voor elk artikel zijn vereist, zoals informatie over de auteur.

Navigeer naar de map die overeenkomt met de locatie in de inhoudsopgave die u in stap 1 voor uw artikel hebt bepaald. Die map bevat de Markdown-bestanden voor alle artikelen in dat hoofdstuk. Maak indien nodig een nieuwe map waarin u de bestanden voor uw inhoud plaatst. Het hoofdartikel voor dat hoofdstuk heet *index.md*. Voor afbeeldingen en andere statische resources maakt u de submap **media** in de map waarin uw artikel staat, als deze submap nog niet is gemaakt. Maak in de map **media** een submap met de naam van het artikel (met uitzondering van het indexbestand). Voorbeeldcode moet in de opslagplaats `dotnet/samples` staan, zoals beschreven in de sectie over [voorbeelden](#contributing-to-samples).

Volg de juiste Markdown-syntaxis. Voor voorbeelden van algemene syntaxis raadpleegt u het [sjabloon en Markdown-cheatsheet](dotnet-style-guide.md).

## <a name="example-structure"></a>Voorbeeldstructuur

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**Stap 4:** dien een PR (Pull Request - pull-aanvraag) in van uw vertakking naar de hoofdvertakking.

> [!IMPORTANT]
> De functionaliteit [automatisering van commentaar](how-to-write-workflows-major.md#review-and-sign-off) is op dit moment in geen enkele .NET-documentenopslagplaats beschikbaar. Leden van het .NET-documententeam zullen uw pull-aanvraag beoordelen en samenvoegen.

Per aanvraag mag per keer één actie-item worden behandeld. Met de aanvraag kunnen een of meerdere bestanden worden aangepast. Als u oplossingen van meerdere problemen in verschillende bestanden wilt aanpakken, kunt u beter afzonderlijke pull-aanvragen gebruiken. Als u niet alleen markdown bijwerkt maar ook voorbeelden maakt, moet u een afzonderlijke pull-aanvraag voor voorbeelden maken.

Als u met uw pull-aanvraag een bestaand probleem oplost, voegt u het trefwoord `Fixes #Issue_Number` toe aan het Commit-bericht of de beschrijving van de pull-aanvraag. Op die manier wordt het actie-item automatisch afgesloten zodra de pull-aanvraag is samengevoegd. Zie [Actie-items afsluiten via Commit-berichten](https://help.github.com/articles/closing-issues-via-commit-messages/) voor meer informatie.

Het .NET-team beoordeelt uw pull-aanvraag en laat u weten of er andere updates/wijzigingen nodig zijn voor de goedkeuring.

**Stap 5:** voer eventuele benodigde updates aan uw vertakking door die u met het team hebt besproken.

De onderhoudsmedewerkers voegen uw pull-aanvraag samen met de hoofdvertakking zodra feedback is toegepast en uw wijziging is goedgekeurd.

We pushen regelmatig alle commits van de hoofdvertakking naar de livevertakking; u kunt uw bijdrage dan live bekijken op https://docs.microsoft.com/dotnet/. Normaalgesproken publiceren we deze elke werkdag. Door onderhoudswerkzaamheden wordt de publicatie mogelijk enkele dagen vertraagd.

## <a name="contributing-to-samples"></a>Bijdragen aan voorbeelden

In de opslagplaats [dotnet/voorbeelden](https://github.com/dotnet/samples) staat alle voorbeeldcode die deel uitmaakt van onderwerpen in de .NET-documentatie. Er zijn diverse projecten die in submappen zijn onderverdeeld. Deze submappen zijn op vergelijkbare wijze ingericht als de documenten voor .NET.

We maken het volgende onderscheid voor code die in onze opslagplaats aanwezig is:

- Voorbeelden: lezers kunnen de voorbeelden downloaden en uitvoeren. Alle voorbeelden moeten volledige toepassingen of bibliotheken zijn. In het geval het voorbeeld een bibliotheek maakt, moet deze eenheidstesten of een toepassing bevatten waarmee lezers de code kunnen uitvoeren. Vaak wordt meer dan één technologie, functie of toolkit gebruikt. Het readme.md-bestand voor elk voorbeeld verwijst naar het artikel zodat u meer kunt lezen over de concepten die in de voorbeelden worden gegeven.
- Codefragmenten: hiermee geeft u uitleg over een kleiner concept of een kleinere taak. U kunt ermee compileren, maar ze zijn niet bedoeld om als complete toepassing te gebruiken. Ze moeten wel op de goede manier worden uitgevoerd, maar ze zijn geen voorbeeldtoepassing voor een typisch scenario. In plaats daarvan zijn ze ontworpen om zo klein mogelijk te zijn om één concept of functie uit te leggen. Deze fragmenten moeten niet langer zijn dan één scherm met code.

Alle code bevindt zich in de opslagplaats [dotnet/voorbeelden](https://github.com/dotnet/samples). We werken aan de ontwikkeling van een model waarin de structuur van onze map met voorbeelden overeenkomt met de structuur van onze map met documenten. We volgen de volgende standaarden:

- De map *codefragmenten* op het hoogste niveau bevat codefragmenten voor kleine, doelgerichte voorbeelden.
- Er worden API-verwijzingsvoorbeelden in een map geplaatst volgens dit patroon: *snippets/\<language>/api/\<namespace>/\<apiname>*.
- Andere mappen op het hoogste niveau komen overeen met de mappen op het hoogste niveau in de opslagplaats *documenten*. De opslagplaats Documenten bevat bijvoorbeeld de map *machine learning/zelfstudies* en de voorbeelden voor zelfstudies over machine learning bevinden zich in de map *voorbeelden/machine learning/zelfstudies*.

Daarnaast moeten alle voorbeelden in de mappen *kern* en *standaard* worden ontwikkeld en uitgevoerd op alle platformen die door .NET Core worden ondersteund. Dit zal door ons CI-ontwikkelingssysteem worden afgedwongen. De map *framework* op het hoogste niveau bevat voorbeelden die alleen in Windows worden ontwikkeld en gevalideerd.

Voorbeeldprojecten moeten worden ontwikkeld en uitgevoerd op de breedste set platformen die voor het gegeven voorbeeld mogelijk is. In de praktijk betekent dit dat u waar mogelijk consoletoepassingen op basis van .NET Core moet ontwikkelen. Voor voorbeelden die specifiek zijn voor internet of een UI-framework moeten die hulpprogramma's waar nodig worden toegevoegd. Voorbeelden zijn bijvoorbeeld webtoepassingen, mobiele apps, WPF of WinForms-apps.

We werken aan de ontwikkeling van een CI-systeem voor alle code. Wanneer u voorbeelden bijwerkt, moet u ervoor zorgen dat elke update deel uitmaakt van een project dat kan worden ontwikkeld. U kunt het beste ook testen toevoegen om te controleren of de voorbeelden correct zijn.

Elk volledige voorbeeld dat u maakt, moet een *readme.md*-bestand bevatten. Dit bestand moet een korte beschrijving van het voorbeeld (van 1 à 2 paragrafen) bevatten. Uit het *readme.md*-bestand moeten lezers kunnen opmaken wat ze gaan leren wanneer ze dit voorbeeld verkennen. In het *readme.md*-bestand moet ook een koppeling naar het live-document op de [.NET-documentatiesite](https://docs.microsoft.com/dotnet/welcome) staan. Vervang `/docs` in het pad van de opslagplaats door `http://docs.microsoft.com/dotnet` om te bepalen op welke locatie een bepaald bestand in de opslagplaats aan die site wordt toegewezen.

Uw onderwerp bevat ook koppelingen naar het voorbeeld. Geef een directe koppeling op naar de map van het voorbeeld op GitHub.

### <a name="writing-a-new-snippet-or-sample"></a>Een nieuw codefragment of voorbeeld schrijven

1. Uw voorbeeld **moet deel uitmaken van een project dat kan worden ontwikkeld**. De projecten moeten waar mogelijk worden ontwikkeld op alle platformen die door .NET Core worden ondersteund, met uitzondering van voorbeelden die functies of hulpprogramma's aangeven die specifiek bij een platform horen.

2. Uw voorbeeld moet, met het oog op consistentie, aan de [corefx-coderingsstijl](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) voldoen.

    - Daarnaast kunt u beter `static`-methoden gebruiken in plaats van de instantiemethoden wanneer u iets wilt tonen waarvoor het niet nodig is om een nieuw object te instantiëren.

3. Uw voorbeeld moet over **de juiste verwerking van uitzonderingen** beschikken. Alle uitzonderingen moeten kunnen worden verwerkt die zich in de context van het voorbeeld kunnen voordoen. Een voorbeeld waarmee bijvoorbeeld de methode [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) wordt aangeroepen om gebruikersinvoer op te halen, moet de juiste verwerking van uitzonderingen gebruiken wanneer een ingevoerde tekenreeks als argument naar een methode wordt doorgestuurd. Als uw voorbeeld verwacht dat een methode-aanroep zal mislukken, moet de resulterende uitzondering ook worden verwerkt. Verwerk altijd de specifieke uitzonderingen die de methode opwerpt en niet de uitzonderingen uit de basisklasse zoals [Exception](https://docs.microsoft.com/dotnet/api/system.exception) of [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

4. Als u met uw voorbeeld een zelfstandig pakket bouwt, moet u, naast de runtimes die door uw voorbeeld worden gebruikt, ook de runtimes opgeven die door ons CI-ontwikkelingssysteem worden gebruikt:
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

Op korte termijn zal er een CI-systeem beschikbaar zijn om deze projecten te ontwikkelen.

U maakt als volgt een voorbeeld:

1. Meld een [actie-item](https://github.com/dotnet/docs/issues) aan of voeg commentaar toe aan een bestaand actie-item waaraan u werkt.
2. Schrijf het onderwerp waarin de concepten worden uitgelegd die in uw voorbeeld worden aangegeven (bijvoorbeeld: `docs/standard/linq/where-clause.md`).
3. Schrijf uw voorbeeld (voorbeeld: `WhereClause-Sample1.cs`).
4. Maak een Program.cs met een hoofdinvoerpunt waardoor uw voorbeelden worden aangeroepen. Als er al een aanroep bestaat, voegt u deze aan uw voorbeeld toe:
    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```
U kunt .NET Core-codefragmenten of -voorbeelden bouwen met behulp van de .NET Core SLI. Deze kunt u installeren met de [.NET Core SDK](https://www.microsoft.com/net/download). U kunt uw voorbeeld als volgt bouwen en uitvoeren:

1. Ga naar de map met voorbeelden en bouw uw voorbeeld om op fouten te controleren:

    ```console
    dotnet build
    ```
2. Voer uw voorbeeld uit:

    ```console
    dotnet run
    ```

3. Voeg een readme.md-bestand toe aan de hoofdmap van uw voorbeeld. 

   Dit bestand moet een korte beschrijving van de code bevatten en mensen verwijzen naar het artikel waarin het voorbeeld wordt genoemd.

Met uitzondering van vermeldingen moeten alle voorbeelden vanaf de opdrachtregel worden gebouwd op platformen die door .NET Core worden ondersteund. Er zijn een aantal voorbeelden die specifiek bedoeld zijn voor Visual Studio en waarvoor Visual Studio 2017 of hoger is vereist. Daarnaast bevatten enkele voorbeelden platformspecifieke functies. Hiervoor is het specifieke platform vereist. Voor andere voorbeelden en codefragmenten is het .NET Framework vereist. Deze worden uitgevoerd op Windows-platformen en hiervoor is het Developer Pack voor de beoogde Framework-versie vereist.

## <a name="the-c-interactive-experience"></a>De interactieve C#-ervaring

Aan alle voorbeelden die in een artikel staan, wordt een [taaltag](how-to-write-use-markdown.md#code-snippets) toegevoegd om de brontaal aan te geven. Voor korte codevoorbeelden in C# kan de taaltag `csharp-interactive` worden gebruikt om een C#-voorbeeld op te geven dat in de browser wordt uitgevoerd. (Voor inlinecodevoorbeelden wordt de tag `csharp-interactive` gebruikt; voor codefragmenten die uit de bron zijn ingesloten gebruikt u de tag `code-csharp-interactive`.) Deze codevoorbeelden geven een codevenster en een uitvoervenster in het artikel weer. In het uitvoervenster wordt alle uitvoer weergegeven door het uitvoeren van de interactieve code zodra de gebruiker het voorbeeld heeft uitgevoerd.

De interactieve C#-ervaring verandert de manier waarop wij met voorbeelden werken. Bezoekers kunnen het voorbeeld uitvoeren om de resultaten te zien. Aan de hand van een aantal factoren wordt bepaald of het voorbeeld of de bijbehorende tekst informatie over de uitvoer moet bevatten.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>Wanneer moet u de verwachte uitvoer weergeven zonder het voorbeeld uit te voeren?

- Artikelen die voor beginners zijn bedoeld, moet uitvoer geven zodat lezers de uitvoer van hun werk kunnen vergelijken met het verwachte antwoord.
- Voorbeelden waarbij de uitvoer integraal deel uitmaakt van het onderwerp, moeten die uitvoer weergeven. In artikelen die bijvoorbeeld over opgemaakte tekst gaan, moet de tekstindeling worden getoond zonder het voorbeeld uit te voeren.
- Wanneer zowel het voorbeeld als de verwachte uitvoer kort is, kunt u overwegen de uitvoer weer te geven. Dit bespaart wat tijd.
- In artikelen waarin wordt uitgelegd hoe de huidige cultuur of niet-variabele cultuur invloed heeft op de uitvoer, moet de verwachte uitvoer worden verklaard. De interactieve REPL (de lus tussen lezen, evalueren en afdrukken) wordt uitgevoerd op een host op basis van Linux. De standaardcultuur en de niet-variabele cultuur produceren verschillende uitvoer op verschillende besturingssystemen en computers. In het artikel moet de uitvoer in Windows-, Linux- en Mac-systemen worden uitgelegd.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>Wanneer moet u verwachte uitvoer niet in het voorbeeld opnemen?

- In artikelen waarin het voorbeeld een langere uitvoer genereert, moet die niet in commentaar worden opgenomen. Hierdoor wordt de code verborgen zodra het voorbeeld is uitgevoerd.
- Artikelen waarin het voorbeeld een onderwerp aantoont, maar de uitvoer niet essentieel is om het onderwerp te begrijpen. Code waarmee bijvoorbeeld een LINQ-query wordt uitgevoerd om de querysyntaxis uit te leggen en vervolgens elk item in de uitvoerverzameling weer te geven.

> [!NOTE]
> U merkt wellicht dat een in aantal onderwerpen op dit moment niet alle richtlijnen worden gevolgd die hierin zijn opgegeven. We werken aan consistentie voor de hele site. Controleer de lijst met [openstaande actie-items](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) die we momenteel voor dat specifieke doel volgen.

## <a name="contributor-license-agreement"></a>Licentieovereenkomst voor bijdragers

U moet de [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) ondertekenen voordat uw pull-aanvraag wordt samengevoegd. Dit is een eenmalige vereiste voor projecten in de .NET Foundation. Ga voor meer informatie over [Contribution License Agreements (CLA's)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) naar Wikipedia.

De overeenkomst: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

U hoeft de overeenkomst niet van tevoren te ondertekenen. U kunt uw pull-aanvraag klonen, vertakken en verzenden zoals u gewend bent. Wanneer uw pull-aanvraag wordt gemaakt, wordt deze door een CLA-bot geclassificeerd. Als het een kleine wijziging betreft (u corrigeert bijvoorbeeld een typfout), dan krijgt de pull-aanvraag het label `cla-not-required`. Anders wordt de aanvraag als `cla-required` geclassificeerd. Zodra u de CLA hebt ondertekend, krijgen de huidige en alle toekomstige pull-aanvragen het label `cla-signed`.
