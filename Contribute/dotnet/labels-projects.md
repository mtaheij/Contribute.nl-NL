---
title: Roadmap van labels en projecten
description: In dit artikel wordt uitgelegd hoe labels en projecten worden gebruikt in de dotnet/docs-opslagplaats.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "80760371"
---
# <a name="labels-and-projects-roadmap"></a>Roadmap van labels en projecten

Het team voor .NET-docs maakt uitgebreid gebruik van [GitHub-labels](https://github.com/dotnet/docs/labels) om ons werk te organiseren. Door te filteren op combinaties van labels kunnen we ons snel richten op gedeelten van belang op de website van [.NET docs](https://docs.microsoft.com/dotnet).

We gebruiken ook [GitHub-projecten](https://github.com/dotnet/docs/projects) om sprints en andere doelgerichte EPICS te organiseren.

Deze roadmap biedt uitleg over hoe we deze organisatieprogramma's gebruiken en beschikt over koppelingen naar handige filters waarmee we interessegebieden kunnen vinden.

## <a name="labels"></a>Labels

Begin, als dit de eerste keer is dat u een bijdrage levert aan [dotnet/docs](https://github.com/dotnet/docs), met de [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-problemen. Dit zijn problemen met een meer gericht bereik. Deze zijn een uitstekende manier om uw eerste bijdrage te maken. Vanuit de up-for-grabs-weergave kunt u problemen verder filteren op basis van gebieden en prioriteit. Er zijn goede problemen gevonden voor beginners met een [goed-eerste-probleem](https://github.com/dotnet/docs/labels/good-first-issue) als u eerst een kleinere bijdrage wilt proberen.

We gebruiken labels om op verschillende manieren problemen te classificeren:

- [.NET-gidsen](#find-a-single-net-guide) en [gedeelten van een gids](#search-one-section-of-a-guide).
- [Doelrelease](#releases)
- [Prioriteit](#priority)

U kunt een label van elke set (gids, release, prioriteit) combineren om voor een beperkte focus te zorgen waarmee u problemen kunt vinden waaraan u wilt werken.

### <a name="find-a-single-net-guide"></a>Eén .NET-gids zoeken

We gebruiken labels voor alle e-books over architectuur en voor elke .NET-gids.

![:book: gids op lichtgroene achtergrond](./media/labels-projects/guide.png "Voorvoegsel voor labels voor architectuurgidsen")

De e-books over architectuur worden aangeduid met het voorvoegsel `:book: guide` en hebben een lichtgroene achtergrond. Dit zijn de gebieden in lange vorm die over aanbevolen architectuur handelen. Hier worden actuele problemen gefilterd voor alle .NET-gidsen over architectuur.

- [ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker lifecycle](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernizing w/ Windows containers](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET Microservices](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Serverless apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Deze labelstijl wordt ook toegepast op de [ontwerprichtlijnen van Framework](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines). Dit gebied heeft hetzelfde labelontwerp, maar pull-aanvragen van de community worden afgeraden. Dit materiaal wordt herdrukt met toestemming en mag niet worden bewerkt.

![:books: Gebied op donkerblauwe achtergrond](./media/labels-projects/area.png "Voorvoegsel voor labels voor gebieden van .NET-gidsen")

Elke .NET-gids wordt vermeld met het voorvoegsel `:books: Area` en heeft een donkerblauwe achtergrond. Hier worden actuele problemen gefilterd voor alle .NET-gidsen.

- [API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Desktop Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - kan worden verwijderd
- [.NET Core Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - kan worden verwijderd.
- [Visual Basic Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Een gedeelte van een gids doorzoeken

![:card_file_box: Gebied op mediumblauwe achtergrond](./media/labels-projects/technology.png "Voorvoegsel voor labels voor subgebieden van .NET-gidsen")

De .NET-gidsen zijn groot, zodat deze labels het bereik verder beperken tot een gedeelte van een gids. Elk subgebied van een .NET-gids wordt vermeld met het voorvoegsel `:card_file_box: Technology` en heeft een mediumblauwe achtergrond. Veel van deze labels zijn van toepassing op meerdere gidsen, terwijl andere zich in slechts één gids bevinden. Nadat u hebt gefilterd op een gebied, voegt u een van deze labels toe om het bereik van problemen verder te beperken.

- AppCompat
- Async Task
- C# Advanced concepts
- C# compiler
- C# Fundamentals
- C# Get Started
- C# Language Reference
- C# Null safety
- C# What's new
- CLI
- Data Access
- Docker
- Installers
- LINQ
- NCL
- .NET Standard
- Roslyn APIs
- Beveiliging
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>Releases

![:checkered_flag: Release: op donkergeel](./media/labels-projects/release.png "Voorvoegsel voor releaselabels")

Problemen met een label voor een specifieke release worden vermeld met het voorvoegsel `:checkered_flag: Release:` en hebben een donkergele achtergrond.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Prioriteit

Prioritaire labels worden alle `P` gevolgd door één cijfer. Lagere waarden geven een hogere prioriteit aan:

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>Hoe zit het met de andere labels?

Er zijn veel andere labels waarmee de inhoudsteams verschillende classificaties van problemen beheren. Als u geen lid bent van het inhoudsteam, kunt u deze labels negeren.

## <a name="projects"></a>Projecten

We gebruiken projecten op twee manieren:

- Month YYYY-projecttypen: Dit zijn scrumborden voor het maandelijkse werkplan.
- Langlopende EPICS: Deze worden gebruikt om taken doelgericht te organiseren, wanneer het werk wordt uitgevoerd over meerdere maanden.
