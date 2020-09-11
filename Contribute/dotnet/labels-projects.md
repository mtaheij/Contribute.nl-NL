---
title: Roadmap voor labels, projecten en mijlpalen
description: In dit artikel wordt uitgelegd hoe labels, projecten en mijlpalen worden gebruikt in de dotnet/docs-opslagplaats.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: b8e9f2a33f9b4a8025aa36a890bff1017cf132c6
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559258"
---
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="c8e7a-103">Roadmap voor labels, projecten en mijlpalen</span><span class="sxs-lookup"><span data-stu-id="c8e7a-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="c8e7a-104">Het team voor .NET-docs maakt uitgebreid gebruik van [GitHub-labels](https://github.com/dotnet/docs/labels) om ons werk te organiseren.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="c8e7a-105">Door te filteren op combinaties van labels kunnen we ons snel richten op gedeelten van belang op de website van [.NET docs](https://docs.microsoft.com/dotnet).</span><span class="sxs-lookup"><span data-stu-id="c8e7a-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="c8e7a-106">We kunnen bijvoorbeeld alle open `P1`-problemen met prioriteit één openen met een query bij [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span><span class="sxs-lookup"><span data-stu-id="c8e7a-106">For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span></span>

<span data-ttu-id="c8e7a-107">We gebruiken [GitHub-projecten](https://github.com/dotnet/docs/projects) om sprints en andere doelgerichte EPICS te organiseren.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="c8e7a-108">We gebruiken ook [GitHub-mijlpalen](https://github.com/dotnet/docs/milestones) om het werk bij te houden.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="c8e7a-109">Het beste is om projecten te zien voor planning (problemen) en mijlpalen voor werk (pull-aanvragen).</span><span class="sxs-lookup"><span data-stu-id="c8e7a-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="c8e7a-110">Deze roadmap biedt uitleg over hoe we deze organisatieprogramma's gebruiken en beschikt over koppelingen naar handige filters waarmee we interessegebieden kunnen vinden.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="c8e7a-111">Labels</span><span class="sxs-lookup"><span data-stu-id="c8e7a-111">Labels</span></span>

<span data-ttu-id="c8e7a-112">Begin, als dit de eerste keer is dat u een bijdrage levert aan [dotnet/docs](https://github.com/dotnet/docs), met de [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-problemen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="c8e7a-113">Dit zijn problemen met een meer gericht bereik.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="c8e7a-114">Deze zijn een uitstekende manier om uw eerste bijdrage te maken.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="c8e7a-115">Vanuit de up-for-grabs-weergave kunt u problemen verder filteren op basis van gebieden en prioriteit.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="c8e7a-116">Er zijn goede problemen gevonden voor beginners met een [goed-eerste-probleem](https://github.com/dotnet/docs/labels/good-first-issue) als u eerst een kleinere bijdrage wilt proberen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="c8e7a-117">We gebruiken labels om op verschillende manieren problemen te classificeren:</span><span class="sxs-lookup"><span data-stu-id="c8e7a-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="c8e7a-118">[.NET-gidsen](#find-a-single-net-guide) en [gedeelten van een gids](#search-one-section-of-a-guide).</span><span class="sxs-lookup"><span data-stu-id="c8e7a-118">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="c8e7a-119">Doelrelease</span><span class="sxs-lookup"><span data-stu-id="c8e7a-119">Target release</span></span>](#releases)
- [<span data-ttu-id="c8e7a-120">Priority</span><span class="sxs-lookup"><span data-stu-id="c8e7a-120">Priority</span></span>](#priority)

<span data-ttu-id="c8e7a-121">U kunt een label van elke set (gids, release, prioriteit) combineren om voor een beperkte focus te zorgen waarmee u problemen kunt vinden waaraan u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="c8e7a-122">Eén .NET-gids zoeken</span><span class="sxs-lookup"><span data-stu-id="c8e7a-122">Find a single .NET guide</span></span>

<span data-ttu-id="c8e7a-123">We gebruiken labels voor alle e-books over architectuur en voor elke .NET-gids.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="c8e7a-124">![:book: gids op lichtgroene achtergrond](./media/labels-projects/guide.png "Voorvoegsel voor labels voor architectuurgidsen")</span><span class="sxs-lookup"><span data-stu-id="c8e7a-124">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="c8e7a-125">De e-books over architectuur worden aangeduid met het voorvoegsel `:book: guide` en hebben een lichtgroene achtergrond.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-125">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="c8e7a-126">Dit zijn de gebieden in lange vorm die over aanbevolen architectuur handelen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-126">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="c8e7a-127">Hier worden actuele problemen gefilterd voor alle .NET-gidsen over architectuur.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-127">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="c8e7a-128">ASP.NET Core web apps</span><span class="sxs-lookup"><span data-stu-id="c8e7a-128">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="c8e7a-129">Blazor</span><span class="sxs-lookup"><span data-stu-id="c8e7a-129">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="c8e7a-130">Cloud Native</span><span class="sxs-lookup"><span data-stu-id="c8e7a-130">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="c8e7a-131">Docker lifecycle</span><span class="sxs-lookup"><span data-stu-id="c8e7a-131">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="c8e7a-132">gRPC</span><span class="sxs-lookup"><span data-stu-id="c8e7a-132">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="c8e7a-133">Modernizing w/ Windows containers</span><span class="sxs-lookup"><span data-stu-id="c8e7a-133">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="c8e7a-134">.NET Microservices</span><span class="sxs-lookup"><span data-stu-id="c8e7a-134">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="c8e7a-135">Serverloze apps</span><span class="sxs-lookup"><span data-stu-id="c8e7a-135">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="c8e7a-136">Deze labelstijl wordt ook toegepast op de [ontwerprichtlijnen van Framework](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span><span class="sxs-lookup"><span data-stu-id="c8e7a-136">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="c8e7a-137">Dit gebied heeft hetzelfde labelontwerp, maar pull-aanvragen van de community worden afgeraden.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-137">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="c8e7a-138">Dit materiaal wordt herdrukt met toestemming en mag niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-138">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="c8e7a-139">![:books: Gebied op donkerblauwe achtergrond](./media/labels-projects/area.png "Voorvoegsel voor labels voor gebieden van .NET-gidsen")</span><span class="sxs-lookup"><span data-stu-id="c8e7a-139">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="c8e7a-140">Elke .NET-gids wordt vermeld met het voorvoegsel `:books: Area` en heeft een donkerblauwe achtergrond.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-140">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="c8e7a-141">Hier worden actuele problemen gefilterd voor alle .NET-gidsen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-141">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="c8e7a-142">Naslaginformatie voor API</span><span class="sxs-lookup"><span data-stu-id="c8e7a-142">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="c8e7a-143">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="c8e7a-143">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="c8e7a-144">C# Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-144">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="c8e7a-145">Desktop Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-145">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="c8e7a-146">F# Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-146">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="c8e7a-147">ML.NET Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-147">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="c8e7a-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - kan worden verwijderd</span><span class="sxs-lookup"><span data-stu-id="c8e7a-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="c8e7a-149">.NET Core Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-149">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="c8e7a-150">.NET for Apache Spark Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-150">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="c8e7a-151">.NET Framework Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-151">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="c8e7a-152">.NET Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-152">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="c8e7a-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - kan worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="c8e7a-154">Visual Basic Guide</span><span class="sxs-lookup"><span data-stu-id="c8e7a-154">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="c8e7a-155">Een gedeelte van een gids doorzoeken</span><span class="sxs-lookup"><span data-stu-id="c8e7a-155">Search one section of a guide</span></span>

<span data-ttu-id="c8e7a-156">![:card_file_box: Gebied op mediumblauwe achtergrond](./media/labels-projects/technology.png "Voorvoegsel voor labels voor subgebieden van .NET-gidsen")</span><span class="sxs-lookup"><span data-stu-id="c8e7a-156">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="c8e7a-157">De .NET-gidsen zijn groot, zodat deze labels het bereik verder beperken tot een gedeelte van een gids.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-157">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="c8e7a-158">Elk subgebied van een .NET-gids wordt vermeld met het voorvoegsel `:card_file_box: Technology` en heeft een mediumblauwe achtergrond.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-158">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="c8e7a-159">Veel van deze labels zijn van toepassing op meerdere gidsen, terwijl andere zich in slechts één gids bevinden.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-159">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="c8e7a-160">Nadat u hebt gefilterd op een gebied, voegt u een van deze labels toe om het bereik van problemen verder te beperken.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-160">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="c8e7a-161">AppCompat</span><span class="sxs-lookup"><span data-stu-id="c8e7a-161">AppCompat</span></span>
- <span data-ttu-id="c8e7a-162">Async Task</span><span class="sxs-lookup"><span data-stu-id="c8e7a-162">Async Task</span></span>
- <span data-ttu-id="c8e7a-163">C# Advanced concepts</span><span class="sxs-lookup"><span data-stu-id="c8e7a-163">C# Advanced concepts</span></span>
- <span data-ttu-id="c8e7a-164">C# compiler</span><span class="sxs-lookup"><span data-stu-id="c8e7a-164">C# compiler</span></span>
- <span data-ttu-id="c8e7a-165">C# Fundamentals</span><span class="sxs-lookup"><span data-stu-id="c8e7a-165">C# Fundamentals</span></span>
- <span data-ttu-id="c8e7a-166">C# Get Started</span><span class="sxs-lookup"><span data-stu-id="c8e7a-166">C# Get Started</span></span>
- <span data-ttu-id="c8e7a-167">C# Language Reference</span><span class="sxs-lookup"><span data-stu-id="c8e7a-167">C# Language Reference</span></span>
- <span data-ttu-id="c8e7a-168">C# Null safety</span><span class="sxs-lookup"><span data-stu-id="c8e7a-168">C# Null safety</span></span>
- <span data-ttu-id="c8e7a-169">C# What's new</span><span class="sxs-lookup"><span data-stu-id="c8e7a-169">C# What's new</span></span>
- <span data-ttu-id="c8e7a-170">CLI</span><span class="sxs-lookup"><span data-stu-id="c8e7a-170">CLI</span></span>
- <span data-ttu-id="c8e7a-171">Data Access</span><span class="sxs-lookup"><span data-stu-id="c8e7a-171">Data Access</span></span>
- <span data-ttu-id="c8e7a-172">Docker</span><span class="sxs-lookup"><span data-stu-id="c8e7a-172">Docker</span></span>
- <span data-ttu-id="c8e7a-173">Installers</span><span class="sxs-lookup"><span data-stu-id="c8e7a-173">Installers</span></span>
- <span data-ttu-id="c8e7a-174">LINQ</span><span class="sxs-lookup"><span data-stu-id="c8e7a-174">LINQ</span></span>
- <span data-ttu-id="c8e7a-175">NCL</span><span class="sxs-lookup"><span data-stu-id="c8e7a-175">NCL</span></span>
- <span data-ttu-id="c8e7a-176">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="c8e7a-176">.NET Standard</span></span>
- <span data-ttu-id="c8e7a-177">Roslyn APIs</span><span class="sxs-lookup"><span data-stu-id="c8e7a-177">Roslyn APIs</span></span>
- <span data-ttu-id="c8e7a-178">Beveiliging</span><span class="sxs-lookup"><span data-stu-id="c8e7a-178">Security</span></span>
- <span data-ttu-id="c8e7a-179">WCF</span><span class="sxs-lookup"><span data-stu-id="c8e7a-179">WCF</span></span>
- <span data-ttu-id="c8e7a-180">WF</span><span class="sxs-lookup"><span data-stu-id="c8e7a-180">WF</span></span>
- <span data-ttu-id="c8e7a-181">WIF</span><span class="sxs-lookup"><span data-stu-id="c8e7a-181">WIF</span></span>
- <span data-ttu-id="c8e7a-182">WinForms</span><span class="sxs-lookup"><span data-stu-id="c8e7a-182">WinForms</span></span>
- <span data-ttu-id="c8e7a-183">WPF</span><span class="sxs-lookup"><span data-stu-id="c8e7a-183">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="c8e7a-184">Releases</span><span class="sxs-lookup"><span data-stu-id="c8e7a-184">Releases</span></span>

<span data-ttu-id="c8e7a-185">![:checkered_flag: Release: op donkergeel](./media/labels-projects/release.png "Voorvoegsel voor releaselabels")</span><span class="sxs-lookup"><span data-stu-id="c8e7a-185">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="c8e7a-186">Problemen met een label voor een specifieke release worden vermeld met het voorvoegsel `:checkered_flag: Release:` en hebben een donkergele achtergrond.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-186">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="c8e7a-187">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="c8e7a-187">.NET Core 2.2</span></span>
- <span data-ttu-id="c8e7a-188">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="c8e7a-188">.NET Core 3.0</span></span>
- <span data-ttu-id="c8e7a-189">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="c8e7a-189">.NET Framework 4.8</span></span>
- <span data-ttu-id="c8e7a-190">.NET 5</span><span class="sxs-lookup"><span data-stu-id="c8e7a-190">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="c8e7a-191">Prioriteit</span><span class="sxs-lookup"><span data-stu-id="c8e7a-191">Priority</span></span>

<span data-ttu-id="c8e7a-192">Prioritaire labels worden alle `P` gevolgd door één cijfer.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-192">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="c8e7a-193">Lagere waarden geven een hogere prioriteit aan:</span><span class="sxs-lookup"><span data-stu-id="c8e7a-193">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="c8e7a-194">P0 - Geeft problemen of pull-aanvragen weer met een kritieke prioriteit</span><span class="sxs-lookup"><span data-stu-id="c8e7a-194">P0 - Indicates issues or PRs that are critical priority</span></span>
- <span data-ttu-id="c8e7a-195">P1 - Hoge prioriteit</span><span class="sxs-lookup"><span data-stu-id="c8e7a-195">P1 - High priority</span></span>
- <span data-ttu-id="c8e7a-196">P2 - Gemiddelde prioriteit</span><span class="sxs-lookup"><span data-stu-id="c8e7a-196">P2 - Medium priority</span></span>
- <span data-ttu-id="c8e7a-197">P3 - Lage prioriteit</span><span class="sxs-lookup"><span data-stu-id="c8e7a-197">P3 - Low priority</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="c8e7a-198">Hoe zit het met de andere labels?</span><span class="sxs-lookup"><span data-stu-id="c8e7a-198">What about the other labels</span></span>

<span data-ttu-id="c8e7a-199">Er zijn veel andere labels waarmee de inhoudsteams verschillende classificaties van problemen beheren.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-199">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="c8e7a-200">Als u geen lid bent van het inhoudsteam, kunt u deze labels negeren.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-200">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="c8e7a-201">Projecten</span><span class="sxs-lookup"><span data-stu-id="c8e7a-201">Projects</span></span>

<span data-ttu-id="c8e7a-202">Projecten zijn bedoeld voor planningsdoeleinden, waar werk met prioriteit wordt geautomatiseerd in een Kanbanbord.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-202">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="c8e7a-203">Projecten mogen altijd alleen GitHub-problemen bevatten, _geen_ pull-aanvragen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-203">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="c8e7a-204">Projecten verschillen van mijlpalen, omdat mijlpalen alleen pull-aanvragen kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-204">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="c8e7a-205">We gebruiken projecten op twee manieren:</span><span class="sxs-lookup"><span data-stu-id="c8e7a-205">We use projects in two ways:</span></span>

- <span data-ttu-id="c8e7a-206">`Month YYYY`-projecttypen: Dit zijn kanbanborden voor het maandelijkse werkplan.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-206">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="c8e7a-207">Voorbeelden, [juli 2020](https://github.com/dotnet/docs/projects/103), [augustus 2020](https://github.com/dotnet/docs/projects/117) enzovoorts.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-207">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="c8e7a-208">Langlopende EPICS: Deze worden gebruikt om taken doelgericht te organiseren, wanneer het werk wordt uitgevoerd over meerdere maanden.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-208">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="c8e7a-209">Voorbeelden: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106) enzovoorts.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-209">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="c8e7a-210">Mijlpalen</span><span class="sxs-lookup"><span data-stu-id="c8e7a-210">Milestones</span></span>

<span data-ttu-id="c8e7a-211">Mijlpalen volgen doorgaans dezelfde naamconventies van projecten `Month YYYY`, maar ze verschillen van projecten.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-211">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="c8e7a-212">We gebruiken mijlpalen om voltooid werk bij te houden.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-212">We use milestones to track completed work.</span></span> <span data-ttu-id="c8e7a-213">Mijlpalen mogen _geen_ problemen (mogelijk werk) bevatten, maar alleen pull-aanvragen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-213">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="c8e7a-214">De huidige mijlpaal wordt automatisch toegepast op nieuwe pull-aanvragen.</span><span class="sxs-lookup"><span data-stu-id="c8e7a-214">The current milestone is automatically applied to new pull requests.</span></span>
