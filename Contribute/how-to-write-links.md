---
title: Koppelingen in documentatie gebruiken
description: Dit artikel biedt ondersteuning voor het maken van koppelingen naar inhoud in docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: 94ba4cefd9aff70b38502aa397a3761127c8089f
ms.sourcegitcommit: 9852045bac75fd5d90c0ffc88d2a17dd45ba015f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/19/2020
ms.locfileid: "85107109"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="a8c56-103">Koppelingen in documentatie gebruiken</span><span class="sxs-lookup"><span data-stu-id="a8c56-103">Use links in documentation</span></span>

<span data-ttu-id="a8c56-104">In dit artikel wordt beschreven hoe u hyperlinks gebruikt van pagina's die op docs.microsoft.com worden gehost.</span><span class="sxs-lookup"><span data-stu-id="a8c56-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="a8c56-105">Koppelingen kunnen eenvoudig in Markdown worden toegevoegd, met een aantal afwijkende conventies.</span><span class="sxs-lookup"><span data-stu-id="a8c56-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="a8c56-106">Koppelingen verwijzen gebruikers naar inhoud op dezelfde pagina, op omliggende pagina's of op externe websites en URL's.</span><span class="sxs-lookup"><span data-stu-id="a8c56-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="a8c56-107">De back-end van docs.microsoft.com gebruikt Open Publishing Services (OPS), dat ondersteuning biedt voor Markdown die compatibel is met [CommonMark][] en is geparseerd via de parseerengine [Markdig][].</span><span class="sxs-lookup"><span data-stu-id="a8c56-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="a8c56-108">Deze Markdown-variant is meestal geschikt voor [GitHub Flavored Markdown (GFM)][GFM], aangezien de meeste docs worden bewaard in GitHub en daar kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="a8c56-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="a8c56-109">Er wordt aanvullende functionaliteit toegevoegd met Markdown-extensies.</span><span class="sxs-lookup"><span data-stu-id="a8c56-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8c56-110">Alle koppelingen moeten zijn beveiligd (`https` vs. `http`) wanneer het doel dit ondersteunt (dit zou voor de grote meerderheid moeten gelden).</span><span class="sxs-lookup"><span data-stu-id="a8c56-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="a8c56-111">Tekst van koppeling</span><span class="sxs-lookup"><span data-stu-id="a8c56-111">Link text</span></span>

<span data-ttu-id="a8c56-112">De woorden die u gebruikt in de tekst van de koppeling moeten duidelijk de bestemming van de koppeling aangeven.</span><span class="sxs-lookup"><span data-stu-id="a8c56-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="a8c56-113">Gebruik dus normale beschrijvende tekst of de titel van de pagina die u wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8c56-114">Gebruik niet 'klik hier'.</span><span class="sxs-lookup"><span data-stu-id="a8c56-114">Do not use "click here."</span></span> <span data-ttu-id="a8c56-115">Het is nadelig voor de zoekmachineoptimalisatie en geeft geen goede beschrijving van het doelobject.</span><span class="sxs-lookup"><span data-stu-id="a8c56-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="a8c56-116">**Goed:**</span><span class="sxs-lookup"><span data-stu-id="a8c56-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="a8c56-117">**Fout:**</span><span class="sxs-lookup"><span data-stu-id="a8c56-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="a8c56-118">Koppelingen van het ene artikel naar het andere</span><span class="sxs-lookup"><span data-stu-id="a8c56-118">Links from one article to another</span></span>

<span data-ttu-id="a8c56-119">Er zijn twee typen hyperlinks die worden ondersteund door het publicatie systeem: **URL's** en **bestandskoppelingen**.</span><span class="sxs-lookup"><span data-stu-id="a8c56-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="a8c56-120">Een URL-koppeling kan een URL-pad zijn dat relatief is ten opzichte van de hoofdmap van docs.microsoft.com of een absolute URL die de volledige URL-syntaxis bevat (bijvoorbeeld `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span><span class="sxs-lookup"><span data-stu-id="a8c56-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="a8c56-121">Gebruik URL-koppelingen wanneer u een koppeling maakt naar inhoud buiten de huidige _docset_ of tussen automatisch gegenereerde naslaginformatie en conceptuele artikelen in de docset.</span><span class="sxs-lookup"><span data-stu-id="a8c56-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="a8c56-122">De eenvoudigste manier om een relatieve koppeling te maken, is door de URL te kopiëren uit uw browser en vervolgens `https://docs.microsoft.com/en-us` te verwijderen uit de waarde die u in Markdown hebt geplakt.</span><span class="sxs-lookup"><span data-stu-id="a8c56-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="a8c56-123">Neem geen landinstellingen op in URL's voor Microsoft-eigenschappen (u kunt bijvoorbeeld '/en-us' uit de URL verwijderen).</span><span class="sxs-lookup"><span data-stu-id="a8c56-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="a8c56-124">Een bestandskoppeling wordt gebruikt om een koppeling te maken van het ene naar het andere artikel binnen de docset.</span><span class="sxs-lookup"><span data-stu-id="a8c56-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="a8c56-125">Alle bestandspaden gebruiken tekens die gebruikmaken van slash- (`/`) in plaats van backslash-tekens.</span><span class="sxs-lookup"><span data-stu-id="a8c56-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="a8c56-126">Een artikel wordt gekoppeld aan een ander artikel in dezelfde map:</span><span class="sxs-lookup"><span data-stu-id="a8c56-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="a8c56-127">Een artikel wordt gekoppeld aan een artikel in de bovenliggende map van de huidige map:</span><span class="sxs-lookup"><span data-stu-id="a8c56-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="a8c56-128">Een artikel wordt gekoppeld aan een artikel in een submap van de huidige map:</span><span class="sxs-lookup"><span data-stu-id="a8c56-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="a8c56-129">Een artikel wordt gekoppeld aan een artikel in een submap van de bovenliggende map van de huidige map:</span><span class="sxs-lookup"><span data-stu-id="a8c56-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="a8c56-130">Geen van de eerder genoemde voorbeelden gebruikt de `~/` als onderdeel van de koppeling.</span><span class="sxs-lookup"><span data-stu-id="a8c56-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="a8c56-131">Als u een koppeling wilt maken naar een absoluut pad dat bij de hoofdmap van de opslagplaats begint, begint u de koppeling met `/`.</span><span class="sxs-lookup"><span data-stu-id="a8c56-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="a8c56-132">Als u de `~/` opneemt, worden de koppelingen ongeldig als er wordt verwezen naar bronopslagplaatsen in GitHub.</span><span class="sxs-lookup"><span data-stu-id="a8c56-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="a8c56-133">Als u het pad begint met `/`, wordt het correct omgezet.</span><span class="sxs-lookup"><span data-stu-id="a8c56-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="a8c56-134">Structuur van koppelingen op docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a8c56-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="a8c56-135">Inhoud die is gepubliceerd op docs.microsoft.com heeft de volgende URL-structuur:</span><span class="sxs-lookup"><span data-stu-id="a8c56-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="a8c56-136">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="a8c56-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="a8c56-137">`<locale>` -geeft de taal van het artikel weer (bijvoorbeeld: en-us of de-de)</span><span class="sxs-lookup"><span data-stu-id="a8c56-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="a8c56-138">`<product-service>` -de naam van het product of de service (bijvoorbeeld: powershell, dotnet, of azure)</span><span class="sxs-lookup"><span data-stu-id="a8c56-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="a8c56-139">`[<feature-service>]` -(optioneel) de naam van de functie of subservice van het product (bijvoorbeeld: csharp of load balancer)</span><span class="sxs-lookup"><span data-stu-id="a8c56-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="a8c56-140">`[<subfolder>]` -(optioneel) de naam van een submap binnen een functie</span><span class="sxs-lookup"><span data-stu-id="a8c56-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="a8c56-141">`<topic>` -de naam van het artikelbestand voor het onderwerp (bijvoorbeeld: load balancer-overzicht of overzicht)</span><span class="sxs-lookup"><span data-stu-id="a8c56-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="a8c56-142">`[?view=\<view-name>]` -(optioneel) de weergavenaam die wordt gebruikt door de versieselector voor inhoud met meerdere beschikbare versies (bijvoorbeeld: azps-3.5.0)</span><span class="sxs-lookup"><span data-stu-id="a8c56-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="a8c56-143">Artikelen in dezelfde _docset_ bevatten in de meeste gevallen hetzelfde URL-fragment `<product-service>`.</span><span class="sxs-lookup"><span data-stu-id="a8c56-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="a8c56-144">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="a8c56-144">For example:</span></span>
> - <span data-ttu-id="a8c56-145">Dezelfde docset</span><span class="sxs-lookup"><span data-stu-id="a8c56-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="a8c56-146">Verschillende docset</span><span class="sxs-lookup"><span data-stu-id="a8c56-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="a8c56-147">Bladwijzerkoppelingen</span><span class="sxs-lookup"><span data-stu-id="a8c56-147">Bookmark links</span></span>

<span data-ttu-id="a8c56-148">Als u een bladwijzerkoppeling wilt maken naar een kop in het *huidige* bestand, gebruikt u een hash-symbool gevolgd door de kop in kleine letters.</span><span class="sxs-lookup"><span data-stu-id="a8c56-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="a8c56-149">Verwijder leestekens uit de kop en vervang spaties door streepjes:</span><span class="sxs-lookup"><span data-stu-id="a8c56-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="a8c56-150">Als u wilt koppelen naar een bladwijzerkop in een ander artikel, gebruikt u de koppeling ten opzichte van het bestand of de site plus een hash-symbool, gevolgd door de woorden van de kop.</span><span class="sxs-lookup"><span data-stu-id="a8c56-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="a8c56-151">Verwijder leestekens uit de kop en vervang spaties door streepjes:</span><span class="sxs-lookup"><span data-stu-id="a8c56-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="a8c56-152">U kunt ook de bladwijzerkoppeling uit de URL kopiëren.</span><span class="sxs-lookup"><span data-stu-id="a8c56-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="a8c56-153">Als u de URL wilt vinden, beweegt u de muisaanwijzer over de kopregel op docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a8c56-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="a8c56-154">Er wordt nu een koppelingspictogram weergegeven:</span><span class="sxs-lookup"><span data-stu-id="a8c56-154">You should see a link icon appear:</span></span>

![Koppelingspictogram in artikelkop](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="a8c56-156">Klik op het koppelingspictogram en kopieer vervolgens de ankertekst van de bladwijzer uit de URL (dat wil zeggen, het deel na de hash).</span><span class="sxs-lookup"><span data-stu-id="a8c56-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="a8c56-157">De Docs-extensie bevat ook hulpprogramma's om koppelingen te maken.</span><span class="sxs-lookup"><span data-stu-id="a8c56-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="a8c56-158">Expliciete ankerkoppelingen</span><span class="sxs-lookup"><span data-stu-id="a8c56-158">Explicit anchor links</span></span>

<span data-ttu-id="a8c56-159">De toevoeging van expliciete ankerkoppelingen via de HTML-tag `<a>` is niet vereist of aanbevolen, behalve in hub- en landingspagina's.</span><span class="sxs-lookup"><span data-stu-id="a8c56-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="a8c56-160">Gebruik in plaats daarvan de automatisch gegenereerde bladwijzers zoals beschreven in [bladwijzerkoppelingen](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="a8c56-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="a8c56-161">Geef als volgt ankers op voor hub- en landingspagina's:</span><span class="sxs-lookup"><span data-stu-id="a8c56-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="a8c56-162">of</span><span class="sxs-lookup"><span data-stu-id="a8c56-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="a8c56-163">En geef het volgende op om een koppeling naar het anker te maken:</span><span class="sxs-lookup"><span data-stu-id="a8c56-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="a8c56-164">Ankertekst moet altijd uit kleine letters bestaan en mag geen spaties bevatten.</span><span class="sxs-lookup"><span data-stu-id="a8c56-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="a8c56-165">XRef-koppelingen (kruisverwijzing)</span><span class="sxs-lookup"><span data-stu-id="a8c56-165">XRef (cross reference) links</span></span>

<span data-ttu-id="a8c56-166">XRef-koppelingen zijn de aanbevolen manier om een koppeling naar API's te maken, omdat ze tijdens het bouwen worden gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="a8c56-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="a8c56-167">Als u in de huidige docset of andere docsets een koppeling wilt maken naar automatisch gegenereerde pagina's met API-naslaginformatie, gebruikt u XRef-koppelingen met de unieke id ([UID](#determine-the-uid)) van het type of lid.</span><span class="sxs-lookup"><span data-stu-id="a8c56-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="a8c56-168">U kunt de [Docs Markdown-extensie voor VS Code][docsextension] (onderdeel van het Docs Authoring Pack) gebruiken om .NET XRref-koppelingen in te voegen die worden weergegeven in de [.NET API-browser][].</span><span class="sxs-lookup"><span data-stu-id="a8c56-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="a8c56-169">Controleer of de API waarnaar u een koppeling wilt maken zich op [docs.microsoft.com][docs] bevindt, door alle of een deel van de volledige naam in het zoekvak van de [.NET API-browser][] of [Windows UWP][] te typen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="a8c56-170">Als er geen resultaten worden weergegeven, is het type nog niet aanwezig op docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a8c56-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="a8c56-171">Voor de syntaxis hebt u de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="a8c56-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="a8c56-172">Automatische koppelingen:</span><span class="sxs-lookup"><span data-stu-id="a8c56-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="a8c56-173">Standaard toont de koppelingstekst alleen de naam van het lid of het type.</span><span class="sxs-lookup"><span data-stu-id="a8c56-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="a8c56-174">De optionele queryparameter `displayProperty=nameWithType` genereert een volledig gekwalificeerde koppelingstekst, dat wil zeggen, **naamruimte.type** voor typen en **type.lid** voor typeleden, inclusief opsommingstypeleden.</span><span class="sxs-lookup"><span data-stu-id="a8c56-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="a8c56-175">Koppelingen in de Markdown-stijl:</span><span class="sxs-lookup"><span data-stu-id="a8c56-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="a8c56-176">Gebruik koppelingen in de Markdown-stijl voor XRef als u de tekst van de koppeling wilt aanpassen die wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a8c56-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="a8c56-177">Voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="a8c56-177">Examples:</span></span>

- <span data-ttu-id="a8c56-178">**\<xref:System.String>** wordt weergegeven als <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="a8c56-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="a8c56-179">**\<xref:System.String?displayProperty=nameWithType>** wordt weergegeven als <xref:System.String?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="a8c56-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="a8c56-180">**\[String class](xref:System.String)** weergegeven als [String class](xref:System.String).</span><span class="sxs-lookup"><span data-stu-id="a8c56-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="a8c56-181">De queryparameter `displayProperty=fullName` werkt op dezelfde manier als `displayProperty=nameWithType` voor klassen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="a8c56-182">Dat wil zeggen dat de koppelingstekst **naamruimte.klassenaam** wordt.</span><span class="sxs-lookup"><span data-stu-id="a8c56-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="a8c56-183">De koppelingstekst wordt voor leden echter weergegeven als **naamruimte.klassenaam.lidnaam**, wat mogelijk niet gewenst is.</span><span class="sxs-lookup"><span data-stu-id="a8c56-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c56-184">UID's zijn hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="a8c56-184">UIDs are case sensitive.</span></span> <span data-ttu-id="a8c56-185">`<xref:System.Object>` wordt bijvoorbeeld correct omgezet, maar `<xref:system.object>` niet.</span><span class="sxs-lookup"><span data-stu-id="a8c56-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="a8c56-186">Waarschuwingen voor XRef-builds en incrementele builds</span><span class="sxs-lookup"><span data-stu-id="a8c56-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="a8c56-187">In een incrementele build worden alleen bestanden gecompileerd die zijn gewijzigd of waarvoor een wijziging is aangebracht.</span><span class="sxs-lookup"><span data-stu-id="a8c56-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="a8c56-188">Als er een build-waarschuwing over een ongeldige XRef-koppeling wordt weergegeven, maar de koppeling wel geldig is, kan dit zijn omdat de build incrementeel is.</span><span class="sxs-lookup"><span data-stu-id="a8c56-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="a8c56-189">Het bestand dat de waarschuwing veroorzaakt, is niet gewijzigd, dus is deze niet gecompileerd en worden eerdere waarschuwingen opnieuw afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="a8c56-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="a8c56-190">De waarschuwing verdwijnt wanneer het bestand wordt gewijzigd of als u een volledige build activeert (u kunt een volledige build starten op ops.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a8c56-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="a8c56-191">Dit is een nadeel van incrementele builds, omdat DocFX geen gegevensupdate kan detecteren in de XRef-service.</span><span class="sxs-lookup"><span data-stu-id="a8c56-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="a8c56-192">De UID bepalen</span><span class="sxs-lookup"><span data-stu-id="a8c56-192">Determine the UID</span></span>

<span data-ttu-id="a8c56-193">De UID is doorgaans gelijk de volledig gekwalificeerde klasse- of lidnaam.</span><span class="sxs-lookup"><span data-stu-id="a8c56-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="a8c56-194">Er zijn ten minste twee manieren om de UID te bepalen:</span><span class="sxs-lookup"><span data-stu-id="a8c56-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="a8c56-195">Klik met de rechtermuisknop op de pagina [Docs][docs] voor een type of lid, selecteer **Bron weergeven** en kopieer vervolgens de waarde voor **Inhoud** voor **ms.assetid**:</span><span class="sxs-lookup"><span data-stu-id="a8c56-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![ms.assetid in de bron voor webpagina](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="a8c56-197">Gebruik de [site voor automatisch aanvullen][] door een deel van of de volledige naam van het type aan de URL toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="a8c56-198">Als u bijvoorbeeld `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in de adresbalk van uw browser invoert, worden alle typen en methoden weergegeven die **WriteLine** in hun naam bevatten, samen met de bijbehorende UID.</span><span class="sxs-lookup"><span data-stu-id="a8c56-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="a8c56-199">De UID verifiëren</span><span class="sxs-lookup"><span data-stu-id="a8c56-199">Verify the UID</span></span>

<span data-ttu-id="a8c56-200">Als u wilt testen of u de juiste UID hebt, vervangt u **System.String** in de volgende URL door uw UID en plakt u deze in de adresbalk van een browser:</span><span class="sxs-lookup"><span data-stu-id="a8c56-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="a8c56-201">De UID in de URL is hoofdlettergevoelig, en als u een UID voor een overbelasting van een methode controleert, moet u geen spaties tussen de parametertypen opnemen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="a8c56-202">Als u een van de volgende items ziet, hebt u de juiste UID:</span><span class="sxs-lookup"><span data-stu-id="a8c56-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="a8c56-203">Als alleen `[]` op de pagina worden weergegeven, hebt u de verkeerde UID.</span><span class="sxs-lookup"><span data-stu-id="a8c56-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="a8c56-204">Percentagecodering van URL's</span><span class="sxs-lookup"><span data-stu-id="a8c56-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="a8c56-205">Speciale tekens in de UID moeten de volgende HTML-codering hebben:</span><span class="sxs-lookup"><span data-stu-id="a8c56-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="a8c56-206">Teken</span><span class="sxs-lookup"><span data-stu-id="a8c56-206">Character</span></span> | <span data-ttu-id="a8c56-207">HTML-codering</span><span class="sxs-lookup"><span data-stu-id="a8c56-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="a8c56-208">%60</span><span class="sxs-lookup"><span data-stu-id="a8c56-208">%60</span></span>           |
| `#`       | <span data-ttu-id="a8c56-209">%23</span><span class="sxs-lookup"><span data-stu-id="a8c56-209">%23</span></span>           |
| `*`       | <span data-ttu-id="a8c56-210">%2A</span><span class="sxs-lookup"><span data-stu-id="a8c56-210">%2A</span></span>           |

<span data-ttu-id="a8c56-211">Bekijk een volledige lijst met [percentagecodes](https://en.wikipedia.org/wiki/Percent-encoding).</span><span class="sxs-lookup"><span data-stu-id="a8c56-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="a8c56-212">Voorbeelden van codering:</span><span class="sxs-lookup"><span data-stu-id="a8c56-212">Encoding examples:</span></span>

- <span data-ttu-id="a8c56-213">``System.Threading.Tasks.Task`1`` wordt als `System.Threading.Tasks.Task%601` gecodeerd (zie sectie [ over algemene typen](#generic-types))</span><span class="sxs-lookup"><span data-stu-id="a8c56-213">``System.Threading.Tasks.Task`1`` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="a8c56-214">`System.Exception.#ctor` wordt gecodeerd als `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="a8c56-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="a8c56-215">`System.Object.Equals*` wordt gecodeerd als `System.Object.Equals%2A`</span><span class="sxs-lookup"><span data-stu-id="a8c56-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="a8c56-216">Algemene typen</span><span class="sxs-lookup"><span data-stu-id="a8c56-216">Generic types</span></span>

<span data-ttu-id="a8c56-217">Algemene typen zijn typen als `System.Collections.Generic.List<T>`.</span><span class="sxs-lookup"><span data-stu-id="a8c56-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="a8c56-218">Als u naar dit type bladert in de [.NET API-browser](https://docs.microsoft.com/dotnet/api/) en de bijbehorende URL bekijkt, ziet u dat `<T>` als `-1` is geschreven in de URL, die in werkelijkheid staat voor **'1**:</span><span class="sxs-lookup"><span data-stu-id="a8c56-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="a8c56-219">Als u een koppeling wilt maken naar een algemeen type zoals **List\<T>** , codeert u het accent grave-teken **\`** als **%60**, zoals wordt weergegeven in het volgende voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="a8c56-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="a8c56-220">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8c56-220">Methods</span></span>

<span data-ttu-id="a8c56-221">Als u een koppeling wilt maken naar een methode, kunt u een koppeling maken naar de algemene methodenpagina door een sterretje (`*`) toe te voegen aan de naam van de methode of aan een specifieke overbelasting.</span><span class="sxs-lookup"><span data-stu-id="a8c56-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="a8c56-222">Gebruik bijvoorbeeld de algemene pagina wanneer u een koppeling wilt maken naar de methode `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` zonder specifieke parametertypen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="a8c56-223">Het sterretje wordt gecodeerd als `%2A`.</span><span class="sxs-lookup"><span data-stu-id="a8c56-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="a8c56-224">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="a8c56-224">For example:</span></span>

<span data-ttu-id="a8c56-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` vormt een koppeling naar <xref:System.Object.Equals%2A?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="a8c56-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="a8c56-226">Als u een koppeling wilt maken naar een specifieke overbelasting, voegt u haakjes achter de naam van de methode toe en voegt u de volledige typenaam van elke parameter toe.</span><span class="sxs-lookup"><span data-stu-id="a8c56-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="a8c56-227">Plaats geen spatie tussen de typenamen, anders werkt de koppeling niet.</span><span class="sxs-lookup"><span data-stu-id="a8c56-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="a8c56-228">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="a8c56-228">For example:</span></span>

<span data-ttu-id="a8c56-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` maakt een koppeling naar <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="a8c56-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="a8c56-230">Koppelingen vanuit Include-bestanden</span><span class="sxs-lookup"><span data-stu-id="a8c56-230">Links from includes</span></span>

<span data-ttu-id="a8c56-231">Omdat Include-bestanden deel uitmaken van een andere map moet u een langer relatief pad gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a8c56-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="a8c56-232">Gebruik de volgende notatie om vanuit een Include-bestand een koppeling naar een artikel te maken:</span><span class="sxs-lookup"><span data-stu-id="a8c56-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="a8c56-233">Met de [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)-extensie voor Visual Studio Code kunt u relatieve koppelingen en bladwijzers correct invoegen zonder dat u zich met paden bezig hoeft te houden.</span><span class="sxs-lookup"><span data-stu-id="a8c56-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="a8c56-234">Koppelingen in selectors</span><span class="sxs-lookup"><span data-stu-id="a8c56-234">Links in selectors</span></span>

<span data-ttu-id="a8c56-235">Een selector is een navigatieonderdeel dat als vervolgkeuzelijst in een docs-artikel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a8c56-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="a8c56-236">Als de lezer een waarde in de vervolgkeuzelijst selecteert, wordt het geselecteerde artikel geopend in de browser.</span><span class="sxs-lookup"><span data-stu-id="a8c56-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="a8c56-237">De selectorlijst bevat gewoonlijk koppelingen naar nauw verwante artikelen, bijvoorbeeld over hetzelfde onderwerp in meerdere programmeertalen, of naar een reeks nauw verwante artikelen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="a8c56-238">Als u met selectors werkt die zijn opgenomen in een Include-bestand, gebruikt u de volgende koppelingsstructuur:</span><span class="sxs-lookup"><span data-stu-id="a8c56-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="a8c56-239">Koppelingen met verwijzingen</span><span class="sxs-lookup"><span data-stu-id="a8c56-239">Reference-style links</span></span>

<span data-ttu-id="a8c56-240">U kunt koppelingen met verwijzingen gebruiken zodat uw broninhoud gemakkelijker te lezen is.</span><span class="sxs-lookup"><span data-stu-id="a8c56-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="a8c56-241">Bij koppelingen met verwijzingen wordt de syntaxis voor de inlinekoppeling vervangen door een eenvoudige syntaxis en kunnen de lange URL's naar het einde van het artikel worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="a8c56-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="a8c56-242">Hier volgt het voorbeeld van [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="a8c56-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="a8c56-243">Inlinetekst:</span><span class="sxs-lookup"><span data-stu-id="a8c56-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="a8c56-244">Koppelingsverwijzingen aan het einde van het artikel:</span><span class="sxs-lookup"><span data-stu-id="a8c56-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="a8c56-245">Zorg ervoor dat u een spatie typt tussen de dubbele punt en de koppeling.</span><span class="sxs-lookup"><span data-stu-id="a8c56-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="a8c56-246">Als u de spatie vergeet bij het maken van een koppeling naar andere technische artikelen, werkt de koppeling niet meer in het gepubliceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="a8c56-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="a8c56-247">Een koppeling maken naar pagina's die geen deel uitmaken van de technische documentatie</span><span class="sxs-lookup"><span data-stu-id="a8c56-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="a8c56-248">Als u een koppeling wilt maken naar een pagina in een ander Microsoft-domein (zoals de pagina met prijzen, de SLA-pagina of naar iets dat geen documentatieartikel is), gebruikt u een absolute URL, maar laat u de landcode achterwege.</span><span class="sxs-lookup"><span data-stu-id="a8c56-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="a8c56-249">Het doel hier is dat de koppelingen werken in GitHub en op de weergegeven site:</span><span class="sxs-lookup"><span data-stu-id="a8c56-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="a8c56-250">Een koppeling maken naar sites van derden</span><span class="sxs-lookup"><span data-stu-id="a8c56-250">Links to third-party sites</span></span>

<span data-ttu-id="a8c56-251">Het beste kunt u gebruikers zo weinig mogelijk doorsturen naar andere sites.</span><span class="sxs-lookup"><span data-stu-id="a8c56-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="a8c56-252">Soms is het echter nodig. Houd in die gevallen rekening met de volgende informatie wanneer u een koppeling maakt naar sites van derden:</span><span class="sxs-lookup"><span data-stu-id="a8c56-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="a8c56-253">**Verantwoordelijkheden**: Maak een koppeling naar de inhoud van een derde partij als u informatie van deze partij wilt delen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="a8c56-254">Het is bijvoorbeeld niet de taak van Microsoft om mensen te vertellen hoe ze Android-ontwikkeltools moeten gebruiken. Dat is namelijk de taak van Google.</span><span class="sxs-lookup"><span data-stu-id="a8c56-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="a8c56-255">We kunnen eventueel wel uitleggen hoe Android-ontwikkeltools moeten worden gebruikt *met* Azure, maar het is aan Google om te vertellen hoe hun eigen tools moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a8c56-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="a8c56-256">**Aftekening door PM**: Geef aan dat Microsoft moet aftekenen op inhoud van derden.</span><span class="sxs-lookup"><span data-stu-id="a8c56-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="a8c56-257">Door een koppeling te maken, zeggen we iets over ons vertrouwen in die inhoud en onze verplichtingen als mensen de instructies volgen</span><span class="sxs-lookup"><span data-stu-id="a8c56-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="a8c56-258">**Controle van de nieuwheid**: Controleer of de inhoud van de derde partij nog steeds actueel, correct en relevant is en of de koppeling niet is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="a8c56-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="a8c56-259">**Offsite**: Zorg ervoor dat gebruikers er zich van bewust zijn dat ze naar een andere site gaan.</span><span class="sxs-lookup"><span data-stu-id="a8c56-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="a8c56-260">Als dat niet blijkt uit de context, maakt u dat met een aparte zin duidelijk. Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="a8c56-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="a8c56-261">Bijvoorbeeld: "Tot de vereisten behoren ook de Android-ontwikkelhulpprogramma's, die u kunt downloaden op de Android Studio-site."</span><span class="sxs-lookup"><span data-stu-id="a8c56-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="a8c56-262">**Volgende stappen**: Het is prima om een koppeling te maken naar, bijvoorbeeld, een MVP-blog in de sectie Volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="a8c56-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="a8c56-263">Maar nogmaals, wijs de gebruikers erop dat ze de site verlaten.</span><span class="sxs-lookup"><span data-stu-id="a8c56-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="a8c56-264">**Juridisch**: We kunnen een beroep doen op de juridisch bindende bepalingen onder **Koppelingen naar de sites van derden** in de voettekst **Gebruiksvoorwaarden** op elke microsoft.com-pagina.</span><span class="sxs-lookup"><span data-stu-id="a8c56-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API-browser]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[site voor automatisch aanvullen]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
